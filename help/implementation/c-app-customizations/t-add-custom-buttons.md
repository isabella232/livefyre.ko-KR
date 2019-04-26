---
description: Livefyre 앱에 맞춤형 액션을 추가할 수 있습니다.
seo-description: Livefyre 앱에 맞춤형 액션을 추가할 수 있습니다.
seo-title: 사용자 정의 단추 추가
solution: Experience Manager
title: 사용자 정의 단추 추가
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 사용자 정의 단추 추가{#add-custom-buttons}

Livefyre 앱에 맞춤형 액션을 추가할 수 있습니다.

Livefyre를 사용하면 컨텐츠의 기존 작업 단추 (예 **[!UICONTROL Share]**: 및 **[!UICONTROL Flag]**) 옆에 사용자 정의 단추를 추가할 수 있습니다.

mobile 인수를 사용하여 단추가 모바일 장치에 표시되는지 여부를 정의합니다.

예를 들어 모바일 장치 인터페이스에 대한 사용자 정의 작업 단추를 추가하려면 다음을 수행하십시오.

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

1. 추가할 각 버튼에 대해 설명하는 객체 배열을 포함하여 Actionbuttons 라는 convconfig 개체에서 추가 인수를 전달합니다.
1. 각 단추에 대해 표시할 텍스트의 키를 정의합니다.
1. 각 단추에 대해 클릭 이벤트에서 호출할 콜백을 추가합니다.

콜백은 두 개의 키가 있는 객체로 호출됩니다. `authorId` `contentId`And.
