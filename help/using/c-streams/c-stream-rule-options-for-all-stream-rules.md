---
description: 이러한 옵션은 모든 소셜 네트워크의 모든 스트림 규칙 또는 게시 방법에 적용됩니다.
title: 모든 스트림 규칙에 대한 스트림 규칙 옵션
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---

# 모든 스트림 규칙에 대한 스트림 규칙 옵션{#stream-rule-options-for-all-stream-rules}

이러한 옵션은 모든 소셜 네트워크의 모든 스트림 규칙 또는 게시 방법에 적용됩니다.

텍스트 및 키워드 필드에 대한 검색 기능:

* 키워드를 입력하면 개별 단어에 대해 Livefyre는 자동으로 부울 연산자 **OR**&#x200B;을 사용합니다. 예를 들어 단어 *cake* 또는 *recipe*&#x200B;로 게시물을 검색하려면 *cake*&#x200B;를 입력한 다음 **[!UICONTROL keyword]** 필드에 *recipe*&#x200B;을 입력합니다.

* 정확한 구문 텍스트를 따옴표로 묶어서 정확한 구문을 검색할 수 있습니다. 예를 들어 *케이크 레서피* 구문을 정확히 검색하려면 **[!UICONTROL keyword]** 필드에 *&quot;케이크 레서피&quot;*&#x200B;를 입력합니다.

* 부울 값과 정확한 구문 검색을 하나의 스트림 규칙에 결합할 수 있습니다. 예를 들어 각 구를 한 번에 하나씩 입력하여 *케이크*, *레서피* 및 *&quot;케이크 레서피&quot;*&#x200B;를 검색할 수 있습니다.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 다음 중 하나를 선택합니다.

   * **[!UICONTROL All Content.]** 모든 컨텐츠를 허용합니다.
   * **[!UICONTROL Media Required.]** 이미지와 비디오가 포함된 컨텐츠만 허용합니다. instagram 및 Facebook 컨텐츠의 경우 **[!UICONTROL Photos]** 또는 **[!UICONTROL Videos]**&#x200B;만 지정할 수 있습니다.

* **[!UICONTROL Language]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 검색할 언어를 선택합니다. 기본 언어는 영어입니다.
* **[!UICONTROL Smart Tags]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 컨텐츠를 식별하는 데 사용할 태그를 선택합니다. Livefyre는 컴퓨터 비전 기술을 사용하여 특정 스마트 태그가 포함된 사진과 비디오를 찾아 검색을 보다 정확하게 합니다. **[!UICONTROL ANY]** 수정자를 사용하여 태그 또는 **[!UICONTROL ALL]** 수정자를 사용하여 컨텐츠를 스트림으로 필터링하여 모든 태그를 사용하는 스트림으로 컨텐츠를 필터링합니다. 스트림에서 원하지 않는 내용이 포함된 사진에 대한 태그를 입력하려면 **[!UICONTROL Image contains none of these smart tags]** 필드를 사용합니다. 텍스트 내용에는 이 옵션이 작동하지 않습니다.

* **[!UICONTROL Products]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 제품 카탈로그의 제품과 스트림 규칙을 일치하도록 제품 태그를 추가합니다.
* **[!UICONTROL Premoderate]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 다음 중 하나를 선택합니다.

   * **[!UICONTROL On]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 들어오는 모든 규칙 콘텐츠를 사전 중재합니다. ModQ의 스트림 섹션에서 사전 중재된 컨텐츠를 볼 수 있습니다. **[!UICONTROL On]** 은 앱 설정의 설정을 무시합니다.
   * **[!UICONTROL Off]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 들어오는 규칙 내용을 사전 중재하지 마십시오. **[!UICONTROL Off]** 은 앱 설정의 설정을 무시합니다.
   * **[!UICONTROL Inherited (Off)]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 사이트의 사전 중재 설정을 사용합니다(**[!UICONTROL Site Settings]** 아래).

* **[!UICONTROL SAFE Rules]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 다음 중 하나를 선택합니다.
   * **[!UICONTROL Apply SAFE Rules]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 모든 SAFE 규칙을 이 스트림에 적용합니다.
   * **[!UICONTROL Apply SAFE Rules for:]** 이 스트림 규칙에 대해 안전 규칙을 적용하려면 옵션 중 하나 이상을 선택합니다.
   * **[!UICONTROL Disable SAFE Rules]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 스트림에 SAFE 규칙을 적용하지 마십시오.

소셜 네트워크 또는 컨텐트 유형에 특정한 스트림 규칙 옵션은 해당 소셜 네트워크 또는 컨텐트 유형에 대한 다음 설명서를 참조하십시오.

* [Facebook 페이지](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [이메일](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
