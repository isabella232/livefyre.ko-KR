---
description: 'null'
seo-description: 'null'
seo-title: 비속어 필터 사용
solution: Experience Manager
title: 비속어 필터 사용
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 비속어 필터 사용{#using-the-profanity-filter}

Livefyre 앱에 게시된 모든 콘텐츠가 비속어로 확인되었습니다. 비속어 목록에 포함된 단어가 컨텐츠 또는 사용자의 표시 이름에 있는 경우 해당 컨텐츠는 "비속어"로 표시되므로 앱 컨텐츠의 사전 중재, 규칙, ModQ 또는 일반 검색에 대해 필터링할 수 있습니다.

>[!NOTE]
>
>스튜디오 관리자 및 관리자의 컨텐츠는 비속어 규칙 확인의 대상이 아니며 중재자가 게시한 컨텐츠는 플래그 지정되지 않습니다.

Livefyre는 기본 비속어 목록을 제공합니다. 네트워크 수준에서 이 목록을 적용하거나, 사용자 목록을 제공하거나, 두 항목의 합계를 사용하도록 선택할 수 있습니다. 네트워크 내의 개별 사이트는 네트워크 비속어 목록을 상속하거나 사이트별로 맞춤화된 목록을 사용할 수 있습니다.

고유한 비속어 목록을 네트워크 기본값으로 제공하려면 Livefyre 계정 관리자에게 보내주십시오.

## 비속어 필터링 활성화 {#section_yqc_qsk_f1b}

네트워크 및 사이트 수준 모두에서 비속어 필터를 활성화하고 구성합니다. 네트워크 수준에서 비속어 필터를 비활성화하여 네트워크에서 상속되는 모든 사이트에 대한 불경어 필터를 자동으로 비활성화합니다.

>[!NOTE]
>
>Livefyre를 통해 전달되는 모든 컨텐츠는 비속어로 확인됩니다. 기본 SAFE 비속어 목록 또는 사용자 지정 비속어 목록에 포함된 단어가 포함된 컨텐츠가 발견되면 "비속어"로 표시됩니다. Livefyre가 이러한 항목에 대해 자동으로 조치를 취하도록 설정하려면 **[!UICONTROL Enable Profanity Checking]** 로 **[!UICONTROL ON]**&#x200B;이동하십시오.

## 네트워크에 대한 비속어 필터 사용 {#section_twd_ssk_f1b}

1. 네트워크 풀다운 **[!UICONTROL Network]** 메뉴에서 선택합니다.
1. 이동 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 아래로 스크롤하여 **[!UICONTROL Profanity List]**&#x200B;로 **[!UICONTROL Enable Profanity Checking]** 설정합니다 **[!UICONTROL ON]**.

1. 이 **[!UICONTROL Update Network Profanity List]** 필드를 사용하여 목록에 단어를 추가하거나 단어를 클릭하여 목록에서 제거합니다.

>[!NOTE]
>
>네트워크 수준 비속어 목록을 편집해도 이미 존재하는 사이트 수준 목록은 영향을 받지 않습니다. 네트워크를 사이트의 변경 내용을 적용하려면 변경 **[!UICONTROL Restore Network List]** 후 사이트에 대해 선택합니다.

## 사이트에 대한 비속어 필터 사용 {#section_fld_wsk_f1b}

1. 네트워크 풀다운 메뉴에서 사이트를 선택합니다.
1. 이동 **[!UICONTROL Settings > Site Settings > Moderation]**.
1. 아래로 **[!UICONTROL Profanity List]** 스크롤하여 **[!UICONTROL Enable Profanity Checking]** 로 **[!UICONTROL ON]**&#x200B;설정합니다.

1. 다음 옵션 중 하나를 선택합니다.

   * 네트워크에서 비속어 목록을 상속하려면(일반적이지 않음) **[!UICONTROL Use Site Profanity List]** 으로 **[!UICONTROL OFF]**&#x200B;설정합니다.

   * 사이트에 대한 비속어 목록을 편집하려면 목록을 편집할 수 **[!UICONTROL Use Site Profanity List]** 있는 필드를 **[!UICONTROL On]** 열도록 **[!UICONTROL Update Profanity List]** 설정합니다.

      * 단어를 제거하려면 해당 단어를 클릭합니다.
      * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력하고 **[!UICONTROL Return]**&#x200B;클릭합니다.

      * 목록에 단어가 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.
   * 네트워크 비속어 목록을 다시 가져와서 사이트에 적용하려면 을(를) 클릭합니다. **[!UICONTROL Restore Network List]**
   * 목록에서 모든 콘텐츠를 지우고 처음부터 시작하려면 을(를) **[!UICONTROL Clear List]**&#x200B;클릭합니다.


## 욕설이 포함된 컨텐츠 작업 {#section_epy_dtk_f1b}

비속어 목록을 사용하여 컨텐츠 검색을 필터링하고 ModQ용 사전 중재 규칙을 만들 수 있습니다.

비속어가 포함된 컨텐츠를 검색하려면 으로 **[!UICONTROL Library > App Content]**&#x200B;이동한 **[!UICONTROL Filter by Flags]** 다음 **[!UICONTROL Profanity]** 확인란을 선택합니다. 선택한 사이트나 네트워크에 대한 비속어 필터에 의해 걸린 모든 컨텐츠가 표시됩니다. 이 목록에는 SocialSync 및 Streams를 사용하여 앱에 가져온 콘텐츠가 포함됩니다.

사전 중재 규칙을 만들려면 Studio에서 **[!UICONTROL Settings > Network Settings > Moderation]**&#x200B;을 선택합니다. 불경스러운 필터가 활성화되면 새로운 규칙이 나타나므로 불경스러운 내용이 포함된 컨텐츠에 플래그를 지정하거나 사전 중재할 수 있습니다. 기본적으로 이 규칙은 profane 컨텐츠에 대해 자동으로 활성화하며, 이 컨텐츠는 **[!UICONTROL Premoderate]** 또는 **[!UICONTROL Trash it]** **[!UICONTROL Bozo it]**&#x200B;으로 변경될 수 있습니다.

>[!NOTE]
>
>단일 컨텐츠가 여러 규칙 유형(예: SAFE 및 플래그 규칙 모두)에 적용되는 경우 더 엄격한 규칙이 적용됩니다. 예:사전 중재 규칙에 따라 일부 컨텐츠를 사전 중재한다고 되어 있지만 SAFE 규칙이 컨텐츠를 휴지통에 버리도록 되어 있는 경우, 폐기됩니다.

## 네트워크에 대한 비속어 목록 보기 및 업데이트 {#section_qdb_btk_f1b}

1. 이동 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 아래로 스크롤하여 **[!UICONTROL Profanity List]** 섹션으로 이동합니다.
1. 네트워크에 대해 활성화된 목록(Livefyre 기본값 또는 업로드된 사용자 지정 목록)을 **[!UICONTROL Enable Profanity Checking]** **[!UICONTROL On]** 표시하고 편집하도록 설정합니다. 다음과 같은 방법으로 목록을 편집할 수 있습니다.
   * 단어를 제거하려면 해당 단어를 클릭합니다.
   * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력하고 **[!UICONTROL Return]**&#x200B;클릭합니다.
   * 목록에 단어가 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.

>[!NOTE]
>
>스튜디오 관리자와 중재자만 불경사 목록을 편집할 수 있습니다.

