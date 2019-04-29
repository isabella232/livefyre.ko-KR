---
description: Livefyre가 URL를 사용하여 업데이트된 프로필 정보를 가져올 수 있도록 URL 끝점을 등록합니다.
seo-description: Livefyre가 URL를 사용하여 업데이트된 프로필 정보를 가져올 수 있도록 URL 끝점을 등록합니다.
seo-title: Studio에 끝점 등록
solution: Experience Manager
title: Studio에 끝점 등록
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Studio에 끝점 등록{#register-the-endpoint-with-studio}

Livefyre가 URL를 사용하여 업데이트된 프로필 정보를 가져올 수 있도록 URL 끝점을 등록합니다.

네트워크당 한 번만 풀 URL에 대해 ping를 등록합니다. 이 값이 설정되면 사용자 관리 시스템의 사용자 프로필 데이터를 가져오기 위한 끝점이 변경되지 않는 한 이 값을 변경하면 안 됩니다.

1. Studio를 사용하여 Livefyre에 이 URL 끝점을 등록합니다.
1. Livefyre가 업데이트된 사용자 프로필 정보를 가져올 URL를 등록하고 이동 후 **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** **[!UICONTROL Ping for Pull URL]** 필드에 입력합니다.

   예를 들어 URL는 다음과 같이 표시될 수 있습니다. `https://example.yoursite.com/some_path/?id={id}`

