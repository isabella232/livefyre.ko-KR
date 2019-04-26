---
seo-title: 앱 포함
solution: Experience Manager
title: 앱 포함
uuid: E 75 CAF 0 E -04 EA -4 B 04-89 ED-FEA 1183 ECF 63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 앱 포함{#embed-an-app}

Livefyre. js 임베드 코드 구조를 사용하여 Livefyre 앱을 웹 페이지에 추가합니다.

이 설명서는 기술 사용자를 위한 것입니다. For [non-technical information about Apps](/help/using/c-about-apps/c-about-apps.md).

이 섹션에서는 사이트에 Livefyre 앱을 내장하기 위해 페이지 템플릿에 포함해야 하는 코드 구조에 대해 설명합니다.

1. Livefyre 자리 표시자로.html 파일을 만듭니다.

   원하는 텍스트 편집기에서 새.html 파일을 만듭니다. 앱이 포함될 자리 표시자 Livefyre `<div>` 요소를 만듭니다.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. livefyre. js 라이브러리를 포함합니다.

   Livefyre JS 라이브러리를 포함합니다. 요소의 `<script>` 요소에 다음 참조를 `<head>` 배치합니다. 브라우저에서 페이지를 열고 브라우저의 웹 관리자를 사용하여 Livefyre가 로드되었는지 확인합니다.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Livefyre 앱을 제작합니다.

   사용하려는 Livefyre 패키지에 전달하여 Core 및 SDK 앱을 모두 구성하는 `Livefyre.require` 데 사용합니다.

   1. 핵심 앱 구축

      핵심 앱 (댓글, 라이브 블로그 또는 채팅) 를 만들려면 다음 구조를 사용하십시오.

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. SDK 앱을 빌드합니다.

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

      특정 앱에 대한 [자세한](/help/using/c-about-apps/c-about-apps.md)내용을 참조하십시오. 예기치 않게 끊어진 통합을 방지하려면 패키지의 최신 주요 버전 ( [Livefyre. require](https://cdn.livefyre.com/packages.html)) 에 고정하는 것이 좋습니다.

다음: 사이트에 인증을 추가하여 사용자가 댓글을 게시할 수 있도록 합니다.
