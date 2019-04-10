---
description: 기본 iOS 앱에 Livefyre를 추가합니다.
seo-description: 기본 iOS 앱에 Livefyre를 추가합니다.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: BFDEF 31 A -49 FC -4 B 25-B 0 C 5-300 F 27067302
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

기본 iOS 앱에 Livefyre를 추가합니다.

이 오픈 소스 라이브러리를 사용하여 Livefyre 서비스를 기본 iOS 앱에 통합할 수 있습니다. Livefyre streamhub iOS SDK는 탁월한 afnetworking 라이브러리를 기반으로 일반적인 API 메커니즘을 기반으로 한 얇은 레이어를 제공합니다.

또한 Livefyre는 다음 SDK를 기반으로 두 개의 iOS 샘플 앱을 제공합니다. Comment Stream and a Review Sample Apps.

## SDK를 Cocoa Pod로 프로젝트에 통합 (권장) {#section_qc5_h3v_zz}

프로젝트에 Streamhub-iOS SDK를 추가하는 가장 편리한 방법은 Cocoapods를 사용하는 것입니다. Cocoapods가 없는 경우 GEM install cocoapods 및 pod 설정을 실행합니다. 다음은 podfile 입니다.

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

또한 Cocoapod 설치에 사양 저장소를 추가해야 `~/.cocoapods/repos` 합니다 (디렉토리로 복제합니다.).

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

앱 프로젝트 루트에 Podfile 이 만들어지고 위의 저장소가 추가되면 다음을 실행합니다.

```
pod install
```

모든 종속성을 다운로드하고 Myapp. xcworkspace 파일을 만들어 Xcode에서 앱 프로젝트를 열 수 있습니다.

## Xcode 하위 프로젝트로 {#section_jcm_g3v_zz}

또는 리포지토리 복제:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

그런 다음 Xcode 프로젝트 (lfsclient. xcodeproj) 를 앱에 하위 프로젝트로 추가합니다 (lfsclient. xcodeproj 파일을 Xcode의 프로젝트 탐색기 창으로 드래그하여 쉽게 수행).

또한 종속성 ([Afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)) 를 사용하여 동일한 작업을 수행해야 합니다.

## 한 번에 모든 항목 다운로드 (권장하지 않음) {#section_rpb_f3v_zz}

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
>Xcode 6에서 테스트를 실행하려면 pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704의 framework_ search_ paths에 $ (platform_ dir)/developer/library/frameworks를 추가해야[](https://stackoverflow.com/a/24651704)합니다.

Livefyre에서 요청할 때 Livefyre가 제공하는 lfstestconfig. plist 파일이 필요합니다.

## Xcode 설명서 {#section_arl_b3v_zz}

[설명서를](https://livefyre.github.com/StreamHub-iOS-SDK/) 찾아보거나 시스템에 Xcode (appledoc가 설치되어야 함) 에서 "문서" 대상을 만들 수 있습니다.

## 요구 사항 {#section_m5l_13v_zz}

v 0.2.0 이후 streamhub iOS SDK 버전을 사용하려면 iOS 6.0 이상이 필요합니다.

## 부록 (JSON 지원) {#section_pcd_5hv_zz}

Streamhub-iOS SDK Internals를 사용하는 사용자의 경우, 기본 JSON 파서 (apple에서 제공하는 nsjsonserialization 대신) 로 수정된 [jsonkit](https://github.com/escherba/JSONKit) 버전이 사용됩니다. Apple에서 제공한 파서는 시스템에서 표현할 수 있는 정수나 부동 소수점 숫자가 포함된 JSON 파일 디코딩을 지원하지 않으므로 이렇게 해야 합니다. Adobe의 수정된 jsonkit 버전은 예외를 throw 하는 대신 해당 시스템 최대값에 매우 많이 잘립니다.
