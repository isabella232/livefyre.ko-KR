---
description: Livefyre. js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 발견할 수 있도록 합니다.
seo-description: Livefyre. js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 발견할 수 있도록 합니다.
seo-title: Livefyre ID 초기화
title: Livefyre ID 초기화
uuid: 9365 D 827-2734-4 A 84-BFE 7-9 BE 573 B 2 B 03 E
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID 초기화{#initialize-livefyre-identity}

Livefyre. js 인증 패키지는 페이지의 모든 소셜 구성 요소가 단일 인증 통합을 발견할 수 있도록 합니다.

Livefyre는 적절한 인증 위임 계약을 `lfep-auth-delegate` 수행하는 패키지를 제공합니다. auth 에는 로그인 및 로그아웃과 같은 인증 작업을 수행하는 방법을 아는 authdelegate 객체가 제공되어야 합니다.

1. livefyre. js를 웹 페이지에 추가합니다.
1. 이러한 작업을 Livefyre ID에 위임하도록 인증하려면 다음을 추가합니다.

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
