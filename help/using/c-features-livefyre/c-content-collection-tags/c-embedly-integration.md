---
description: embed.ly를 사용하여 앱에 직접 다양한 미디어 형식을 표시합니다.
seo-description: embed.ly를 사용하여 앱에 직접 다양한 미디어 형식을 표시합니다.
seo-title: Embedly 통합
solution: Experience Manager
title: Embedly 통합
uuid: 1 F 27 E 32 C-C 2 C 3-4 F 7 C -93 de-C 9 C 7 BF 783 D 6 A
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Embedly 통합 {#embedly-integration}

앱에서 `embed.ly` 바로 다양한 미디어 포맷을 표시할 수 있습니다.

Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify, Tumblr 등 다양한 소스의 임베드된 미디어 컨텐츠를 보다 효과적으로 활용하기 위해 Livefyre 앱은 URL 확장을 위해 타사 공급자로 포함됩니다. 사용자나 중재자가 게시물에 지원되는 링크를 포함하는 경우 링크에 포함된 미디어가 컬렉션에 게시될 때 확장됩니다.

이를 통해 Livefyre 앱은 포함된 250 개 이상의 다양한 미디어 옵션에 액세스할 수 있습니다.

>[!NOTE]
>
>Livefyre는 Embedly의 전체 공급자 목록만 확장합니다. 공급자가 Twitter, YouTube, Imgur, Vine, Wikipedia 또는 Soundcloud 인 경우에만 포함된 이미지가 HTTPS 페이지에서 확장됩니다. 링크 확장 또는 소스에 대한 자세한 내용은 기술 계정 관리자에게 문의하십시오.

이 페이지에는 인기 있는 일부 미디어 유형 및 허용되는 URL 패턴의 예가 나와 있습니다. `Embed.ly` 는 계속해서 새 소스를 추가하고 있습니다. 전체 공급자 목록은 `https://embed.ly/embed/features/providers`에서 확인하십시오.

>[!NOTE]
>
>서식이 지정된 서식을 사용하려면 전체 Permalink가 필요합니다. 단축된 링크는 작동하지 않습니다.

공개적으로 볼 수 있는 컨텐츠만 임베드할 수 있습니다. 공개되지 않은 컨텐츠를 포함하려고 하면 컨텐츠에 대한 링크가 블로그 게시물에 나타나고 자리 표시자 아이콘이 함께 표시됩니다. 링크를 클릭하면 Facebook 메시지와 같이 컨텐츠가 호스팅된 서비스에서 친구의 오류 메시지에 대한 오류 메시지가 Reader에 표시됩니다. 미디어가 예상대로 확장되지 않으면 계정 관리자에게 문의하십시오.

## Embedly URL 샘플

| type | 공급자 | URL |
|--- |--- |--- |
| maps | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>****참고: URL는 다음으로 시작해야 `http` 합니다. `https.` |
| 소셜 네트워킹 | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| 비디오 | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| 사진 | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite의 컨텐츠 업로드 서비스) | `https://ow.ly/i/*` |
| 투표 | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | droplr | `https://d.pr/i/*` |
| 오디오 | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| 블로그 | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

이 기능을 사용하는 앱:

* [회전판](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [채팅](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [미디어 담벼락](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [모자이크](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [투표](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [트렌딩](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [업로드 단추](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

