---
description: 사이트 방문자가 이 추적을 옵트아웃할 수 있도록 userPrivacyOptOut 플래그를 페이지에 추가합니다.
seo-description: 사이트 방문자가 이 추적을 옵트아웃할 수 있도록 userPrivacyOptOut 플래그를 페이지에 추가합니다.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

사이트 방문자가 이 추적을 옵트아웃할 수 있도록 페이지에 `userPrivacyOptOut` 플래그를 추가합니다.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다.

Livefyre 앱을 포함하고 방문자가 추적에 동의하지 않는 경우, 방문자의 개인 정보를 보호하기 위해 기능을 비활성화하도록 Livefyre를 동적으로 구성할 수 있습니다.

구성되면 Livefyre는 다음을 수행합니다.

* 앱에서 인증 지원을 비활성화합니다.
* Livecount 및 이벤트 생성 비활성화
* 페이지에 있는 앱에서 만든 기존 쿠키 삭제
* 제3자가 쿠키를 만들지 못하도록 하기 위해 제3자 도메인의 이미지가 있는 프록시 미디어
* 보기 위해 추가 클릭이 필요한 제3자 비디오에 대해 비디오 마스크 클릭스루 사용

## 옵트아웃 페이지 구성

Livefyre 앱을 포함하는 통합으로 사이트 방문자가 단일 JavaScript 변수를 사용하여 동의를 하지 않은 경우 Livefyre를 구성할 수 있습니다.

지침:

1. `Livefyre.js` JavaScript 앞에 `userPrivacyOptOut` 플래그를 추가합니다.

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. `userPrivacyOptOut` 뒤에 있는 페이지에 `Livefyre.js`을 추가합니다.

   Livefyre 앱은 향상된 개인정보 보호 설정으로 인스턴스화합니다.

   >[!NOTE]
   >
   >Livefyre 앱이 로드되면 `userPrivacyOptOut` 값을 변경하지 마십시오.

사이트 방문자가 옵트아웃을 선택한 경우 동의 워크플로우에서 `userPrivacyOptOut`을(를) true로 설정하도록 하십시오.
