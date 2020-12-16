---
description: 사용자 콘텐츠를 대화형 맵으로 플롯
seo-description: 사용자 콘텐츠를 대화형 맵으로 플롯
seo-title: 맵
solution: Experience Manager
title: 맵
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 2%

---


# 맵{#map}

사용자 콘텐츠를 대화형 맵으로 플롯

맵에서는 지리화된 컨텐츠를 월드 맵에 스트리밍할 수 있으므로 뉴스와 라이브 이벤트 간의 소셜 버즈를 찾을 수 있습니다. 텍스트, 댓글, 사진 및 트윗을 비롯한 모든 해당 컨텐츠가 표시됩니다.

>[!NOTE]
>
>맵은 Livefyre가 맵을 렌더링하는 데 사용하는 데이터를 제공하는 [©OpenStreetMap](https://www.openstreetmap.org/copyright)에서 지원합니다.

## 통합 {#section_w2m_db2_d1b}

맵을 사용하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅되는 내장 버전을 사용하는 것입니다.

먼저 [Livefyre.js](https://github.com/Livefyre/Livefyre.js)를 페이지에 추가합니다.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 맵 앱이 표시될 요소를 배치합니다.

```
<div id="map" style="height: 500px;"></div>
```

마지막으로 Livefyre.require를 사용하여 맵을 구성하고 Streamhub-sdk에서 파이프를 꽂을 컬렉션을 가져옵니다. 맵은 지리화된 메타데이터가 있는 컨텐츠만 표시할 수 있습니다. Twitter 및 Instagram Curate는 이 기능을 지원합니다. 최상의 성능을 얻으려면 컬렉션에 대한 모든 조정 규칙에 지리적 위치 필터를 포함하십시오.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

이 [라이브 예제](https://codepen.io/cheung31/pen/wkmbF)를 확인하십시오.

## 구성 {#section_jc5_gxb_c1b}

`initial`

컬렉션에서 로드하고 맵에 표시할 항목의 초기 수입니다. 이 번호가 로드되면 사용자는 단추를 클릭하여 더 많이 표시할 수 있습니다. (선택 사항입니다. 기본값은 50입니다.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

렌더링에 사용되는 기본 [홍보](https://leafletjs.com/) 맵에 전달하는 옵션 이 옵션을 사용하여 맵의 초기 중심점, 초기 및 최대 확대/축소 레벨을 포함하여 [전단지 맵 옵션](https://leafletjs.com/reference.html#map-options)을 설정합니다. (선택 사항입니다.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

