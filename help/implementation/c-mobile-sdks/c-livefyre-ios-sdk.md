---
description: 기본 iOS 앱에 Livefyre 추가
seo-description: 기본 iOS 앱에 Livefyre 추가
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

기본 iOS 앱에 Livefyre 추가

이 오픈 소스 라이브러리를 사용하여 Livefyre 서비스를 기본 iOS 앱에 통합할 수 있습니다. Livefyre StreamHub iOS SDK 파섹

또한 Livefyre는 이 SDK를 기반으로 하는 두 개의 iOS 샘플 앱을 제공합니다.댓글 스트림 및 평가 샘플 앱.

## SDK를 Cocoa Pod로 프로젝트에 통합(권장) {#section_qc5_h3v_zz}

프로젝트에 StreamHub-iOS SDK를 추가하는 가장 편리한 방법은 CocoaPods를 사용하는 것입니다. CococoaPods가 없는 경우 gem 설치 코드 및 창 설정을 실행하십시오. 다음은 포드파일의 예입니다.

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

CocoaPod 설치 시 사양 저장소를 추가해야 합니다(이렇게 하면 `~/.cocoapods/repos` 디렉토리로 복제).

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

앱 프로젝트 루트에 Podfile이 생성되어 위의 저장소가 추가되면 다음을 실행합니다.

```
pod install
```

이렇게 하면 모든 종속성이 다운로드되고 MyApp.xcworkspace 파일이 만들어집니다. 이 파일은 지금부터 Xcode에서 앱 프로젝트를 열 때 사용해야 합니다.

## Xcode 하위 프로젝트로 {#section_jcm_g3v_zz}

또는 저장소를 복제합니다.

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

그런 다음 Xcode 프로젝트(LFSClient.xcodeproj)를 하위 프로젝트로 앱에 추가합니다(LFSClient.xcodeproj 파일을 Xcode의 Project Navigator 창으로 간단히 드래그하여 손쉽게 수행).

종속성(AFNetworking, JSONKit)[을](https://github.com/AFNetworking/AFNetworking)사용하여 동일한 작업을 수행해야 [합니다](https://github.com/escherba/JSONKit).

## 한 번에 모두 다운로드(권장되지 않음) {#section_rpb_f3v_zz}

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
>Xcode 6에서 테스트를 실행하려면 $(PLATFORM_DIR)/Developer/Library/Frameworks를 Pods-test-XCTest+OHHTTPStubSuiteCleanUp podhttps://stackoverflow.com/a/24651704의 FRAMEWORK_SEARCH_PATHS에 추가해야[합니다](https://stackoverflow.com/a/24651704).

요청 시 Livefyre가 제공하는 Livefyre의 LFSTestConfig.plist 파일이 필요합니다.

## Xcode 설명서 {#section_arl_b3v_zz}

문서를 [](https://livefyre.github.com/StreamHub-iOS-SDK/) 찾아보거나 시스템에 Xcode에서 "문서" 타겟을 구축할 수 있습니다(응용 프로그램을 설치해야 함).

## 요구 사항 {#section_m5l_13v_zz}

v0.2.0 이후의 StreamHub iOS SDK 버전은 iOS 6.0 이상이 필요합니다.

## 부록(JSON 지원) {#section_pcd_5hv_zz}

StreamHub-iOS SDK 내실을 보는 사용자는 수정된 JSONKit 버전을 기본 JSON [구문 분석기로](https://github.com/escherba/JSONKit) 사용합니다(Apple에서 제공한 NSJSONSerialization 대신). Apple 제공 구문 분석기는 시스템에서 나타낼 수 있는 수보다 큰 정수나 부동 소수점 숫자를 포함하는 JSON 파일 디코딩을 지원하지 않으므로 이 작업을 수행해야 했습니다. 수정된 JSONKit 버전은 예외를 발생시키지 않고 해당 시스템 최대값에 매우 큰 수를 자릅니다.
