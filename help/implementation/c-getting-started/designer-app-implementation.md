---
description: Livefyre 앱에서 Bootstrap 및 Stream API를 사용할 수 있습니다.
seo-description: Livefyre 앱에서 Bootstrap 및 Stream API를 사용할 수 있습니다.
seo-title: 앱 구현
solution: Experience Manager
title: 앱 구현
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# 앱 구현 {#appimplementation}

사용 사례:고객으로서 Livefyre를 타사 CMS에 통합하려는 경우 Livefyre.js 메서드를 사용합니다.

사용자 지정 AEM 구성 요소나 WordPress, Sitecore 또는 DemandWare와 같은 다른 CMS에 Livefyre를 구현하는 방법에는 세 가지가 있습니다.디자이너 앱 구현, API, 구현 및 타사 인증 통합을 참조하십시오.

## 디자이너 앱 구현 {#designerapp}

소개:Livefyre 앱을 가장 간단하고 신속하게 통합하는 방법 사용자 정의된 Javascript 포함 코드를 디자인, 구성 및 생성하여 페이지에 Live App을 신속하게 통합할 수 있습니다.

방법:Livefyre 앱 [만들기, 미리 보기, 게시 및 포함](/help/using/c-about-apps/c-create-an-app.md)

예: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js 구현 {#livefyrejsimp}

소개:Livefyre.js [는](/help/implementation/c-livefyre.js.md) 사이트에서 Apps 및 Auth를 지원하는 핵심 라이브러리입니다. Livefyre 앱 임베드 및 타사 사용자 인증 플랫폼과의 통합에 도움이 되는 다른 Livefyre JavaScript 라이브러리를 로드하는 데 사용할 수 있는 글로벌 `window.Livefyre` 개체와 단일 공개 방법인 Livefyre.require를 정의합니다.

방법:

* [CollectionMeta 토큰을 사용하여 컬렉션 만들기](/help/implementation/t-create-a-collectionmeta-token.md)

* 앱 통합을 사용하여 앱을 타사 CMS에 통합

예:

* 댓글 앱: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 평가 앱: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* 미디어 벽: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* SDK를 사용한 고급 사용자 지정에 대해서는 StreamHub SDK를 참조하십시오.

## API 구현 {#apiimplementation}

사용자 정의된 경험과 데이터 시각화를 만들기 위해 Bootstrap 및 스트림 API를 사용하여 Livefyre 및 소셜 데이터를 사용함으로써 Livefyre 앱을 처음부터 만들 수 있습니다.

## 타사 인증 통합 {#thirdpartyauth}

인증이 필요한 Livefyre 앱의 경우 [타사](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 인증 플랫폼용 ID 통합을 참조하십시오.

## 고객 사례 {#customerexamples}

다음 고객은 서드파티 CMS 통합을 통해 Livefyre를 구현했습니다.

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [시간 초과](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
