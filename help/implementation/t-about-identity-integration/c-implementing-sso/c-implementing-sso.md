---
description: Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 사용하여 사용자를 인증하려면 AuthDelegate 개체에 forEachAuthentication 메서드를 구현하는 것이 좋습니다.
seo-description: Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 사용하여 사용자를 인증하려면 AuthDelegate 개체에 forEachAuthentication 메서드를 구현하는 것이 좋습니다.
seo-title: SSO 구현
solution: Experience Manager
title: SSO 구현
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SSO 구현{#implementing-sso}

Livefyre 앱에서 트리거되지 않는 흐름을 통해 Livefyre를 사용하여 사용자를 인증하려면 AuthDelegate 개체에 forEachAuthentication 메서드를 구현하는 것이 좋습니다.

이 메서드는 `authDelegate` 가 전달될 때 호출되며, 여러 번 전달할 수 있는 인증 함수를 `auth.delegate`전달합니다. 이 메서드는 인증에 대한 전역 참조 없이도 사용자가 직접 포함할 `AuthDelegateobject` 수 있도록 인증 이벤트에 대한 컨트롤 버전을 제공합니다.

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
>로그인이 성공하면 auth는 사용자를 위한 세션을 만들고 페이지 새로 고침 및 다시 로드 시 사용자의 세션을 로드합니다. `auth.logout()` 이 세션을 지웁니다. 즉, 인증과 별도로 사용자의 세션을 관리할 필요가 없습니다.

