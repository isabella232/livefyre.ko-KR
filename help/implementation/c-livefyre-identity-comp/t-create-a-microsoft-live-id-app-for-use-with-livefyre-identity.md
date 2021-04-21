---
description: Microsoft Live Id와 함께 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.
title: Livefyre ID와 함께 사용할 Microsoft Live ID 앱 만들기
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Livefyre ID에 사용할 Microsoft Live ID 앱 만들기{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Microsoft Live Id와 함께 Livefyre ID를 사용하여 사용자가 Facebook 로그인을 사용하여 사이트에서 앱을 상호 작용할 수 있도록 할 수 있습니다.

사용자가 Microsoft Live ID 자격 증명으로 로그인하도록 허용하려면 Livefyre에 다음 Microsoft Live ID 정보가 필요합니다.

* 클라이언트 ID(개인 키)
* 클라이언트 암호(암호)

Livefyre ID에 사용할 Microsoft Live ID 앱을 만들려면:

1. [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)에서 Microsoft Live 계정을 만들거나 로그인합니다.
1. Livefyre ID에 사용할 앱을 새로 만들거나 기존 앱을 선택합니다.
1. **[!UICONTROL Add Platform]**&#x200B;을 클릭한 다음 플랫폼 유형으로 [웹]을 선택합니다.
1. **[!UICONTROL Allow Implicit Flow]** 옵션이 선택되어 있는지 확인하고 {network-name} 대신 네트워크 이름을 사용하여 리디렉션 URL을 입력합니다.`https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. 새 암호/키 쌍을 생성하여 개인 키를 가져옵니다.
1. **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**&#x200B;에서 **[!UICONTROL Enable Microsoft Live Login]** 전환을 **[!UICONTROL On]**&#x200B;로 전환합니다.
1. Microsoft Live 클라이언트 ID 및 Microsoft Live 클라이언트 암호를 입력합니다.
1. 클릭 **[!UICONTROL Save Settings]**.

완료되면 Microsoft Live Id의 앱 세부 정보 페이지에는 Studio의 통합 설정 페이지에 사용할 앱의 클라이언트 ID(소비자 키) 및 클라이언트 암호(소비자 암호)가 나열됩니다.
