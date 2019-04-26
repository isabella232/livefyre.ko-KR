---
description: Tumblr에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Tumblr에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Tumblr 규칙
solution: Experience Manager
title: Tumblr 규칙
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tumblr 규칙{#tumblr-rules}

Tumblr에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

Tumblr 블로그를 기반으로 Tumblr 규칙을 만들고 태그별로 필터링합니다. Tumblr 스트림은 5 분마다 업데이트되며, 피드의 처음 20 개 항목에서 아직 Livefyre에 존재하지 않는 컨텐츠를 찾습니다. Livefyre는 피드의 처음 20 개 항목을 모두 무시합니다.

Tumblr 규칙을 앱 또는 폴더로 가져오는 Tumblr 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Blog]**

   * Tumblr **[!UICONTROL Blog Name]** 블로그의를 입력합니다. URL (*staff.tumblr.com*) 또는 블로그 이름 (*직원*) 를 입력합니다.

   * 지정된 태그를 포함하는 게시물별로 결과를 **[!UICONTROL Tag]** 필터링하려면 최대 하나를 포함합니다.

* **[!UICONTROL Include recent items.]** 이 설정이 다음으로 설정되어 있는 경우:

   * **[!UICONTROL Enabled]**, Livefyre는 발행 날짜에 관계없이 피드에 처음 20 개 컨텐츠 항목을 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 작성 날짜 이상 버전과 동일한 발행 날짜를 사용하여 피드에 처음 20 개 컨텐츠 항목을 추가합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 [대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
