---
description: Livefyre 앱에 대한 데이터를 수집하도록 Adobe Analytics 및 DTM(Dynamic Tag Manager)을 설정합니다.
title: Livefyre와 Adobe Analytics 및 Dynamic Tag Manager(DTM) 사용
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
source-git-commit: 53aead87db517e6f68266a66115889509287a287
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 1%

---

# Livefyre와 Adobe Analytics 및 Dynamic Tag Manager(DTM) 사용{#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Livefyre 앱에 대한 데이터를 수집하도록 Adobe Analytics 및 DTM(Dynamic Tag Manager)을 설정합니다.

## 1단계: Adobe Analytics에서 이벤트 설정 {#section_iks_kgd_4cb}

Livefyre 이벤트를 Adobe Analytics 보고서 세트 관리자의 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

보고서 세트 관리자에 대한 자세한 내용은 [보고서 세트 관리자](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)를 참조하십시오.

1. 관리자 사용자로 Adobe Analytics에 로그인합니다.
1. Adobe Analytics 관리 보고서 세트 관리자를 엽니다.
1. 새 보고서 세트를 만들거나 기존 보고서 세트를 선택합니다.
1. 수정할 보고서 세트를 클릭하여 보고서 세트를 편집한 다음 **[!UICONTROL Edit Settings > Conversion > Success Events]** 로 이동합니다.
1. Livefyre 이벤트를 하나 이상의 사용자 지정 성공 이벤트에 매핑합니다.

## 2단계: 전환 변수 설정

Livefyre 전환 변수(eVar)를 Adobe Analytics 관리자 보고서 세트 관리자의 전환 변수에 매핑합니다. 전환 변수는 Livefyre 이벤트에서 수집된 데이터를 식별하는 방법을 결정하는 정렬 함수 역할을 합니다.

1. 보고서 세트 관리자에서 **[!UICONTROL Edit Settings > Conversion > Conversion Variables]** 을 클릭합니다.
1. 사용할 사용자 지정 전환 변수(eVar)를 선택하고 Livefyre 전환 변수에 매핑합니다. Livefyre 전환 변수를 사용자 지정 전환 변수에 매핑하려면:
* 전환 변수 활성화
* 전환 변수에 이름을 지정합니다
* 전환 변수에 유형을 지정합니다
1. 사용자 지정 전환 변수를 저장합니다.

## 3단계: DTM을 사용하여 Livefyre 이벤트와 함께 보고서 세트 추가 {#section_t15_2hd_4cb}

