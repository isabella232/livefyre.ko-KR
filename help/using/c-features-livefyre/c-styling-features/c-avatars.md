---
description: 사용자가 컨텐츠와 함께 표시되는 이미지를 사용자 지정할 수 있도록 허용합니다.
seo-description: 사용자가 컨텐츠와 함께 표시되는 이미지를 사용자 지정할 수 있도록 허용합니다.
seo-title: 아바타
title: 아바타
uuid: BF 20 F 3 BC -3 DCC -4 E 16-A 629-3380 D 1 A 7 A 3 F 2
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 아바타{#avatars}

사용자가 컨텐츠와 함께 표시되는 이미지를 사용자 지정할 수 있도록 허용합니다.

사용자 아바타는 모든 앱의 콘텐츠 옆에 (기본적으로) 표시되며 구현에서 사용되는 ID 프로필 시스템에서 가져옵니다. 이러한 아바타는 표시되는 앱에 따라 크기가 다릅니다.

(앱에는 표시되지 않을 경우 Livefyre를 사용하여 아바타를 비활성화할 수 있습니다.)

>[!NOTE]
>
>Avatar는 채팅 시 25 p x 25 p, 대부분의 다른 앱에서 50 p x 50 p에 표시됩니다.

## 아바타 스토리지 {#section_zbh_x1f_wy}

Avatars는 Livefyre에서 비동기식으로 로드됩니다. 사용자가 응용 프로그램에 처음 로그인하거나 연관된 아바타 이미지 파일을 변경하면 프로필 이미지가 작업 대기열에 추가됩니다. (사용자가 Livefyre 아바타 저장 위치에 업로드되는 동안 기본 아바타가 일시적으로 표시됩니다.)

## Gravatars {#section_mqh_p1f_wy}

Livefyre는 Gravatars 사용을 지원합니다. 사용자에게 사용자 프로필의 일부로 사용자 정의 아바타가 없는 경우 Livefyre는 해당 사용자를 위한 Gravatar를 확인합니다. Gravatar가 없는 경우 기본 아바타가 사용됩니다.

Livefyre wordpress 플러그인을 사용하여 주석이 포함된 경우 다음 조건이 충족되는 경우 사용자의 Gravatar가 사용됩니다.

* Gravatar가 wordpress 관리 패널에서 활성화되었으며,
* 사용자에게 Gravatar 계정이 있고,
* 사용자 지정 아바타가 제공되지 않습니다.

자세한 내용은 Wordpress Gravatar 설명서를 참조하십시오.



이 기능을 사용하는 앱:

* [회전판](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [채팅](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [미디어 담벼락](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [모자이크](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

