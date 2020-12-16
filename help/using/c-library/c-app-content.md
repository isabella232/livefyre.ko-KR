---
description: Livefyre 네트워크에서 콘텐츠 관리
seo-description: Livefyre 네트워크에서 콘텐츠 관리
seo-title: 앱 콘텐츠 탭
solution: Experience Manager
title: 앱 콘텐츠 탭
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---


# 앱 콘텐츠 탭{#app-content-tab}

Livefyre 네트워크에서 콘텐츠 관리

라이브러리의 앱 콘텐츠 탭에서는 앱 전체에 게시된 콘텐츠를 검색하고 중재할 수 있습니다. **[!UICONTROL App Content]** 탭에서는 와일드카드 검색을 포함한 여러 검색 필터를 사용하여 검색 매개 변수를 보다 빠르고 쉽게 정의할 수 있습니다.

앱 콘텐츠 탭을 사용하여 다음을 수행할 수 있습니다.

* 컨텐츠 검색
* 콘텐트 내역 보기
* 컨텐츠 중재
* 태그 추가
* 기능 컨텐츠
* 제품 카탈로그의 제품과 컨텐츠 연결

앱 콘텐츠 탭을 사용하여 콘텐츠를 중재하는 방법에 대한 자세한 내용은 [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)을 참조하십시오.

## 와일드카드 검색 {#section_jvr_ntm_zz}

Livefyre 검색 필드는 일부 일치 항목을 포착하기 위해 단어(또는 단어 조각)에 별표(*)를 추가할 수 있는 와일드카드를 지원합니다.

예:

* 공은 공만 반환합니다.
* ball*은 공기와 풍선을 반환합니다.
* *볼 리턴 볼 및 축구
* *ball*은 공과 유니볼을 반환하고

## {#section_fw1_mtm_zz} 콘텐트 검색

앱 콘텐츠 패널에서는 여러 가지 콘텐츠 필터링 옵션을 사용하여 검색 범위를 좁힐 수 있습니다.

![](assets/PublishedState-1024x367.png)

**[!UICONTROL Quick Filters]** 풀다운을 사용하여 반환된 내용의 범위를 **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** 또는 **[!UICONTROL Rights Requests]** 상태로 좁힙니다. 그런 다음 **[!UICONTROL Filter by]** 옵션을 선택하고 검색 범위를 좁히는 데 사용할 수 있는 확인란 또는 입력 필드를 사용합니다.

풀다운 메뉴를 사용하여 목록의 내용을 **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** 또는 **[!UICONTROL Most liked]**&#x200B;별로 정렬합니다.

## 옵션 {#section_aqn_xqm_zz}별로 필터링

**[!UICONTROL Filter by]** 막대를 사용하여 다음 옵션을 필터링합니다.

* **상태** 컨텐츠의 현재 중재 상태(**,  [!UICONTROL All Content]**,  **[!UICONTROL Approved]** **[!UICONTROL Pending]** 또는  **[!UICONTROL Bozo]**)로 필터링할 수 있습니다.

* **** 소스컨텐츠 소스별로 필터링할 수 있습니다. 스트림에 직접 게시된 사용자 생성 콘텐츠를 나열하려면 **[!UICONTROL Livefyre]**&#x200B;을 선택합니다. 이러한 소스에서 앱에 가져온 콘텐츠를 포함하려면 **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** 또는 **[!UICONTROL RSS]**&#x200B;를 선택합니다.

* **플래그** 선택 플래그를 사용하면 SAFE(비속어, 스팸 또는 마술처럼 중재됨)에  **[!UICONTROL User Flags]** 의해  **[!UICONTROL System Flags]** (스팸, 주제 외, 공격 또는 반대) 또는 **[!UICONTROL Moderation Recommendations]**&#x200B;으로 필터링하거나 필터링할 수있습니다.  ![](assets/appcontentfilter.png)

