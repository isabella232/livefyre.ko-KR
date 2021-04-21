---
description: 기본 iOS 앱에 Livefyre를 추가합니다.
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

기본 iOS 앱에 Livefyre를 추가합니다.

오픈 소스 라이브러리를 사용하여 Livefyre 서비스를 기본 iOS 앱으로 통합할 수 있습니다. Livefyre StreamHub iOS SDK는 뛰어난 AFNetworking 라이브러리를 기반으로, 일반적인 API 메커니즘 주위의 가상 레이어를 제공합니다.

또한 Livefyre는 이 SDK를 기반으로 2개의 iOS 샘플 앱을 제공합니다.주석 스트림 및 평가 샘플 앱.

## SDK를 Cocoa Pod(권장) {#section_qc5_h3v_zz}(으)로 프로젝트에 통합

프로젝트에 StreamHub-iOS SDK를 추가하는 가장 편리한 방법은 CocoaPod을 사용하는 것입니다. CocoaPod가 없는 경우 gem 설치 코드 및 창 설정을 실행하십시오. 다음은 포드파일의 예입니다.

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

또한 CocoaPod 설치에 사양 리포지토리를 추가해야 합니다(이렇게 하면 `~/.cocoapods/repos` 디렉토리로 복제됨).

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

앱 프로젝트 루트에 Podfile이 생성되어 위의 저장소가 추가되면 다음을 실행합니다.

```
pod install
```

모든 종속성을 다운로드하고 MyApp.xcworkspace 파일을 만듭니다. 이 파일을 지금부터 Xcode에서 앱 프로젝트를 열려면 사용해야 합니다.

## Xcode 하위 프로젝트 {#section_jcm_g3v_zz}

또는 저장소를 복제합니다.

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

그런 다음 Xcode 프로젝트(LFSClient.xcodeproj)를 하위 프로젝트로 추가합니다(LFSClient.xcodeproj 파일을 Xcode의 Project Navigator 창으로 손쉽게 드래그).

종속성([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit))과 동일한 작업을 수행해야 합니다.

## 한 번에 모든 것 다운로드(권장되지 않음) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Xcode 6에서 테스트를 실행하려면 Pods-test-XCTest+OHHTTPStubeSuiteCleanUp 창[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)에서 $(PLATFORM_DIR)/Developer/Library/Frameworks를 FRAMEWORK_SEARCH_PATHS에 추가해야 합니다.

요청 시 Livefyre가 제공하는 Livefyre의 LFSTestConfig.plist 파일이 필요합니다.

## Xcode 설명서 {#section_arl_b3v_zz}

[설명서](https://livefyre.github.com/StreamHub-iOS-SDK/)를 찾아보거나 Xcode에 &quot;문서&quot; 대상을 만들 수 있습니다(응용 프로그램을 설치해야 함).

## 요구 사항 {#section_m5l_13v_zz}

v0.2.0을 사용하려면 iOS 6.0 이상이 필요하므로 StreamHub iOS SDK 버전이 필요합니다.

## 부록(JSON 지원) {#section_pcd_5hv_zz}

StreamHub-iOS SDK 내실을 보는 사용자의 경우, 수정된 버전의 [JSONKit](https://github.com/escherba/JSONKit)을 기본 JSON 파서(Apple 제공 NSJSONSerialization 대신)로 사용합니다. Apple 제공 구문 분석기는 시스템에서 표현할 수 있는 정수 또는 부동 소수점 번호가 포함된 JSON 파일 디코딩을 지원하지 않으므로 이 작업을 수행해야 했습니다. JSONKit의 수정된 버전은 예외를 발생시키지 않고 해당 시스템 최대값에 매우 큰 수를 자릅니다.
