---
description: Livefyre.js를 사용하여 Livefyre 앱에 대한 페이지 전체 인증을 추가합니다.
title: Livefyre.js를 사용하여 앱에 인증 추가
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}를 사용하여 앱에 인증 추가

Livefyre.js를 사용하여 Livefyre 앱에 대한 페이지 전체 인증을 추가합니다.

`Livefyre.js Aut`h는 웹 사이트의 모든 앱이 단일 인증 통합을 공유할 수 있도록 하는 Livefyre에서 개발한 JavaScript 패키지입니다. Auth를 사용하면 사용자가 정의한 AuthDelegate 개체에 이러한 흐름을 위임하여 사용자의 등록, 로그인 및 로그아웃하는 방법을 정의할 수 있습니다.

## 1단계:페이지 {#section_pgp_jtt_bbb}에 대한 인증 활성화

사용자가 로그인하고 기존 인증 시스템을 사용하여 앱과 상호 작용할 수 있도록 하려면 `Livefyre.js`을 사용하여 페이지에 대한 인증을 활성화합니다.

1. 페이지에서 인증을 활성화하려면 웹 페이지 또는 웹 사이트 템플릿의 *&lt;head>* 요소에 `Livefyre.js`을(를) 추가하십시오.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 인증을 활성화하려면 `Livefyre.require`을(를) 사용합니다. `Livefyre.require`을(를) 사용하는 것은 다른 패키지를 호출하는 데 필요한 사용과 유사합니다. 인증이 필요한 통합 코드는 다음과 같습니다.

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 2단계:AuthDelegate 등록 {#section_oqm_15t_bbb}

인증을 활성화하려면 `AuthDelegate`을(를) 만들고 `Livefyre.js` 인증에 전달합니다.

`AuthDelegate`은 사용자가 로그인하고, 로그아웃하고, 프로필을 보는 방법을 결정하는 객체입니다.

1. AdBox `AuthDelegate`. `AuthDelegate`을 구성하는 방법은 ID 공급자에 따라 다릅니다. 자세한 내용은 ID 통합을 참조하십시오.

1. `AuthDelegate`을(를) `Livefyre.js` 인증에 전달합니다. 가장 간단한 `AuthDelegate`은 사용자가 앱에서 위임된 로그인 메서드를 트리거할 때마다 동일한 사용자를 기록합니다.

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 3단계:사용자 데이터 동기화 {#section_u4m_j5t_bbb}

Livefyre와 ID 공급자 간에 사용자 프로필 정보를 동기화합니다.

Livefyre와 ID 공급자 간에 사용자 프로필 정보를 동기화해야 합니다. 자세한 내용은 [Janrain Capture 통합](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)을 참조하십시오.
