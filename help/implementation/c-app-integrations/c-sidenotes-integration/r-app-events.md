---
description: Sidenotes의 인스턴스에서 이벤트를 들을 수 있습니다.
seo-description: Sidenotes의 인스턴스에서 이벤트를 들을 수 있습니다.
seo-title: Sidenotes 앱 이벤트
solution: Experience Manager
title: Sidenotes 앱 이벤트
uuid: AFCA 4 B 03-C 370-41 CA-AA 12-45 BC 357517 CA
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes 앱 이벤트 {#sidenotes-app-events}

Sidenotes의 인스턴스에서 이벤트를 들을 수 있습니다.

콜백은 메서드와 함께 등록 및 등록되지 않은 `onmethod` 상태로 등록할 `removeListener` 수 있습니다. 콜백을 `once` 한 번만 호출한 다음 등록 취소하면 편리하게 메서드를 사용할 수 있습니다.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Livefyre 이벤트에 대한 자세한 내용은 참조 섹션의 JavaScript Events 페이지를 참조하십시오.

| key | 설명 |
|--- |--- |
| sidenotes. initialized | 앱이 인스턴스화되고, 데이터가 있고, 페이지에 있을 때 실행됩니다. |
| sidenotes. commentflag | 댓글에 플래그가 지정되었을 때 실행됩니다. 데이터 포함: <br><ul><li>`targetId`: 플래그가 달린 주석 ID</li><li>`type`: 플래그 유형 문자열 `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 댓글이 게시되면 실행됩니다. 데이터 포함: <br><ul><li> `authorId`: 댓글 작성자의 ID </li><li>`bodyHtml`: 주석 본문 </li><li> `parent`: 댓글 상위의 ID 또는 null</li></ul> |
| `sidenotes.commentShared` | 댓글이 공유되면 실행됩니다. 데이터 포함: <br><ul><li>`targetId`: 공유된 주석 ID </li><li> `sharedToFacebook`: 댓글이 Facebook에 공유되었는지 여부 </li><li>`sharedToTwitter`: 주석이 Twitter로 공유되었는지 여부</li></ul> |
| `sidenotes.commentVoted` | 댓글이 투표되면 실행됩니다. 데이터 포함: <br><ul><li>`targetId`: 투표한 댓글의 ID </li><li> `targetAuthorId`: 댓글이 투표된 작성자의 ID</li><li> `type`: 숫자 투표 유형: 0: ' clear ', 1: ' upvote'또는 2: ' downvote '</li></ul> |
| `sidenotes.userLoggedIn` | 사용자가 로그인할 때 실행됩니다. 데이터 포함: <br><ul><li>`avatar`: 사용자를 위한 아바타 URL </li><li>`displayName`: 사용자의 표시 이름</li><li>`id`: 사용자의 ID</li><li> `isModerator`: 사용자가 현재 컬렉션의 중재자인지 여부</li></ul> |
| `sidenotes.userLoggedOut` | 사용자가 로그아웃할 때 호출됩니다. |
