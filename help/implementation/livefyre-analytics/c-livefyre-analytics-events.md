---
title: Livefyre Analytics 이벤트
description: Livefyre Analytics 이벤트
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 5%

---

# Livefyre Analytics 이벤트

## 이벤트 개체 정의 {#section_dh1_yhn_pdb}

다음 코드는 페이지의 Analytics 처리기에서 수신되는 이벤트 개체의 필드를 정의합니다.

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

## Livefyre Analytics 이벤트 및 eVar {#section_u3k_tft_mcb}

다음 Livefyre 이벤트를 사용하여 보고서 세트 관리자를 사용하여 보고서에서 사용할 사용자 지정 이벤트에 매핑합니다. Adobe Analytics의 보고서 세트에 대한 자세한 내용은 [보고서 세트 관리자](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)를 참조하십시오. 보고서 세트 관리자에서 Livefyre 이벤트를 사용하는 방법에 대한 자세한 내용은 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb) 을 참조하십시오.

## Livefyre Analytics 이벤트

| 이벤트 | 설명 |
|---|---|
| 초기화 | 하나 이상의 Livefyre 앱을 포함하는 페이지가 로드되는 경우 |
| 로드 | 사용자 보기에 관계없이 페이지에서 앱이 로드될 때마다 |
| 보기 | 앱이 처음으로 뷰포트에 입력되면. |
| 게시물 | 사용자가 언제든지 다음을 포함한 댓글 또는 컨텐츠 조각 게시합니다. 최상위 게시물, 회신, 검토, 미디어 벽 업로드 |
| 게시됨 | 게시물이 성공했을 때. |
| Twitter_회신 | 사용자가 Twitter에 응답할 때마다 |
| Twitter_Like | 컨텐츠가 공유된 위치: 리트윗 |
| Livefyre_Like | 언제든지 앱에서 livefyre와 같은 기능이 사용됩니다 |
| Livefyre_Unlimited | 사용자가 언제든지 다음과 같은 livefyre를 원하지 않음 |
| ShareOnPost | 언제든지 사용자가 컨텐츠를 게시하고 게시물 공유 기능을 사용합니다 |
| ShareButtonClick | 사용자가 언제든지 댓글에 있는 공유 단추를 클릭하면 |
| ShareTwitter | twitter에 공유 를 클릭할 때 |
| ShareFacebook | facebook에 공유를 클릭할 때 |
| ShareURL | URL에 공유 텍스트 영역을 선택하거나 복사할 때 |
| 회신 확장 | 사용자가 + 또는 확장 링크를 클릭하여 최상위 게시물에 대한 모든 답글을 볼 때 |
| 답글 축소 | 사용자가 - 또는 축소 링크를 클릭하여 최상위 게시물에 대한 모든 답글을 볼 때 |
| FlagClick | 사용자가 언제든지 플래그 모달을 엽니다. |
| FlagSpam | 사용자가 컨텐츠에 스팸으로 플래그를 지정하는 경우 |
| 플래그 동의 안 함 | 사용자가 컨텐츠에 동의하지 않는다고 플래그를 지정하는 경우 |
| 플래그 공격 | 사용자가 컨텐츠에 대해 불쾌하게 플래그를 지정하는 경우 |
| 플래그 해제 주제 | 사용자가 컨텐츠에 오프라는 플래그를 지정할 때 |
| 플래그 취소 | 사용자가 플래그를 제출할 때 언제든지 X나 &quot;취소&quot;를 클릭합니다 |
| FollowCollection | 언제든지 대화 후(&quot;I&#39;m interest&quot; in Review) |
| UnfollowCollection | 대화가 미진행될 때 |
| 추가 요청 | 언제든지 사용자가 앱에 더 많은 콘텐츠를 로드할 때(고속에도 필요함) |
| ModalView | 언제든지 사용자가 클릭하여 모달에서 컨텐츠를 볼 수 있습니다 |
| TwitterRetweetClick | 컨텐츠가 공유된 위치: 리트윗 |
| PostButtonClick | 사용자가 게시물을 클릭할 때(&quot;무슨 생각을 하십니까?&quot;) 버튼 |
| 로그인 | 사용자가 언제든지 로그인함 |
| 로그아웃 | 사용자가 로그아웃할 때마다 언제든지 |

다음은 Livefyre에서 제공하는 전환 변수(eVar) 목록입니다.

## 전환 변수 - eVar

| 이벤트 | 설명 |
|--- |--- |
| 네트워크 ID | Livefyre의 네트워크 ID/이름 |
| 앱 ID | 앱의 URN |
| 컨텍스트 ID | Livefyre의 컨텐츠 ID |
| 앱 유형 | Livefyre 앱 유형. 옵션: <br><ul><li>라이브 블로그  </li><li> 기능 카드</li><li>회전판</li><li>대화 </li><li>설명</li><li>필름 스트립</li><li>맵</li><li>모자이크</li><li>미디어 월</li><li>트렌딩</li><li>업로드 버튼</li></ul> |
| 컨텐츠 유형 | Instagram, Twitter, Facebook, LiveFyre, YouTube 등 |

## 추가 정보 {#section_b3d_4yl_pdb}

이 페이지에서 설명한 주제에 대한 자세한 내용은 다음을 참조하십시오.

* [보고서 세트 관리자](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [태그](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
