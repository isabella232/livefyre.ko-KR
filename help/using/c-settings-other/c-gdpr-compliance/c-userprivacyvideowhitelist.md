---
description: 를 사용하여 비디오 도메인을 허용 목록에 추가할 수 있습니다.
seo-description: 를 사용하여 비디오 도메인을 허용 목록에 추가할 수 있습니다.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

사용자 정의 비디오 및 플레이어를 Livefyre 시각화 앱에 표시되는 비디오의 일부로 사용하는 경우 비디오 도메인을 허용 목록에 추가할 수 있습니다. 비디오 도메인을 허용 목록에 추가하면 사용자 정의 비디오 및 플레이어에 대한 비디오 마스크가 제거됩니다.

>[!NOTE]
>
>특정 경로를 사용하여 안전한 비디오만 허용 목록에 표시됩니다. 넓은 경로(예: sampleddomain.com)를 배치하면 안전하지 않은 비디오를 허용 목록에 추가할 수 있습니다.

* 이후 `userPrivacyVideoWhitelist` 추가를 `userPrivacyOptOut`참조하십시오. 모든 Livefyre 개인정보 보호 플래그를 한 Livefyre 개체의 일부로 한 번에 추가할 수 있습니다.
* `userPrivacyVideoWhitelist` 소셜 미디어에서 포함되지 않은 컨텐츠에만 적용됩니다.

다음 예제에서는 `sampledomain.com/cdn/videos` 경로를 사용하여 앱에 표시되는 비디오가 허용 목록에 표시됩니다.

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
