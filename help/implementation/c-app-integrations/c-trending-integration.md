---
description: 사이트 또는 네트워크에서 가장 유효한 컬렉션을 보여줍니다.
title: 트렌딩
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# 트렌딩{#trending}

사이트 또는 네트워크에서 가장 유효한 컬렉션을 보여줍니다.

트렌드를 사용하여 사이트 또는 네트워크의 최근 활동과 함께 컬렉션을 표시할 수 있습니다.

## 통합 {#section_wtz_whb_c1b}

트렌드를 통합하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅된 내장 버전을 사용하는 것입니다.

먼저 [Livefyre.js](https://github.com/Livefyre/Livefyre.js)를 페이지에 추가합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 앱이 나타날 요소를 배치합니다.

```
<div id="trending"></div>
```

마지막으로 `Livefyre.require`을 사용하여 구성 요소를 구성합니다.

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

이제 트렌딩 앱이 있습니다! [이 예제](https://codepen.io/gobengo/pen/GijEy)에서 이 모든 기능을 확인하십시오.

## 구성 {#section_k5k_qhb_c1b}

`network`

컬렉션을 가져올 네트워크입니다. (필수 여부.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

네트워크 내의 단일 사이트에서만 컬렉션을 표시하려면 사이트 ID를 입력하십시오. (선택 사항입니다.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

단일 컬렉션 태그를 제공하여 해당 태그가 있는 컬렉션만 표시합니다. (선택 사항입니다.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
