---
description: Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.
seo-description: Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.
seo-title: 날짜 및 타임스탬프 사용자 지정
solution: Experience Manager
title: 날짜 및 타임스탬프 사용자 지정
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# 날짜 및 타임스탬프 사용자 지정{#customize-the-date-and-time-stamp}

Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.

Livefyre 앱은 옵션 매개 변수 datetimeFormat을 제공하여 아래 설명된 대로 날짜 형식을 지정합니다.

* [용어](#c_date_time_stamp/section_xsk_jn4_xz)
* [서식 지정](#c_date_time_stamp/section_ynx_gn4_xz)
* [심볼 지정](#c_date_time_stamp/section_inq_2n4_xz)

## 용어 {#section_xsk_jn4_xz}

* **절대** 시간 목록은 정확성과 특정 시간으로 정의됩니다(예: 2012년 1월 1일 12:00pm).
* **상대** 시간 목록은 일반적이고 덜 정밀한 시간(예: 25초 전, 14분 전, 1일 전, 1년 전 등)으로 정의됩니다.

## {#section_ynx_gn4_xz} 서식 지정

인수를 지정하지 않을 경우 datetimeFormat 매개 변수에는 다음과 같은 기본 비헤이비어가 있습니다.

* 날짜/시간 형식:MMMM d yyyy(2012년 1월 8일)
* 절대 시간(상대적 타임스탬프가 절대 타임스탬프가 될 때까지 14일)까지 20160분(14일)

datetimeFormat 매개 변수에는 다음 세 가지 인수 형식을 사용할 수 있습니다.datetime, format 및 string.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

absoluteFormat 및/또는 minutesUntilAbsoluteTime을 지정하는 객체입니다. 값이 -1인 minutesUntilAbsoluteTime을 사용하면 시간 절대 시간이 즉시 시작됩니다.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Date 객체로 가져와서 표시할 datetime 문자열을 반환하는 함수입니다

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## 기호 지정 {#section_inq_2n4_xz}

JDK, ICU 및 CLDR에 정의된 패턴 사양에 따라 datetime 형식 지정 함수와 JS에서 일반적인 사용을 약간 수정할 수 있습니다. 자세한 내용은 [Google Closure 라이브러리 문서](https://developers.google.com/closure/library/docs/overview)를 참조하십시오.

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

&#39;*&#39;로 표시된 항목은 아직 지원되지 않습니다.

&#39;#&#39;로 표시된 항목은 Java와 다르게 작동합니다.

패턴 글자의 개수는 형식을 결정합니다.

* **텍스트:** 4 이상, 전체 양식 사용 4개 미만이면 짧고 간략화된 형식을 사용하십시오. (예:&quot;EEE&quot;는 &quot;월요일&quot;을, &quot;EEE&quot;는 &quot;월&quot;을 생성합니다.)
* **숫자:** 최소 숫자 수입니다. 이 양만큼 짧은 숫자는 0으로 채워집니다(예:&quot;m&quot;이 &quot;6&quot;을 만드는 경우 &quot;mm&quot;은 &quot;06&quot;을 만듭니다.) 특히 일 년.즉, &#39;y&#39;의 개수가 2이면 연도는 2자리로 잘립니다. (예:&quot;yyyy&quot;가 &quot;1997&quot;을 만들면 &quot;yy&quot;가 &quot;97&quot;을 만듭니다.) 다른 필드와 달리, 분수 초는 0으로 오른쪽에 채워집니다.
* **텍스트 및 번호:** 3 이상 텍스트를 사용합니다. 3개 미만이면 번호를 사용하십시오. (예:&quot;M&quot;은 &quot;1&quot;을, &quot;MM&quot;은 &quot;01&quot;을, &quot;MMM&quot;은 &quot;Jan&quot;을, &quot;MMMM&quot;은 &quot;1월&quot;을 생산합니다.)

[&#39;a&#39; 범위에 없는 패턴의 모든 문자..&#39;z&#39;] 및 [&#39;A&#39;.&#39;Z&#39;]은(는) 인용된 텍스트로 처리됩니다. 예를 들어, &#39;:&#39;, &#39;.&#39;, &#39;, &#39;#&#39; 및 &#39;@&#39;와 같은 문자는 단일 따옴표 안에 포함되지 않더라도 결과 시간 텍스트에 나타납니다.
