---
description: twitter과 함께 Livefyre ID를 사용하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.
title: Livefyre ID와 함께 사용할 Twitter 앱 만들기
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Livefyre ID와 함께 사용할 Twitter 앱 만들기{#create-a-twitter-app-for-use-with-livefyre-identity}

twitter과 함께 Livefyre ID를 사용하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.

twitter 로그인을 사용하려면 Livefyre에 다음 Twitter 앱 정보가 필요합니다.

* 소비자 키(API 키)
* 소비자 비밀(API 비밀)

Livefyre ID에 사용할 Twitter 앱을 만들려면:

1. [https://apps.twitter.com/](https://apps.twitter.com/)로 이동하고 Twitter 계정에 로그인하여 새 앱을 만들거나 Livefyre ID에 사용할 기존 앱을 선택합니다.
1. 앱에 대한 설정 페이지에서:

   * **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre`(여기서 **{networkName}**&#x200B;은(는) Livefyre에서 제공한 네트워크 이름입니다. 예:** **[!UICONTROL `labs.fyre.co`]****.)[!UICONTROL labs]
   * **[!UICONTROL Enable Callback Locking]** 선택을 취소합니다.
   * 선택 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. **[!UICONTROL Permissions]** 탭에서 **[!UICONTROL Access: Read only]**&#x200B;을 선택합니다.

완료되면 Twitter의 응용 프로그램 관리 > 키 및 액세스 토큰 페이지에는 Studio의 통합 설정 페이지에 사용할 앱의 소비자 키(API 키) 및 소비자 암호(API 암호)가 나열됩니다.
