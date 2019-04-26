---
description: 사용자 지정 스타일은 Sidenotes 생성자에 주입된 개체를 통해 적용됩니다.
seo-description: 사용자 지정 스타일은 Sidenotes 생성자에 주입된 개체를 통해 적용됩니다.
seo-title: Sidenotes 사용자 정의 스타일
title: Sidenotes 사용자 정의 스타일
uuid: 0 F 6 D 7 AD 6-1 F 6 A -4 ED 2-B 86 A -0 D 03782 E 591 E
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sidenotes 사용자 정의 스타일{#sidenotes-custom-styles}

사용자 지정 스타일은 Sidenotes 생성자에 주입된 개체를 통해 적용됩니다.

«keys» 는 DOM 요소를 나타내는 개체 키이고, «properties» 는 특정 키에 대한 CSS 속성입니다. 예를 들어, Blockbtn (sidenotes popover를 실행하는 단추) 의 스타일을 사용자 정의하려면 다음과 같은 개체가 만들어집니다.

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

| **key** | **속성** | 설명 |
|---|---|---|
| `anonymousAvatar` | ' height ',' width ' | 텍스트 영역 편집기의 왼쪽에 있는 익명의 아바타 이미지입니다. |
| `blockBtn` | ' Fontcolor ',' fontsize ',' Left ',' Position ',' Right ',' Top ' | [시작] 로 지정된 요소 옆에 배치된 "launcher 아이콘". |
| `blockBtnActive` | ' Fontcolor ',' fontsize ',' Left ',' Position ',' Right ',' Top ' | Launcher 아이콘이 표시됩니다. |
| `commentAvatar` | ' height ',' width ' | 최상위 수준 메모 왼쪽에 있는 아바타 이미지입니다. |
| `commentBody` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | 스레드된 메모의 텍스트 본문입니다. |
| `commentDisplayName` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | 메모를 남긴 사용자의 표시 이름입니다. |
| `commentDownvote` | ' Fontcolor ',' fontsize ' | Downvote 단추를 클릭합니다. |
| `commentReplyExpand` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | 많은 답글이 있는 스레드를 확장하는 단추입니다. |
| `commentTags` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | 사용자에 대한 태그를 참조하십시오. |
| `commentUpvote` | ' Fontcolor ',' fontsize ' | [투표 중] 단추를 클릭합니다. |
| `editorTextarea` | ' height ',' width ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Textarea 입력 상자를 참조하십시오. |
| `mediaBlockBtn` | ' Fontcolor ',' fontsize ',' Left ',' Position ',' Right ',' Top ' | 미디어 항목 (img, 비디오) 위쪽에 있는 미디어 시작 아이콘. |
| `mediaBlockBtnActive` | ' Fontcolor ',' fontsize ',' Left ',' Position ',' Right ',' Top ' | 활성 상태의 미디어 시작 아이콘 |
| `numSidenotes` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' Height ',' Width ' | 컬렉션에서 Sidenotes 수를 표시하는 클릭 가능한 단추입니다. |
| `numSidenotesPopover` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' Height ',' Width ' | 사용자의 Sidenotes에 대한 간단한 설명을 제공합니다. |
| `popover` | ' Backgroundcolor ' | Launcher 아이콘이 호출되면 표시되는 팝업입니다. |
| `popoverArrowLeft` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | 시작 아이콘이 있는 DOM 요소를 가리키는 포매터에 있는 왼쪽 화살표 요소입니다. |
| `popoverArrorRight` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | 시작 아이콘이 있는 DOM 요소를 가리키는 팝오버 오른쪽 화살표 요소입니다. |
| `popoverArrowTop` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | 시작 아이콘이 있는 DOM 요소를 가리키는 팝오버 위의 위쪽 화살표 요소입니다. |
| `replyAvatar` | ' height ',' width ' | 댓글 수준 메모 왼쪽에 있는 아바타 이미지입니다. |
| `streamPoweredBy` | ' Backgroundcolor ',' bordercolor ',' lineheight ' | " Powered by "footer on the popover. |
| `streamQueueButton` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | 새 노트 스트림을 열려 있는 팝업으로 표시할 시기를 나타내는 단추입니다. |
| `userAvatar` | ' height ',' width ' | 텍스트 영역 편집기의 왼쪽에 있는 인증된 사용자의 아바타 이미지입니다. |

