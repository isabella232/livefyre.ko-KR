---
description: 권한 요청 작동 방식을 살펴볼 수 있습니다. 사용자가 생성한 콘텐츠 (UGC) 를 Livefyre 앱으로 가져오면 컨텐츠에
  무제한의 재사용이 포함됩니다. Twitter 또는 Instagram에서 컨텐트를 사용하려면 작성자의 허가가 있어야 합니다.
seo-description: 권한 요청 작동 방식을 살펴볼 수 있습니다. 사용자가 생성한 콘텐츠 (UGC) 를 Livefyre 앱으로 가져오면 컨텐츠에
  무제한의 재사용이 포함됩니다. Twitter 또는 Instagram에서 컨텐트를 사용하려면 작성자의 허가가 있어야 합니다.
seo-title: 권한 요청
title: 권한 요청
uuid: d 3194 afa-f 3 c 6-44 ed-b 03 f -9 b 1 ecb 50 c 1 d 3
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 권한 요청{#requesting-rights}

권한 요청 작동 방식을 살펴볼 수 있습니다. 사용자가 생성한 콘텐츠 (UGC) 를 Livefyre 앱으로 가져오면 컨텐츠에 무제한의 재사용이 포함됩니다. Twitter 또는 Instagram에서 컨텐트를 사용하려면 작성자의 허가가 있어야 합니다.

라이브러리, 앱 컨텐츠, MODQ 및 AEM 상거래에서 다음 권한 상태를 사용할 수 있습니다.

* **[!UICONTROL Granted]**. 작성자가 컨텐트를 재사용할 권한을 부여하면 자산의 상태가 변경됩니다 **[!UICONTROL Granted]**.

* **[!UICONTROL Expired]**. Livefyre는 14 일 동안 작성자의 답글을 위해 Instagram와 Twitter 스트림을 모니터링합니다. 14 일 후 요청이 만료되고 Rights Request 상태가로 **[!UICONTROL Expired]**변경되고 두 번째 요청을 보내거나 라이브러리에서 항목을 제거할 수 있습니다.
* **[!UICONTROL Requested]**. 라이브러리의 콘텐트에 대한 권한을 요청합니다. 한 번에 하나 이상의 자산에 대해 이 작업을 수행할 수 있습니다. 권한 요청 후 Livefyre는 자산 상태를로 **[!UICONTROL Requested]**설정합니다.
* **[!UICONTROL Needs Review]**. 작성자가 # Approvalhashtag를 포함하지 않는 메모로 답글을 달 경우 자산의 상태가 변경됩니다 **[!UICONTROL Needs Review]**.

* **[!UICONTROL Request Failed]**. 요청을 보내지 못했습니다 (토큰 만료 때문).
* **[!UICONTROL Request Pending]**. 한 번에 너무 많지 않도록 권한 요청을 큐에 넣습니다.

Twitter 및 Instagram에서 취득한 자산에 대한 권한을 요청할 수 있습니다. 권한을 요청하려면 라이브러리에 에셋을 저장해야 합니다.

부분적으로 자동화된 워크플로우를 사용하여 Instagram의 자산에 대한 권한을 요청하려면 *Instagram 비즈니스 계정을* 구성해야 합니다.

귀하는 비즈니스 계정별 검색 또는 스트림 검색에서 취득한 콘텐트에 대해서만 이 기능을 사용할 수 있습니다. 개인 Instagram 계정에서 구입한 콘텐츠에 대한 권한을 요청하려면 권한 요청을 수동으로 전송해야 합니다.

>[!NOTE]
>
>다른 종류의 Instagram 계정 및 사용 방법에 대한 자세한 내용은 Instagram 계정 [정보를](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)참조하십시오. Instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 수동 권한 요청 [전송을 참조하고](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) 부분적으로 자동화된 권한 요청 [전송을 참조하십시오](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library).

