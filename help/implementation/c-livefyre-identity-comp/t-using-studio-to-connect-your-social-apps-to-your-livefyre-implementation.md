---
description: 소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모달을 사용자 정의합니다.
seo-description: 소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모달을 사용자 정의합니다.
seo-title: Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결
title: Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

소셜 로그인을 활성화하려면 Studio를 사용하여 Livefyre 통합에 소셜 앱의 자격 증명을 추가하고 로그인 모달을 사용자 정의합니다.

## 로그인 양식 사용자 지정 {#section_v4c_hv2_3z}

로그인 모달을 사용하면 앱에 로그인할 때 사용자에게 표시되는 정보를 사용자 정의할 수 있습니다. 모달 창을 사용자 정의할 수 있습니다.

* **** 로고:로그인 모델에서 사용할 로고를 업로드합니다.
* **** 글꼴 모음:브랜딩과 일치하는 글꼴을 선택합니다.
* **** 브랜드 색상:모달 내의 특정 텍스트에 사용할 16진수 색상을 입력합니다.
* **** 약관 URL:회사 약관 페이지의 URL을 입력합니다. Livefyre ID에 사용하려면 이 필드가 필요합니다.

## Livefyre ID 번역 {#section_xxt_z52_3z}

Livefyre ID에서 텍스트 문자열에 대한 번역 세트를 만들고 수정할 수 있습니다.

Livefyre ID와 번역 세트 사용에 대한 자세한 내용은 번역 세트를 참조하십시오.

Livefyre ID에 대해 사용자 정의할 수 있는 특정 문자열에 대한 자세한 내용은 Livefyre ID를 참조하십시오.

## 이메일로 로그인 활성화 {#section_dlv_wzt_bbb}

사용자가 이메일 주소를 사용하여 사이트에 로그인하여 앱과 상호 작용할 수 있도록 합니다.

Livefyre 기본 계정을 사용하여 로그인을 활성화하려면:

1. Livefyre **[!UICONTROL Integration Settings]** Studio로 이동합니다.
1. 전환을 **[!UICONTROL Enable Login with Email]** 다음으로 전환합니다 **[!UICONTROL On]**.

## Facebook 계정을 사용하여 로그인 활성화 {#section_ph3_515_bbb}

Facebook 계정을 Livefyre에 연결하면 사용자가 Facebook 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있습니다.

Facebook 계정을 사용하여 로그인을 활성화하려면:

1. 전환을 **[!UICONTROL Enable Login with Facebook]** 다음으로 전환합니다 **[!UICONTROL ON]**.

1. Facebook 앱 및 **[!UICONTROL App ID]** 을 **[!UICONTROL App Secret]**&#x200B;추가합니다.

   이러한 값은 https://developers.facebook.com/apps/에서 다운로드할 수 있는 앱용 Facebook 개발자 대시보드에 [나열되어 있습니다](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Google에서 로그인 활성화 {#section_fq3_kb5_bbb}

Google+ 계정을 Livefyre에 연결하면 사용자가 Google+ 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있습니다.

Google+ 계정을 사용하여 로그인을 활성화하려면:

1. 전환을 **[!UICONTROL Enable Login with Google]** 다음으로 전환합니다 **[!UICONTROL ON]**.

1. Google 앱 **[!UICONTROL Client ID]** 및 **[!UICONTROL Client secret]**&#x200B;을 추가합니다.

   이러한 값은 https://console.cloud.google.com/에서 제공하는 Google Cloud Platform 프로젝트 인터페이스에 [나열되어 있습니다](https://console.cloud.google.com/apis/library). 이 정보를 검색하려면 로 **[!UICONTROL API Manager > Credentials]**&#x200B;이동하여 프로젝트 이름을 클릭합니다.

## Twitter 계정을 사용하여 로그인 활성화 {#section_iyz_wb5_bbb}

Twitter 계정을 Livefyre에 연결하면 사용자가 Twitter 로그인을 사용하여 사이트에서 Apps와 상호 작용할 수 있습니다.

To enable login using a Twitter account:

1. 전환을 **[!UICONTROL Enable Login with Twitter]** 다음으로 전환합니다 **[!UICONTROL ON]**.

1. Twitter 앱의 **[!UICONTROL Consumer Key (API Key)]** 및 **[!UICONTROL Consumer Secret (API Secret)]**&#x200B;을 추가합니다.

   이러한 값은 https://apps.twitter.com/에서 사용할 수 있는 Twitter 앱의 **[!UICONTROL Keys and Access Tokens]** 페이지에 [나열되어 있습니다](https://apps.twitter.com/).

## Yahoo!를 사용하여 로그인 활성화 계정 {#section_s1q_3c5_bbb}

Yahoo! 사용자가 Yahoo! 로그인 정보를 참조하십시오.

Yahoo!를 사용하여 로그인을 활성화하려면 account:

1. 전환을 **[!UICONTROL Enable Login with Yahoo!]** 다음으로 전환합니다 **[!UICONTROL ON]**.

1. Yahoo! 추가 앱과 **[!UICONTROL Client ID]** 함께 사용할 수 **[!UICONTROL Client Secret]**&#x200B;있습니다.

   이러한 값은 Yahoo! 앱 세부 정보 페이지. developer.yahoo.com/apps에서 [확인할 수 있습니다](https://developer.yahoo.com/apps).

## Microsoft Live 계정을 사용하여 로그인 활성화 {#section_z42_4c5_bbb}

Microsoft Live ID 계정을 Livefyre에 연결하면 사용자가 Microsoft Live ID 로그인을 사용하여 사이트에서 앱과 상호 작용할 수 있습니다.

Microsoft Live ID 계정을 사용하여 로그인을 활성화하려면:

1. 에서 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**&#x200B;전환 **[!UICONTROL Enable Microsoft Live Login]** 설정을 로 **[!UICONTROL On]**&#x200B;전환합니다.

1. and를 **[!UICONTROL Microsoft Live Client ID (Private Key)]** 입력합니다 **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. 클릭 **[!UICONTROL Save Settings]**.

   및 **[!UICONTROL Microsoft Live Client ID (Private Key)]** **[!UICONTROL Microsoft Live Client Secret (Password)]** 값은 Microsoft Live ID 앱 세부 사항 페이지에 나열됩니다.

## Social 앱을 Livefyre Identity에 연결 {#section_on2_vc5_bbb}

사용자가 사이트의 앱에 대해 Livefyre ID 구현을 사용할 수 있도록 합니다.

1. 앱 만들기.
1. &gt; **[!UICONTROL Studio]** &gt; **[!UICONTROL Settings]** &gt; **[!UICONTROL Integration Settings]**&gt; **[!UICONTROL Livefyre Identity]**&#x200B;로 이동합니다.

1. 제작한 앱에 대한 필수 앱 자격 증명을 입력합니다.