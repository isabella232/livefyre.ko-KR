---
description: 앱에서 표준 Livefyre 앱 구성 요소를 제거합니다.
seo-description: 앱에서 표준 Livefyre 앱 구성 요소를 제거합니다.
seo-title: 앱 요소 숨기기
solution: Experience Manager
title: 앱 요소 숨기기
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 앱 요소 숨기기{#hide-app-elements}

앱에서 표준 Livefyre 앱 구성 요소를 제거합니다.

CSS를 사용하여 페이지에서 기본 Livefyre 앱 요소를 숨겨 필요에 맞게 사용자 경험을 사용자 정의할 수 있습니다.

앱에서 요소를 숨기려면 표시를 없음으로 설정하면 됩니다.

예:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```

