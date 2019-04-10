---
description: 사용자는 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있습니다.
seo-description: 사용자는 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있습니다.
seo-title: Change Collection
solution: Experience Manager
title: Change Collection
uuid: 81 C 8 A 554-375 F -4659-9 E 25-5 B 3618824633
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Change Collection {#change-collection}

사용자는 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있습니다.

Livefyre 앱이 이미 로드되어 있는 동안 변경 내용 모음 위임 기능을 사용하여 URL를 변경하지 않고 페이지에 표시되는 컬렉션을 변경합니다. 이 기능을 사용하여 사진 갤러리 또는 비디오 갤러리 또는 표시된 컬렉션이 사용자 동작 후에 바뀌는 다른 앱을 표시할 수 있습니다.

예를 들어 갤러리에서 비디오나 사진을 클릭하면 해당 선택 영역에 해당하는 컬렉션이 로드되고 페이지의 URL는 변경되지 않습니다.

[단일 페이지에서 세 컬렉션 중 하나를](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count)로드하려면:

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
