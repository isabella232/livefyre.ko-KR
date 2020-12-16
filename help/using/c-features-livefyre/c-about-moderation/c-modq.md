---
description: 지능적인 단일 인터페이스에서 컨텐츠를 중재합니다.
seo-description: 지능적인 단일 인터페이스에서 컨텐츠를 중재합니다.
seo-title: ModQ를 사용하여 컨텐츠 중재
title: ModQ를 사용하여 컨텐츠 중재
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# ModQ{#moderate-content-using-modq}을 사용하여 콘텐트 중재

지능적인 단일 인터페이스에서 컨텐츠를 중재합니다.

ModQ는 사용자가 정의한 사전 중재 규칙과 일치하는 사이트 또는 네트워크의 모든 컨텐츠의 실시간 큐를 만들어 중재자가 주의가 필요한 컨텐츠에만 집중할 수 있도록 합니다.

ModQ 설정을 정의하면, 스트림에 들어가는 새 컨텐츠 또는 사용자가 플래그를 지정한 기존 컨텐츠가 대기열에 추가됩니다. 규칙을 변경하면 ModQ에서 내용이 제거되지는 않지만 새 설정에 따라 대기열에 새 내용이 추가됩니다.

ModQ를 사용하면 다음 작업을 수행할 수 있습니다.

* 컨텍스트에서 중재하고 전체 스레드를 보고 개별 컨텐츠 조각 또는 전체 스레드를 한 번의 클릭으로 승인, 휴지통 또는 Bozo를 봅니다.
* 워크플로우의 속도와 효율성을 높일 수 있습니다.
* 컨텐츠에 응답하여 커뮤니티에 대한 참여를 높일 수 있습니다.
* 여러 중재자가 서로의 작업을 복제하지 않고도 컨텐츠를 통해 작업할 수 있습니다.

Livefyre 컨텐츠는 최대 6주 동안 ModQ에 나열되며, 해결되지 않은 미리 중재된 스트림 컨텐츠는 90일 동안 ModQ에 나열됩니다.

>[!NOTE]
>
>ModQ에 포함하기 위해 여러 규칙과 일치하는 컨텐츠 한 조각이 여러 번 나열될 수 있습니다. 예를 들어, 컨텐츠 조각이 공세를 위해 사용자 플래그 규칙을 트리거한 다음 나중에 Profane에 대한 다른 규칙을 트리거하는 경우 ModQ에 두 번 나열됩니다.

ModQ에 표시되지 않는 컨텐츠에는 다음이 포함됩니다.

* 숨겨진 콘텐츠.
* 중재자가 승인한 컨텐츠.
* 금지된 사용자가 게시한 컨텐츠 또는 금지된 사용자가 적용한 사용자 플래그.

## ModQ 탐색 {#section_uv4_db2_yy}

ModQ는 다음과 같이 두 개의 탭 패널로 분할됩니다.

* **[!UICONTROL Items]** 중재 대상이 지정된 모든 Livefyre 기본 및 SocialSync 컨텐츠를 나열합니다. 이 탭에는 중재 후 플래그 지정되거나 편집된 소셜 검색 또는 스트림 컨텐츠가 포함됩니다.
* **[!UICONTROL Streams Premoderation]** 사전 중재가 활성화된 상태에서 Streams에서 앱에 입력하는 모든 컨텐츠를 나열합니다. (자세한 내용은 스트림 만들기를 참조하십시오.)

두 탭 모두 동일한 필터 및 중재 도구를 많이 제공합니다.

* **[!UICONTROL Item Count]** 대기열에 남아 있는 항목 수는 ModQ의 왼쪽 위 모서리에 표시됩니다.
* **[!UICONTROL Filter]** 창 **[!UICONTROL Filter]** 에 표시될 컨텐츠의 매개 변수를 정의하려면 아이콘을 클릭합니다.
* **[!UICONTROL History]** 화면 오른쪽  **[!UICONTROL History]** 상단에 있는 단추를 클릭하여 최근에 중재된 컨텐츠 목록을 열고 작업을 검토하거나 최근 중재 작업을 변경할 수 있습니다. 단추를 다시 클릭하여 큐에 있는 컨텐츠로 돌아갑니다. 최근 작업 100개만 표시됩니다. **히스토리** 는 다른 중재자가 수행한 작업을 나열하지 않습니다.

