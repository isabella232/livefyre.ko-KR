---
description: 사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 트리거하도록 Ping을 만듭니다.
seo-description: 사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 트리거하도록 Ping을 만듭니다.
seo-title: Ping 구축
solution: Experience Manager
title: Ping 구축
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516

---


# Ping 구축{#build-the-ping}

사용자가 프로필을 업데이트할 때 페이지가 Livefyre를 트리거하도록 Ping을 만듭니다.

Livefyre가 와 함께 업데이트 알림 `networkName` 을 받으면 시스템이 가져오기 `user_id`를 위해 Ping에 가져오기 요청을 보냅니다.

>[!NOTE]
>
>Ping에 대한 응답으로 403/Not Authorized가 표시되면 Ping 요청에 잘못된 `lftoken` 추가가 있음을 나타냅니다. 네트워크 소유자 권한 `lftoken` 이 있는 사용자 `user_id` 또는 시스템 사용자인지 확인하십시오. Livefyre 라이브러리를 사용하는 경우 이 방법을 사용하여 요청에 대해 유효한 시스템 토큰을 생성합니다 `buildLivefyreToken` .

1. 사용자가 프로필을 업데이트할 때 Livefyre를 트리거하는 코드를 페이지에 추가합니다. 다음과 같이 URL을 구성합니다.

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Livefyre에서 네트워크 이름을 제공했습니다.
   * **[!UICONTROL user_id:]** 사용자 ID.
   * **[!UICONTROL token:]** 유효한 시스템 토큰.

1. 요청 구조를 가져옵니다.
