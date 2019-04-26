---
description: 사용자가 앱과 상호 작용할 수 있도록 인증 패키지를 설치합니다.
seo-description: 사용자가 앱과 상호 작용할 수 있도록 인증 패키지를 설치합니다.
seo-title: 인증 패키지
solution: Experience Manager
title: 인증 패키지
uuid: 4 EEC 30 CF -66 B 6-408 D -985 D -3 E 23 B 8 B 70 D 01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 인증 패키지{#authentication-package}

사용자가 앱과 상호 작용할 수 있도록 인증 패키지를 설치합니다.

Livefyre 앱은 글로벌 인증 패키지를 사용하여 사용자를 앱 작업과 연결합니다. 인증 패키지는 `Livefyre.require`을 통해 사용할 수 있습니다.

페이지에서 인증을 활성화하려면 먼저 웹 페이지 `Livefyre.js` 또는 웹 사이트 템플릿의 `<head>` 요소에 추가합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Livefyre를 사용하는 경우 AUTH를 활성화해야 하는 것은 다른 패키지를 호출해야 하는 것과 비슷합니다. 인증이 필요한 통합 코드는 다음과 같습니다.

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 메서드 {#section_ojx_1lz_fz}

위와 `Livefyre.require`같이 포함된 인증 모듈은 인증 관련 이벤트에 대해 페이지에 다른 앱을 알리기 위해 호출할 수 있는 다음 방법을 표시합니다.

| 메서드 | 설명 |
|--- |--- |
| `.login(callback)` | 등록된 Authdelegate에 의해 구현된 로그인 흐름을 트리거합니다. 일반적으로 인증이 활성화된 앱은 호스트 페이지 자체가 아닌 이 이름을 호출합니다. |
| `.logout(callback)` | 최종 사용자가 일부 외부 수단으로 로그아웃했고, 모든 신뢰 앱이 다음 로그인할 때까지 인증 상태를 지워야 한다는 점을 인증합니다. 이렇게 하면 auth로 유지 관리되는 내부 세션이 지워집니다. |
| `.authenticate(credentials)` | 사용자가 일부 외부 수단으로 인증했음을 인증하고, Livefyre 인증 토큰이 최종 사용자에 대해 조달되었습니다. Livefyre 토큰을 사용하여 쿠키를 설정하거나 사용자를 위한 토큰을 가지고 있고 사용자를 명시적으로 로그인하려는 경우 이 옵션을 사용합니다. 예를 들면 다음과 같습니다. <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 인증 세부 사항 (예: 사용자 정의 인증 흐름) 를 정의한 개체에 위임합니다. Livefyre 앱의 대화형 기능을 활성화하려면 호스트 페이지에 의해 호출되어야 합니다. |

