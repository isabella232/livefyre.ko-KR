---
description: Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고 SEO
  친화적으로 유지할 수 있습니다.
seo-description: Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고
  SEO 친화적으로 유지할 수 있습니다.
seo-title: Storify 2와 Google AMP 사용
solution: Experience Manager
title: Storify 2와 Google AMP 사용
uuid: 40 C 9 F 083-7284-43 BA-AE 27-53 B 1 FF 9 E 3954
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Storify 2와 Google AMP 사용{#use-google-amp-with-storify}

Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고 SEO 친화적으로 유지할 수 있습니다.

Storify 2와 함께 Google AMP를 사용하려면 Google AMP 마크업으로 Storify 2 앱에 대한 페이지를 만들어야 합니다.

AMP 버전의 앱은 원래 페이지에서 업데이트를 요청합니다 (amp-live-list API에서 **pollinterval** **매개 변수를** 사용하여 업데이트 요청 간격 설정). AMP 페이지의 방문자가 최신 컨텐츠를 빠르게 얻도록 하려면 Storify 2 amp 페이지에 낮은 캐시 TTL를 두십시오.

Storify 2 앱에 게시물로 포함된 비이미지 자산 (예: 비디오) 는 AMP 사양에 지정된 HTTPS를 사용해야 합니다. Google 클라우드 CDN (Content Delivery Network) 를 사용하는 AMP URL는 HTTPS를 사용합니다.

Storify 2와 함께 Google AMP를 사용하려면

1. 사이트에서 AMP 인증 템플릿을 만들 수 있습니다.
1. 다음 Google AMP API 중 하나 이상을 사용하여 Google AMP 페이지를 사용자 정의합니다.
   1. [amp-iframe to](https://www.ampproject.org/docs/reference/components/amp-iframe) customize the storify 2 display
   1. [amp-live-list를 사용하여](https://www.ampproject.org/docs/reference/components/amp-live-list) 업데이트를 위한 시간 간격 사용자 정의
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) 를 사용하여 소셜 공유 단추 추가
1. 다음 Storify 2 AMP 페이지의 내용을 <style amp-custom> 태그: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 다음 Storify 2 AMP 마크업 API의 내용을 Google AMP 템플릿에 포함시킵니다. `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 여기서 {{app_ id}} 는 Livefyre Studio의 Storify 2 앱에 대한 앱 ID 입니다.
   1. 유일한 쿼리 매개 변수는 앱이 업데이트를 확인하는 간격인 **Pollinterval**입니다 (밀리초 단위 설정).
   1. URL 에는 가장 최근 게시물 (트윗, 비디오 등) 의 컨텐츠가
   1. Google AMP 페이지를 업데이트하려면 발행자 페이지가 이 URL의 내용을 자주 가져와야 합니다.