* **날짜/** 시간컨텐츠가 원래  **[!UICONTROL Created]**   **[!UICONTROL Modified]** (또는 SocialSync 또는 스트림을 통해 앱에 가져올 수 있음) 또는 마지막(편집, 플래그 지정됨 또는 상태 변경)으로 필터링할 수 있습니다.

* **작성자** 작성자의  **[!UICONTROL IP]** 주소,  **[!UICONTROL Display Name]** (사용자 패널이나 작성자가 게시한 컨텐츠 위에 있음) 또는  **[!UICONTROL User ID]**(사용자 패널에 있음)에 따라 필터링할 수 있습니다.

* **포함** 을 사용하여 최근 90일 동안의 컨텐츠를 또는 별로 필터링할  **[!UICONTROL Keyword]** 수  **[!UICONTROL Content Tag]** 있습니다. 미디어가 포함된 컨텐츠만 반환하려면 **[!UICONTROL Media]** 확인란을 선택합니다. 모든 콘텐트를 검색하려면 목록의 모든 콘텐트를 아래로 스크롤한 다음 **[!UICONTROL Search full data]**&#x200B;을 클릭합니다.

   **참고:** 여러 개의 키워드 및 컨텐트 태그 검색은 지원되지 않습니다. 여러 키워드 또는 태그를 입력하면 검색에 마지막 단어가 사용됩니다.

   컨텐트 태그로 검색할 때 검색 필드에 입력할 때 제안된 태그가 자동으로 채워집니다. 검색 결과는 태그가 할당된 모든 컨텐츠를 반환합니다. 이 필드를 사용하여 주요 콘텐트를 검색하거나 Studio의 모든 주요 콘텐트에서 **[!UICONTROL Featured]** 레이블을 클릭합니다.

   **참고:** 태그 이름 앞에 빼기(-) 기호를 사용하여 해당 태그를 포함하지 않는 컨텐츠를 검색합니다. 예:&#39;-Miley&#39;를 검색하여 &#39;Miley&#39; 태그가 포함되지 않은 모든 컨텐츠를 검색합니다.

* **앱** 상위 ID **[!UICONTROL Collection ID]**,  **[!UICONTROL App Tag]**&#x200B;또는  **상위 ID로 필터링할 수 있습니다**. 상위 ID로 필터링하면 입력 콘텐츠 ID에 대한 응답인 모든 콘텐츠를 반환합니다. (쉼표로 구분된 태그를 입력하여 여러 태그로 필터링합니다.)

* **권한** 권한 요청 상태**,  [!UICONTROL Requested]**  **[!UICONTROL Granted]** **[!UICONTROL Replied]** 또는  **[!UICONTROL Expired]**&#x200B;을 기준으로 필터링할 수 있습니다.

## Bozo 컨텐트 {#section_afl_vqm_zz}

앱에서 **[!UICONTROL Bozo]** 컨텐츠는 컨텐츠 작성자에게만 표시됩니다. 이렇게 하면 다른 모든 사용자 및 중재자로부터 컨텐츠를 숨긴 채 컨텐츠가 승인되었다고 믿을 수 있습니다.

>[!NOTE]
>
>SocialSync 또는 Streams **[!UICONTROL cannot]**&#x200B;에서 시작된 소셜 컨텐츠는 Bozo로 설정됩니다.

다음과 같은 이유로 Bozo 컨텐츠를 만들 수 있습니다.

* SAFE로 스팸으로 식별된 컨텐츠는 자동으로 Bozo 상태로 설정됩니다.
* 금지된 사용자의 모든 컨텐츠는 자동으로 Bozo로 설정됩니다.
* 컨텐츠는 Studio의 Bozo로 표시될 수 있습니다.
* 중재자는 스트림에서 바로 Bozo 컨텐츠를 볼 수 있습니다.

## 콘텐트 내역 보기 {#section_ayz_tqm_zz}

콘텐츠 패널에서는 사전 중재, 스팸 필터링, 게시 날짜, 항목에 할당된 사용자 플래그 또는 메모를 포함하여 목록에 있는 모든 컨텐츠의 내역을 검토할 수 있습니다.

내용 패널 아래쪽에 있는 탭을 사용하여 작업 내역을 확인합니다.

* **[!UICONTROL More Info:]** 제출, 편집, 스팸 확인, 상태 변경 및 메모를 포함하여 이 컨텐츠에 대한 모든 활동을 나열합니다. Livefyre 콘텐츠 ID 및 사용자의 IP 주소도 이 섹션에 표시됩니다.
* **[!UICONTROL Replies:]** 최대 6개의 답글을 나열합니다. 게시물에 대한 모든 답글을 표시하려면 **[!UICONTROL Show all replies]**&#x200B;을 클릭합니다.

* **[!UICONTROL Flags & Reports:]** 컨텐트에 플래그를 지정한 사용자의 아바타와 모든 보고서(컨텐츠에 플래그를 지정할 때 사용자가 추가한 노트)를 포함한 모든 사용자 플래그를 나열합니다.
* **[!UICONTROL Add a note:]** 다른 관리자 또는 중재자가 볼 수 있는 메모를 추가할 수 있습니다.
* **[!UICONTROL Request Rights:]** 권한  **[!UICONTROL New Rights Request]** 요청을 실행할 수 있는 대화 상자를 엽니다.

* **[!UICONTROL Save as Asset:]**선택한 항목을 자산 라이브러리에 저장, 앱에 게시 또는 작성자의 권한 재사용을 요청할 수 있는 **[!UICONTROL Advanced Options]** 대화 상자를 엽니다.

![](assets/PublishedMoreInfo-1024x462.png)

## {#section_xb4_mxr_rdb} 콘텐츠에 태그 추가

컨텐츠 태그 지정을 사용하면 컨텐츠를 분류하여 손쉽게 검색하고 스타일을 지정할 수 있으며 컨텐츠를 특색으로 표시할 수 있습니다.

태그를 추가하려면 컨텐츠 아래의 더하기( **[!UICONTROL +]**) 아이콘을 클릭하면 됩니다. 새 태그를 입력하거나 기존 태그 목록에서 선택합니다.

![](assets/PublishedAddTag-1024x338.png)

## 모든 자산에서 이미지 검색 중 {#section_zxf_hsf_wcb}

라이브러리에 컨텐츠를 추가한 후에는 스마트 태그로 컨텐츠를 검색할 수 있습니다.

라이브러리의 모든 에셋 아래에서 **[!UICONTROL Show Filters]**&#x200B;을 클릭한 다음 다음을 클릭하여 기존 이미지를 검색할 수 있습니다.

* 검색 필드에 검색할 텍스트 입력
* 연관성별로 정렬
* 스마트 태그로 검색할 텍스트를 **[!UICONTROL Tags]** 필드에 입력합니다. 스마트 태그 등급 알고리즘은 스마트 태그 신뢰 점수, 컨텐츠의 새로운 여부, 사용자가 컨텐츠에 부여한 별 수를 사용하여 컨텐츠를 필터링합니다.

## 주요 내용 {#section_emb_kqm_zz}

기본 **[!UICONTROL Featured]** 태그를 선택하여 컨텐트를 특색으로 표시하고 사용자에게 중요하다고 강조 표시합니다. 태그가 지정되면 사용자 정의 스타일 옵션을 사용하여 앱에서 주요 콘텐츠를 사용자 정의합니다.

## 기능 또는 기능 해제 내용 {#section_ojx_3qm_zz}

* Studio에서 콘텐츠 옆의 **[!UICONTROL +]** 기호를 클릭하고 드롭다운 목록에서 **[!UICONTROL Featured]** 태그를 선택한 다음 기능 콘텐츠에 대해 **[!UICONTROL Enter]**&#x200B;를 클릭합니다. 태그가 저장되고 컨텐츠 옆에 표시됩니다.

* 기능을 해제하려면 컨텐츠 부분에 표시되는 **[!UICONTROL Featured]** 태그의 **[!UICONTROL x]**&#x200B;을 클릭합니다.

* 댓글, 라이브 블로그 또는 리뷰 앱 내에서 원하는 컨텐츠를 가리키고 **[!UICONTROL Feature]**&#x200B;을 클릭합니다. 기능을 해제하려면 컨텐트 위로 마우스를 가져간 다음 **[!UICONTROL Unfeature]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>공간 제약으로 인해 채팅 컨텐츠는 Studio를 사용해서만 특별 또는 특별 표시되지 않을 수 있으며 앱 자체 내에서 특화된 것이 아닙니다.

## 주요 컨텐츠 편집 {#section_pyw_hqm_zz}

컨텐츠에 대한 대부분의 일반 작업은 다음을 제외하고 특별 컨텐츠에서 수행할 수 있습니다.

* 주요 컨텐츠는 플래그를 지정할 수 없습니다.
* 원할 경우 삭제할 수는 있지만 사용자가 기능을 수행한 후에는 컨텐츠를 편집할 수 없습니다. 중재자는 주요 컨텐츠를 편집할 수 있습니다.

