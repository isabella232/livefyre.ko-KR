---
description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 가져오기 요청 구조를 만듭니다.
seo-description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 가져오기 요청 구조를 만듭니다.
seo-title: 요청 구조 가져오기
solution: Experience Manager
title: 요청 구조 가져오기
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# 요청 구조 가져오기{#pull-request-structure}

사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 가져오기 요청 구조를 만듭니다.

Livefyre가 끝점 URL에 대한 가져오기 요청을 발행합니다.

예를 들어, 가져오기 끝점 URL이 다음과 같은 경우

```
https://example.yoursite.com/some_path/?id={id}
```

이 끝점에 대한 Livefyre 가져오기 요청은 다음과 같습니다.

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

여기서 `lftoken` 은 네트워크 키로 서명된 JSON 웹 토큰이며 **[!UICONTROL {userAuthToken}]** Livefyre에서 생성된 사용자 인증 토큰입니다.

1. 가져오기 URL에 `lftoken` 대한 Ping 요청이 악성 에이전트가 아니라 Livefyre에 의해 전송되었는지 확인하는 데 사용합니다.
1. 들어오는 모든 요청에 대해:

   * 쿼리 문자열이 요청에 있는지 확인합니다. `lftoken`
   * Livefyre 라이브러리의 `validateLivefyreToken` 방법을 사용하여 네트워크 키로 `lftoken` 서명했는지 확인합니다.

   * 존재하지 않거나 유효성 검사에 실패한 `lftoken` 경우 종단점이 프로필 정보로 응답하도록 허용하지 마십시오. 대신 403(금지됨) 상태 코드로 응답하고 응답 본문이 없습니다.

1. `userAuthToken` 사용자 ID가 "system"인 사용자에 대한 Livefyre `buildUserAuthToken` 메서드로 생성됩니다. 이 사용자는 모든 새 네트워크에 대해 처음 생성된 사용자입니다.
