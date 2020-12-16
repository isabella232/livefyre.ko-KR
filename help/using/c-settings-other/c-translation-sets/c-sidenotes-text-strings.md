---
description: Livefyre 사이드노트에 대한 텍스트 문자열 사용자 정의
seo-description: Livefyre 사이드노트에 대한 텍스트 문자열 사용자 정의
seo-title: 텍스트 문자열 사이드노트
solution: Experience Manager
title: 텍스트 문자열 사이드노트
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 12%

---


# 사이드노트 텍스트 문자열{#sidenotes-text-strings}

Livefyre 사이드노트에 대한 텍스트 문자열 사용자 정의

이 페이지에서는 Sidecotes 앱의 사용자 지정에 사용할 수 있는 모든 문자열을 나열하고 설명합니다. 핵심 Livefyre 앱에 사용할 수 있는 문자열에 대한 자세한 내용은 문자열 사용자 지정을 참조하십시오.

구현
인증
스트림 정보
작성자/컨텐츠 정보
사용자 작업
게시 함수
중재자 인터페이스
오류

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
| 인증 메뉴 문자열 | menuAuthSignInBtn | 로그인 |
|  | menuAuthSignedInMsg | {action}에 로그인해야 합니다. |
|  | menuUserEditProfile | 프로필 편집 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 로그아웃 |
|  | menuUserBackBtn | 모든 |

## 스트림 정보 {#section_wpy_gl4_xz}

콘텐츠 스트림 정보 및 표시에 사용할 수 있는 문자열.

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 정보 메뉴 옵션 | menuInfoCopyright | © Livefyre, Inc. 2014 |
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
|  | datetimeMonths | 배열. 기본값 =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExpliction | 이제 문장, 단락, 이미지 및 인용문에 직접 주석을 읽고 쓸 수 있습니다.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">텍스트</span> 를 강조 표시하고  <span class="&rdquo;fycon-write&rdquo;"></span> 아이콘을 클릭하거나 각 단락 끝 <span class="&rdquo;fycon-action-view&rdquo;"></span> 에 있는 아이콘을 클릭합니다. |
|  | questionMockText | &quot;친숙한&quot; 것은 &quot;친숙하다&quot; 라는 이유로 잘 알려져 있지 않다. |
|  | questionTitle | 사이드노트란? |

## 사용자 작업 {#section_qxd_fl4_xz}

사용자 작업에 사용할 수 있는 문자열:플래그 지정, 공유 및 기존 컨텐츠 좋아요 지정

| 요소 | 키 | 기본 텍스트 |
|---|---|---|
| 응답 메뉴 옵션 | menuRepliesViewTitle | 세부 사항 |
|  | menuRepliesViewReply | 대화에 회신 |
| 공유 메뉴 옵션 | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 공유 |
| 플래그 메뉴 옵션 | menuFlagOptionUnagree | 반대 |
|  | menuFlagOptionOffensive | 공격 |
|  | menuFlagOptionOffTopic | 주제 해제 |
|  | menuFlagOptionSpam | 스팸 |
|  | menuFlagTitle | 플래그... |
|  | facebookShareCaption | &quot;{title}&quot;의 사이드노트 |
| 모바일 사용자 옵션 | sliderCommentTally | / |
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
| 삭제 메뉴 옵션 | menuConfirmAccept | 예, {action} |
|  | menuConfirmCancel | 취소 |
|  | menuConfirmTitle | 계속하시겠습니까? |
| 기타 메뉴 옵션 | menuEtcOptionApprove | 승인 |
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
| 자세히 메뉴의 확인 메시지 | notificationApproved | 승인됨 |
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

