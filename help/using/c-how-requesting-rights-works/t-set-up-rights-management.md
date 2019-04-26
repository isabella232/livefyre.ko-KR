---
description: Instagram 및 Twitter 게시물에 대한 권한 요청 설정을 정의합니다.
seo-description: Instagram 및 Twitter 게시물에 대한 권한 요청 설정을 정의합니다.
seo-title: 권한 관리 설정
solution: Experience Manager
title: 권한 관리 설정
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 권한 관리 설정{#set-up-rights-management}

Instagram 및 Twitter 게시물에 대한 권한 요청 설정을 정의합니다.

권한 요청 설정을 정의하려면 먼저 Instagram 또는 Twitter에 대해 하나 이상의 소셜 계정을 구성해야 합니다. Social 계정을 구성하는 방법에 대한 자세한 내용은 Social 계정 [추가를](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)참조하십시오.

>[!NOTE]
>
>권한 관리는 네트워크 수준에서만 구성할 수 있습니다. 사이트별 권한 관리는 구성할 수 없습니다.

1. Livefyre Studio에서 **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**로 이동합니다.

   >[!NOTE]
   >
   >권한 관리 계정을 설정하려면 중재자 또는 관리자 네트워크 수준 권한이 필요합니다.

1. 권한 관리 계정이 설정되어 있지 **[!UICONTROL +Add New Account]** 않은 경우 선택합니다.
1. Rights Management에 사용할 소셜 네트워크를 **[!UICONTROL Create New Setting]** 클릭합니다.

   >[!NOTE]
   >
   >Instagram 계정의 경우 부분 자동화를 통해 권한을 요청하려면 Instagram 비즈니스 계정이 있어야 합니다. 다른 종류의 Instagram 계정 및 사용 방법에 대한 자세한 내용은 Instagram 계정 [정보를](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)참조하십시오.

1. 표시된 필드를 채웁니다. 모든 필드는 필수입니다.

   * **[!UICONTROL Display name:]** 권한 요청 계정에 사용할 Twitter 또는 Instagram 계정을 식별하는 표시 이름을 입력합니다. 이 이름은 내부에서만 사용됩니다.
   * ****[!UICONTROL Enabled:]기본적으로 켜짐으로 설정됩니다. 계정에 대한 권한 관리를 활성화합니다.
   * **[!UICONTROL Approval hashtag:]** 컨텐츠 소유자가 컨텐츠 사용에 동의함을 나타내는 데 사용할 해시 태그입니다.
   * **[!UICONTROL Terms and conditions:]** 컨텐트의 재사용에 대한 네트워크의 약관 링크. 이 필드는 대/소문자를 구분합니다.
   * **[!UICONTROL Network and sites:]** 이 계정이 컨텐츠 재사용을 요청할 수 있는 네트워크 또는 사이트입니다. 이 계정을 전체 네트워크에서 사용할 수 있게 하려면 목록에서 첫 번째 항목을 선택하거나 Command/CTRL 키를 사용하여 특정 사이트로 제한합니다.
   * **[!UICONTROL Default message:]** 권한 요청과 함께 표시할 메시지입니다. 권한을 요청할 때 이 메시지를 무시할 수 있습니다.

      * 중재자가 컨텐츠 작성자에게 요청을 제기할 때 Livefyre는 중재자에게 기본 메시지 중 하나를 제공합니다. 중재자는 보내기 전에 다른 기본 메시지를 생성하거나 메시지를 편집할 수 있습니다. 메시지에는 작성자의 Twitter 또는 Instagram 핸들 ({handle}), 승인 해시 태그 ({granttag}) 및 약관 링크 ({termslink}) 가 포함되어야 합니다.

         **[!UICONTROL Note:]** {handle}, {granttag} 및 {termslink} 는 모두 대/소문자를 구분합니다.

         **[!UICONTROL Note:]** 악의적인 사용을 방지하기 위해 Twitter는 포함된 모든 URL를 [t. co](https://t.co/) 형식으로 래핑합니다. 기본 메시지가 140 자를 초과하지 않도록 기본 메시지의 URL를 포함하는 것이 좋습니다.

      * 권한 요청 메시지 작성을 위한 우수 사례:

         * 로봇이 아닌 여러 개의 기본 메시지를 만들 수 있습니다. 다음 기본 메시지를 만들기 전에 각 기본 메시지를 저장합니다.
         * 중재자가 발송하기 전에 이 메모를 개인화하여 네트워크의 요청에 스팸 태그가 지정되지 않도록 합니다.

1. Rights **[!UICONTROL Save Settings]** Request 계정을 추가하려면을 클릭합니다.
자산 라이브러리에서 권한 요청을 보냅니다. 자산 [라이브러리에서 권한 요청을 보내는 방법에 대한 자세한 내용은 권한 요청](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) 전송을 참조하십시오.