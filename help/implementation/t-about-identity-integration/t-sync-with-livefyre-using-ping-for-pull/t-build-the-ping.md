---
description: 사용자가 프로필을 업데이트할 때 Livefyre 페이지가 표시되도록 Ping을 만듭니다.
seo-description: 사용자가 프로필을 업데이트할 때 Livefyre 페이지가 표시되도록 Ping을 만듭니다.
seo-title: Ping 구축
solution: Experience Manager
title: Ping 구축
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Ping{#build-the-ping} 빌드

사용자가 프로필을 업데이트할 때 Livefyre 페이지가 표시되도록 Ping을 만듭니다.

Livefyre가 `networkName` 및 `user_id`의 업데이트 알림을 받으면 시스템이 가져오기 URL을 위해 Ping에 가져오기 요청을 보냅니다.

>[!NOTE]
>
>Ping 요청에 대한 응답으로 403/인증되지 않음 은 Ping 요청에 잘못된 `lftoken`이 추가되었음을 나타냅니다. `lftoken`이(가) 네트워크 소유자 권한이 있는 `user_id`에 해당하는지 또는 시스템 사용자를 위한 것인지 확인하십시오. Livefyre 라이브러리를 사용하는 경우 `buildLivefyreToken` 메서드를 사용하여 요청에 대한 유효한 시스템 토큰을 생성합니다.

1. 사용자가 프로필을 업데이트할 때 Livefyre를 트리거하는 코드를 페이지에 추가합니다. 다음과 같이 URL을 구성합니다.

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Livefyre에서 네트워크 이름을 제공했습니다.
   * **[!UICONTROL user_id:]** 사용자 ID.
   * **[!UICONTROL token:]** 유효한 시스템 토큰입니다.

1. 요청 구조를 가져옵니다.
