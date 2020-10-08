---
description: 처음부터 Livefyre 앱을 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.
seo-description: 처음부터 Livefyre 앱을 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.
seo-title: Livefyre와 타사 통합
solution: Experience Manager
title: Livefyre를 CMS에 통합
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 타사 통합을 통해 Livefyre 구현

처음부터 Livefyre 앱을 제작하여 맞춤형 경험 및 데이터 시각화를 만들 수 있습니다.

Bootstrap 및 스트림 API를 사용하여 Livefyre 및 소셜 데이터를 사용함으로써 Livefyre 앱을 처음부터 만들 수 있습니다.

인증이 필요한 Livefyre 앱의 경우 지원되는 타사 인증 플랫폼에 대한 자세한 내용은 ID 통합을 참조하십시오.

대화 앱(댓글, 채팅, 라이브 블로그, 사이드노트)을 구현하려면

1. 앱 통합 수행
a.CollectionMeta 토큰을 사용하여 컬렉션을 만듭니다.
b.Livefyre.js 임베드 코드 구조를 사용하여 Livefyre 앱을 사이트에 통합할 수 있습니다.

   * Livefyre.js 임베드 코드 구조를 사용하는 방법에 대한 자세한 내용은 앱 [임베드](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)를 참조하십시오.

   * 댓글 앱 통합 방법에 대한 자세한 내용은 [주석을 참조하십시오](/help/using/c-about-apps/c-comments/c-comments.md).

   * 채팅 앱 통합 방법에 대한 자세한 내용은 [채팅을 참조하십시오](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * 라이브 블로그 앱을 통합하는 방법에 대한 자세한 내용은 [라이브 블로그를 참조하십시오](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * 사이드노트 앱 통합 방법에 대한 자세한 내용은 [사이드노트를 참조하십시오](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. 인증 통합을 수행합니다.
a.사용자 인증 토큰을 만들어 Livefyre에 사용자 데이터를 전달하고 저장할 수 있습니다.
b.타사 사용자 및 인증 플랫폼 통합 지원되는 플랫폼 목록은 ID [통합을 참조하십시오](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. 앱 맞춤화를 수행합니다. 앱 사용자 지정 옵션을 사용하여 브랜딩 및 스타일을 일치시키고 사용자 정의 기능을 추가할 수 있습니다.

시각화 응용 프로그램을 만들려면(맵, 미디어 벽, 트렌드, 회전판, 필름스트립, 스토리, 기능 카드, 모자이크, 투표):

1. 앱 통합 수행
a.CollectionMeta 토큰을 사용하여 컬렉션을 만듭니다.
b.Livefyre.js 임베드 코드 구조를 사용하여 Livefyre 앱을 사이트에 통합할 수 있습니다. Livefyre.js 임베드 코드 구조를 사용하는 방법에 대한 자세한 내용은 앱 [임베드](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)를 참조하십시오.

   * 맵 앱 통합 방법에 대한 자세한 내용은 [맵을 참조하십시오](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * 미디어 담벼락 앱 통합 방법에 대한 자세한 내용은 [미디어 장벽을 참조하십시오](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * 트렌드 앱을 통합하는 방법에 대한 자세한 내용은 트렌드를 [참조하십시오](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. 인증 통합을 수행합니다.
a.사용자 인증 토큰을 만들어 사용자 데이터를 Livefyre에 전달하고 저장합니다.
b.타사 사용자 및 인증 플랫폼 통합 지원되는 플랫폼 목록은 ID [통합을 참조하십시오](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre는 Livefyre.js를 사용하는 Carousel, Filmstrip, Storify, Feature Card, Mosaic 및 Polls 앱을 지원하지 않습니다.

앱 만들기 프로세스를 사용하여 [이러한 앱을](/help/using/c-about-apps/c-create-an-app.md) 통합합니다.