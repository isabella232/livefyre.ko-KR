---
description: Livefyre 기반의 Android 앱을 제작할 수 있습니다.
seo-description: Livefyre 기반의 Android 앱을 제작할 수 있습니다.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793 FA 9-3 EA 1-4890-B 36 D-B 631 F 1 C 6 F 7 DE
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Android SDK{#android-sdk}

Livefyre 기반의 Android 앱을 제작할 수 있습니다.

이 라이브러리를 사용하여 Livefyre 서비스를 기본 Android 앱에 통합합니다. [Livefyre streamhub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 는 Gradle/Android Studio 개발 환경을 기반으로 일반적인 API 메커니즘을 둘러싸는 얇은 레이어를 제공합니다.

또한 Livefyre는 이 SDK [를 기반으로](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 샘플 샘플 앱을 제공합니다.

Livefyre Android SDK는 Eclipse 및 Android Studio 모두에서 사용할 수 있습니다.

>[!NOTE]
>
>Livefyre Android SDK를 설치하기 전에 환경에 [Android SDK가](https://developer.android.com/sdk/index.html) 설치되어 있어야 합니다. 또한 Android 개발자 문서 >에 설명된 바와 같이 일부 추가 Android SDK 패키지를 포함해야 합니다.
>[SDK 패키지 추가](https://developer.android.com/sdk/installing/adding-packages.html)

Android SDK 관리자 (Android Studio 또는 Eclipse 도구 모음에서 사용 가능) 를 사용하여 권장 패키지를 모두 설치합니다. Android 지원 저장소도 포함해야 합니다.

## Eclipse {#section_dtm_slv_zz}

Livefyre Android SDK를 Eclipse에서 프로젝트에 추가하려면 다음을 수행하십시오.

1. Github에서 [최신 streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 를 이용할 수 있습니다.
1. 기존 프로젝트를 시작하거나 새로운 프로젝트를 만듭니다.
1. To import the streamhub-android-sdk into your workspace go to **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. streamhub-android-sdk를 찾아보고 선택합니다. 이제 패키지 탐색기에 표시됩니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Properties,]** Android 탭을 선택합니다.
1. 라이브러리 섹션에서 선택한 **[!UICONTROL Add button,]** 다음 라이브러리 목록에서 Streamhub-Android-SDK를 선택합니다.
1. **[!UICONTROL Apply]****[!UICONTROL OK]**을 클릭합니다.

## Android Studio {#section_vpw_klv_zz}

Livefyre Android SDK를 Android Studio에서 프로젝트에 추가하려면 다음을 수행하십시오.

1. Github에서 [최신 streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 를 이용할 수 있습니다.
1. 기존 프로젝트를 시작하거나 새로운 프로젝트를 만듭니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open Module Settings]**선택합니다.
1. 창의 왼쪽 위 모퉁이에 있는 **[!UICONTROL +]** 단추를 선택합니다.
1. Select **[!UICONTROL Import Existing Project.]** (New Version of Android Studio, you can find **[!UICONTROL Import Existing Project]** under **[!UICONTROL More Modules]**.)

1. streamhub-android-sdk를 찾아보고 선택합니다.

Android Studio는 SDK를 Gradle 버전으로 전환할 것을 요청할 수 있습니다. 이러한 경우 [ **[!UICONTROL next]** 다음 **[!UICONTROL finish]**] 를 선택합니다.

프로젝트 **폴더 > 앱 폴더 > Build. gradle** 파일 종속성으로 이동하여 종속성을 추가합니다.

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

다음 라인이 **프로젝트 폴더 > Settings. gradle** 파일에 있는지 확인합니다.

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>config. java 내에서 구성을 사용자 지정할 수 있습니다.

## 클라이언트 {#section_yfq_blv_zz}

Streamhub Android SDK는 Livefyre API 끝점을 요청하는 데 사용할 수 있는 여러 클라이언트 클래스를 노출합니다.

* **Adminclient** 사용자 정보, 키 및 기타 메타데이터에 대한 사용자 인증 토큰을 교환합니다.

* **Bootstrapclient** 특정 컬렉션에 대한 최신 컨텐츠와 메타데이터를 가져옵니다.

* **Streamclient** 컬렉션을 위한 스트림을 폴링하여 신규, 업데이트된 및 삭제된 컨텐츠를 검색합니다.

* **Writeclient** 게시물, 플래그 및 컬렉션의 좋아요 컨텐츠.

