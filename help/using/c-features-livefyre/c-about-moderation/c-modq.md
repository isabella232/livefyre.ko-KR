---
description: 지능형 인터페이스를 통해 컨텐츠를 중재합니다.
seo-description: 지능형 인터페이스를 통해 컨텐츠를 중재합니다.
seo-title: MODQ를 사용하여 컨텐츠 중재
title: MODQ를 사용하여 컨텐츠 중재
uuid: c 630 fb 85-7 bd 0-4 da 0-ac 7 e -080 e 970 fb 4 f 9
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# MODQ를 사용하여 컨텐츠 중재{#moderate-content-using-modq}

지능형 인터페이스를 통해 컨텐츠를 중재합니다.

MODQ는 사용자가 정의한 사전 중재 규칙과 일치하는 사이트나 네트워크에서 모든 컨텐츠의 실시간 큐를 만들어 중재자가 주의가 필요한 컨텐츠에만 집중할 수 있도록 합니다.

MODQ 설정을 정의한 후에는 스트림을 입력하는 새 컨텐츠 또는 사용자가 플래그를 지정한 기존 컨텐츠가 대기열에 추가됩니다. 규칙을 변경하면 MODQ에서 컨텐츠가 제거되지는 않지만 새 설정에 따라 새 컨텐츠가 큐에 추가됩니다.

MODQ를 사용하면 다음을 수행할 수 있습니다.

* 한 번의 클릭으로 컨텍스트 내에서 중재, 전체 스레드 보기, 개별 컨텐츠 또는 전체 컨텐츠 조각 승인, 폐기, 보조 등의 작업을 수행할 수 있습니다.
* 워크플로우의 속도와 효율성을 높일 수 있습니다.
* 컨텐츠에 대한 답글을 달면 커뮤니티의 참여도를 높일 수 있습니다.
* 여러 중재자가 서로의 작업을 복제하지 않고도 컨텐츠를 통해 작업할 수 있습니다.

Livefyre 컨텐츠는 최대 6 주 동안 MODQ에 나열되며, 미리 중재된 스트림 컨텐츠는 MODQ에 90 일간 나열됩니다.

>[!NOTE]
>
>단일 컨텐츠가 MODQ에 포함된 여러 규칙과 일치하는 경우 여러 번 나열될 수 있습니다. 예를 들어 컨텐츠가 불쾌하기 위해 사용자 플래그 규칙을 트리거하는 경우 나중에 Profane에 대한 다른 규칙을 트리거하면 modq에 두 번 나열됩니다.

MODQ에 표시되지 않는 컨텐츠에는 다음이 포함됩니다.

* 트레이트 콘텐츠
* 중재자가 승인한 컨텐츠.
* 금지된 사용자가 게시한 컨텐츠 또는 금지된 사용자가 적용한 사용자 플래그.

## MODQ 탐색 {#section_uv4_db2_yy}

MODQ는 다음 두 개의 탭 구분 패널로 분할됩니다.

* **[!UICONTROL Items]** 중재용으로 예약된 모든 livefyre-native 및 socialsync 컨텐츠를 나열합니다. 이 탭에는 중재 후에 플래그 지정되거나 편집된 모든 소셜 검색 또는 스트림 컨텐츠가 포함되어 있습니다.
* **[!UICONTROL Streams Premoderation]** 미리 설정된 상태로 스트림에서 앱에 입력된 모든 콘텐츠를 나열합니다. 자세한 내용은 스트림 만들기를 참조하십시오.

두 탭은 동일한 필터 및 중재 도구를 많이 제공합니다.

