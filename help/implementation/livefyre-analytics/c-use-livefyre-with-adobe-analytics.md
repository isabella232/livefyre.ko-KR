---
description: 'null'
seo-description: 'null'
seo-title: Adobe Analytics 및 Dynamic Tag Manager(DTM)를 사용하여 Livefyre를 사용하고, Adobe Analytics 및 Dynamic Tag Manager(DTM)를 사용하여 Dtm(다이내믹 태그 관리자)를
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 987482066f1ca3c021a5c9f0fc0109edff616c0a

---


# Adobe Analytics 및 Dynamic Tag Manager(DTM)에서 Livefyre 사용{#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Livefyre 앱에 대한 데이터를 수집하도록 Adobe Analytics 및 DTM 파섹

## 1단계:Adobe Analytics에서 이벤트 설정 {#section_iks_kgd_4cb}

Livefyre 이벤트를 Adobe Analytics 보고서 세트 관리자에서 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

보고서 세트 관리자에 대한 자세한 내용은 보고서 세트 [관리자를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. 관리자 사용자로 Adobe Analytics에 로그인합니다.
1. Adobe Analytics 관리 보고서 세트 관리자를 엽니다.
1. 새 보고서 세트를 만들거나 기존 보고서 세트를 선택합니다.
1. 수정할 보고서 세트를 클릭하여 보고서 세트를 편집한 다음 **[!UICONTROL Edit Settings > Conversion > Success Events]**&#x200B;로 이동합니다.
1. Livefyre 이벤트를 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

## 2단계:전환 변수 설정

Livefyre 전환 변수(eVar)를 Adobe Analytics 관리 보고서 세트 관리자의 전환 변수에 매핑합니다. 전환 변수는 정렬 함수와 같이 작동하여 Livefyre 이벤트에서 수집된 데이터를 식별하는 계획을 결정합니다.

1. 보고서 세트 관리자에서 을 **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**&#x200B;클릭합니다.
1. 사용할 사용자 지정 전환 변수(eVar)를 선택하고 Livefyre 전환 변수에 매핑합니다. Livefyre 전환 변수를 사용자 지정 전환 변수에 매핑하려면:
* 전환 변수 활성화
* 전환 변수 이름 지정
* 전환 변수에 유형 지정
1. 사용자 지정 전환 변수를 저장합니다.

## 3단계:DTM을 사용하여 Livefyre 이벤트와 함께 보고서 세트 추가 {#section_t15_2hd_4cb}

Adobe Analytics를 DTM에 추가하면 Analytics가 작동합니다. 이렇게 하려면 새 속성과 도구를 만들고 Livefyre 이벤트가 있는 새 보고서 세트를 속성에 추가합니다. DTM 파섹 에 대한 자세한 내용은 DTM을 [참조하십시오](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Livefyre 이벤트로 설정한 보고서 세트에 대해 이미 속성 또는 도구를 설정한 경우 이 단계를 수행할 필요가 없습니다.

1. DTM에서 기존 속성을 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구를 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구가 없는 경우 **[!UICONTROL Add a Tool]** 단추를 클릭합니다.
도구에 대해 다음 매개 변수를 설정합니다.

   * Set **[!UICONTROL Tool Type]** to **[!UICONTROL Adobe Analytics]**.
   * Enable **[!UICONTROL Automatic Configuration]**.
   * Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Livefyre 이벤트가 있는 보고서 세트의 이름을 **[!UICONTROL Report Suites]** 필드에 추가하거나 확인합니다.

## 4단계:페이지 로드 규칙을 설정하여 분석 처리 설정 {#section_jfj_j3d_4cb}

모든 데이터를 가져오도록 페이지 로드 규칙을 설정합니다. 페이지 로드 규칙을 사용하면 페이지가 로드될 때 이벤트를 기록하는 규칙에 사용자 지정 javascript를 배치할 수 있습니다.

>[!NOTE]
>
>이벤트 기반 규칙 또는 직접 호출 규칙을 사용하지 마십시오.

1. DTM에서 **[!UICONTROL Rules]** 탭을 선택합니다.
1. 클릭 **[!UICONTROL Page Load Rules]**.
1. 단추를 **[!UICONTROL Create New Rule]** 클릭합니다.
1. 단추를 클릭하여 **[!UICONTROL Conditions]** 섹션을 **[!UICONTROL Plus]** 엽니다.
1. 규칙을 트리거합니다. 규칙을 비동기적으로 지연 또는 구현하려면 유형을 **[!UICONTROL DOM Ready]** 선택하거나 **[!UICONTROL Onload]** 트리거합니다.
1. (선택 사항) 추가 매개 변수를 추가하여 Livefyre 앱을 표시하는 페이지를 제한합니다. 추가 구성 옵션에 대한 자세한 내용은 DTM을 [참조하십시오](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. 아래에서 **[!UICONTROL Javascript/ Third Party Tags]**&#x200B;탭을 클릭한 **[!UICONTROL Non-sequential]** 다음 을 클릭합니다 **[!UICONTROL Add New Script]**.
1. 스크립트 **[!UICONTROL Sequential HTML]** 유형으로 선택합니다.
1. 다음 스크립트를 코드 편집기에 추가하고 을 클릭합니다 **[!UICONTROL Save Code]**.

   다음 스크립트는 Livefyre JavaScript가 로드된 후 `livefyre_analytics` 직접 호출 규칙을 호출합니다. 다음 스크립트 예제에서는 400ms마다 `livefyre.analytics` 해당 페이지가 있는지 확인합니다. 페이지가 로드되면 livefyre.analytics는 추적 정보를 전송합니다.

   ```
   /** 
   * Poll for Livefyre.analytics object to exist since it gets loaded via the 
   * Livefyre.js JavaScript file. Depending on the timing, this could already 
   * exist or need a little time. 
   */ 
   function pollForAnalytics() {  
   if (Livefyre.analytics) { 
     _satellite.track('livefyre_analytics'); 
       return true; 
     } 
     setTimeout(pollForAnalytics, 400); 
   } 
   setTimeout(pollForAnalytics, 400);
   ```

1. 클릭 **[!UICONTROL Save Code]**.
1. 클릭 **[!UICONTROL Save Rule]**.

## 5단계:직접 호출 규칙을 만들어 Livefyre에 대한 Adobe Analytics 매핑 구성을 구성합니다. {#section_gvp_b1g_pdb}

사용자 지정 이벤트, DTM 내의 Adobe Analytics UI 필드 및 데이터 요소를 사용하여 Livefyre와 DTM을 구현하는 다른 방법이 있습니다. 이 문서에서는 사용자 지정 Javascript를 사용하여 동일한 효과를 수행합니다.

1. DTM에서 규칙 **탭을** 선택한 다음 직접 호출 **규칙을 클릭합니다**.
1. Click on the **Create New Rule** button.
1. 새 규칙의 이름을 Livefyre **Analytics로 지정합니다**.
1. **조건** 구성 영역을 확장합니다.
1. 문자열 **필드에** 을 입력합니다 `livefyre_analytics`.
1. Javascript/타사 태그 섹션을 확장하고 새 스크립트 **추가 단추를 클릭합니다** .
1. Livefyre **Analytics** 구성을 [태그 이름] **입력 상자에** 입력합니다.
1. 비순차적 **Javascript를 선택합니다**.
1. 다음 Livefyre 구성 코드를 코드 편집기에 입력하고 [코드 저장] **단추를** 클릭합니다.

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
     } 
     ]
   
     /** 
   ```

   * Livefyre의 모든 분석 이벤트에 대한 분석 처리기를 추가합니다. 각 이벤트에 대해 글로벌 객체의 데이터를 설정한 다음 이벤트를 전달합니다.

   ```
   */ 
   function addAnalyticsHandler() {  
     Livefyre.analytics.addHandler(function (events) { 
       (events || []).forEach(function (data) {  
         console.log('Event handled:', data.type);  
         trackLivefyreEvent(data); 
       }); 
     }); 
   } 
   addAnalyticsHandler();  
   ```

1. 규칙 **저장을 클릭합니다**.

## 6단계:페이지 로드 규칙 변경 승인 {#section_pxc_11t_ycb}

1. 탭으로 **[!UICONTROL Approvals]** 이동합니다.
1. 클릭 **[!UICONTROL Approve]**.
1. 승인을 **[!UICONTROL Yes, approve]** 확인하려면 을 클릭합니다.
1. 이동 **[!UICONTROL Overview > Publish Queue]**.
1. 게시할 규칙을 선택합니다.
1. 클릭 **[!UICONTROL Publish Selected]**.
1. 을 **[!UICONTROL Publish]** 클릭하여 게시할 것임을 확인합니다.

## 스크립트 {#section_xkb_vft_mcb}

다음 샘플 코드는 특정 eVar를 사용 가능한 Livefyre eVar에 매핑합니다. Livefyre 전환 변수( `eVar`) 이름(예: `appId`)은 보고서 세트 관리자에서 설정한 이름(예: `eVar81`)에 매핑됩니다. 이 스크립트의 `eVar` 이름을 사용자 지정 전환 변수로 변경합니다.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

다음 샘플 코드는 보고서 세트 관리자에서 설정한 특정 이벤트를 사용 가능한 Livefyre 이벤트와 매핑합니다. 이 예에서는 `event82` 어떤 유형의 사용자 상호 작용 이벤트(예: 컨텐츠 좋아요 또는 공유)를 구별하지 않고 사용자 상호 작용 이벤트로 설정됩니다. 모든 사용자 상호 작용 정보를 블록에 기록하는 효율적인 방법입니다. DTM Analytics UI의 이벤트를 데이터 요소 참조와 매핑할 수도 있습니다.

```
var eventMap = { 
  FlagCancel: 'event82',  
  FlagClick: 'event82',  
  FlagDisagree: 'event82',  
  FlagOffensive: 'event82',  
  FlagOffTopic: 'event82',  
  FlagSpam: 'event82',  
  Like: 'event82', 
  Load: 'event81',  
  RequestMore: 'event82',  
  ShareButtonClick: 'event82',  
  ShareFacebook: 'event82',  
  ShareOnPostClick: 'event82',  
  ShareTwitter: 'event82',  
  ShareURL: 'event82',  
  SortStream: 'event82',  
  TwitterLikeClick: 'event82', 
  TwitterReplyClick: 'event82',  
  TwitterRetweetClick: 'event82',  
  TwitterUserFollow: 'event82' 
};
```

다음 샘플에서는 이 목록에 이벤트가 없으면 아무 작업도 하지 않는다고 설명합니다. 이 코드 섹션을 수정할 필요가 없습니다.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

다음 코드는 `event82` 기록하는 이벤트 유형을 구별합니다. 전환 변수는 `eVar83` 사용자 상호 작용 유형을 기록하고, 스크립트는 사용자 상호 작용 데이터를 유형별로 구분하도록 `eVar83` 설정합니다. 따라서 `eVar83` 기록된 데이터를 특정 유형의 사용자 상호 작용으로 분류할 수 있습니다.

```
  var vars = ['events'];  
  switch (event) { 
    case 'event82': s.eVar83 = data.type;  
      vars.push('eVar83');  
      break; 
    default: 
  } 
   
  ['generator', 'evars'].forEach(function (type) {  
    var obj = data[type]; 
    for (var d in obj) { 
      if (obj.hasOwnProperty(d) && evarMap[d]) {  
        s[evarMap[d]] = obj[d];  
        vars.push(evarMap[d]); 
      } 
    } 
  }); 
   
  s.linkTrackVars = vars.join(',');  
  s.linkTrackEvents = event;  
  s.events = event; 
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

다음 코드 샘플에서는 발생하는 모든 이벤트를 수신하기 위한 핸들러를 추가합니다. 로드 시 페이지 로드 규칙을 사용하고 이벤트가 존재하기를 기다렸다가 앱의 모든 이벤트에 대한 핸들러를 설정하고 추적합니다. 이 코드를 수정할 필요가 없습니다.

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## 추가 정보

이 페이지에서 설명하는 항목에 대한 자세한 내용은 다음을 참조하십시오.

* [보고서 세트 관리자](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [규칙](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
