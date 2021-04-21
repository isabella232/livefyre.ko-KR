---
description: RSS 피드에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
title: RSS 규칙
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# RSS 규칙{#rss-rules}

RSS 피드에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

피드의 처음 50개 항목에서 Livefyre에 아직 존재하지 않는 콘텐츠를 찾아 RSS 스트림은 5분마다 업데이트됩니다. Livefyre는 피드에서 처음 50개 항목을 지나는 모든 항목을 무시합니다.

RSS 피드의 컨텐츠를 앱 또는 폴더로 가져올 RSS 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL URL]** RSS 피드를 참조하십시오.
* **[!UICONTROL Include recent items.]** 이 값을 다음으로 설정한 경우:

   * **[!UICONTROL Enabled]**, Livefyre는 게시 날짜에 관계없이 피드에 있는 처음 50개의 컨텐츠 항목을 스트림에 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 생성 날짜 이상과 동일한 게시 날짜를 사용하여 피드에 있는 처음 50개의 컨텐츠 항목을 스트림에 추가합니다.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 항목 링크 또는 XML에서 정보를 가져옵니다.

**RSS 규칙**

Livefyre는 다음 RSS 사양을 기반으로 RSS 피드를 파싱합니다.

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [미디어 RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom 피드](https://validator.w3.org/feed/docs/atom.html)

Livefyre는 이러한 사양을 따르지 않는 피드를 읽지 않으며 해당 콘텐츠는 스트림으로 가져올 수 없습니다. WC3 피드 유효성 검사 서비스를 사용하여 RSS 피드의 구문을 확인하고 유효한지 확인합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 대한 [스트림 규칙 옵션](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)을 참조하십시오.
