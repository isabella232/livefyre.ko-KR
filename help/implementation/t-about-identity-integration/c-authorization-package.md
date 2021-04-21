---
description: 사용자가 앱과 상호 작용할 수 있도록 사용자 인증을 활성화하려면 인증 패키지를 설치합니다.
title: 인증 패키지
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# 인증 패키지{#authentication-package}

사용자가 앱과 상호 작용할 수 있도록 사용자 인증을 활성화하려면 인증 패키지를 설치합니다.

Livefyre 앱은 글로벌 인증 패키지를 사용하여 사용자를 앱 동작과 연결합니다. 인증 패키지는 `Livefyre.require`을 통해 사용할 수 있습니다.

페이지에서 인증을 활성화하려면 먼저 웹 페이지 또는 웹 사이트 템플릿의 `<head>` 요소에 `Livefyre.js`을(를) 추가하십시오.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Livefyre.require를 사용하여 인증 활성화는 다른 패키지를 호출하는 데 사용하는 사용과 유사합니다. 인증이 필요한 통합 코드는 다음과 같습니다.

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 메서드{#section_ojx_1lz_fz}에서 사용할 수 있습니다 

위에 `Livefyre.require`을(를) 사용하여 포함되면 인증 모듈에는 인증 관련 이벤트에 대해 페이지의 다른 앱에 알리기 위해 호출할 수 있는 다음 방법이 표시됩니다.

| 메서드 | 설명 |
|--- |--- |
| `.login(callback)` | 등록된 AuthDelegate에 의해 구현된 로그인 흐름을 트리거합니다. 일반적으로 인증 사용 앱만 이 호출을 사용하며 호스트 페이지 자체가 아닙니다. |
| `.logout(callback)` | 최종 사용자가 외부 방법으로 로그아웃했으며 모든 신뢰 앱은 다음 로그인 전까지 인증 상태를 지워야 한다는 것을 인증 시 알립니다. 이렇게 하면 Auth에서 유지 관리하는 내부 세션이 지워집니다. |
| `.authenticate(credentials)` | 사용자가 일부 외부 방법으로 인증했으며 최종 사용자에 대해 Livefyre 인증 토큰이 획득되었음을 Auth에 알립니다. Livefyre 토큰으로 쿠키를 설정하거나 사용자를 위한 토큰이 있고 사용자를 명시적으로 로그인하려는 경우 이 옵션을 사용합니다. 예: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 인증(예: 사용자 정의 인증 흐름)의 구현 세부 정보를 사용자가 정의한 객체에 위임할 수 있습니다. Livefyre 앱의 대화형 기능을 활성화하려면 호스트 페이지에서 호출해야 합니다. |
