---
description: 권한 요청이 작동하는 방법을 알아봅니다. 사용자 생성 콘텐츠(UGC)를 Livefyre 앱으로 가져올 때 콘텐츠에는 재사용 권한이 포함됩니다. twitter 또는 Instagram의 컨텐츠를 사용하려면 작성자의 권한이 있어야 합니다.
title: 권한 요청
exl-id: c709f55b-1773-4de6-82c2-6d3963671095
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 권한 요청{#requesting-rights}

권한 요청이 작동하는 방법을 알아봅니다. 사용자 생성 콘텐츠(UGC)를 Livefyre 앱으로 가져올 때 콘텐츠에는 재사용 권한이 포함됩니다. twitter 또는 Instagram의 컨텐츠를 사용하려면 작성자의 권한이 있어야 합니다.

라이브러리, 앱 컨텐츠, ModQ 및 AEM Commerce에서 다음 권한 상태를 사용할 수 있습니다.

* **[!UICONTROL Granted]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 작성자가 컨텐츠를 재사용할 수 있는 권한을 사용자에게 부여하면 자산의 상태가 **[!UICONTROL Granted]**&#x200B;으로 변경됩니다.

* **[!UICONTROL Expired]** 구문을 사용하는 키-값 쌍으로 전달됩니다. Livefyre는 14일 동안 작성자의 응답을 위해 Instagram 및 Twitter 스트림을 모니터링합니다. 14일이 지나면 요청이 만료되고 권한 요청 상태가 **[!UICONTROL Expired]**&#x200B;으로 변경되며 두 번째 요청을 보내거나 라이브러리에서 항목을 제거할 수 있습니다.
* **[!UICONTROL Requested]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 라이브러리의 콘텐트에 대한 권한을 요청합니다. 한 번에 하나 이상의 자산에 대해 이 작업을 수행할 수 있습니다. 권한을 요청하면 Livefyre가 자산 상태를 **[!UICONTROL Requested]**&#x200B;으로 설정합니다.
* **[!UICONTROL Needs Review]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 작성자가 #approvalHashtag을 포함하지 않는 메모로 답글을 달면, 자산의 상태가 **[!UICONTROL Needs Review]**&#x200B;으로 변경됩니다.

* **[!UICONTROL Request Failed]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 요청을 보내지 못했습니다(만료된 토큰 등으로 인해).
* **[!UICONTROL Request Pending]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 한 번에 너무 많은 수가 전송되지 않도록 권한 요청을 대기시킵니다.

twitter 및 Instagram에서 얻은 자산에 대한 권한을 요청할 수 있습니다. 권한을 요청하려면 자산을 라이브러리에 저장해야 합니다.

부분적으로 자동화된 워크플로우를 사용하여 Instagram의 자산에 대한 권한을 요청하려면 *Instagram 비즈니스 계정*&#x200B;을 구성해야 합니다.

이 기능은 비즈니스 계정으로 검색 또는 스트림 검색을 통해 얻은 컨텐츠에만 사용할 수 있습니다. 개인 Instagram 계정에서 얻은 콘텐츠에 대한 권한을 요청하려면 권한 요청을 수동으로 보내야 합니다.

>[!NOTE]
>
>다양한 유형의 Instagram 계정 및 이를 사용하는 방법에 대한 자세한 내용은 [Instagram 계정 정보](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)를 참조하십시오. instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 [수동 권한 요청 보내기](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) 및 [부분적으로 자동화된 권한 요청 보내기](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library)를 참조하십시오.
