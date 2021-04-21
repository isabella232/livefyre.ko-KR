---
description: 비디오 도메인 목록을 허용할 수 있습니다.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Livefyre 시각화 앱에 표시되는 비디오의 일부로 사용자 정의 비디오 및 플레이어를 사용하는 경우 비디오 도메인을 허용 목록에 추가할 수 있습니다. 비디오 도메인 목록을 허용하면 사용자 정의 비디오 및 플레이어에 대한 비디오 마스크가 제거됩니다.

>[!NOTE]
>
>특정 경로를 사용하여 안전한 비디오만 허용 목록에 표시할 수 있습니다. 넓은 경로(예: sampledomain.com)를 삽입하는 경우 안전하지 않은 비디오를 허용할 수 있습니다.

* `userPrivacyOptOut` 뒤에 `userPrivacyVideoWhitelist`을 추가합니다. 모든 Livefyre 개인정보 보호 플래그를 하나의 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.
* `userPrivacyVideoWhitelist` 소셜 미디어에 포함되지 않은 컨텐츠에만 적용됩니다.

다음 예에서 `sampledomain.com/cdn/videos` 경로를 사용하여 앱에 표시되는 비디오는 허용 목록에 표시됩니다.

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
