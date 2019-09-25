---
description: 사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의합니다.
seo-description: 사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의합니다.
seo-title: CSS 클래스
solution: Experience Manager
title: CSS 클래스
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS 클래스{#css-classes}

사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의합니다.

채팅, 댓글, 라이브 블로그, 검토 및 사이드노트에 사용할 수 있습니다.

CSS를 사용하여 Livefyre 앱을 사용자 정의하여 기본 App CSS를 사용자 정의 가능한 Stylesheet로 간단하게 재정의하여 페이지와의 보다 완벽한 통합을 실현할 수 있습니다. 이 섹션에서는 사용 가능한 CSS 사용자 지정에 대해 설명합니다.

* [편집기 CSS](#c_css_classes/section_edx_prh_xz)
* [정렬 옵션 CSS](#c_css_classes/section_btq_4rh_xz)
* [CSS 주석 달기](#c_css_classes/section_mlv_nrh_xz)
* [주요 주석 CSS](#c_css_classes/section_m2v_mrh_xz)
* [보관된 주석 CSS](#c_css_classes/section_bs5_lrh_xz)
* [주석 알림 기능 CSS](#c_css_classes/section_dy4_krh_xz)
* [CSS 클래스 저장](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 편집기 CSS {#section_edx_prh_xz}

이러한 클래스를 사용하여 포스트 편집기 인터페이스를 변경합니다.

| 클래스 | 설명 |
|---|---|
| .fyre-comment-count | 댓글 수를 표시하는 텍스트입니다. |
| .fyre-login-bar | 로그인 막대와 옵션이 포함된 테두리 상자. |
| .fyre-live container | 듣던 사람과 아바타의 수를 둘러싸는 테두리 상자. |
| .fyre-editor | .fyre-login-bar, .fyre-live 컨테이너 및 사용자가 주석을 작성하는 텍스트 영역 주위의 테두리 상자. |
| .fyre-stream-sort | 정렬 옵션 주위의 테두리 상자. |

편집기 필드 배경색, 편집기 내에 표시되는 텍스트의 글꼴 색상, 크기 및 패밀리를 포함하여 앱 구성 자체에서 스타일을 편집할 수도 있습니다.

주석 편집기를 사용자 정의하려면 editorCss:{} 개체를 fyre.conv.load()에 추가하고 원하는 스타일을 포함합니다. 예를 들어, 사용자 지정 CSS로 편집기를 업데이트하려면:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## 정렬 옵션 CSS {#section_btq_4rh_xz}

| 클래스 | 설명 |
|---|---|
| .fyre-stream-sort | 전체 정렬 옵션 div. |
| .fyre-stream-sort-latest | "최신" 옵션 |
| .fyre-stream-sort-olest | "오래된 항목" 옵션 |
| .fyre-stream-sort-bar | 옵션 사이의 구분 기호 막대입니다. |
| .fyre-stream-sort-selected | 현재 선택된 정렬 옵션입니다. |

HTML 구조:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

정렬 옵션을 구분하는 '|'을 숨깁니다.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS 주석 달기 {#section_mlv_nrh_xz}

| 클래스 | 설명 |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre는 Livefyre의 Studio, Profile Sync를 통해 추가된 각 사용자 태그에 대해 이 형식으로 CSS 클래스를 [만듭니다](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). 이 클래스는 해당 태그를 포함하여 사용자 계정에서 게시한 모든 컨텐츠의 배경을 스타일을 지정하는 데 사용할 수 있습니다. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre는 Livefyre Studio를 통해 추가된 각 컨텐츠 태그에 대해 이 형식으로 CSS 클래스를 [만듭니다](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). 이 클래스는 태그를 추가한 모든 콘텐츠의 스타일을 지정하는 데 사용할 수 있습니다. |
| .fyre-comment-user | 사용자 프로필 사진이 포함된 테두리 상자. |
| .fyre-comment-username | 사용자 이름입니다. |
| .fyre-adjustiher | 중재자 테두리 상자. |
| .fyre 주석 | 댓글 텍스트/링크 주위에 테두리 상자가 표시됩니다. |
| .fyre-comment-article | 전체 주석 컨텐츠의 테두리 상자. |
| .fyre-comment-date | "게시 후 시간" 요소에 첨부된 태그입니다. |
| .fyre-comment-media | 미디어 컨텐츠 주위의 테두리 상자. |
| .fyre-comment-actions | 주석에 대해 수행할 수 있는 작업 주위의 테두리 상자. |
| .fyre-comment like | "좋아요" 링크 주위의 테두리 상자. |
| .fyre-comment-reply | "응답" 링크 주위의 테두리 상자. |

## 주요 주석 CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>모든 주석 CSS 클래스는 주요 컨텐츠에도 적용될 수 있습니다.

| 클래스 | 설명 |
|---|---|
| .fyre-features-content-wrapper | 독자의 컨테이너 div. |
| .fyre-features-header | 제목 표시줄입니다. |
| .fyre-featured-header-icon | 헤더의 쿼리 아이콘 |
| .fyre-features-title | 머리글 텍스트입니다. |
| .fyre추천 본문 | 독자의 주요 컨텐트에 대한 컨테이너 div. |
| .fyre-features-quote | 각 컨텐츠 항목을 시작하는 견적 아이콘 |

## 보관된 주석 CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>모든 컨텐츠 CSS 클래스는 보관된 컨텐츠에도 적용될 수 있습니다.

| 클래스 | 설명 |
|---|---|
| .fyre-archive-stream-title | "보관함" 텍스트. |
| .fyre-archive-stream-title-icon | "보관 위치에서" 헤더의 로고. |

## 주석 알림 기능 CSS {#section_dy4_krh_xz}

이러한 클래스를 사용하면 Livefyre 주석 알림 기능을 사용자 지정할 수 있습니다.

| 클래스 | 설명 |
|---|---|
| .fyre 알림 | 목록 항목의 div(새 컨텐츠와 아카이브 컨텐츠 모두)입니다. |
| .fyre 알림 기능 | Notifier의 내용을 나타내는 래퍼입니다. |
| .fyre-notifier-archive | 최신 게시물을 제외한 모든 새 컨텐츠의 래퍼입니다. |
| .fyre-notifier-avatar | 아바타의 이미지입니다. |
| .fyre-notifier-avatar-container | 사용자 아바타의 컨테이너 div. 위치를 정의할 수 있습니다. |
| .fyre-notifier-avatar-shading | avatar div의 음영입니다. |
| .fyre-notifier-banner | 사용자 아바타와 가장 최근에 게시한 항목에 대한 컨텐츠 조각을 표시하는 알림 표시자의 미리 보기 컨텐츠의 컨테이너입니다. |
| .fyre-notifier-base | 알림 표시자의 정보 부분에 대한 컨테이너로, 새 주석 수, 알림 표시자 캡션 및 닫기 단추를 나열합니다. |
| .fyre-notifier-base-close | 알림 표시자에 대한 닫기 단추(x)에 대한 컨테이너 div. |
| .fyre-notifier-base-shadow | 알림 표시자 베이스의 음영입니다. |
| .fyre-notifier-caption | 알림 표시자에 대해 표시되는 텍스트입니다. 기본적으로 '새 주석'입니다. |
| .fyre-notifier-close | 알림 표시자를 닫는 단추입니다. |
| .fyre-notifier-container | 알림 표시자의 컨테이너에는 배너와 베이스가 모두 포함됩니다. |
| .fyre-notifier-counter | 알림 표시자에 나열된 번호의 컨테이너입니다. |
| .fyre-notifier-list | 최신 컨텐츠 조각에 대한 컨테이너입니다. |
| .fyre-notifier-message | 컨텐츠의 처음~30자가 표시되었습니다. |
| .fyre-notifier-message-container | 헤더 메시지의 컨테이너 div. |
