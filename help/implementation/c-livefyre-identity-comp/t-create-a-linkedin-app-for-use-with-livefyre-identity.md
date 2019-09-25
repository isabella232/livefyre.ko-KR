---
description: LinkedIn과 함께 Livefyre Id를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.
seo-description: LinkedIn과 함께 Livefyre Id를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.
seo-title: Livefyre Id와 함께 사용할 LinkedIn 앱 만들기
solution: Experience Manager
title: Livefyre Id와 함께 사용할 LinkedIn 앱 만들기
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre Id와 함께 사용할 LinkedIn 앱 만들기{#create-a-linkedin-app-for-use-with-livefyre-identity}

LinkedIn과 함께 Livefyre Id를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.

LinkedIn 로그인을 활성화하려면 Livefyre에 다음과 같은 LinkedIn 앱 정보가 필요합니다.

* 소비자 키(API 키)
* 소비자 비밀(API 비밀)

Livefyre Id와 함께 사용할 LinkedIn 앱을 만들려면:

1. https://www.linkedin.com/secure/developer으로 이동하여 LinkedIn 계정에 로그인하여 새 앱을 만들거나 Livefyre Identity와 함께 사용할 기존 앱을 선택합니다.
1. 클릭 **[!UICONTROL Create Application]**.
1. 양식을 작성하여 애플리케이션을 만듭니다.
1. 에서 **[!UICONTROL Default Application Permissions]**&#x200B;앱 **[!UICONTROL r_basicprofile]** 및 **[!UICONTROL r_emailaddress]** 앱 권한을 활성화합니다.
1. 를 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** 다음으로 입력합니다 `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. 앱을 저장합니다.
1. 에서 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**&#x200B;전환 **[!UICONTROL Enable LinkedIn Login]** 설정을 로 **[!UICONTROL On]**&#x200B;전환합니다.
1. LinkedIn 클라이언트 ID 및 LinkedIn 클라이언트 암호를 입력합니다.
1. 클릭 **[!UICONTROL Save Settings]**.

완료되면 LinkedIn의 앱 세부 정보 페이지에는 앱의 API 키(소비자 키) 및 API 암호(소비자 암호)가 표시되어 Studio의 통합 설정 페이지에서 사용할 수 있습니다.
