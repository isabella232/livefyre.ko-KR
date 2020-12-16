---
description: Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고 SEO에 맞게 유지할 수 있습니다.
seo-description: Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고 SEO에 맞게 유지할 수 있습니다.
seo-title: Storify 2에서 Google AMP 사용
solution: Experience Manager
title: Storify 2에서 Google AMP 사용
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Storify 2{#use-google-amp-with-storify}에서 Google AMP 사용

Livefyre API를 사용하여 Google AMP 기능을 Storify 2 페이지에 추가하여 컨텐츠를 인터랙티브하고 SEO에 맞게 유지할 수 있습니다.

Storify 2에서 Google AMP를 사용하려면 Google AMP 마크업이 있는 Storify 2 앱용 페이지를 만들어야 합니다.

앱의 AMP 버전이 원래 페이지에서 업데이트를 요청합니다(업데이트 요청에 대한 간격을 설정하려면 **amp-live-list** API의 **pollInterval** 매개 변수 사용). AMP 페이지의 방문자가 최신 컨텐츠를 빠르게 얻을 수 있도록 하려면 Storify 2 AMP 페이지에서 낮은 캐시 TTL을 유지하십시오.

Storify 2 앱의 게시물로 포함된 비이미지 자산(예: 비디오)은 AMP 사양에서 지정한 대로 HTTPS를 사용해야 합니다. Google Cloud CDN(Content Delivery Network)을 사용하는 AMP URL은 HTTPS를 사용합니다.

Storify 2에서 Google AMP를 사용하려면:

1. 사이트에서 AMP 유효성 검사 템플릿을 만듭니다.
1. 다음 Google AMP API 중 하나 이상을 사용하여 Google AMP 페이지를 사용자 정의합니다.
   1. [Storify 2 ](https://www.ampproject.org/docs/reference/components/amp-iframe) 디스플레이 사용자 정의
   1. [amp-live-listto](https://www.ampproject.org/docs/reference/components/amp-live-list) 를 사용하여 업데이트 시간 간격 사용자 정의
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) shareto소셜 공유 단추 추가
1. 다음 Storify 2 AMP 페이지의 내용을 `<style amp-custom>` 태그 내에 있는 Storify 2 페이지의 CSS에 포함시킵니다.[https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 다음 Storify 2 AMP 마크업 API의 내용을 Google AMP 템플릿에 포함하십시오.`https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 여기서 {{APP_ID}}은(는) Livefyre Studio의 Storify 2 앱에 대한 앱 ID입니다.
   1. 유일한 쿼리 매개 변수는 **pollInterval**&#x200B;입니다. 이 간격은 앱이 업데이트를 확인하는 간격(밀리초 단위)입니다.
   1. URL에는 최신 게시물(트윗, 비디오 등 포함)의 컨텐츠가 포함됩니다.
   1. 게시자 페이지는 Google AMP 페이지를 업데이트하려는 만큼 이 URL에서 컨텐트를 가져와야 합니다.
