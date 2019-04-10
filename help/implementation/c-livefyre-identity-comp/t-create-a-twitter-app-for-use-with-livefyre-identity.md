---
description: Twitter에서 Livefyre ID를 사용하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수
  있습니다.
seo-description: Twitter에서 Livefyre ID를 사용하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할
  수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Twitter 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Twitter 앱 만들기
uuid: 841 CCE 7 C -618 D -4154-85 A 3-1 DE 96 D 04 BB 69
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre ID와 함께 사용할 Twitter 앱 만들기{#create-a-twitter-app-for-use-with-livefyre-identity}

Twitter에서 Livefyre ID를 사용하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.

Twitter 로그인을 활성화하려면 Livefyre에서 다음과 같은 Twitter 앱 정보가 필요합니다.

* Consumer 키 (API 키)
* Consumer secret (API secret)

Livefyre ID와 함께 사용할 Twitter 앱을 만들려면:

1. [https://apps.twitter.com/](https://apps.twitter.com/)로 이동한 다음 Twitter 계정에 로그인하여 새 앱을 만들거나 Livefyre ID와 함께 사용할 기존 앱을 선택합니다.
1. 앱에 대한 설정 페이지에서:

   * Enter ( **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` where **{networkname}** is your Livefyre provided network name. 예를 들면 다음과 같습니다. ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * 선택 취소합니다 **[!UICONTROL Enable Callback Locking]**.
   * **[!UICONTROL Allow this application to be used to Sign in with Twitter]**Select.

1. **[!UICONTROL Permissions]** 탭에서 **[!UICONTROL Access: Read only]**를 선택합니다.

완료되면, Twitter의 응용 프로그램 관리 > 키 및 액세스 토큰 페이지는 앱의 소비자 키 (API 키) 와 소비자 암호 (API 암호) 를 스튜디오의 통합 설정 페이지에 사용할 수 있게 나열합니다.
