---
description: 컨텐츠 스트리밍이 실시간으로 포함된 미디어 월을 만들 수 있습니다.
seo-description: 컨텐츠 스트리밍이 실시간으로 포함된 미디어 월을 만들 수 있습니다.
seo-title: 미디어 담벼락
solution: Experience Manager
title: 미디어 담벼락
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 미디어 담벼락{#media-wall}

컨텐츠 스트리밍이 실시간으로 포함된 미디어 월을 만들 수 있습니다.

미디어 월을 사용하면 사이트에 대한 실시간 소셜 담벼락을 만들 수 있습니다. Livefyre JavaScript SDK의 streamhub-wallpackage를 사용하여 라이브 이벤트 처리, 사진 콘테스트 호스팅, 웹 사이트의 소셜 섹션 강화 등에 유용한 라이브 매력적인 전체 화면의 타일 컨텐츠 컨텐츠로 Livefyre 소셜 피드를 표시할 수 있습니다.

## 통합 {#section_jfm_bwb_c1b}

미디어 월을 추가하는 가장 빠른 방법은 Livefyre의 CDN에 호스팅된 내장 버전을 사용하는 것입니다.

먼저 [livefyre. js](https://github.com/Livefyre/Livefyre.js) 를 사이트에 추가합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

그런 다음 미디어 벽이 나타날 요소를 배치합니다.

```
<div id="wall"></div>
```

마지막으로 구성 요소를 구성하는 `Livefyre.require` 데 사용합니다.

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

이제 벽이 있습니다. 이 예에서는 이 모든 작업을 [직접 확인해](https://codepen.io/gobengo/pen/dFwDL)보십시오.

**오류를 발견하시겠습니까?** 올바른 환경 매개 변수를 전달하는지 확인하십시오. 옵션에는 `livefyre.com` (프로덕션) 또는 `t402.livefyre.com` (UAT) 이 있습니다.

>[!NOTE]
>
>미디어 담벼락 앱에서 렌더링하는 트윗의 스타일 지정 사용자 지정 기능은 Twitter [의 디스플레이 요구 사항에 따라 수행해야](https://dev.twitter.com/terms/display-requirements)합니다.

## 구성 옵션 {#section_ucv_qvb_c1b}

`columns`

담벼락 구성 시 미디어 담벼락에 대한 열 수를 정의할 수 있습니다. 이 옵션이 설정되면, 각 열의 폭은 지정된 개수의 열을 유지하면서 미디어 벽의 컨테이너 크기에 맞게 자동으로 조정됩니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

페이지 로드 시 렌더링할 컨텐츠 항목의 수입니다. 기본값은 50 입니다.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

미디어 벽의 컨테이너 요소 내에서 각 열에 대한 최소 (픽셀) 너비를 설정할 수 있습니다. (미디어 담벼락에 컨테이너 요소의 너비에 따라 적절한 수의 열이 자동으로 선택됩니다. 기본적으로 미디어 담벼락 너비를 최소 컨텐츠 폭 (정의되지 않은 경우 300 px) 로 나누면 열 수가 결정됩니다.)

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

기본적으로 컨텐츠 일부에 대한 첨부 파일이 있으면 미디어 벽은 클릭 가능한 썸네일을 표시합니다. 클릭하면 앱이 사진/비디오 첨부 파일을 완전히 표시하는 모달 창이 열립니다. 이 옵션을 비활성화하려면 modal를 false로 설정합니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

벽에 [!UICONTROL Post Content] 표시할 단추를 정의합니다. 이 옵션을 사용하려면 이 옵션을 전달해야 `opts.collection`하며 livefyre. js 인증 통합을 페이지에 추가해야 합니다.

`postButton` 매개 변수:

* `false` (기본값): [콘텐트 게시] 단추를 표시하지 마십시오. (읽기 전용 미디어 월을 만듭니다.)
* `true` (또는 `LiveMediaWall.postButtons.contentWithPhotos`): 첨부된 사진이 있는 텍스트 컨텐츠를 추가할 수 있는 단추를 포함할 수 있습니다.

* `LiveMediaWall.postButtons.content`: 사용자가 텍스트 컨텐츠를 추가할 수 있지만 사진을 첨부할 수는 없도록 해주는 단추를 포함할 수 있습니다.
* `LiveMediaWall.postButtons.photo`: 사용자가 사진을 추가할 수 있지만 텍스트를 추가할 수 있는 단추를 포함할 수 있습니다.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

단추를 클릭할 때 담벼락에 추가할 컨텐츠 항목의 [!UICONTROL Show More] 수를 정의합니다.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 스타일링 구성 옵션 {#section_ztv_dvb_c1b}

미디어 담벼락에서는 텍스트 색상, 스타일 및 크기를 사용자 정의할 수 있는 다양한 구성 옵션도 제공합니다. 이러한 옵션을 구현하려면 다음 구문을 사용하십시오.

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

유효한 입력이 필요하면 CSS [글꼴 모음](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [글꼴 크기](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [행 높이](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) 및 [색상](https://www.w3.org/TR/css3-color/#colorunits) 속성에 대한 W 3 C 표준을 참조하십시오.

* **Bodyfontsize** *(CSS 글꼴 크기 문자열)* 컨텐츠 본문 텍스트의 글꼴 크기입니다.

* **Bodylineheight** *(CSS line height 문자열)* 컨텐츠 본문 텍스트의 줄 높이입니다.

* **Buttonactivebackgroundcolor** *(CSS 색상 문자열)** 활성 상태의 단추 배경의 색상입니다.

* **Buttonbordercolor** *(CSS 색상 문자열)** 단추 테두리의 색상입니다.

* **Buttonhoverbackgroundcolor** *(CSS 색상 문자열)* 마우스를 가리키면 단추 배경의 색상이 표시됩니다.

* **Buttontextcolor** *(CSS 색상 문자열)* 단추 레이블의 색상입니다.

* **Cardbackgroundcolor** *(CSS 색상 문자열)* 미디어 담벼락의 내용 카드에 대한 배경색입니다.

* **Displaynamecolor** *(CSS 색상 문자열)* 필라인의 표시 이름에 대한 색상입니다.

* **Fontfamily** *(CSS 글꼴 모음 문자열)* 본문 텍스트에 대한 글꼴 모음입니다.

* **Footertextcolor** *(CSS 색상 문자열)* 보조 텍스트 (예: 바닥글 텍스트 및 필인의 사용자 이름) 의 색상입니다.

* **Linkattachmentbackgroundcolor** *(CSS 색상 문자열)* 링크 첨부 파일의 배경색입니다 (누적 첨부 파일).

* **Linkattachmentbordercolor** *(CSS 색상 문자열)* 링크 첨부 파일의 테두리 색상 (누적 첨부 파일) 입니다.

* **Linkattachmenttextcolor** *(CSS 색상 문자열)* 첨부 파일 링크의 색상입니다.

* **Linkcolor** *(CSS 색상 문자열)* 하이퍼링크 색상 (예: 본문 텍스트의 링크 및 표시 이름 링크)

* **Textcolor** *(CSS 색상 문자열)* 본문 텍스트에 대한 색상입니다.

* **Titlefontsize** *(CSS 글꼴 크기 문자열)* 컨텐츠 제목의 글꼴 크기입니다.

* **Titlelineheight** *(CSS line height 문자열)* 컨텐츠 제목의 줄 높이입니다.

* **Sourcelogocolor** *(CSS 색상 문자열)* 소스 로고의 색상입니다.

* **Usernamecolor** *(CSS 색상 문자열)* 필라인의 username에 대한 색상입니다.
