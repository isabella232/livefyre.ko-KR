---
description: Livefyre 사용자에게 표시되는 아이콘을 @mention 풀다운 메뉴에서 변경합니다.
seo-description: 언급 풀다운 메뉴에서 Livefyre 사용자에게 표시되는 아이콘을 변경합니다.
seo-title: 언급 아이콘 변경
solution: Experience Manager
title: Mention 아이콘 변경
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# 변경 `@mention` 아이콘 {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

풀다운 메뉴에 사용되는 Livefyre 아이콘을 사용자가 선택한 아이콘으로 변경하여 자신의 아이콘을 사용하여 커뮤니티 구성원을 표시할 수 있습니다. `@mention`

## 예

이 아이콘을 변경하려면 다음 CSS를 스타일시트에 추가합니다. &lt;*your resource*&gt; url을 선택한 이미지의 URL로 교체하여 기본 Livefyre 배지를 대체합니다.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
