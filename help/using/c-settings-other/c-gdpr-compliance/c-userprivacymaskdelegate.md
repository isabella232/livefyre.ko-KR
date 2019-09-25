---
description: 를 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.
seo-description: 를 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

를 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.

이 텍스트는 GDPR 규정을 준수하기 위해 존재합니다. 소스가 프록시를 지원하지 않는 경우 사용자가 비디오를 클릭하고 해당 소스에서 잠재적 추적을 승인하지 않는 한 Livefyre는 이 텍스트와 마스크를 컨텐츠에 표시합니다.

사용하지 않는 `userPrivacyMaskDelegate`경우 다음 기본 텍스트가 표시됩니다.

이후 `userPrivacyMaskDelegate` 추가를 `userPrivacyOptOut`참조하십시오. 모든 Livefyre 개인정보 보호 플래그를 한 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.

다음은 사용 방법에 대한 `userPrivacyMaskDelegate`예입니다.

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
