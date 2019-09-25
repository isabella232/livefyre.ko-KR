---
description: .js 구현을 사용하여 사이드노트를 구현합니다.
seo-description: .js 구현을 사용하여 사이드노트를 구현합니다.
seo-title: 사이드노트 구현
solution: Experience Manager
title: 사이드노트 구현
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 사이드노트 구현{#sidenotes-implementation}

## 방주 구현(.js 구현 사용)

이 기능을 구현하려면 재정의할 문자열의 1-1 개체 매핑을 Javascript 구성 개체에 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

### 예

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
