---
description: embed.ly를 사용하여 앱에 직접 다양한 미디어 형식을 표시합니다.
seo-description: embed.ly를 사용하여 앱에 직접 다양한 미디어 형식을 표시합니다.
seo-title: Embedly 통합
solution: Experience Manager
title: Embedly 통합
uuid: 1f27e32c-c2c3-4f7c-93de-c9c7bf783d6a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Embedly 통합{#embedly-integration}

Use `embed.ly` to display multiple media formats, directly in the App.

Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify, Tumblr 등 다양한 소스의 임베디드 미디어 컨텐츠를 보다 효과적으로 사용하려면 Livefyre 앱이 URL 확장을 위한 타사 공급자로 Embeddly를 사용합니다. 사용자나 중재자가 게시물에 지원되는 링크를 포함하는 경우, 링크에 포함된 미디어는 컬렉션에 게시되면 확장됩니다.

Livefyre 앱에서 임베딩에서 지원하는 250개 이상의 임베디드 미디어 옵션에 액세스할 수 있습니다.

>[!NOTE]
>
>Livefyre는 Embeddly의 전체 공급자 목록의 하위 집합만 확장합니다. 임베디드 이미지는 제공업체가 Twitter, YouTube, Imgur, Vine, Wikipedia 또는 SoundCloud인 경우에만 HTTPS 페이지에서 확장됩니다. 링크 확장 또는 출처에 대한 자세한 내용은 기술 계정 관리자에게 문의하십시오.

이 페이지에는 자주 사용되는 포함된 미디어 유형 및 허용되는 URL 패턴의 예가 나와 있습니다. `Embed.ly` 는 새로운 소스를 지속적으로 추가하고 있습니다. 공급자 전체 목록을 보려면 로 이동하십시오 `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>임베디드 서식을 사용하려면 전체 링크가 필요합니다. 단축된 링크는 작동하지 않습니다.

공개적으로 볼 수 있는 컨텐츠만 임베드할 수 있습니다. If you attempt to embed a piece of content that is not public, the link to the content will appear in the blog post, and a placeholder icon will accompany it. When clicked, the link will take the reader to an error message from the service where the content is hosted, such as a Facebook message for a friends-only photo. Please contact your Account Manager if you notice that media is not expanded as expected.

## Sample Embedly URLs

| 유형 | 공급자 | URL |
|--- |--- |--- |
| Maps | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**참고**:URL은 다음으로 `http` 시작해야 합니다. `https.` |
| 소셜 네트워킹 | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| 비디오 | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| 사진 | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite의 컨텐츠 업로드 서비스) | `https://ow.ly/i/*` |
| 투표 | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | 드롭러 | `https://d.pr/i/*` |
| 오디오 | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| 블로그 | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

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
* [업로드 버튼](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

