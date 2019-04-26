---
description: Livefyre 앱의 문자열 사용자 정의
seo-description: Livefyre 앱의 문자열 사용자 정의
seo-title: 문자열 현지화
solution: Experience Manager
title: 문자열 현지화
uuid: c 0 ab 352 d -5 d 3 a -45 d 7-bbd 0-aed 165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 문자열 현지화{#localize-strings}

Livefyre 앱의 문자열 사용자 정의

Livefyre 앱의 대부분의 HTML 요소에 대한 텍스트 문자열을 사용자 정의할 수 있습니다. 이렇게 하면 렌더링된 HTML 요소 텍스트 (예: "post as" 단추, "comment count" 텍스트 또는 "sign in" 단추) 를 유효한 UTF -8 문자열로 변경할 수 있습니다. 이 기능을 사용하여 스트림 구현에 개성을 추가하거나 사용자의 앱 언어 현지화

* 댓글, 채팅 및 라이브 블로그

   * [구현](#c-localize-strings/section_im4_224_xz)
   * [계정 액세스](#c-localize-strings/section_cm3_d24_xz)
   * [스트림 정보](#c-localize-strings/section_wx1_c24_xz)
   * [스트림 정렬](#c-localize-strings/section_ih2_124_xz)
   * [컨텐츠 정보](#c-localize-strings/section_llv_yd4_xz)
   * [주요 컨텐츠](#c-localize-strings/section_gmw_vd4_xz)
   * [텍스트 편집기](#c-localize-strings/section_ky5_td4_xz)
   * [응답 옵션](#c-localize-strings/section_zvt_qd4_xz)
   * [주석 알림 기능](#c-localize-strings/section_qqt_pd4_xz)
   * [오류 메시지](#c-localize-strings/section_omz_jxn_xz)

* [시간 및 날짜 형식](#c-localize-strings/section_yz4_g5n_xz)
* [미디어 담벼락](#c-localize-strings/section_vwt_d5n_xz)
* [map](#c-localize-strings/section_fxv_c5n_xz)
* [모자이크](#c-localize-strings/section_e2s_b5n_xz)
* [회전판](#c-localize-strings/section_l2z_hkn_xz)
* [Feature Card](#c-localize-strings/section_mw2_hkn_xz)
* [투표](#c-localize-strings/section_pdg_fwh_xz)
* [Livefyre Identity](#c-localize-strings/section_zc3_xvh_xz)
* 자세히:
   * [텍스트 문자열 검토](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Sidenotes](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## 구현 {#section_im4_224_xz}

이 기능을 구현하려면 Javascript 구성 개체로 재정의할 문자열의 1-1 개체 매핑을 전달합니다. 필드를 제공하지 않으면 기본 텍스트가 사용됩니다.

예:

```
var customStrings = {     
   postAsButton: "New Post As Text",     
   postEditButton: "New Post Edit Text"  
};   
   convConfig["strings"] = customStrings; fyre.conv.load(     
   networkConfig,     
   [convConfig],     
   function(){}  
);
```

이 페이지에는 Livefyre 코어 앱에 맞게 사용자 정의할 수 있는 모든 텍스트 문자열이 나열됩니다.

## 계정 액세스 {#section_cm3_d24_xz}

인증 프로세스 및 인증된 사용자 메뉴에서 사용할 수 있는 문자열.

![](assets/strings_threadheader-150x40.png)

| element | key | 기본 텍스트 |
|---|---|---|
|  | Displayname | % s |
|  | Editprofile | 프로필 편집 |
|  | Notifications 설정 | 알림 설정 |
|  | siteadmin | 관리 콘솔 (Studio 링크) |
|  | 로그아웃 | 로그아웃 |

## 스트림 정보 {#section_wx1_c24_xz}

컨텐츠 스트림 정보에 사용할 수 있는 문자열입니다. 의견 수렴, 앱에 대한 게시물 수 및 사용자가 로그인하거나 계정 정보에 액세스할 수 있도록 허용합니다.

| key | 기본 텍스트 | 스트림 데이터 |
|---|---|---|
|  | Commentcountlabelzero | % s 주석 |
|  | Commentcountlabel | % s 주석 |
|  | Commentcountlabelmultiple | % s 댓글 |
|  | Listenercount | 청중 의견 수렴 |
|  | Listenercountmulti | 의견 수렴 |
|  | Liveblogpostcountlabelzero | POST |
|  | Liveblogpostcountlabel | POST |
|  | Liveblogpostcountlabelmultiple | 게시물 |
| 스레드 옵션 | Threadbreakoutbutton | 전체 스레드 표시 |
|  | Togglecollapse | 축소 전환 |
| 고속/큐에 있는 주석 | 새로 고침 | 새로 고침 |
|  | Newcomment | 새 주석 |
|  | Newcomments | 새 댓글 |
|  | Newreply | 새 답글 |
|  | Newreply | 새 답글 |

## 스트림 정렬 {#section_ih2_124_xz}

연령 또는 인기별로 반환된 컨텐츠를 정렬하는 데 사용할 수 있습니다.

![](assets/strings_newestoldesttop-1-150x56.png)

| key | 기본 텍스트 | 헤더 옵션 |
|---|---|---|
|  | Sortlatest | 최신 항목 |
|  | Sortoldest | 가장 오래된 항목 |
|  | Sorttopcomments | 주요 주석 |
|  | Sorthotthreads | Hot Threads |
|  | Sortseparator |  |  |
|  | 간편한 정렬 | 로드 중 |
|  | Topcommentscontentnotfoundmessaging | 아직 좋아요 수가 부족합니다. |
|  | Hotthreadscontentnotfoundmessaging | 아직 스레드가 부족합니다. |
|  | Streamrefreshmsg | 새로운 기능 보기 |
| 바닥글 옵션 | Archiveheadertitle | 보관용 |
|  | Archiveshowmore | 더 보기 |
|  | Showmore | 추가 주석 표시 |
|  | Showmoreliveblog | 게시물 더 보기 |

![](assets/strings_threadend-150x47.png)

## 컨텐츠 정보 {#section_llv_yd4_xz}

게시물 정보 나열: 사용자 이름, 적용된 사용자 태그 및 게시 시간.

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| key | 기본 텍스트 | author |
|---|---|---|
|  | 중재자 | 중재자 |
|  | Hovercardviewprofile | 전체 프로필 보기 |
| 게시물 정보 | Timejustnow | 지금 |
|  | Timeminutesago | 분 전 |
|  | Timeminutesagoplural | 분 전 |
|  | Timehoursago | 시간 전 |
|  | Timehoursagoplural | 시간 전 |
|  | Timedaysago | 일 전 |
|  | Timedaysagoplural | 일 전 |
|  | Likesmultiple | 좋아요 |
|  | Likessingular | like |
|  | Moderatoredittimestamp | 중재자가 편집함 |
|  | Commenttombstone | 이 댓글은 삭제되었습니다. |
|  | Permalinknotfoundmessaging | 이 댓글은 더 이상 표시되지 않습니다. |
|  | Quickprofiletooltip | 빠른 프로필 |

## 주요 컨텐츠 {#section_gmw_vd4_xz}

활성화되면 주요 컨텐츠가 스트림 맨 위에 나열됩니다.

|  | key | 기본 텍스트 |
|---|---|---|
| 주요 레이블 |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | Featuredcommentstag | 주요 기능 |
|  | Featuredcommentfiedleplural | 주요 주석 |

## 텍스트 편집기 {#section_ky5_td4_xz}

기본적으로 모든 사용자에 대해 페이지 상단에서 사용할 수 있습니다.

![](assets/strings_texteditor-1-150x77.png)

|  | key | 기본 텍스트 |
|---|---|---| 
| 편집기 단추 | 팔로우 | + 팔로우 |
|  | Unfollow | - Unfollow |
|  | Liveblogfollow | 라이브 블로그 팔로우 |
|  | Liveblogunfollow | 라이브 블로그 팔로우 취소 |
|  | Postbutton (로그인한 사용자에 대해 사용 가능) | 게시물 주석 |
|  | Postasbutton (인증되지 않은 사용자에 대해 사용 가능) | 다른 이름으로 주석 게시... |
|  | Posteditbutton | 주석 편집 |
|  | Posteditasbutton | 다른 이름으로 주석 편집... |
|  | Posteditcancelbutton | 취소 |
|  | Editordisabled | 이 대화는 현재 새 주석에 대해 차단되었습니다. |
| 채팅 옵션 | livechatpostbuttonlabel | POST |
|  | Livechatposteditbutton | edit |
|  | Livechatwindow sinstruction | Ctrl + Enter 키를 눌러 Post를 게시합니다. |
|  | Livechatotherinstruction | Command + Enter 키를 눌러 Post 키를 게시합니다. |

## 응답 옵션 {#section_zvt_qd4_xz}

별도로 명시되지 않는 한, 로그인한 모든 사용자가 사용할 수 있습니다. 액세스하려면 콘텐츠 패널 위에 마우스를 놓습니다.

![](assets/strings_banusermodal-150x36.png)

| key | 기본 텍스트 |  |
|---|---|---|
| 사용자 응답 옵션 | 최종 사용자에게 제공됩니다. |  |
| Flagbutton | flag |
|  | Flagcommenttooltip | flag |
|  | Editbutton (작성자 및 중재자만 사용 가능) | edit |
|  | Deletebutton (작성자 및 중재자만 사용 가능) | delete |
|  | Deletecommenttooltip | delete |
|  | sharebutton | 공유 |
|  | Sharecommenttooltip | 공유 |
|  | Likebutton | like |
|  | Unlikebutton | unlike |
|  | Replybutton | 답글 |
|  | Replybuttonsingular (채팅 및 라이브 블로그에 사용 가능) | 답글 |
|  | Replybuttonplural (채팅 및 라이브 블로그에 사용 가능) | 답글 |

![](assets/strings_responseoptions-150x35.png)

| key | 기본 텍스트 |  |
|---|---|---|
| Flag Modal | flagtitle | 플래그 % s의 주석 |
|  | Flagsubtitle | 다음으로 플래그 지정 |
|  | Flagdefaultselectoption | 선택 |
|  | Flagspam | 스팸 |
|  | Flagspambutton | 스팸 |
|  | Flagspamcommenttooltip | 스팸 |
|  | Flagoffensive | 불쾌함 |
|  | Flagoffensivebutton | 불쾌함 |
|  | Flagoffensivecommenttooltip | 불쾌함 |
|  | 플래그 없음 | 동의하지 않음 |
|  | Flagdisagreebutton | 동의하지 않음 |
|  | Flagdisagreecommenttooltip | 동의하지 않음 |
|  | Flagofftopic | Off Topic |
|  | Flagofftopicbutton | Off Topic |
|  | Flagofftopiccommenttooltip | Off Topic |
|  | Flagemail | 이메일 |
|  | Flagemailplaceholder | you@example.com |
|  | Flagnotes | 참고 |
|  | Flagnotesplaceholder | 여기에 입력 시작... |
|  | Flagconfirmbutton | OK |
|  | Flagcancelbutton | 취소 |
|  | Flagconfirmationmessage | % s의 주석을 % s (으) 로 플래그 지정하시겠습니까? |
|  | Flagsuccessmsg | 댓글에 플래그가 지정되었습니다. |

![](assets/strings_flagmodal-150x87.png)

| key | 기본 텍스트 |  |
|---|---|---|
| Share Modal | sharetitle | 주석 공유 |
|  | Shareplaceholdertext | 어떻게 생각하십니까? |
|  | Sharelabel | 공유 위치: |
|  | Sharetexttwitter | blank |
|  | Sharetextfacebook | blank |
|  | Sharetextlinkedin | blank |
|  | Sharebuttontext | 공유 |
|  | Sharepermalink | Permalink |
|  | Loadingpermalink | 짧은 URL 로드 중... |
|  | sharetext | 댓글을 게시했습니다. 확인해 보십시오! |

![](assets/strings_sharemodal-150x59.png)

| key | 기본 텍스트 |  |
|---|---|---|
| 답글 모달기 | Postreplyasbutton | 다른 이름으로 주석 게시... |
|  | Postreplybutton (로그인한 사용자에 대해 사용 가능) | 게시물 주석 |
|  | Backtohotthreads | 핫 스레드로 돌아가기 |

![](assets/strings_backto-150x48.png)

| key | 기본 텍스트 |  |
|---|---|---|
| Twitter @ mention modal | mentiontitle | 공유 의견 공유 |
|  | Mentionsubtitletwitter | 트윗 공유: |
|  | Mentiondefaulttext | Livefyre 댓글을 입력했습니다. |
|  | Mentionconfirmbutton | OK |
|  | Mentioncancelbutton | 취소 |
|  | Mentionerrorgeneral | 죄송합니다. 잘못된 문제가 발생했습니다. Livefyre는 경고를 받았습니다. |
|  | Mentionerrornoneselected | 하나 이상의 언급이 활성화되어 있어야 합니다. |
|  | Mentionmenutitle | 친구를 확인하고 언급합니다 |
|  | mentiontwitterconnect | Twitter에 연결 |
|  | mentiontwitterpping | 친구 가져오기... |
|  | Mentionsuccessmsg | 언급이 성공적으로 전송되었습니다. |

![](assets/strings_sharemention-150x60.png)

| key | 기본 텍스트 |  |
|---|---|---|
| 모달 편집 | 스튜디오 관리자, 사용자 관리자 또는 중재자에게 제공 |  |
| @ (@ 언급의 경우) | </> (사용자 지정 HTML 창을 엽니다.) |  |
|  | Customhtmldialogtitle (modal의 헤더로 표시) | 사용자 정의 HTML 추가 |

![](assets/strings_moderatoreditmodal-150x49.png)

| key | 기본 텍스트 |  |
|---|---|---|
| 중재자 응답 옵션 | 스튜디오 관리자, 사용자 관리자 또는 중재자에게 제공됩니다. |  |
| Pendingcomment | 보류 중 |
|  | Banuserbutton | BAN 사용자 |
|  | Banusertooltip | BAN 사용자 |
|  | bozobutton | Bozo |
|  | Bozocommenttooltip | Bozo |
|  | Featurebutton | 기능 |
|  | Featurecommenttooltip | 기능 |
|  | unfeaturebutton | Unfunctionality |
|  | Featuredcommenttooltip | Unfunctionality |

![](assets/strings_adminoptions-150x33.png)

| key | 기본 텍스트 |  |
|---|---|---|
| 사용자 모달링 금지 | 스튜디오 관리자, 사용자 관리자 또는 중재자에게 제공됩니다. |  |
| Bantitle | BAN 사용자 |  |
|  | Banconfirmation | 이 사용자를 금지하시겠습니까? |
|  | Banconfirmbutton | OK |
|  | Bancancelbutton | 취소 |

## 주석 알림 기능 {#section_qqt_pd4_xz}

활성화된 경우 페이지 하단에 모든 Livefyre 대화 앱을 사용할 수 있습니다.

![](assets/strings_notifier-150x112.png)

|  | key | 기본 텍스트 |
|---|---|---|
| 알림 표시자 레이블 | Comment알림 기능 | 새 주석 |
|  | Commentnotifierplural | 새 댓글 |
|  | Liveblognotifier | 새 게시물 |
|  | Liveblognotifierplural | 새 게시물 |

## 오류 메시지 {#section_omz_jxn_xz}

사용자 지정 가능한 오류 메시지에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Errorautherror | 이 대화에 댓글을 게시할 권한이 없습니다. |
| Errorcomments notallowed | 댓글은 이 대화에서 허용되지 않습니다. |
| Errordefault | 오류가 발생했습니다. 다시 시도하십시오. |
| Errorduplicate | 댓글을 좋아한다면 게시할 수 없습니다. |
| erroreditduplicate | 주석을 편집할 때는 주석을 변경해야 합니다. |
| Erroreditnotallowed | 이 대화에서는 댓글을 편집할 수 없습니다. |
| Erroredittimeexceeded | 댓글 편집 기간이 만료되었습니다. |
| Errorempty | 빈 댓글을 게시하려고 하는 것 같습니다. |
| Errorexpired | 세션이 만료되었습니다. 페이지를 다시 로드하십시오. |
| Errorflagnotselected | 플래그 유형을 선택하십시오. |
| Errorguestliked | 죄송합니다. 계정이 있는 사용자만 컨텐츠를 좋아할 수 있습니다. |
| Errorinsufficientpermissions | 권한 부족 |
| Errorinvalidchar | 잘못된 문자를 게시하려고 시도하는 것 같습니다. |
| Errorlikeowncomment | 자신의 의견은 마음에 들지 않습니다. |
| Errormalformed | 잘못된 형식의 컨텐츠를 게시하려고 하는 것 같습니다. |
| Errormaxchars | 댓글이 너무 깁니다. 편집 후 다시 시도하십시오. |
| Errormedianotavailable | 미디어가 더 이상 표시되지 않습니다. |
| Errorshowmore | 추가 댓글을 로드하는 동안 오류가 발생했습니다. |
| Multiplemedianotallowederror | 사용자의 권한은 한 번에 하나의 미디어 첨부 파일만 부여합니다. |

## 시간 및 날짜 형식 {#section_yz4_g5n_xz}

시각화 앱 내의 콘텐츠 카드에 날짜가 표시되는 방식을 번역하고 사용자 정의할 수 있습니다.

| key | 기본 텍스트 |
|---|---|
| Hoursago | {number} h |
| Hoursagosingular | {number} h |
| Justnow | 1s |
| Minutesago | {number} m |
| minutesagosingular | {number} m |
| Monthdayformat | {day} {monthabbrev} |
| Monthdayyearformat | {day} {monthabbrev} {year} |
| Monthnames | 1 월, 2 월, 3 월, 4 월, 5 월, 6 월, 7 월, 8 월, 9 월, 10 월, 11 월, 12 월 |
| Monthnamesabbrev | 1 월, 2 월, 3 월, 4 월, 5 월, 6 월, 7 월, 8 월, 9 월, 10 월, 11 월, 12 월 |
| secondsago | {number} s |
| secondsagosingular | {number} s |

## 미디어 담벼락 {#section_vwt_d5n_xz}

미디어 담벼락 앱에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Featuredtext | 주요 기능 |
| Sharebuttontext | 공유 |

| key | 기본 텍스트 |
|---|---|
| Postbuttontext | 무슨 생각을 하고 계십니까? |
| Postmodaltitle | 댓글 게시 |
| Postmodalbutton | 댓글 게시 |
| Postmodalplaceholder | 어떻게 하시겠습니까? |
| showmorebuttontext | 자세한 내용 |
| Sharebuttontext | 공유 |

## map {#section_fxv_c5n_xz}

지도에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Featuredtext | 주요 기능 |
| Sharebuttontext | 공유 |

## 모자이크 {#section_e2s_b5n_xz}

Mosaics에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Featuredtext | 주요 기능 |
| Sharebuttontext | 공유 |

## 회전판 {#section_l2z_hkn_xz}

Carousel에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Featuredtext | 주요 기능 |
| Sharebuttontext | 공유 |

## Feature Card {#section_mw2_hkn_xz}

기능 카드에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Featuredtext | 주요 기능 |
| Sharebuttontext | 공유 |

## 앱 업로드 {#section_grc_gkn_xz}

업로드 앱에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Postbuttontext | 무슨 생각을 하고 계십니까? |
| Postmodaltitle | 댓글 게시 |
| Postmodalbutton | 댓글 게시 |
| Postmodaltitleplaceholder | 제목 입력 |
| Postmodalplaceholder | 어떻게 하시겠습니까? |
| Postmodalconfirationtitle | 게시해 주셔서 감사합니다. |
| Postmodalconfirmationmessage | 게시물을 검토하고 있습니다. |
| Postmodalconfirmationbutton | done |
| title |  |
| message |  |
| Editorerrorattachmentsrequired | 첨부 파일이 필요합니다. |
| Editorerrorbody | 메시지를 추가하십시오 |
| Editorerrorduplicate | 노트를 원하는 만큼 두 번 게시할 수 없습니다. |
| Editorerrorgeneric | 오류가 발생했습니다. |
| Editorerrortitlerequired | 제목은 필수입니다. |

## 투표 {#section_pdg_fwh_xz}

투표에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|---|---|
| Totalvoteslabel | % s 총 투표 수 |
| Sharestringtext | % s에 투표한 바 있습니다. 투표 결과 |
| Pollclosedlabel | 이 투표는 현재 차단되었습니다. |

## Livefyre Identity {#section_zc3_xvh_xz}

Livefyre ID에 사용할 수 있는 문자열입니다.

| key | 기본 텍스트 |
|--- |--- |
| Automaticallyfollowconversations | 내가 참여한 대화를 자동으로 따릅니다. |
| back | back |
| 소개 | 소개 |
| create | create |
| Createanewaccount | 새 계정 만들기 |
| Createnewaccountwithemail | 이메일로 새 계정 만들기 |
| Changeavatar | 아바타 변경 |
| 파일 선택 | 파일 선택 |
| Completeaccount | 전체 계정 |
| 이메일을 보낼 수 있는 기능 | 누군가 나에게 회신할 때 이메일 전송 |
| Emailcommentsifollow | 내가 팔로우하는 대화의 댓글 이메일 |
| Emailsenttoresetpassword | 이메일 전송! 받은 편지함에서 암호 재설정 링크가 있는지 확인 |
| Emailverificationsent | 이메일 확인 전송 |
| Firstname | first name |
| Forgotpassword | 암호를 잊으셨습니까? |
| Forgotyourpassword | 암호를 잊으셨습니까? |
| Forgotyourpasswordinstructions | 아래에 사용자 이름 또는 이메일 주소를 입력하면 암호를 변경하기 위한 링크가 전송됩니다. |
| Forminputclosebuttontext | 닫기 |
| Forminputcancelbuttontext | 취소 |
| Forminputsavebuttontext | 저장 |
| Hasnotleftanycomments | 댓글을 남기지 않은 경우 |
| Locationisfrom | is from |
| Labelavatar | Avatar |
| Labelcomments | 댓글 |
| Labelconfirmnewpassword | 새 암호 확인 |
| Labelconfirmpassword | 암호 확인 |
| Labelemail | 이메일 주소 |
| Labellikes | 좋아요 |
| Labelloading | 로드 중 |
| Labelnewpassword | 새 암호 |
| Labelnotification | 알림 |
| Labelpassword | password |
| Labelprofile | profile |
| Labelusername | username |
| Labelusernameoremail | 사용자 이름 또는 이메일 |
| Lastname | 성 |
| livefyreaccount | Livefyre 계정 |
| 위치 | 위치 |
| Loadingprofile | 프로필 로드 |
| Newpassword | 새 암호 |
| Oldpassword | 이전 암호 |
| on | on |
| OR | OR |
| Passwordlinkexpired | 암호를 재설정하기 위해 클릭한 링크가 만료되었습니다. 암호를 다시 설정하면 새 링크가 전송됩니다. |
| Pleasecheckemailtocomplete | 등록을 완료하려면 이메일을 확인하십시오. |
| 게시됨 | 게시됨 |
| Poweredby | Powered by |
| Profilenocertificationimmediate | immediate |
| Profilenocertificationhourly | 시간별 |
| Profilenocertificationnever | never |
| Recentcomments | 최근 댓글 |
| 재설정 | 재설정 |
| Resetpassword | 암호 재설정 |
| 로그인 | 로그인 |
| Signinwith | 로그인 |
| Signinwithemail | 이메일로 로그인 |
| 등록 | 등록 |
| socialaccount | 소셜 계정 |
| Successpasswordchanged | 성공! 암호가 변경되었으며 이제 |
| Termsandconditions | 약관 |
| Termsandconditionsintro | 가입하면 |
| Termsofuse | 사용 약관 |
| Termsofuseintro | 로그인하면 |
| Thisuser | 이 사용자 |
| Verifypassword | 암호 확인 |
| Filesizelimit | 최대 2 MB |
| Accountnotfound | 계정을 찾을 수 없음 |
| Avatarimageexceedsize | 아바타 이미지가 2 MB 파일 제한을 초과했습니다. |
| Fieldisrequired | 필드는 정수만 허용합니다. |
| Fieldonlyacceptsavalidemail | 필드가 유효한 이메일만 수락합니다. |
| Fieldonlyacceptdependencyters | 필드에는 문자만 허용됩니다. |
| Filesizemustbelessthanmb | 파일 크기는 MB 보다 {#}작아야 합니다. |
| invalidusernameorpassword | 잘못된 사용자 이름 또는 암호 |
| Minimumlengthofcharacters | 최소 문자 {#} 길이 |
| Maximumlengthofcharacters | 최대 문자 {#} 길이 |
| Therewasanerror | 오류가 발생했습니다. |
| Thisfieldisrequired | 이 필드는 필수입니다. |
| Validfileextensions | 유효한 파일 확장 |
| Valuemustmatch | 값이 일치해야 합니다. |
| Passwordlength | 길이가 6-32 자로 길어집니다. |
| Passwordcharacters | 소문자 문자와 대문자를 모두 포함합니다. |
| Passwordsymbols | 하나 이상의 숫자와 기호를 포함합니다. |
| Passwordusername | 사용자 이름을 포함하지 않습니다. |
| Passwordpopovertitle | 암호는 다음을 수행해야 합니다. |
| Passworderrorcontainsfirstname | 입력한 암호는 사용자 이름, 이름 또는 성을 포함합니다. 보안상의 이유로 사용자 이름, 이름 또는 성을 포함하지 않는 암호를 입력하십시오. 암호에 다음이 포함되어야 합니다. 6-32 문자 대문자 문자소문자 a 기호 |
| Passworderrorcontainslastname | 입력한 암호는 사용자 이름, 이름 또는 성을 포함합니다. 보안상의 이유로 사용자 이름, 이름 또는 성을 포함하지 않는 암호를 입력하십시오. 암호에 다음이 포함되어야 합니다. 6-32 문자 대문자 문자소문자 a 기호 |
| Passworderrorcontainsusername | 입력한 암호는 사용자 이름, 이름 또는 성을 포함합니다. 보안상의 이유로 사용자 이름, 이름 또는 성을 포함하지 않는 암호를 입력하십시오. 암호에 다음이 포함되어야 합니다. 6-32 문자 대문자 문자소문자 a 기호 |
| Passworderrortooshort | pasword의 최소 6 자 |
| Passworderrortoolong | 암호에 최대 32 자 |
| Passworderrormissinguppercase | 암호에는 하나 이상의 대문자 문자가 있어야 합니다. |
| Passworderrormissinglowercase | Passsword 에는 하나 이상의 소문자 문자가 포함되어야 합니다. |
| Passworderrormissingsymbol | 암호에는 세트에 하나 이상의 기호가 포함되어야 합니다. `!@#$%^&*()?.,<>\’;:”[]{}|` |


