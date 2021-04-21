---
description: Livefyre 검토에 대한 텍스트 문자열 사용자 지정
title: 텍스트 문자열 검토
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 5%

---

# 텍스트 문자열 검토{#review-text-strings}

Livefyre 검토에 대한 텍스트 문자열 사용자 지정

이 페이지에서는 리뷰 앱에서 사용자 정의에 사용할 수 있는 문자열을 나열하고 설명합니다. 여기에 나열된 문자열은 문자열 사용자 지정에 나열된 Livefyre 핵심 앱에 대한 기본 문자열에 추가하여 무시합니다. 중복이 나열되는 경우 이 표에 나열된 문자열이 검토 앱에 대한 기본값입니다.

구현
검토/등급 인터페이스
스트림 정보
작성자/컨텐츠 정보
사용자 작업
게시 함수
오류

## 구현 {#section-vsy-1k4-xz}

이 기능을 구현하려면 재정의할 문자열의 1-1 개체 매핑을 Javascript 구성 개체에 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

예:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 검토 / 등급 인터페이스 {#section_iyv_zj4_xz}

검토 및 등급 사용자 인터페이스에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|--- |--- |--- |
| 단추 | editReviewBtn | 검토 편집 |
|  | reviewBtn | [쓰기 검토](https://d.pr/i/QscA) |
|  | reviewsClosed | [검토 완료](https://d.pr/i/zr7M) |
|  | showReviewBtn | [검토 표시](https://d.pr/i/onxU) |
|  | follow | 관심 있어요 |
|  | shareText | 방금 검토를 한 거예요. 확인! |
| 등급 도구 설명 | ratingValues | 배열. 기본값 = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>참고:각 별의 왼쪽 및 오른쪽 절반 모두에 동일한 이름을 할당하려면 배열의 값을 복제해야 합니다. |
| 부분 등급 지정 | ratingSubpartPlaceholder | 배열. 기본값 = `[]` |
|  | ratingSubpartTitles | 배열. 기본값 = `[]` |
|  | reviewStreamTitle | 기본적으로 비어 있습니다. 검토 요약 섹션의 제목입니다. |
| Misc | averageRating | [평균 사용자 등급](https://d.pr/i/QscA) |
|  | 상세 분류 헤더 | [등급 분류](https://d.pr/i/QscA) |
|  | prop | %s/%s이(가) 유용함 |
|  | helpidPlural | %s/%s이(가) 유용함 |
|  | outOf | / |
|  | ratingType | 별 |

## 스트림 정보 {#section_wmv_yj4_xz}

콘텐츠 스트림 정보 및 표시에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 정렬 | sortBy | 기본적으로 비어 있습니다. |
|  | sortHighestRated | [최고 평점](https://d.pr/i/huTd) |
|  | sortLestRated | [최저 등급](https://d.pr/i/huTd) |
|  | sortMost유익함 | [가장 유용한 정보](https://d.pr/i/huTd) |
| 스트림 오류입니다. | showMore | 자세히 표시 |
| 높은 스트림 속도 | newComment | 새 검토 |
|  | newComments | 새로운 평가 |
| 리스너 수 | listenerCount | 의견 수렴 |
|  | listenerCountPlural | 사람들이 듣는 소리 |
| 주석 수 | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 주석 알림 기능 수 | commentNotifier | 새 검토 |
|  | commentNotifierPlural | 새로운 평가 |

## 작성자 / 콘텐트 정보 {#section_osx_xj4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있는 검색입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 스레드 소규모 회의 | reviewsContentNotFoundMsg | [이 검토는 더 이상 표시되지 않습니다.](https://d.pr/i/svXs) |
|  | backToComments | 리뷰로 돌아가기 |

## 사용자 작업 {#section_tlx_wj4_xz}

사용자 작업에 사용할 수 있는 문자열:기존 컨텐트에 대한 플래그 지정, 공유 및 표시가 도움이 됩니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 주석 바닥글 | wasReviewInprovided | [도움이 되십니까?](https://d.pr/i/Q0mA) |
|  | wasReviewIncluentMobile | 도움이 되십니까? |
|  | ownWasReviewInsive | [유용한 정보를 찾았습니다.](https://d.pr/i/Q0mA) |
|  | reviewWasInsistance | [예](https://d.pr/i/Q0mA) |
|  | helpidDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotIncorporated | [아니오 ](https://d.pr/i/Q0mA) |
| 투표 양식 | voteTitle | 이 검토가 도움이 되었습니까? |
|  | 투표다운투표 | 아니오 |
|  | voteReplyTitle | 이 답변이 도움이 되었습니까? |
|  | voteTitle | 이 말이 도움이 되었습니까? |
|  | voteUpvote | 예 |
| 플래그 양식 | flagTitle | %s 검토 플래그 지정 |
|  | flagSuccessMsg | 검토에 플래그가 지정되었습니다. |
| 모바일 플래그 지정 | flagConfirmationMessage | %s의 검토에 %s(으)로 플래그를 지정하시겠습니까? |
| 언급 양식 | menusDefaultText | Livefyre 검토에서 널 언급했어! |
| Share modal | shareTitle | 검토 공유 |

## 게시물 함수 {#section_yl1_wj4_xz}

사용자가 검토를 게시하는 데 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 편집자 | bodyPlaceholder | 검토 작성... |
|  | postEditButton | 편집 |
|  | postEditCancelButton | 취소 |
|  | postAsButton | 게시물 검토 형식.. |
|  | postButton | 게시물 검토 |
|  | postReplyAsButton | 다른 이름으로 게시.. |
|  | postReplyButton | 게시물 |
|  | shareButton | 공유 |
|  | titlePlaceholder | Title… |

## 오류 {#section_jbc_vj4_xz}

일반 오류 메시지에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 오류 | errorAlreadyPosted | 하나의 검토만 게시할 수 있습니다. |
|  | errorAuthError | 이 대화에 대한 검토를 게시할 권한이 없습니다. |
|  | errorCommentsNotAllowed | 현재 검토를 게시할 수 없습니다. |
|  | errorDislikeOwnComment | 자신의 리뷰를 싫어할 수는 없다 |
|  | errorDuplicate | 리뷰를 좋아한 만큼 두 번 게시할 수 없습니다. |
|  | errorEditDuplicate | 검토 내용을 편집할 때 검토 본문을 변경해야 합니다. |
|  | errorEditNotAllowed | 이 대화에서 검토를 편집할 수 없습니다. |
|  | errorEditTimeExceeded | 죄송합니다. 검토 편집 기간이 만료되었습니다. |
|  | errorEmpty | 빈 검토를 게시하려고 하는 것 같습니다. |
|  | errorEmptyTitle | 빈 제목을 게시하려는 것 같습니다 |
|  | errorFieldRating | 별 등급 |
|  | errorFieldReview | 검토 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 죄송합니다. 검토가 너무 깁니다. 편집하고 다시 시도하십시오. |
|  | errorMissingFields | 다음 항목을 입력하십시오. |
|  | errorRatingEmpty | 빈 등급을 제출할 수 없습니다. |
|  | errorRatingNotSet | 모든 등급을 설정해야 합니다. |
|  | errorRatingNotValid | 등급은 객체여야 합니다. |
|  | errorShowMore | 추가 검토를 로드하는 동안 오류가 발생했습니다. |
|  | errorTitleMaxChars | 죄송합니다. 제목이 너무 깁니다. 편집하고 다시 시도하십시오. |
|  | errorVotOwnComment | 자신의 검토에 투표할 수 없다 |
