---
description: RSS 피드에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: RSS 피드에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: RSS 규칙
solution: Experience Manager
title: RSS 규칙
uuid: 3 C 9 E 2069-BB 85-41 DC -8 B 35-6237642 A 538 A
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# RSS 규칙{#rss-rules}

RSS 피드에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

RSS 스트림은 5 분마다 업데이트되어 피드의 처음 50 개 항목에서 아직 Livefyre에 존재하지 않는 컨텐츠를 찾습니다. Livefyre는 피드의 처음 50 개 항목을 모두 무시합니다.

RSS 피드의 콘텐츠를 앱 또는 폴더에 가져올 RSS 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL URL]** 를 참조하십시오.
* **[!UICONTROL Include recent items.]** 이 설정이 다음으로 설정되어 있는 경우:

   * **[!UICONTROL Enabled]**, Livefyre는 발행 날짜에 관계없이 피드에 처음 50 개의 컨텐츠 항목을 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 작성 날짜 이상 버전과 동일한 발행 날짜를 사용하여 피드에 처음 50 개의 컨텐츠 항목을 추가합니다.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 항목 링크 또는 XML에서 정보를 가져옵니다.

**RSS 규칙**

Livefyre는 다음 RSS 사양을 기반으로 RSS 피드를 분석합니다.

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [미디어 RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom 피드](https://validator.w3.org/feed/docs/atom.html)

Livefyre는 이러한 사양을 준수하지 않는 피드를 읽지 않으며 해당 컨텐츠는 스트림으로 가져올 수 없습니다. WC 3 피드 유효성 검사 서비스를 사용하여 RSS 피드의 구문을 확인하고 유효성을 확인합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 [대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
