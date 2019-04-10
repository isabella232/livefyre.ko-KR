---
description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-title: JavaScript 이벤트 정의 및 예제
solution: Experience Manager
title: JavaScript 이벤트 정의 및 예제
uuid: 61 DA 2 E 2 E -8 FCD -482 D -93 DF-C 946 F 0475277
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# JavaScript 이벤트 정의 및 예제{#javascript-events-definitions-and-examples}

대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다. 예를 들어 사용자가 Twitter 또는 Facebook와 같은 또는 새 컨텐츠가 게시될 때 페이지를 업데이트하려는 경우 페이지를 업데이트할 수 있습니다.

또한 Livefyre 에서는 타사 분석 통합 (Adobe Analytics JS, Google Analytics, 다이내믹 태그 관리 등) 에 이벤트를 추가하여 앱 이벤트를 추적할 수 있습니다. 자세한 내용은 타사 통합 관리자와 협력하여 올바른 이벤트를 제공하십시오.

이러한 이벤트에 바인딩하려면 페이지에서 앱을 인스턴스화할 때 다음 코드를 페이지에 추가합니다. 이벤트 이름 대체 `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>데이터 객체는 모든 이벤트 핸들러에 대해 제공됩니다. 예제 데이터 개체는 각 이벤트를 따릅니다.

## 댓글 게시됨 {#section_qfr_51p_xz}

사용자가 댓글을 게시했습니다.

* null의 상위는 새 댓글입니다.
* None의 상위는 편집된 댓글입니다.
* For parent는 회신의 상위 ID 입니다.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## Commentflag {#section_szy_s1p_xz}

사용자가 댓글을 지정했습니다.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## Commentliked {#section_vc1_r1p_xz}

사용자가 댓글을 좋아했습니다.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## Commentshared {#section_nqb_31p_xz}

사용자가 스트림에서 주석을 공유했습니다. 이 이벤트는 사용자가 댓글 편집기에서 공유할 때 실행되지 않습니다. 이 이벤트는 [공유] 단추를 클릭하면 실행됩니다.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## Commentcountupdated {#section_qdq_f1p_xz}

이 대화의 총 표시 댓글 수가 변경되었습니다 (증가 또는 감소).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## Userloggedin {#section_yjt_vz4_xz}

사용자가 로그인했습니다.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## Userloggedout {#section_tsg_5z4_xz}

사용자가 로그아웃되었습니다.

데이터가 정의되지 않았습니다.

## socialmention {#section_a1w_tz4_xz}

사용자가 주석에 @ 언급을 포함했습니다. 다음 배열을 반환합니다.

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## Commentfeatured

중재자 사용자가 댓글을 작성했습니다. 다음 배열을 반환합니다.

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## Initialrendercomplete {#section_odc_4z4_xz}

주석 스트림이 로드되고 초기 컨텐츠 집합이 서버에서 가져와 사용자에게 표시되었습니다.

데이터가 정의되지 않았습니다.

## Showmore {#section_pqg_nz4_xz}

사용자가 단추를 **[!UICONTROL Show More]** 클릭했습니다.

데이터가 정의되지 않았습니다.

## Userfollowed {#section_xxw_jz4_xz}

사용자가 **[!UICONTROL Follow]** 단추를 클릭할 때 true를 반환하고 콘텐트가 스트림에 게시되면 false를 반환합니다.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## Userunfollowed {#section_wm1_gz4_xz}

사용자가 **[언로우** ] 단추를 클릭할 때 true를 반환하고 콘텐트가 스트림에 게시되면 false를 반환합니다.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

