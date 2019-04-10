---
description: 사이트에서 Livefyre를 강화하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-description: 사이트에서 Livefyre를 강화하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-title: Updateanchors 메서드
solution: Experience Manager
title: livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Updateanchors 메서드 {#updateAnchorsMethod}

Updateanchors 메서드를 사용하여 페이지에 동적 내용을 동적으로 추가합니다.

이 방법은 페이지 매김을 수행하는 데 유용합니다. 그렇지 않으면 시트워크북 가능 컨텐츠가 페이지에 동적으로 추가됩니다. 이 메서드는 일치하는 요소에 대한 새 앵커를 정의하고 단일 인수를 사용합니다. Newselector.

**Newselector**. Sidenotes에 추가할 선택기입니다. 선택기 문자열, Jquery 오브젝트 또는 요소 배열 (앱 빌드 중에 전달된 선택기 인수로 허용되는 유형 중 하나) 이 될 수 있습니다.
형식:

```
app.updateAnchors(newSelectors);
```

예:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