* **[!UICONTROL Item Count]** 대기열에 남아 있는 항목의 수가 modq의 왼쪽 위 모퉁이에 표시됩니다.
* **[!UICONTROL Filter]** 아이콘을 클릭하여 **[!UICONTROL Filter]** 창에 표시할 컨텐츠를 정의합니다.
* **[!UICONTROL History]** 화면 오른쪽 상단에 있는 **[!UICONTROL History]** 단추를 클릭하여 최근에 조정된 컨텐츠 목록을 열면 작업을 검토하거나 최근 중재 작업을 변경할 수 있습니다. 단추를 다시 클릭하면 큐가 있는 컨텐츠로 돌아갑니다. 100 개의 최근 작업만 표시됩니다. **내역은** 다른 중재자가 수행한 작업을 나열하지 않습니다.

* **[!UICONTROL User Pane]** 페이지 오른쪽 상단의 확장 또는 축소 단추를 클릭하여 사용자 창을 열거나 닫습니다.

## MODQ 컨텐츠 이해 {#section_oxm_kgz_y1b}

나열된 각 컨텐츠에는 게시되었던 사이트와 작성자를 비롯한 미리 보기 정보가 표시됩니다. 항목을 선택하면 모든 미디어를 포함한 전체 컨텐츠가 표시됩니다.

>[!NOTE]
>
>Livefyre 기본 컨텐츠는 스트림 또는 기타 소셜 미디어 소스를 통해 앱에 추가되는 컨텐츠보다 더 많은 정보를 표시합니다.

항목을 선택하면 다음 정보가 표시됩니다.

* **[!UICONTROL Time in Queue:]** 컨텐츠가 MODQ에 추가된 시간을 나열합니다.
* **[!UICONTROL App name:]** 컨텐츠가 표시되는 앱. 앱과 함께 사이트에 연결합니다.
* **[!UICONTROL Content Body:]** 텍스트 및 미디어 썸네일을 사용할 수 있습니다.
* **[!UICONTROL Status:]** 컨텐츠의 현재 상태 (보류 중, 트위닝됨 등).
* **[!UICONTROL Author information:]** 작성자의 이름 및 사용자 이름입니다.
* **[!UICONTROL Timestamp:]** 컨텐츠를 만들 때의 상대적 타임스탬프. 스튜디오의 앱 컨텐츠 페이지에 있는 컨텐츠 조각에 대한 Permalinks
* **[!UICONTROL Flag Type:]** 불쾌함, 반대, 스팸 등

   * 안전 플래그: 스팸 및 벌크.
   * 네트워크 및 사이트 비속어 목록에 의해 적용되는 플래그: 비욕.
   * 플래그로 적용되는 플래그: 혐오스러운 음성, PII (개인 식별 정보), 모욕 및 모욕
   * 사용자 플래그: 스팸, 주제 외, 불쾌함 및 반대.

* **[!UICONTROL Flag origin:]** 나열된 플래그 소스입니다. SAFE, 사용자 이름 또는 Livefyre 일 수 있습니다.
* **[!UICONTROL More info:]** 좋아요 수, 사용자 플래그, 답글, 컨텐츠에 적용된 태그 등 컨텐츠에 대한 세부 사항을 나열합니다. 사이트를 클릭하면 컨텐츠가 있는 사이트의 최상위 페이지가 열립니다. 타임스탬프를 클릭하면 페이지의 컨텍스트에서 컨텐츠의 스레드 보기가 열립니다.

## MODQ의 필터 옵션 {#section_r2c_qc2_yy}

MODQ 창의 왼쪽 상단에 있는을 클릭하여 **[!UICONTROL Filter]** 나열된 콘텐츠에 대해 사용 가능한 필터 옵션이 있는 패널을 엽니다. 옵션을 선택하면 MODQ가 자동으로 업데이트되어 필터링된 컨텐츠만 나열됩니다. 선택한 **[!UICONTROL Clear filters]** 모든 옵션을 지우려면을 클릭하고 전체 항목 목록을 다시 로드하십시오.

**[!UICONTROL Items]** AND **[!UICONTROL Streams Premoderation]** 탭에서 다양한 필터 옵션을 사용할 수 있습니다.

