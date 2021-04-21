---
description: twitter에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
title: Twitter 규칙
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Twitter 규칙{#twitter-rules}

twitter에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

해시 태그, 키워드, @mentions 또는 작성자를 기반으로 Twitter 규칙을 만듭니다.

규칙에 대해 **[!UICONTROL Words]** 및 **[!UICONTROL Username]**&#x200B;을 추가하면 두 항목이 모두 포함된 내용이 반환됩니다.

>[!NOTE]
>
>Livefyre는 Twitter 표시 지침을 준수하며 고객은 이러한 지침을 준수할 책임이 있습니다. 자세한 내용은 해당 [디스플레이 요구 사항](https://dev.twitter.com/terms/display-requirements)에 대한 Twitter 설명서를 참조하십시오.

twitter 피드에서 앱 또는 폴더로 콘텐츠를 가져오는 Twitter 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Keywords]**
   * twitter 스트림에 포함하거나 제외할 **[!UICONTROL Keywords]**&#x200B;을 입력합니다. **[!UICONTROL Contains any of these words]** 및 **[!UICONTROL Does not contain any of these words]** 필드 모두에 값을 지정하면 첫 번째 값이 포함된 트윗이 반환되고 두 번째 트윗은 포함되지 않습니다. 단일 필드에 여러 값을 입력할 수 있으며 값이 들어 있는 결과를 반환합니다. 부울 연산자 AND를 사용하여 두 개 이상의 단어가 포함된 트윗을 검색하려면 두 개의 앰퍼샌드(*&amp;*)를 사용하여 두 단어를 구분합니다.
   * 예를 들어 **[!UICONTROL Contains any of these words]** 키워드 Giants, Posey 및 **[!UICONTROL Does not contain any of these words]** 키워드 Dodger를 입력하면 *Giants* 또는 *Posey*&#x200B;라는 단어가 포함된 모든 트윗을 반환하고 *Dags*라는 단어는 포함하지 않습니다.
*자이언츠* 및 *Posey*&#x200B;라는 단어가 모두 포함된 트윗을 검색하려면 &quot;Giants &amp; Posey&quot;를 입력합니다. 이 기능은 Twitter 규칙의 **[!UICONTROL Contains any of these words]** 및 **[!UICONTROL Does not contain any of these words]** 필드에만 지원됩니다.

* **[!UICONTROL Hashtags]**&#x200B;를 참조하십시오.
   * twitter 스트림에 포함하거나 제외할 **[!UICONTROL Hashtags]**&#x200B;을 입력합니다. **[!UICONTROL Contains any of these words]** 및 **[!UICONTROL Does not contain any of these words]** 필드 모두에 값을 지정하면 첫 번째 필드에 해시 태그가 들어 있고 두 번째 필드에 해시 태그를 포함하지 않는 트윗이 반환됩니다. 단일 필드에 여러 값을 입력할 수 있습니다. 스트림은 값이 들어 있는 결과를 반환합니다.

* **[!UICONTROL Usernames]**
   * 스트림에 풀링하거나 스트림에서 제외하려면 **[!UICONTROL @mentions]** 또는 **[!UICONTROL authors]**&#x200B;을 입력합니다. 확인란을 사용하여 선택한 작성자의 **[!UICONTROL Retweets]** 또는 **[!UICONTROL replies]**&#x200B;도 포함해야 하는지 여부를 정의합니다.

   >[!NOTE]
   >
   >작성자를 포함하거나 제외할 수 있습니다.이 두 필드를 단일 Twitter 규칙으로 결합할 수는 없습니다.

* **[!UICONTROL Minimum number of followers.]** 사용자가 게시물에서 정보를 가져와야 하는 최소 팔로워 수를 선택합니다.
* **[!UICONTROL Location]**

   * 위치(일반 위도/경도 형식(+/- 90, +/- 180)로 구/군/시, 우편 번호, 주소 또는 지리적 코드를 입력합니다. 제안을 포함한 드롭다운 메뉴를 표시할 위치를 입력하기 시작합니다. 드롭다운에서 위치를 선택합니다. 지도에는 해당 위치의 핀이 표시됩니다. 슬라이더를 조정하여 각 위치에 대해 1.6에서 25마일 반경을 선택합니다. 반경을 선택하지 않으면 Livefyre는 8마일의 기본값을 자동으로 선택합니다.
   >[!NOTE]
   >
   >두 필드 모두에 대해 입력 위치의 중앙으로부터 거리가 계산됩니다.

   * 둘 이상의 위치 및 반경을 추가할 수 있습니다. 상자에 있는 위치 이름 옆에 있는 X를 클릭하여 위치를 삭제할 수 있습니다.
   * **[!UICONTROL Is near this location]** 및 **[!UICONTROL Is not near this location]** 필드를 결합하여 **[!UICONTROL Is near this location]** 필드의 위치에 있는 컨텐츠를 가져오지만 **[!UICONTROL Is not near this location]** 필드의 위치 근처에 있는 것은 아닙니다.


* **[!UICONTROL Additional Filters]**
   * 추가 필터를 사용하여 Twitter 규칙을 더 세분화합니다. 다음을 수행할지 여부를 정의합니다.
      * 타깃팅된 트윗에 **[!UICONTROL Replies]**&#x200B;을(를) 포함합니다(스트림이 빠른 속도로 되면 이 기능은 자동으로 비활성화됩니다.).
      * **[!UICONTROL Verified Twitter accounts only.]**&#x200B;의 트윗 포함
      * **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** 또는 **[!UICONTROL Images Only.]** 포함
      * 선택한 **[!UICONTROL Minimum number of followers]**(임의, 100, 500, 1000, 1000, 10,000 또는 100,000) 계정의 트윗만 포함합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 대한 [스트림 규칙 옵션](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)을 참조하십시오.
