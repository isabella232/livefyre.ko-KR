---
description: 번역 세트를 사용하면 앱에 대한 대체 언어를 지정할 수 있습니다.
seo-description: 번역 세트를 사용하면 앱에 대한 대체 언어를 지정할 수 있습니다.
seo-title: 번역 세트
solution: Experience Manager
title: 번역 세트
uuid: 8 BA 66 A 61-5520-482 A-BC 0 B-E 4 F 6 B 57 F 1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48

---


# 번역 세트 {#translation-sets}

번역 세트를 사용하면 앱에 대한 대체 언어를 지정할 수 있습니다.

<!-- 
c_translation_sets.dita
-->

번역 설정을 사용하여 다양한 언어로 앱을 로컬라이즈하거나 스튜디오 내의 한 위치에서 여러 앱에 대한 대체 텍스트를 지정할 수 있습니다. 예를 들어 모든 스페인어 사이트에서 모든 앱 필드에 스페인어 언어를 사용하도록 할 수 있습니다. 모든 필드가 사이트 또는 네트워크의 음성 및 느낌과 일치하도록 텍스트를 수정할 수도 있습니다.

Storify 2를 제외한 모든 앱에 대한 번역 설정을 지정할 수 있습니다. 현지화할 수 있는 필드에 대한 자세한 내용은 [현지화 문자열을](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)참조하십시오.

댓글, 라이브 블로그 및 채팅은 번역 세트 내에서 동일한 문자열 세트를 공유합니다.

네트워크, 사이트, 앱 또는 API를 사용할 번역 세트를 지정합니다.

서로 다른 수준의 번역 세트는 이 패턴 다음에 서로 겹쳐집니다.

* API 변환 세트는 모든 수준 (앱, 네트워크 및 사이트) 에서 모든 번역 세트를 무시합니다.
* 앱 번역 세트는 네트워크 수준 및 사이트 수준 번역 집합을 무시합니다.
* 사이트 수준 번역 세트는 네트워크 수준 번역 집합을 무시합니다.

## 텍스트 문자열 검토 {#c-review-text-strings}

Livefyre 검토를 위한 텍스트 문자열 사용자 지정을 참조하십시오.

이 페이지에서는 검토 앱에서 사용자 지정에 사용할 수 있는 문자열을 나열하고 설명합니다. 문자열 사용자 정의에 나열된 Livefyre 핵심 앱의 기본 문자열에 대한 추가 및 재정의 문자열이 여기에 나와 있습니다. 중복 항목이 나열되는 경우, 이 표에 나열된 문자열은 검토 앱의 기본값입니다.

* 구현
* 리뷰/평점 인터페이스
* 스트림 정보
* 작성자/컨텐츠 정보
* 사용자 작업
* 게시물 함수
* 오류

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 단추 |  |  |
|  | Editreviewbtn | 편집 검토 |
|  | Reviewbtn | Write Review |
|  | Reviewsclosed | 닫은 평가 |
|  | Showreviewbtn | 검토 표시 |
|  | 팔로우 | 관심이 있습니다 |
|  | sharetext | 방금 검토를 마쳤습니다. 확인해 보십시오! |
| 등급 툴팁 |  |  |
|  | Ratingvalues | 배열. default =[' poor ',' poor ',' fair ',' fair ',' average ',' average ',' good ',' good ',' excellent ',' superior ']; |
|  |  | 참고: 배열의 값을 복제하여 각 별의 왼쪽 및 오른쪽 절반을 같은 이름으로 지정해야 합니다. |
| 하위 파트 등급 지정 |  |  |
|  | Ratingsubpartplaceholder | 배열. 기본값 =[] |
|  | Ratingsubparttitles | 배열. 기본값 =[] |
|  | Reviewstreamtitle | 기본적으로 비어 있습니다. 검토 요약 섹션의 제목입니다. |
| Misc |  |  |
|  | Averagerating | 평균 사용자 등급 |
|  | Breakdownheader | 등급 분류 |
|  | 유용성 | % s of % s found useful |
|  | 도움말 | % s of % s found useful |
|  | outof | / |
|  | Ratingtype | 별 |

## 스트림 정보 {#section_wmv_yj4_xz}

