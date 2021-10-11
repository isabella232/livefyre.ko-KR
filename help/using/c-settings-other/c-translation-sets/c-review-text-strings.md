---
description: Livefyre 검토에 대한 텍스트 문자열 사용자 지정.
title: 텍스트 문자열 검토
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# 텍스트 문자열 검토{#review-text-strings}

Livefyre 검토에 대한 텍스트 문자열 사용자 지정.

이 페이지에서는 Review 앱에서 사용자 지정할 수 있는 문자열을 나열하고 설명합니다. 여기에 나열된 문자열은 String Customizations에 나열된 Livefyre 코어 앱의 기본 문자열에 대해 추가 및 무시합니다. 중복 항목이 나열되는 경우 이 표에 나열된 문자열이 검토 앱의 기본값입니다.

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

## 검토/등급 인터페이스 {#section_iyv_zj4_xz}

검토 및 등급 사용자 인터페이스에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|--- |--- |--- |
| 단추 | editReviewBtn | 검토 편집 |
|  | reviewBtn | 쓰기 검토 |
|  | reviewsClosed | 검토가 종료됨 |
|  | showReviewBtn | 검토 표시 |
|  | 팔로우 | 관심 있어요 |
|  | shareText | 방금 검토를 했어요. 확인해! |
| 등급 도구 설명 | ratingValues | 배열. 기본값 = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>참고: 배열에 있는 값을 복제하여 각 별의 왼쪽과 오른쪽 절반을 같은 이름으로 할당해야 합니다. |
| 등급 하위 부분 | ratingSubpartPlaceholder | 배열. 기본값 = `[]` |
|  | ratingSubpartTitles | 배열. 기본값 = `[]` |
|  | reviewStreamTitle | 기본적으로 비어 있습니다. 리뷰의 요약 섹션 제목입니다. |
| Misc | averageRating | 평균 사용자 등급 |
|  | breakdownHeader | 등급 분류 |
|  | 유용한 | %s/%s이(가) 유용한 것으로 발견되었습니다. |
|  | documentPlural | %s/%s이(가) 유용한 것으로 발견되었습니다. |
|  | outOf | / |
|  | ratingType | 별 |

## 스트림 정보 {#section_wmv_yj4_xz}

컨텐츠 스트림 정보 및 표시에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 정렬 | sortBy | 기본적으로 비어 있습니다. |
|  | sortHighestQued | 최고 등급 |
|  | sortLowed | 최저 등급 |
|  | sortMostDocument | 가장 유용한 |
| 스트림 오류입니다. | showMore | 자세히 표시 |
| 고속 스트림 | newComment | 새 검토 |
|  | newComments | 새 검토 |
| 리스너 카운트 | listenerCount | 사용자 의견 |
|  | listenerCountPlural | 듣는 사람 |
| 댓글 카운트 | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 주석 알림 카운트 | commentNotifier | 새 검토 |
|  | commentNotifierPlural | 새 검토 |

## 작성자/컨텐츠 정보 {#section_osx_xj4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 스레드 브레이크아웃 | reviewsContentNotFoundMsg | 이 검토는 더 이상 표시되지 않습니다 |
|  | backToComments | 리뷰로 돌아가기 |

## 사용자 작업 {#section_tlx_wj4_xz}

사용자 작업에 사용할 수 있는 문자열: 기존 컨텐츠 플래그 지정, 공유 및 표시가 도움이 됩니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 댓글 바닥글 | wasReviewDocument | 도움이 될까요? |
|  | wasReviewDocumentMobile | 도움이 될까요? |
|  | ownWasReviewDocument | 유용한 정보를 찾았습니다. |
|  | reviewWasDocument | 예 |
|  | documentDivider | amp;vert; |
|  | reviewWasNotDocument | 아니오 |
| 투표 모달 | voteTitle | 이 검토가 도움이 되었습니까? |
|  | voteDownvote | 아니오 |
|  | voteReplyTitle | 이 대답이 도움이 되었습니까? |
|  | voteTitle | 이 말이 도움이 되었습니까? |
|  | 투표수 | 예 |
| 플래그 모달 | flagTitle | %s 검토 플래그 지정 |
|  | flagSuccessMsg | 검토에 플래그가 지정되었습니다. |
| 모바일 플래그 지정 | flagConfirmationMessage | %s 검토 플래그를 %s(으)로 지정하시겠습니까? |
| 언급 모달 | mentionDefaultText | Livefyre 리뷰에서 널 언급했어! |
| 공유 모달 | shareTitle | 공유 검토 |

## 게시 함수 {#section_yl1_wj4_xz}

검토를 게시하는 사용자가 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 편집자 | bodyPlaceholder | 쓰기 검토... |
|  | postEditButton | 편집 |
|  | postEditCancelButton | 취소 |
|  | postAsButton | 게시 검토:.. |
|  | postButton | 게시물 검토 |
|  | postReplyAsButton | 게시 위치.. |
|  | postReplyButton | 게시물 |
|  | shareButton | 공유 |
|  | titlePlaceholder | Title… |

## 오류 {#section_jbc_vj4_xz}

일반 오류 메시지에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 오류 | errorAlreadyPosted | 리뷰를 하나만 게시할 수 있습니다. |
|  | errorAuthError | 이 대화에 대한 검토를 게시할 권한이 없습니다. |
|  | errorCommentsNotAllowed | 지금은 리뷰를 게시할 수 없습니다 |
|  | errorIncludeOwnComment | 자기 리뷰를 싫어할 수는 없다 |
|  | errorDuplicate | 리뷰를 좋아했다면 두 번 게시할 수 없습니다. |
|  | errorEditDuplicate | 검토할 때 검토 본문을 변경해야 합니다. |
|  | errorEditNotAllowed | 이 대화에 대한 검토는 편집할 수 없습니다. |
|  | errorEditTimeExceeded | 죄송합니다. 검토 편집 기간이 만료되었습니다. |
|  | errorEmpty | 빈 검토를 게시하려고 하는 것 같습니다. |
|  | errorEmptyTitle | 빈 제목을 게시하려고 하는 것 같습니다 |
|  | errorFieldRating | 별 등급 |
|  | errorFieldReview | 검토 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 죄송합니다. 검토가 너무 깁니다. 편집하고 다시 시도하십시오. |
|  | errorMissingFields | 을(를) 입력하십시오. |
|  | errorRatingEmpty | 빈 등급을 제출할 수 없습니다 |
|  | errorRatingNotSet | 모든 등급을 설정해야 합니다. |
|  | errorRatingNotValid | 등급은 객체여야 합니다. |
|  | errorShowMore | 추가 검토를 로드하는 동안 오류가 발생했습니다. |
|  | errorTitleMaxChars | 죄송합니다, 제목이 너무 깁니다. 편집하고 다시 시도하십시오. |
|  | errorVoteOwnComment | 자신의 검토에 투표할 수 없습니다 |
