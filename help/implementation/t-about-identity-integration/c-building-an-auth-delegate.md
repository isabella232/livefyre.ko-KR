---
description: AuthDelegate 객체는 인증 작업 및 이벤트를 수행하는 방법에 대한 원하는 동작을 구현하므로 사이트의 기존 인증 시스템과의 통합을 사용자 정의할 수 있습니다.
seo-description: AuthDelegate 객체는 인증 작업 및 이벤트를 수행하는 방법에 대한 원하는 동작을 구현하므로 사이트의 기존 인증 시스템과의 통합을 사용자 정의할 수 있습니다.
seo-title: AuthDelegate 개체
solution: Experience Manager
title: AuthDelegate 개체
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# AuthDelegate 개체{#authdelegate-object}

AuthDelegate 객체는 인증 작업 및 이벤트를 수행하는 방법에 대한 원하는 동작을 구현하므로 사이트의 기존 인증 시스템과의 통합을 사용자 정의할 수 있습니다.

## 인증 위임 만들기 {#section_wmn_tv2_gz}

인증 패키지가 작업을 수행하려면 인증 대리자와 함께 제공해야 합니다. 인증 대리자는 이 주제의 메서드 중 하나를 구현하는 JavaScript 객체입니다.

## .login(finishLogin) {#section_mpk_lv2_gz}

유효한 사용자에 로그인하고 오류가 있는 경우 Error 객체 또는 사용자의 Livefyre 자격 증명을 사용하여 finishLogin 함수를 호출합니다. 이 방법의 일반적인 구현은 사용자를 로그인 페이지로 리디렉션하거나 새 창 또는 모달을 엽니다.

이 예제는 인증 토큰, 토큰을 사용하여 Livefyre 사용자의 인증에 자동으로 알립니다.

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

가장 간단한 로그인 위임은 최종 사용자에게 Livefyre 인증 토큰을 요청할 수 있습니다.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finishLogout) {#section_uqz_2v2_gz}

사용자를 로그아웃하고 오류가 있는 경우 Error 객체로 finishLogout 함수를 호출하거나 로그아웃을 성공적으로 알리는 데 null을 호출합니다.

예:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

사용자 프로필을 보는 동작을 수행합니다.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

사용자 프로필을 편집하는 동작을 수행합니다.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

위에 나열된 모든 방법을 구현함으로써 사용자 정의 인증 위임으로 인증을 구성할 수 있습니다. 위임을 구성한 후에는 위임 방법을 사용하여 인증에 위임을 제공할 수 있습니다.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

