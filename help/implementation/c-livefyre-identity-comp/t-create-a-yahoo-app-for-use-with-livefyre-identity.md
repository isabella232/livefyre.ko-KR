---
description: Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.
seo-description: Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.
seo-title: Yahoo! 만들기 Livefyre ID와 함께 사용할 앱
solution: Experience Manager
title: Yahoo! 만들기 Livefyre ID와 함께 사용할 앱
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Yahoo! 만들기 Livefyre ID와 함께 사용할 앱{#create-a-yahoo-app-for-use-with-livefyre-identity}

Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.

사용자가 Yahoo 자격 증명을 사용하여 로그인하도록 허용하려면 Livefyre에 다음 Yahoo App 정보가 필요합니다.

* 클라이언트 ID(소비자 키)
* 클라이언트 암호(소비자 암호)

Yahoo! livefyre Identity와 함께 사용할 수 있는 앱:

1. https://developer.yahoo.com/apps/ [으로](https://developer.yahoo.com/apps/)이동하여 Yahoo! 계정을 사용하여 새 앱을 만들거나 Livefyre Id와 함께 사용할 기존 앱을 선택합니다.
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. 및 **[!UICONTROL API Permissions: Profiles (Social Directory)]** 을 **[!UICONTROL Read Public]**&#x200B;선택합니다.

   완료되면 Yahoo의 앱 세부 정보 페이지에는 앱의 클라이언트 ID(소비자 키) 및 클라이언트 암호(소비자 암호)가 표시되어 Studio의 통합 설정 페이지에 사용됩니다.

   >[!NOTE]
   >
   >Yahoo! yahoo! 앱과 클라이언트 ID 및 클라이언트 암호 필드를 Studio에 비워 두면 Livefyre가 OpenID를 사용하여 이러한 사용자를 Livefyre 앱에 기록합니다. 이 경우 OAuth 및 사용자 지정 브랜딩을 사용할 수 없습니다.