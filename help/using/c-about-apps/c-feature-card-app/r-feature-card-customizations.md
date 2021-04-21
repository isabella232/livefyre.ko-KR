---
description: 맵 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.
title: 기능 카드 사용자 정의
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 기능 카드 사용자 지정{#feature-card-customizations}

맵 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.

<!-- 
r_feature_card_customization.dita
 -->

기능 카드 앱은 표준 사용자 지정 사항:** [!UICONTROL Theme]**, 브랜드 색상, 글꼴 모음 및 글꼴 크기만 포함합니다.

다음을 사용하여 기능 카드를 사용자 정의할 수 있습니다.

* **[!UICONTROL Style]** 및  **[!UICONTROL Config]** 옵션  **[!UICONTROL App Designer]**&#x200B;사용 **[!UICONTROL App Designer]**&#x200B;의 모든 앱에 대한 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 앱 맞춤화를 참조하십시오.

* 통합 툴. 통합 도구를 사용하여 앱을 사용자 정의하는 방법에 대한 자세한 내용은 앱 통합을 참조하십시오.
* **[!UICONTROL Call-to-action button]** 제품 카탈로그의 클릭유도문안 단추를 사용하여 사용자에게 제품 또는 사이트로 안내하여 추가 작업을 수행할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환을 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 콘텐츠에 대한 [클릭유도문안] 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하도록 전환하려면 이 전환을 켜십시오.

      >[!NOTE]
      >
      >컨텐츠는 컨텐츠에 대한 권한이 부여되지 않은 경우에도 표시되지만, 컨텐츠 권한이 부여되지 않으면 클릭유도문안 단추가 컨텐츠와 함께 표시되지 않습니다.

   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위에 머리글에 표시할 단어. 기본 용어는 &quot;Shop these products:&quot;입니다.
   * **[!UICONTROL Call-to-action button text]** 클릭유도문안 단추의 텍스트를 사용자 정의합니다. 기본 텍스트는 &quot;지금 구입&quot;입니다.
   * **[!UICONTROL Product display options]** 클릭유도문안 단추 **[!UICONTROL Photo]** 와  **[!UICONTROL Product name]** 함께 표시할 항목을 선택합니다.
   * **[!UICONTROL Product URL referral tracking]** 전환을 켜서 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 매개 변수를 추가하여 앱 컨텐츠에서 관련 제품 페이지로 참조 추적을 추가로 지정합니다.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 여러 제품 페이지에 하나의 앱을 만들려면 이 옵션을 선택합니다. 각 제품 페이지에 대해 제품별 UGC를 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select Product folders]** 구문을 사용하는 키-값 쌍으로 전달됩니다. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. 둘 이상의 폴더를 선택하려면 `CTRL/Command + click`을 사용합니다. Livefyre는 폴더를 사용하여 다양한 페이지의 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 앱에 게시되었지만 다른 제품 ID로 태그가 지정된 컨텐츠를 표시하려면 이 설정을 전환합니다. 앱의 제품별 콘텐츠가 표시되면 Livefyre가 다른 제품의 콘텐츠와 제품과 연관되지 않은 콘텐츠를 표시합니다. Livefyre는 먼저 동일한 제품 ID로 콘텐츠를 우선 배치하고, 다른 제품 ID를 사용하여 앱에 게시된 콘텐츠를 제품 ID가 없는 앱에 게시했습니다.
