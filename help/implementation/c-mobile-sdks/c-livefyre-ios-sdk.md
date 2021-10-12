---
description: 기본 iOS 앱에 Livefyre를 추가합니다.
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

기본 iOS 앱에 Livefyre를 추가합니다.

이 오픈 소스 라이브러리를 사용하여 Livefyre 서비스를 기본 iOS 앱에 통합합니다. Livefyre StreamHub iOS SDK는 뛰어난 AFNetworking 라이브러리를 기반으로 공통 API 메커니즘 주위에 씬 레이어를 제공합니다.

또한 Livefyre에서는 이 SDK를 기반으로 두 개의 iOS 샘플 앱을 제공합니다. 주석 스트림 및 검토 샘플 앱.

## 프로젝트에 SDK를 Cocoa Pod로 통합(권장) {#section_qc5_h3v_zz}

프로젝트에 StreamHub-iOS SDK를 추가하는 가장 편리한 방법은 CocoaPod를 사용하는 것입니다. CocoaPod가 없는 경우 gem install coapods 및 pod setup을 실행합니다. 다음은 Podfile의 예입니다.

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

CocoaPod 설치에 사양 리포지토리를 추가해야 합니다(이렇게 하면 `~/.cocoapods/repos` 디렉토리에 복제됨).

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

앱 프로젝트 루트에 Podfile이 생성되고 위의 저장소가 추가되면 다음을 실행합니다.

```
pod install
```

이렇게 하면 모든 종속성이 다운로드되고 MyApp.xcworkspace 파일이 만들어집니다. 이 파일은 지금부터 Xcode에서 앱 프로젝트를 여는 데 사용해야 합니다.

## Xcode 하위 프로젝트로 {#section_jcm_g3v_zz}

또는 리포지토리를 복제합니다.

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

그런 다음 Xcode 프로젝트(LFSClient.xcodeproj)를 하위 프로젝트로 앱에 추가합니다(LFSClient.xcodeproj 파일을 Xcode의 Project Navigator 창으로 쉽게 드래그하여 수행).

또한 종속성([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit))과 동일한 작업을 수행해야 합니다.

## 모든 항목을 한 번에 다운로드(권장되지 않음) {#section_rpb_f3v_zz}

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
>Xcode 6에서 테스트를 실행하려면 $(PLATFORM_DIR)/Developer/Library/Frameworks를 Pods-test-XCTest+OHHTTPStubeSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)에 FRAMEWORK_SEARCH_PATHS에 추가해야 합니다.

요청 시 Livefyre에서 제공하는 Livefyre의 LFSTestConfig.plist 파일이 필요합니다.

## Xcode 설명서 {#section_arl_b3v_zz}

[설명서](https://github.com/Livefyre/StreamHub-iOS-SDK)를 찾아보거나 Xcode에서 &quot;Documentation&quot; 타겟을 작성할 수 있습니다(appledoc를 설치해야 함).

## 요구 사항 {#section_m5l_13v_zz}

v0.2.0을 사용하려면 iOS 6.0 이상이 필요하므로 StreamHub iOS SDK 버전입니다.

## 부록(JSON 지원) {#section_pcd_5hv_zz}

StreamHub-iOS SDK 내역을 보는 사용자의 경우, 수정된 버전의 [JSONKit](https://github.com/escherba/JSONKit)을 기본 JSON 파서(Apple에서 제공한 NSJSONSerialization 대신)로 사용합니다. Apple에서 제공한 파서는 시스템에서 나타낼 수 있는 정수 또는 부동 소수점 번호가 들어 있는 JSON 파일 디코딩을 지원하지 않으므로 이 작업을 수행해야 했습니다. JSONKit의 수정된 버전은 예외를 throw하는 대신 해당 시스템 최대값으로 매우 큰 숫자를 자릅니다.
