---
description: Janrain Capture 및 Backplane를 사용하는 고객은 SSO (Single Sign On) 에 Livefyre
  인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.
seo-description: Janrain Capture 및 Backplane를 사용하는 고객은 SSO (Single Sign On) 에 Livefyre
  인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776 e 9626-DB 04-4 c 34-ADFE -681 A 71 B 552 C 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Janrain Capture 및 Backplane를 사용하는 고객은 SSO (Single Sign On) 에 Livefyre 인증을 사용할 수 있으므로 사용자가 사이트에 로그인할 때 Livefyre 앱을 즉시 이용할 수 있습니다.

이 내장된 캡처/백플레인 통합을 활용하려면 Capture 앱 및 Livefyre. js 통합 모두에 대한 구성을 변경해야 합니다.

>[!NOTE]
>
>Janrain Capture를 사용하지 않는 경우 이 섹션을 건너뜁니다.

자세한 내용은 [Janrain의 백플레인 설명서를](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)참조하십시오.

1. [캡처 설정](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (선택 사항) [Livefyre를 Capture 앱에 추가합니다](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Authdelegate 객체를 만듭니다.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [풀링을 위해 Ping와 Livefyre를 동기화할 수 있습니다.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 1 단계: 캡처 설정 {#section_r2f_kxt_bbb}

Livefyre는 Janrain Capture 앱에서 특정 자격 증명을 필요로 합니다.

1. Janrain Capture 앱을 설치합니다.
1. Livefyre에 대한 다음 정보를 수집합니다.

   * Janrain Capture 인스턴스에 액세스할 수 있습니다.
   * Janrain Engage Dashboard 이용
   * 캡처 설정 및 자격 증명.
   * 참여 자격 증명
   * ID URL.

>[!NOTE]
>
>Livefyre는 CNAME 으로부터 직접 데이터를 수신합니다. 따라서 이 ID URL는 Janrain 캡처의 실제 CNAME로 확인되는 CNAMED 레코드 (별칭 URL CNAME) 일 수 없습니다.

## 2 단계: (선택 사항) Livefyre를 Capture 앱에 추가 {#section_z2s_txt_bbb}

Livefyre를 Capture 앱에 저장된 사용자에게 추가하면 사용자에게 이메일 알림을 보내거나 사용자가 댓글을 달 수 있는 대화를 자동으로 팔로우할 수 있습니다.

1. 1 [단계 완료: 캡처](#c_janrain_capture_backplane/section_r2f_kxt_bbb)설정
1. 아래의 Livefyre 기본 필드를 추가합니다. 모든 필드는 선택 사항입니다.

| 매개 변수 | type | 설명 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 문자열 | 사용자가 팔로우하는 아티클에 댓글을 달 때 사용자에게 알립니다. 즉시, 종종 또는 절대 안 될 수 있습니다. |
| **[!UICONTROL livefyre_likes]** | 문자열 | 사용자가 게시물 중 하나를 좋아하면 사용자에게 알립니다. 즉시, 종종 또는 절대 안 될 수 있습니다. |
| **[!UICONTROL livefyre_replies]** | 문자열 | 사용자가 게시물 중 하나에 답글을 달 때 사용자에게 알립니다. 즉시, 종종 또는 절대 할 수 없습니다. |
| **[!UICONTROL livefyre_moderator_comments]** | 문자열 | 중재자가 중재하는 대화에 댓글을 달 때 중재자에게 알립니다. 즉시, 또는 그렇지 않을 수 있습니다. |
| **[!UICONTROL livefyre_moderator_flags]** | 문자열 | 중재자가 중재하는 대화의 게시물에 플래그를 지정할 때 중재자에게 알립니다. 즉시, 종종 또는 절대 할 수 없습니다. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolean | 사용자가 게시물을 떠날 때 대화를 자동으로 수행합니다. true 또는 false 일 수 있습니다. |

## 3 단계: Janrain 통합을 위한 authdelegate 개체 빌드 {#section_asv_vyt_bbb}

Livefyre. require는 Auth가 Janrain 백플레인 버스를 수신할 수 있도록 하는 플러그인을 제공합니다.

### login {#login}

백플레인 채널에서 ID/로그인 메시지가 브로드캐스트되면 사용자의 Livefyre 인증 토큰을 통해 auth. authenticate () 가 호출됩니다. 여전히 Authdelegate를 구현해야 합니다.

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
>window. backplane 개체는 Livefyre Backplane 플러그인과 함께 auth. plugin를 호출하기 전에 페이지에서 정의해야 합니다. 백플레인 개체가 사용 가능한지 확인하려면 Onready 콜백에서 Livefyre 인스턴스화 코드를 호출합니다. 다른 애플리케이션이 백플레인 개체를 사용할 수 있는 시기를 결정하려면 Janrain 담당자에게 문의하십시오.



>[!NOTE]
>
>인증 위임은 Janrain 인스턴스에 따라 다릅니다.

다음은 인증 위임자가 Janrain Capture 통합을 찾는 방법의 몇 가지 예입니다.

* `errback`: 인증 대리인의 로그인 메서드에 전달된 콜백
* `janrain`: Janrain Capture 변수에 대한 참조입니다.
* `window.Backplane`: 백플레인 객체에 대한 참조입니다.

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

* `finishLogout`: 인증 대리인의 로그인 메서드에 전달된 콜백.

* `window.Backplane`: 백플레인 객체에 대한 참조입니다.

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

사용자가 방문하려는 사이트의 모든 부분으로 링크하여 자신의 프로필 페이지를 볼 수 있습니다. 이 예제는 전달된 작성자 개체를 출력합니다.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### 프로필 보기 {#viewprofile}

프로필 편집처럼, 이 작업은 현재 로그인한 사용자와 다른 사용자의 페이지로 링크해야 합니다. 그러나 이 방법은 제대로 구현될 수 있습니다. 이 예에서는 author 매개 변수를 콘솔에 기록합니다.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## 4 단계: Janrain 통합을 위한 Ping를 통해 Livefyre와 동기화 {#section_ilv_bzt_bbb}

Capture 사용자 관리 시스템과 동기화된 Livefyre 원격 프로파일은 풀다운에 대해 Ping 이라고 하는 일련의 단계를 포함합니다. 이 프로세스에서는 Janrain에서 유효한 액세스 토큰을 가져온 다음, 아래 3 단계에서 지정된 종단점에 해당 토큰을 전달해야 합니다.

1. Janrain의 액세스 코드를 입수합니다.

   액세스 코드를 받으려면 필요한 자격 증명을 제공하고 user_ type를 "user" 로 지정한 다음 현재 사용자의 UUID 로서 UUID를 업데이트합니다. 자세한 내용은 [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)를 참조하십시오.

1. 액세스 토큰을 위한 액세스 코드를 트레이드합니다. 필요한 자격 증명을 제공하고 1 단계에서 받은 액세스 코드를 입력한 다음 grant_ type를 «authorization_ code» 로 지정합니다.

   자세한 내용은 [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)를 참조하십시오.

1. Livefyre "Ping to Pull Capture" 끝점을 누릅니다.

   종단점 URL: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] 여기서 ***{networkname}*** 는 Livefyre가 제공하는 네트워크 이름이고, jrtoken는 2 단계에서 Janrain 으로부터 받은 토큰입니다.

   이 엔드포인트를 히트하면 202 개의 응답이 수신되고 Livefyre가 비동기 프로세스를 시작합니다.

## 모든 작업 방식 {#concept_mty_f31_2cb}

내장된 캡처/백플레인 통합을 활용하려면 Capture 앱 및 Livefyre. js 통합 기능을 모두 변경해야 합니다.

Janrain는 백플레인 버스를 통해 성공적인 로그인/로그아웃 메시지를 전송합니다. 이 버스는 Livefyre 앱이 제대로 구성되어 있을 때 이를 수행합니다. 이러한 메시지에는 앱 사용자를 로그인하거나 로그아웃한 것으로 표시하는 데 필요한 모든 정보가 포함되어 있습니다. 개발자는 브라우저의 개발자 콘솔에서 네트워크 탭을 검사하여 백플레인 버스 메시지를 볼 수 있습니다.

## 로그인 코드 예 {#section_ftt_tvp_mz}

요청:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

답변:

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

답변:

```
Backplane.finishInit("{CHANNEL}");
```

이러한 메시지가 네트워크 요청에 나타나지 않을 경우 Livefyre는 로그인/로그아웃 시도를 인식하지 못해 Livefyre가 사용자를 앱에 통합할 수 없게 됩니다.