* **[!UICONTROL User Pane]** 페이지 오른쪽 위에 있는 확장 또는 축소 단추를 클릭하여 사용자 창을 열거나 닫습니다.

## ModQ 컨텐츠 이해 {#section_oxm_kgz_y1b}

나열된 각 컨텐츠 조각에는 게시된 사이트와 작성자를 비롯하여 미리 보기 정보가 표시됩니다. 항목을 선택하면 모든 미디어를 포함한 전체 컨텐츠가 표시됩니다.

>[!NOTE]
>
>Livefyre 기본 컨텐츠는 스트림 또는 기타 소셜 미디어 소스를 통해 앱에 추가된 컨텐츠보다 더 많은 정보를 표시합니다.

항목을 선택하면 다음 정보가 표시됩니다.

* **[!UICONTROL Time in Queue:]** 는 컨텐츠 조각이 ModQ에 추가된 시간을 나열합니다.
* **[!UICONTROL App name:]** 콘텐츠가 표시되는 앱. 앱을 사용하여 사이트에 연결합니다.
* **[!UICONTROL Content Body:]** 텍스트 및 미디어 축소판(가능한 경우).
* **[!UICONTROL Status:]** 컨텐츠의 현재 상태(보류 중, 휴지됨 등)입니다.
* **[!UICONTROL Author information:]** 작성자 이름과 사용자 이름입니다.
* **[!UICONTROL Timestamp:]** 컨텐츠를 만든 시점의 상대적 타임스탬프입니다. Studio의 앱 콘텐츠 페이지에 있는 콘텐츠 부분에 대한 링크를 표시합니다.
* **[!UICONTROL Flag Type:]** 공격, 반대, 스팸 등

   * 안전 플래그:스팸과 벌크.
   * 네트워크 및 사이트 비속어 목록에서 적용되는 플래그:욕설.
   * SAFE에 의해 적용된 플래그:증오 연설, PII(개인 식별 정보), 모욕 및 모욕.
   * 사용자 플래그:스팸, 주제 외, 불쾌함 및 반대.

* **[!UICONTROL Flag origin:]** 나열된 플래그의 소스입니다. SAFE, 사용자 이름 또는 Livefyre일 수 있습니다.
* **[!UICONTROL More info:]** 좋아요 수, 사용자 플래그, 답글 및 컨텐츠에 적용된 태그를 포함하여 컨텐트에 대한 세부 사항을 나열합니다. 사이트를 클릭하면 컨텐츠가 있는 사이트의 최상위 페이지가 열립니다. 타임스탬프를 클릭하면 페이지의 컨텍스트에서 컨텐츠의 스레드 보기가 열립니다.

## ModQ {#section_r2c_qc2_yy}의 필터 옵션

ModQ 창의 왼쪽 상단에 있는 **[!UICONTROL Filter]**&#x200B;을 클릭하여 나열된 내용에 대해 사용 가능한 필터 옵션이 있는 패널을 엽니다. 옵션을 선택하면 ModQ가 자동으로 업데이트되어 필터링된 컨텐츠만 나열됩니다. 선택한 모든 옵션을 지우려면 **[!UICONTROL Clear filters]**&#x200B;을 클릭하고 전체 항목 목록을 다시 로드합니다.

**[!UICONTROL Items]** 및 **[!UICONTROL Streams Premoderation]** 탭에 대해 다른 필터 옵션을 사용할 수 있습니다.

**[!UICONTROL Items]** 및 **[!UICONTROL Streams Premoderation]** 모두 아래의 ModQ에 다음 옵션을 사용할 수 있습니다.

