---
description: 페이지에서 Livefyre 로고의 위치를 변경합니다.
seo-description: 페이지에서 Livefyre 로고의 위치를 변경합니다.
seo-title: Livefyre 로고 이동
solution: Experience Manager
title: Livefyre 로고 이동
uuid: 807304 AE -6070-4505-87 DB -169 A 925 F 714 C
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre 로고 이동{#move-the-livefyre-logo}

페이지에서 Livefyre 로고의 위치를 변경합니다.

Livefyre 와의 계약이 허용하는 경우 콘텐츠 스트림 상단에서 하단으로 Livefyre 로고를 이동할 수 있습니다.

예를 들어 Livefyre 앱이 포함된 요소 바로 다음에 다음 HTML를 추가합니다.

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

그런 다음 페이지의 Stylesheet에 다음을 추가합니다.

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

