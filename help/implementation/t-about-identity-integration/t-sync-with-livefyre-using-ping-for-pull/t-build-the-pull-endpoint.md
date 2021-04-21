---
description: 사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 수 있도록 끌어오기 끝점을 만듭니다.
title: 풀 끝점 만들기
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# 풀 끝점 만들기{#build-the-pull-endpoint}

사용자 ID 시스템에 대한 액세스 요청을 받고 응답할 수 있도록 끌어오기 끝점을 만듭니다.

1. Livefyre 요청을 받고 최신 사용자 데이터가 포함된 JSON 개체를 사용하여 응답하는 HTTPS 끝점을 만듭니다.

   >[!NOTE]
   >
   >이 끝점에 액세스할 수 있어야 합니다. 또한 요청과 응답을 모두 HTTPS 프로토콜을 통해 보내는 것이 좋습니다.

1. Studio에 끝점을 등록합니다.
