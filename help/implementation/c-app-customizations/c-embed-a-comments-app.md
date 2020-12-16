---
description: 댓글 앱을 포함시키는 것은 핵심 앱을 포함시키는 과정을 따릅니다.
seo-description: 댓글 앱을 포함시키는 것은 핵심 앱을 포함시키는 과정을 따릅니다.
seo-title: 댓글 앱 포함
solution: Experience Manager
title: 댓글 앱 포함
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# 주석 앱 포함{#embed-a-comments-app}

댓글 앱을 포함시키는 것은 핵심 앱을 포함시키는 과정을 따릅니다.

댓글 앱 포함은 [앱 포함](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)에 설명된 핵심 앱을 포함하는 프로세스를 따릅니다.

## 예

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

CollectionMeta 빌드 섹션에 설명된 대로 CollectionMeta는 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT로 인코딩되기 전에 다음 형식을 사용합니다.

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

