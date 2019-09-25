---
description: YouTube 규칙에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: YouTube 규칙에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: YouTube 규칙
solution: Experience Manager
title: YouTube 규칙
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# YouTube 규칙 {#youtube-rules}

YouTube 규칙에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

사용자, 채널 또는 재생 목록을 기반으로 YouTube 규칙을 만듭니다.

YouTube 콘텐츠를 YouTube의 앱 또는 폴더로 가져오는 YouTube 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL User]**
   * 스트림에 **[!UICONTROL User]** 사용자의 비디오를 포함할 별칭 문자열을 입력합니다.
   * 예를 들어, 입력하려는 사용자 피드의 URL이 `https://www.youtube.com/user/livefyresupport`인 경우 간단하게 입력합니다 `livefyresupport`.

* **[!UICONTROL Channel]**
   * 스트림에 채널의 비디오를 **[!UICONTROL Channel]** 포함할 별칭 문자열을 입력합니다.
   * 예를 들어, 입력할 채널 피드의 URL이 `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`인 경우 간단하게 입력합니다 `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * 스트림에 재생 목록의 비디오를 **[!UICONTROL Playlist]** 포함할 별칭 문자열을 입력합니다.
   * 예를 들어 입력하려는 재생 목록 피드의 URL이 `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`인 경우 `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** 이 값이 다음과 같이 설정된 경우:
   * **[!UICONTROL Enabled]**, Livefyre는 발행 날짜에 관계없이 피드의 처음 15개의 컨텐츠 항목을 스트림에 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 생성 날짜 이상과 동일한 발행 날짜를 사용하여 피드의 처음 15개의 컨텐츠 항목을 스트림에 추가합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 [규칙에 대한 스트림 규칙 옵션을 참조하십시오](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