* **[!UICONTROL App]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 앱 검색 필드를 사용하여 결과를 앱별로 필터링합니다. 여러 앱을 선택할 수 있습니다.
* **[!UICONTROL System Flags]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 스팸, 비속어, SAFE 및 중재 규칙과 같은 규칙으로 컨텐츠를 필터링합니다.

   * **[!UICONTROL Spam]**&#x200B;을 선택하면 SAFE로 스팸으로 태그가 지정된 모든 컨텐츠가 표시됩니다.
   * **[!UICONTROL Profanity]**&#x200B;을 선택하면 네트워크 또는 사이트 비속어 목록에서 Profane 태그가 지정된 모든 컨텐트가 나열됩니다.
   * **[!UICONTROL SAFE]**&#x200B;을 선택하면 SAFE 규칙 결과로 ModQ에 입력된 모든 컨텐츠가 나열됩니다.
   * **[!UICONTROL Premoderation]**&#x200B;을 선택하면 네트워크, 스트림 또는 앱 설정에서 사전 중재에 태그가 지정된 모든 콘텐츠가 표시됩니다.

* **[!UICONTROL User Flags]** 사용자 플래그별로 컨텐츠를 필터링합니다. 옵션에는 공격, 스팸, 주제 외 및 반대 등이 있습니다.
* **[!UICONTROL Rights Requests.]** 확인란을 클릭하여 권한이 부여된 컨텐츠만 표시합니다.
* **[!UICONTROL Entered the queue.]** 내용이 ModQ로 전송된 시간별로 컨텐츠를 필터링합니다. 콘텐츠가 ModQ로 전송된 시간은 콘텐츠가 앱에 게시된 시간이 아닐 수도 있습니다.

**[!UICONTROL Streams Premoderation]** 아래의 ModQ에 다음 옵션을 사용할 수 있습니다.

* **[!UICONTROL Social Source]** 컨텐츠가 시작된 소셜 소스별로 컨텐츠를 필터링합니다. 예를 들어 소셜 소스의 옵션에는 Twitter, Instagram, Facebook 및 RSS가 포함됩니다.

**[!UICONTROL Items]** 아래의 ModQ에 다음 옵션을 사용할 수 있습니다.

**[!UICONTROL Moderation Recommendations]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 자동화된 중재 추천에서 제공한 권장 사항으로 컨텐츠를 필터링합니다.

다음 이미지는 ModQ에서 중재 Recommendations의 모양을 보여줍니다. ![](assets/mod_reco1.png)

컨텐츠가 **[!UICONTROL Network Settings > Moderation]** 및 **[!UICONTROL Network Settings > ModQ]**&#x200B;에 설정되면 컨텐츠에 대한 중재 권장 사항이 제공됩니다.

## ModQ {#section_h4g_wrn_z1b}에서 사용할 수 있는 작업

ModQ에서 각 컨텐츠로 수행할 작업을 결정할 수 있습니다.

다음 옵션 중 하나를 선택합니다.

* 컨텐츠를 승인하는 **[!UICONTROL Checkbox]** 아이콘
* 내용을 휴지통으로 보내는 **[!UICONTROL Trash can]** 아이콘
* **[!UICONTROL Request Rights]** 을 클릭하여 컨텐츠 소유자로부터 컨텐츠에 대한 권한을 요청합니다.

   >[!NOTE]
   >
   >Instagram의 콘텐츠에 대한 ModQ의 권한은 요청할 수 없습니다. 라이브러리 또는 앱 콘텐츠를 사용하여 Instagram에서 콘텐츠에 대한 권한 요청을 보내야 합니다.

* **[!UICONTROL Feature and Approve]** 컨텐츠를 승인하고 컨텐츠 일부를 특정할 수 있습니다.
* **[!UICONTROL Product Tag and Approve]** 제품 카탈로그의 제품을 컨텐츠에 추가한 다음 승인합니다.
* **[!UICONTROL Mark as Pending]** 을 클릭하여 컨텐츠를 보류 중으로 표시합니다.

