---
description: 실시간으로 컨텐츠 스트리밍을 통해 미디어 장벽을 만들 수 있습니다.
seo-description: 실시간으로 컨텐츠 스트리밍을 통해 미디어 장벽을 만들 수 있습니다.
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Media Wall{#media-wall}

실시간으로 컨텐츠 스트리밍을 통해 미디어 장벽을 만들 수 있습니다.

미디어 장벽을 사용하면 사이트에 대한 실시간 소셜 장벽을 만들 수 있습니다. Livefyre JavaScript SDK의 스트리밍 허브-배경 패키지를 사용하여 Livefyre 소셜 피드를 라이브 이벤트, 사진 콘테스트 호스팅 및 웹 사이트의 소셜 섹션 강화 등에 사용할 수 있는 시각적으로 매력적인 타일 방식의 컨텐츠 경험으로 표시할 수 있습니다.

## 통합 {#section_jfm_bwb_c1b}

미디어 담벼락을 추가하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅된 내장 버전을 사용하는 것입니다.

먼저 [Livefyre.js](https://github.com/Livefyre/Livefyre.js) 사이트를 추가합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 미디어 벽이 나타날 요소를 배치합니다.

```
<div id="wall"></div>
```

마지막으로 구성 요소를 `Livefyre.require` 구성하는 데 사용합니다.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

이제 벽도 있잖아! 이 [예에서는](https://codepen.io/gobengo/pen/dFwDL)이 모든 것을 확인하십시오.

**오류가 발생합니까?** 올바른 환경 매개 변수를 전달하는지 확인하십시오. 옵션에는 `livefyre.com` (프로덕션) 또는 `t402.livefyre.com` (UAT)가 포함됩니다.

>[!NOTE]
>
>미디어 담벼락 앱에서 렌더링된 트윗의 스타일링 맞춤화는 Twitter의 표시 요구 사항에 따라 수행해야 [합니다](https://dev.twitter.com/terms/display-requirements).

## 구성 옵션 {#section_ucv_qvb_c1b}

`columns`

벽을 구성할 때 미디어 담벼락의 열 수를 정의할 수 있습니다. 이 옵션을 설정하면 지정된 열 수를 유지하면서 각 열의 너비가 미디어 담벼락의 컨테이너 크기에 맞게 자동으로 조정됩니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

페이지 로드 시 렌더링할 컨텐츠 항목의 수입니다. 기본값은 50입니다.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

미디어 담벼락의 컨테이너 요소 내에서 각 열에 대한 최소(픽셀) 너비를 설정할 수 있습니다. 미디어 벽은 컨테이너 요소의 폭에 따라 적절한 수의 열을 자동으로 선택합니다. 기본적으로 미디어 벽의 너비는 최소 컨텐츠 너비(정의되지 않은 경우 300px)로 나누어져 열 수를 결정합니다.

>[!NOTE]
>
>열 옵션과 함께 이 옵션을 사용하지 마십시오.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

기본적으로 일부 컨텐츠에 대한 첨부 파일이 있으면 미디어 벽은 클릭 가능한 축소판을 표시합니다. 클릭하면 앱은 사진/비디오 첨부 파일을 전체적으로 표시하는 모달을 엽니다. 이 옵션을 비활성화하려면 modal을 false로 설정합니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

벽에 표시할 [!UICONTROL Post Content] 단추를 정의합니다. 이 옵션을 사용하려면 `opts.collection`전달하여 Livefyre.js 인증 통합을 페이지에 추가해야 합니다.

`postButton` 매개 변수:

* `false` (기본값):게시물 컨텐츠 단추를 표시하지 않습니다. (읽기 전용 미디어 벽을 만듭니다.)
* `true` (또는 `LiveMediaWall.postButtons.contentWithPhotos`):사용자가 첨부된 사진과 함께 텍스트 컨텐츠를 추가할 수 있는 단추를 포함합니다.

* `LiveMediaWall.postButtons.content`:사용자가 사진을 첨부하지 않고 텍스트 컨텐츠를 추가할 수 있는 단추를 포함합니다.
* `LiveMediaWall.postButtons.photo`:사용자가 사진을 추가할 수 있지만 텍스트는 추가할 수 있는 단추를 포함합니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

단추를 클릭할 때 담벼락에 추가할 컨텐츠 항목의 수를 [!UICONTROL Show More] 정의합니다.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 스타일 구성 옵션 {#section_ztv_dvb_c1b}

또한 Media Wall은 텍스트 색상, 스타일 및 크기를 사용자 정의할 수 있는 여러 구성 옵션을 제공합니다. 이러한 옵션을 구현하려면 다음 구문을 사용하십시오.

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

유효한 입력은 CSS 글꼴 제품군, 글꼴 크기 [,](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)줄 높이 [및](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)색상 [속성에 대한 W3C 표준을](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) 참조하십시오 [.](https://www.w3.org/TR/css3-color/#colorunits) 색상 및 색상속성을 참조하십시오.

* **bodyFontSize** *(CSS 글꼴 크기 문자열)* 컨텐츠 본문 텍스트의 글꼴 크기입니다.

* **bodyLineHeight***(CSS Line Height String)* 컨텐츠 본문 텍스트의 선 높이입니다.

* **buttonActiveBackgroundColor***(CSS 색상 문자열)** 활성 상태의 단추 배경에 대한 색입니다.

* **buttonBorderColor** *(CSS 색상 문자열)** 단추 테두리의 색상입니다.

* **buttonHoverBackgroundColor***(CSS 색상 문자열)* 단추 배경을 가리키는 색입니다.

* **buttonTextColor***(CSS 색상 문자열)* 단추 레이블의 색상입니다.

* **cardBackgroundColor***(CSS Color String)* 미디어 담벼락의 컨텐츠 카드에 대한 배경색입니다.

* **displayNameColor***(CSS 색상 문자열)* 필자의 표시 이름에 대한 색상입니다.

* **fontFamily***(CSS Font Family String)* 본문 텍스트의 글꼴 모음입니다.

* **footerText** Color *(CSS 색상 문자열)* 보조 텍스트의 색상(예: 바닥글 텍스트 및 행의 사용자 이름)입니다.

* **linkAttachmentBackgroundColor***(CSS 색상 문자열)* 링크 첨부(누적 첨부 파일)에 대한 배경색입니다.

* **linkAttachmentBorderColor***(CSS 색상 문자열)* 링크 첨부(누적 첨부 파일)에 대한 테두리 색입니다.

* **linkAttachmentTextColor***(CSS 색상 문자열)* 링크 첨부 텍스트의 색상입니다.

* **linkColor** (CSS *색상 문자열)* 하이퍼링크의 색입니다(본문 텍스트의 링크 및 표시 이름 링크).

* **textColor** (CSS *색상 문자열)* 본문 텍스트의 색상입니다.

* **titleFontSize** *(CSS 글꼴 크기 문자열)* 컨텐츠 제목의 글꼴 크기입니다.

* **titleLineHeight** *(CSS 행 높이 문자열)* 컨텐츠 제목의 행 높이입니다.

* **sourceLogoColor***(CSS 색상 문자열)* 소스 로고의 색상입니다.

* **username** Color *(CSS Color String)* 필자의 사용자 이름 색상입니다.
