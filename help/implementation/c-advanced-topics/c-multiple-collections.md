---
description: 하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.
seo-description: 하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.
seo-title: 여러 컬렉션
solution: Experience Manager
title: 여러 컬렉션
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---


# 여러 컬렉션 {#multiple-collections}

하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.

사이트의 단일 페이지에 여러 컬렉션을 포함할 수 있습니다. 예를 들어, 이벤트를 게시하려면 이벤트 도중 개별 앱이 페이지 측면에 있는 라이브 블로그 또는 채팅 토론이 있을 수 있으며, 소셜 웹에서 관련 선별된 컨텐츠가 표시됩니다. 또는 옆쪽에 채팅 기능이 있는 아티클 아래에 댓글 앱을 포함할 수 있습니다.

한 페이지에서 여러 대화를 가져오려면 배열에 하나 이상의 구성을 추가하고 배열을 로드 호출에 전달합니다. 예.

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
