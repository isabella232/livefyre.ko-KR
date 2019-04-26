---
description: Livefyre. js를 사용하여 날짜 및 타임스탬프를 사용자 정의할 수 있습니다.
seo-description: Livefyre. js를 사용하여 날짜 및 타임스탬프를 사용자 정의할 수 있습니다.
seo-title: 날짜 및 타임스탬프 사용자 정의
solution: Experience Manager
title: 날짜 및 타임스탬프 사용자 정의
uuid: 632 EA 405-56 B 7-4664-8 D 2 B -0 DD 0 A 7611 BD 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 날짜 및 타임스탬프 사용자 정의{#customize-the-date-and-time-stamp}

Livefyre. js를 사용하여 날짜 및 타임스탬프를 사용자 정의할 수 있습니다.

Livefyre 앱은 아래에 설명된 대로 날짜 형식을 지정하는 datetimeformat 옵션 매개 변수를 제공합니다.

* [용어](#c_date_time_stamp/section_xsk_jn4_xz)
* [서식 지정](#c_date_time_stamp/section_ynx_gn4_xz)
* [심볼 지정](#c_date_time_stamp/section_inq_2n4_xz)

## 용어 {#section_xsk_jn4_xz}

* **절대 타임스탬프는** 정확하고 특정 시간으로 정의됩니다 (예: 2012 년 1 월 1 일 오후 12:00 시).
* **상대적 타임스탬프는** 일반 및 덜 정확한 시간 (예: 25 초 전, 14 분 전, 1 일 전, 1 년 전 등) 로 정의됩니다.

## 서식 지정 {#section_ynx_gn4_xz}

인수가 제공되지 않으면 Datetimeformat 매개 변수에 다음과 같은 기본 비헤이비어가 적용됩니다.

* Datetime 형식: MMMM D YYYY (2012 년 1 월 8 일)
* 절대적 시간 (상대적 타임스탬프가 절대 타임스탬프가 될 때까지 14 일) 까지 20160 분 (14 일)

Datetimeformat 매개 변수는 가능한 세 가지 인수 유형을 수용합니다. datetime, format 및 string.

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

Absoluteformat 및/또는 minutesuntilabeastetime를 지정하는 개체. 값이 -1 인 Minutesuntilabsolutetime는 시간 절대 시간을 즉시 만듭니다.

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

date 객체를 인수로 사용하고 표시할 datetime 문자열을 반환하는 함수

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

## 심볼 지정 {#section_inq_2n4_xz}

JS의 일반적인 사용을 약간 수정하여 JDK, ICU 및 CLDR에 정의된 패턴 사양을 따르는 datetime 서식 지정 함수 자세한 내용은 [Google Closure 라이브러리 설명서를](https://developers.google.com/closure/library/docs/overview)참조하십시오.

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

' *' 로 표시된 항목은 아직 지원되지 않습니다.

' #' 로 표시된 항목은 Java와 다르게 작동합니다.

패턴 글자 수에 따라 형식이 결정됩니다.

* **텍스트:** 4 이상, 전체 양식을 사용하십시오. 4 미만의 경우 간단한 또는 약어 양식을 사용합니다. (예: " EEEE "는" 월요일 "을 생성하며," EEE "는" MON "을 생성합니다.
* **숫자:** 최소 자릿수. 이 금액에 짧은 숫자가 0로 추가됩니다 (예: " m "이" 6 "을 생성하는 경우" MM "은" 06 "을 생성합니다. 년은 특별히 처리됩니다. 즉,' Y'의 개수가 2 이면 연도를 2 자리로 잘립니다. (예: «YYYY» 가 «1997» 를 생성하는 경우 «YY» 는 «97» 를 생성합니다.) 다른 필드와 달리 분수 초는 오른쪽에 0 이 추가됩니다.
* **텍스트 및 번호:** 3 이상, 텍스트를 사용합니다. 3 미만, 숫자를 사용합니다. (예: " M "은" 1 "을," MM "은" 01 "을," MMM "은" Jan "을," MMMM "은" 1 월 "을 생성합니다.

패턴의'a'범위에 속하지 않는 [모든 문자. 'z'] 와 ['a '. 'z'] 는 인용된 텍스트로 처리됩니다. 예를 들면 다음과 같은 문자가 있습니다. ','. ',',' #' 및 ' @' 는 결과 시간 텍스트에 나타나며, 작은 따옴표 내에 받아들여지지 않습니다.
