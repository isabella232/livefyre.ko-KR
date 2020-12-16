---
description: Tumblr에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Tumblr에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Tumblr 규칙
solution: Experience Manager
title: Tumblr 규칙
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Tumblr 규칙{#tumblr-rules}

Tumblr에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

Tumblr 블로그를 기반으로 태그를 필터링하여 Tumblr 규칙을 만들 수 있습니다. Tumblr 스트림은 5분마다 업데이트되며 피드의 처음 20개 항목에서 Livefyre에 아직 존재하지 않는 콘텐츠를 찾습니다. Livefyre는 피드에서 처음 20개 항목을 지나는 모든 항목을 무시합니다.

Tumblr의 콘텐츠를 앱 또는 폴더로 가져올 수 있는 Tumblr 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Blog]**

   * Tumblr 블로그에서 **[!UICONTROL Blog Name]**&#x200B;을 입력합니다. URL(*stafblr.tumblr.com*) 또는 블로그 이름(*staff*)을 입력합니다.

   * 최대 1개의 **[!UICONTROL Tag]**&#x200B;을 포함하여 지정된 태그를 포함한 게시물별로 결과를 필터링합니다.

* **[!UICONTROL Include recent items.]** 이 값을 다음으로 설정한 경우:

   * **[!UICONTROL Enabled]**, Livefyre는 게시 날짜에 관계없이 피드에 있는 처음 20개의 컨텐츠 항목을 스트림에 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 생성 날짜 이상과 동일한 게시 날짜를 사용하여 피드에 있는 처음 20개의 컨텐츠 항목을 스트림에 추가합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 대한 [스트림 규칙 옵션](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)을 참조하십시오.
