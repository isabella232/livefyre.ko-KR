---
description: 회전판 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.
seo-description: 회전판 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.
seo-title: Studio를 사용하여 회전판 사용자 정의
solution: Experience Manager
title: Studio를 사용하여 회전판 사용자 정의
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Studio를 사용하여 회전판 사용자 정의{#customize-a-carousel-using-studio}

회전판 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.

모든 앱은 의 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션을 사용합니다 **[!UICONTROL App Designer]**. 의 모든 앱에 대한 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 앱 맞춤화를 **[!UICONTROL App Designer]**&#x200B;참조하십시오.

앱 디자이너에서 다음과 같은 추가 옵션을 사용하여 회전판을 사용자 지정할 수 있습니다.

* **[!UICONTROL Max Number of Items]**

   회전판에 표시할 항목 수를 설정합니다. 기본값은 50입니다.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. 컴퓨터 화면만 해당

   * 컨텐츠가 600픽셀보다 크면 가로로 표시됩니다.
   * 컨텐츠가 600픽셀 미만인 경우 세로로 표시됩니다.
   * **수직.** 컴퓨터 화면 또는 모바일 장치의 경우 모바일 장치에서는 카드가 화면 크기에 맞게 축소됩니다.

* **[!UICONTROL Call-to-action button]** 제품 카탈로그의 클릭유도문안 단추를 사용하여 사용자에게 제품 또는 사이트로 안내하여 추가 작업을 수행할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환을 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 컨텐츠에 대한 클릭유도문안 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하도록 전환을 켜짐으로 전환합니다.
   >[!NOTE]
   >
   >컨텐츠는 컨텐츠에 대한 권한이 부여되지 않은 경우에도 표시되지만, 컨텐츠에 대한 권한이 부여되지 않으면 클릭유도문안 단추가 컨텐츠와 함께 표시되지 않습니다.

   * **[!UICONTROL Show call-to-action in tile]**. 사이트 방문자가 카드를 클릭하고 더 큰 창에서 콘텐트를 열 때만 클릭하는 클릭유도문안 단추를 표시하는 대신 타일에 클릭유도문안 단추를 표시할지 여부를 선택합니다.
   * **[!UICONTROL Call-to-action indication text]** 사용자에게 카드를 클릭하여 클릭하도록 하는 메시지를 표시하는 텍스트입니다.
   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위의 머리글에 표시할 단어 기본 텍스트는 "Shop these products:"입니다.
   * **[!UICONTROL Call-to-action button text]** 컨텐츠 모달에서 클릭유도문안 단추에 표시할 단어입니다. 기본 텍스트는 "지금 구입:"입니다.
   * **[!UICONTROL Product display options]** 클릭유도문안 버튼을 표시할 **[!UICONTROL Photo]** 것인지, 클릭유도문안 **[!UICONTROL Product name]** 버튼을 표시할 것인지를 선택합니다.
   >[!NOTE]
   >
   >사진 및 제품 이름 단추가 활성화되면 파란색이 강조 표시됩니다.

   * **[!UICONTROL Product URL referral tracking]** 전환을 켜짐으로 전환하여 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 매개 변수를 추가하여 앱 콘텐츠에서 관련 제품 페이지에 대한 참조 추적을 추가로 지정합니다.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. 여러 제품 페이지에 대해 하나의 앱을 만들려면 이 옵션을 선택합니다. 각 제품 페이지에 대해 제품별 UGC를 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select Product folders]**. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. 두 개 이상의 폴더를 선택하려면 Ctrl/Command + 클릭을 사용합니다. Livefyre는 폴더를 사용하여 다양한 페이지의 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]**. 앱에 게시되었지만 다른 제품 ID로 태그된 콘텐츠를 표시하려면 이 설정을 전환합니다. 앱의 제품별 콘텐츠가 표시되면 Livefyre는 다른 제품의 콘텐츠와 제품과 연결되지 않은 콘텐츠를 표시합니다. Livefyre는 먼저 동일한 제품 ID로 콘텐츠를 우선 적용한 다음 다른 제품 ID로 앱에 게시된 콘텐츠를 제품 ID가 없는 앱에 게시합니다.
