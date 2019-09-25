---
description: 통합 및 테스트 중에 콘솔을 통해 사용자를 로그인하여 인증을 디버깅할 수 있습니다.
seo-description: 통합 및 테스트 중에 콘솔을 통해 사용자를 로그인하여 인증을 디버깅할 수 있습니다.
seo-title: 디버깅 인증 위임
solution: Experience Manager
title: 디버깅 인증 위임
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 디버깅 인증 위임{#debugging-auth-delegate}

통합 및 테스트 중에 콘솔을 통해 사용자를 로그인하여 인증을 디버깅할 수 있습니다.

다음 `auth.authenticate` (토큰)을 사용하여 콘솔을 통해 사용자를 로그인하고 Livefyre 사용자 토큰을 전달하여 페이지에서 사용자를 인증합니다.

또한 위에 표시된 예제를 수정하고 JavaScript에서 다음 코드 조각을 추가하여 사용자를 Livefyre에 빠르게 로그인할 수 있습니다(인증에 대한 참조 필요).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

