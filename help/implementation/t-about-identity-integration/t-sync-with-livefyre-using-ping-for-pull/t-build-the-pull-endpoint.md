---
description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답하는 풀 끝점을 빌드합니다.
seo-description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답하는 풀 끝점을 빌드합니다.
seo-title: 가져오기 끝점 구축
solution: Experience Manager
title: 가져오기 끝점 구축
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 가져오기 끝점 구축{#build-the-pull-endpoint}

사용자 ID 시스템에 대한 액세스 요청을 받고 응답하는 풀 끝점을 빌드합니다.

1. Livefyre 요청을 받고 최신 사용자 데이터를 포함하는 JSON 개체로 응답하는 HTTPS 끝점을 만듭니다.

   >[!NOTE]
   >
   >이 끝점에 액세스할 수 있어야 합니다. 또한 요청과 응답은 HTTPS 프로토콜을 통해 보내는 것이 좋습니다.

1. Studio를 사용하여 종단점을 등록합니다.