다음 옵션을 **[!UICONTROL Items]** 두 가지 모두에서 modq에 사용할 수 **[!UICONTROL Streams Premoderation]**있습니다.

* **[!UICONTROL App]**. 앱별로 결과를 필터링하려면 검색 앱 필드를 사용하십시오. 여러 앱이 선택될 수 있습니다.
* **[!UICONTROL System Flags]**. 스팸, 비속어, 안전 및 중재 규칙과 같은 규칙으로 컨텐츠를 필터링합니다.

   * 선택하면 **[!UICONTROL Spam]** 스팸으로 태그가 지정된 모든 컨텐츠가 보호됩니다.
   * 선택하면 **[!UICONTROL Profanity]** 네트워크 또는 사이트 비속어 목록에 의해 태그가 지정된 모든 콘텐츠가 나열됩니다.
   * 선택하면 **[!UICONTROL SAFE]** 보호 규칙의 결과로 modq를 입력하는 모든 컨텐츠가 나열됩니다.
   * 선택하면 **[!UICONTROL Premoderation]** 네트워크, 스트림 또는 앱 설정으로 중재용으로 태그가 지정된 모든 콘텐츠가 나열됩니다.

* **[!UICONTROL User Flags]** 사용자 플래그로 콘텐츠를 필터링합니다. 옵션에는 불쾌함, 스팸, 주제없음, 반대 등이 있습니다.
* **[!UICONTROL Rights Requests.]** 확인란을 클릭하여 권한이 부여된 컨텐츠만 표시합니다.
* **[!UICONTROL Entered the queue.]** 컨텐츠를 MODQ로 전송된 시간 프레임으로 필터링합니다. 컨텐츠가 MODQ로 전송된 시간은 콘텐츠가 앱에 게시된 시간이 아닐 수 있습니다.

아래의 MODQ에 대해 다음 옵션을 사용할 **[!UICONTROL Streams Premoderation]**수 있습니다.

* **[!UICONTROL Social Source]** 컨텐츠가 시작된 소셜 소스별로 컨텐트를 필터링합니다. 예를 들어 소셜 소스에는 Twitter, Instagram, Facebook 및 RSS가 포함됩니다.

아래의 MODQ에 대해 다음 옵션을 사용할 **[!UICONTROL Items]**수 있습니다.

**[!UICONTROL Moderation Recommendations]**. 자동화된 중재 권장 사항으로 지정된 권장 사항으로 컨텐츠를 필터링합니다.

다음 이미지는 MODQ에서 중재 권장 사항이 표시되는 모습을 보여줍니다. ![](assets/mod_reco1.png)

중재 권장 사항은 **[!UICONTROL Network Settings > Moderation]** 및 **[!UICONTROL Network Settings > ModQ]**에 설정된 컨텐츠를 위해 제공됩니다.

## MODQ에서 사용할 수 있는 작업 {#section_h4g_wrn_z1b}

MODQ에서 각 컨텐츠로 수행할 작업을 결정할 수 있습니다.

다음 옵션 중 하나를 선택합니다.

* 컨텐츠를 승인할 **[!UICONTROL Checkbox]** 아이콘
* 휴지통으로 컨텐츠를 전송하는 **[!UICONTROL Trash can]** 아이콘
* **[!UICONTROL Request Rights]** 컨텐츠 소유자의 컨텐츠에 대한 권한을 요청하려면

   >[!NOTE]
   >
   >Instagram의 컨텐츠에 대한 MODQ의 권한은 요청할 수 없습니다. Instagram에서 컨텐츠에 대한 권한 요청을 보내려면 라이브러리 또는 앱 컨텐츠를 사용해야 합니다.

* **[!UICONTROL Feature and Approve]** to approve the content and also feature the piece of content.
* **[!UICONTROL Product Tag and Approve]** 제품 카탈로그의 제품을 컨텐츠에 추가한 다음 승인합니다.
* **[!UICONTROL Mark as Pending]** to mark the content as pending.