Analytics를 작동하도록 DTM에 Adobe Analytics을 추가합니다. 이렇게 하려면 새 속성 및 도구를 만들고 Livefyre 이벤트가 있는 새 보고서 세트를 속성에 추가합니다. DTM에 대한 자세한 내용은 [DTM](https://experienceleague.adobe.com/docs/dtm/using/c-overview.html?lang=en)을 참조하십시오.

Livefyre 이벤트로 설정한 보고서 세트에 대해 이미 속성 또는 도구를 설정한 경우 이 단계를 수행할 필요가 없습니다.

1. DTM에서 기존 속성을 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구를 만들거나 편집합니다.
1. 기존 Adobe Analytics 도구가 없는 경우 **[!UICONTROL Add a Tool]** 버튼을 클릭합니다.
도구에 대해 다음 매개 변수를 설정합니다.

   * **[!UICONTROL Tool Type]** 을 **[!UICONTROL Adobe Analytics]**(으)로 설정합니다.
   * 활성화 **[!UICONTROL Automatic Configuration]**.
   * 활성화 **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Livefyre 이벤트가 있는 보고서 세트의 이름을 **[!UICONTROL Report Suites]** 필드에 추가하거나 확인합니다.

## 4단계: Analytics 처리를 설정할 페이지 로드 규칙 설정 {#section_jfj_j3d_4cb}

모든 데이터를 가져올 페이지 로드 규칙 을 설정합니다. 페이지 로드 규칙을 사용하면 페이지가 로드될 때 이벤트를 기록하는 규칙에 사용자 지정 Javascript를 배치할 수 있습니다.

>[!NOTE]
>
>이벤트 기반 규칙 또는 직접 호출 규칙을 사용하지 마십시오.

1. DTM에서 **[!UICONTROL Rules]** 탭을 선택합니다.
1. 클릭 **[!UICONTROL Page Load Rules]**.
1. **[!UICONTROL Create New Rule]** 단추를 클릭합니다.
1. **[!UICONTROL Plus]** 단추를 클릭하여 **[!UICONTROL Conditions]** 섹션을 엽니다.
1. 규칙을 트리거합니다. 규칙을 비동기식으로 지연 또는 구현하려면 **[!UICONTROL DOM Ready]** 또는 **[!UICONTROL Onload]** 트리거 유형을 선택합니다.
1. (선택 사항) 추가 매개 변수를 추가하여 Livefyre 앱을 표시하는 페이지를 제한합니다. 추가 구성 옵션에 대한 자세한 내용은 [DTM](https://experienceleague.adobe.com/docs/dtm/using/c-overview.html?lang=en)을 참조하십시오.
1. **[!UICONTROL Javascript/ Third Party Tags]**&#x200B;에서 **[!UICONTROL Non-sequential]** 탭을 클릭한 다음 **[!UICONTROL Add New Script]**&#x200B;를 클릭합니다.
1. 스크립트 유형으로 **[!UICONTROL Sequential HTML]** 을 선택합니다.
1. 코드 편집기에 다음 스크립트를 추가하고 **[!UICONTROL Save Code]** 을 클릭합니다.

   다음 스크립트는 Livefyre JavaScript가 로드된 후 `livefyre_analytics` 직접 호출 규칙을 호출합니다. 다음 스크립트 예제에서는 400ms마다 `livefyre.analytics`이 페이지에 있는지 확인합니다. 페이지가 로드되면 livefyre.analytics에서 추적 정보를 보냅니다.

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

## 5단계: Livefyre에 대한 Adobe Analytics 매핑 구성을 구성하기 위한 직접 호출 규칙 만들기 {#section_gvp_b1g_pdb}

사용자 지정 이벤트, DTM 내의 Adobe Analytics UI 필드 및 데이터 요소를 사용하여 DTM으로 Livefyre를 구현하는 다른 방법이 있습니다. 이 문서는 사용자 지정 Javascript를 사용하여 동일한 효과를 수행합니다.

1. DTM에서 **규칙** 탭을 선택한 다음 **직접 호출 규칙**&#x200B;을 클릭합니다.
1. **새 규칙 만들기** 단추를 클릭합니다.
1. 새 규칙 이름을 **Livefyre Analytics**&#x200B;로 지정합니다.
1. **conditions** 구성 영역을 확장합니다.
1. **문자열** 필드에 `livefyre_analytics`를 입력합니다.
1. Javascript/타사 태그 섹션을 확장하고 **새 스크립트 추가** 단추를 클릭합니다.
1. **태그 이름** 입력 상자에 **Livefyre Analytics 구성**&#x200B;을 입력합니다.
1. **비순차적 Javascript**&#x200B;를 선택합니다.
1. 다음 Livefyre 구성 코드를 코드 편집기에 입력하고 **Save Code** 단추를 클릭합니다.

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

   * Livefyre의 모든 분석 이벤트에 대한 분석 핸들러를 추가합니다. 각 이벤트에 대해 글로벌 개체에 대한 데이터를 설정한 다음 이벤트를 전달합니다.

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

1. **규칙 저장**&#x200B;을 클릭합니다.

## 6단계: 페이지 로드 규칙에 대한 변경 승인 {#section_pxc_11t_ycb}

1. **[!UICONTROL Approvals]** 탭으로 이동합니다.
1. 클릭 **[!UICONTROL Approve]**.
1. **[!UICONTROL Yes, approve]** 을 클릭하여 승인을 확인합니다.
1. 이동 **[!UICONTROL Overview > Publish Queue]**.
1. 게시할 규칙을 선택합니다.
1. 클릭 **[!UICONTROL Publish Selected]**.
1. **[!UICONTROL Publish]** 을 클릭하여 게시할지 확인합니다.

## 스크립트 {#section_xkb_vft_mcb}

다음 샘플 코드는 특정 eVar를 사용 가능한 Livefyre eVar에 매핑합니다. Livefyre 전환 변수( `eVar`) 이름(예: `appId`)은 보고서 세트 관리자에서 설정한 이름(예: `eVar81`)에 매핑됩니다. 이 스크립트의 `eVar` 이름을 사용자 지정 전환 변수로 변경합니다.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {
  appId: 'eVar81',
  appType: 'eVar82'
};
```

다음 샘플 코드는 보고서 세트 관리자에서 설정한 특정 이벤트를 사용 가능한 Livefyre 이벤트와 매핑합니다. 이 예에서 `event82`은 컨텐츠를 좋아하거나 공유하는 등의 사용자 상호 작용 이벤트 유형을 구별하지 않고 임의의 사용자 상호 작용 이벤트로 설정됩니다. 이는 모든 사용자 상호 작용 정보를 블록에 기록하는 효율적인 방법입니다. DTM Analytics UI의 이벤트를 데이터 요소를 참조하여 매핑할 수도 있습니다.

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

다음 샘플에서는 이 목록에 이벤트가 없으면 아무 작업도 수행하지 마십시오. 이 코드 섹션을 수정할 필요가 없습니다.

```
function trackLivefyreEvent(data) {
  var event = eventMap[data.type];
  console.log('Track:', data.type, event);

  if (!event) {
    console.warn(data.type, 'is not mapped to an event in AA');
    return;
  }
```

다음 코드는 `event82` 이 기록하는 이벤트 유형을 구별합니다. 전환 변수 `eVar83`은 사용자 상호 작용 유형을 기록하고 스크립트는 `eVar83`을 설정하여 사용자 상호 작용 데이터를 유형별로 구분합니다. 따라서 `eVar83` 에서는 기록된 데이터를 특정 유형의 사용자 상호 작용으로 분류할 수 있습니다.

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

다음 코드 샘플은 발생하는 모든 이벤트를 수신하기 위해 처리기를 추가합니다. 로드 시 페이지 로드 규칙을 사용하고, 이벤트가 존재할 때까지 기다렸다가 앱의 모든 이벤트에 대한 처리기를 설정하고 추적합니다. 이 코드를 수정할 필요가 없습니다.

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

이 페이지에서 설명한 주제에 대한 자세한 내용은 다음을 참조하십시오.

* [보고서 세트 관리자](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [DTM](https://experienceleague.adobe.com/docs/dtm/using/c-overview.html?lang=en)
* [규칙](https://experienceleague.adobe.com/docs/dtm/using/resources/rules/create-rules.html?lang=en)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
