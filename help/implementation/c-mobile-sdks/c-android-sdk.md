---
description: Livefyre 기반의 Android 앱 제작
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Android SDK{#android-sdk}

Livefyre 기반의 Android 앱 제작

이 라이브러리를 사용하여 Livefyre 서비스를 기본 Android 앱에 통합할 수 있습니다. [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK)는 Grade/Android Studio 개발 환경을 기반으로 일반적인 API 메커니즘을 둘러싼 가상 레이어를 제공합니다.

또한 Livefyre는 이 SDK를 기반으로 [평가](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 샘플 앱을 제공합니다.

이 Livefyre Android SDK는 Eclipse 및 Android Studio 모두에서 사용할 수 있습니다.

>[!NOTE]
>
>Livefyre Android SDK를 설치하기 전에 환경에 [Android SDK](https://developer.android.com/sdk/index.html)가 설치되어 있어야 합니다. Android 개발자 문서 > 에 설명된 대로 일부 추가 Android SDK 패키지를 포함해야 합니다.
>[SDK 패키지 추가](https://developer.android.com/sdk/installing/adding-packages.html)

Android SDK Manager(Android Studio 또는 Eclipse 도구 모음에서 사용 가능)를 사용하여 권장 패키지를 모두 설치합니다. Android 지원 저장소도 포함해야 합니다.

## Eclipse {#section_dtm_slv_zz}

Eclipse에서 프로젝트에 Livefyre Android SDK를 추가하려면:

1. GitHub에서 최신 [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)를 가져옵니다.
1. 기존 프로젝트로 시작하거나 새 프로젝트를 만듭니다.
1. StreamHub-Android-SDK를 작업 영역으로 가져오려면 **[!UICONTROL File > Import > General > Existing Project into Workspace]**&#x200B;으로 이동하십시오.
1. StreamHub-Android-SDK를 검색하고 선택합니다.이제 패키지 탐색기에 표시됩니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Properties,]** Android 탭을 선택합니다.
1. 라이브러리 섹션에서 **[!UICONTROL Add button,]**&#x200B;을 선택한 다음 라이브러리 목록에서 StreamHub-Android-SDK를 선택합니다.
1. **[!UICONTROL Apply]** 및 **[!UICONTROL OK]**&#x200B;을 클릭합니다.

## Android Studio {#section_vpw_klv_zz}

Android Studio에서 프로젝트에 Livefyre Android SDK를 추가하려면:

1. GitHub에서 최신 [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)를 가져옵니다.
1. 기존 프로젝트로 시작하거나 새 프로젝트를 만듭니다.
1. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open Module Settings]** 을 선택합니다.
1. 창의 왼쪽 위 모서리에서 **[!UICONTROL +]** 단추를 선택합니다.
1. **[!UICONTROL Import Existing Project.]** 선택 (새 버전의 Android studio에서는 **[!UICONTROL More Modules]** 아래에 **[!UICONTROL Import Existing Project]**&#x200B;을 찾을 수 있습니다.)

1. StreamHub-Android-SDK를 검색하고 선택합니다.

Android Studio는 SDK를 일반 버전으로 전환할 것을 요청할 수 있습니다.이러한 경우 **[!UICONTROL next]**, **[!UICONTROL finish]**&#x200B;을 차례로 선택합니다.

종속성 아래의 **프로젝트 폴더 > 앱 폴더 > build.grade** 파일로 이동하여 다음 종속성을 추가합니다.

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

다음 줄이 **프로젝트 폴더 > settings.grade** 파일에 있는지 확인합니다.

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Config.java 내에서 구성을 사용자 지정할 수 있습니다.

## 고객 {#section_yfq_blv_zz}

StreamHub Android SDK는 Livefyre API 끝점을 요청하는 데 사용할 수 있는 여러 클라이언트 클래스를 표시합니다.

* **** AdminClientExchange 사용자 정보, 키 및 기타 메타데이터에 대한 사용자 인증 토큰입니다.

* **Bootstrap** Client특정 컬렉션에 대한 최신 컨텐츠 및 메타데이터를 가져올 수 있습니다.

* **StreamClient** 새 콘텐츠, 업데이트됨 및 삭제된 콘텐츠를 검색할 수 있도록 컬렉션용 스트림을 폴링합니다.

* **컬렉션** 의 콘텐츠를 WriteClientPost, 플래그 및 좋아요.
