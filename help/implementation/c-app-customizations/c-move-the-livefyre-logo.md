---
description: 페이지에서 Livefyre 로고의 위치를 변경합니다.
title: Livefyre 로고 이동
exl-id: dc6c26cf-e0b9-4af3-8a3c-e58ea4ecbc44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Livefyre 로고 이동{#move-the-livefyre-logo}

페이지에서 Livefyre 로고의 위치를 변경합니다.

Livefyre와의 계약에 따라 허용되는 경우 Livefyre 로고를 콘텐츠 스트림 맨 위에서 맨 아래로 이동할 수 있습니다.

예를 들어 Livefyre 앱이 포함된 요소 바로 다음에 있는 다음 HTML을 페이지에 추가합니다.

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

그런 다음 페이지의 스타일시트에 다음을 추가합니다.

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
