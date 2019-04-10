---
description: 소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모티브를 사용자
  정의합니다.
seo-description: 소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모티브를
  사용자 정의합니다.
seo-title: Studio를 사용하여 소셜 앱을 Livefyre 구현과 연결
title: Studio를 사용하여 소셜 앱을 Livefyre 구현과 연결
uuid: BE 14869 c-e 0 df -48 cd-a 1 f 3-99 eb 953 dd 9 ce
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Studio를 사용하여 소셜 앱을 Livefyre 구현과 연결{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모티브를 사용자 정의합니다.

## 로그인 모달 사용자 지정 {#section_v4c_hv2_3z}

로그인 모달 기능을 사용하면 앱에 로그인할 때 표시되는 정보를 사용자 정의할 수 있습니다. 모달 창을 사용자 지정할 수 있습니다.

* **로고:** 로그인 양식에 사용할 로고를 업로드합니다.
* **글꼴 모음:** 브랜드와 일치하는 글꼴을 선택합니다.
* **브랜드 색상:** 모달 내의 특정 텍스트에 사용할 16 진수 색상을 입력합니다.
* **약관 URL:** 회사의 약관 페이지에 대한 URL를 입력합니다. 이 필드는 Livefyre ID와 함께 사용해야 합니다.

## Livefyre ID 번역 {#section_xxt_z52_3z}

Livefyre ID의 텍스트 문자열에 대한 번역 세트를 만들고 수정할 수 있습니다.

Livefyre ID에서 번역 세트 사용에 대한 자세한 내용은 번역 세트를 참조하십시오.

Livefyre ID에 맞게 사용자 정의할 수 있는 특정 문자열에 대한 자세한 내용은 Livefyre ID를 참조하십시오.

## 이메일로 로그인 활성화 {#section_dlv_wzt_bbb}

사용자가 자신의 이메일 주소를 사용하여 사이트에 로그인하여 앱과 상호 작용할 수 있도록 합니다.

Livefyre 기본 계정을 사용하여 로그인을 활성화하려면:

1. Livefyre Studio **[!UICONTROL Integration Settings]** 에서 탐색합니다.
1. **[!UICONTROL Enable Login with Email]** 전환 스위치를 전환합니다 **[!UICONTROL On]**.

## Facebook 계정을 사용하여 로그인 활성화 {#section_ph3_515_bbb}

Facebook 계정을 Livefyre에 연결하면 사용자가 Facebook 로그인을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.

Facebook 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Facebook]** 전환 스위치를 전환합니다 **[!UICONTROL ON]**.

1. Facebook 앱의 **[!UICONTROL App ID]** 및 **[!UICONTROL App Secret]**을 추가합니다.

   이러한 값은 https://developers.facebook.com/apps/에서 [제공하는 앱의 Facebook 개발자 대시보드에 나열되어](https://developers.facebook.com/apps/675503539257343/dashboard/)있습니다.

## Google에서 로그인 활성화 {#section_fq3_kb5_bbb}

Google + 계정을 Livefyre에 연결하면 사용자가 Google + 로그인을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.

Google + 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Google]** 전환 스위치를 전환합니다 **[!UICONTROL ON]**.

1. Google 앱의 **[!UICONTROL Client ID]** 및 **[!UICONTROL Client secret]**을 추가합니다.

   이러한 값은 https://console.cloud.google.com/에서 [제공하는 Google Cloud Platform 프로젝트 인터페이스에 나열되어](https://console.cloud.google.com/apis/library)있습니다. 이 정보를 검색하려면 이동한 다음 **[!UICONTROL API Manager > Credentials]**프로젝트 이름을 클릭합니다.

## Twitter 계정을 사용하여 로그인 활성화 {#section_iyz_wb5_bbb}

Twitter 계정을 Livefyre에 연결하면 사용자가 Twitter 로그인을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.

Twitter 계정을 사용하여 로그인을 활성화하려면:

1. **[!UICONTROL Enable Login with Twitter]** 전환 스위치를 전환합니다 **[!UICONTROL ON]**.

1. Twitter 앱을 **[!UICONTROL Consumer Key (API Key)]** 추가합니다 **[!UICONTROL Consumer Secret (API Secret)]**.

   이러한 값은 https://apps.twitter.com/에서 제공하는 Twitter 앱의 **[!UICONTROL Keys and Access Tokens]**[페이지에 나열되어](https://apps.twitter.com/)있습니다.

## Yahoo! account {#section_s1q_3c5_bbb}

Yahoo! 사용자가 Yahoo! 로그인을 참조하십시오.

Yahoo! 계정:

1. **[!UICONTROL Enable Login with Yahoo!]** 전환 스위치를 전환합니다 **[!UICONTROL ON]**.

1. Yahoo! 앱 **[!UICONTROL Client ID]** 및 **[!UICONTROL Client Secret]**.

   이러한 값은 Yahoo! 앱 상세 정보 페이지를 [](https://developer.yahoo.com/apps)참조하십시오.

## Microsoft Live 계정을 사용하여 로그인 활성화 {#section_z42_4c5_bbb}

Microsoft Live ID 계정을 Livefyre에 연결하면 사용자가 Microsoft Live ID 로그인을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.

Microsoft Live ID 계정을 사용하여 로그인을 활성화하려면:

1. 에서 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]****[!UICONTROL Enable Microsoft Live Login]** 전환 스위치를 **[!UICONTROL On]**전환합니다.

1. **[!UICONTROL Microsoft Live Client ID (Private Key)]** AND **[!UICONTROL Microsoft Live Client Secret (Password)]**를 입력합니다.

1. **[!UICONTROL Save Settings]**을 클릭합니다.

   **[!UICONTROL Microsoft Live Client ID (Private Key)]** AND **[!UICONTROL Microsoft Live Client Secret (Password)]** 값은 Microsoft Live ID 앱 세부 사항 페이지에 나와 있습니다.

## Livefyre ID에 소셜 앱 연결 {#section_on2_vc5_bbb}

사용자가 사이트에서 앱에 대한 Livefyre ID 구현을 사용하도록 할 수 있습니다.

1. 앱을 제작합니다.
1. **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**>로 이동합니다 **[!UICONTROL Livefyre Identity]**.

1. 제작한 앱에 필요한 앱 자격 증명을 입력합니다.