---
description: 참조 트래픽에서 페이지로의 클릭을 추적합니다.
seo-description: 참조 트래픽에서 페이지로의 클릭을 추적합니다.
seo-title: 참조 추적
solution: Experience Manager
title: 참조 추적
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# 참조 추적{#referral-tracking}

참조 트래픽에서 페이지로의 클릭을 추적합니다.

소셜 네트워크에 댓글이 게시되거나 공유될 때, 그리고 Livefyre 이메일에 포함된 링크용 참조 변수를 URL에 추가합니다. 이 변수를 사용하여 Livefyre 앱에서 소셜 또는 소유한 속성에 대한 참조 트래픽을 추적할 수 있습니다.

Livefyre 앱을 사용하면 참조 트래픽으로 인한 데이터 스트림을 추적할 수 있으므로 사이트의 트래픽을 분석할 수 있습니다.

## Livefyre 참조 트래픽 추적 {#section_nsy_qp4_xz}

소셜 네트워크의 Livefyre 참조 트래픽 및 이메일은 페이지의 URL에서 쿼리 문자열 매개 변수를 검사하고 페이지에 코드를 구현하여 분석 공급자를 통해 이것을 추적함으로써 추적할 수 있습니다. 댓글이 소셜 네트워크에 게시되거나 공유될 때, 그리고 Livefyre 이메일에 포함된 링크용 URL에 대한 참조 링크가 추가됩니다.

## 구현 예 {#section_xvs_x44_xz}

트래픽이 StreamHub 기반 알림에서 온 경우 이메일, facebook, twitter, linkedin 또는 permalink 값을 갖는 hubRefSrc 쿼리 문자열 매개 변수가 있습니다. hubRefSrc 매개 변수 이름은 Livefyre 배달 팀이 네트워크 수준에서 구성할 수 있습니다.

분석 플랫폼과 통합하려면 페이지가 로드될 때 hubRefSrc를 검색하고 트래픽이 있을 경우 이를 기록해야 합니다.

예:

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

* [대화](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [평가](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [사이드노트](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

