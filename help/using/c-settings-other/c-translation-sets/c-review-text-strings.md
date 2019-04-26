---
description: Livefyre 검토를 위한 텍스트 문자열 사용자 지정을 참조하십시오.
seo-description: Livefyre 검토를 위한 텍스트 문자열 사용자 지정을 참조하십시오.
seo-title: 텍스트 문자열 검토
solution: Experience Manager
title: 텍스트 문자열 검토
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 텍스트 문자열 검토{#review-text-strings}

Livefyre 검토를 위한 텍스트 문자열 사용자 지정을 참조하십시오.

이 페이지에서는 검토 앱에서 사용자 지정에 사용할 수 있는 문자열을 나열하고 설명합니다. 문자열 사용자 정의에 나열된 Livefyre 핵심 앱의 기본 문자열에 대한 추가 및 재정의 문자열이 여기에 나와 있습니다. 중복 항목이 나열되는 경우, 이 표에 나열된 문자열은 검토 앱의 기본값입니다.

구현
검토/평점 인터페이스
스트림 정보
작성자/컨텐츠 정보
사용자 작업
게시물 함수
오류

## 구현 {#section-vsy-1k4-xz}

이 기능을 구현하려면 Javascript 구성 개체로 재정의할 문자열의 1-1 개체 매핑을 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

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

## 리뷰/평점 인터페이스 {#section_iyv_zj4_xz}

검토 및 등급 사용자 인터페이스에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|--- |--- |--- |
| 단추 | Editreviewbtn | 편집 검토 |
|  | Reviewbtn | [Write Review](https://d.pr/i/QscA) |
|  | Reviewsclosed | [닫은 평가](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [검토 표시](https://d.pr/i/onxU) |
|  | 팔로우 | 관심이 있습니다 |
|  | sharetext | 방금 검토를 마쳤습니다. 확인해 보십시오! |
| 등급 툴팁 | Ratingvalues | 배열. 기본값 = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>참고: 배열의 값을 복제하여 각 별의 왼쪽 및 오른쪽 절반을 같은 이름으로 지정해야 합니다. |
| 하위 파트 등급 지정 | Ratingsubpartplaceholder | 배열. 기본값 = `[]` |
|  | Ratingsubparttitles | 배열. 기본값 = `[]` |
|  | Reviewstreamtitle | 기본적으로 비어 있습니다. 검토 요약 섹션의 제목입니다. |
| Misc | Averagerating | [평균 사용자 등급](https://d.pr/i/QscA) |
|  | Breakdownheader | [등급 분류](https://d.pr/i/QscA) |
|  | 유용성 | % s of % s found useful |
|  | 도움말 | % s of % s found useful |
|  | outof | / |
|  | Ratingtype | 별 |

## 스트림 정보 {#section_wmv_yj4_xz}

컨텐츠 스트림 정보에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| 정렬 | Sortby | 기본적으로 비어 있습니다. |
|  | sorthighestrated | [최고 등급](https://d.pr/i/huTd) |
|  | Sortlowestrated | [가장 낮은 등급](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [가장 유용한 정보](https://d.pr/i/huTd) |
| 스트림 Misc. | Showmore | 더 보기 |
| 고속 스트림 스트리밍 | Newcomment | 새로운 검토 |
|  | Newcomments | 새로운 검토 |
| 리스너 카운트 | Listenercount | 청중 의견 수렴 |
|  | Listenercountmulti | 의견 수렴 |
| 주석 수 | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelmultiple | Livereviews<strong> | </strong>% s |
| 주석 알림 횟수 | Comment알림 기능 | 새로운 검토 |
|  | Commentnotifierplural | 새로운 검토 |

## 작성자/컨텐츠 정보 {#section_osx_xj4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있습니다.

| element | key | 기본 텍스트 |
|---|---|---|
| 스레드 소규모 회의 | Reviewscontentnotfoundmessaging | [이 검토는 더 이상 표시되지 않습니다.](https://d.pr/i/svXs) |
|  | Backtocomments | 검토로 돌아가기 |

## 사용자 작업 {#section_tlx_wj4_xz}

사용자 작업에 사용할 수 있는 문자열: 기존 컨텐츠 플래그 지정, 공유 및 표시

| element | key | 기본 텍스트 |
|---|---|---|
| 주석 바닥글 | Wasreviewhelpful | [도움이 되셨습니까?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | 도움이 되셨습니까? |
|  | Ownwasreviewhelpful | [도움이 됩니다.](https://d.pr/i/Q0mA) |
|  | Reviewwasuseful | [예](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [no](https://d.pr/i/Q0mA) |
| 투표 모달 | Votetitle | 이 검토가 유용했습니까? |
|  | Votedownvote | no |
|  | Votereplytitle | 이 회신은 유용합니까? |
|  | Votetitle | 이 댓글이 유용했습니까? |
|  | Voteupvote | 예 |
| Flag Modal | flagtitle | 플래그 % s의 검토 |
|  | Flagsuccessmsg | 검토에 플래그가 지정되었습니다. |
| 모바일 플래그 지정 | Flagconfirmationmessage | % s의 검토를 % s (으) 로 플래그 지정하시겠습니까? |
| 언급표 | Mentiondefaulttext | Livefyre를 소개합니다. |
| Share Modal | sharetitle | 공유 검토 |

## 게시물 함수 {#section_yl1_wj4_xz}

사용자가 검토를 게시하는 데 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| 편집기 | Bodyplaceholder | 검토 작성... |
|  | Posteditbutton | edit |
|  | Posteditcancelbutton | 취소 |
|  | Postasbutton | 다른 이름으로 검토 후... |
|  | Postbutton | 게시물 검토 |
|  | Postreplyasbutton | 다른 이름으로 게시... |
|  | Postreplybutton | POST |
|  | sharebutton | 공유 |
|  | titleplaceholder | 제목... |

## 오류 {#section_jbc_vj4_xz}

일반 오류 메시지에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| 오류 | Erroralreadyposted | 하나의 검토만 게시할 수 있습니다. |
|  | Errorautherror | 이 대화에 대한 검토를 게시할 권한이 없습니다. |
|  | Errorcomments notallowed | 현재 검토를 게시할 수 없습니다. |
|  | Errordislikeowncomment | 자신의 평가를 싫어할 수 없습니다. |
|  | Errorduplicate | 리뷰를 좋아한다면 게시할 수 없습니다. |
|  | erroreditduplicate | 편집할 때 검토 본문을 변경해야 합니다. |
|  | Erroreditnotallowed | 이 대화에서 검토를 편집할 수 없습니다. |
|  | Erroredittimeexceeded | 죄송합니다. 검토 편집 기간이 만료되었습니다. |
|  | Errorempty | 빈 검토를 게시하려고 하는 것 같습니다. |
|  | Erroremptytitle | 빈 제목을 게시하려고 시도하는 것 같습니다. |
|  | Errorfieldrating | 별 등급 |
|  | Errorfieldreview | 리뷰 |
|  | Errorfieldtitle | title |
|  | Errormaxchars | 죄송합니다. 검토가 너무 깁니다. 편집 후 다시 시도하십시오. |
|  | Errormissingfields | Please enter a |
|  | Errorratingempty | 빈 등급은 제출할 수 없습니다. |
|  | Errorratingnotset | 모든 등급을 설정해야 합니다. |
|  | Errorratingnotvalid | 등급은 개체여야 합니다. |
|  | Errorshowmore | 더 많은 검토를 로드하는 동안 오류가 발생했습니다. |
|  | Errortitlemaxchars | 죄송합니다. 제목이 너무 깁니다. 편집 후 다시 시도하십시오. |
|  | Errorvoteowncomment | 자체 검토에 투표할 수 없습니다. |

