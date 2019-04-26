---
description: 통합 및 테스트 동안 콘솔을 통해 사용자를 로그인하여 권한을 디버그할 수 있습니다.
seo-description: 통합 및 테스트 동안 콘솔을 통해 사용자를 로그인하여 권한을 디버그할 수 있습니다.
seo-title: 디버깅 인증 위임
solution: Experience Manager
title: 디버깅 인증 위임
uuid: FB 0 C 7396-190 E -4 DC 9-BF 26-23 DDE 9 EFD 45 D
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 디버깅 인증 위임{#debugging-auth-delegate}

통합 및 테스트 동안 콘솔을 통해 사용자를 로그인하여 권한을 디버그할 수 있습니다.

다음 `auth.authenticate` (토큰) 를 사용하여 콘솔에서 사용자를 로그인하고 Livefyre 사용자 토큰을 전달하여 페이지에서 사용자를 인증합니다.

또한 위에 표시된 예제를 수정하고 JavaScript에 인라인 코드를 추가하여 사용자를 Livefyre에 빠르게 기록할 수 있습니다 (auth에 대한 참조가 필요).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

