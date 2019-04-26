---
description: Livefyre 앱을 처음부터 제작하여 맞춤형 경험과 데이터 시각화를 제작할 수 있습니다.
seo-description: Livefyre 앱을 처음부터 제작하여 맞춤형 경험과 데이터 시각화를 제작할 수 있습니다.
seo-title: Livefyre와 타사 통합 통합
solution: Experience Manager
title: Livefyre를 CMS에 통합
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# 타사 통합을 통해 Livefyre 구현

Livefyre 앱을 처음부터 제작하여 맞춤형 경험과 데이터 시각화를 제작할 수 있습니다.

Bootstrap 및 스트림 API를 사용하여 Livefyre 및 소셜 데이터를 사용하여 Livefyre 앱을 처음부터 만들 수 있습니다.

인증이 필요한 Livefyre 앱의 경우 지원되는 타사 인증 플랫폼에 대한 자세한 내용은 ID 통합을 참조하십시오.

대화 앱 (댓글, 채팅, 라이브 블로그, Sidenotes) 를 구현하려면:

1. 앱 통합을 수행합니다.
a. Collectionmeta 토큰을 사용하여 컬렉션을 만듭니다.
b. Livefyre. js 임베드 코드 구조를 사용하여 Livefyre 앱을 사이트에 통합할 수 있습니다.

   * Livefyre. js 임베드 코드 구조를 사용하는 방법에 대한 자세한 내용은 앱 [임베딩을 참조하십시오](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * 댓글 앱 통합에 대한 자세한 내용은 [댓글을](/help/using/c-about-apps/c-comments/c-comments.md)참조하십시오.

   * 채팅 앱을 통합하는 방법에 대한 자세한 내용은 [채팅을](/help/using/c-about-apps/c-chat-app/c-chat-app.md)참조하십시오.

   * 라이브 블로그 앱을 통합하는 방법에 대한 자세한 내용은 [라이브 블로그를](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)참조하십시오.

   * Sidenotes 앱을 통합하는 방법에 대한 자세한 내용은 [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)를 참조하십시오.

1. 인증 통합을 수행합니다.
a. Livefyre에서 사용자 데이터를 전달하고 저장할 사용자 인증 토큰을 만듭니다.
b. 타사 사용자 및 인증 플랫폼을 통합할 수 있습니다. 지원되는 플랫폼 목록은 [ID 통합을](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)참조하십시오.

1. 앱 맞춤화 수행 앱 맞춤화 옵션을 사용하여 브랜딩 및 스타일에 맞는 맞춤형 기능을 추가할 수 있습니다.

시각화 앱을 만들려면 (맵, 미디어 담벼락, 트렌드, 회전식, 필름스트립, 스토리화, 기능 카드, 모자이크, 투표):

1. 앱 통합을 수행합니다.
a. Collectionmeta 토큰을 사용하여 컬렉션을 만듭니다.
b. Livefyre. js 임베드 코드 구조를 사용하여 Livefyre 앱을 사이트에 통합할 수 있습니다. Livefyre. js 임베드 코드 구조를 사용하는 방법에 대한 자세한 내용은 앱 [임베딩을 참조하십시오](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * 맵 앱 통합에 대한 자세한 내용은 [맵을](/help/using/c-about-apps/c-map-app/c-map-app.md)참조하십시오.

   * 미디어 담벼락 앱을 통합하는 방법에 대한 자세한 내용은 [미디어 월을](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md)참조하십시오.

   * 트렌드 앱을 통합하는 방법에 대한 자세한 내용은 [트렌드를](/help/using/c-about-apps/c-trending-app/c-trending-app.md)참조하십시오.

1. 인증 통합을 수행합니다.
a. 사용자 데이터를 전달하여 Livefyre에 사용자 데이터를 전달하는 사용자 인증 토큰을 만듭니다.
b. 타사 사용자 및 인증 플랫폼을 통합할 수 있습니다. 지원되는 플랫폼 목록은 [ID 통합을](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)참조하십시오.

>[!NOTE]
>
>Livefyre는 Carousel, Filmstrip, Storify, Feature Card, Mosaic 및 Livefyre. js를 사용하는 투표를 지원하지 않습니다.
앱 제작 프로세스를 사용하여 [이러한 앱을](/help/using/c-about-apps/c-create-an-app.md) 통합합니다.