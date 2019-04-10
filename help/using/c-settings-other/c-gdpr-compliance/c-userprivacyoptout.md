---
description: 사이트 방문자가 이 추적을 거부할 수 있도록 Userprivacyoptout 플래그를 페이지에 추가합니다.
seo-description: 사이트 방문자가 이 추적을 거부할 수 있도록 Userprivacyoptout 플래그를 페이지에 추가합니다.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: A 043 C 50 E -0 A 02-4 C 83-BBCE -54 B 9 B 51316 A 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyoptout{#userprivacyoptout}

사이트 방문자가 이 추적을 거부할 수 있도록 `userPrivacyOptOut` 페이지에 플래그를 추가합니다.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다.

Livefyre 앱을 내장하고 방문자가 추적에 동의하지 않는 경우, Livefyre를 동적으로 구성하여 방문자의 개인 정보를 보장하는 기능을 비활성화할 수 있습니다.

구성된 경우 Livefyre는 다음을 수행합니다.

* 앱에서 인증 지원을 비활성화합니다.
* Livecount 및 이벤트 생성 비활성화
* 페이지에 있는 앱에서 만든 기존 쿠키를 삭제합니다.
* 타사 도메인의 이미지가 포함된 프록시 미디어를 사용하여 타사 쿠키 만들기 방지
* 추가 클릭이 필요한 타사 비디오에 대한 비디오 마스크 클릭스루 사용

## 옵트아웃을 위한 페이지 구성

Livefyre 앱을 임베드하는 통합은 사이트 방문자가 단일 JavaScript 변수를 사용하여 동의하지 않은 경우 Livefyre를 구성할 수 있습니다.

지침:

1. JavaScript 앞에 `userPrivacyOptOut` 플래그를 `Livefyre.js` 추가합니다.

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 이후에 `Livefyre.js` 페이지에 추가합니다 `userPrivacyOptOut`.

   Livefyre 앱은 더 높은 개인 정보 설정으로 인스턴스화합니다.

   >[!NOTE]
   >
   >Livefyre 앱이 로드한 `userPrivacyOptOut` 후에는 값을 변경하지 마십시오.

사이트 방문자가 옵트아웃을 선택하는 경우 동의 워크플로우에서를 `userPrivacyOptOut` true로 설정합니다.
