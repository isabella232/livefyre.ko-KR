---
description: facebook과 함께 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 할 수 있습니다.
title: Livefyre ID와 함께 사용할 Facebook 앱 만들기
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Livefyre ID와 함께 사용할 Facebook 앱 만들기{#create-a-facebook-app-for-use-with-livefyre-identity}

facebook과 함께 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 할 수 있습니다.

사용자가 Facebook 자격 증명으로 로그인할 수 있도록 하려면 Livefyre에 다음과 같은 Facebook 앱 정보가 필요합니다.

* 앱 ID
* 앱 암호

Livefyre ID와 함께 사용할 Facebook 앱을 만들려면:

1. [https://developers.facebook.com/apps](https://developers.facebook.com/apps)로 이동합니다.
1. facebook 개발자 계정에 로그인합니다.
1. **[!UICONTROL Add New App]**&#x200B;을 클릭하거나 Livefyre ID에 사용할 기존 앱을 선택합니다.
1. **[!UICONTROL Settings]**&#x200B;을 클릭한 다음 **[!UICONTROL Basic]**&#x200B;을 클릭합니다. **[!UICONTROL Contact Email]** 주소, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** 및 **[!UICONTROL Terms of Service URL]**&#x200B;을 입력합니다.
1. **[!UICONTROL Products]** 옆의 더하기 기호( **[!UICONTROL +]**)를 클릭합니다.
1. **[!UICONTROL Facebook Login]** 아래의 **[!UICONTROL Set Up]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Settings]**&#x200B;을 클릭하고 다음을 설정합니다.

   * **[!UICONTROL Client OAuth Login]**&#x200B;을(를) **[!UICONTROL Yes]**(으)로 설정합니다.
   * **[!UICONTROL Web OAuth Login]**&#x200B;을(를) **[!UICONTROL Yes]**(으)로 설정합니다.
   * **[!UICONTROL Use Strict Mode for Redirect URIs]**&#x200B;을(를) **[!UICONTROL Yes]**(으)로 설정합니다.
   * **[!UICONTROL Enforce HTTPS for Web OAuth Login]**&#x200B;을(를) **[!UICONTROL Yes]**(으)로 설정합니다.
   * **[!UICONTROL Valid OAuth redirect URLs]** 아래에서 URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre`(여기서 `{networkName}`은(는) Livefyre가 제공한 네트워크 이름)을 추가합니다.

1. **[!UICONTROL App Review]** 아래:

   * 앱을 공개합니다.
   * **[!UICONTROL Login Permissions]**&#x200B;의 **[!UICONTROL Approved Items]**&#x200B;에 `email`, `public_profile` 및 `user_friends`가 포함되어 있는지 확인합니다.

완료되면 Facebook 개발자의 대시보드 페이지에 Studio의 통합 설정에 사용할 앱 ID와 앱 암호가 나열됩니다.
