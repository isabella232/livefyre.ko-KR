---
description: 언급 풀다운 메뉴에서 Livefyre 사용자에게 표시되는 아이콘을 변경합니다.
title: 언급 아이콘 변경
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# `@mention` 아이콘 {#change-mention-icon} 변경

`@mention` 풀다운 메뉴에서 Livefyre 사용자에 대해 표시되는 아이콘을 변경합니다.

`@mention` 풀다운 메뉴에 사용되는 Livefyre 아이콘을 선택한 아이콘으로 변경하여 자신만의 아이콘으로 커뮤니티 구성원을 표시할 수 있습니다.

## 예

이 아이콘을 변경하려면 스타일시트에 다음 CSS를 추가하십시오. &lt;*리소스* url을 기본 Livefyre 배지 대신 선택한 이미지의 URL로 바꿉니다.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
