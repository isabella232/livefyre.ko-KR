---
description: 사용자가 앱과 상호 작용할 수 있도록 사용자 인증을 활성화하려면 인증 패키지를 설치합니다.
seo-description: 사용자가 앱과 상호 작용할 수 있도록 사용자 인증을 활성화하려면 인증 패키지를 설치합니다.
seo-title: 인증 패키지
solution: Experience Manager
title: 인증 패키지
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 인증 패키지{#authentication-package}

사용자가 앱과 상호 작용할 수 있도록 사용자 인증을 활성화하려면 인증 패키지를 설치합니다.

Livefyre 앱은 전역 인증 패키지를 사용하여 사용자를 앱 동작과 연결합니다. 인증 패키지는 를 통해 사용할 수 `Livefyre.require`있습니다.

페이지에서 인증을 활성화하려면 먼저 웹 페이지 또는 웹 사이트 템플릿의 `Livefyre.js` 요소에 `<head>` 추가하십시오.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Livefyre.require를 사용하여 인증 활성화는 다른 패키지를 호출하는 데 필요한 사용과 유사합니다. 인증이 필요한 통합 코드는 다음과 같습니다.

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 메서드{#section_ojx_1lz_fz}에서 사용할 수 있습니다 

상기와 같이 `Livefyre.require`포함되면, 인증 모듈에서는 호출한 다음 방법을 통해 인증 관련 이벤트에 대해 페이지의 다른 앱에 알릴 수 있습니다.

| 메서드 | 설명 |
|--- |--- |
| `.login(callback)` | 등록된 AuthDelegate에 의해 구현된 로그인 흐름을 트리거합니다. 일반적으로 인증만 활성화된 앱은 호스트 페이지 자체가 아니라 이 앱을 호출합니다. |
| `.logout(callback)` | 최종 사용자가 외부 방법으로 로그아웃했으며 모든 신뢰 앱이 다음 로그인 시까지 인증 상태를 지워야 함을 인증 인증에 알립니다. 이렇게 하면 Auth에서 유지 관리하는 내부 세션이 지워집니다. |
| `.authenticate(credentials)` | 사용자가 외부 방법으로 인증되었으며 최종 사용자에 대해 Livefyre 인증 토큰이 획득되었음을 Auth에 알립니다. Livefyre 토큰으로 쿠키를 설정하거나 사용자에 대한 토큰이 있고 사용자를 명시적으로 로그인하려는 경우 이 옵션을 사용합니다. 예: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 사용자 정의 인증 흐름과 같은 인증에 대한 구현 세부 사항을 사용자가 정의한 개체에 위임합니다. Livefyre 앱의 대화형 기능을 활성화하려면 호스트 페이지에서 호출해야 합니다. |

