---
description: 하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.
seo-description: 하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.
seo-title: 여러 컬렉션
solution: Experience Manager
title: 여러 컬렉션
uuid: 9675 FFD 7-1 A 59-42 A 1-B 3 BA -40 AF 1744 CFD 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 여러 컬렉션 {#multiple-collections}

하나의 페이지에 여러 컬렉션을 표시할 수 있습니다.

사이트의 단일 페이지에 여러 컬렉션을 포함할 수 있습니다. 예를 들어 이벤트를 게시하려면 이벤트 중에 별도의 앱이 있는 이벤트 중에 라이브 블로그 또는 채팅 토론이 있을 수 있으며, 소셜 웹에서 관련된 선별된 컨텐츠가 표시됩니다. 또는 문서 아래에 채팅과 함께 댓글 앱을 포함할 수도 있습니다.

페이지에 대한 여러 대화를 가져오려면 배열에 하나 이상의 구성을 추가하고 이 배열을 로드 호출에 전달합니다. 예를 들어,

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
