---
description: Livefyre Sidenotes의 텍스트 문자열 사용자 정의
seo-description: Livefyre Sidenotes의 텍스트 문자열 사용자 정의
seo-title: Sidenotes 텍스트 문자열
solution: Experience Manager
title: Sidenotes 텍스트 문자열
uuid: A 3735237-E 55 D -4 BC 0-B 88 D -8 A 323980 EE 09
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes 텍스트 문자열{#sidenotes-text-strings}

Livefyre Sidenotes의 텍스트 문자열 사용자 정의

이 페이지에서는 Sidenotes 앱의 사용자 지정에 사용할 수 있는 모든 문자열을 나열하고 설명합니다. 코어 Livefyre 앱에 사용할 수 있는 문자열에 대한 자세한 내용은 문자열 사용자 정의를 참조하십시오.

구현
인증
스트림 정보
작성자/컨텐츠 정보
사용자 작업
게시물 기능
중재자 인터페이스
오류

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
| Auth 메뉴 문자열 | Menuauthsigninbtn | 로그인 |
|  | Menuauthsignedinmessaging | {action} 에 로그인되어 있어야 합니다. |
|  | Menuusereditprofile | 프로필 편집 |
|  | Menuuseradmin | Admin Console |
|  | Menuuserlogout | 로그아웃 |
|  | Menuuserbackbtn | all |

## 스트림 정보 {#section_wpy_gl4_xz}

컨텐츠 스트림 정보에 사용할 수 있는 문자열입니다.

| element | key | 기본 텍스트 |
|---|---|---|
| 정보 메뉴 옵션 | Menuinfocopyright | © Livefyre, Inc. 2014 |
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
|  | Datetimemonths | 배열. 기본값 =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | Questiondescription | 이제 문장, 단락, 이미지 및 견적에서 직접 주석을 읽고 쓸 수 있습니다.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">텍스트를</span> 강조 표시하고 <span class="&rdquo;fycon-write&rdquo;"></span> 아이콘을 클릭하거나 각 단락의 끝에 있는 <span class="&rdquo;fycon-action-view&rdquo;"></span> 아이콘을 클릭합니다. |
|  | Questionmoqutext | " 친숙한 "이란" 친숙한 "이유로 잘 알려져 있지 않습니다. |
|  | Questiontitle | 소개 소개 |

## 사용자 작업 {#section_qxd_fl4_xz}

사용자 작업에 사용할 수 있는 문자열: 기존 컨텐츠 플래그 지정, 공유 및 좋아요 표시

| element | key | 기본 텍스트 |
|---|---|---|
| 응답 메뉴 옵션 | Menupreciesviewtitle | 세부 사항 |
|  | Menupreciesviewreply | 대화에 응답 |
| 공유 메뉴 옵션 | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | menusharetitle | 공유 |
| 플래그 메뉴 옵션 | Menuflagoptiondisagree | 동의하지 않음 |
|  | Menuflagoptionoffensive | 불쾌함 |
|  | Menuflagoptionofftopic | Off Topic |
|  | Menuflagoptionspam | 스팸 |
|  | Menuflagtitle | 다른 이름으로 플래그 지정... |
|  | Facebooksharecaption | " {title} "의 Sidenotes |
| 모바일 사용자 옵션 | Slidercommenttally | of |
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
| 메뉴 옵션 삭제 | Menuconfirmaccept | 예, {action} |
|  | Menuconfirmcancel | 취소 |
|  | Menuconfirmtitle | 계속하시겠습니까? |
| etc menu options | Menuetcoptionapprove | 승인 |
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
| 추가 메뉴에서 확인 메시지 | Notificationapproved | 승인됨 |
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

