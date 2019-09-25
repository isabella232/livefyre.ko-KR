---
description: 사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.
seo-description: 사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.
seo-title: 사이드노트 사용자 지정 스타일
title: 사이드노트 사용자 지정 스타일
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 사이드노트 사용자 지정 스타일{#sidenotes-custom-styles}

사용자 지정 스타일은 Sidecotes 생성자에 삽입된 객체를 통해 적용됩니다.

"keys"는 DOM 요소를 나타내는 개체 키이고, "properties"는 특정 키에 대해 지원되는 CSS 속성입니다. 예를 들어, blockBtn(Sidecotes 팝업을 시작하는 단추)의 스타일을 사용자 정의하려면 다음과 같은 개체를 만듭니다.

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
| `anonymousAvatar` | 'height', 'width' | 텍스트 영역 편집기의 왼쪽에 있는 익명의 아바타 이미지. |
| `blockBtn` | 'fontColor', 'fontSize', 'left', 'position', 'right', 'top' | sidecenote로 지정된 요소 옆에 "실행 프로그램 아이콘"이 배치됩니다. |
| `blockBtnActive` | 'fontColor', 'fontSize', 'left', 'position', 'right', 'top' | 활성 상태인 경우 시작 아이콘. |
| `commentAvatar` | 'height', 'width' | 최상위 노트의 왼쪽에 있는 아바타 이미지. |
| `commentBody` | 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 스레드된 메모의 텍스트 본문입니다. |
| `commentDisplayName` | 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 메모를 남긴 사용자의 표시 이름입니다. |
| `commentDownvote` | 'fontColor', 'fontSize' | 메모에 있는 [다운로드 투표] 단추 |
| `commentReplyExpand` | 'backgroundColor', 'borderColor', 'borderWidth', 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 답글이 많은 스레드를 확장하는 단추입니다. |
| `commentTags` | 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 메모에 있는 사용자에 대한 태그입니다. |
| `commentUpvote` | 'fontColor', 'fontSize' | 메모에 대한 투표 단추. |
| `editorTextarea` | 'height', 'width', 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 메모를 남길 수 있는 텍스트 영역 입력 상자 |
| `mediaBlockBtn` | 'fontColor', 'fontSize', 'left', 'position', 'right', 'top' | 미디어 항목(img, video) 위에 있을 때 미디어 시작 아이콘 |
| `mediaBlockBtnActive` | 'fontColor', 'fontSize', 'left', 'position', 'right', 'top' | 활성 상태의 미디어 실행 프로그램 아이콘 |
| `numSidenotes` | 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight', 'backgroundColor', 'borderColor', 'borderWidth', 'height', 'width' | 컬렉션에 있는 사이드 노트 수를 보여주는 클릭 가능 단추. |
| `numSidenotesPopover` | 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight', 'backgroundColor', 'borderColor', 'borderWidth', 'height', 'width' | 사용자를 위한 Sidecnotes에 대한 간단한 설명과 함께 팝업 창을 표시합니다. |
| `popover` | 'backgroundColor' | 실행 프로그램 아이콘이 호출될 때 표시되는 팝업입니다. |
| `popoverArrowLeft` | 'backgroundImage', 'height', 'left', 'right', 'top', 'width' | 실행 시작 아이콘이 포함된 DOM 요소를 가리키는 팝업의 왼쪽 화살표 요소입니다. |
| `popoverArrorRight` | 'backgroundImage', 'height', 'left', 'right', 'top', 'width' | 시작 관리자 아이콘이 포함된 DOM 요소를 가리키는 팝업 창의 오른쪽 화살표 요소입니다. |
| `popoverArrowTop` | 'backgroundImage', 'height', 'left', 'right', 'top', 'width' | 실행 프로그램 아이콘이 포함된 DOM 요소를 가리키는 팝업 상단의 화살표 요소입니다. |
| `replyAvatar` | 'height', 'width' | 회신 수준 메모 왼쪽에 있는 아바타 이미지. |
| `streamPoweredBy` | 'backgroundColor', 'borderColor', 'lineHeight' | "Powered by" footer on the poolver. |
| `streamQueueButton` | 'backgroundColor', 'borderColor', 'borderWidth', 'fontColor', 'fontFamily', 'fontSize', 'fontWeight', 'lineHeight' | 새 메모가 열린 팝업으로 스트리밍되는 시기를 나타내는 단추입니다. |
| `userAvatar` | 'height', 'width' | 인증된 사용자의 아바타 이미지를 텍스트 영역 편집기 왼쪽에 표시합니다. |

