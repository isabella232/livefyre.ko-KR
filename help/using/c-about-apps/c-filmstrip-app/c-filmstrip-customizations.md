---
title: 필름스트립 사용자 지정
description: 필름스트립 사용자 지정
exl-id: 2765699f-7adc-4b17-acfb-ef594ff65e89
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 필름스트립 사용자 지정{#filmstrip-customizations}

모든 앱은 **[!UICONTROL App Designer]**&#x200B;에서 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션을 사용합니다. **[!UICONTROL App Designer.]**&#x200B;의 모든 앱에 대한 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 앱 맞춤화를 참조하십시오.

앱 디자이너의 다음 추가 옵션을 사용하여 필름스트립을 사용자 정의할 수 있습니다.

* **[!UICONTROL Content fit]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 카드를 채울 콘텐트를 자르려면 **[!UICONTROL crop]**, 카드 전체에 칠하든 말든 카드에 전체 이미지를 표시하려면 **[!UICONTROL Aspect Ratio]** 을 선택합니다.
* **[!UICONTROL Tile Size]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 타일 크기를 픽셀 단위로 입력합니다.
* **[!UICONTROL Show Notifications]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 새 콘텐츠에 대한 알림을 필름스트립 앱으로 스트리밍할 때 표시할지 여부를 선택합니다.
* **[!UICONTROL Require rights]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 권한 요청 상태가 &quot;부여됨&quot;인 컨텐츠만 표시하려면 이 옵션을 활성화합니다.
* **[!UICONTROL Hide social branding when rights granted]** 컨텐트에 대한 권한이 부여될 때 원래 소셜 미디어 네트워크(Twitter 또는 Instagram)에 대한 로고를 제거하려면 이 옵션을 활성화합니다.
* **[!UICONTROL Call-to-action button]** 제품 카탈로그의 클릭유도문안 단추를 사용하여 사용자에게 제품 또는 사이트로 안내하여 추가 작업을 수행할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환을 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 콘텐츠에 대한 클릭유도문안 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하도록 전환하려면 이 전환을 켜십시오.

      >[!NOTE]
      >
      >컨텐츠는 컨텐츠에 대한 권한이 부여되지 않은 경우에도 표시되지만, 컨텐츠에 대한 권한이 부여되지 않으면 클릭유도문안 단추가 컨텐츠와 함께 표시되지 않습니다.

   * **[!UICONTROL Show call-to-action in tile]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 사이트 방문자가 카드를 클릭하고 더 큰 창에서 콘텐트를 열 때만 클릭유도문안 단추를 표시하는 대신 필름스트립 타일에 클릭유도문안 단추를 표시할지 여부를 선택합니다.
   * **[!UICONTROL Call-to-action indication text]** 사용자에게 클릭 유도 문안 양식을 열 수 있도록 카드를 표시하는 텍스트입니다.
   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위에 머리글에 표시할 단어입니다. 기본 텍스트는 &quot;Shop these products:&quot;입니다.
   * **[!UICONTROL Call-to-action button text]** 컨텐츠 모달에서 클릭유도문안 단추에 표시할 단어입니다. 기본 텍스트는 &quot;지금 구입:&quot;입니다.
   * **[!UICONTROL Product display options]** 클릭유도문안 단추 **[!UICONTROL Photo]** 와 함께 표시 **[!UICONTROL Product name]** 를 표시할지 여부를 선택합니다.

      >[!NOTE]
      >
      >사진 및 제품 이름 단추가 활성화되면 파란색으로 강조 표시됩니다.

   * **[!UICONTROL Product URL referral tracking]** 전환을 켜서 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 매개 변수를 추가하여 앱 컨텐츠에서 관련 제품 페이지로 참조 추적을 추가로 지정합니다.

* **[!UICONTROL Embed App in multiple pages]**&#x200B;를 참조하십시오.

   * **[!UICONTROL Filter UGC by Product ID]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 여러 제품 페이지에 하나의 앱을 만들려면 이 옵션을 선택합니다. 각 제품 페이지에 대해 제품별 UGC를 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select product folders]** 구문을 사용하는 키-값 쌍으로 전달됩니다. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. 둘 이상의 폴더를 선택하려면 Ctrl/Command + 클릭을 사용합니다. Livefyre는 폴더를 사용하여 다양한 페이지의 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 앱에 게시되었지만 다른 제품 ID로 태그가 지정된 컨텐츠를 표시하려면 이 설정을 전환합니다. 앱의 제품별 콘텐츠가 표시되면 Livefyre가 다른 제품의 콘텐츠와 제품과 연관되지 않은 콘텐츠를 표시합니다. Livefyre는 먼저 동일한 제품 ID로 콘텐츠를 우선 배치하고, 다른 제품 ID를 사용하여 앱에 게시된 콘텐츠를 제품 ID가 없는 앱에 게시했습니다.

Livefyre.js를 사용하여 필름스트립을 사용자 지정하는 방법에 대한 자세한 내용은 [필름스트립 옵션](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)을 참조하십시오.
