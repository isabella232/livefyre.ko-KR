---
description: null
seo-description: null
seo-title: Adobe Analytics 및 DTM (Dynamic Tag Manager) 의 Livefyre와 Adobe Analytics
  및 DTM (Dynamic Tag Manager) 이 포함된 DTM (Dynamic Tag Manager) 사용
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Adobe Analytics 및 DTM (Dynamic Tag Manager) 에서 Livefyre 사용{#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Livefyre 앱용 데이터를 수집하도록 Adobe Analytics 및 DTM (Dynamic Tag Manager) 를 설정합니다.

## 1 단계: Adobe Analytics에서 이벤트 설정 {#section_iks_kgd_4cb}

Livefyre 이벤트를 Adobe Analytics 보고서 세트 관리자에서 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

보고서 세트 관리자에 대한 자세한 내용은 [보고서 세트 관리자를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Adobe Analytics에 관리자 사용자로 로그인합니다.
1. Adobe Analytics 관리자 보고서 세트 관리자를 엽니다.
1. 새 보고서 세트를 만들거나 기존 보고서 세트를 선택합니다.
1. 수정할 보고서 세트를 클릭하여 보고서 세트를 편집한 **[!UICONTROL Edit Settings > Conversion > Success Events]**다음 이동합니다.
1. Livefyre 이벤트를 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

## 2 단계: 전환 변수 설정

Livefyre 전환 변수 (evar) 를 Adobe Analytics 관리자 보고서 세트 관리자의 전환 변수에 매핑합니다. 전환 변수는 Livefyre 이벤트에서 수집한 데이터를 식별하는 방법을 결정하는 정렬 함수처럼 작동합니다.

1. **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**를 클릭합니다.
1. 사용할 사용자 지정 전환 변수 (Evar) 를 선택하고 Livefyre 전환 변수에 매핑합니다. Livefyre 전환 변수를 사용자 지정 전환 변수에 매핑하려면:
* 전환 변수 활성화
* 전환 변수 이름 지정
* 전환 변수 a 유형 지정
1. 사용자 지정 전환 변수를 저장합니다.

## 3 단계: DTM를 사용하여 Livefyre 이벤트에 보고서 세트 추가 {#section_t15_2hd_4cb}

Adobe Analytics를 DTM에 추가하여 분석 작업을 수행할 수 있습니다. 이렇게 하려면 새 속성과 도구를 만들고 Livefyre 이벤트에 새 보고서 세트를 추가합니다. DTM에 대한 자세한 내용은 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)를 참조하십시오.

Livefyre 이벤트로 설정한 보고서 세트에 대해 속성 또는 도구 세트가 설정되어 있는 경우 이 단계를 수행할 필요가 없습니다.

1. DTM에서 기존 속성을 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구를 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구가 존재하지 않는 경우 **[!UICONTROL Add a Tool]** 단추를 클릭합니다.
도구에 대해 다음 매개 변수를 설정합니다.
* 으로 설정합니다 **[!UICONTROL Tool Type]****[!UICONTROL Adobe Analytics]**.
* 활성화 **[!UICONTROL Automatic Configuration]**.
* 활성화 **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Livefyre Events로 보고서 세트의 이름을 **[!UICONTROL Report Suites]** 필드에 추가하거나 확인합니다.

## 4 단계: 페이지 로드 규칙을 설정하여 분석 처리 설정 {#section_jfj_j3d_4cb}

모든 데이터를 가져오도록 페이지 로드 규칙을 설정합니다. 페이지 로드 규칙을 사용하면 페이지가 로드될 때 이벤트를 기록하는 규칙에 사용자 지정 Javascript를 배치할 수 있습니다.

>[!NOTE]
>
>이벤트 기반 규칙 또는 직접 호출 규칙을 사용하지 마십시오.

1. DTM에서 **[!UICONTROL Rules]** 탭을 선택합니다.
1. **[!UICONTROL Page Load Rules]**을 클릭합니다.
1. **[!UICONTROL Create New Rule]** 단추를 클릭합니다.
1. 단추를 클릭하여 **[!UICONTROL Conditions]** 섹션을 **[!UICONTROL Plus]** 엽니다.
1. 규칙을 트리거합니다. 규칙을 비동기식으로 지연하거나 구현하려는 경우 유형을 선택하거나 **[!UICONTROL DOM Ready]****[!UICONTROL Onload]** 트리거합니다.
1. (선택 사항) Livefyre 앱을 표시하는 페이지를 제한하는 추가 매개 변수를 추가합니다. 추가 구성 옵션에 대한 자세한 내용은 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)를 참조하십시오.
1. 아래에서 **[!UICONTROL Javascript/ Third Party Tags]****[!UICONTROL Non-sequential]** 탭을 클릭한 다음을 클릭합니다 **[!UICONTROL Add New Script]**.
1. 스크립트 **[!UICONTROL Sequential HTML]** 유형으로 선택합니다.
1. 다음 스크립트를 코드 편집기에 추가하고 **[!UICONTROL Save Code]**를 클릭합니다.
다음 스크립트는 Livefyre JavaScript 로드 후 `livefyre_analytics` 직접 호출 규칙을 호출합니다. 다음 스크립트 예제는 400 ms가 페이지에 `livefyre.analytics` 있는지 확인하기 위해 확인합니다. 페이지가 로드되면 Livefyre. Analytics가 추적 정보를 전송합니다.

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

