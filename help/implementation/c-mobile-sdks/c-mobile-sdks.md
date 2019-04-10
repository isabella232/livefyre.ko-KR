---
description: 기본 모바일 앱에 Livefyre 추가
seo-description: 기본 모바일 앱에 Livefyre 추가
seo-title: Mobile SDK
solution: Experience Manager
title: Mobile SDK
uuid: 84 C 7 CA 1 C -3401-492 A-BFA 5-62 B 996947 A 44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mobile SDK{#mobile-sdks}

기본 모바일 앱에 Livefyre 추가

만들려는 사용자 정의 범위에 따라 모바일 구현에 사용할 수 있는 여러 가지 옵션이 있습니다.

* 모바일 웹 앱
* Livefyre Android 또는 iOS SDK
* HTTP API

## 모바일 웹 앱 {#section_t2k_vpb_11b}

모바일 디바이스에서 웹 페이지를 여는 고객은 축소된 화면 크기 및 수정 사항을 처리하기 위한 수정 사항을 포함하여 모바일에 맞게 최적화된 Livefyre 컨텐츠 스트림을 자동으로 얻게 됩니다.

>[!NOTE]
>
>Android WebView에서 Livefyre 앱을 사용하는 경우 Android [websettings. setdomstorageenabled](https://developer.android.com/reference/android/webkit/WebSettings.html) 매개 변수를 true로 설정해야 합니다. Localstorage가 활성화되지 않은 경우 Livefyre는 Livefyre 앱에 사용자를 로그인할 수 없게 됩니다.

모바일용으로 최적화하기 위해 Livefyre는 댓글, 라이브 블로그 및 채팅 앱 기능을 다음과 같이 제한합니다.

* POST
* edit
* flag
* like
* 답글
* 리스너 카운트
* 댓글 수
* 인라인 보류 중인 중재
* 호버카드
* 주요 주석
* Hot Threads
* 큐 주석

모바일 웹 앱에서 작성자의 이름을 클릭하면 새 페이지에서 호버카드 정보가 열립니다.

## Livefyre Android SDK 또는 iOS SDK {#section_zdz_spb_11b}

Livefyre는 다음 두 가지 모바일 SDK도 제공합니다. iOS SDK 및 Android SDK. 이러한 SDK는 HTTP 엔드포인트를 둘러싸는 래퍼로서, 데이터를 전송하고 수신할 수 있는 보다 간편한 방법을 제공합니다. 이러한 SDK와 함께 제공되는 인터페이스는 없으므로 모바일 앱 내에서 컨텐츠가 표시되고 사용되는 방식에 대한 유연성이 높아집니다.

Android 및 iOS SDK는 댓글, 라이브 블로그 및 채팅을 위한 다음 기능을 지원합니다.

| iOS 기능: | Android 기능: |
|--- |--- |
| <ul><li> POST </li><li>edit </li><li>flag </li><li>like </li><li>답글 </li><li>Hot Threads</li></ul> | <ul><li>POST </li><li>edit </li><li>like </li><li>답글 </li><li>Hot Threads</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API는 Livefyre 플랫폼에서 대화와 컨텐츠를 만들 수 있도록 해주는 엔드포인트 그룹입니다. 모든 Livefyre를 사용할 수 있습니다. 이 솔루션을 사용하면 엔지니어링 팀의 개발 시간이 더 많이 걸리지만 Livefyre 제품군을 사용할 때 유연성을 높일 수 있고 기본 모바일 통합이 가능합니다.

>[!IMPORTANT]
>
>**모바일 클라이언트 내에서 사용자 인증 토큰을** 만들지 마십시오. 이는 비보안 앱 내에 Livefyre 암호 네트워크 키를 표시해야 하기 때문입니다. 보다 강력하고 안전한 솔루션을 보려면 사용자 인증 토큰 섹션을 참조하십시오.

