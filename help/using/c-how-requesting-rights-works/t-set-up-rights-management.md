---
description: instagram 및 Twitter 게시물에 대한 권한 요청에 대한 설정을 정의합니다.
title: Rights Management 설정
exl-id: d3d3e837-0ed0-47a8-ac5c-7b9da431d149
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Rights Management 설정{#set-up-rights-management}

instagram 및 Twitter 게시물에 대한 권한 요청에 대한 설정을 정의합니다.

권한 요청 설정을 정의하려면 먼저 Instagram 또는 Twitter에 대해 하나 이상의 소셜 계정을 구성해야 합니다. 소셜 계정 구성 방법에 대한 자세한 내용은 [소셜 계정 추가](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)를 참조하십시오.

>[!NOTE]
>
>네트워크 수준에서만 권한 관리를 구성할 수 있습니다. 사이트별 권한 관리를 구성할 수 없습니다.

1. Livefyre 스튜디오 내에서 **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**&#x200B;로 이동합니다.

   >[!NOTE]
   >
   >Rights Management 계정을 설정하려면 중재자 또는 관리자 네트워크 수준 권한이 필요합니다.

1. 설정된 Rights Management 계정이 없는 경우 **[!UICONTROL +Add New Account]**&#x200B;을 선택합니다.
1. Rights Management에 사용할 소셜 네트워크 아래의 **[!UICONTROL Create New Setting]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >instagram 계정의 경우 일부 자동화를 통해 권한을 요청할 수 있는 Instagram 비즈니스 계정이 있어야 합니다. 다양한 유형의 Instagram 계정 및 이를 사용하는 방법에 대한 자세한 내용은 [Instagram 계정 정보](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)를 참조하십시오.

1. 표시된 필드를 채웁니다. 모든 필드는 필수입니다.

   * **[!UICONTROL Display name:]** 표시 이름을 입력하여 Rights Request 계정에 사용할 Twitter 또는 Instagram 계정을 식별합니다. 이 이름은 내부용입니다.
   * **[!UICONTROL Enabled:]**기본적으로 켜짐으로 설정합니다. 계정에 대한 권한 관리를 활성화합니다.
   * **[!UICONTROL Approval hashtag:]** 컨텐츠 소유자가 컨텐츠 사용에 동의함을 나타내는 데 사용할 해시 태그입니다.
   * **[!UICONTROL Terms and conditions:]** 컨텐츠를 재사용할 수 있도록 네트워크의 약관 링크. 이 필드는 대/소문자를 구분합니다.
   * **[!UICONTROL Network and sites:]** 이 계정이 콘텐츠 재사용 권한을 요청할 수 있는 네트워크 또는 사이트입니다. 전체 네트워크에서 이 계정을 사용할 수 있게 하려면 목록에서 첫 번째 항목을 선택하거나 Command/Ctrl 키를 사용하여 특정 사이트로 제한합니다.
   * **[!UICONTROL Default message:]** 권한 요청과 함께 표시할 메시지입니다. 권한을 요청할 때 이 메시지를 무시할 수 있습니다.

      * 중재자가 컨텐츠 작성자에게 요청을 발행하면 Livefyre는 중재자에게 기본 메시지 중 하나를 제공합니다. 중재자는 보내기 전에 다른 기본 메시지를 생성하거나 메시지를 편집할 수 있습니다. 메시지는 작성자의 Twitter 또는 Instagram 핸들({handle}), 사용자의 승인 해시 태그({grantTag}) 및 약관({termsLink})에 대한 링크를 포함해야 합니다.

         **[!UICONTROL Note:]** {handle}, {grantTag} 및 {termsLink}은 모두 대/소문자를 구분합니다.

         **[!UICONTROL Note:]** 악성 사용을 방지하기 위해 Twitter은 포함된 모든 URL을  [t.](https://t.co/) coformatting으로 래핑합니다. 기본 메시지가 140자를 초과하지 않도록 하려면 기본 메시지에 URL을 포함하지 않는 것이 좋습니다.

      * 권한 요청 메시지를 쓰는 우수 사례:

         * 로봇처럼 들리지 않도록 여러 기본 메시지를 만듭니다. 다음 기본 메시지를 만들기 전에 각 기본 메시지를 저장합니다.
         * 네트워크의 요청이 스팸으로 태그가 지정되지 않도록 중재자가 보내기 전에 이 메모를 개인화하도록 장려합니다.

1. **[!UICONTROL Save Settings]**을 클릭하여 권한 요청 계정을 추가합니다.
자산 라이브러리에서 권한 요청을 보냅니다. 자산 라이브러리에서 권한 요청을 보내는 방법에 대한 자세한 내용은 [권한 요청 보내기](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset)를 참조하십시오.