컨텐츠 스트림 정보에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| *정렬* |  |  |
|  | Sortby | *기본적으로 비어 있습니다.* |
|  | sorthighestrated | [최고 등급](https://d.pr/i/huTd) |
|  | Sortlowestrated | [가장 낮은 등급](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [가장 유용한 정보](https://d.pr/i/huTd) |
| *스트림 Misc.* |  |  |
|  | Showmore | 더 보기 |
| *고속 스트림 스트리밍* |  |  |
|  | Newcomment | 새로운 검토 |
|  | Newcomments | 새로운 검토 |
| *리스너 카운트* |  |  |
|  | Listenercount | 청중 의견 수렴 |
|  | Listenercountmulti | 의견 수렴 |
| *주석 수* |  |  |
|  | Commentcountlabel | Livereviews |
|  | Commentcountlabelmultiple | Livereviews |
| *주석 알림 횟수* |  |  |
|  | Comment알림 기능 | 새로운 검토 |
|  | Commentnotifierplural | 새로운 검토 |

## 작성자/컨텐츠 정보 {#section_osx_xj4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있습니다.

| element | key | 기본 텍스트 |
|---|---|---|
| *스레드 소규모 회의* |  |  |
|  | Reviewscontentnotfoundmessaging | [이 검토는 더 이상 표시되지 않습니다.](https://d.pr/i/svXs) |
|  | Backtocomments | 검토로 돌아가기 |

## 사용자 작업 {#section_tlx_wj4_xz}

사용자 작업에 사용할 수 있는 문자열: 기존 컨텐츠 플래그 지정, 공유 및 표시

| element | key | 기본 텍스트 |
|---|---|---|
| *주석 바닥글* |  |  |
|  | Wasreviewhelpful | [도움이 되셨습니까?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | 도움이 되셨습니까? |
|  | Ownwasreviewhelpful | [도움이 됩니다.](https://d.pr/i/Q0mA) |
|  | Reviewwasuseful | [예](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [no](https://d.pr/i/Q0mA) |
| *투표 모달* |  |  |
|  | Votetitle | 이 검토가 유용했습니까? |
|  | Votedownvote | no |
|  | Votereplytitle | 이 회신은 유용합니까? |
|  | Votetitle | 이 댓글이 유용했습니까? |
|  | Voteupvote | 예 |
| *Flag Modal* |  |  |
|  | flagtitle | 플래그 % s의 검토 |
|  | Flagsuccessmsg | 검토에 플래그가 지정되었습니다. |
| *모바일 플래그 지정* |  |  |
|  | Flagconfirmationmessage | % s의 검토를 % s (으) 로 플래그 지정하시겠습니까? |
| *언급표* |  |  |
|  | Mentiondefaulttext | Livefyre를 소개합니다. |
| *Share Modal* |  |  |
|  | sharetitle | 공유 검토 |

## 게시물 함수 {#section_yl1_wj4_xz}

사용자가 검토를 게시하는 데 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| *편집기* |  |  |
|  | Bodyplaceholder | 검토 작성... |
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
| 오류 |  |  |
|  | Erroralreadyposted | 하나의 검토만 게시할 수 있습니다. |
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

## Sidenotes 텍스트 문자열 {#c_sidenotes_text_strings}

Livefyre Sidenotes의 텍스트 문자열 사용자 정의

<!-- 

c_sidenotes_text_strings.dita

 -->

이 페이지에서는 Sidenotes 앱의 사용자 지정에 사용할 수 있는 모든 문자열을 나열하고 설명합니다. 코어 Livefyre 앱에 사용할 수 있는 문자열에 대한 자세한 내용은 문자열 사용자 정의를 참조하십시오.

* 구현
* AUTH
* 스트림 정보
* 작성자/컨텐츠 정보
* 사용자 작업
* 게시물 함수
* 중재자 인터페이스
* 오류

## 구현 {#section_wp2_ql4_xz}

이 기능을 구현하려면 Javascript 구성 개체로 재정의할 문자열의 1-1 개체 매핑을 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

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

| element | key | 기본 텍스트 |
|---|---|---|
| *Auth 메뉴 문자열* |  |  |
|  | Menuauthsigninbtn | 로그인 |
|  | Menuauthsignedinmessaging | {action} 에 로그인되어 있어야 합니다. |
|  | Menuusereditprofile | 프로필 편집 |
|  | Menuuseradmin | Admin Console |
|  | Menuuserlogout | 로그아웃 |
|  | Menuuserbackbtn | all |

## 스트림 정보 {#section_wpy_gl4_xz}

컨텐츠 스트림 정보에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| *정보 메뉴 옵션* |  |  |
|  | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | help |
|  | menuinfolivefyrelink | Livefyre.com 방문 |

## 작성자/컨텐츠 정보 {#section_dhb_gl4_xz}

작성자 및 개별 컨텐츠 정보에 사용할 수 있습니다.

| element | key | 기본 텍스트 |
|---|---|---|
|  | Commentmoderatortag | MOD |
|  | Commentpendingtag | 보류 중 |
|  | Commentreadmorelink | 자세히 보기 |
|  | Commentreplylink | {number} 답글 참조 |
|  | Commentreplylinksing | 답글 보기 |
|  | Commentvotecount | 투표수 |
|  | Commentvotecountsing | 투표 |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | * 배열. 기본값 = *[ ' 1 월 ',' 2 월 ',' 3 월 ',' 4 월 ',' 5 월 ',' 6 월 ',' 7 월 ',' 8 월 ',' 9 월 ',' 10 월 ',' 11 월 ',' 12 월 ' ] |
|  | Questiondescription | 이제 문장, 단락, 이미지 및 견적에서 직접 주석을 읽고 쓸 수 있습니다. <br>텍스트를 강조 표시하고 아이콘을 클릭하거나 각 단락의 끝에 있는 아이콘을 클릭합니다. |
|  | Questionmoqutext | " 친숙한 "이란" 친숙한 "이유로 잘 알려져 있지 않습니다. |
|  | Questiontitle | 소개 소개 |

## 사용자 작업 {#section_qxd_fl4_xz}

사용자 작업에 사용할 수 있는 문자열: 기존 컨텐츠 플래그 지정, 공유 및 좋아요 표시

| element | key | 기본 텍스트 |
|---|---|---|
| *응답 메뉴 옵션* |  |  |
|  | Menupreciesviewtitle | 세부 사항 |
|  | Menupreciesviewreply | 대화에 응답 |
| *공유 메뉴 옵션* |  |  |
|  | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | menusharetitle | 공유 |
| *플래그 메뉴 옵션* |  |  |
|  | Menuflagoptiondisagree | 동의하지 않음 |
|  | Menuflagoptionoffensive | 불쾌함 |
|  | Menuflagoptionofftopic | Off Topic |
|  | Menuflagoptionspam | 스팸 |
|  | Menuflagtitle | 다른 이름으로 플래그 지정... |
|  | Facebooksharecaption | " {title} "의 Sidenotes |
| *모바일 사용자 옵션* |  |  |
|  | Slidercommenttally | of |
|  | Sliderinvitation eread | read |
|  | Sliderinvitation ewrite | write |
|  | 슬라이드로딩 | 로드 중... |
|  | Sliderwritetext | 어떻게 생각하십니까? 눌러서 작성을 완료합니다. |

## 게시물 함수 {#section_xzf_2l4_xz}

사용자가 컨텐츠를 게시하는 데 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
|  | Editoreditbtn | 저장 |
|  | Editoreditposting | 저장 중... |
|  | Editoreditreplytitle | 회신 편집 |
|  | Editoredittitle | Sienote 편집 |
|  | Editorplaceholder | 어떻게 생각하십니까? |
|  | Editorpostbtn | 게시물 안내 |
|  | Editorpostbtnmobile | POST |
|  | Editorposting | 게시 중... |
|  | Editorreplybtn | 게시물 회신 |
|  | Editorreplytitle | 회신 쓰기 |
|  | Editortitle | 문자 쓰기 |
|  | Emptyimageblocktxt | 어떻게 생각하십니까? |
|  | Emptytextblocktxt | + |
|  | replybtn | 답글 |
|  | Threadreplybtn | 대화에 응답 |
| *메뉴 옵션 삭제* |  |  |
|  | Menuconfirmaccept | 예, {action} |
|  | Menuconfirmcancel | 취소 |
|  | Menuconfirmtitle | 계속하시겠습니까? |
| *etc menu options* |  |  |
|  | Menuetcoptionapprove | 승인 |
|  | Menuetcoptiondelete | delete |
|  | Menuetcoptionedit | edit |
|  | Menuetcoptionflag | flag |
|  | Menuetcoptionshare | 공유 |
|  | Menuetcpostedat | {date} 에 게시됨 |
|  | Menuetctitle | 자세히 |

## 중재자 인터페이스 {#section_o5f_dl4_xz}

사용자 인증 중재자 인터페이스에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| *추가 메뉴에서 확인 메시지* |  |  |
|  | Notificationapproved | 승인됨 |
|  | Notificationdeleted | 삭제됨 |
|  | Notificationflag | 플래그 지정됨 |

## 오류 {#section_gtk_cl4_xz}

일반 오류 메시지에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
|  | Errorconnection | 걱정하지 마십시오. 연결이 끊어진 것 같습니다. |
|  | Errorduplicate | 메모도 마음에 드지만 게시할 수는 없습니다. |
|  | Errorgeneral | 오류가 발생했습니다. 다시 시도하십시오. |
|  | Errorserver | 서버에서 잘못된 문제가 발견되었습니다. 다시 시도하시겠습니까? |
