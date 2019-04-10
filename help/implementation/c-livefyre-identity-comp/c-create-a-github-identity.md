---
description: Github ID와 Livefyre ID를 사용하여 사용자가 github 로그인을 사용하여 사이트의 앱을 상호 작용할 수 있습니다.
seo-description: Github ID와 Livefyre ID를 사용하여 사용자가 github 로그인을 사용하여 사이트의 앱을 상호 작용할
  수 있습니다.
seo-title: Livefyre ID와 함께 사용할 수 있는 github ID 앱 제작
title: Livefyre ID와 함께 사용할 수 있는 github ID 앱 제작
uuid: CF 56164 C -1521-4 A 42-89 CB -39483764807 E
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre ID와 함께 사용할 수 있는 github ID 앱 제작{#create-a-github-identity-app-for-use-with-livefyre-identity}

Github ID와 Livefyre ID를 사용하여 사용자가 github 로그인을 사용하여 사이트의 앱을 상호 작용할 수 있습니다.

사용자가 Github ID 자격 증명을 사용하여 로그인할 수 있도록 하려면 Livefyre에 다음과 같은 github ID 정보가 필요합니다.

* 클라이언트 ID (개인 키)
* 클라이언트 암호 (암호)

Livefyre ID와 함께 사용할 Github ID 앱을 만들려면:

1. 에서 Github 계정을 만들거나 로그인합니다 [](https://github.com/settings/developers).
1. Livefyre ID에 사용할 기존 앱을 새로 등록하거나 선택합니다.
1. 양식에 모든 정보를 입력합니다. 대신 네트워크 이름을 사용하여를 **[!UICONTROL Authorization callback URL]**입력합니다 `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. 에서 **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]****[!UICONTROL Enable GitHub Login]** 전환 스위치를 **[!UICONTROL On]**전환합니다.

1. Github 클라이언트 ID 및 github 클라이언트 암호를 입력합니다.
1. **[!UICONTROL Save Settings]**을 클릭합니다.

완료되면 Github ID의 앱 세부 정보 페이지는 앱의 클라이언트 ID (소비자 키) 와 클라이언트 암호 (소비자 암호) 를 스튜디오의 통합 설정 페이지에 사용할 수 있도록 나열합니다.
