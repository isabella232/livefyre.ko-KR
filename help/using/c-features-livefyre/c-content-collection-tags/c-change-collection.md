---
description: 사용자가 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있도록 허용합니다.
seo-description: 사용자가 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있도록 허용합니다.
seo-title: 컬렉션 변경
solution: Experience Manager
title: 컬렉션 변경
uuid: 69bafcc7-c55e-47d6-bc79-b0db8 파섹
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 컬렉션 변경{#change-collection}

사용자가 단일 페이지 레이아웃 및 URL에서 컬렉션을 클릭스루할 수 있도록 허용합니다.

Livefyre 앱이 이미 로드되어 있는 동안 URL을 변경하지 않고 컬렉션 변경 위임을 사용하여 페이지에 표시된 컬렉션을 변경합니다. 이 기능을 사용하여 사진, 비디오 갤러리 또는 사용자 작업 후 표시되는 컬렉션이 변경되는 기타 앱을 표시할 수 있습니다.

예를 들어 갤러리에서 비디오나 사진을 클릭하면 해당 선택 항목에 대한 컬렉션이 로드되지만 페이지의 URL은 변경되지 않습니다.

단일 [댓글 수](/help/implementation/c-advanced-topics/t-display-comment-count.md) 페이지에서 세 개의 컬렉션 중 하나를 로드하려면:

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