>[!NOTE]
>
>컨텐츠 일부를 휴지하면 컨텐츠 일부와 컨텐츠 부분에 대한 모든 응답이 ModQ에서 영구적으로 제거됩니다. 패싱된 콘텐츠를 앱에 배치하려면 [패싱된 항목을 다시 앱](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)에 추가를 참조하십시오.

컨텐츠가 이미 원하는 상태에 있는 경우 휴지통, 보조 또는 승인을 선택하면 상태가 확인되고 목록에서 항목이 제거됩니다. 콘텐츠 일부를 중재하면 큐에서 해당 콘텐츠가 즉시 제거되고 다른 중재자의 대기열에서 비활성화됩니다.

>[!NOTE]
>
>스트림 컨텐츠는 Bozo&#39;d가 아닐 수 있습니다.스트림 콘텐츠를 트래싱하면 스트림에서 영구적으로 제거되며 실행 취소할 수 없습니다.

컨텐츠가 중재되면 중재자의 ModQ에서 제거되고 작성자는 더 이상 스트림 내에서 컨텐츠를 편집할 수 없습니다. 중재자가 항목을 해임하거나 사용자가 댓글을 삭제하는 경우 다른 중재자의 대기열에 실시간으로 흐리게 표시됩니다. 컨텐츠가 회색으로 표시되면 중재자가 목록에서 해당 컨텐츠를 제거하고 다른 중재자 활동과 관계없이 페이지에서 자신의 위치를 유지할 수 있도록 페이지에 **[!UICONTROL Clear Moderated]** 단추가 표시됩니다.

## ModQ {#section_tpx_qgz_y1b}에서 휴지통 함수 사용

설정 섹션을 사용하여 컨텐츠가 [해시됨]으로 표시된 경우 사용할 수 있는 옵션을 선택합니다.

* ****[!UICONTROL Confirm Trash]**** 컨텐츠를 휴지통으로 설정할 때 중재자가 자신의 작업을 확인하도록 하려면 이 옵션을 활성화합니다. 활성화되면 컨텐트에 대해 **[!UICONTROL Trash]**&#x200B;을 선택하면 **[!UICONTROL Reason for Moderation]**&#x200B;을 요청하는 대화 상자가 표시되고 **[!UICONTROL Note]**&#x200B;를 입력할 수 있는 필드가 제공됩니다.

   (이 설정은 네트워크 수준에서 **[!UICONTROL only]**&#x200B;을 사용할 수 있으며 네트워크 아래의 모든 사이트에 적용됩니다.)

* ****[!UICONTROL Hide Replies]**** 상위 댓글이 해시되거나 Bozo&#39;d가 파싱될 때 자동으로 답글을 휴지통으로 만들려면 이 옵션을 활성화합니다.

## ModQ {#section_tmw_lg1_z1b}의 사용자 상태 변경

사용자 요약 패널에서 **[!UICONTROL User actions]** 버튼을 클릭하여 사용자를 음소거, 금지 또는 허용 목록에 표시합니다.

* **[!UICONTROL Mute:]** 나열된 컨텐트에 플래그를 지정한 사용자의 플래그 음소거를 수행할 수 있습니다. 사전 중재 필터에서 사용자의 플래그를 제외하려면 이 옵션을 사용합니다. 플래그가 달린 컨텐트는 플래그 결과로 ModQ에 들어가지 않으며 플래그 규칙은 플래그 규칙에 포함되지 않습니다.
* **[!UICONTROL Ban:]** 나열된 사용자를 사이트 또는 네트워크에서 금지할 수 있습니다. (스튜디오 관리자 또는 사용자 관리자만 사용자를 네트워크를 금지할 수 있습니다.)
* **[!UICONTROL Whitelist:]** 나열된 사용자의 사이트 또는 네트워크 목록을 허용할 수 있습니다. (Studio 관리자 또는 사용자 관리자만 사용자 목록을 네트워크에서 허용할 수 있습니다.)



ModQ를 사용하는 앱:

* [대화](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [사이드노트](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [업로드 버튼](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

