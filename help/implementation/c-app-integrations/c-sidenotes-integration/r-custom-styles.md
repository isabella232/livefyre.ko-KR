---
description: 사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.
seo-description: 사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.
seo-title: 사이드노트 사용자 지정 스타일
title: 사이드노트 사용자 지정 스타일
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# 사이드노트 사용자 지정 스타일{#sidenotes-custom-styles}

사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.

&quot;keys&quot;는 DOM 요소를 나타내는 개체 키이고, &quot;속성&quot;은 특정 키에 대해 지원되는 CSS 속성입니다. 예를 들어, blockBtn(사이드노트 팝오버를 시작하는 단추)의 스타일을 사용자 정의하려면 다음과 같은 객체를 만듭니다.

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **키** | **속성** | 설명 |
|---|---|---|
| `anonymousAvatar` | &#39;height&#39;, &#39;width&#39; | 텍스트 영역 편집기의 왼쪽에 있는 익명의 아바타 이미지. |
| `blockBtn` | &#39;fontColor&#39;, &#39;fontSize&#39;, &#39;left&#39;, &#39;position&#39;, &#39;right&#39;, &#39;top&#39; | &quot;실행(Launcher) 아이콘&quot;이 sidecote로 지정된 요소 옆에 배치됩니다. |
| `blockBtnActive` | &#39;fontColor&#39;, &#39;fontSize&#39;, &#39;left&#39;, &#39;position&#39;, &#39;right&#39;, &#39;top&#39; | 활성 상태인 경우 시작 아이콘. |
| `commentAvatar` | &#39;height&#39;, &#39;width&#39; | 상단 메모 왼쪽에 있는 아바타 이미지. |
| `commentBody` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 스레드된 메모의 텍스트 본문. |
| `commentDisplayName` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 메모를 남긴 사용자의 표시 이름입니다. |
| `commentDownvote` | &#39;fontColor&#39;, &#39;fontSize&#39; | 메모에 있는 [다운로드] 단추. |
| `commentReplyExpand` | &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 많은 수의 답글이 있는 스레드 확장 단추. |
| `commentTags` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 메모에 있는 사용자에 대한 태그입니다. |
| `commentUpvote` | &#39;fontColor&#39;, &#39;fontSize&#39; | 메모에 있는 [투표] 단추. |
| `editorTextarea` | &#39;height&#39;, &#39;width&#39;, &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 메모를 남길 수 있는 텍스트 영역 입력 상자 |
| `mediaBlockBtn` | &#39;fontColor&#39;, &#39;fontSize&#39;, &#39;left&#39;, &#39;position&#39;, &#39;right&#39;, &#39;top&#39; | 미디어 항목(img, video) 위에 있을 때 미디어 시작 아이콘. |
| `mediaBlockBtnActive` | &#39;fontColor&#39;, &#39;fontSize&#39;, &#39;left&#39;, &#39;position&#39;, &#39;right&#39;, &#39;top&#39; | 활성 상태의 미디어 실행 아이콘 |
| `numSidenotes` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39;, &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;height&#39;, &#39;width&#39; | 컬렉션에 있는 사이드노트 수를 보여주는 클릭 가능 단추. |
| `numSidenotesPopover` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39;, &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;height&#39;, &#39;width&#39; | 사용자를 위한 Sidecotes에 대한 간단한 설명이 있는 팝업 메뉴 |
| `popover` | &#39;backgroundColor&#39; | 런처 아이콘이 호출될 때 표시되는 팝업입니다. |
| `popoverArrowLeft` | &#39;backgroundImage&#39;, &#39;height&#39;, &#39;left&#39;, &#39;right&#39;, &#39;top&#39;, &#39;width&#39; | 런처 아이콘이 포함된 DOM 요소를 가리키는 팝업의 왼쪽 화살표 요소입니다. |
| `popoverArrorRight` | &#39;backgroundImage&#39;, &#39;height&#39;, &#39;left&#39;, &#39;right&#39;, &#39;top&#39;, &#39;width&#39; | 시작 관리자 아이콘이 포함된 DOM 요소를 가리키는 팝업의 오른쪽 화살표 요소입니다. |
| `popoverArrowTop` | &#39;backgroundImage&#39;, &#39;height&#39;, &#39;left&#39;, &#39;right&#39;, &#39;top&#39;, &#39;width&#39; | 시작 관리자 아이콘이 포함된 DOM 요소를 가리키는 팝업에서 위쪽 화살표 요소입니다. |
| `replyAvatar` | &#39;height&#39;, &#39;width&#39; | 댓글 수준 메모 왼쪽에 있는 아바타 이미지. |
| `streamPoweredBy` | &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;lineHeight&#39; | &quot;Powered by&quot; footer on the popover. |
| `streamQueueButton` | &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 새 노트가 열린 팝업으로 스트리밍되는 시기를 나타내는 단추입니다. |
| `userAvatar` | &#39;height&#39;, &#39;width&#39; | 인증된 사용자의 아바타 이미지를 텍스트 영역 편집기의 왼쪽에 표시합니다. |

