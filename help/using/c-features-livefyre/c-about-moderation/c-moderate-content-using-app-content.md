---
description: 라이브러리의 앱 콘텐츠 탭에서는 앱 전체에 게시된 콘텐츠를 중재할 수 있습니다.
seo-description: 라이브러리의 앱 콘텐츠 탭에서는 앱 전체에 게시된 콘텐츠를 중재할 수 있습니다.
seo-title: 앱 콘텐츠를 사용하여 콘텐츠 중재
title: 앱 콘텐츠를 사용하여 콘텐츠 중재
uuid: 1c648128-e7ef-4836-afe5-eff52de30e7e
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# 앱 콘텐츠{#moderate-content-using-app-content}를 사용하여 콘텐츠 중재

라이브러리의 앱 콘텐츠 탭에서는 앱 전체에 게시된 콘텐츠를 중재할 수 있습니다.

## 콘텐트 {#section_md5_sqm_zz} 중재

앱 콘텐츠 패널을 사용하여 상태를 변경하거나 작성자의 상태를 변경하거나 메모를 추가하여 나열된 콘텐츠를 중재할 수 있습니다. 컨텐츠를 중재하려면 나열된 컨텐츠 위로 마우스를 가져가 사용 가능한 마커를 변경하거나 **[!UICONTROL pulldown]** 메뉴를 사용하여 개별 또는 여러 개의 선택한 컨텐츠의 상태를 변경합니다.

![](assets/PublishedActionsMenu-1024x402.png)

앱 컨텐츠에서 다음 작업을 수행할 수 있습니다.

* **[!UICONTROL Tag Content]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 개별 또는 여러 콘텐트에 동시에 태그를 추가하려면 **[!UICONTROL Tag Content]**&#x200B;을 선택합니다.

* **[!UICONTROL Ignore Flags]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 플래그가 지정된 검색 필터 결과에서 선택한 컨텐츠를 제외하려면 **[!UICONTROL Ignore Flags]**&#x200B;을 선택합니다. 항목에 대해 **[!UICONTROL Ignore Flags]**&#x200B;을 선택해도 상태가 변경되지 않습니다.모든 Studio 사용자의 경우 앞으로 이 검색 필터의 검색 결과에서 이 필터를 제거합니다.

* **[!UICONTROL Change Content Status]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 콘텐트를 클릭한 다음 **[!UICONTROL Actions]** 메뉴를 사용하여 상태를 변경합니다. Command 키 또는 Ctrl 키를 사용하여 여러 항목을 선택한 다음 메뉴를 사용하여 여러 콘텐트의 상태를 동시에 변경합니다.

   옵션은 나열된 내용의 현재 상태에 따라 달라집니다.

   | 현재 상태 | 변경 대상: |
   |---|---|
   | 승인됨 | 보류 중, 휴지통, 보조 |
   | 보조 | 승인됨, 보류 중, 휴지통 |
   | 휴지통 | 승인됨, 보류 중, Bozo, 삭제 |
   | 대기 중 | 승인, 휴지통, Bozo |

* **[!UICONTROL Save as Assets]** 구문을 사용하는 키-값 쌍으로 전달됩니다. **[!UICONTROL Save as Assets]**&#x200B;을 선택하여 선택한 항목을 자산 라이브러리에 저장, 앱에 게시 또는 작성자의 재사용 권한을 요청할 수 있는 고급 옵션 대화 상자를 엽니다.

* 권장 사항을 기반으로 중재합니다. 앱 콘텐츠의 **[!UICONTROL Moderation Recommendation Indicator]**&#x200B;을 사용하여 중재 권장 사항이 해시될 가능성이 있다고 판단되는 컨텐츠를 필터링합니다.

   앱 컨텐츠에서 중재 권장 사항은 다음과 같습니다. ![](assets/modreco3.png)

## 사이드노트 컨텐트 중재 {#section_i2s_nqm_zz}

[컨텐트] 패널에서 사이드노트를 사용하는 것은 다음과 같은 여러 가지 방법으로 다른 유형의 컨텐츠와 작업하는 것과는 다릅니다.

* 추가 정보, 답글, 플래그 및 보고서 및 메모 추가 탭을 사용할 수 없습니다.
* 사이드노트에 태그를 지정하거나 [특집]으로 표시할 수는 없습니다.

중재할 컨텐츠만 표시하는 것은 아닙니다.또한 사이드노트가 추가될 때 선택한 텍스트를 표시하여 컨텍스트에서 컨텐츠를 평가할 수 있습니다.

![](assets/SidenotesContent.png)

사용자가 선택한 인용 부호 전체를 포함하도록 확장하려면 텍스트 상자를 클릭합니다.

사이드노트 컨텐츠 중재는 위에서 설명한 대로 일괄 변경과 개별 상태 변경을 모두 허용합니다.

## Livefyre 사용자 중재 {#section_grw_mqm_zz}

Livefyre 사용자가 풀다운 메뉴를 열 수 있도록 Livefyre 사용자 이름 위에 마우스를 놓으면 **[!UICONTROL Ban the User]**, **[!UICONTROL More Info]** 또는 **[!UICONTROL Comments]** 목록을 볼 수 있습니다. 이 메뉴를 클릭하면 Studio의 **[!UICONTROL Users]** 페이지에 사용자 정보 카드가 열립니다.

**[!UICONTROL Users]** 페이지에서 사용자를 중재하는 방법에 대한 자세한 내용은 [사용자 ModQ 중재](/help/using/c-features-livefyre/c-about-moderation/t-moderate-users-modq.md#t_moderate_users_modq)를 참조하십시오.
