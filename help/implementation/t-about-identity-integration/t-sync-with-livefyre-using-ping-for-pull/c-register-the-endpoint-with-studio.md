---
description: URL 끝점을 등록하면 Livefyre가 URL을 사용하여 업데이트된 프로필 정보를 가져올 수 있습니다.
seo-description: URL 끝점을 등록하면 Livefyre가 URL을 사용하여 업데이트된 프로필 정보를 가져올 수 있습니다.
seo-title: Studio에 끝점 등록
solution: Experience Manager
title: Studio에 끝점 등록
uuid: 4eb816ee-d743-43bf-bcee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Studio에 끝점 등록{#register-the-endpoint-with-studio}

URL 끝점을 등록하면 Livefyre가 URL을 사용하여 업데이트된 프로필 정보를 가져올 수 있습니다.

풀링 URL에 대한 Ping을 네트워크당 한 번만 등록합니다. 한 번 설정하면 사용자 관리 시스템에서 사용자 프로필 데이터를 가져오기 위한 끝점이 변경되지 않는 한 이 값이 변경되지 않습니다.

1. Studio를 사용하여 이 URL 끝점을 Livefyre에 등록합니다.
1. Livefyre가 업데이트된 사용자 프로필 정보를 가져올 URL을 등록하고, **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**&#x200B;이동하여 **[!UICONTROL Ping for Pull URL]** 필드에 입력합니다.

   예를 들어, URL은 다음과 같을 수 있습니다. `https://example.yoursite.com/some_path/?id={id}`

