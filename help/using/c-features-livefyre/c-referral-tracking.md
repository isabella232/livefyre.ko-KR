---
description: 참조 트래픽에서 페이지로 다시 클릭 수를 추적합니다.
seo-description: 참조 트래픽에서 페이지로 다시 클릭 수를 추적합니다.
seo-title: 참조 추적
solution: Experience Manager
title: 참조 추적
uuid: 7 DAF 615 D -0 c 07-49 D 1-ADB 2-1 AC 67 EA 563 E 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 참조 추적{#referral-tracking}

참조 트래픽에서 페이지로 다시 클릭 수를 추적합니다.

Livefyre는 댓글이 소셜 네트워크에 게시되거나 소셜 네트워크에 공유될 때 URL에 참조 변수를 추가하고 Livefyre 이메일에 포함된 링크를 추가합니다. 이 변수를 사용하여 Livefyre 앱의 참조 트래픽을 Social 또는 소유한 소유물로 추적합니다.

Livefyre 앱을 사용하면 참조 트래픽으로 인한 데이터 스트림을 추적할 수 있으므로 사이트 트래픽을 분석할 수 있습니다.

## Livefyre 참조 트래픽 추적 {#section_nsy_qp4_xz}

소셜 네트워크 및 이메일의 Livefyre 참조 트래픽은 페이지의 URL에서 쿼리 문자열 매개 변수를 검사하고 페이지에서 코드를 구현하여 Analytics 공급자를 통해 추적할 수 있습니다. Livefyre는 댓글이 소셜 네트워크에 게시되거나 공유되는 경우 URL에 대한 참조 링크 및 Livefyre 이메일에 포함된 Permalink에 첨부합니다.

## 구현 예 {#section_xvs_x44_xz}

트래픽이 Streamhub 기반 알림에서 전송된 경우, 이메일, Facebook, Twitter, linkedin 또는 Permalink 값을 갖는 hubrefsrc 쿼리 문자열 매개 변수가 있습니다. Hubrefsrc 매개 변수 이름은 Livefyre 배달 팀에서 네트워크 수준에서 구성할 수 있습니다.

Analytics 플랫폼과 통합하려면 페이지가 로드에서 hubrefsrc를 찾고 있는 경우 트래픽을 기록해야 합니다.

예를 들면 다음과 같습니다.

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```



이 기능을 사용하는 앱:

* [채팅](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [평가](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

