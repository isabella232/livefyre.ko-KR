---
description: Livefyre가 URL을 사용하여 업데이트된 프로필 정보를 가져올 수 있도록 URL 끝점을 등록합니다.
title: Studio에 끝점 등록
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Studio{#register-the-endpoint-with-studio}에 끝점 등록

Livefyre가 URL을 사용하여 업데이트된 프로필 정보를 가져올 수 있도록 URL 끝점을 등록합니다.

Ping for Pull URL은 네트워크당 한 번만 등록합니다. 한 번 설정되면 사용자 관리 시스템에서 사용자 프로필 데이터를 가져오기 위한 끝점이 변경되지 않는 한 이 값은 변경되지 않아야 합니다.

1. Studio를 사용하여 Livefyre에 이 URL 끝점을 등록합니다.
1. Livefyre가 업데이트된 사용자 프로필 정보를 가져올 URL을 등록하고 **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**&#x200B;으로 이동한 다음 **[!UICONTROL Ping for Pull URL]** 필드에 입력합니다.

   예를 들어 URL은 다음과 같을 수 있습니다.`https://example.yoursite.com/some_path/?id={id}`
