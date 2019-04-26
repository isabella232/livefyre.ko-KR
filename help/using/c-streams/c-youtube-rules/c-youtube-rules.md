---
description: YouTube 규칙에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: YouTube 규칙에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: YouTube 규칙
solution: Experience Manager
title: YouTube 규칙
uuid: EC 6 A 3780-7119-45 C 3-8 AB 2-FB 0 F 9803 D 161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# YouTube 규칙 {#youtube-rules}

YouTube 규칙에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

사용자, 채널 또는 재생 목록을 기반으로 YouTube 규칙을 만듭니다.

YouTube에서 앱 또는 폴더로 컨텐츠를 가져오는 YouTube 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL User]**
   * 스트림에 사용자의 비디오를 포함하려면 Vanity **[!UICONTROL User]** 문자열을 입력합니다.
   * 예를 들어 입력하려는 사용자 피드의 URL를 입력하면 입력하면 `https://www.youtube.com/user/livefyresupport``livefyresupport`됩니다.

* **[!UICONTROL Channel]**
   * 스트림에 채널의 비디오를 **[!UICONTROL Channel]** 포함하려면 Vanity 문자열을 입력합니다.
   * 예를 들어 입력할 채널 피드의 URL를 입력하면 입력하면 `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg``UCeNZlh03MyUkjRlLFpVQxsg`됩니다.

* **[!UICONTROL Playlist]**
   * 스트림의 재생 목록에서 비디오를 포함하려면 Vanity **[!UICONTROL Playlist]** 문자열을 입력합니다.
   * 예를 들어, 입력할 재생 목록 피드의 URL를 `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`입력하면 `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** 이 설정이 다음으로 설정되어 있는 경우:
   * **[!UICONTROL Enabled]**, Livefyre는 발행 날짜에 관계없이 피드에 처음 15 개의 컨텐츠 항목을 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 작성 날짜 이상 버전과 동일한 발행 날짜를 사용하여 피드에 처음 15 개의 컨텐츠 항목을 추가합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 [대한 스트림 규칙 옵션을 참조하십시오](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
