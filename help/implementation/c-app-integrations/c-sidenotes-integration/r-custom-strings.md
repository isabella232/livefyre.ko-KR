---
description: null
seo-description: null
seo-title: Sidenotes 사용자 정의 문자열
title: Sidenotes 사용자 정의 문자열
uuid: 73745273-D 3 FB -4569-8910-D 149 FB 37 A 7 B 4
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes 사용자 정의 문자열{#sidenotes-custom-strings}

사용자 지정 문자열은 Sidenotes 생성자에 주입된 개체를 통해 적용되며, 응용 프로그램을 통해 사용되는 기본 문자열을 무시합니다. 스타일 또는 언어 사양에 맞게 언어의 일부를 사용자 정의하는 데 사용할 수 있습니다. 문자열은 기본적으로 기본값이 병합됩니다.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| key | 기본값 |
|---|---|
| Appname | Sidenotes |
| Commentmoderatortag | MOD |
| Commentpendingtag | 보류 중 |
| Commentreadmorelink | 자세히 보기 |
| Commentreplylink | {number} 답글 참조 |
| Commentreplylinksing | 답글 보기 |
| Commentvotecount | 투표수 |
| Commentvotecountsing | 투표 |
| Editorplaceholder | 어떻게 생각하십니까? |
| Editorpostbtn | 게시물 안내 |
| Editorpostbtnmobile | POST |
| Editorposting | 게시 중... |
| Editorreplybtn | 게시물 회신 |
| Editorreplytitle | 회신 쓰기 |
| Editortitle | 메모 작성 |
| Emptyimageblocktxt | 어떻게 생각하십니까? |
| Emptytextblocktxt | + |
| Errorconnection | 걱정하지 마십시오. 연결이 끊어진 것 같습니다. |
| Errorduplicate | 메모도 마음에 드지만 게시할 수는 없습니다. |
| Errorgeneral | 오류가 발생했습니다. 다시 시도하십시오. |
| Errorserver | 서버에서 잘못된 문제가 발견되었습니다. 다시 시도하시겠습니까? |
| Facebooksharecaption | " {title} "의 sidenotes |
| Menuauthsignedinmessaging | {action} 에 로그인되어 있어야 합니다. |
| Menuauthsigninbtn | 로그인 |
| Menubackbtn | back |
| Menuconfirmaccept | 예, {action} |
| Menuconfirmcancel | 취소 |
| Menuconfirmtitle | 계속하시겠습니까? |
| Menuetcoptionapprove | 승인 |
| Menuetcoptiondelete | delete |
| Menuetcoptionedit | edit |
| Menuetcoptionflag | flag |
| Menuetcoptionshare | 공유 |
| Menuetcpostedat | {date} 에 게시됨 |
| Menuetctitle | 자세히 |
| Menuflagoptiondisagree | 동의하지 않음 |
| Menuflagoptionoffensive | 불쾌함 |
| Menuflagoptionofftopic | Off Topic |
| Menuflagoptionspam | 스팸 |
| Menuflagtitle | 다른 이름으로 플래그 지정... |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | help |
| menuinfolivefyrelink | Livefyre.com 방문 |
| Menupreciesviewreply | 대화에 응답 |
| Menupreciesviewtitle | 세부 사항 |
| Menushareoptionfacebook | Facebook |
| menushareoptionlink | Copy Permalink |
| Menushareoptionlinkcomplete | 복사됨 |
| Menushareoptionlinkfailed | 복사 실패 |
| Menushareoptiontwitter | Twitter |
| menusharetitle | 공유 |
| Notificationapproved | 승인됨 |
| Notificationdeleted | 삭제됨 |
| Notificationflag | 플래그 지정됨 |
| Permalinkbackbtn | all |
| Permalinktitle | Permalink |
| Questiondescription | 이제 문장, 단락, 이미지 및 견적에서 직접 주석을 읽고 쓸 수 있습니다.<br><br>텍스트를 강조 표시하고 "fycon-write" 아이콘을 클릭하거나 각 단락의 끝에 있는 "fycon-action-view" 아이콘을 클릭합니다. |
| Questionmoqutext | " 친숙한 "이란" 친숙한 "이유로 잘 알려져 있지 않습니다. |
| Questiontitle | 소개 소개 |
| Queuedcommentsplural | {number} 새 Sidenotes |
| Queuedcommentssingular | 1 새로운 기능 시작하기 |
| Queuedrepliesplural | {number} 새 답글 |
| Queuedśessingular | 1 개의 새 답글 |
| replybtn | 답글 |
| Signintopost | 로그인하여 시연하기 |
| Slidercommenttally | of |
| Sliderinvitation eread | read |
| Sliderinvitation ewrite | write |
| Sliderwritetext | 어떻게 생각하십니까? 눌러서 쓰기 |
| Threadcollapsebtn | 축소 |
| Threadexpandbtnmultiple | {number} 답글 확장 |
| Threadexpandbtnsingular | 1 회 응답 확장 |
| Threadreplybtn | 대화에 응답 |
