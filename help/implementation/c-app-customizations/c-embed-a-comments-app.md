---
description: 댓글 앱을 임베드하면 핵심 앱을 임베드하는 프로세스가 따릅니다.
seo-description: 댓글 앱을 임베드하면 핵심 앱을 임베드하는 프로세스가 따릅니다.
seo-title: 주석 앱 포함
solution: Experience Manager
title: 주석 앱 포함
uuid: E 4982 AD 3-CAB 1-4805-A 55 C -594 CCA 3 B 7203
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 주석 앱 포함{#embed-a-comments-app}

댓글 앱을 임베드하면 핵심 앱을 임베드하는 프로세스가 따릅니다.

댓글 앱을 임베드하면 앱 [임베드에 설명된 핵심 앱 임베드에 대한 프로세스가 따릅니다.](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

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

Building collectionmeta section에 명시된 대로 collectionmeta는 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT 인코딩하기 전에 다음 형식을 사용합니다.

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

