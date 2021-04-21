---
description: Livefyre.require는 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.
title: AuthDelegate를 사용하여 Janrain을 Livefyre에 연결
exl-id: d0fe0e88-5827-478b-b2ef-03f06fb3902c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}을(를) 사용하여 Janrain을 Livefyre에 연결

Livefyre.require는 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.

ID/로그인 메시지가 백플레인 채널에서 브로드캐스트되면 사용자의 Livefyre 인증 토큰으로 auth.authenticate()가 호출됩니다. 여전히 AuthDelegate를 구현해야 합니다.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>window.Backplane 개체는 Livefyre 백플레인 플러그인으로 auth.plugin을 호출하기 전에 페이지에 정의해야 합니다. 백플레인 개체를 사용할 수 있는지 확인하려면 onReady 콜백에서 Livefyre 인스턴스화 코드를 호출합니다. 다른 응용 프로그램에서 후면판 개체를 사용할 수 있는 시기를 확인하려면 Jannain 담당자에게 문의하십시오.

다음은 인증 대리인이 Janrain Capture 통합을 찾는 방법에 대한 몇 가지 예입니다.

>[!NOTE]
>
>인증 위임은 Janrain 인스턴스에 따라 달라집니다.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 인증 대리인의 로그인 메서드에 전달된 콜백
* Janrain 캡처 변수에 대한 참조입니다.
* :후면판 개체에 대한 참조입니다.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

로그아웃

* **finishLogout:** 인증 대리인의 로그인 메서드에 전달된 콜백입니다.

* **window.백플레인:** 백플레인 개체에 대한 참조입니다.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

프로필 편집

이 링크는 사용자가 자신의 프로필 페이지를 보기 위해 방문하려는 사이트의 어느 부분이든지 링크할 수 있습니다. 이 예는 전달된 작성자 개체만 인쇄합니다.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

프로필 보기

프로필 편집과 같이, 현재 로그인한 사용자와 다른 사용자의 페이지에 링크해야 합니다. 이 작업은 사용자가 원하는 대로 실행할 수 있습니다. 이 예제에서는 작성자 매개 변수를 콘솔에 간단하게 기록합니다.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```
