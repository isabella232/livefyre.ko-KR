---
description: Microsoft Live ID에 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱을
  상호 작용할 수 있습니다.
seo-description: Microsoft Live ID에 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서
  앱을 상호 작용할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Microsoft Live Identity 앱 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Microsoft Live Identity 앱 만들기
uuid: 0 C 13 E 1 BC -817 F -43 ED -85 D 5-09 C 9 E 95 B 6234
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre ID와 함께 사용할 Microsoft Live Identity 앱 만들기{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Microsoft Live ID에 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있습니다.

사용자가 Microsoft Live ID 자격 증명을 사용하여 로그인할 수 있도록 하기 위해 Livefyre 에는 다음과 같은 Microsoft Live ID 정보가 필요합니다.

* 클라이언트 ID (개인 키)
* 클라이언트 암호 (암호)

Livefyre ID와 함께 사용할 Microsoft Live Identity 앱을 만들려면:

1. https://apps.dev.microsoft.com에서 [Microsoft Live 계정을 만들거나 로그인합니다.](https://apps.dev.microsoft.com/)
1. Livefyre ID에 사용할 기존 앱을 새로 만들거나 선택합니다.
1. 을 클릭하고 **[!UICONTROL Add Platform]**플랫폼 유형으로 웹을 선택합니다.
1. **[!UICONTROL Allow Implicit Flow]** 이 옵션이 선택되어 있는지 확인하고, {network-name} 대신 네트워크 이름을 사용하여 리디렉션 URL를 입력합니다. `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. 새 암호/키 쌍을 생성하여 개인 키를 가져옵니다.
1. 에서 **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]****[!UICONTROL Enable Microsoft Live Login]** 전환 스위치를 **[!UICONTROL On]**전환합니다.
1. Microsoft Live 클라이언트 ID와 Microsoft Live 클라이언트 암호를 입력합니다.
1. **[!UICONTROL Save Settings]**을 클릭합니다.

완료되면 Microsoft Live ID의 앱 세부 정보 페이지는 앱의 클라이언트 ID (소비자 키) 와 클라이언트 암호 (소비자 암호) 를 스튜디오의 통합 설정 페이지에 사용할 수 있도록 나열합니다.
