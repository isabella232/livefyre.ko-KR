---
description: 번역 세트를 사용하면 앱의 대체 언어를 지정할 수 있습니다.
seo-description: 번역 세트를 사용하면 앱의 대체 언어를 지정할 수 있습니다.
seo-title: 번역 세트
solution: Experience Manager
title: 번역 세트
uuid: 8ba66a61-5520-482a-bc0b-e4f6b57f1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 7%

---


# 번역 세트 {#translation-sets}

번역 세트를 사용하면 앱의 대체 언어를 지정할 수 있습니다.

<!-- 
c_translation_sets.dita
-->

번역 설정을 사용하여 앱을 다양한 언어로 현지화하거나 Studio의 한 위치에서 여러 앱에 대한 대체 텍스트를 지정하십시오. 예를 들어 모든 스페인어 사이트에서 모든 앱 필드에 스페인어 언어를 사용하도록 할 수 있습니다. 또한 모든 필드가 사이트 또는 네트워크의 음성과 느낌에 일치하도록 텍스트를 수정할 수도 있습니다.

Storify 2를 제외한 모든 앱에 대한 번역 설정을 지정할 수 있습니다. 현지화할 수 있는 필드에 대한 자세한 내용은 [문자열 현지화](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)를 참조하십시오.

주석, 라이브 블로그 및 채팅은 번역 집합 내에서 동일한 문자열 집합을 공유합니다.

네트워크, 사이트, 앱 또는 API 사용에 대한 번역 세트를 지정합니다.

서로 다른 수준의 평행 이동 세트는 다음 패턴에 우선합니다.

* API 번역 세트는 모든 수준의 번역 세트(앱, 네트워크 및 사이트)를 무시합니다.
* 앱 번역 세트는 네트워크 수준 및 사이트 수준 번역 세트를 무시합니다.
* 사이트 수준 번역 세트는 네트워크 수준 번역 세트를 덮어씁니다.

## 텍스트 문자열 검토 {#c-review-text-strings}

Livefyre 검토에 대한 텍스트 문자열 사용자 지정

이 페이지에서는 리뷰 앱에서 사용자 정의에 사용할 수 있는 문자열을 나열하고 설명합니다. 여기에 나열된 문자열은 문자열 사용자 지정에 나열된 Livefyre 핵심 앱에 대한 기본 문자열에 추가하여 무시합니다. 중복이 나열되는 경우 이 표에 나열된 문자열이 검토 앱에 대한 기본값입니다.