>[!NOTE]
>
>컨텐츠가 조각나면 컨텐츠 조각과 컨텐츠에 대한 모든 답글이 modq에서 영구적으로 제거됩니다. 앱에 콘텐츠를 깔끔하게 정리하려면 앱에 스와이프 항목 [추가를 참조하십시오](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

컨텐츠가 이미 원하는 상태에 있는 경우 휴지통, 보조 또는 승인을 선택하여 상태를 확인하고 목록에서 항목을 제거합니다. 컨텐츠 일부를 중재하면 큐에서 즉시 제거되고 다른 중재자의 대기열에서 비활성화됩니다.

>[!NOTE]
>
>스트림 컨텐츠는 Bozo'd가 아닐 수 있습니다. 스트림 컨텐츠를 레스터스하면 스트림에서 영구적으로 제거되며 실행 취소할 수 없습니다.

컨텐츠가 조정되면 중재자의 MODQ에서 제거되고 작성자가 스트림 내에서 더 이상 편집할 수 없게 됩니다. 중재자가 항목을 삭제하거나 사용자가 주석을 삭제하는 경우, 다른 중재자의 대기열에서 실시간으로 회색으로 표시됩니다. 컨텐츠가 회색으로 표시되면, **[!UICONTROL Clear Moderated]** 이 단추가 페이지에 표시되어 중재자가 목록에서 해당 단추를 제거할 수 있고 다른 중재자 활동과 관계없이 페이지에서 자신의 위치를 유지할 수 있습니다.

## MODQ에서 휴지통 기능 사용 {#section_tpx_qgz_y1b}

설정 섹션을 사용하여 컨텐츠가 트윗으로 표시되면 사용할 수 있는 옵션을 선택합니다.

* ****[!UICONTROL Confirm Trash]**** 컨텐츠를 휴지통으로 설정할 때 중재자가 자신의 작업을 확인하도록 하려면 이 옵션을 활성화합니다. 활성화할 경우 컨텐츠 선택은 **[!UICONTROL Trash]** A **[!UICONTROL Reason for Moderation]**를 요구하는 대화 상자를 표시하고 A를 입력할 **[!UICONTROL Note]** 수 있는 필드를 제공합니다.

   이 설정은 네트워크 수준에서 사용할 수 **[!UICONTROL only]** 있으며, 네트워크 아래에 있는 모든 사이트에 적용됩니다.

* ****[!UICONTROL Hide Replies]**** 상위 댓글이 트래싱되거나 보조 상태일 때 자동으로 답글을 보내려면 이 옵션을 활성화합니다.

## MODQ에서 사용자 상태 변경 {#section_tmw_lg1_z1b}

사용자 요약 패널에서 **[!UICONTROL User actions]** 단추를 클릭하여 사용자를 음소거, 금지 또는 화이트 리스트로 만듭니다.

* **[!UICONTROL Mute:]** 나열된 콘텐트에 플래그를 지정한 사용자의 플래그를 음소거할 수 있습니다. 이 옵션을 사용하여 중재 필터에서 사용자의 플래그를 제외합니다. 플래그가 지정된 컨텐츠는 플래그 결과로 modq를 입력하지 않으며 플래그가 플래그 규칙에 포함되지 않습니다.
* **[!UICONTROL Ban:]** 사이트 또는 네트워크에서 나열된 사용자를 금지할 수 있습니다. (스튜디오 관리자 또는 사용자 관리자만 사용자를 네트워크 금지할 수 있습니다.)
* **[!UICONTROL Whitelist:]** 사이트 또는 네트워크에 대해 나열된 사용자를 화이트리스트에 표시할 수 있습니다. (스튜디오 관리자 또는 사용자 관리자만 화이트 리스트를 사용자 정의할 수 있습니다.)



MODQ를 사용하는 앱:

* [채팅](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [업로드 단추](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

