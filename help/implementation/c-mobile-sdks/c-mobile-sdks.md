---
description: 기본 모바일 앱에 Livefyre 추가
seo-description: 기본 모바일 앱에 Livefyre 추가
seo-title: Mobile SDK
solution: Experience Manager
title: Mobile SDK
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mobile SDK{#mobile-sdks}

기본 모바일 앱에 Livefyre 추가

모바일 구현에 사용할 수 있는 옵션은 다음과 같은 사용자 정의 범위에 따라 다릅니다.

* 모바일 웹 앱
* Livefyre Android 또는 iOS SDK
* HTTP API

## 모바일 웹 앱 {#section_t2k_vpb_11b}

모바일 장치에서 웹 페이지를 여는 고객은 축소된 화면 크기에 맞게 스타일링을, 터치 이벤트를 처리하기 위해 수정하는 방법을 포함하여 모바일에 최적화된 Livefyre 컨텐츠 스트림을 자동으로 받습니다.

>[!NOTE]
>
>Android WebView에서 Livefyre 앱을 사용하는 경우 Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) 매개 변수를 true로 설정해야 합니다. localStorage가 활성화되지 않은 경우 Livefyre는 사용자를 Livefyre 앱에 로그인할 수 없습니다.

모바일용으로 최적화하기 위해 Livefyre는 댓글, 라이브 블로그 및 채팅 앱 기능을 다음으로 제한합니다.

* 게시물
* 편집
* 플래그
* 좋아요
* 답글
* 리스너 수
* 댓글 수
* 인라인 보류 중 중재
* 호버카드
* 상위 댓글
* 핫 스레드
* 큐 댓글

모바일 웹 앱에서 작성자의 이름을 클릭하면 새 페이지에 있는 호버카드 정보가 열립니다.

## Livefyre Android SDK 또는 iOS SDK {#section_zdz_spb_11b}

또한 Livefyre는 두 개의 모바일 SDK를 제공합니다.iOS SDK 및 Android SDK. 이러한 SDK는 보다 간편한 데이터 전송 및 수신 방법을 제공하기 위해 구축된 HTTP 엔드포인트 주위에 래퍼됩니다. 이러한 SDK에는 인터페이스가 제공되지 않으므로 모바일 앱 내에서 컨텐츠가 표시되고 사용되는 방식에 보다 유연하게 대처할 수 있습니다.

Android 및 iOS SDK는 댓글, 라이브 블로그 및 채팅에 대해 다음 기능을 지원합니다.

| iOS 기능: | Android 기능: |
|--- |--- |
| <ul><li> 게시물 </li><li>편집 </li><li>플래그 </li><li>좋아요 </li><li>답글 </li><li>핫 스레드</li></ul> | <ul><li>게시물 </li><li>편집 </li><li>좋아요 </li><li>답글 </li><li>핫 스레드</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API는 Livefyre 플랫폼에서 대화와 컨텐츠를 만들 수 있는 끝점 그룹입니다. 또한 모든 Livefyre를 즉시 스트리밍할 수 있습니다. 이 솔루션은 엔지니어링 팀의 개발 시간이 더 필요하지만 Livefyre 제품 패키지를 사용할 때 유연성이 더 뛰어나고 기본 모바일 통합을 지원합니다.

>[!IMPORTANT]
>
>**보안되지 않은 앱 내에서 Livefyre 비밀 네트워크 키를 노출해야 하므로 모바일 클라이언트 내에서 사용자 인증 토큰을 만들지 마십시오** . 보다 강력하고 안전한 솔루션은 사용자 인증 토큰 섹션을 참조하십시오.

