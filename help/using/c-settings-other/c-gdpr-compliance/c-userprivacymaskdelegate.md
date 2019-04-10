---
description: 을 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.
seo-description: 을 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 E 5 A 2750-BF 45-4 E 70-A 5 F 9-37 F 5 E 7 C 61 F 8 E
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

을 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.

GDPR 규정을 준수하는 텍스트입니다. 소스에서 프록시를 지원하지 않으면 사용자가 비디오를 클릭해서 해당 소스에서 잠재적 추적을 승인하지 않는 한 Livefyre는 이 텍스트와 마스크를 표시합니다.

사용하지 않으면 다음과 같은 `userPrivacyMaskDelegate`기본 텍스트가 표시됩니다.

이후에 `userPrivacyMaskDelegate` 추가합니다 `userPrivacyOptOut`. Livefyre의 모든 개인정보 보호 플래그를 하나의 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.

`userPrivacyMaskDelegate`다음은 사용 방법의 예입니다.

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
