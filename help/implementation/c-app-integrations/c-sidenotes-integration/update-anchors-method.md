---
description: 사이트에서 Livefyre의 강력한 기능을 제공하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-description: 사이트에서 Livefyre의 강력한 기능을 제공하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-title: updateAnchors 메서드
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# updateAnchors 메서드 {#updateAnchorsMethod}

updateAnchors 메서드를 사용하여 사이드화된 컨텐츠를 페이지에 동적으로 추가합니다.

이 방법은 페이지를 매기거나, 페이지에 sidecenote 가능 컨텐츠를 동적으로 추가하는 경우에 유용합니다. 이 메서드는 일치하는 요소에 대한 새 앵커를 정의하고 단일 인수를 사용합니다.newSelectors를 참조하십시오.

**newSelectors**. 사이드노트에 추가할 선택기입니다. 이것은 선택기 문자열, jQuery 객체 또는 요소 배열일 수 있습니다(앱 생성 중에 전달되는 selectors 인수로 허용되는 유형).
형식:

```
app.updateAnchors(newSelectors);
```

예:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
