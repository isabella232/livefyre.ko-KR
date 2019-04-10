---
description: 사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 ping 하도록 ping를 만듭니다.
seo-description: 사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 ping 하도록 ping를 만듭니다.
seo-title: Ping 빌드
solution: Experience Manager
title: Ping 빌드
uuid: CB 8 CC 043-9 EA 5-407 C-B 70 F -3 F 1 E 37 Accdae
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ping 빌드{#build-the-ping}

사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 ping 하도록 ping를 만듭니다.

Livefyre가 `networkName` AND `user_id`로 업데이트 알림을 받으면 시스템에서는 풀 URL에 대한 ping 요청을 ping에 보냅니다.

>[!NOTE]
>
>403/ping에 대한 응답으로 승인되지 않은 경우 ping 요청에 유효하지 않은 `lftoken` 첨부물이 추가되었음을 나타냅니다. IS `lftoken` for a is for a `user_id` network owner privileges or the system user. Livefyre 라이브러리를 사용하는 경우 `buildLivefyreToken` 이 방법을 사용하여 요청에 유효한 시스템 토큰을 생성합니다.

1. 사용자가 프로필을 업데이트할 때 Livefyre를 ping 하는 코드를 페이지에 추가합니다. 다음과 같이 URL를 작성합니다.

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Livefyre가 네트워크 이름을 제공했습니다.
* **[!UICONTROL user_id:]** 사용자의 ID.
* **[!UICONTROL token:]** 유효한 시스템 토큰.

1. 요청 구조를 풀링합니다.
