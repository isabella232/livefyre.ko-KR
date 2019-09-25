---
description: Livefyre.js는 사이트의 앱에 대한 인증을 제공하는 작은 기본 라이브러리입니다.
seo-description: Livefyre.js는 사이트의 앱에 대한 인증을 제공하는 작은 기본 라이브러리입니다.
seo-title: 페이지에 Livefyre.js 추가
title: 페이지에 Livefyre.js 추가
uuid: fe52446e-4911-4160-a68c-7413e9bc6222
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 페이지에 Livefyre.js 추가{#add-livefyre-js-to-the-page}

Livefyre.js는 사이트의 앱에 대한 인증을 제공하는 작은 기본 라이브러리입니다.

인증을 활성화하려면:

1. 웹 페이지 또는 웹 사이트 템플릿의 `<head>` 요소에 Livefyre.js를 추가합니다.
1. 페이지에 다음 중 하나를 추가합니다.

   * `globalwindow.Livefyre` 변수에 설정된 ID
   * `Livefyre.require` to load other Livefyre packages on demand

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```

