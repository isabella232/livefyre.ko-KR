---
description: Livefyre 앱에 사용자 정의 동작을 추가합니다.
seo-description: Livefyre 앱에 사용자 정의 동작을 추가합니다.
seo-title: 사용자 정의 단추 추가
solution: Experience Manager
title: 사용자 정의 단추 추가
uuid: 27d24c21-d8 파섹
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 사용자 정의 단추 추가{#add-custom-buttons}

Livefyre 앱에 사용자 정의 동작을 추가합니다.

Livefyre를 사용하면 컨텐츠 일부에서 기존 작업 단추(예: **[!UICONTROL Share]**&#x200B;및 **[!UICONTROL Flag]**) 옆에 사용자 정의 단추를 추가할 수 있습니다.

모바일 인수를 사용하여 단추를 모바일 장치에 표시할지 여부를 정의합니다.

예를 들어 모바일 장치 인터페이스에 대한 사용자 정의 작업 단추를 추가하려면:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. 추가하려는 각 단추를 설명하는 개체 배열을 포함하는 actionButtons라는 ConnectConfig 개체에 추가 인수를 전달합니다.
1. 각 단추에 대해 표시할 텍스트의 키를 정의합니다.
1. 각 단추에 대한 클릭 이벤트에 대해 호출할 콜백을 추가합니다.

콜백은 두 개의 키가 있는 개체와 함께 호출됩니다. `authorId` 및 `contentId`Adobe
