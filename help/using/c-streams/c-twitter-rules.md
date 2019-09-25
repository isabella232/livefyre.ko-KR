---
description: Twitter에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Twitter에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Twitter 규칙
solution: Experience Manager
title: Twitter 규칙
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter 규칙{#twitter-rules}

Twitter에서 콘텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

해시 태그, 키워드, @언급 또는 작성자를 기반으로 Twitter 규칙을 만듭니다.

규칙 **[!UICONTROL Words]** 및 **[!UICONTROL Username]** 을 추가하면 두 항목을 모두 포함하는 컨텐츠가 반환됩니다.

>[!NOTE]
>
>Livefyre는 Twitter 디스플레이 지침을 준수하며 고객은 이러한 지침을 준수할 책임이 있습니다. 자세한 내용은 Twitter의 디스플레이 요구 사항에 대한 설명서를 [참조하십시오](https://dev.twitter.com/terms/display-requirements).

Twitter 피드의 콘텐츠를 앱 또는 폴더로 가져오는 Twitter 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Keywords]**
   * Twitter 스트림에 **[!UICONTROL Keywords]** 포함하거나 제외할 항목을 입력합니다. 및 필드 모두에 대한 값을 **[!UICONTROL Contains any of these words]** **[!UICONTROL Does not contain any of these words]** 지정하면 첫 번째 값이 들어 있는 트윗이 반환되고 두 번째 트윗은 포함되지 않습니다. 단일 필드에 여러 값을 입력할 수 있으며 값이 들어 있는 결과를 반환합니다. 부울 연산자 AND를 사용하여 둘 이상의 단어가 포함된 트윗을 검색하려면 두 앰퍼샌드(*&amp;&amp;*)를 사용하여 두 단어를 분리합니다.
   * 예를 들어 Giants, Posey 및 Keyword Dodger **[!UICONTROL Contains any of these words]** 를 포함한 모든 트윗을 반환하고 **[!UICONTROL Does not contain any of these words]** Dodger *를* 입력하지 *않고* Dodger *를*입력합니다.
Giants와 Posey가 모두 포함된 *트윗을* 검색하려면 **"Giants &amp; Posey"를 입력합니다. 이 기능은 Twitter 규칙의 **[!UICONTROL Contains any of these words]** 및 **[!UICONTROL Does not contain any of these words]** 필드에 대해서만 지원됩니다.

* **[!UICONTROL Hashtags]**.
   * Twitter 스트림에 **[!UICONTROL Hashtags]** 포함하거나 제외할 항목을 입력합니다. 및 **[!UICONTROL Contains any of these words]** **[!UICONTROL Does not contain any of these words]** 필드 모두에 값을 지정하면 첫 번째 필드에 해시 태그가 포함된 트윗이 반환되고 두 번째 필드에 해시 태그가 포함되지 않습니다. 단일 필드에 여러 값을 입력할 수 있습니다. 스트림은 값이 들어 있는 결과를 반환합니다.

* **[!UICONTROL Usernames]**
   * 스트림을 **[!UICONTROL @mentions]** 입력하거나 **[!UICONTROL authors]** 스트림으로 가져오거나 스트림에서 제외합니다. 확인란을 사용하여 선택한 작성자도 포함할지 **[!UICONTROL Retweets]** 여부를 **[!UICONTROL replies]** 정의합니다.
   >[!NOTE]
   >
   >작성자를 포함하거나 제외할 수 있습니다.이 두 필드를 단일 Twitter 규칙으로 결합할 수 없습니다.

* **[!UICONTROL Minimum number of followers.]** 사용자가 게시물에서 정보를 가져와야 하는 최소 팔로워 수를 선택합니다.
* **[!UICONTROL Location]**

   * 위치(도시, 지프 코드, 주소 또는 지리적 코드를 일반적인 위도/경도 형식(+/- 90, +/- 180)으로 입력합니다. 제안을 포함하여 드롭다운 메뉴를 표시할 위치를 입력하기 시작합니다. 드롭다운에서 위치를 선택합니다. 맵에 해당 위치의 핀이 표시됩니다. 슬라이더를 조정하여 각 위치의 반경 1마일에서 40km까지 선택합니다. 반경을 선택하지 않으면 Livefyre가 8마일의 기본값을 자동으로 선택합니다.
   >[!NOTE]
   >
   >두 필드 모두에 대해 입력 위치의 중심에서 거리가 계산됩니다.

   * 둘 이상의 위치 및 반경을 추가할 수 있습니다. 상자에서 위치 이름 옆에 있는 X를 클릭하여 위치를 삭제할 수 있습니다.
   * 필드와 **[!UICONTROL Is near this location]** 필드를 결합하여 **[!UICONTROL Is not near this location]** 필드의 위치 내에 있는 컨텐츠를 가져오지만 **[!UICONTROL Is near this location]** **[!UICONTROL Is not near this location]** 필드의 위치 근처에 있지는 않습니다.


* **[!UICONTROL Additional Filters]**
   * 추가 필터를 사용하여 Twitter 규칙을 더 세밀하게 수정할 수 있습니다. 다음을 수행할지 여부를 정의합니다.
      * 타깃팅된 트윗에 **[!UICONTROL Replies]** 포함(스트림이 빠른 경우 이 기능은 자동으로 비활성화됩니다.)
      * 다음에서 트윗 포함 **[!UICONTROL Verified Twitter accounts only.]**
      * 포함 **[!UICONTROL All Content]**&#x200B;또는 **[!UICONTROL Vines Only]**&#x200B;또는 **[!UICONTROL Images Only.]**
      * 선택한 계정의 트윗만 포함( **[!UICONTROL Minimum number of followers]** 임의, 100, 500, 1000, 10,000 또는 100,000).

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 [규칙에 대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
