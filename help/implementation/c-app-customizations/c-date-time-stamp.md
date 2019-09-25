---
description: Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.
seo-description: Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.
seo-title: 날짜 및 타임스탬프 사용자 정의
solution: Experience Manager
title: 날짜 및 타임스탬프 사용자 정의
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 날짜 및 타임스탬프 사용자 정의{#customize-the-date-and-time-stamp}

Livefyre.js를 사용하여 날짜 및 타임스탬프를 사용자 정의합니다.

Livefyre Apps는 아래 설명된 대로 날짜 형식을 지정할 수 있는 옵션 매개 변수 datetimeFormat을 제공합니다.

* [용어](#c_date_time_stamp/section_xsk_jn4_xz)
* [서식 지정](#c_date_time_stamp/section_ynx_gn4_xz)
* [기호 지정](#c_date_time_stamp/section_inq_2n4_xz)

## 용어 {#section_xsk_jn4_xz}

* **절대 타임스탬프는** 정확하고 특정 시간(예: 2012년 1월 1일 12:00pm)으로 정의됩니다.
* **상대 타임스탬프는** 일반적이고 덜 정밀한 시간(예: 25초 전, 14분 전, 1일 전, 1년 전 등)으로 정의됩니다.

## 서식 지정 {#section_ynx_gn4_xz}

datetimeFormat 매개 변수는 인수를 지정하지 않을 때 다음과 같은 기본 동작을 가집니다.

* 날짜/시간 형식:MMMM d yyyy(2012년 1월 8일)
* 상대 타임스탬프가 절대 타임스탬프가 될 때까지 20160분(14일)

datetimeFormat 매개 변수는 세 가지 가능한 인수 유형을 허용합니다.datetime, format 및 string.

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

absoluteFormat 및/또는 minutesUntilAbsoluteTime을 지정하는 개체입니다. 값이 -1인 minutesUntilAbsoluteTime은 시간을 절대 시간으로 즉시 만듭니다.

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

Date 객체로 가져와서 표시할 datetime 문자열을 반환하는 함수입니다.

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

JDK, ICU 및 CLDR에 정의된 패턴 사양에 따른 datetime 서식 함수를 사용하고, JS에서 일반적인 사용을 약간 수정할 수 있습니다. 자세한 내용은 Google Closure [라이브러리 설명서를 참조하십시오](https://developers.google.com/closure/library/docs/overview).

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

'*'로 표시된 항목은 아직 지원되지 않습니다.

'#'로 표시된 항목은 Java와 다르게 작동합니다.

패턴 글자의 개수는 형식을 결정합니다.

* **** 텍스트:4 이상, 전체 양식을 사용하십시오. 4개 미만이면 짧은 양식이나 약어를 사용합니다. (예:"EEE"는 "월요일", "EEE"는 "월"을 생성합니다.)
* **** 번호:최소 자릿수입니다. 이 양만큼 짧은 숫자는 0으로 채워집니다(예:"m"이 "6"을 생성하는 경우 "mm"은 "06"을 생성합니다.) 특히 올해.즉, 'y'의 개수가 2이면 연도는 2자리로 잘립니다. (예:"yyyy"가 "1997"을 생성하는 경우 "yy"는 "97"을 생성합니다.) 다른 필드와 달리, 분수 초는 0으로 오른쪽에 채워져 있습니다.
* **** 텍스트 및 번호:3 이상 텍스트를 사용하십시오. 3개 미만, 사용 번호 (예:"M"은 "1", "MM"은 "01"을, "MMM"은 "Jan"을, "MMMM"은 "Jan"을 생성합니다.)

'a'의 범위에 속하지 않는 패턴의 [모든 문자..'z'] and ['A'.'Z는] 인용 텍스트로 처리됩니다. 예를 들어 ':', '.', ', '#' 및 '@'와 같은 문자는 단일 인용 부호 내에 적용되지 않더라도 결과 시간 텍스트에 표시됩니다.
