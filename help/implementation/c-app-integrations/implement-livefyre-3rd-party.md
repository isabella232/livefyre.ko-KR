---
description: Livefyre 앱을 처음부터 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.
seo-description: Livefyre 앱을 처음부터 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.
seo-title: Livefyre와 타사 통합 통합
solution: Experience Manager
title: Livefyre를 CMS에 통합
uuid: 5a3e18e8-8568-4 파섹
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# 타사 통합을 통해 Livefyre 구현

Livefyre 앱을 처음부터 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.

You can create a Livefyre App from scratch by consuming Livefyre and social data using the Bootstrap and Stream API.

For Livefyre Apps that require authentication, see Identity Integration for information about supported third party authentication platforms.

To implement Conversation Apps (Comments, Chat, Live Blog, Sidenotes):

1. Perform App integration.
a. Create a Collection Using the CollectionMeta Token.
b. Integrate Livefyre Apps to sites using the Livefyre.js embed code structure.

   * For more information on how to use the Livefyre.js embed code structure, see Embed an App.[](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

   * For information on how to integrate the Comments App, see Comments.[](/help/using/c-about-apps/c-comments/c-comments.md)

   * For information on how to integrate the Chat App, see Chat.[](/help/using/c-about-apps/c-chat-app/c-chat-app.md)

   * For information on how to integrate the Live Blog App, see Live Blog.[](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)

   * For information on how to integrate the Sidenotes App, see Sidenotes.[](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)

1. Perform authentication integration.
a. Create User Auth tokens to pass and store user data in Livefyre.
b. Integrate third party user and authentication platforms. For a list of supported platforms, see Identity Integration.[](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)

1. 앱 맞춤화를 수행합니다. 앱 맞춤화 옵션을 사용하여 브랜딩 및 스타일을 일치시키고 사용자 정의 기능을 추가할 수 있습니다.

시각화 응용 프로그램(맵, 미디어 벽, 트렌드, 회전판, 필름스트립, 스토리, 기능 카드, 모자이크, 투표)을 만들려면:

1. 앱 통합을 수행합니다.
a.CollectionMeta 토큰을 사용하여 컬렉션을 만듭니다.
b.Livefyre.js 임베드 코드 구조를 사용하여 Livefyre 앱을 사이트에 통합할 수 있습니다. Livefyre.js 임베드 코드 구조를 사용하는 방법에 대한 자세한 내용은 앱 [임베드](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)참조

   * 맵 앱을 통합하는 방법에 대한 자세한 내용은 맵을 [참조하십시오](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Media Wall 응용 프로그램을 통합하는 방법에 대한 자세한 내용은 Media Wall [을 참조하십시오](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * 트렌드 앱을 통합하는 방법에 대한 자세한 내용은 트렌드를 [참조하십시오](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. 인증 통합을 수행합니다.
a.사용자 인증 토큰을 만들어 사용자 데이터를 Livefyre에 전달하고 저장합니다.
b.타사 사용자 및 인증 플랫폼 통합 지원되는 플랫폼 목록은 ID 통합을 [참조하십시오](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre는 Livefyre.js를 사용하는 Carousel, Filmstrip, Storify, Feature Card, Mosaic 및 Polls 앱을 지원하지 않습니다.
앱 만들기 프로세스를 사용하여 [이러한 앱을](/help/using/c-about-apps/c-create-an-app.md) 통합합니다.