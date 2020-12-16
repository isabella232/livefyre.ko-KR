---
description: LinkedIn과 함께 Livefyre ID를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.
seo-description: LinkedIn과 함께 Livefyre ID를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 LinkedIn 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 LinkedIn 앱 만들기
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Livefyre ID에 사용할 LinkedIn 앱 만들기{#create-a-linkedin-app-for-use-with-livefyre-identity}

LinkedIn과 함께 Livefyre ID를 사용하여 사용자가 LinkedIn 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.

LinkedIn 로그인을 사용하려면 Livefyre에 다음과 같은 LinkedIn 앱 정보가 필요합니다.

* 소비자 키(API 키)
* 소비자 비밀(API 비밀)

Livefyre ID에 사용할 LinkedIn 앱을 만들려면:

1. https://www.linkedin.com/secure/developer으로 이동하여 LinkedIn 계정에 로그인하여 새 앱을 만들거나 Livefyre ID에 사용할 기존 앱을 선택합니다.
1. 클릭 **[!UICONTROL Create Application]**.
1. 양식을 작성하여 애플리케이션을 만듭니다.
1. **[!UICONTROL Default Application Permissions]**&#x200B;에서 **[!UICONTROL r_basicprofile]** 및 **[!UICONTROL r_emailaddress]** 앱 권한을 활성화합니다.
1. **[!UICONTROL OAuth 2.0 Authorized Redirect URL]**&#x200B;을 `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`(으)로 입력합니다.
1. 앱을 저장합니다.
1. **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**&#x200B;에서 **[!UICONTROL Enable LinkedIn Login]** 전환을 **[!UICONTROL On]**&#x200B;로 전환합니다.
1. LinkedIn 클라이언트 ID 및 LinkedIn 클라이언트 암호를 입력합니다.
1. 클릭 **[!UICONTROL Save Settings]**.

완료되면 LinkedIn의 앱 세부 정보 페이지에는 Studio의 통합 설정 페이지에 사용할 앱의 API 키(소비자 키) 및 API 암호(소비자 암호)가 나열됩니다.