1. **[!UICONTROL Save Code]**을 클릭합니다.
1. **[!UICONTROL Save Rule]**을 클릭합니다.

## 5 단계: 직접 호출 규칙을 만들어 Livefyre에 대한 Adobe Analytics 매핑 구성 만들기 {#section_gvp_b1g_pdb}

사용자 지정 이벤트, DTM 내 Adobe Analytics UI 필드 및 데이터 요소를 사용하여 DTM를 사용하여 Livefyre를 구현하는 다른 방법이 있습니다. 이 문서에서는 사용자 지정 Javascript를 사용하여 동일한 효과를 냅니다.

1. DTM에서 **규칙** 탭을 선택한 다음 직접 호출 **규칙을 클릭합니다**.
1. 새 규칙 **만들기** 버튼을 클릭합니다.
1. 새 규칙 **Livefyre 분석 이름을 지정합니다**.
1. **조건** 구성 영역을 확장합니다.
1. **문자열** 필드에서를 입력합니다 `livefyre_analytics`.
1. Javascript/타사 태그 섹션을 확장하고 새 스크립트 **추가** 버튼을 클릭합니다.
1. **Livefyre 분석 구성을** **태그 이름** 입력 상자에 입력합니다.
1. 비순차적 **Javascript**를 선택합니다.
1. Livefyre 구성 코드를 코드 편집기에 입력하고 코드 **저장** 버튼을 클릭합니다.

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

* Livefyre의 모든 분석 이벤트에 대한 Analytics 처리기를 추가합니다. 각 이벤트에 대해 전역 개체에 대한 데이터를 설정한 다음 이벤트를 전달합니다.

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s =_ satellite. gettoolsbytype`('sc')[0]`. gets ();
var evarmap = {appid: ' Evar 81 ',
apptype: ' Evar 82 '};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {flagcancel: ' event 82 ',\
플래그 클릭: ' event 82 ',\
플래그 반대: ' event 82 ',\
Flagoffensive: ' event 82 ',\
Flagofftopic: ' event 82 ',\
플래그 스팸: ' event 82 ',\
좋아요: ' event 82 ',
load: ' event 81 ',\
요청자세한 내용: ' event 82 ',\
Sharebuttonclick: ' event 82 ',\
Sharefacebook: ' event 82 ',\
Shareonpostclick: ' event 82 ',\
Sharetwitter: ' event 82 ',\
Shareurl: ' event 82 ',\
Sortstream: ' event 82 ',\
Twitterlikeclick: ' event 82 ',
twitterreplyclick: ' event 82 ',\
Twitterretweetclick: ' event 82 ',\
Twitteruserfollow: ' event 82 '};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log (' track: ', data. type, event);

if (! event) {console.
warn (data. type,' is not mapped to an event in AA ');\
return;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = [' events '];\
switch (event) {case'event
82 ': s. evar 83 = data. type;\
var. push (' evar 83 ');\
break;
기본값:}

[' generator ',' evars ']. foreach (function (type) {\
var obj = datatype[];
for (obj d in obj) {if
(obj. hasownproperty (d) & & evarmapd[]) {\
s [evarmapd[]] = OBJD[];\
var. push (evarmapd[]);}}});

s. linktrackvars = vars. join (',');\
s. linktrackevents = event;\
s. events = event;

console. log (' linktrackvars: ', s. linktrackvars);\
console. log (' linktrackevents: ', s. linktrackevents);\
console. log (' events: ', s. events);

s. tl ();}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Livefyre의 모든 분석 이벤트에 대한 Analytics 처리기를 추가합니다. 각 이벤트에 대해 전역 개체에 대한 데이터를 설정한 다음 이벤트를 전달합니다.

*/function
addanalyticshandler () {livefyre.
analytics. addhandler (function (events) {(events || []). foreach (function (data) {console.
log (' event handled: ', data. type);
Tracklivefyreevent (data);});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

