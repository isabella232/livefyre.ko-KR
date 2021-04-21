---
description: YouTube 규칙에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
title: YouTube 규칙
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# YouTube 규칙 {#youtube-rules}

YouTube 규칙에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

사용자, 채널 또는 재생 목록을 기반으로 YouTube 규칙을 만듭니다.

YouTube 규칙을 만들어 YouTube의 콘텐츠를 앱 또는 폴더로 가져오려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL User]**
   * 스트림에 사용자의 비디오를 포함할 **[!UICONTROL User]**&#x200B;의 별칭 문자열을 입력합니다.
   * 예를 들어 입력하려는 사용자 피드의 URL이 `https://www.youtube.com/user/livefyresupport`이면 `livefyresupport`을(를) 입력하십시오.

* **[!UICONTROL Channel]**
   * 스트림에 채널의 비디오를 포함할 **[!UICONTROL Channel]**&#x200B;의 별칭 문자열을 입력합니다.
   * 예를 들어 입력할 채널 피드의 URL이 `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`인 경우 `UCeNZlh03MyUkjRlLFpVQxsg`만 입력합니다.

* **[!UICONTROL Playlist]**
   * 스트림에 재생 목록의 비디오를 포함할 **[!UICONTROL Playlist]**&#x200B;의 별칭 문자열을 입력합니다.
   * 예를 들어, 입력하려는 재생 목록 피드의 URL이 `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`인 경우 `PLFE5670C92BDAC201`만 입력합니다.

* **[!UICONTROL Include recent items.]** 이 값을 다음으로 설정한 경우:
   * **[!UICONTROL Enabled]**, Livefyre는 게시 날짜에 관계없이 피드에 있는 처음 15개의 컨텐츠 항목을 스트림에 추가합니다.
   * **[!UICONTROL Disabled]**, Livefyre는 스트림 규칙 생성 날짜 이상과 동일한 게시 날짜를 사용하여 피드에 있는 처음 15개의 컨텐츠 항목을 스트림에 추가합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 대한 [스트림 규칙 옵션](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)을 참조하십시오.
