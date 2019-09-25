---
description: Instagram에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Instagram에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Instagram 규칙
title: Instagram 규칙
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Instagram 규칙{#instagram-rules}

Instagram에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

>[!NOTE]
>
>Instagram 스트림을 만들려면 먼저 Instagram 비즈니스 계정을 하나 이상 의 **[!UICONTROL Social Accounts]** 섹션에 추가해야 합니다 **[!UICONTROL Network Settings]**. Instagram 계정을 구성하는 방법에 대한 자세한 내용은 Instagram 계정 [정보를 참조하십시오](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

@mentions 또는 해시 태그를 기반으로 Instagram 규칙을 만듭니다.

>[!NOTE]
>
>모든 Instagram 규칙에는 해시 태그가 하나 이상 필요합니다. 키워드와 규칙에 대한 사용자 이름을 추가하면 두 항목을 모두 포함하는 컨텐츠가 반환됩니다.

Instagram 피드에서 Instagram 피드의 콘텐츠를 앱 또는 폴더로 가져오려면 다음을 기준으로 필터링합니다.

* **[!UICONTROL Words]**

   * Instagram 스트림에 **[!UICONTROL hashtags]** 포함하거나 제외할 항목을 입력합니다. 및 **[!UICONTROL Contains]** 필드 모두에 대한 값을 지정하면 첫 번째 **[!UICONTROL Does not contain]** 필드를 포함하고 두 번째 이미지를 포함하지 않는 이미지가 반환됩니다.

   * 예를 들어 Giants, **[!UICONTROL Contains]** Posey 및 **[!UICONTROL Does not contain]** 키워드 Dodger 키워드를 입력하면 Giants 또는 Posey라는 단어가 포함된 모든 게시물이 반환되고 Dazers라는 단어는 포함되지 않습니다.

      >[!NOTE]
      >
      >Instagram Rules는 작성자의 댓글에 나열된 해시태그를 포함하는 게시물을 반환하며 이는 스트림에 나타나지 않을 수 있습니다.

* **[!UICONTROL Mentions]**

   * Enter **[!UICONTROL @mentions]** 키를 눌러 스트림으로 가져오거나 스트림에서 제외합니다.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Instagram 스트림 규칙에서 작성자 검색을 사용하려면 Livefyre에 Instagram 비즈니스 계정이 설정되어 있어야 합니다. Livefyre에서 Instagram 비즈니스 계정을 설정하는 방법에 대한 자세한 내용은 Instagram 계정 [정보를 참조하십시오](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Enter **[!UICONTROL @usernames]** 키를 눌러 스트림으로 들어갑니다. @username **과** 연결된 계정은 Instagram 비즈니스 계정이어야 합니다.

   * 스트림에서 제외할 **@usernames** 를 입력합니다.

* **[!UICONTROL Additional Filters]**

   * 스트림에 포함할지, **[!UICONTROL All Content]****[!UICONTROL Videos Only]**&#x200B;또는 **[!UICONTROL Photos Only]** 포함할지 여부를 선택합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 [규칙에 대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
