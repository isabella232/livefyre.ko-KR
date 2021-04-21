---
description: 통합 및 테스트 중에 콘솔을 통해 사용자를 로그인하여 권한을 디버깅할 수 있습니다.
title: 디버깅 인증 위임
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 인증 위임 디버깅{#debugging-auth-delegate}

통합 및 테스트 중에 콘솔을 통해 사용자를 로그인하여 권한을 디버깅할 수 있습니다.

다음 `auth.authenticate`(토큰)을 사용하여 사용자를 콘솔을 통해 로그인하고 Livefyre 사용자 토큰을 전달하여 페이지에서 사용자를 인증합니다.

위에 표시된 예제를 수정하고 JavaScript에서 다음 코드 조각을 온라인상으로 추가하여 사용자를 Livefyre(인증 참조 필요)에 빠르게 로그인할 수도 있습니다.

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
