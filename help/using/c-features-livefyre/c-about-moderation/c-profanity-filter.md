---
description: 'null'
seo-description: 'null'
seo-title: 비속어 필터 사용
solution: Experience Manager
title: 비속어 필터 사용
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# 비속어 필터 사용{#using-the-profanity-filter}

Livefyre 앱에 게시된 모든 콘텐츠가 비속어로 확인되었습니다. 비속어 목록에 포함된 단어가 컨텐츠 또는 사용자의 표시 이름에 있는 경우 해당 컨텐츠는 &quot;비속어&quot;로 플래그로 표시되므로 앱 컨텐츠의 사전 중재, 규칙, ModQ 또는 일반 검색으로 필터링할 수 있습니다.

>[!NOTE]
>
>스튜디오 관리자 및 관리자의 컨텐츠는 비속어 규칙 확인의 대상이 아니며 중재자가 게시한 컨텐츠는 플래그가 지정되지 않습니다.

Livefyre는 기본 비속어 목록을 제공합니다. 네트워크 수준에서 이 목록을 적용하거나, 사용자 고유의 목록을 제공하거나, 둘 중 하나의 집계를 사용하도록 선택할 수 있습니다. 네트워크 내의 개별 사이트는 네트워크 비속어 목록을 상속하거나 사이트별로 맞춤화된 목록을 사용할 수 있습니다.

고유한 사용자 지정 비속어 목록을 네트워크 기본값으로 지정하려면 Livefyre 계정 관리자에게 보내주십시오.

## 비속어 필터링 활성화 {#section_yqc_qsk_f1b}

네트워크 및 사이트 수준 모두에서 비속어 필터를 활성화하고 구성합니다. 네트워크 수준에서 비속어 필터를 비활성화하여 네트워크에서 상속되는 모든 사이트에 대해 비속어 필터를 자동으로 비활성화합니다.

>[!NOTE]
>
>Livefyre를 통과하는 모든 컨텐츠가 불경스러운 것으로 확인됩니다. 기본 SAFE 비속어 목록 또는 사용자 지정 비속어 목록에 포함된 단어를 포함하는 컨텐츠가 발견되면 &quot;비속어&quot;로 표시됩니다. 이러한 항목에 대해 자동으로 작업을 수행하도록 Livefyre를 설정하려면 **[!UICONTROL Enable Profanity Checking]**&#x200B;을 **[!UICONTROL ON]**&#x200B;로 전환하십시오.

## 네트워크 {#section_twd_ssk_f1b}에 대해 비속어 필터 사용

1. 네트워크 풀다운 메뉴에서 **[!UICONTROL Network]**&#x200B;을 선택합니다.
1. 이동 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. **[!UICONTROL Profanity List]**&#x200B;으로 스크롤하고 **[!UICONTROL Enable Profanity Checking]**&#x200B;을 **[!UICONTROL ON]**&#x200B;로 설정합니다.

1. **[!UICONTROL Update Network Profanity List]** 필드를 사용하여 목록에 단어를 추가하거나 단어를 클릭하여 목록에서 제거합니다.

>[!NOTE]
>
>네트워크 수준 비속어 목록을 편집해도 이미 설치되어 있는 사이트 수준 목록은 영향을 받지 않습니다. 네트워크를 통해 사이트를 변경하려면 변경 후 사이트에 대해 **[!UICONTROL Restore Network List]**&#x200B;을 선택합니다.

## 사이트 {#section_fld_wsk_f1b}에 대해 비속어 필터 사용

1. 네트워크 풀다운 메뉴에서 사이트를 선택합니다.
1. 이동 **[!UICONTROL Settings > Site Settings > Moderation]**.
1. **[!UICONTROL Profanity List]**&#x200B;으로 스크롤하고 **[!UICONTROL Enable Profanity Checking]**&#x200B;을 **[!UICONTROL ON]**&#x200B;로 설정합니다.

1. 다음 옵션 중 하나를 선택합니다.

   * 네트워크에서 비속어 목록을 상속하려면(일반적이지 않음) **[!UICONTROL Use Site Profanity List]**&#x200B;을 **[!UICONTROL OFF]**&#x200B;으로 설정합니다.

   * 사이트에 대한 불경어 목록을 편집하려면 **[!UICONTROL Use Site Profanity List]**&#x200B;을 **[!UICONTROL On]**&#x200B;으로 설정하여 목록을 편집할 수 있는 **[!UICONTROL Update Profanity List]** 필드를 엽니다.

      * 단어를 제거하려면 단어를 클릭합니다.
      * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력하고 **[!UICONTROL Return]**&#x200B;을 누릅니다.

      * 목록에 단어가 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.
   * 네트워크 불경사 목록을 다시 가져와서 사이트에 적용하려면 **[!UICONTROL Restore Network List]** 을 클릭합니다.
   * 목록에서 모든 콘텐츠를 지우고 처음부터 시작하려면 **[!UICONTROL Clear List]**&#x200B;을 클릭합니다.


## 비속어 {#section_epy_dtk_f1b}을 포함하는 컨텐츠 작업

비속어 목록을 사용하여 컨텐츠 검색을 필터링하고 ModQ용 중재 규칙을 만들 수 있습니다.

비속어가 포함된 컨텐츠를 검색하려면 **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]**&#x200B;로 이동하여 **[!UICONTROL Profanity]** 확인란을 선택합니다. 선택한 사이트나 네트워크에 대한 비속어 필터에서 걸린 모든 컨텐츠가 표시됩니다. 이 목록에는 SocialSync 및 Streams를 사용하여 앱에 가져온 콘텐츠가 포함됩니다.

사전 중재 규칙을 만들려면 Studio에서 **[!UICONTROL Settings > Network Settings > Moderation]**&#x200B;을 선택합니다. 비속어 필터가 활성화되면 새로운 규칙이 나타나므로 비속어를 포함하는 컨텐트에 플래그를 지정하거나 사전 중재할 수 있습니다. 기본적으로 이 규칙은 프로파일 컨텐트에 대해 **[!UICONTROL Premoderate]**&#x200B;을(를) 자동으로 활성화합니다. 이 컨텐츠는 **[!UICONTROL Trash it]** 또는 **[!UICONTROL Bozo it]**&#x200B;로 변경될 수 있습니다.

>[!NOTE]
>
>단일 컨텐츠가 여러 규칙 유형(예: SAFE 및 Flag 규칙 모두)의 적용을 받는 경우 더 엄격한 규칙이 적용됩니다. 예:사전 중재 규칙에 컨텐츠 일부분을 사전 중재하도록 되어 있지만, 안전 규칙이 휴지통에 버리도록 되어 있는 경우, 휴지됩니다.

## 네트워크 {#section_qdb_btk_f1b}에 대한 비속어 목록 보기 및 업데이트

1. 이동 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. **[!UICONTROL Profanity List]** 섹션으로 스크롤합니다.
1. 네트워크에 대해 활성화된 목록(Livefyre 기본값 또는 업로드된 사용자 지정 목록)을 표시하려면 **[!UICONTROL Enable Profanity Checking]**&#x200B;을(를) **[!UICONTROL On]**&#x200B;으로 설정하고 편집합니다. 다음과 같은 방법으로 목록을 편집할 수 있습니다.
   * 단어를 제거하려면 단어를 클릭합니다.
   * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력하고 **[!UICONTROL Return]**&#x200B;을 누릅니다.
   * 목록에 단어가 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.

>[!NOTE]
>
>스튜디오 관리자와 중재자만 비속어 목록을 편집할 수 있습니다.

