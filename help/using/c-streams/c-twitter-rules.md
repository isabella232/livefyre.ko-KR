---
description: Twitter에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-description: Twitter에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
seo-title: Twitter 규칙
solution: Experience Manager
title: Twitter 규칙
uuid: A 7 FD 2398-FD 6 B -4 C 24-92 B 2-7471176 D 7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter 규칙{#twitter-rules}

Twitter에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

해시 태그, 키워드, @ 언급 또는 작성자를 기반으로 Twitter 규칙을 만듭니다.

규칙을 추가하면 **[!UICONTROL Words]****[!UICONTROL Username]** 두 항목이 모두 포함된 컨텐츠가 반환됩니다.

>[!NOTE]
>
>Livefyre는 Twitter 디스플레이 가이드라인을 준수하며, 고객은 이러한 가이드라인을 준수할 책임이 있습니다. 자세한 내용은 Twitter의 [디스플레이 요구 사항에](https://dev.twitter.com/terms/display-requirements)대한 설명서를 참조하십시오.

Twitter 피드에서 앱 또는 폴더로 컨텐츠를 가져오는 Twitter 규칙을 만들려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Keywords]**
   * Twitter **[!UICONTROL Keywords]** 스트림에서 포함하거나 제외하려면 Enter 키를 누릅니다. **[!UICONTROL Contains any of these words]** AND **[!UICONTROL Does not contain any of these words]** 필드에 대한 값을 지정하면 첫 번째 항목이 포함된 트윗이 반환되고 두 번째 항목이 포함되지 않습니다. 단일 필드에 대한 여러 값을 입력하면 값이 들어 있는 결과가 반환됩니다. 부울 연산자를 사용하고 두 개 이상의 단어가 포함된 트윗을 검색하려면 두 개의 앰퍼샌드 (*& &*) 를 사용하여 두 개의 단어를 구분합니다.
   * 예를 들어 키워드 giants, **[!UICONTROL Contains any of these words]** posey 및 **[!UICONTROL Does not contain any of these words]** keyword dodger를 입력하면 *giants* 또는 *posey* 단어가 포함되고 dodger 라는 단어를 *포함하지 않는 모든 트윗이 반환됩니다*.
*Giants* 와 *Posey*단어가 모두 포함된 트윗을 검색하려면 "Giants & & Posey" 를 입력합니다. 이 기능은 Twitter 규칙의 **[!UICONTROL Contains any of these words]** 및 **[!UICONTROL Does not contain any of these words]** 필드에 대해서만 지원됩니다.

* **[!UICONTROL Hashtags]**.
   * Twitter **[!UICONTROL Hashtags]** 스트림에서 포함하거나 제외하려면 Enter 키를 누릅니다. **[!UICONTROL Contains any of these words]** 와 **[!UICONTROL Does not contain any of these words]** 필드 모두에 대한 값을 지정하면 첫 번째 필드에 해시 태그가 들어 있고 두 번째 필드에 해시 태그가 들어 있지 않은 트윗이 반환됩니다. 단일 필드에 여러 값을 입력할 수 있습니다. 스트림에서는 값이 들어 있는 결과를 반환합니다.

* **[!UICONTROL Usernames]**
   * 스트림을 입력하거나 **[!UICONTROL @mentions]****[!UICONTROL authors]** 스트림에서 제외하거나 제외합니다. 확인란을 사용하여 선택한 **[!UICONTROL Retweets]** 작성자의 **[!UICONTROL replies]** 포함 여부도 정의할 수 있습니다.
   >[!NOTE]
   >
   >귀하는 작성자를 포함하거나 제외할 수 있습니다. 이러한 두 필드를 하나의 Twitter 규칙으로 결합할 수는 없습니다.

* **[!UICONTROL Minimum number of followers.]** 사용자가 게시물에서 정보를 가져와야 하는 최소 팔로워 수를 선택합니다.
* **[!UICONTROL Location]**

   * 위치 (구/군/시/경도 형식 (+/- 90, +/- 180) 의 도시, 우편 번호, 주소 또는 지리 코드를 입력합니다.) 위치 입력을 시작하여 제안 사항이 있는 드롭다운 메뉴를 표시합니다. 드롭다운에서 위치를 선택합니다. 맵에 해당 위치의 핀이 표시됩니다. 슬라이더를 조정하여 각 위치에 대해 1 마일 ~ 25 마일 반경을 선택합니다. 반경을 선택하지 않으면 Livefyre는 자동으로 8 마일을 선택합니다.
   >[!NOTE]
   >
   >두 필드 모두 입력 위치의 중심에서 거리가 계산됩니다.

   * 둘 이상의 위치와 반경을 추가할 수 있습니다. 상자에서 위치 이름 옆에 있는 X를 클릭하여 위치를 삭제할 수 있습니다.
   * **[!UICONTROL Is near this location]** 및 **[!UICONTROL Is not near this location]** 필드를 결합하여 **[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]** 필드의 위치에 있는 위치에 있는 컨텐츠를 가져올 수 있습니다.


* **[!UICONTROL Additional Filters]**
   * 추가 필터를 사용하여 Twitter 규칙을 더욱 세밀하게 조정할 수 있습니다. 다음을 사용할지 여부를 정의합니다.
      * 타깃팅된 **[!UICONTROL Replies]** 트윗에 포함 (스트림이 고속 처리되는 경우 이 기능은 자동으로 비활성화됩니다.)
      * 트윗 포함 **[!UICONTROL Verified Twitter accounts only.]**
      * , **[!UICONTROL All Content]**또는 **[!UICONTROL Vines Only]**, 또는 **[!UICONTROL Images Only.]**
      * 선택한 **[!UICONTROL Minimum number of followers]** (모두, 100, 500, 1000, 10,000 또는 100,000) 계정이 있는 트윗만 포함합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 [대한 스트림 규칙 옵션을 참조하십시오](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
