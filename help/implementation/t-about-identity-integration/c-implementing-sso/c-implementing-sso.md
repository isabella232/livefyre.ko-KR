---
description: Livefyre 앱에서 트리거하지 않는 흐름을 통해 Livefyre를 통해 사용자를 인증하려면 AuthDelegate 개체에 forEachAuthentication 메서드를 구현하는 것이 좋습니다.
title: SSO 구현
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# SSO 구현{#implementing-sso}

Livefyre 앱에서 트리거하지 않는 흐름을 통해 Livefyre를 통해 사용자를 인증하려면 AuthDelegate 개체에 forEachAuthentication 메서드를 구현하는 것이 좋습니다.

이 메서드는 `authDelegate`이(가) `auth.delegate`에 전달될 때 호출되며, 여러 번 전달할 수 있는 인증 함수를 전달합니다. 이 메서드는 인증에 대한 전역 참조 없이 `AuthDelegateobject`을 자체 포함할 수 있도록 인증 이벤트에 대한 제어 버전을 제공합니다.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre는 사용자 토큰으로 인증을 조율합니다. 따라서 Livefyre를 사용하여 사용자를 인증하려면 ID 서비스에서 이 토큰을 반환해야 합니다. Livefyre 사용자 토큰을 만드는 방법을 알아보려면 사용자 인증 토큰 빌드를 참조하십시오.

>[!NOTE]
>
>로그인이 성공하면 auth는 사용자에 대한 세션을 만들고 페이지 새로 고침 및 다시 로드 시 사용자의 세션을 로드합니다. `auth.logout()` 이 세션을 지웁니다. 이는 인증과 별도로 사용자의 세션을 관리할 필요가 없음을 의미합니다.
