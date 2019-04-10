---
description: Google에서 Livefyre ID를 사용하여 Google 로그인 기능을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.
seo-description: Google에서 Livefyre ID를 사용하여 Google 로그인 기능을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.
seo-title: Livefyre ID와 함께 사용할 Google 프로젝트 만들기
solution: Experience Manager
title: Livefyre ID와 함께 사용할 Google 프로젝트 만들기
uuid: B 0 A 6 BB 8 A-ABEA -4 F 5 C -92 ED -026 E 60183 E 1 D
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre ID와 함께 사용할 Google 프로젝트 만들기{#create-a-google-project-for-use-with-livefyre-identity}

Google에서 Livefyre ID를 사용하여 Google 로그인 기능을 사용하여 사이트의 앱과 상호 작용할 수 있습니다.

사용자가 Google 자격 증명을 사용하여 로그인할 수 있도록 하기 위해 Livefyre 에는 다음과 같은 Google 프로젝트 정보가 필요합니다.

* 클라이언트 ID
* 클라이언트 암호

Livefyre ID와 함께 사용할 Google 프로젝트를 만들려면:

1. [https://console.cloud.google.com/project](https://console.cloud.google.com/project) 로 이동하고 Google 계정에 로그인하여 Livefyre ID에 사용할 기존 앱을 새로 만들거나 선택합니다.
1. 앱용 프로젝트 대시보드 내에서 **[!UICONTROL Enable and Manage APIs]**를 클릭합니다.
1. API 개요 페이지의 소셜 API에서를 클릭하여 Google + API를 활성화합니다.
1. API 자격 증명 페이지에서 **[!UICONTROL Credentials > New credentials > OAuth]** 클라이언트 ID를 선택합니다. **[!UICONTROL Create client ID]** 페이지가 열리면 다음을 수행합니다.

   * 애플리케이션 유형을 선택합니다. 웹 애플리케이션.
   * 에 대한을 **[!UICONTROL Name]****[!UICONTROL Client ID]**입력합니다.
   * 필드를 **[!UICONTROL Authorized JavaScript origins]** 비워 둡니다.
   * **[!UICONTROL Authorized redirect URIs]**Enter: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` Livefyre **[!UICONTROL {networkName}]** 는 네트워크 이름을 제공합니다. 예를 들면 다음과 같습니다. ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * 자격 증명을 **[!UICONTROL Create]** 저장하려면을 클릭합니다.

완료되면 Google의 API 관리자 > 자격 증명 페이지가 프로젝트의 클라이언트 ID와 클라이언트 암호를 나열하여 스튜디오의 통합 설정 페이지에 사용합니다.
