---
description: null
seo-description: null
seo-title: 다른 Analytics 도구와의 Livefyre 사용
solution: Experience Manager
title: 다른 Analytics 도구와의 Livefyre 사용
uuid: 26 C 835 F 6-Aced -41 F 7-AABE -418 AFCE 8 A 829
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 다른 Analytics 도구와의 Livefyre 사용{#use-livefyre-with-other-analytics-tool}

분석 도구를 사용하여 Livefyre 앱과의 사용자 상호 작용에 대한 데이터를 수집할 수 있습니다. Adobe Analytics 또는 원하는 도구를 사용할 수 있습니다.

Adobe Analytics가 아닌 원하는 툴에서 Livefyre를 사용하려면 이 페이지에 설명된 절차를 따르십시오.

## 1 단계: 이벤트 핸들러 설정 {#section_ngm_gzl_pdb}

Livefyre 앱을 사용하는 페이지에서 이벤트 핸들러를 설정합니다. 이렇게 하면 Analytics에 사용할 수 있는 해당 페이지의 앱에서 데이터를 수집할 수 있습니다.

livefyre. js를 페이지에 추가하여 이벤트 핸들러를 설정합니다. Livefyre. js는 비동기식으로 로드됩니다. 파일 크기를 줄이고 로드 성능을 향상시키기 위해 즉시 분석을 사용할 수 없습니다. 데이터가 제공될 때까지 Analytics 개체를 반드시 폴링해야 합니다. 페이지에 이 스크립트를 배치하거나 자신의 컴파일된 스크립트 내에 번들로 사용할 수 있습니다.

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

## 2 단계: 핸들러 함수 구현

Livefyre. analytics 기능을 페이지에서 사용할 수 있게 되면, analyticshandler 함수를 구현하여 수신된 이벤트를 원하는 분석 제공업체에 전송합니다.

1. Analytics 핸들러는 개별적으로 반복해서 전송되어야 하고 개별적으로 전송되어야 하는 이벤트 배열을 수신합니다 (공급자가 이를 지원하는 경우).
1. 처리기에 의해 수신된 이벤트 데이터를 Analytics 공급자가 요구하는 형식으로 매핑합니다.
1. 데이터를 Analytics 공급자에게 보냅니다.

