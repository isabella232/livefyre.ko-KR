---
description: Yahoo! 사용자가 Yahoo! 로그인을 참조하십시오.
seo-description: Yahoo! 사용자가 Yahoo! 로그인을 참조하십시오.
seo-title: Yahoo! Livefyre ID와 함께 사용할 수 있는 앱
solution: Experience Manager
title: Yahoo! Livefyre ID와 함께 사용할 수 있는 앱
uuid: 6863 CD 2 E-EB 0 D -465 B-B 706-88 ECACCF 41 BC
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Yahoo! Livefyre ID와 함께 사용할 수 있는 앱{#create-a-yahoo-app-for-use-with-livefyre-identity}

Yahoo! 사용자가 Yahoo! 로그인을 참조하십시오.

사용자가 Yahoo 자격 증명으로 로그인할 수 있도록 하기 위해 Livefyre 에는 다음과 같은 Yahoo 앱 정보가 필요합니다.

* 클라이언트 ID (소비자 키)
* 클라이언트 암호 (소비자 비밀)

Yahoo! Livefyre ID 사용 앱:

1. [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)로 이동하여 Yahoo! Livefyre ID에 사용할 기존 앱을 새로 만들거나 기존 앱을 선택합니다.
1. **[!UICONTROL Application Type: Web Application]**Select.
1. Enter **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. **[!UICONTROL API Permissions: Profiles (Social Directory)]****[!UICONTROL Read Public]**AND를 선택합니다.

   완료되면, Yahoo의 앱 세부 정보 페이지는 앱의 클라이언트 ID (소비자 키) 와 클라이언트 암호 (소비자 암호) 를 스튜디오의 통합 설정 페이지에 사용할 수 있도록 나열합니다.

   >[!NOTE]
   >
   >Yahoo! Yahoo! 앱을 사용하고 클라이언트 ID와 클라이언트 비밀 필드를 Studio Blank에 두면 Livefyre는 openid를 사용하여 이러한 사용자를 Livefyre 앱에 로그인합니다. 이 경우에는 OAuth 및 사용자 정의 브랜딩을 사용할 수 없습니다.