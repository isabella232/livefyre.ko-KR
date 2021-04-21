---
description: 을 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

을 사용하여 비디오 마스크에 표시되는 경고 텍스트를 변경할 수 있습니다.

이 텍스트는 GDPR 규정을 준수하기 위해 존재합니다. 소스가 프록시를 지원하지 않을 경우 사용자가 비디오를 클릭하고 해당 소스로부터 잠재적인 추적을 승인하지 않는 경우 Livefyre는 이 텍스트와 마스크를 컨텐츠에 표시합니다.

`userPrivacyMaskDelegate`을 사용하지 않으면 다음 기본 텍스트가 표시됩니다.

`userPrivacyOptOut` 뒤에 `userPrivacyMaskDelegate`을 추가합니다. 모든 Livefyre 개인정보 보호 플래그를 하나의 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.

다음은 `userPrivacyMaskDelegate` 사용 방법의 예입니다.

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
