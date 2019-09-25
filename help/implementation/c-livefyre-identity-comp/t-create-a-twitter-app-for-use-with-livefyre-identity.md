---
description: Twitter와 Livefyre Id를 함께 사용하면 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.
seo-description: Twitter와 Livefyre Id를 함께 사용하면 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Twitter 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Twitter 앱 만들기
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID와 함께 사용할 Twitter 앱 만들기{#create-a-twitter-app-for-use-with-livefyre-identity}

Twitter와 Livefyre Id를 함께 사용하면 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.

Twitter 로그인을 활성화하려면 다음 Twitter 앱 정보가 필요합니다.

* 소비자 키(API 키)
* 소비자 비밀(API 비밀)

Livefyre ID와 함께 사용할 Twitter 앱을 만들려면:

1. https://apps.twitter.com/ [으로](https://apps.twitter.com/)이동하여 Twitter 계정에 로그인하여 새 앱을 만들거나 Livefyre Id와 함께 사용할 기존 앱을 선택합니다.
1. 앱에 대한 설정 페이지에서:

   * Livefyre **[!UICONTROL Callback URL:]** 를 `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` 입력합니다. 여기서 **{networkName}** 은(는) Livefyre가 제공한 네트워크 이름입니다. For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * 선택 **[!UICONTROL Enable Callback Locking]**&#x200B;취소합니다.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 탭에서 **[!UICONTROL Permissions]** 을 선택합니다 **[!UICONTROL Access: Read only]**.

완료되면 Twitter의 애플리케이션 관리 &gt; 키 및 액세스 토큰 페이지에는 앱의 소비자 키(API 키) 및 소비자 암호(API 암호)가 표시되어 Studio의 통합 설정 페이지에 사용됩니다.
