---
description: Media Wall 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.
title: 미디어 벽 사용자 지정
exl-id: bc34d8da-9e14-4226-b38d-128889bc31cc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# 미디어 벽 사용자 지정{#media-wall-customizations}

Media Wall 앱의 크기, 폭 및 상호 작용 옵션을 변경합니다.



미디어 벽은 실시간 이미지 및 기타 컨텐츠를 실시간 소셜 담벼락에 스트리밍하여 이벤트를 둘러싼 모든 활동을 시각화합니다.

활성화된 경우 사용자가 텍스트, 이미지 또는 비디오를 이 앱에 직접 게시할 수 있습니다. 지원되는 파일 형식은 다음과 같습니다.

* 이미지:JPEG, GIF, PNG
* 비디오:Quicktime/MOV, MP4, MPEG, WebM
* 오디오:WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   표시되는 컨텐츠 항목의 초기 수를 설정합니다.

* **[!UICONTROL Load content with animation.]** 애니메이션이 있는 페이지에서 미디어 월을 로드하려면 이 옵션을 설정합니다. 애니메이션이 없는 페이지에 미디어 월을 로드하려면 이 옵션을 끕니다.
* **[!UICONTROL Number of columns.]** 미디어 벽의 열 수를 설정합니다. 창 또는 브라우저의 크기와 상관없이 열 수는 동일하게 유지됩니다. [자동]을 선택하면 열 수가 화면 크기에 맞게 최적화된 열 수를 표시하도록 조정됩니다.
* **[!UICONTROL Fit content to width]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 옵션이 꺼져 있으면 내용이 정사각형으로 잘립니다. 전체 카드를 채우는지 여부에 상관없이 이 옵션을 켜서 카드의 전체 이미지를 표시합니다.
* **[!UICONTROL Include content modal]**

   사용자가 스트림에서 사진을 클릭하여 오버레이된 팝업 창에서 열 수 있습니다.

* **[!UICONTROL Require rights]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 권한 요청 상태가 &quot;부여됨&quot;인 컨텐츠만 표시하려면 이 옵션을 활성화합니다.
* **[!UICONTROL Hide social branding when rights granted]** 컨텐트에 대한 권한이 부여될 때 원래 소셜 미디어 네트워크(Twitter 또는 Instagram)에 대한 로고를 제거하려면 이 옵션을 활성화합니다.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 사용자가 업로드 단추와 함께 텍스트, 사진 또는 비디오를 게시하도록 허용할지 여부를 선택합니다.
   * **[!UICONTROL Require Media]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 업로드 단추를 사용하여 사진 또는 비디오 컨텐츠만 업로드하도록 사용자에게 요구하려면 토글을 켜십시오.
   * 다음 업로드 단추 필드에 대한 기본 텍스트를 편집할 수 있습니다.

      * **[!UICONTROL Upload Button Text]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 업로드 단추에 사용할 텍스트입니다. 기본 텍스트는 &quot;무슨 생각입니까?&quot;입니다.
      * **[!UICONTROL Comment Modal Title]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 방문자가 컨텐츠를 게시하는 데 사용하는 모달 사이트 제목입니다. 기본 텍스트는 &quot;댓글 게시&quot;입니다.
      * **[!UICONTROL Comment Modal Button]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 사이트 방문자가 컨텐츠를 게시하기 위해 클릭하는 단추 텍스트. 기본 텍스트는 &quot;댓글 게시&quot;입니다.

* **[!UICONTROL Call-to-action button]** 제품 카탈로그의 클릭유도문안 단추를 사용하여 사용자에게 제품 또는 사이트로 안내하여 추가 작업을 수행할 수 있습니다.

   * **[!UICONTROL Call-to-action button]** 전환을 켜짐으로 전환하여 클릭유도문안 단추를 표시합니다.
   * **[!UICONTROL Require rights to display products]** 콘텐츠에 대한 [클릭유도문안] 단추가 표시되기 전에 컨텐츠 소유자가 컨텐츠에 대한 권한을 부여하도록 전환하려면 이 전환을 켜십시오.

      >[!NOTE]
      >
      >컨텐츠는 컨텐츠에 대한 권한이 부여되지 않은 경우에도 표시되지만, 컨텐츠 권한이 부여되지 않으면 클릭유도문안 단추가 컨텐츠와 함께 표시되지 않습니다.

   * **[!UICONTROL Call-to-action header text]** 컨텐츠 모달에서 클릭유도문안 단추 위에 머리글에 표시할 단어. 기본 용어는 &quot;Shop these products:&quot;입니다.
   * **[!UICONTROL Call-to-action button text]** 컨텐츠 모달의 클릭유도문안 단추에 표시할 단어입니다. 기본 텍스트는 &quot;지금 구입:&quot;입니다.
   * **[!UICONTROL Product display options]** 클릭유도문안 버튼을 사용하여 사진 및 제품 이름을 표시할지 여부를 선택합니다.

      >[!NOTE]
      >
      >사진 및 제품 이름 단추가 활성화되면 파란색으로 강조 표시됩니다.

   * **[!UICONTROL Product URL referral tracking]** 전환을 켜서 이 앱의 참조를 관련 제품 페이지로 추적합니다.
   * **[!UICONTROL Referral tracking key-value pairs]** 매개 변수를 추가하여 앱 컨텐츠에서 관련 제품 페이지로 참조 추적을 추가로 지정합니다.

* **[!UICONTROL Product page filter]**&#x200B;를 참조하십시오.
   * **[!UICONTROL Filter UGC by Product ID]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 여러 제품 페이지에 하나의 앱을 만들려면 이 옵션을 선택합니다. 각 제품 페이지에 대해 제품별 UGC를 앱으로 필터링합니다. 하나 이상의 폴더를 선택하여 특정 컬렉션을 앱에 연결할 수 있습니다.
   * **[!UICONTROL Select Product folders]** 구문을 사용하는 키-값 쌍으로 전달됩니다. UGC를 필터링하는 데 사용할 최상위 제품 폴더를 선택합니다. 둘 이상의 폴더를 선택하려면 Ctrl/Command + 클릭을 사용합니다. Livefyre는 폴더를 사용하여 다양한 페이지의 앱에 표시할 해당 폴더의 제품을 결정합니다.
   * **[!UICONTROL Show related content]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 앱에 게시되었지만 다른 제품 ID로 태그가 지정된 컨텐츠를 표시하려면 이 설정을 전환합니다. 앱의 제품별 콘텐츠가 표시되면 Livefyre가 다른 제품의 콘텐츠와 제품과 연관되지 않은 콘텐츠를 표시합니다. Livefyre는 먼저 동일한 제품 ID로 콘텐츠를 우선 배치하고, 다른 제품 ID를 사용하여 앱에 게시된 콘텐츠를 제품 ID가 없는 앱에 게시했습니다.

다음을 사용하여 미디어 담을 사용자 정의할 수 있습니다.

* **[!UICONTROL Style]** 및  **[!UICONTROL Config]** 옵션  **[!UICONTROL App Designer]**&#x200B;사용 **[!UICONTROL App Designer]**&#x200B;의 모든 앱에 대한 표준 **[!UICONTROL Style]** 및 **[!UICONTROL Config]** 옵션에 대한 자세한 내용은 앱 맞춤화를 참조하십시오.

* 통합 툴. 통합 도구를 사용하여 미디어 담벼락을 사용자 지정하는 방법에 대한 자세한 내용은 [미디어 담벼락 통합](/help/implementation/c-app-integrations/c-media-wall-integration.md)을 참조하십시오.
