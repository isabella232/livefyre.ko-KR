---
description: null
seo-description: null
seo-title: 필름스트립 사용자 정의
solution: Experience Manager
title: 필름스트립 사용자 정의
uuid: 99 F 8 B 697-4 AA 3-4813-BCAC-D 0 E 0 BDEE 252 D
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 필름스트립 사용자 정의{#filmstrip-customizations}

모든 앱 사용 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션 **[!UICONTROL App Designer]**. 앱의 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 **[!UICONTROL App Designer.]**

App Designer에서 다음 추가 옵션을 사용하여 필름스트립을 사용자 정의할 수 있습니다.

* **[!UICONTROL Content fit]**. 전체 **[!UICONTROL crop]** 카드가 가득 찼는지 여부에 상관없이 카드를 채우거나 **[!UICONTROL Aspect Ratio]** 카드에 전체 이미지를 표시하려면 컨텐츠를 자릅니다.
* **[!UICONTROL Tile Size]**. 타일 크기 (픽셀 단위) 를 입력합니다.
* **[!UICONTROL Show Notifications]**. 필름스트립 앱에 스트리밍될 때 새 컨텐츠에 대한 알림을 표시할지 여부를 선택합니다.
* **[!UICONTROL Require rights]**. Rights Request 상태가 "Granted" 인 컨텐츠만 표시하려면 이 옵션을 활성화합니다.
* **[!UICONTROL Hide social branding when rights granted]** 컨텐츠에 대한 권한이 부여될 때 원래 소셜 미디어 네트워크 (Twitter 또는 Instagram) 에 대한 로고를 제거하도록 켭니다.
* **[!UICONTROL Call-to-action button]** 제품 카탈로그가 있는 클릭유도문안 단추를 사용하여 추가 작업을 위해 제품 또는 사이트로 이동할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환 스위치를 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 컨텐츠에 대한 클릭유도문안 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하려면 전환 스위치를 켬으로 전환합니다.

      >[!NOTE]
      >
      >컨텐츠에 대한 권한이 부여되지 않더라도 컨텐츠가 표시되지만, 컨텐츠에 대한 권한이 부여되지 않으면 클릭유도문안 버튼이 컨텐트와 함께 표시되지 않습니다.

   * **[!UICONTROL Show call-to-action in tile]**. 사이트 방문자가 카드를 클릭하고 더 큰 창에서 해당 컨텐츠를 열 때에만 클릭유도문안 단추를 표시하는 대신 필름스트립 타일에 클릭유도문안 단추를 표시할지 여부를 선택합니다.
   * **[!UICONTROL Call-to-action indication text]** 표시할 텍스트를 표시할 텍스트입니다.
   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위의 헤더에 표시할 단어입니다. 기본 텍스트는 "다음 제품: ".
   * **[!UICONTROL Call-to-action button text]** 컨텐츠 모달 내의 클릭유도문안 단추에 표시할 단어입니다. 기본 텍스트는 "지금 구입: ".
   * **[!UICONTROL Product display options]** 클릭유도문안 단추를 **[!UICONTROL Photo]** 표시할지 **[!UICONTROL Product name]** 여부를 선택합니다.

      >[!NOTE]
      >
      >사진 및 제품 이름 단추가 활성화되면 파란색으로 강조 표시됩니다.

   * **[!UICONTROL Product URL referral tracking]** 전환 스위치를 켜짐으로 전환하여 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 앱 컨텐츠의 참조 추적을 관련 제품 페이지로 더 지정하려면 매개 변수를 추가합니다.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 여러 제품 페이지에 대해 하나의 앱을 만들려면 이 옵션을 선택합니다. 제품별 UGC를 각 제품 페이지에 대한 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select product folders]**. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. CTRL/Command 키를 누른 상태에서 두 개 이상의 폴더를 선택합니다. Livefyre는 폴더를 사용하여 다양한 페이지에서 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]**. 앱에 게시되었지만 다른 제품 ID로 태그가 지정된 콘텐츠를 표시하려면 이 옵션을 전환합니다. 앱별 콘텐츠가 표시되면 Livefyre는 제품과 연결되지 않은 다른 제품 및 컨텐트에 대한 컨텐츠를 표시합니다. Livefyre는 동일한 제품 ID로 콘텐츠를 우선 순위화한 다음 다른 제품 ID로 앱에 게시한 다음 제품 ID 없이 앱에 게시되는 콘텐츠를 우선 순위를 매깁니다.

livefyre. js를 사용하여 필름스트립을 사용자 지정하는 방법에 대한 자세한 내용은 [필름스트립 옵션을](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) 참조하십시오.

