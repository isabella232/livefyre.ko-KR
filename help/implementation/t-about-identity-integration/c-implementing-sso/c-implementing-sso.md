---
description: Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 인증하기 위해 Livefyre는 authdelegate
  개체에 foreachauthentication 메서드를 구현하도록 권장합니다.
seo-description: Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 인증하기 위해 Livefyre는 authdelegate
  개체에 foreachauthentication 메서드를 구현하도록 권장합니다.
seo-title: SSO 구현
solution: Experience Manager
title: SSO 구현
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SSO 구현{#implementing-sso}

Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 인증하기 위해 Livefyre는 authdelegate 개체에 foreachauthentication 메서드를 구현하도록 권장합니다.

이 메서드는에 `authDelegate` 전달될 때 `auth.delegate`호출되며, 전달할 수 있는 인증 함수에 전달됩니다. 이 방법은 인증 이벤트에 대한 제어 기능을 제공하므로 인증에 `AuthDelegateobject` 대한 글로벌 참조 없이 자체 포함될 수 있습니다.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre는 사용자 토큰을 사용하여 인증을 조정합니다. 따라서 Livefyre를 사용하여 사용자를 인증하려면 ID 서비스에서 이 토큰을 반환해야 합니다. Livefyre 사용자 토큰을 만드는 방법에 대한 자세한 내용은 사용자 인증 토큰 빌드를 참조하십시오.

>[!NOTE]
>
>로그인 성공 후 AUTH는 사용자를 위한 세션을 만들고 페이지를 새로 고치고 다시 로드하면 사용자의 세션을 로드합니다. `auth.logout()` 이 세션을 지웁니다. 즉, 권한 부여와는 별도로 사용자의 세션을 관리할 필요가 없습니다.

