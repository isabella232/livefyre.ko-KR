---
description: 을 사용하여 비디오 도메인을 허용 목록에 추가할 수 있습니다.
seo-description: 을 사용하여 비디오 도메인을 허용 목록에 추가할 수 있습니다.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Livefyre 시각화 앱에 표시되는 비디오의 일부로 사용자 정의 비디오 및 플레이어를 사용하는 경우 비디오 도메인을 화이트리스트에 추가할 수 있습니다. 비디오 도메인을 화이트리스트하면 사용자 정의 비디오 및 플레이어에 사용할 비디오 마스크가 제거됩니다.

>[!NOTE]
>
>특정 경로를 사용하여 안전한 비디오만 화이트리스트에 포함됩니다. 광범위한 경로 (예: sampledomain.com) 를 사용하면 안전하지 않은 비디오를 화이트리스트에 추가할 수 있습니다.

* 이후에 `userPrivacyVideoWhitelist` 추가합니다 `userPrivacyOptOut`. Livefyre의 모든 개인정보 보호 플래그를 하나의 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.
* `userPrivacyVideoWhitelist` 소셜 미디어에서 포함되지 않은 컨텐츠에만 적용됩니다.

다음 예에서는 `sampledomain.com/cdn/videos` 경로의 앱에 표시되는 비디오가 화이트리스트에 포함됩니다.

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
