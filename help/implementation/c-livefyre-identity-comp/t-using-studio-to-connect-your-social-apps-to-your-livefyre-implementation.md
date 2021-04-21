---
description: 소셜 로그인을 활성화하려면 Studio를 사용하여 소셜 앱의 자격 증명을 Livefyre 통합에 추가하고 로그인 양식을 사용자 정의합니다.
title: Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결
exl-id: 2ccb9737-8c59-4c1d-93d3-61f913b3cdd6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

소셜 로그인을 활성화하려면 Studio를 사용하여 소셜 앱의 자격 증명을 Livefyre 통합에 추가하고 로그인 양식을 사용자 정의합니다.

## 로그인 양식 사용자 지정 {#section_v4c_hv2_3z}

로그인 양식을 사용하면 앱에 로그인할 때 사용자에게 표시되는 정보를 사용자 정의할 수 있습니다. 모달 창을 사용자 정의할 수 있습니다.

* **로고:** 로그인 모델에서 사용할 로고를 업로드합니다.
* **글꼴 모음:** 브랜딩과 일치하는 글꼴을 선택합니다.
* **브랜드 색상:** 모달 내의 특정 텍스트에 사용할 16진수 색상을 입력합니다.
* **약관 URL: 회사 약관 페이지의 URL을** 입력합니다. 이 필드는 Livefyre ID에 사용할 때 필요합니다.

## Livefyre ID 번역 중 {#section_xxt_z52_3z}

Livefyre ID에서 텍스트 문자열에 대한 번역 세트를 만들고 수정할 수 있습니다.

Livefyre ID와 함께 번역 세트를 사용하는 방법에 대한 자세한 내용은 번역 세트를 참조하십시오.

Livefyre ID에 대해 사용자 정의할 수 있는 특정 문자열에 대한 자세한 내용은 Livefyre ID를 참조하십시오.

## {#section_dlv_wzt_bbb} 전자 메일로 로그인 활성화

사용자가 자신의 이메일 주소를 사용하여 사이트에 로그인하여 자신의 앱과 상호 작용할 수 있도록 합니다.

Livefyre 기본 계정을 사용하여 로그인을 활성화하려면:

1. Livefyre 스튜디오의 **[!UICONTROL Integration Settings]**&#x200B;으로 이동합니다.
1. **[!UICONTROL Enable Login with Email]** 토글을 **[!UICONTROL On]**&#x200B;으로 전환합니다.

## facebook 계정 {#section_ph3_515_bbb}을(를) 사용하여 로그인 활성화

facebook 계정을 Livefyre에 연결하면 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있습니다.

facebook 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Facebook]** 토글을 **[!UICONTROL ON]**&#x200B;으로 전환합니다.

1. facebook 앱의 **[!UICONTROL App ID]** 및 **[!UICONTROL App Secret]**&#x200B;을(를) 추가합니다.

   이러한 값은 [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/)에서 사용할 수 있는 앱용 Facebook 개발자 대시보드에 나열됩니다.

## Google {#section_fq3_kb5_bbb}에서 로그인 활성화

Google+ 계정을 Livefyre에 연결하여 사용자가 Google+ 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 합니다.

Google+ 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Google]** 토글을 **[!UICONTROL ON]**&#x200B;으로 전환합니다.

1. Google 앱의 **[!UICONTROL Client ID]** 및 **[!UICONTROL Client secret]**&#x200B;을(를) 추가합니다.

   이러한 값은 [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library)에서 사용할 수 있는 Google Cloud Platform 프로젝트 인터페이스에 표시됩니다. 이 정보를 검색하려면 **[!UICONTROL API Manager > Credentials]**&#x200B;으로 이동하여 프로젝트 이름을 클릭합니다.

## twitter 계정 {#section_iyz_wb5_bbb}을(를) 사용하여 로그인 활성화

twitter 계정을 Livefyre에 연결하여 사용자가 Twitter 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 합니다.

twitter 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Twitter]** 토글을 **[!UICONTROL ON]**&#x200B;으로 전환합니다.

1. twitter 앱의 **[!UICONTROL Consumer Key (API Key)]** 및 **[!UICONTROL Consumer Secret (API Secret)]**&#x200B;을(를) 추가합니다.

   이러한 값은 Twitter 앱의 **[!UICONTROL Keys and Access Tokens]** 페이지에 나열되며 [https://apps.twitter.com/](https://apps.twitter.com/)에서 사용할 수 있습니다.

## Yahoo!를 사용하여 로그인 활성화 계정 {#section_s1q_3c5_bbb}

Yahoo! 사용자가 자신의 Yahoo! 로그인 정보를 참조하십시오.

Yahoo!를 사용하여 로그인을 활성화하려면 account:

1. **[!UICONTROL Enable Login with Yahoo!]** 토글을 **[!UICONTROL ON]**&#x200B;으로 전환합니다.

1. Yahoo! 추가 앱의 **[!UICONTROL Client ID]** 및 **[!UICONTROL Client Secret]**.

   이러한 값은 Yahoo! 앱 세부 정보 페이지. [developer.yahoo.com/apps](https://developer.yahoo.com/apps)에서 이용할 수 있습니다.

## Microsoft Live 계정 {#section_z42_4c5_bbb}을(를) 사용하여 로그인 활성화

Microsoft Live ID 계정을 Livefyre에 연결하여 사용자가 Microsoft Live ID 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있도록 합니다.

Microsoft Live ID 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**&#x200B;에서 **[!UICONTROL Enable Microsoft Live Login]** 전환을 **[!UICONTROL On]**&#x200B;로 전환합니다.

1. **[!UICONTROL Microsoft Live Client ID (Private Key)]** 및 **[!UICONTROL Microsoft Live Client Secret (Password)]**&#x200B;을 입력합니다.

1. 클릭 **[!UICONTROL Save Settings]**.

   **[!UICONTROL Microsoft Live Client ID (Private Key)]** 및 **[!UICONTROL Microsoft Live Client Secret (Password)]** 값은 Microsoft Live ID 앱 세부 정보 페이지에 나열됩니다.

## 소셜 앱을 Livefyre ID {#section_on2_vc5_bbb}에 연결

사용자가 사이트의 앱에 대해 Livefyre ID 구현을 사용할 수 있도록 합니다.

1. 앱 만들기.
1. **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** **[!UICONTROL Livefyre Identity]**&#x200B;로 이동합니다.

1. 만든 앱에 대한 필수 앱 자격 증명을 입력합니다.
