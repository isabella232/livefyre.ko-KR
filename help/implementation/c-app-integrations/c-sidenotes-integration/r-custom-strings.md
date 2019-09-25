---
description: 'null'
seo-description: 'null'
seo-title: 사이드노트 사용자 지정 문자열
title: 사이드노트 사용자 지정 문자열
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 사이드노트 사용자 지정 문자열{#sidenotes-custom-strings}

사용자 지정 문자열은 Sidenotes 생성자에 삽입된 객체를 통해 적용되며 응용 프로그램을 통해 사용되는 기본 문자열을 재정의합니다. 이러한 기능은 스타일 또는 언어 사양에 맞게 언어의 모든 부분을 사용자 지정하는 데 사용할 수 있습니다. 문자열은 자동으로 기본값으로 병합됩니다.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| 키 | 기본값 |
|---|---|
| appName | 사이드노트 |
| commentAdvertiserTag | Mod |
| commentPendingTag | 대기 중 |
| commentReadMoreLink | 자세히 보기 |
| commentReplyLink | 답글 {number}개 보기 |
| commentReplyLinkSing | 회신 보기 |
| commentVoteCount | 투표 |
| comment 파섹 | 개의 투표 |
| editorPlaceholder | 어떻게 생각해? |
| editorPostBtn | 게시물 사이드노트 |
| editorPostBtnMobile | 게시물 |
| editorPublishing | 게시 중… |
| editorReplyBtn | 회신 게시 |
| editorReplyTitle | 답글 쓰기 |
| editorTitle | 메모 작성 |
| emptyImageBlockTxt | 어떻게 생각해? |
| emptyTextBlockTxt | + |
| errorConnection | 아.. 당신은 사이가 좋지 않은 것 같아요 |
| errorDuplicate | 저희도 마음에 드는데 두 번 게시할 수는 없습니다 |
| errorGeneral | 오류가 발생했습니다. 다시 시도하십시오. |
| errorServer | 서버에 문제가 발생했습니다. 다시 시도하시겠습니까? |
| facebookShareCaption | "{title}"의 SideNotes |
| menuAuthSignedInMsg | {action}에 로그인해야 합니다. |
| menuAuthSignInBtn | 로그인 |
| menuBackBtn | 뒤로 |
| menuConfirmAccept | 예, {action} |
| menuConfirmCancel | 취소 |
| menuConfirmTitle | 계속하시겠습니까? |
| menuEtcOptionApprove | 승인 |
| menuEtcOptionDelete | 삭제 |
| menuEtcOptionEdit | 편집 |
| menuEtcOptionFlag | 플래그 |
| menuEtcOptionShare | 공유 |
| menuEtcPostedAt | {date}에 게시됨 |
| menuEtcTitle | 자세히 |
| menuFlagOptionDissuse | 반대 |
| menuFlagOptionOffensive | 공격 |
| menuFlagOptionOffTopic | 주제 해제 |
| menuFlagOptionSpam | 스팸 |
| menuFlagTitle | 플래그 지정... |
| menuInfoCopyright | (C) Livefyre, Inc. 2014 |
| menuInfoHelp | 도움말 |
| menuInfoLivefyreLink | Livefyre.com 방문 |
| menuRepliesViewReply | 대화에 회신 |
| menuRepliesViewTitle | 세부 사항 |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Permalink 복사 |
| menuShareOptionLinkComplete | 복사됨 |
| menuShareOptionLinkFailed | 복사 실패 |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | 공유 |
| notificationApproved | 승인됨 |
| notificationDeleted | 삭제됨 |
| notificationFlagged | 플래그 지정됨 |
| permalinkBackBtn | 모든 |
| permalinkTitle | 페르말링크 |
| 질문 설명 | 이제 문장, 단락, 이미지 및 따옴표에 직접 주석을 읽고 쓸 수 있습니다.<br><br>텍스트를 강조 표시하고 "fycon-write" 아이콘을 클릭하거나 각 단락 끝에 있는 "fycon-action-view" 아이콘을 클릭합니다. |
| questionMockText | "친숙한" 것은 "친숙하다" 라는 이유로 잘 알려져 있지 않다. |
| questionTitle | 사이드노트란? |
| queuedCommentsPlural | {number}개의 새 사이드노트 |
| queuedCommentsSingular | 1 새 시드노트 |
| queuedRepliesPlural | {number}개의 새 답글 |
| queuedRepliesSingular | 1 새 답글 |
| replyBtn | 답글 |
| signInToPost | 사이드노트 작성을 위해 로그인 |
| sliderCommentTally | / |
| sliderInviteRead | 읽음 |
| sliderInviteWrite | 쓰기 |
| sliderWriteText | 어떻게 생각해? 눌러서 쓰기 |
| threadCollapseBtn | 축소 |
| threadExpandBtnPlural | 답글 {number}개 확장 |
| threadExpandBtnSingular | 답글 1개 확장 |
| threadReplyBtn | 대화에 회신 |
