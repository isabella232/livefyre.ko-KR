---
description: Livefyre 앱에 Bootstrap 및 스트림 API를 사용할 수 있습니다.
seo-description: Livefyre 앱에 Bootstrap 및 스트림 API를 사용할 수 있습니다.
seo-title: 앱 구현
solution: Experience Manager
title: 앱 구현
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# 앱 구현 {#appimplementation}

사용 사례:고객으로서 Livefyre를 제3자 CMS에 통합하여 Livefyre.js 메서드를 사용하고 싶습니다.

Livefyre를 사용자 정의 AEM 구성 요소 또는 WordPress, Sitecore 또는 DemandWare와 같은 다른 CMS에 구현하는 방법에는 3가지가 있습니다.디자이너 앱 구현, API, 구현 및 제3자 인증 통합을 참조하십시오.

## 디자이너 앱 구현 {#designerapp}

소개:Livefyre 앱을 가장 간단하고 신속하게 통합하는 방법 사용자 지정된 Javascript 포함 코드를 디자인, 구성 및 생성하여 페이지에 Live App을 신속하게 통합할 수 있습니다.

방법:[Livefyre 앱 만들기, 미리 보기, 게시 및 포함](/help/using/c-about-apps/c-create-an-app.md)

예:[https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js 구현 {#livefyrejsimp}

소개:[Livefyre.js](/help/implementation/c-livefyre.js.md)는 사이트에서 앱과 인증에 대한 기능을 제공하는 핵심 라이브러리입니다. 전역 `window.Livefyre` 개체와 단일 공개 방법인 Livefyre.require를 정의합니다. 이 메서드는 Livefyre 앱을 내장하고 제3자 사용자 인증 플랫폼과 통합하는 데 도움이 되는 다른 Livefyre JavaScript 라이브러리를 로드하는 데 사용할 수 있습니다.

방법:

* [CollectionMeta 토큰을 사용하여 컬렉션 만들기](/help/implementation/t-create-a-collectionmeta-token.md)

* 앱 통합을 사용하여 앱을 제3자 CMS에 통합

예:

* 댓글 앱:[https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 검토 앱:[https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* 미디어 벽:[https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* SDK를 사용한 고급 사용자 정의에 대해서는 StreamHub SDK를 참조하십시오.

## API 구현 {#apiimplementation}

사용자 정의된 경험 및 데이터 시각화를 만들기 위해 Bootstrap 및 스트림 API를 사용하여 Livefyre 및 소셜 데이터를 사용함으로써 Livefyre 앱을 처음부터 만들 수 있습니다.

## 제3자 인증 통합 {#thirdpartyauth}

인증이 필요한 Livefyre 앱의 경우 제3자 인증 플랫폼의 경우 [ID 통합](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)을 참조하십시오.

## 고객 예 {#customerexamples}

다음 고객은 제3자 CMS 통합과 함께 Livefyre를 구현했습니다.

* [PGA 투어 미디어 벽](https://www.pgatour.com/social-hub.html)

* [시간 초과](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
