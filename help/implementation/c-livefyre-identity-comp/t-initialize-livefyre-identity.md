---
description: Livefyre.js 인증 패키지는 페이지의 모든 소셜 구성 요소에서 단일 인증 통합을 검색할 수 있도록 합니다.
title: Livefyre ID 초기화
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Livefyre ID 초기화{#initialize-livefyre-identity}

Livefyre.js 인증 패키지는 페이지의 모든 소셜 구성 요소에서 단일 인증 통합을 검색할 수 있도록 합니다.

Livefyre는 적절한 인증 위임을 만들 `lfep-auth-delegate` 패키지를 제공합니다. 로그인 및 로그아웃 등의 인증 작업을 수행하는 방법을 알고 있는 AuthDelegate 객체를 AuthDelegate로 제공해야 합니다.

1. Livefyre.js를 웹 페이지에 추가합니다.
1. Livefyre ID에 이러한 작업을 위임하려면 다음을 추가합니다.

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
