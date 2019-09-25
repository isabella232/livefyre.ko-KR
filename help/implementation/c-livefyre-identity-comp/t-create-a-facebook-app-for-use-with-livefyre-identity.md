---
description: Facebook과 함께 Livefyre Id를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 할 수 있습니다.
seo-description: Facebook과 함께 Livefyre Id를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Facebook 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Facebook 앱 만들기
uuid: a7f7be4e-8986-4e79-831a-0bb0ae55599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID와 함께 사용할 Facebook 앱 만들기{#create-a-facebook-app-for-use-with-livefyre-identity}

Facebook과 함께 Livefyre Id를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 할 수 있습니다.

사용자가 Facebook 자격 증명으로 로그인하도록 허용하려면 Livefyre에 다음 Facebook 앱 정보가 필요합니다.

* 앱 ID
* 앱 암호

Livefyre ID와 함께 사용할 Facebook 앱을 만들려면:

1. https://developers.facebook.com/apps으로 [이동합니다](https://developers.facebook.com/apps).
1. Facebook 개발자 계정에 로그인합니다.
1. Livefyre ID에 사용할 기존 앱을 **[!UICONTROL Add New App]** 클릭하거나 선택합니다.
1. 을 **[!UICONTROL Settings]**&#x200B;클릭한 다음 **[!UICONTROL Basic]**&#x200B;을 클릭합니다. 주소, **[!UICONTROL Contact Email]****[!UICONTROL Display Name]**&#x200B;및 **[!UICONTROL Privacy Policy URL]****[!UICONTROL Terms of Service URL]**&#x200B;주소를 입력합니다.
1. 옆에 있는 더하기 기호( **[!UICONTROL +]**)를 **[!UICONTROL Products]**&#x200B;클릭합니다.
1. 아래에서 을 **[!UICONTROL Set Up]** 클릭합니다 **[!UICONTROL Facebook Login]**.
1. 다음을 **[!UICONTROL Settings]** 클릭하고 설정합니다.

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * 에서 URL **[!UICONTROL Valid OAuth redirect URLs]**&#x200B;을 `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` 추가합니다(여기서 `{networkName}` 사용자의 Livefyre 제공 네트워크 이름).

1. Under **[!UICONTROL App Review]**:

   * 앱을 공개하세요.
   * 에 **[!UICONTROL Approved Items]** 에 **[!UICONTROL Login Permissions]** 및 `email`가 포함되었는지 확인합니다 `public_profile``user_friends`.

완료되면 Facebook 개발자의 대시보드 페이지에 Studio의 통합 설정에서 사용할 앱 ID와 앱 암호가 나열됩니다.
