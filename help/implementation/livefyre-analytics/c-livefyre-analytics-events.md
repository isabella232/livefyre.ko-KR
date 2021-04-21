---
title: Livefyre 분석 이벤트
description: Livefyre 분석 이벤트
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre 분석 이벤트

## 이벤트 개체 정의 {#section_dh1_yhn_pdb}

다음 코드는 페이지의 분석 핸들러가 수신한 이벤트 객체의 필드를 정의합니다.

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

## Livefyre 분석 이벤트 및 eVar {#section_u3k_tft_mcb}

보고서 세트 관리자를 사용하는 보고서에서 사용할 사용자 지정 이벤트에 매핑하는 다음 Livefyre 이벤트입니다. Adobe Analytics의 보고서 세트에 대한 자세한 내용은 [보고서 세트 관리자](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)를 참조하십시오. 보고서 세트 관리자에서 Livefyre 이벤트를 사용하는 방법에 대한 자세한 내용은 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)을(를) 참조하십시오.

## Livefyre 분석 이벤트

| 이벤트 | 설명 |
|---|---|
| 초기화 | 하나 이상의 Livefyre 앱이 포함된 페이지를 로드할 때 |
| 로드 | 사용자 보기에 상관없이 앱에서 페이지를 로드할 때마다 |
| 보기 | 앱이 뷰포트에 처음 입력했을 때. |
| 게시물 | 사용자가 언제든지 ex를 비롯한 댓글 또는 컨텐츠 일부를 게시할 수 있습니다.최상위 게시물, 답글, 검토, 미디어 담벼락 업로드 |
| 게시됨 | 게시물이 성공했을 때 |
| Twitter_회신 | 사용자가 Twitter에 응답할 때마다 |
| Twitter_좋아요 | 컨텐츠가 공유된 위치:리트윗 |
| Livefyre_Like | livefyre와 유사한 기능이 앱에서 언제든지 사용 |
| Livefyre_Unlike | 사용자가 언제든지 |
| ShareOnPost | 사용자가 컨텐츠를 게시하고 게시물에서 공유 기능을 사용할 때마다 |
| ShareButtonClick | 사용자가 언제든지 댓글에 있는 공유 버튼을 클릭하면 |
| ShareTwitter | twitter에 공유를 클릭할 때 |
| ShareFacebook | facebook에 공유를 클릭할 때 |
| ShareURL | URL에 공유 텍스트 영역이 선택/복사되면 |
| 답글 확장 | 사용자가 + 또는 확장 링크를 클릭하여 최상위 게시물의 모든 답글을 볼 때 |
| 답글 축소 | 사용자가 - 또는 축소 링크를 클릭하여 최상위 게시물의 모든 답글을 볼 때 |
| FlagClick | 사용자가 언제든지 플래그 양식 |
| FlagSpam | 사용자가 컨텐트에 스팸으로 플래그를 지정하는 경우 |
| 플래그 반대 | 사용자가 내용에 동의하지 않는다고 플래그를 지정하는 경우 |
| FlagOffensive | 사용자가 컨텐츠를 불쾌하게 플래그를 지정할 때 |
| FlagOffTopic | 사용자가 컨텐츠를 다른 항목으로 플래그를 지정하는 경우 |
| 플래그 취소 | 플래그를 제출할 때 언제든지 X를 클릭하거나 &quot;취소&quot;를 클릭할 수 있습니다. |
| FollowCollection | 언제든지 대화 후(&quot;관심 있음&quot; 검토) |
| UnfollowCollection | 대화가 미행 상태일 때 |
| 요청 자세히 | 사용자가 앱에 더 많은 콘텐츠를 로드할 때마다(빠른 속도를 위해 필요) |
| ModalView | 사용자가 모달에서 컨텐츠를 보기 위해 클릭하면 언제든지 |
| TwitterRetweetClick | 컨텐츠가 공유된 위치:리트윗 |
| PostButtonClick | 사용자가 게시물을 클릭하면(&quot;무슨 생각을 하십니까?&quot;) 버튼 |
| 로그인 | 사용자가 로그인한 시간 |
| 로그아웃 | 사용자가 로그아웃할 때마다 |

다음은 Livefyre가 제공하는 전환 변수(eVar) 목록입니다.

## 전환 변수 - eVar

| 이벤트 | 설명 |
|--- |--- |
| 네트워크 ID | Livefyre의 네트워크 ID/이름 |
| 앱 ID | 앱의 URN |
| 컨텍스트 ID | Livefyre의 콘텐츠 ID |
| 앱 유형 | Livefyre 앱 유형을 참조하십시오. 옵션: <br><ul><li>라이브 블로그  </li><li> 기능 카드</li><li>회전판</li><li>대화 </li><li>설명</li><li>필름스트립</li><li>맵</li><li>모자이크</li><li>미디어 벽</li><li>트렌딩</li><li>업로드 버튼</li></ul> |
| 컨텐츠 유형 | Instagram, Twitter, Facebook, LiveFyre, YouTube 등 |

## 추가 정보 {#section_b3d_4yl_pdb}

이 페이지에서 설명하는 항목에 대한 자세한 내용은 다음을 참조하십시오.

* [보고서 세트 ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[관리자DTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [규칙](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
