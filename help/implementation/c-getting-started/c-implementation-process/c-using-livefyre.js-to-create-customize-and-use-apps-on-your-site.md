---
seo-title: 앱 포함
solution: Experience Manager
title: 앱 포함
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 앱{#embed-an-app} 포함

Livefyre.js 임베드 코드 구조를 사용하여 웹 페이지에 Livefyre 앱을 추가할 수 있습니다.

이 설명서는 기술 사용자를 위한 것입니다. [Apps](/help/using/c-about-apps/c-about-apps.md)에 대한 기술적 정보가 아닌 경우.

이 섹션에서는 사이트에 Livefyre 앱을 포함하기 위해 페이지 템플릿에 포함해야 하는 코드 구조에 대해 설명합니다.

1. Livefyre 자리 표시자로 .html 파일을 만듭니다.

   원하는 텍스트 편집기에서 새 .html 파일을 만듭니다. 앱이 포함될 자리 표시자 Livefyre `<div>` 요소를 만듭니다.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Livefyre.js 라이브러리를 포함합니다.

   그런 다음 Livefyre JS 라이브러리를 포함합니다. `<head>` 요소의 `<script>` 요소에 다음 참조를 배치합니다. 그런 다음 브라우저에서 페이지를 열고 브라우저의 웹 관리자를 사용하여 Livefyre가 로드되었는지 확인합니다.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Livefyre 앱을 빌드합니다.

   사용하려는 Livefyre 패키지를 전달하여 `Livefyre.require`을(를) 사용하여 핵심 앱과 SDK 앱을 모두 구성합니다.

   1. 핵심 앱 빌드를 참조하십시오.

      핵심 앱(댓글, 라이브 블로그 또는 채팅)을 빌드하려면 다음 구조를 사용합니다.

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. SDK 앱 빌드를 참조하십시오.

      미디어 담벼락 또는 피드와 같은 SDK 앱을 빌드하려면 다음 구조를 사용하십시오.

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      특정 앱](/help/using/c-about-apps/c-about-apps.md)에 대한 자세한 내용은 [을 참조하십시오. 예기치 않은 통합이 손상되지 않도록 하려면 패키지의 최신 주요 버전([Livefyre.require](https://cdn.livefyre.com/packages.html)를 통해 찾을 수 있음)에 고정하는 것이 좋습니다.

다음:사용자가 댓글을 게시할 수 있도록 사이트에 인증을 추가합니다.
