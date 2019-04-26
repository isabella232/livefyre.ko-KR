---
description: 사용자 그룹에 대한 사용자 지정 스타일 컨텐츠에 대해 먼저 계정에 사용자 태그를 추가한 다음 CSS를 사용하여 컨텐츠에 스타일을
  지정해야 합니다.
seo-description: 사용자 그룹에 대한 사용자 지정 스타일 컨텐츠에 대해 먼저 계정에 사용자 태그를 추가한 다음 CSS를 사용하여 컨텐츠에
  스타일을 지정해야 합니다.
seo-title: 사용자 지정 스타일 적용
solution: Experience Manager
title: 사용자 지정 스타일 적용
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 사용자 지정 스타일 적용{#applying-custom-styles}

사용자 그룹에 대한 사용자 지정 스타일 컨텐츠에 대해 먼저 계정에 사용자 태그를 추가한 다음 CSS를 사용하여 컨텐츠에 스타일을 지정해야 합니다.

Studio 나 Ping를 통해 추가된 각 사용자 태그에 대해 Livefyre는 두 개의 CSS 클래스를 만듭니다. 두 개의 CSS 클래스가 모두 그룹 컨텐츠에 스타일을 지정하는 데 사용됩니다.

사용자 태그를 CSS 클래스로 변환할 때:

* Livefyre는 다음과 같은 두 가지 클래스를 만듭니다. fyre-author-tag-*** < your_ group >*** 및 fyre-tag-author-*** < your_ group >***. 둘 다 컨텐츠에 스타일을 지정하는 데 사용할 수 있습니다.

* 태그에 포함된 모든 공백은 밑줄로 변환됩니다. 예를 들면 다음과 같습니다. ' 즐겨찾는 사용자'는 favorite_ user가 됩니다.
* 그룹 이름에 포함된 유니코드 문자는 변환되지 않으며 클래스 이름에 유니코드로 표시됩니다. 예를 들면 다음과 같습니다. 사용자 그룹'modérateur'는 fyre-comment-author-tag-modérateur가 됩니다.

사용자 그룹이 만들어지면 Livefyre의 CSS 클래스를 사용하여 컨텐츠에 대한 사용자 정의 스타일을 적용합니다.

## 중재자 및 소유자를 위한 컨텐츠 스타일 지정 {#section_vjv_2cv_xz}

* CSS 클래스. fyre-Moderator를 사용합니다.

   >[!NOTE]
   >
   >소유자는 중재자이므로 이 클래스는 스트림에서도 해당 컨텐츠에 적용됩니다.

* CSS 규칙을 만들어 그룹에 대한 배지를 표시하거나 스타일을 지정합니다.

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 사용자 그룹에 대한 컨텐츠 스타일 지정 {#section_ghn_s1v_xz}

CSS 규칙을 만들어 그룹에 대한 배지를 표시하거나 스타일을 지정합니다.

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

CSS 클래스 fyre-author-tag-*** < your_ group >*** 또는 fyre-tag-author-*** < your_ group >*** 를 사용하여 선택한 태그와 연결된 계정에서 게시된 각 항목에 대한 글꼴과 배경을 스타일링합니다.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

