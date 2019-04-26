---
description: 이러한 옵션은 모든 소셜 네트워크 또는 게시 메서드의 스트림 규칙에 적용됩니다.
seo-description: 이러한 옵션은 모든 소셜 네트워크 또는 게시 메서드의 스트림 규칙에 적용됩니다.
seo-title: 모든 스트림 규칙에 대한 스트림 규칙 옵션
solution: Experience Manager
title: 모든 스트림 규칙에 대한 스트림 규칙 옵션
uuid: 4072 EE 83-31 E 7-4 DE 6-918 C -134 B 8 B 8032 E 1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# 모든 스트림 규칙에 대한 스트림 규칙 옵션{#stream-rule-options-for-all-stream-rules}

이러한 옵션은 모든 소셜 네트워크 또는 게시 메서드의 스트림 규칙에 적용됩니다.

텍스트 및 키워드 필드에 대한 검색 기능:

* 키워드를 입력할 때 Livefyre는 자동으로 부울 연산자 **또는** 개별 단어를 사용합니다. 예를 들어 *단어 케이크나* *레서피가*있는 게시물을 검색하려면 *케이크를*입력한 다음 필드에 *레서피를 입력합니다***[!UICONTROL keyword]** .

* 정확한 구문 텍스트를 따옴표로 묶어 정확한 구문을 검색할 수 있습니다. 예를 들어 정확히 구문의 *케이크 레시피를*검색하려면 필드에 *"Cake Recipe" 를* **[!UICONTROL keyword]** 입력합니다.

* 부울 및 정확한 구문 검색을 하나의 스트림 규칙에 결합할 수 있습니다. 예를 들어 각 문구를 한 번에 하나씩 입력하여 *케이크*, *레시피*및 *"케이크 레시피"* 를 검색할 수 있습니다.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. 다음 중 하나를 선택합니다.

   * **[!UICONTROL All Content.]** 모든 콘텐츠를 허용합니다.
   * **[!UICONTROL Media Required.]** 이미지와 비디오가 포함된 컨텐츠만 허용 (Instagram 및 Facebook 콘텐츠의 경우, 또는만 지정할 **[!UICONTROL Photos]** 수 **[!UICONTROL Videos]** 있습니다.)

* **[!UICONTROL Language]**. 검색할 언어를 선택합니다. 영어가 기본 언어입니다.
* **[!UICONTROL Smart Tags]**. 컨텐츠를 식별하는 데 사용할 태그를 선택합니다. Livefyre는 컴퓨터 비전 기술을 사용하여 특정 스마트 태그가 포함된 사진과 비디오를 식별하여 보다 정교하게 검색할 수 있게 되었습니다. 모든 **[!UICONTROL ANY]** 태그를 사용하는 스트림으로 컨텐트를 필터링하려면 수정자를 사용하거나, 모든 **[!UICONTROL ALL]** 태그를 사용하는 스트림으로 컨텐츠를 필터링하려면 수정자를 사용합니다. 스트림을 **[!UICONTROL Image contains none of these smart tags]** 사용하여 스트림에서 원하지 않는 컨텐츠가 포함된 사진에 태그를 입력합니다. 텍스트 내용에는 이 옵션이 작동하지 않습니다.

* **[!UICONTROL Products]**. 제품 카탈로그의 제품을 사용하여 스트림 규칙과 일치하는 제품 태그를 추가합니다.
* **[!UICONTROL Premoderate]**. 다음 중 하나를 선택합니다.

   * **[!UICONTROL On]**. 모든 들어오는 규칙 컨텐츠를 중재합니다. modq의 스트림 섹션에서 미리 중재된 컨텐츠를 볼 수 있습니다. **[!UICONTROL On]** 앱 설정에서 설정을 무시합니다.
   * **[!UICONTROL Off]**. 들어오는 규칙 컨텐츠를 미리 중재하지 마십시오. **[!UICONTROL Off]** 앱 설정에서 설정을 무시합니다.
   * **[!UICONTROL Inherited (Off)]**. 사이트의 사전 중재 설정을 사용합니다 (아래 **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. 다음 중 하나를 선택합니다.
   * **[!UICONTROL Apply SAFE Rules]**. 이 스트림에 모든 보호 규칙을 적용합니다.
   * **[!UICONTROL Apply SAFE Rules for:]** 하나 이상의 옵션을 선택하여 이 스트림 규칙에 대한 보호 규칙을 적용합니다.
   * **[!UICONTROL Disable SAFE Rules]**. 이 스트림에 보호 규칙을 적용하지 마십시오.

소셜 네트워크 또는 컨텐츠 유형과 관련된 스트림 규칙 옵션은 해당 소셜 네트워크 또는 컨텐츠 유형에 대한 다음 설명서를 참조하십시오.

* [Facebook 페이지](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [이메일](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
