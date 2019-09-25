---
description: Facebook 페이지에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Facebook 페이지에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Facebook 페이지 규칙
solution: Experience Manager
title: Facebook 페이지 규칙
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Facebook 페이지 규칙{#facebook-page-rules}

Facebook 페이지에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

Facebook 페이지 규칙을 사용하여 Facebook 페이지에서 공개적으로 게시된 컨텐츠를 스트리밍할 수 있습니다. 컨텐츠는 SocialSync와 동일한 빈도로 앱 또는 폴더로 가져오며, 이 빈도는 Facebook 페이지 및 게시물 트래픽 패턴에 따라 변경됩니다. Facebook 페이지 내의 링크도 지원되며, 스트림에 표시됩니다.

Facebook 페이지 규칙을 만들어 Facebook 페이지의 콘텐츠를 앱 또는 폴더로 가져오려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Facebook Page]**

   * 페이지 **[!UICONTROL Name]** 항목을 입력합니다. URL에 대해 후행 텍스트만 입력합니다. **** 예:컨텐츠를 추가하려면 `https://facebook.com/KellysSuperFunFanPage`필드에 KellysSuperFunFanPage *를* **[!UICONTROL Name]** 입력합니다.

   * 페이지 게시물에 사용자 댓글을 포함하려면 **[!UICONTROL Include Facebook Comments for each post]** 켜십시오.
   * 다른 사용자의 게시물을 제외하려면 **[!UICONTROL Only Show Author Posts]** 켜십시오.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 [규칙에 대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre는 Facebook에서 수신한 컨텐츠로 제한되므로 Facebook 페이지의 모든 게시물이 스트림에 포함된다고 보장할 수 없습니다.

>[!NOTE]
>
>Facebook SocialSync와 Facebook 페이지 규칙이 모두 특정 Facebook 페이지에 대해 활성화되어 있고 사용자 댓글이 Facebook 페이지 규칙에 대해 활성화되어 있으면 스트림 규칙이 SocialSync를 덮어씁니다. SocialSync를 사용하지 않고 Facebook 페이지 조정 규칙만을 기반으로 컨텐츠가 앱으로 스트리밍됩니다.

Facebook 페이지 큐레이트에서 지원하는 컨텐츠 유형은 다음과 같습니다.

* 페이지 소유자 또는 관리자

   * 상태
   * 사진
   * 비디오를 링크로

* 표준 Facebook 사용자

   * 상태
   * 사진
   * 비디오를 링크로

* 제3자

   * 상태

