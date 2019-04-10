---
description: . js 구현을 사용하여 Sidenotes를 구현합니다.
seo-description: . js 구현을 사용하여 Sidenotes를 구현합니다.
seo-title: Sidenotes 구현
solution: Experience Manager
title: Sidenotes 구현
uuid: AA 13852 E-E 2 B 0-4 A 86-97 CD-D 08 AB 5 E 2 CFAB
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes 구현{#sidenotes-implementation}

## 방주 구현(.js 구현 사용)

이 기능을 구현하려면 Javascript 구성 개체로 재정의할 문자열의 1-1 개체 매핑을 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

### 예

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
