---
description: 다른 사용자의 콘텐츠 또는 콘텐츠를 Facebook, Twitter 또는 LinkedIn으로 공유합니다.
seo-description: 다른 사용자의 콘텐츠 또는 콘텐츠를 Facebook, Twitter 또는 LinkedIn으로 공유합니다.
seo-title: 소셜 공유
solution: Experience Manager
title: 소셜 공유
uuid: 3fd8a628-2414-45b5-b91c-2ad33aad2634
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 소셜 공유{#social-sharing}

다른 사용자의 콘텐츠 또는 콘텐츠를 Facebook, Twitter 또는 LinkedIn으로 공유합니다.

소셜 미디어 공유를 사용하면 커뮤니티는 앱의 의견을 Facebook, Twitter 및 LinkedIn을 비롯한 소셜 네트워크의 친구와 공유하고 다른 사용자의 컨텐츠를 Facebook 및 Twitter에 공유할 수 있습니다. 소셜 미디어 공유를 활성화하면 커뮤니티에서 컨텐츠에 대한 최상의 응답을 전파하고 더 많은 트래픽을 사이트에 가져올 수 있습니다.

## 소셜 네트워크에 컨텐츠 공유 {#section_t1q_mz2_wy}

Livefyre 앱에 콘텐츠를 게시할 때 사용자가 Twitter, Facebook 또는 LinkedIn에 공유할 수 있도록 네트워크를 구성할 수 있습니다. 기본 Livefyre에는 세 사이트 모두에 대한 링크가 **[!UICONTROL Share Modal]** 포함되어 있습니다. 귀하는 게시물 API를 사용하여 이 모달을 사용자 지정하여 Livefyre 기본값을 재정의하고 고유한 양식을 구현할 수 있습니다. 자세한 내용은 고급 항목 &gt; 소셜 공유 활성화를 참조하십시오.

사용자가 소셜 네트워크(Facebook, Twitter 또는 LinkedIn)에 댓글을 게시하기 **[!UICONTROL Share]** 위해 클릭하면 소셜 앱을 통해 로그인하라는 메시지가 표시됩니다. 사용 가능한 공유 옵션 목록을 사용자 정의할 수 있습니다. 기본적으로 Facebook 및 Twitter 공유 확인란은 모든 앱에 표시됩니다.) 사용자 지정 네트워크의 경우 소셜 앱을 소셜 앱으로 구성해야 합니다. 통합 프로세스의 일부로 Studio의 통합 설정 페이지를 통해 앱 자격 증명을 추가하십시오.

>[!NOTE]
>
>LinkedIn은 Livefyre 커뮤니티 댓글에 기본적으로 포함되어 있습니다. 사용자 지정 네트워크는 앱을 포함할 때 'li' 값을 전달하여 주석 도구 모음에서 LinkedIn 단추를 활성화해야 합니다. (자세한 내용은 개발자 문서에서 소셜 공유 활성화를 참조하십시오.)

## 다른 사용자의 컨텐츠를 소셜 네트워크에 공유 {#section_blw_vy2_wy}

다른 사용자의 게시물을 **[!UICONTROL Share]** 클릭하면 [주석 공유] 창이 열립니다. 이 창에는 편집 가능한 텍스트 필드, 사용 가능한 공유 옵션 및 게시물에 대한 링크가 포함되어 있습니다.

게시물을 **[!UICONTROL Share]** 클릭하여 다음을 수행합니다.

* 사용자는 Twitter 또는 Facebook 아이콘을 클릭하여 소셜 네트워크에 연결할 수 있습니다.
* 사용자의 소셜 네트워크에 페이지를 게시하도록 인증한 후 Twitter 또는 Facebook 단추가 표시되어 사용자가 활성 상태임을 알려줍니다.
* 사용자는 공유 게시물 상자 내에서 컨텐츠를 개인화할 수 있습니다.
* 을 **[!UICONTROL Share]** 클릭하면 사용자의 활성 소셜 네트워크에 컨텐츠가 전송되고, 이 링크를 통해 사용자가 공유하려는 정확한 게시물이 다른 사람에게 전송됩니다.
* 또한 사용자는 이메일, 블로그 게시물 또는 소셜 네트워크 내에 Permalink를 붙여 넣어 특정 댓글에 대한 링크를 공유하도록 선택할 수 있습니다.

>[!NOTE]
>
>통합 중에 사용자가 공유할 수 있는 소셜 네트워크를 결정할 수 있습니다. 사용자 정의 Permalink를 통합하여 현재 미디어 링크와 균일성을 부여할 수도 있습니다.

다른 **[!UICONTROL Share]** 사용자의 게시물을 클릭하면 편집 가능한 텍스트 필드, 사용 가능한 공유 옵션 및 게시물에 대한 링크가 포함된 **[!UICONTROL Share Comment]** 창이 열립니다.

게시물을 **[!UICONTROL Share]** 클릭하여 다음을 수행합니다.

* 사용자는 Twitter 또는 Facebook 아이콘을 클릭하여 소셜 네트워크에 연결할 수 있습니다.
* 사용자의 소셜 네트워크에 페이지를 게시하도록 인증한 후 Twitter 또는 Facebook 단추가 표시되어 사용자가 활성 상태임을 알려줍니다.
* 사용자는 공유 게시물 상자 내에서 컨텐츠를 개인화할 수 있습니다.
* 을 **[!UICONTROL Share]** 클릭하면 사용자의 활성 소셜 네트워크에 컨텐츠가 전송되고, 이 링크를 통해 사용자가 공유하려는 정확한 게시물이 다른 사람에게 전송됩니다.
* 또한 사용자는 이메일, 블로그 게시물 또는 소셜 네트워크 내에 Permalink를 붙여 넣어 특정 댓글에 대한 링크를 공유하도록 선택할 수 있습니다.

>[!NOTE]
>
>통합 중에 사용자가 공유할 수 있는 소셜 네트워크를 결정할 수 있습니다. 사용자 정의 Permalink를 통합하여 현재 미디어 링크와 균일성을 부여할 수도 있습니다.



이 기능을 사용하는 앱:

* [회전판](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [대화](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [기능 카드](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [맵](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [모자이크](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [투표](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [사이드노트](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [트렌딩](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)

