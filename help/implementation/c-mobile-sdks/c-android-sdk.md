---
description: Livefyre 기반의 Android 앱 제작
seo-description: Livefyre 기반의 Android 앱 제작
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Livefyre 기반의 Android 앱 제작

이 라이브러리를 사용하여 Livefyre 서비스를 기본 Android 앱에 통합할 수 있습니다. Livefyre [StreamHub Android](https://github.com/Livefyre/StreamHub-Android-SDK) SDK는 Gradle/Android Studio 개발 환경을 기반으로 공통 API 메커니즘 주위에 가상 레이어를 제공합니다.

또한 Livefyre는 [이](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) SDK를 기반으로 리뷰 샘플 앱을 제공합니다.

이 Livefyre Android SDK는 Eclipse 및 Android Studio 모두에서 사용할 수 있습니다.

>[!NOTE]
>
>Livefyre Android SDK를 설치하기 전에 [환경에 Android](https://developer.android.com/sdk/index.html) SDK가 설치되어 있어야 합니다. Android 개발자 문서 &gt; 에 설명된 대로 일부 추가 Android SDK 패키지를 포함해야 합니다.
>[SDK 패키지 추가](https://developer.android.com/sdk/installing/adding-packages.html)

Android SDK Manager(Android Studio 또는 Eclipse 도구 모음에서 사용 가능)를 사용하여 권장 패키지를 모두 설치합니다. Android 지원 저장소도 포함해야 합니다.

## Eclipse {#section_dtm_slv_zz}

Eclipse에서 프로젝트에 Livefyre Android SDK를 추가하려면:

1. GitHub에서 최신 [StreamHub-Android-SDK를](https://github.com/Livefyre/StreamHub-Android-SDK) 다운로드할 수 있습니다.
1. 기존 프로젝트로 시작하거나 새 프로젝트를 만듭니다.
1. StreamHub-Android-SDK 파섹 **[!UICONTROL File > Import > General > Existing Project into Workspace]**
1. StreamHub-Android-SDK를 찾아 선택합니다.이제 패키지 탐색기에 표시됩니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 Android 탭을 **[!UICONTROL Properties,]** 선택합니다.
1. 라이브러리 섹션에서 라이브러리 목록에서 StreamHub-Android-SDK를 **[!UICONTROL Add button,]** 선택한 다음
1. 를 **[!UICONTROL Apply]** 클릭하고 **[!UICONTROL OK]**&#x200B;있습니다.

## Android Studio {#section_vpw_klv_zz}

Android Studio에서 프로젝트에 Livefyre Android SDK를 추가하려면:

1. GitHub에서 최신 [StreamHub-Android-SDK를](https://github.com/Livefyre/StreamHub-Android-SDK) 다운로드할 수 있습니다.
1. 기존 프로젝트로 시작하거나 새 프로젝트를 만듭니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open Module Settings]**&#x200B;선택합니다.
1. 창의 왼쪽 위 모서리에 있는 **[!UICONTROL +]** 단추를 선택합니다.
1. 선택 **[!UICONTROL Import Existing Project.]** (새 버전의 Android 스튜디오에서는 **[!UICONTROL Import Existing Project]** 아래에서 찾을 수 **[!UICONTROL More Modules]**&#x200B;있습니다.)

1. StreamHub-Android-SDK를 찾아 선택합니다.

Android Studio는 SDK를 일반 버전으로 전환할 것을 요청할 수 있습니다.이 경우 **[!UICONTROL next]** 을 선택합니다 **[!UICONTROL finish]**.

종속성 아래의 **프로젝트 폴더 &gt; 앱 폴더 &gt; build.gradle** 파일로 이동하여 다음 종속성을 추가합니다.

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

다음 줄이 **프로젝트 폴더 &gt; settings.gradle** 파일에 있는지 확인합니다.

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Config.java 내에서 구성을 사용자 지정할 수 있습니다.

## 고객 {#section_yfq_blv_zz}

StreamHub Android SDK 파섹

* **AdminClient** 사용자 정보, 키 및 기타 메타데이터에 대한 사용자 인증 토큰을 교환합니다.

* **BootstrapClient** 특정 컬렉션에 대한 최신 컨텐츠 및 메타데이터를 가져올 수 있습니다.

* **StreamClient** 새 콘텐츠, 업데이트된 콘텐츠 및 삭제된 콘텐츠를 검색하기 위해 컬렉션에 대한 스트림을 폴링합니다.

* **WriteClient** 컬렉션의 콘텐츠 게시, 플래그 및 좋아요.

