---
description: Storify 앱에 사용할 수 있는 CSS 클래스입니다.
seo-description: Storify 앱에 사용할 수 있는 CSS 클래스입니다.
seo-title: Storify CSS classes
solution: Experience Manager
title: Storify CSS classes
uuid: 168 A 0 DB 0-A 209-417 A-BA 91-A 33 B 4 D 411 C 8 D
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Storify CSS classes{#storify-css-classes}

Storify 앱에 사용할 수 있는 CSS 클래스입니다.

CSS를 사용하여 자체 스타일 시트와 함께 기본 CSS를 무시하면 페이지와의 보다 완벽한 통합을 위해 Storify 앱을 사용자 정의할 수 있습니다. 이 섹션에서는 사용 가능한 CSS 사용자 지정에 대해 설명합니다.

## Author elements {#section_tdy_hsh_xz}

게시물의 작성자 아바타, 작성자 이름 및 타임스탬프에 대한 스타일링을 사용자 지정할 수 있습니다.

![](assets/StorifyAuthorCSS.png)

| class | 설명 |
|---|---|
| . s-author-name | author |
| . s-author-avatar | 작성자의 아바타. |
| . s-img | 작성자의 아바타 이미지입니다. |
| . s-timestamp | 컨텐츠가 게시된 날짜 타임스탬프입니다. |

## 헤더 요소 {#section_nbv_gsh_xz}

스토리 페이지에 대한 머리글 섹션을 사용자 지정할 수 있습니다.

![](assets/StorifyHeaderCSS-countdown-1.png)

| **class** | **설명** |
|---|---|
| . super-header | 기본 헤더 |
| . outer-header | 기본 헤더 행 1 |
| . s-countdown | 기본 헤더 행 1 카운트다운 타이머 |
| . s-liveness | 기본 헤더 행 1 «라이브» 상태 |
| . base-header | 기본 머리글 행 2 |
| . s-dropdown | 기본 헤더 행 2 정렬 드롭다운 트리거입니다. |
| . s-dropdown-menu | 기본 머리글 행 2 정렬 드롭다운 메뉴를 참조하십시오. |
| . s-dropdown-triangle | 기본 머리글 행 2 정렬 드롭다운 메뉴 삽입 기호. |
| . s-dropdown-option | 기본 머리글 행 2 정렬 드롭다운 메뉴 항목을 참조하십시오. |
| . s-views | 기본 헤더 행 2 보기 수입니다. |
| . s-share-button 단추 | 기본 머리글 행 2 공유 단추. |
| . s-share-menu | 기본 머리글 행 2 공유 메뉴를 참조하십시오. |

## 게시물 요소 {#section_lrs_fsh_xz}

게시물의 스토리 요소에 대한 스타일링을 사용자 지정할 수 있습니다.

![](assets/StorifyPostCSS.png)

| **class** | **설명** |
|---|---|
| . s-liveblog | 전체 스토리 요소에 대한 컨테이너 |
| . s-post | 게시물 컨테이너 |
| . s-modal-content | 게시물 모달 컨테이너 |
| . s-element-content | 게시물 내의 모든 컨텐츠 요소 |
| . s-element-text ul | 텍스트 요소 |
| . s-element-text h 2 | 텍스트 요소 제목 |
| . s-element-text p | 텍스트 요소 단락 |
| . s-element-text ul | 텍스트 요소 무순서 목록 |
| . s-element-text ol | 텍스트 요소 순서 목록 |
| . s-element-text li | 텍스트 요소 목록 항목 |
| . s-element-text blockquote | blockquote |
| . s-element-text blockquote: before | 작은 따옴표 시작 아이콘 |
| . s-element-text blockquote: after | 작은 따옴표 끝 아이콘 |
| . s-element-image | 인라인 이미지 요소 컨테이너 |
| . s-img | `<img>` element |
| . s-image-caption | 소셜 미디어에 있는 이미지 및 비디오에 대한 캡션 (예: Instagram 이미지) |
| . s-upload-image-caption | 스토리 편집기를 통해 업로드된 이미지 및 비디오에 대한 캡션 |
| . s-element-video | 비디오 요소 |
| . s-element-quote | 인용 요소 (예: 텍스트만 포함 트윗 |
| . s-element-quote-image | 이미지 요소 (예: 트윗 (이미지 포함) |
| . s-element-quote-video | 비디오 요소 (예: 비디오가 포함된 트윗 |
| . s-link-body | 견적 내에서 링크 미리 보기 (예: 링크 미리 보기 포함 트윗 |

## 바닥글 요소 {#section_ozc_zrh_xz}

각 개별 게시물에 대해 바닥글 섹션을 사용자 지정할 수 있습니다.

![](assets/storify_CSS_footer.png)

| **class** | **설명** |
|---|---|
| . s-post-footer | 게시물의 바닥글입니다. |
| . s-sidenotes a | 게시물의 바닥글에 있는 [Sidenotes] 단추. |
| . s-like | 게시물의 바닥글에 있는 "좋아요" 단추입니다. |
