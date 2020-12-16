---
description: Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.
seo-description: Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.
seo-title: Yahoo! 만들기 Livefyre ID와 함께 사용할 앱
solution: Experience Manager
title: Yahoo! 만들기 Livefyre ID와 함께 사용할 앱
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Yahoo! 만들기 Livefyre ID에 사용할 앱{#create-a-yahoo-app-for-use-with-livefyre-identity}

Yahoo!에서 Livefyre ID를 사용할 수 있습니다. 사용자가 Yahoo! 로그인 정보를 참조하십시오.

사용자가 Yahoo 자격 증명으로 로그인하도록 허용하려면 Livefyre에 다음 Yahoo 앱 정보가 필요합니다.

* 클라이언트 ID(소비자 키)
* 클라이언트 비밀(소비자 비밀)

Yahoo!를 만들려면 Livefyre ID와 함께 사용할 앱:

1. [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)로 이동하여 Yahoo!에 로그인합니다. 계정을 사용하여 새 앱을 만들거나 Livefyre ID에 사용할 기존 앱을 선택합니다.
1. 선택 **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. **[!UICONTROL API Permissions: Profiles (Social Directory)]** 및 **[!UICONTROL Read Public]**&#x200B;을 선택합니다.

   완료되면 Yahoo의 앱 세부 정보 페이지에는 Studio의 통합 설정 페이지에 사용할 앱의 클라이언트 ID(소비자 키) 및 클라이언트 암호(소비자 암호)가 나열됩니다.

   >[!NOTE]
   >
   >Yahoo! Yahoo! 앱과 함께 클라이언트 ID 및 클라이언트 암호 필드를 Studio에 비워 두면 Livefyre가 OpenID를 사용하여 이러한 사용자를 Livefyre 앱에 로그인합니다. 이 경우 OAuth 및 사용자 지정 브랜딩을 사용할 수 없습니다.