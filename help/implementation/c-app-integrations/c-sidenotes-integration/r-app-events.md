---
description: 사이드노트의 인스턴스에서 이벤트를 들을 수 있습니다.
seo-description: 사이드노트의 인스턴스에서 이벤트를 들을 수 있습니다.
seo-title: 사이드노트 앱 이벤트
solution: Experience Manager
title: 사이드노트 앱 이벤트
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 사이드노트 앱 이벤트 {#sidenotes-app-events}

사이드노트의 인스턴스에서 이벤트를 들을 수 있습니다.

콜백은 `onmethod`에 등록되고 `removeListener` 메서드로 등록을 취소할 수 있습니다. 콜백을 한 번만 호출한 다음 등록을 취소하면 편의를 위해 `once` 메서드를 사용할 수 있습니다.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Livefyre 이벤트에 대한 자세한 내용은 참조 섹션의 JavaScript 이벤트 페이지를 참조하십시오.

| 키 | 설명 |
|--- |--- |
| sidenotes.initialized | 앱이 인스턴스화되고, 데이터가 있으며, 페이지에 있을 때 실행됩니다. |
| sidenotes.commentFlagged | 댓글에 플래그가 지정되면 실행됩니다. 데이터에는 다음이 포함됩니다.<br><ul><li>`targetId`:플래그가 지정된 댓글의 id</li><li>`type`:플래그 유형 문자열  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 댓글이 게시되면 실행됩니다. 데이터에는 다음이 포함됩니다.<br><ul><li> `authorId`:주석 작성자 id </li><li>`bodyHtml`:주석의 본문 </li><li> `parent`:주석의 부모 id 또는 null</li></ul> |
| `sidenotes.commentShared` | 댓글이 공유되었을 때 실행됩니다. 데이터에는 다음이 포함됩니다.<br><ul><li>`targetId`:공유된 주석의 id </li><li> `sharedToFacebook`:댓글이 Facebook에 공유되었는지 여부 </li><li>`sharedToTwitter`:댓글이 Twitter에 공유되었는지 여부</li></ul> |
| `sidenotes.commentVoted` | 댓글이 표결에 부쳐졌을 때 해고된다. 데이터에는 다음이 포함됩니다.<br><ul><li>`targetId`:투표된 주석 id </li><li> `targetAuthorId`:댓글이 투표된 작성자의 id</li><li> `type`:숫자 투표 유형:0:&#39;clear&#39;, 1:&#39;업투표&#39; 또는 2:&#39;다운투표&#39;</li></ul> |
| `sidenotes.userLoggedIn` | 사용자가 로그인할 때 실행됩니다. 데이터에는 다음이 포함됩니다.<br><ul><li>`avatar`:사용자의 아바타 url </li><li>`displayName`:사용자의 표시 이름</li><li>`id`:사용자의 id</li><li> `isModerator`:사용자가 현재 컬렉션의 중재자인지 여부</li></ul> |
| `sidenotes.userLoggedOut` | 사용자가 로그아웃할 때 실행됩니다. |