* 구현
* 검토/등급 인터페이스
* 스트림 정보
* 작성자/컨텐츠 정보
* 사용자 작업
* 게시 함수
* 오류

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 단추 |  |  |
|  | editReviewBtn | 검토 편집 |
|  | reviewBtn | 쓰기 검토 |
|  | reviewsClosed | 검토 완료 |
|  | showReviewBtn | 검토 표시 |
|  | follow | 관심 있어요 |
|  | shareText | 방금 검토를 한 거예요. 확인! |
| 등급 도구 설명 |  |  |
|  | ratingValues | 배열. 기본값 = [&#39;Poor&#39;, &#39;Poor&#39;, &#39;Fair&#39;, &#39;Average&#39;, &#39;Average&#39;, &#39;Good&#39;, &#39;Good&#39;, &#39;Good&#39;, &#39;Excellent&#39;, &#39;Sureful&#39;]; |
|  |  | 참고: 각 별의 왼쪽 및 오른쪽 절반을 같은 이름으로 할당하려면 배열의 값을 복제해야 합니다. |
| 부분 등급 지정 |  |  |
|  | ratingSubpartPlaceholder | 배열. 기본값 = [] |
|  | ratingSubpartTitles | 배열. 기본값 = [] |
|  | reviewStreamTitle | 기본적으로 비어 있습니다. 검토 요약 섹션의 제목입니다. |
| Misc |  |  |
|  | averageRating | 평균 사용자 등급 |
|  | 상세 분류 헤더 | 등급 분류 |
|  | prop | %s/%s이(가) 유용함 |
|  | helpidPlural | %s/%s이(가) 유용함 |
|  | outOf | / |
|  | ratingType | 별 |

## 스트림 정보 {#section_wmv_yj4_xz}

콘텐츠 스트림 정보 및 표시에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *정렬* |  |  |
|  | sortBy | *기본적으로 비어 있습니다.* |
|  | sortHighestRated | [최고 평점](https://d.pr/i/huTd) |
|  | sortLestRated | [최저 등급](https://d.pr/i/huTd) |
|  | sortMost유익함 | [가장 유용한 정보](https://d.pr/i/huTd) |
| *스트림 오류입니다.* |  |  |
|  | showMore | 자세히 표시 |
| *높은 스트림 속도* |  |  |
|  | newComment | 새 검토 |
|  | newComments | 새로운 평가 |
| *리스너 수* |  |  |
|  | listenerCount | 의견 수렴 |
|  | listenerCountPlural | 사람들이 듣는 소리 |
| *주석 수* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *주석 알림 기능 수* |  |  |
|  | commentNotifier | 새 검토 |
|  | commentNotifierPlural | 새로운 평가 |

## 작성자 / 콘텐트 정보 {#section_osx_xj4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있는 검색입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *스레드 소규모 회의* |  |  |
|  | reviewsContentNotFoundMsg | [이 검토는 더 이상 표시되지 않습니다.](https://d.pr/i/svXs) |
|  | backToComments | 리뷰로 돌아가기 |

## 사용자 작업 {#section_tlx_wj4_xz}

사용자 작업에 사용할 수 있는 문자열:기존 컨텐트에 대한 플래그 지정, 공유 및 표시가 도움이 됩니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *주석 바닥글* |  |  |
|  | wasReviewInprovided | [도움이 되십니까?](https://d.pr/i/Q0mA) |
|  | wasReviewIncluentMobile | 도움이 되십니까? |
|  | ownWasReviewInsive | [유용한 정보를 찾았습니다.](https://d.pr/i/Q0mA) |
|  | reviewWasInsistance | [예](https://d.pr/i/Q0mA) |
|  | helpidDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotIncorporated | [아니오 ](https://d.pr/i/Q0mA) |
| *투표 양식* |  |  |
|  | voteTitle | 이 검토가 도움이 되었습니까? |
|  | 투표다운투표 | 아니오 |
|  | voteReplyTitle | 이 답변이 도움이 되었습니까? |
|  | voteTitle | 이 말이 도움이 되었습니까? |
|  | voteUpvote | 예 |
| *플래그 양식* |  |  |
|  | flagTitle | %s 검토 플래그 지정 |
|  | flagSuccessMsg | 검토에 플래그가 지정되었습니다. |
| *모바일 플래그 지정* |  |  |
|  | flagConfirmationMessage | %s의 검토에 %s(으)로 플래그를 지정하시겠습니까? |
| *언급 양식* |  |  |
|  | menusDefaultText | Livefyre 검토에서 널 언급했어! |
| *Share modal* |  |  |
|  | shareTitle | 검토 공유 |

## 게시물 함수 {#section_yl1_wj4_xz}

사용자가 검토를 게시하는 데 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *편집자* |  |  |
|  | bodyPlaceholder | 검토 작성... |
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
| 오류 |  |  |
|  | errorAlreadyPosted | 하나의 검토만 게시할 수 있습니다. |
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

## 사이드노트 텍스트 문자열 {#c_sidenotes_text_strings}

Livefyre 사이드노트에 대한 텍스트 문자열 사용자 정의

<!-- 

c_sidenotes_text_strings.dita

 -->

이 페이지에서는 Sidecotes 앱의 사용자 지정에 사용할 수 있는 모든 문자열을 나열하고 설명합니다. 핵심 Livefyre 앱에 사용할 수 있는 문자열에 대한 자세한 내용은 문자열 사용자 지정을 참조하십시오.

* 구현
* 인증
* 스트림 정보
* 작성자/컨텐츠 정보
* 사용자 작업
* 게시 함수
* 중재자 인터페이스
* 오류

## 구현 {#section_wp2_ql4_xz}

이 기능을 구현하려면 재정의할 문자열의 1-1 개체 매핑을 Javascript 구성 개체에 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

예:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 인증 {#section_pqf_3l4_xz}

인증 프로세스 및 인증된 사용자 메뉴에서 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *인증 메뉴 문자열* |  |  |
|  | menuAuthSignInBtn | 로그인 |
|  | menuAuthSignedInMsg | {action}에 로그인해야 합니다. |
|  | menuUserEditProfile | 프로필 편집 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 로그아웃 |
|  | menuUserBackBtn | 모든 |

## 스트림 정보 {#section_wpy_gl4_xz}

콘텐츠 스트림 정보 및 표시에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *정보 메뉴 옵션* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | 도움말 |
|  | menuInfoLivefyreLink | Livefyre.com으로 이동 |

## 작성자 / 콘텐트 정보 {#section_dhb_gl4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있는 검색입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
|  | commentConsorizerTag | Mod |
|  | commentPendingTag | 대기 중 |
|  | commentReadMoreLink | 자세히 보기 |
|  | commentReplyLink | 답글 {number}개 보기 |
|  | commentReplyLinkSing | 회신 참조 |
|  | commentVoteCount | 투표 |
|  | commentVoteCountSing | 개의 투표 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *배열. 기본값 = *[ &#39;1월&#39;, &#39;2월&#39;, &#39;3월&#39;, &#39;4월&#39;, &#39;5월&#39;, &#39;7월&#39;, &#39;8월&#39;, &#39;9월&#39;, &#39;10월&#39;, &#39;11월&#39;, &#39;12월&#39; ] |
|  | questionExpliction | 이제 문장, 단락, 이미지 및 인용문에 직접 주석을 읽고 쓸 수 있습니다. <br>텍스트를 강조 표시하고 아이콘을 클릭하거나 각 단락의 끝에 있는 아이콘을 클릭합니다. |
|  | questionMockText | &quot;친숙한&quot; 것은 &quot;친숙하다&quot; 라는 이유로 잘 알려져 있지 않다. |
|  | questionTitle | 사이드노트란? |

## 사용자 작업 {#section_qxd_fl4_xz}

사용자 작업에 사용할 수 있는 문자열:플래그 지정, 공유 및 기존 컨텐츠 좋아요 지정

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *응답 메뉴 옵션* |  |  |
|  | menuRepliesViewTitle | 세부 사항 |
|  | menuRepliesViewReply | 대화에 회신 |
| *공유 메뉴 옵션* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 공유 |
| *플래그 메뉴 옵션* |  |  |
|  | menuFlagOptionUnagree | 반대 |
|  | menuFlagOptionOffensive | 공격 |
|  | menuFlagOptionOffTopic | 주제 해제 |
|  | menuFlagOptionSpam | 스팸 |
|  | menuFlagTitle | 플래그... |
|  | facebookShareCaption | &quot;{title}&quot;의 사이드노트 |
| *모바일 사용자 옵션* |  |  |
|  | sliderCommentTally | / |
|  | sliderInviteRead | 읽음 |
|  | sliderInviteWrite | 쓰기 |
|  | sliderLoading | 로드 중… |
|  | sliderWriteText | 어떻게 생각해? 을 눌러 작성합니다. |

## 게시물 함수 {#section_xzf_2l4_xz}

컨텐츠를 게시하는 사용자에게 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
|  | editorEditBtn | 저장 |
|  | editorEditPosting | 저장 중... |
|  | editorEditReplyTitle | 회신 편집 |
|  | editorEditTitle | 사이드노트 편집 |
|  | editorPlaceholder | 어떻게 생각해? |
|  | editorPostBtn | 게시물 사이드노트 |
|  | editorPostBtnMobile | 게시물 |
|  | editorPublishing | 게시 중… |
|  | editorReplyBtn | 회신 게시 |
|  | editorReplyTitle | 회신 쓰기 |
|  | editorTitle | 사이드노트 쓰기 |
|  | emptyImageBlockTxt | 어떻게 생각해? |
|  | emptyTextBlockTxt | + |
|  | replyBtn | 답글 |
|  | threadReplyBtn | 대화에 회신 |
| *삭제 메뉴 옵션* |  |  |
|  | menuConfirmAccept | 예, {action} |
|  | menuConfirmCancel | 취소 |
|  | menuConfirmTitle | 계속하시겠습니까? |
| *기타 메뉴 옵션* |  |  |
|  | menuEtcOptionApprove | 승인 |
|  | menuEtcOptionDelete | 삭제 |
|  | menuEtcOptionEdit | 편집 |
|  | menuEtcOptionFlag | 플래그 |
|  | menuEtcOptionShare | 공유 |
|  | menuEtcPostedAt | {date}에 게시 |
|  | menuEtcTitle | 자세히 |

## 중재자 인터페이스 {#section_o5f_dl4_xz}

사용자 인증 중재자 인터페이스에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| *자세히 메뉴의 확인 메시지* |  |  |
|  | notificationApproved | 승인됨 |
|  | notificationDeleted | 삭제됨 |
|  | notification플래그 지정됨 | 플래그 지정됨 |

## 오류 {#section_gtk_cl4_xz}

일반 오류 메시지에 사용할 수 있는 문자열입니다.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
|  | errorConnection | 아.. 당신은 사이가 좋지 않은 것 같아요. |
|  | errorDuplicate | 당신의 메모도 마음에 드는데, 두 번 게시할 수는 없습니다. |
|  | errorGeneral | 오류가 발생했습니다. 다시 시도하십시오. |
|  | errorServer | 서버에 문제가 발생했습니다. 다시 한번 해 보시겠습니까? |
