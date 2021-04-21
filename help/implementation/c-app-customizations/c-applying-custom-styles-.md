---
description: 사용자 그룹의 사용자 정의 스타일 컨텐츠를 만들려면 먼저 계정에 사용자 태그를 추가한 다음 CSS를 사용하여 컨텐츠의 스타일을 지정해야 합니다.
title: 사용자 정의 스타일 적용
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 사용자 지정 스타일 적용{#applying-custom-styles}

사용자 그룹의 사용자 정의 스타일 컨텐츠를 만들려면 먼저 계정에 사용자 태그를 추가한 다음 CSS를 사용하여 컨텐츠의 스타일을 지정해야 합니다.

Studio 또는 Ping for Pull을 통해 추가된 각 사용자 태그에 대해 Livefyre는 2개의 CSS 클래스를 만듭니다. 이 두 클래스를 모두 그룹 내용의 스타일을 지정하는 데 사용할 수 있습니다.

사용자 태그를 CSS 클래스로 변환할 때:

* Livefyre는 다음 두 개의 클래스를 만듭니다.fyre-author-tag-***&lt;your_group>*** 및 fyre-tag-author-***&lt;your_group>***. 두 가지 모두 컨텐츠의 스타일을 지정하는 데 사용할 수 있습니다.

* 태그에 포함된 모든 공백은 밑줄로 변환됩니다. 예:&#39;즐겨찾기 사용자&#39;가 favorite_user가 됩니다.
* 그룹 이름에 포함된 유니코드 문자는 변환되지 않고 클래스 이름에 유니코드로 표시됩니다. 예:사용자 그룹 &#39;modereeur&#39;은 이제 주석을 다시 작성하는-author-tag-modereeur가 됩니다.

사용자 그룹이 만들어지면 Livefyre의 CSS 클래스를 사용하여 콘텐츠에 대한 사용자 정의 스타일링을 적용합니다.

## 중재자(및 소유자) {#section_vjv_2cv_xz}에 대한 컨텐츠 스타일 지정

* CSS 클래스 .fyre-adsored를 사용합니다.

   >[!NOTE]
   >
   >소유자는 중재자이므로 스트림의 해당 컨텐츠에도 이 클래스가 적용됩니다.

* CSS 규칙을 만들어 그룹의 배지를 표시하거나 스타일을 지정합니다.

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 사용자 그룹 {#section_ghn_s1v_xz}의 콘텐츠 스타일 지정

CSS 규칙을 만들어 그룹의 배지를 표시하거나 스타일을 지정합니다.

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

CSS 클래스 fyre-author-tag-***&lt;your_group>*** 또는 fyre-tag-author-***&lt;your_group>***을 사용하여 선택한 태그와 연결된 계정에서 게시한 각 항목의 글꼴과 배경을 스타일을 지정합니다.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
