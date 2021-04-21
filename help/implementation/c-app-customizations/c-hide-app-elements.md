---
description: 앱에서 표준 Livefyre 앱 구성 요소를 제거합니다.
title: 앱 요소 숨기기
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# 앱 요소 숨기기{#hide-app-elements}

앱에서 표준 Livefyre 앱 구성 요소를 제거합니다.

CSS를 사용하여 페이지에서 기본 Livefyre 앱 요소를 숨겨 필요에 맞게 사용자 환경을 사용자 정의할 수 있습니다.

앱에서 요소를 숨기려면 표시를 없음으로 설정하기만 하면 됩니다.

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
