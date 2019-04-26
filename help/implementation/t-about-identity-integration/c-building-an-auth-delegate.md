---
description: Authdelegate 개체는 인증 작업 및 이벤트를 수행하는 방법에 대해 원하는 비헤이비어를 구현하므로 사이트의 기존 인증
  시스템과의 통합을 사용자 정의할 수 있습니다.
seo-description: Authdelegate 개체는 인증 작업 및 이벤트를 수행하는 방법에 대해 원하는 비헤이비어를 구현하므로 사이트의 기존
  인증 시스템과의 통합을 사용자 정의할 수 있습니다.
seo-title: Authdelegate 개체
solution: Experience Manager
title: Authdelegate 개체
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Authdelegate 개체{#authdelegate-object}

Authdelegate 개체는 인증 작업 및 이벤트를 수행하는 방법에 대해 원하는 비헤이비어를 구현하므로 사이트의 기존 인증 시스템과의 통합을 사용자 정의할 수 있습니다.

## 인증 위임 만들기 {#section_wmn_tv2_gz}

인증 위임은 작업을 수행하기 전에 인증 위임과 함께 제공해야 합니다. 인증 위임은 이 주제의 메서드 중 하나를 구현하는 모든 JavaScript 개체입니다.

## . login (finishlogin) {#section_mpk_lv2_gz}

유효한 사용자에 로그인하고 오류가 있는 경우 오류 개체 또는 사용자의 Livefyre 자격 증명을 사용하여 finishlogin 함수를 호출합니다. 이 메서드의 일반적인 구현은 사용자를 로그인 페이지로 리디렉션하거나 새 창 또는 모달 양식을 엽니다.

이 예에서는 인증 토큰을 사용하여 Livefyre 사용자에게 토큰을 자동으로 알립니다. 토큰:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

가장 간단한 로그인 위임자는 최종 사용자에게 Livefyre 인증 토큰을 요청할 수 있습니다.

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

## . logout (finishlogout) {#section_uqz_2v2_gz}

오류가 있는 경우 Error 객체를 사용하여 사용자 로그아웃 및 finishlogout 함수를 호출하거나, 로그아웃이 성공했음을 인증하려면 null를 호출합니다.

예를 들면 다음과 같습니다.

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (사용자) {#section_kkv_dv2_gz}

사용자의 프로필을 보려면 조치를 취합니다.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (사용자) {#section_bkx_pq2_gz}

사용자의 프로필을 편집하는 작업을 수행합니다.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

위에 나열된 모든 메서드를 구현함으로써 AUTH를 사용자 지정 인증 위임으로 구성할 수 있습니다. 위임이 구성되면 위임 메서드를 사용하여 인증 권한을 인증할 수 있습니다.

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

