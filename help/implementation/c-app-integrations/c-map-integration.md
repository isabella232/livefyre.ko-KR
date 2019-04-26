---
description: 대화형 맵에 사용자 컨텐츠를 구성합니다.
seo-description: 대화형 맵에 사용자 컨텐츠를 구성합니다.
seo-title: map
solution: Experience Manager
title: map
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# map{#map}

대화형 맵에 사용자 컨텐츠를 구성합니다.

지도를 통해 지오태그가 지정된 컨텐츠를 월드 맵에 스트리밍할 수 있으므로 속보 또는 라이브 이벤트를 중심으로 소셜 버즈를 찾을 수 있습니다. 텍스트, 댓글, 사진, 트윗을 비롯한 모든 해당 콘텐츠가 표시됩니다.

>[!NOTE]
>
>맵은 [Livefyre가 맵을 렌더링하는 데 사용하는 데이터를 제공하는 © openstreetmap](https://www.openstreetmap.org/copyright)를 기반으로 합니다.

## 통합 {#section_w2m_db2_d1b}

Map를 사용하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅된 내장 버전을 사용하는 것입니다.

먼저 [livefyre. js](https://github.com/Livefyre/Livefyre.js) 를 페이지에 추가합니다.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 맵 앱이 나타날 요소를 배치합니다.

```
<div id="map" style="height: 500px;"></div>
```

마지막으로 Livefyre를 사용하여 맵을 만들고 streamhub-SDK에서 컬렉션을 수집해야 합니다. 맵에는 Geotagged 메타데이터가 포함된 컨텐츠만 표시될 수 있습니다. Twitter 및 Instagram 조정에서 이 기능을 지원합니다. 최상의 성과를 얻으려면 컬렉션에 대한 모든 조정 규칙에 지리적 위치 필터를 포함시키십시오.

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

이 [라이브 예제를](https://codepen.io/cheung31/pen/wkmbF)확인하십시오.

## 구성 {#section_jc5_gxb_c1b}

`initial`

컬렉션에서 로드하여 지도에 표시할 항목의 초기 수입니다. 이 숫자가 로드되면 사용자는 단추를 클릭하여 더 볼 수 있습니다. (선택 사항. 기본값은 50 입니다.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

렌더링에 사용되는 기본 [홍보 자료](https://leafletjs.com/) 맵에 전달할 선택 사항입니다. 이 옵션을 사용하여 [맵의 초기 중심점](https://leafletjs.com/reference.html#map-options), 초기 및 최대 확대/축소 수준을 포함한 홍보 자료 맵을 설정할 수 있습니다. (선택 사항)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

