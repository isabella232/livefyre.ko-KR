---
description: null
seo-description: null
seo-title: 비속어 필터 사용
solution: Experience Manager
title: 비속어 필터 사용
uuid: B 0 B 1 Fbae-C 88 C -403 C -9 B 91-DF 6620675 F 39
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 비속어 필터 사용{#using-the-profanity-filter}

Livefyre 앱에 게시된 모든 콘텐츠가 모독 처리됩니다. 비속어 목록에 포함된 단어가 콘텐츠 또는 사용자의 표시 이름에 있는 경우 해당 콘텐츠는 «모욕» 로 플래그가 지정되며, 앱 컨텐츠에서 중재, 규칙, MODQ 또는 일반 검색을 위해 필터링할 수 있습니다.

>[!NOTE]
>
>Studio 관리자 및 관리자 컨텐츠는 비배타적인 규칙 검사의 대상이 아니며 중재자가 게시한 콘텐츠는 플래그가 지정되지 않습니다.

Livefyre는 기본 비등방성 목록을 제공합니다. 네트워크 수준에서 이 목록을 적용하고, 자신의 목록을 제공하거나, 이 목록을 사용할 수 있습니다. 네트워크 내의 개별 사이트는 네트워크 비속어 목록을 상속받거나 사이트 별로 맞춤화된 목록을 사용할 수 있습니다.

사용자 정의 비배타적 목록을 네트워크 기본값으로 제공하려면 Livefyre 계정 관리자에게 보내 주십시오.

## 비등방성 필터링 사용 {#section_yqc_qsk_f1b}

네트워크 및 사이트 수준에서 비속어 필터를 활성화하고 구성합니다. 네트워크에서 상속되는 모든 사이트에 대한 비속어 필터를 자동으로 비활성화하려면 네트워크 수준에서 비속어 필터를 비활성화합니다.

>[!NOTE]
>
>Livefyre를 통과하는 모든 컨텐츠가 비모독 (profical) 를 확인합니다. 기본 안전 비방 목록 또는 사용자 정의 비방 목록에 포함된 단어를 포함하는 컨텐츠가 발견되면 «모욕» 플래그가 지정됩니다. » Livefyre가 이러한 항목에 대해 자동으로 조치를 취할 수 있도록 설정할 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**수 있습니다.

## 네트워크에 대한 비등방성 필터 사용 {#section_twd_ssk_f1b}

1. 네트워크 **[!UICONTROL Network]** 풀다운 메뉴에서 선택합니다.
1. **[!UICONTROL Settings > Network Settings > Moderation]**이동.
1. 아래로 스크롤하여 **[!UICONTROL Profanity List]**로 설정합니다 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**.

1. **[!UICONTROL Update Network Profanity List]** 필드를 사용하여 목록에 단어를 추가하거나 단어를 클릭하여 목록에서 제거합니다.

>[!NOTE]
>
>네트워크 수준 비속어 목록을 편집해도 이미 위치에 있는 사이트별 목록은 영향을 받지 않습니다. 네트워크에서 변경 사항이 사이트에 적용되었는지 확인하려면 변경 사항이 이루어진 후 해당 사이트를 **[!UICONTROL Restore Network List]** 선택합니다.

## 사이트에 대한 비등방성 필터 사용 {#section_fld_wsk_f1b}

1. 네트워크 풀다운 메뉴에서 사이트를 선택합니다.
1. **[!UICONTROL Settings > Site Settings > Moderation]**이동.
1. **[!UICONTROL Profanity List]****[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**으로 스크롤하여로 스크롤합니다.

1. 다음 옵션 중 하나를 선택합니다.

   * 네트워크에서 비배타적인 목록을 상속하려면 (일반적이지 않음) **[!UICONTROL Use Site Profanity List]** 로 **[!UICONTROL OFF]**설정하십시오.

   * 사이트에 대한 비속어 목록을 편집하려면 **[!UICONTROL Use Site Profanity List]** [으로 **[!UICONTROL On]** 설정] **[!UICONTROL Update Profanity List]** 를 선택하여 목록을 열고 목록을 편집합니다.

      * 단어를 제거하려면 단어를 클릭합니다.
      * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력합니다 **[!UICONTROL Return]**.

      * 단어가 목록에 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.
   * 네트워크 비속어 목록을 다시 가져와서 사이트에 적용하려면 **[!UICONTROL Restore Network List]**을 클릭합니다.
   * 목록에서 모든 콘텐츠를 지우고 처음부터 시작하려면 **[!UICONTROL Clear List]**을 클릭합니다.


## Profical 이 포함된 컨텐츠 작업 {#section_epy_dtk_f1b}

비속어 목록을 사용하여 컨텐츠 검색을 필터링하고 MODQ에 대한 중재 규칙을 만들 수 있습니다.

비속어가 포함된 컨텐츠를 검색하려면 이동 **[!UICONTROL Library > App Content]****[!UICONTROL Filter by Flags]****[!UICONTROL Profanity]** 확인란을 선택합니다. 선택한 사이트나 네트워크에 대한 비속어 필터에 의해 포착된 모든 컨텐츠가 표시됩니다. 이 목록에는 Socialsync 및 스트림을 사용하여 앱에 가져온 컨텐츠가 포함됩니다.

Studio Select **[!UICONTROL Settings > Network Settings > Moderation]**에서 미리 중재 규칙을 만들려면 비속어 필터가 활성화되면 새 규칙이 나타나므로 모독 컨텐츠가 포함된 컨텐츠를 플래그를 지정하거나 미리 조정할 수 있습니다. 기본적으로 이 규칙은 Profane 컨텐츠에 **[!UICONTROL Premoderate]** 자동으로 적용되며, 이 규칙은 **[!UICONTROL Trash it]** OR **[!UICONTROL Bozo it]**로 변경될 수 있습니다.

>[!NOTE]
>
>컨텐츠가 여러 규칙 유형 (예: 안전 및 플래그 규칙 모두) 의 적용을 받는 경우 더 엄격한 규칙이 적용됩니다. 예를 들면 다음과 같습니다. 중재 규칙에 컨텐츠가 미리 중재된다고 명시되어 있지만, 보호 규칙을 통해 휴지통을 버리는 경우, 이것은 트윗됩니다.

## 네트워크에 대한 비속어 목록 보기 및 업데이트 {#section_qdb_btk_f1b}

1. **[!UICONTROL Settings > Network Settings > Moderation]**이동.
1. **[!UICONTROL Profanity List]** 섹션으로 스크롤합니다.
1. [ **[!UICONTROL Enable Profanity Checking]** 으로 **[!UICONTROL On]** 설정] 를 클릭하여 네트워크에 대해 활성화된 목록 (Livefyre 기본값 또는 업로드된 사용자 정의 목록) 를 표시하고 편집합니다. 다음 방법으로 목록을 편집할 수 있습니다.
   * 단어를 제거하려면 단어를 클릭합니다.
   * 단어를 추가하려면 **[!UICONTROL Add new word]** 상자에 단어를 입력합니다 **[!UICONTROL Return]**.
   * 단어가 목록에 포함되어 있는지 확인하려면 **[!UICONTROL Test profanity filter]** 상자에 단어를 입력합니다.

>[!NOTE]
>
>스튜디오 관리자와 중재자만 비속어 목록을 편집할 수 있습니다.

