---
description: 'null'
seo-description: 'null'
seo-title: 다른 분석 도구에서 Livefyre 사용
solution: Experience Manager
title: 다른 분석 도구에서 Livefyre 사용
uuid: 26c835f6-aced-41f7-aabe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# 다른 분석 도구에서 Livefyre 사용{#use-livefyre-with-other-analytics-tool}

분석 도구를 사용하여 Livefyre 앱과의 사용자 상호 작용에 대한 데이터를 수집할 수 있습니다. Adobe Analytics 또는 원하는 툴을 사용할 수 있습니다.

Adobe Analytics이 아닌 원하는 도구를 사용하여 Livefyre를 사용하려면 이 페이지에 설명된 절차를 따르십시오.

## 1단계:이벤트 핸들러 {#section_ngm_gzl_pdb} 설정

Livefyre 앱을 사용하는 페이지에 이벤트 핸들러를 설정합니다. 분석에 사용할 수 있는 해당 페이지의 앱의 데이터를 수집할 수 있습니다.

Livefyre.js를 페이지에 추가하여 이벤트 핸들러를 설정합니다. Livefyre.js는 비동기적으로 로드됩니다. 파일 크기를 줄이고 로드 성능을 개선하기 위해 분석을 즉시 사용할 수 없습니다. 데이터를 사용할 수 있을 때까지 분석 개체를 폴링해야 합니다. 이 스크립트를 페이지의 아무 곳이나 배치하거나 자체 컴파일된 스크립트 내에 번들로 제공할 수 있습니다.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## 2단계:처리기 함수 구현

페이지에서 Livefyre.analytics 기능을 사용할 수 있게 되면 analyticsHandler 함수를 구현하여 수신된 이벤트를 원하는 분석 공급자에게 보냅니다.

1. analytics 핸들러는 공급자가 지원하는 경우 개별적으로 또는 일괄적으로 반복해야 하는 일련의 이벤트를 받습니다.
1. 핸들러가 받은 이벤트 데이터를 분석 공급자가 요구하는 형식으로 매핑합니다.
1. 데이터를 분석 공급자에게 보냅니다.

