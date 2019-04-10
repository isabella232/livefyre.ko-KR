---
description: 맵 앱의 크기, 너비 및 상호 작용 옵션을 변경합니다.
seo-description: 맵 앱의 크기, 너비 및 상호 작용 옵션을 변경합니다.
seo-title: 기능 카드 사용자 정의
solution: Experience Manager
title: 기능 카드 사용자 정의
uuid: DD 43 C 076-027 F -42 C 8-BE 2 E -7 D 863 D 4 E 3976
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 기능 카드 사용자 정의{#feature-card-customizations}

맵 앱의 크기, 너비 및 상호 작용 옵션을 변경합니다.

<!-- 
r_feature_card_customization.dita
 -->

Feature Card 앱은 표준 사용자 정의만 포함합니다. ** [!UICONTROL Theme]**, 브랜드 색상, 글꼴 모음 및 글꼴 크기가 있습니다.

다음을 사용하여 기능 카드를 사용자 정의할 수 있습니다.

* **[!UICONTROL Style]** and **[!UICONTROL Config]** options for all apps in the **[!UICONTROL App Designer]**. 의 모든 앱에 대한 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 앱 맞춤화를 참조하십시오 **[!UICONTROL App Designer]**.

* 통합 도구. 통합 도구를 사용하여 앱을 맞춤화하는 방법에 대한 자세한 내용은 앱 통합을 참조하십시오.
* **[!UICONTROL Call-to-action button]** 제품 카탈로그가 있는 클릭유도문안 단추를 사용하여 추가 작업을 위해 제품 또는 사이트로 이동할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환 스위치를 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 컨텐츠에 대한 클릭유도문안 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하려면 전환 스위치를 켬으로 전환합니다.

      >[!NOTE]
      >
      >컨텐츠에 대한 권한이 부여되지 않더라도 컨텐츠가 표시되지만, 컨텐츠에 대한 권한이 부여되지 않으면 클릭유도문안 버튼이 컨텐트와 함께 표시되지 않습니다.

   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위의 헤더에 표시할 단어입니다. 기본 용어는 "다음 제품: ".
   * **[!UICONTROL Call-to-action button text]** 클릭유도문안 단추의 텍스트를 사용자 정의합니다. 기본 텍스트는 "지금 구입" 입니다.
   * **[!UICONTROL Product display options]** 클릭유도문안 단추를 **[!UICONTROL Photo]** 표시할지 **[!UICONTROL Product name]** 여부를 선택합니다.
   * **[!UICONTROL Product URL referral tracking]** 전환 스위치를 켜짐으로 전환하여 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 앱 컨텐츠의 참조 추적을 관련 제품 페이지로 더 지정하려면 매개 변수를 추가합니다.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. 여러 제품 페이지에 대해 하나의 앱을 만들려면 이 옵션을 선택합니다. 제품별 UGC를 각 제품 페이지에 대한 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select Product folders]**. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. 둘 `CTRL/Command + click` 이상의 폴더를 선택하는 데 사용합니다. Livefyre는 폴더를 사용하여 다양한 페이지에서 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]**. 앱에 게시되었지만 다른 제품 ID로 태그가 지정된 콘텐츠를 표시하려면 이 옵션을 전환합니다. 앱별 콘텐츠가 표시되면 Livefyre는 제품과 연결되지 않은 다른 제품 및 컨텐트에 대한 컨텐츠를 표시합니다. Livefyre는 동일한 제품 ID로 콘텐츠를 우선 순위화한 다음 다른 제품 ID로 앱에 게시한 다음 제품 ID 없이 앱에 게시되는 콘텐츠를 우선 순위를 매깁니다.

