---
description: 사이트 또는 네트워크에서 가장 활성화된 컬렉션을 보여줍니다.
seo-description: 사이트 또는 네트워크에서 가장 활성화된 컬렉션을 보여줍니다.
seo-title: 트렌딩
solution: Experience Manager
title: 트렌딩
uuid: 3031523 D-B 487-4 EEA-BBA 6-5 D 8 F 9971874 F
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 트렌딩{#trending}

사이트 또는 네트워크에서 가장 활성화된 컬렉션을 보여줍니다.

트렌드를 사용하여 사이트 또는 네트워크에서 가장 최근 활동이 있는 컬렉션을 선보여 보십시오.

## 통합 {#section_wtz_whb_c1b}

트렌드를 통합하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅된 내장 버전을 사용하는 것입니다.

먼저 [livefyre. js](https://github.com/Livefyre/Livefyre.js) 를 페이지에 추가합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 앱이 나타날 요소를 배치합니다.

```
<div id="trending"></div>
```

마지막으로 구성 요소를 구성하는 `Livefyre.require` 데 사용합니다.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

트렌드 앱이 있습니다. 이 예에서는 이 모든 작업을 [직접 확인해](https://codepen.io/gobengo/pen/GijEy)보십시오.

## 구성 {#section_k5k_qhb_c1b}

`network`

컬렉션이 가져올 네트워크입니다. (필수.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

사이트 ID를 제공하여 네트워크 내의 단일 사이트에서만 컬렉션을 표시합니다. (선택 사항)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

단일 컬렉션 태그를 제공하여 해당 태그가 있는 컬렉션만 표시합니다. (선택 사항)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

