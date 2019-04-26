---
description: 사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의할 수 있습니다.
seo-description: 사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의할 수 있습니다.
seo-title: CSS 클래스
solution: Experience Manager
title: CSS 클래스
uuid: 8714 E 7 E 5-3858-458 F-A 464-DE 87 FD 2 F 0 FF 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS 클래스{#css-classes}

사용 가능한 CSS 클래스를 사용하여 앱의 디스플레이를 사용자 정의할 수 있습니다.

채팅, 댓글, 라이브 블로그, 검토 및 Sidenotes에 제공됩니다.

CSS를 사용하면 고유한 스타일 시트와 함께 기본 앱 CSS를 무시하면 Livefyre 앱을 사용자 정의하여 페이지와의 보다 완벽한 통합을 수행할 수 있습니다. 이 섹션에서는 사용 가능한 CSS 사용자 지정에 대해 설명합니다.

* [편집기 CSS](#c_css_classes/section_edx_prh_xz)
* [정렬 옵션 CSS](#c_css_classes/section_btq_4rh_xz)
* [주석 CSS](#c_css_classes/section_mlv_nrh_xz)
* [주요 주석 CSS](#c_css_classes/section_m2v_mrh_xz)
* [보관된 주석 CSS](#c_css_classes/section_bs5_lrh_xz)
* [주석 알림 기능 CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 편집기 CSS {#section_edx_prh_xz}

이러한 클래스를 사용하여 게시물 편집기 인터페이스를 변경합니다.

| class | 설명 |
|---|---|
| . fyre-comment-count | 댓글 수를 표시하는 텍스트입니다. |
| . Fyre-login-bar | 로그인 막대와 옵션이 포함된 테두리 상자 |
| . fyre-live-container | 의견 수렴 및 아바타 수에 대한 경계 상자 |
| . Fyre-Editor | . fyre-login-bar 주위의 테두리 상자. fyre-live-container 및 사용자가 주석을 쓰는 텍스트 영역. |
| . Fyre-stream-sort | 정렬 옵션 주위의 테두리 상자 |

편집기 필드 배경색, 편집기 내에 표시되는 글꼴 색상, 크기 및 텍스트를 비롯하여 앱 구성 자체에서 스타일을 편집할 수도 있습니다.

주석 편집기를 사용자 정의하려면 Editorcss를 추가합니다. {} object to fyre. conv. load () and include your desired styles. 예를 들어 사용자 지정 CSS로 편집기를 업데이트하려면 다음을 수행합니다.

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

| class | 설명 |
|---|---|
| . Fyre-stream-sort | 전체 정렬 옵션 div. |
| . fyre-stream-sort-latest | «최신» 옵션. |
| . fyre-stream-sort-dest | «가장 오래된» 옵션. |
| . fyre-stream-sort-bar | 옵션 사이에 있는 구분 모음입니다. |
| . fyre-stream-sort-selected | 현재 선택된 정렬 옵션. |

HTML 구조:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

숨기기|' 정렬 옵션 구분.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## 주석 CSS {#section_mlv_nrh_xz}

| class | 설명 |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre는 Livefyre의 Studio, Profile Sync를 통해 추가된 각 사용자 태그에 대해 이 포맷의 CSS 클래스를 [만듭니다](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). 이 클래스는 해당 태그를 포함하여 사용자 계정에서 게시한 모든 컨텐츠에 대해 배경을 스타일링하는 데 사용할 수 있습니다. |
| . fyre-tag-content-icon- *`tag name`* | Livefyre는 Livefyre [Studio를 통해 추가된 각 컨텐츠 태그에 대해 이 포맷의 CSS 클래스를 만듭니다](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). 이 클래스를 사용하여 태그를 추가한 모든 컨텐츠를 스타일을 지정할 수 있습니다. |
| . fyre-comment-user | 사용자 프로필 사진이 포함된 테두리 상자. |
| . fyre-comment-username | 사용자 이름입니다. |
| . Fyre-Moderator | 중재자 테두리 상자. |
| . Fyre-comment | 주석 텍스트/링크 주위의 테두리 상자 |
| . fyre-comment-article | 전체 주석 컨텐츠의 테두리 상자. |
| . fyre-comment-date | " 게시된 이후 시간 "요소에 첨부된 태그입니다. |
| . fyre-comment-media | 미디어 컨텐츠 주위의 테두리 상자 |
| . Fyre-comment-actions | 댓글을 남길 수 있는 동작 주위의 테두리 상자 |
| . fyre-comment-like | «좋아요» 링크를 둘러싼 테두리 상자 |
| . fyre-comment-reply | «답글» 링크를 둘러싼 테두리 상자. |

## 주요 주석 CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>모든 주석 CSS 클래스를 주요 컨텐츠에 적용할 수도 있습니다.

| class | 설명 |
|---|---|
| . fyre-functional-content-wrapper | 독자의 컨테이너 div. |
| . fyre-functional-header | 선도적인 제목 표시줄. |
| . fyre-functional-header-icon | 헤더의 Quill 아이콘. |
| . Fyre-functional-title | 머리글 텍스트입니다. |
| . Fyre-functional-body | 독자의 주요 콘텐츠에 대한 컨테이너 div. |
| . Fyre-주요 따옴표 | 각 컨텐츠 항목을 시작하는 견적 아이콘. |

## 보관된 주석 CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>모든 컨텐츠 CSS 클래스를 보관된 컨텐츠에 적용할 수도 있습니다.

| class | 설명 |
|---|---|
| . fyre-archive-stream-title | " 보관 "텍스트입니다. |
| . fyre-archive-stream-title-icon | " 보관 "헤더의 로고. |

## 주석 알림 기능 CSS {#section_dy4_krh_xz}

이러한 클래스를 사용하면 Livefyre 주석 알림 기능을 사용자 정의할 수 있습니다.

| class | 설명 |
|---|---|
| . Fyre-notification | 목록 항목의 div (새 컨텐츠 및 아카이브 컨텐츠 모두). |
| . Fyre-notifier | 알림 표시자의 내용 래퍼입니다. |
| . Fyre-notifier-archive | 가장 최근 게시물 이외의 모든 새 컨텐츠에 대한 래퍼입니다. |
| . fyre-notifier-avatar | 아바타에 대한 이미지입니다. |
| . fyre-notifier-avatar-container | 사용자 아바타에 대한 컨테이너 div. 배치를 정의할 수 있습니다. |
| . Fyre-notifier-shading-shading | Avatar Div의 음영입니다. |
| . fyre-notifier-banner | 사용자 아바타와 가장 최근에 게시된 항목에 대한 컨텐츠 조각을 표시하는 알림 기능의 미리 보기 컨텐츠 컨테이너. |
| . Fyre-notifier-base | 알림 기능의 정보 부분에 대한 컨테이너입니다. 이 정보는 새 주석 수, 알림 캡션 및 닫기 단추 수를 나열합니다. |
| . fyre-notifier-base-close | 알림 표시자의 닫기 단추 (x) 에 대한 컨테이너 div. |
| . fyre-notifier-base-shadow | 알림 기능의 음영을 참조하십시오. |
| . Fyre-notifier-caption | 알림 표시자에 대해 표시되는 텍스트입니다. ' 새 댓글'이 기본적으로 표시됩니다. |
| . Fyre-notifier-close | 알림 기능을 닫는 단추입니다. |
| . Fyre-notifier-container | 알림 표시자의 컨테이너에는 배너와 기반이 모두 포함됩니다. |
| . Fyre-notifier-counter | 알림 표시기에 나열된 숫자의 컨테이너. |
| . Fyre-notifier-list | 가장 최근 컨텐츠 컨테이너 |
| . fyre-notifier-message | 표시된 컨텐츠의 처음 ~ 30 자 |
| . fyre-notifier-message-container | 헤더 메시지의 컨테이너 div. |
