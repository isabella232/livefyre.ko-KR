---
description: GitHub Identity와 함께 Livefyre Identity를 사용하여 사용자가 GitHub 로그인을 사용하여 사이트에서 Apps와 상호 작용할 수 있도록 할 수 있습니다.
seo-description: GitHub Identity와 함께 Livefyre Identity를 사용하여 사용자가 GitHub 로그인을 사용하여 사이트에서 Apps와 상호 작용할 수 있도록 할 수 있습니다.
seo-title: Livefyre Identity와 함께 사용할 GitHub ID 앱 만들기
title: Livefyre Identity와 함께 사용할 GitHub ID 앱 만들기
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre Identity와 함께 사용할 GitHub ID 앱 만들기{#create-a-github-identity-app-for-use-with-livefyre-identity}

GitHub Identity와 함께 Livefyre Identity를 사용하여 사용자가 GitHub 로그인을 사용하여 사이트에서 Apps와 상호 작용할 수 있도록 할 수 있습니다.

사용자가 GitHub ID 자격 증명을 사용하여 로그인할 수 있도록 하려면 Livefyre에 다음 GitHub ID 정보가 필요합니다.

* 클라이언트 ID(개인 키)
* 클라이언트 암호(암호)

Livefyre Identity와 함께 사용할 GitHub ID 앱을 만들려면:

1. 에서 GitHub 계정을 만들거나 로그인합니다 [](https://github.com/settings/developers).
1. Livefyre Id에 사용할 새 앱을 등록하거나 기존 앱을 선택합니다.
1. 양식에 모든 정보를 입력합니다. 네트워크 **[!UICONTROL Authorization callback URL]**&#x200B;이름 대신 를 입력합니다 `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. 에서 **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**&#x200B;전환 **[!UICONTROL Enable GitHub Login]** 설정을 로 **[!UICONTROL On]**&#x200B;전환합니다.

1. GitHub 클라이언트 ID 및 GitHub 클라이언트 암호를 입력합니다.
1. 클릭 **[!UICONTROL Save Settings]**.

완료되면 GitHub Identity의 앱 세부 정보 페이지에는 Studio의 통합 설정 페이지에서 사용할 앱의 클라이언트 ID(소비자 키) 및 클라이언트 암호(소비자 암호)가 표시됩니다.
