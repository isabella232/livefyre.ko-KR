---
description: 사이트 방문자가 이 추적을 옵트아웃할 수 있도록 userPrivacyOptOut 플래그를 페이지에 추가합니다.
seo-description: 사이트 방문자가 이 추적을 옵트아웃할 수 있도록 userPrivacyOptOut 플래그를 페이지에 추가합니다.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

사이트 방문자가 이 추적을 옵트아웃할 수 있도록 페이지에 `userPrivacyOptOut` 플래그를 추가합니다.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다.

Livefyre 앱을 포함하고 방문자가 추적에 동의하지 않는 경우 Livefyre가 기능을 비활성화하도록 동적으로 구성하여 방문자의 개인 정보를 보호할 수 있습니다.

구성되면 Livefyre는 다음을 수행합니다.

* 앱에서 인증 지원을 비활성화합니다.
* LiveCount 및 이벤트 생성 비활성화
* 페이지에 있는 앱에서 만든 기존 쿠키 삭제
* 타사 도메인이 쿠키를 만들지 못하도록 타사 도메인의 이미지가 있는 프록시 미디어
* 추가 클릭이 필요한 타사 비디오에 대한 비디오 마스크 클릭스루 활성화

## 옵트아웃을 위한 페이지 구성

Livefyre 앱을 내장하는 통합으로 사이트 방문자가 단일 JavaScript 변수를 사용하여 동의하지 않을 때 Livefyre를 구성할 수 있습니다.

지침:

1. JavaScript 앞에 `userPrivacyOptOut` 플래그를 `Livefyre.js` 추가합니다.

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 이후 `Livefyre.js` 어디에서나 페이지에 추가합니다 `userPrivacyOptOut`.

   Livefyre 앱은 향상된 개인 정보 설정을 사용하여 인스턴스화합니다.

   >[!NOTE]
   >
   >Livefyre 앱이 로드되면 값을 변경하지 `userPrivacyOptOut` 마십시오.

사이트 방문자가 옵트아웃을 선택한 경우 동의 워크플로우가 `userPrivacyOptOut` true로 설정되었는지 확인합니다.
