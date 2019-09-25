---
description: 사이트에서 Livefyre를 지원하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-description: 사이트에서 Livefyre를 지원하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-title: updateAnchors 메서드
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# updateAnchors 메서드 {#updateAnchorsMethod}

updateAnchors 메서드를 사용하여 사이드된 컨텐츠를 페이지에 동적으로 추가합니다.

이 방법은 페이지 매김이나, sidecenoable 내용이 페이지에 동적으로 추가되는 다른 경우에 유용합니다. 이 메서드는 일치하는 요소에 대한 새 앵커를 정의하고 단일 인수를 사용합니다.newSelectors.

**newSelectors**. Sidecnotes에 추가할 선택기입니다. 선택기 문자열, jQuery 객체 또는 요소 배열(앱 빌드 중에 전달된 선택기 인수에서 허용하는 모든 유형)일 수 있습니다.
형식:

```
app.updateAnchors(newSelectors);
```

예:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
