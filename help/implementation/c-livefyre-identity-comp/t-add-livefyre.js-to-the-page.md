---
description: Livefyre.js는 사이트의 앱에 대한 인증을 제공하는 작은 기본 라이브러리입니다.
title: 페이지에 Livefyre.js 추가
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# Livefyre.js를 페이지{#add-livefyre-js-to-the-page}에 추가

Livefyre.js는 사이트의 앱에 대한 인증을 제공하는 작은 기본 라이브러리입니다.

인증을 활성화하려면:

1. 웹 페이지 또는 웹 사이트 템플릿의 `<head>` 요소에 Livefyre.js를 추가합니다.
1. 페이지에 다음 중 하나를 추가합니다.

   * `globalwindow.Livefyre` 변수에 설정된 ID
   * `Livefyre.require` 다른 Livefyre 패키지를 on-demand로 불러오려면

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
