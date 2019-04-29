---
description: Facebook에서 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트의 앱과 상호 작용할 수
  있게 할 수 있습니다.
seo-description: Facebook에서 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트의 앱과 상호 작용할
  수 있게 할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Facebook 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Facebook 앱 만들기
uuid: A 7 F 7 BE 4 E -8986-4 E 79-831 A -0 BB 0 AE 555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID와 함께 사용할 Facebook 앱 만들기{#create-a-facebook-app-for-use-with-livefyre-identity}

Facebook에서 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트의 앱과 상호 작용할 수 있게 할 수 있습니다.

사용자가 Facebook 자격 증명으로 로그인할 수 있도록 하기 위해 Livefyre 에는 다음과 같은 Facebook 앱 정보가 필요합니다.

* 앱 ID
* 앱 비밀

Livefyre ID와 함께 사용할 Facebook 앱을 만들려면:

1. [https://developers.facebook.com/apps](https://developers.facebook.com/apps)로 이동합니다.
1. Facebook 개발자 계정으로 로그인합니다.
1. Livefyre ID에 사용할 기존 앱을 클릭하거나 **[!UICONTROL Add New App]** 선택합니다.
1. **[!UICONTROL Settings]** **[!UICONTROL Basic]** 을 클릭합니다. **[!UICONTROL Contact Email]** 주소 **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** 및을 입력합니다 **[!UICONTROL Terms of Service URL]**.
1. 옆에 있는 더하기 기호 ( **[!UICONTROL +]** ) 를 **[!UICONTROL Products]** 클릭합니다.
1. **[!UICONTROL Set Up]** **[!UICONTROL Facebook Login]** 아래를 클릭합니다.
1. 다음을 클릭하여 **[!UICONTROL Settings]** 설정합니다.

   * 으로 설정합니다 **[!UICONTROL Client OAuth Login]** **[!UICONTROL Yes]**.
   * 으로 설정합니다 **[!UICONTROL Web OAuth Login]** **[!UICONTROL Yes]**.
   * 으로 설정합니다 **[!UICONTROL Use Strict Mode for Redirect URIs]** **[!UICONTROL Yes]**.
   * 으로 설정합니다 **[!UICONTROL Enforce HTTPS for Web OAuth Login]** **[!UICONTROL Yes]**.
   * 아래에서 **[!UICONTROL Valid OAuth redirect URLs]** URL를 추가합니다 `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (여기서 `{networkName}` livefyre가 제공하는 네트워크 이름).

1. **[!UICONTROL App Review]** Under:

   * 앱을 공개하십시오.
   * **[!UICONTROL Approved Items]** for **[!UICONTROL Login Permissions]** include `email`, `public_profile`and `user_friends`.

완료되면, Facebook 개발자 대시보드 페이지에 사용자의 앱 ID와 앱 암호를 나열하여 스튜디오의 통합 설정에 사용할 수 있습니다.
