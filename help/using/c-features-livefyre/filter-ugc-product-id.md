---
description: 제품 ID별로 UGC를 필터링하면 각 페이지에 대해 다른 제품별 UGC를 표시하면서 동일한 앱을 여러 페이지에 포함할 수 있습니다.
seo-description: 제품 ID별로 UGC를 필터링하면 각 페이지에 대해 다른 제품별 UGC를 표시하면서 동일한 앱을 여러 페이지에 포함할 수 있습니다.
seo-title: 제품 ID로 UGC 필터링
title: 제품 ID로 UGC 필터링
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# 제품 ID {#filter-ugc-product-id}별로 UGC 필터링

제품 ID별로 UGC를 필터링하면 각 페이지에 대해 다른 제품별 UGC를 표시하면서 동일한 앱을 여러 페이지에 포함할 수 있습니다.

제품 ID별로 UGC를 필터링하려면 다음 단계를 수행합니다.

1. Livefyre 스튜디오에서 **[!UICONTROL Apps]** 탭으로 이동합니다.

1. 수정할 앱을 선택합니다.

1. 왼쪽 레일에서 [디자이너] 탭을 선택합니다.

1. 활성화 **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. UGC를 필터링할 제품 또는 제품이 들어 있는 최상위 제품 폴더를 선택합니다.
여러 폴더를 선택하려면 Ctrl/Command + 클릭을 사용합니다.

1. **[!UICONTROL Show related content]** 비활성화.
활성화되면 `data-lf-attr-product` 특성을 사용하여 필터링된 콘텐츠가 먼저 표시되고, 그 뒤에 앱의 다른 모든 콘텐츠가 표시됩니다.

1. 클릭 **[!UICONTROL Publish]**.

1. 결과 코드에 필터링하려는 제품 ID를 삽입합니다.

>[!NOTE]
>
>제품 ID를 찾으려면 **[!UICONTROL Settings > Products]**&#x200B;으로 이동합니다. 원하는 제품을 찾아 선택하고 ID가 표시됩니다.

예를 들어 미디어 담벼락 앱에 대해 다음 코드가 생성됩니다.

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

제품에 태그를 지정하려면 `data-lf-attr-product` 속성의 `<product 1>`을 원하는 제품 ID로 바꾸십시오. 쉼표로 구분된 제품 ID를 추가로 추가하여 하나 이상의 제품에 태그를 지정할 수 있습니다. 제품은 5단계에서 선택한 최상위 제품 폴더 또는 폴더에 포함되어야 합니다.

수정된 코드 세그먼트는 다음과 같이 표시됩니다.

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

이제 앱에 태그가 지정된 제품 ID만 표시됩니다.