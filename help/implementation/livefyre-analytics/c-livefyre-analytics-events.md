---
description: null
seo-description: null
seo-title: Livefyre 분석 이벤트
solution: Experience Manager
title: Livefyre 분석 이벤트
uuid: 4 EB 5 A 196-CA 33-40 F 8-A 96 D-ED 46469223 DE
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre 분석 이벤트 {#livefyre-analytics-events}

## 이벤트 개체 정의 {#section_dh1_yhn_pdb}

다음 코드는 페이지의 Analytics 핸들러에 의해 수신되는 이벤트 객체의 필드를 정의합니다.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Livefyre 분석 이벤트 및 evar {#section_u3k_tft_mcb}

보고서 세트 관리자를 사용하는 보고서에 사용하기 위해 사용자 지정 이벤트에 매핑할 Livefyre 이벤트입니다. Adobe Analytics의 보고서 세트에 대한 자세한 내용은 [보고서 세트 관리자를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). 보고서 세트 관리자에서 Livefyre 이벤트를 사용하는 방법에 대한 자세한 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)내용은을 참조하십시오.

## Livefyre 분석 이벤트

| 이벤트 | 설명 |
|---|---|
| init | 하나 이상의 Livefyre 앱이 포함된 페이지가 로드되는 경우 |
| load | 사용자가 사용자 보기에 관계없이 페이지에 로드된 시간 |
| view | 앱이 처음으로 뷰포트에 진입한 경우. |
| POST | 사용자가 댓글을 게시하거나 EX: 최상위 게시물, 답글, 검토, 미디어 담벼락 업로드 |
| 게시됨 | 게시물이 성공한 경우 |
| twitter_ reply | 사용자가 Twitter에서 답변한 시간 |
| Twitter_ like | 콘텐트가 공유한 위치: 리트윗 |
| livefyre_ like | Livefyre like feature is used in an app |
| livefyre_ unlike | 사용자가 좋아요를 좋아요를 좋아하지 않는 경우 |
| Shareonpost | 사용자가 컨텐츠를 게시하고 게시 시 공유 기능을 사용하는 시점 |
| Sharebuttonclick | 사용자가 댓글의 공유 단추를 클릭할 때마다 |
| Sharetwitter | Twitter로 공유하는 경우 |
| sharefacebook | Facebook에 공유를 클릭하면 |
| shareurl | URL 텍스트 영역에 공유/복사되는 경우 |
| Expandreplies | 사용자가 + 또는 확장 링크를 클릭하여 최상위 수준의 게시물을 모두 보는 경우 |
| collapsereplies | 사용자가 - 링크를 클릭하거나 축소하여 최상위 수준의 게시물을 모두 보는 경우 |
| 플래그 클릭 | 사용자가 플래그를 모달 모드로 열 때마다 |
| Flagspam | 사용자가 컨텐츠를 스팸으로 플래그로 지정하면 |
| 플래그 없음 | 사용자가 컨텐츠를 동의하지 않음으로 플래그 지정하는 경우 |
| Flagoffensive | 사용자가 콘텐츠를 불쾌하게 플래그를 지정할 때 |
| Flagofftopic | 사용자가 컨텐츠를 꺼짐으로 플래그로 지정하면 |
| Flagcancel | 사용자가 플래그를 제출할 때 X 또는 "취소" 를 클릭할 때마다 |
| Followcollection | 언제든지 대화를 팔로우할 수 있습니다 ("I's Interest"). |
| Unfollowcollection | 대화가 뒤따르는 경우 |
| 요청자세한 내용 | 사용자가 앱에서 더 많은 콘텐츠를 로드할 때마다 (빠른 속도도 필요) |
| Modalview | 사용자가 클릭하여 목차에서 컨텐츠를 볼 때마다 |
| Twitterretweetclick | 콘텐트가 공유한 위치: 리트윗 |
| Postbuttonclick | 사용자가 게시물을 클릭하면 ("마음에 드세요? ") 단추 |
| login | 사용자가 로그인할 때마다 |
| 로그아웃 | 사용자가 로그아웃한 시간 |

다음은 Livefyre가 제공하는 전환 변수 (evar) 의 목록입니다.

## 전환 변수 - Evar

| 이벤트 | 설명 |
|--- |--- |
| 네트워크 ID | Livefyre의 네트워크 ID/이름 |
| 앱 ID | 앱의 URN |
| 컨텍스트 ID | Livefyre의 콘텐츠 ID |
| 앱 유형 | Livefyre 앱 유형. 옵션: <br><ul><li>라이브 블로그  </li><li> Feature Card</li><li>회전판</li><li>채팅 </li><li>댓글</li><li>필름스트립</li><li>map</li><li>모자이크</li><li>미디어 담벼락</li><li>트렌딩</li><li>업로드 단추</li></ul> |
| 컨텐츠 유형 | Instagram, Twitter, Facebook, Livefyre, YouTube 등 |

## 추가 정보 {#section_b3d_4yl_pdb}

이 페이지에서 설명하는 항목에 대한 자세한 내용은 다음을 참조하십시오.

* [보고서 세트 Managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [규칙](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [livefyre. js](/help/implementation/c-livefyre.js.md)