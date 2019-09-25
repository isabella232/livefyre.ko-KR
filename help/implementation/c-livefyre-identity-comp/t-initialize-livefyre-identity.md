---
description: Livefyre.js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 검색할 수 있도록 합니다.
seo-description: Livefyre.js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 검색할 수 있도록 합니다.
seo-title: Livefyre ID 초기화
title: Livefyre ID 초기화
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID 초기화{#initialize-livefyre-identity}

Livefyre.js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 검색할 수 있도록 합니다.

Livefyre는 적절한 인증 위임을 만드는 `lfep-auth-delegate` 패키지를 제공합니다. 인증은 로그인 및 로그아웃 등의 인증 작업을 수행하는 방법을 알고 있는 AuthDelegate 개체를 제공해야 합니다.

1. Livefyre.js를 웹 페이지에 추가합니다.
1. Auth에 이러한 작업을 Livefyre Id에 위임하려면 다음을 추가하십시오.

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
