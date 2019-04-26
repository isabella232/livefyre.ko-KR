---
description: Livefyre. js를 사용하여 Livefyre 앱에 대한 페이지 전체의 인증을 추가할 수 있습니다.
seo-description: Livefyre. js를 사용하여 Livefyre 앱에 대한 페이지 전체의 인증을 추가할 수 있습니다.
seo-title: Livefyre. js를 사용하여 앱에 Authetication 추가
solution: Experience Manager
title: Livefyre. js를 사용하여 앱에 Authetication 추가
uuid: B 7 C 61 E 07-E 341-45 D 7-9112-C 50155 E 38 F 1 D
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# livefyre. js를 사용하여 앱에 인증 추가{#add-authetication-to-an-app-using-livefyre-js}

Livefyre. js를 사용하여 Livefyre 앱에 대한 페이지 전체의 인증을 추가할 수 있습니다.

`Livefyre.js Aut`h는 Livefyre가 개발한 JavaScript 패키지로, 웹 사이트의 모든 앱은 단일 인증 통합을 공유할 수 있습니다. auth를 사용하면 사용자가 정의하는 authdelegate 개체에 이러한 흐름을 위임하여 사용자가 등록, 로그인 및 로그아웃하는 방법을 정의할 수 있습니다.

## 1 단계: 페이지에 대한 인증 활성화 {#section_pgp_jtt_bbb}

사용자가 기존 인증 시스템을 사용하여 로그인하고 앱과 상호 작용할 수 있도록 하기 위해 페이지에 대한 인증을 활성화하는 `Livefyre.js` 데 사용합니다.

1. 페이지에서 인증을 활성화하려면 웹 페이지 `Livefyre.js` 또는 웹 사이트 템플릿의 *< head >* 요소에 추가합니다.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 인증을 활성화하는 `Livefyre.require` 데 사용합니다. Using `Livefyre.require` is similar to call required to call other packages. 인증이 필요한 통합 코드는 다음과 같습니다.

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 2 단계: Authdelegate 등록 {#section_oqm_15t_bbb}

인증을 활성화하려면 인증을 `AuthDelegate` 만들어 `Livefyre.js` 인증으로 전달합니다.

는 `AuthDelegate` 사용자가 로그인하는 방법, 로그아웃 및 프로필 보기 방법을 결정하는 개체입니다.

1. 을 만듭니다 `AuthDelegate`. ID `AuthDelegate` 를 구성하는 방법은 ID 공급자에 따라 다릅니다. 자세한 내용은 ID 통합을 참조하십시오.

1. `AuthDelegate` To `Livefyre.js` Authentication를 전달합니다. 가장 간단한 `AuthDelegate` 로그는 사용자가 앱에서 위임된 로그인 메서드를 트리거할 때마다 동일한 사용자를 기록합니다.

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 3 단계: 사용자 데이터 동기화 {#section_u4m_j5t_bbb}

Livefyre와 ID 공급자 간에 사용자 프로필 정보를 동기화합니다.

Livefyre와 ID 공급자 간에 사용자 프로필 정보를 동기화해야 합니다. 자세한 내용은 [Janrain Capture 통합을](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)참조하십시오.
