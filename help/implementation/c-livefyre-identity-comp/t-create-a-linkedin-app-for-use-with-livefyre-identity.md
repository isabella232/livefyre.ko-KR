---
description: Linkedin에서 Livefyre ID를 사용하여 사용자가 linkedin 로그인을 사용하여 사이트에서 앱을 상호 작용할
  수 있습니다.
seo-description: Linkedin에서 Livefyre ID를 사용하여 사용자가 linkedin 로그인을 사용하여 사이트에서 앱을 상호
  작용할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 linkedin 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 linkedin 앱 만들기
uuid: C 5112 F 24-A 4 E 0-4526-AFE 8-B 8 F 27 A 3 B 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre ID와 함께 사용할 linkedin 앱 만들기{#create-a-linkedin-app-for-use-with-livefyre-identity}

Linkedin에서 Livefyre ID를 사용하여 사용자가 linkedin 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.

Linkedin 로그인을 활성화하려면 Livefyre에 다음과 같은 linkedin 앱 정보가 필요합니다.

* Consumer 키 (API 키)
* Consumer secret (API secret)

Livefyre ID와 함께 사용할 linkedin 앱을 만들려면:

1. https://www.linkedin.com/secure/developer로 이동한 다음 Linkedin 계정에 로그인하여 새 앱을 만들거나 Livefyre ID에 사용할 기존 앱을 선택합니다.
1. **[!UICONTROL Create Application]** 을 클릭합니다.
1. 양식을 작성하여 애플리케이션을 만듭니다.
1. 에서 **[!UICONTROL Default Application Permissions]** **[!UICONTROL r_basicprofile]** 및 **[!UICONTROL r_emailaddress]** 앱 권한을 활성화합니다.
1. AS를 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** 입력합니다 `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. 앱을 저장합니다.
1. 에서 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** **[!UICONTROL Enable LinkedIn Login]** 전환 스위치를 **[!UICONTROL On]** 전환합니다.
1. Linkedin 클라이언트 ID 및 linkedin 클라이언트 암호를 입력합니다.
1. **[!UICONTROL Save Settings]** 을 클릭합니다.

완료되면, Linkedin의 앱 세부 정보 페이지는 앱의 API 키 (소비자 키) 와 API 암호 (소비자 암호) 를 스튜디오의 통합 설정 페이지에 사용할 수 있도록 나열합니다.
