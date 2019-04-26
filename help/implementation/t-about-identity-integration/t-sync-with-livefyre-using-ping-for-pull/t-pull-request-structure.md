---
description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 수 있도록 풀 요청 구조를 만듭니다.
seo-description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 수 있도록 풀 요청 구조를 만듭니다.
seo-title: 요청 구조 가져오기
solution: Experience Manager
title: 요청 구조 가져오기
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 요청 구조 가져오기{#pull-request-structure}

사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 수 있도록 풀 요청 구조를 만듭니다.

Livefyre가 끝점 URL에 대한 풀 요청을 발행합니다.

예를 들어 풀 끝점 URL 이 다음과 같은 경우:

```
https://example.yoursite.com/some_path/?id={id}
```

이 끝점에 대한 Livefyre 풀 요청은 다음과 같습니다.

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

은 `lftoken` 네트워크 키로 서명된 JSON 웹 토큰이며 Livefyre **[!UICONTROL {userAuthToken}]** 에서 생성된 사용자 인증 토큰입니다.

1. 풀 URL에 대한 ping에 대한 요청이 악성 에이전트가 아닌 Livefyre에 의해 전송되었는지 확인하는 `lftoken` 데 사용합니다.
1. 모든 수신 요청에 대해:

   * 쿼리 문자열이 `lftoken` 요청에 있는지 확인합니다.
   * Livefyre 라이브러리의 `validateLivefyreToken` 메서드를 사용하여 네트워크 키가 `lftoken` 서명되었는지 확인합니다.

   * 가 `lftoken` 없거나 유효성 검사가 실패한 경우 종단점을 사용하여 프로필 정보에 응답하지 마십시오. 대신, 403 (금지) 상태 코드로 응답하고 응답 본문을 사용하지 않습니다.

1. `userAuthToken` 사용자 ID «system» 와 함께 사용자에 대한 Livefyre `buildUserAuthToken` 메서드로 생성됩니다. 이 사용자는 모든 새 네트워크에 대해 처음 만든 사용자입니다.
1. 페이지를 테스트하려면 [풀](https://livefyre-p4p-wizard.herokuapp.com/home) 테스터용 Ping를 사용하여 모든 것이 예상대로 작동하는지 확인합니다.
