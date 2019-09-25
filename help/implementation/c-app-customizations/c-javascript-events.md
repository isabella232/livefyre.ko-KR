---
description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-title: JavaScript 이벤트 정의 및 예제
solution: Experience Manager
title: JavaScript 이벤트 정의 및 예제
uuid: 61da2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# JavaScript 이벤트 정의 및 예제{#javascript-events-definitions-and-examples}

대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다. 예를 들어 사용자가 Twitter 또는 Facebook에 컨텐츠를 좋아하거나 공유할 때 또는 새 컨텐츠가 게시될 때 페이지를 업데이트할 수 있습니다.

또한 Livefyre를 사용하면 타사 분석 통합(Adobe Analytics JS, Google Analytics, 다이내믹 태그 관리 등)에 이벤트를 추가하여 앱 이벤트를 추적할 수 있습니다. 자세한 내용은 타사 통합 관리자와 협력하여 올바른 이벤트를 제공합니다.

이러한 이벤트에 바인딩하려면 페이지에서 앱을 인스턴스화할 때 다음 코드를 페이지에 추가하십시오. 이벤트 이름 대체 `{eventName}`:

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
>데이터 개체는 모든 이벤트 핸들러에 대해 제공됩니다. 데이터 개체의 예는 각 이벤트를 따릅니다.

## commentPosted {#section_qfr_51p_xz}

사용자가 댓글을 게시했습니다.

* null의 상위는 새 주석입니다.
* [없음]의 상위 항목은 편집된 주석입니다.
* 상위의 수는 응답의 상위 ID입니다.

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

## commentFlagged {#section_szy_s1p_xz}

사용자가 댓글에 플래그를 지정했습니다.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

사용자가 댓글을 좋아했습니다.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

사용자가 스트림에서 댓글을 공유했습니다. (이 이벤트는 사용자가 주석 편집기에서 공유할 때 발생하지 않습니다.) 이 이벤트는 [공유] 단추를 클릭하면 트리거됩니다.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

이 대화에서 표시되는 주석의 총 수가 변경되었습니다(증가하거나 감소됨).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

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

## userLoggedOut {#section_tsg_5z4_xz}

사용자가 로그아웃되었습니다.

데이터가 정의되지 않았습니다.

## socialEmotion {#section_a1w_tz4_xz}

사용자가 댓글에 @mention을 포함했습니다. 다음 배열을 반환합니다.

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatures

중재자 사용자가 댓글을 달았습니다. 다음 배열을 반환합니다.

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

주석 스트림이 로드되었으며 초기 컨텐츠 세트가 서버에서 가져와서 사용자에게 표시됩니다.

데이터가 정의되지 않았습니다.

## showMore {#section_pqg_nz4_xz}

사용자가 **[!UICONTROL Show More]** 단추를 클릭했습니다.

데이터가 정의되지 않았습니다.

## userFollow {#section_xxw_jz4_xz}

사용자가 **[!UICONTROL Follow]** 단추를 클릭하면 true를 반환하고 내용이 스트림에 게시되면 false를 반환합니다.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollowed {#section_wm1_gz4_xz}

사용자가 [언팔로우] **단추를** 클릭하면 true를 반환하고, 콘텐츠가 스트림에 게시되면 false를 반환합니다.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

