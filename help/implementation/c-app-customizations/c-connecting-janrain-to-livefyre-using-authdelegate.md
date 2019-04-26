---
description: Livefyre. require는 Auth가 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.
seo-description: Livefyre. require는 Auth가 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.
seo-title: Authdelegate를 사용하여 Janrain에 Livefyre 연결
title: Authdelegate를 사용하여 Janrain에 Livefyre 연결
uuid: 9 D 56 E 3 F 4-960 A -4108-AAB 5-2795 B 0 E 71 C 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Authdelegate를 사용하여 Janrain에 Livefyre 연결{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. require는 Auth가 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.

백플레인 채널에서 ID/로그인 메시지가 브로드캐스트되면 사용자의 Livefyre 인증 토큰을 통해 auth. authenticate () 가 호출됩니다. 여전히 Authdelegate를 구현해야 합니다.

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
>window. backplane 개체는 Livefyre Backplane 플러그인과 함께 auth. plugin를 호출하기 전에 페이지에서 정의해야 합니다. 백플레인 개체가 사용 가능한지 확인하려면 Onready 콜백에서 Livefyre 인스턴스화 코드를 호출합니다. 다른 애플리케이션이 백플레인 개체를 사용할 수 있는 시기를 결정하려면 Janrain 담당자에게 문의하십시오.

다음은 인증 위임자가 Janrain Capture 통합을 찾는 방법의 몇 가지 예입니다.

>[!NOTE]
>
>인증 위임은 Janrain 인스턴스에 따라 다릅니다.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 인증 대리인의 로그인 메서드에 전달된 콜백
* Janrain Capture 변수에 대한 참조입니다.
* : 백플레인 객체에 대한 참조입니다.

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

* **Finishlogout:** 인증 대리인의 로그인 메서드에 전달된 콜백.

* **window. backplane:** 백플레인 객체에 대한 참조입니다.

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

사용자가 방문하려는 사이트의 모든 부분으로 링크하여 자신의 프로필 페이지를 볼 수 있습니다. 이 예제는 전달된 작성자 개체를 출력합니다.

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

프로필 편집처럼, 이 작업은 현재 로그인한 사용자와 다른 사용자의 페이지로 링크해야 합니다. 그러나 이 방법은 제대로 구현될 수 있습니다. 이 예에서는 author 매개 변수를 콘솔에 기록합니다.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

