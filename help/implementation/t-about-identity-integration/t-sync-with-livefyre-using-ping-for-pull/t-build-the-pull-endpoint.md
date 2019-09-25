---
description: 풀 끝점을 만들어 사용자 ID 시스템에 대한 액세스 요청을 받고 이에 응답합니다.
seo-description: 풀 끝점을 만들어 사용자 ID 시스템에 대한 액세스 요청을 받고 이에 응답합니다.
seo-title: 풀 끝점 만들기
solution: Experience Manager
title: 풀 끝점 만들기
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 풀 끝점 만들기{#build-the-pull-endpoint}

풀 끝점을 만들어 사용자 ID 시스템에 대한 액세스 요청을 받고 이에 응답합니다.

1. Livefyre 요청을 받고 최신 사용자 데이터가 포함된 JSON 개체를 사용하여 응답하는 HTTPS 끝점을 만듭니다.

   >[!NOTE]
   >
   >이 끝점에 액세스해야 합니다. 또한 HTTPS 프로토콜을 통해 요청과 응답을 모두 보내는 것이 좋습니다.

1. Studio에 끝점을 등록합니다.
