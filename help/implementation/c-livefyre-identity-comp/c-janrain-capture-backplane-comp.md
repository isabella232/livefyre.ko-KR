---
description: Janrain Capture 및 후면판을 사용하는 고객은 SSO(Single Sign On)에 대해 Livefyre 인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.
seo-description: Janrain Capture 및 후면판을 사용하는 고객은 SSO(Single Sign On)에 대해 Livefyre 인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.
seo-title: 잔레인 캡처/후면판
solution: Experience Manager
title: 잔레인 캡처/후면판
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 1%

---


# 재엔 캡처/후면판{#janrain-capture-backplane}

Janrain Capture 및 후면판을 사용하는 고객은 SSO(Single Sign On)에 대해 Livefyre 인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.

이 내장 캡처/후면판 통합을 활용하려면 캡처 앱과 Livefyre.js 통합 모두에 대한 구성을 변경해야 합니다.

>[!NOTE]
>
>Janrain Capture를 사용하지 않는 경우 이 섹션을 건너뜁니다.

자세한 내용은 [Janrain의 후면판 설명서](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)를 참조하십시오.

1. [캡처 설정을 참조하십시오.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (선택 사항) [Livefyre 기본값을 캡처 앱](#c_janrain_capture_backplane/section_z2s_txt_bbb)에 추가합니다.
1. [AuthDelegate 개체를 작성합니다.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Pull용 Ping을 사용하여 Livefyre와 동기화](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 1단계:캡처 설정 {#section_r2f_kxt_bbb}

Livefyre는 Janrain Capture 앱에서 특정 자격 증명이 필요합니다.

1. Janrain Capture 앱을 설정합니다.
1. Livefyre에 대한 다음 정보를 수집합니다.

   * Janrain Capture 인스턴스에 액세스합니다.
   * Janrain Engage 대시보드를 이용할 수 있습니다.
   * 캡처 설정 및 자격 증명을 참조하십시오.
   * 참여 자격 증명.
   * ID URL.

>[!NOTE]
>
>Livefyre는 CNAME에서 직접 데이터를 받습니다.따라서 이 ID URL은 Janrain Capture의 실제 CNAME으로 확인되는 CNAMEd 레코드(별칭 URL CNAME)일 수 없습니다.

## 2단계:(선택 사항) 캡처 앱 {#section_z2s_txt_bbb}에 Livefyre 기본값 추가

Capture 앱에 저장된 사용자에게 Livefyre 기본값을 추가하면 사용자에게 이메일 알림을 보내거나 사용자가 댓글을 남긴 대화를 자동으로 팔로우할 수 있습니다.

1. [단계 1:캡처 설정](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. 다음 Livefyre 기본 필드를 추가합니다. 모든 필드는 선택 사항입니다.

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 문자열 | 팔로우하는 아티클에 대한 댓글이 있을 때 사용자에게 알립니다. 즉시, 자주 또는 절대 안 될 수 있습니다. |
| **[!UICONTROL livefyre_likes]** | 문자열 | 다른 사람이 게시물을 좋아하면 사용자에게 알립니다. 즉시, 자주 또는 절대 안 될 수 있습니다. |
| **[!UICONTROL livefyre_replies]** | 문자열 | 게시물 중 하나에 답글을 남길 때 사용자에게 알립니다. 즉시, 자주 또는 절대 안 할 수 있습니다. |
| **[!UICONTROL livefyre_moderator_comments]** | 문자열 | 누군가가 대화에서 중재하고 있다는 의견을 발표하면 사회자에게 알립니다. 즉시, 자주 또는 사용하지 않을 수 있습니다. |
| **[!UICONTROL livefyre_moderator_flags]** | 문자열 | 누군가가 대화에서 중재하고 있다는 게시물에 플래그를 지정하면 사회자에게 알립니다.즉시, 자주 또는 절대 안 될 수 있습니다. |
| **[!UICONTROL livefyre_autofollow_conversations]** | 부울 | 사용자가 게시물을 떠날 때 대화를 자동으로 팔로우하도록 합니다. true 또는 false일 수 있습니다. |

## 3단계:Janrain 통합용 AuthDelegate 개체 만들기 {#section_asv_vyt_bbb}

Livefyre.require는 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.

### 로그인 {#login}

ID/로그인 메시지가 백플레인 채널에서 브로드캐스트되면 사용자의 Livefyre 인증 토큰으로 auth.authenticate()가 호출됩니다. 여전히 AuthDelegate를 구현해야 합니다.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>window.Backplane 개체는 Livefyre 백플레인 플러그인으로 auth.plugin을 호출하기 전에 페이지에 정의해야 합니다. 백플레인 개체를 사용할 수 있는지 확인하려면 onReady 콜백에서 Livefyre 인스턴스화 코드를 호출합니다. 다른 응용 프로그램에서 후면판 개체를 사용할 수 있는 시기를 확인하려면 Jannain 담당자에게 문의하십시오.



>[!NOTE]
>
>인증 위임은 Janrain 인스턴스에 따라 달라집니다.

다음은 인증 대리인이 Janrain Capture 통합을 찾는 방법에 대한 몇 가지 예입니다.

* `errback`:인증 대리인의 로그인 메서드에 전달된 콜백
* `janrain`:Janrain 캡처 변수에 대한 참조입니다.
* `window.Backplane`:후면판 개체에 대한 참조입니다.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

### 로그아웃 {#logout}

* `finishLogout`:인증 대리인의 로그인 메서드에 전달된 콜백입니다.

* `window.Backplane`:후면판 개체에 대한 참조입니다.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

### 프로필 편집 {#editprofile}

이 링크는 사용자가 자신의 프로필 페이지를 보기 위해 방문하려는 사이트의 어느 부분이든지 링크할 수 있습니다. 이 예는 전달된 작성자 개체만 인쇄합니다.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### 프로필 {#viewprofile} 보기

프로필 편집과 같이, 현재 로그인한 사용자와 다른 사용자의 페이지에 링크해야 합니다. 이 작업은 사용자가 원하는 대로 실행할 수 있습니다. 이 예제에서는 작성자 매개 변수를 콘솔에 간단하게 기록합니다.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## 4단계:Janrain 통합을 위해 Pull을 위한 Ping과 Livefyre 동기화 {#section_ilv_bzt_bbb}

Capture 사용자 관리 시스템과 Livefyre 원격 프로필을 동기화할 수 있는 방법은 Pull용 Ping이라고 하는 일련의 단계입니다. 이 프로세스를 수행하려면 Janrain에서 유효한 액세스 토큰을 입수하고 아래 3단계에서 지정한 끝점에 해당 토큰을 전달해야 합니다.

1. Janrain에서 액세스 코드 받기

   액세스 코드를 얻으려면 필요한 자격 증명을 입력하고 user_type을 &quot;user&quot;로 지정하고 uuid를 현재 사용자의 uuid로 지정하여 업데이트합니다. 자세한 내용은 [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)을 참조하십시오.

1. 액세스 토큰에 대한 액세스 코드를 교환합니다. 1단계에서 받은 액세스 코드와 필요한 자격 증명을 제공하고 grant_type을 &quot;authorization_code&quot;로 지정합니다.

   자세한 내용은 [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)을 참조하십시오.

1. Livefyre &quot;Ping to Pull Capture&quot; 끝점을 히트하십시오.

   끝점 URL:[!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] 여기서 ***{networkName}***&#x200B;은 Livefyre가 제공하는 네트워크 이름이고 jrtoken은 2단계에서 Janrain으로부터 받은 토큰입니다.

   이 끝점을 히트하면 202 응답을 받고 Livefyre가 비동기 프로세스를 시작합니다.

## 모두 작동하는 방식 {#concept_mty_f31_2cb}

이 내장 캡처/후면판 통합을 활용하려면 캡처 앱과 Livefyre.js 통합 모두에 대해 일부 구성을 변경해야 합니다.

Janrain은 백플레인 버스를 통해 성공적인 로그인/로그아웃 메시지를 보냅니다. 이 버스에서는 Livefyre 앱이 적절하게 구성되면 수신 대기합니다. 이러한 메시지에는 앱 사용자가 로그인 또는 로그아웃한 것으로 표시하는 데 필요한 모든 정보가 포함되어 있습니다. 개발자는 브라우저의 개발자 콘솔에서 네트워크 탭을 검사하여 백플레인 버스 메시지를 볼 수 있습니다.

## 로그인 코드 예 {#section_ftt_tvp_mz}

요청:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

응답:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

빈 응답:

```
Backplane.response([]);
```

## 로그아웃 코드 예 {#section_t52_svp_mz}

요청:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

응답:

```
Backplane.finishInit("{CHANNEL}");
```

이러한 메시지가 네트워크 요청에 표시되지 않는 경우 Livefyre는 로그인/로그아웃 시도를 인식하지 못하므로 Livefyre는 사용자를 앱에 통합할 수 없습니다.
