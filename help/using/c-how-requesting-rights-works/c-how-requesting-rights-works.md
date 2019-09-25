---
description: 권한 요청이 작동하는 방식을 알아봅니다. 사용자 생성 콘텐츠(UGC)를 Livefyre 앱으로 가져오면 컨텐츠에 재사용 권한이 포함됩니다. Twitter 또는 Instagram의 컨텐츠를 사용하려면 작성자의 권한이 있어야 합니다.
seo-description: 권한 요청이 작동하는 방식을 알아봅니다. 사용자 생성 콘텐츠(UGC)를 Livefyre 앱으로 가져오면 컨텐츠에 재사용 권한이 포함됩니다. Twitter 또는 Instagram의 컨텐츠를 사용하려면 작성자의 권한이 있어야 합니다.
seo-title: 권한 요청
title: 권한 요청
uuid: d3194afa-f3c6-44ed-b03f-9b1ecb50c1d3
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 권한 요청{#requesting-rights}

권한 요청이 작동하는 방식을 알아봅니다. 사용자 생성 콘텐츠(UGC)를 Livefyre 앱으로 가져오면 컨텐츠에 재사용 권한이 포함됩니다. Twitter 또는 Instagram의 컨텐츠를 사용하려면 작성자의 권한이 있어야 합니다.

라이브러리, 앱 컨텐츠, ModQ 및 AEM Commerce에서 다음 권한 상태를 사용할 수 있습니다.

* **[!UICONTROL Granted]**. 작성자가 컨텐츠를 재사용할 권한을 부여하면 자산의 상태가 로 변경됩니다 **[!UICONTROL Granted]**.

* **[!UICONTROL Expired]**. Livefyre는 Instagram 및 Twitter 스트림을 모니터링하여 14일 동안 작성자의 답변을 확인합니다. 14일 후, 요청이 만료되고 권한 요청 상태가 **[!UICONTROL Expired]**&#x200B;변경되며, 두 번째 요청을 보내거나 라이브러리에서 항목을 제거할 수 있습니다.
* **[!UICONTROL Requested]**. 라이브러리의 콘텐트에 대한 권한을 요청합니다. 한 번에 하나 이상의 자산에 대해 이 작업을 수행할 수 있습니다. 권한을 요청하면 Livefyre가 자산 상태를 로 **[!UICONTROL Requested]**&#x200B;설정합니다.
* **[!UICONTROL Needs Review]**. 작성자가 #approvalHashtag를 포함하지 않는 메모로 답글을 달면 자산의 상태가 **[!UICONTROL Needs Review]**&#x200B;변경됩니다.

* **[!UICONTROL Request Failed]**. 요청을 보내지 못했습니다(만료된 토큰 등으로 인해).
* **[!UICONTROL Request Pending]**. 한 번에 너무 많지 않게 권한 요청을 대기시킵니다.

Twitter 및 Instagram에서 얻은 자산에 대한 권한을 요청할 수 있습니다. 권한을 요청하려면 자산을 라이브러리에 저장해야 합니다.

부분적으로 자동화된 워크플로우를 *사용하여 Instagram에서 자산에 대한 권한을 요청하도록 Instagram 비즈니스 계정을* 구성해야 합니다.

이 기능은 비즈니스 계정에 의한 검색 또는 스트림 검색에서 얻은 컨텐츠에만 사용할 수 있습니다. 개인 Instagram 계정에서 얻은 콘텐츠에 대한 권한을 요청하려면 권한 요청을 수동으로 보내야 합니다.

>[!NOTE]
>
>다양한 종류의 Instagram 계정과 이를 사용하는 방법에 대한 자세한 내용은 Instagram 계정 [정보를 참조하십시오](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts). Instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 수동 권한 요청 [보내기](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) 및 [부분적으로 자동화된 권한 요청 보내기를 참조하십시오](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library).

