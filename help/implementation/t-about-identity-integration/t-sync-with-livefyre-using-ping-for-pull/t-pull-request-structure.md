---
description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답하도록 가져오기 요청 구조를 만듭니다.
title: 요청 구조 가져오기
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# 요청 구조 가져오기{#pull-request-structure}

사용자 ID 시스템에 대한 액세스 요청을 받고 응답하도록 가져오기 요청 구조를 만듭니다.

Livefyre는 끝점 URL에 대한 가져오기 요청을 발행합니다.

예를 들어 풀 끝점 URL이 다음과 같은 경우:

```
https://example.yoursite.com/some_path/?id={id}
```

이 끝점에 대한 Livefyre 가져오기 요청은 다음과 같습니다.

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

여기서 `lftoken`은 사용자의 네트워크 키로 서명된 JSON 웹 토큰이고 **[!UICONTROL {userAuthToken}]**&#x200B;은 Livefyre에서 생성된 사용자 인증 토큰입니다.

1. 가져오기 URL에 대한 Ping 요청이 악성 에이전트가 아니라 Livefyre가 보낸 것임을 확인하려면 `lftoken`을 사용합니다.
1. 들어오는 모든 요청에 대해:

   * 요청에 `lftoken` 쿼리 문자열이 있는지 확인합니다.
   * Livefyre 라이브러리의 `validateLivefyreToken` 메서드를 사용하여 `lftoken`이(가) 네트워크 키로 서명되었는지 확인합니다.

   * `lftoken`이(가) 없거나 유효성 검사에 실패한 경우 종단점이 프로필 정보로 응답하도록 허용하지 마십시오. 대신 403(금지됨) 상태 코드로 응답하고 응답 본문이 없습니다.

1. `userAuthToken` 사용자 id &quot;system&quot;을 사용하여 사용자에  `buildUserAuthToken` 대한 Livefyre 메서드로 생성됩니다. 이 사용자는 모든 새 네트워크에 대해 처음으로 만들어진 사용자입니다.
