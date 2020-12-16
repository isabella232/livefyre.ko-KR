---
description: Livefyre 시스템을 통해 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 알아봅니다.
seo-description: Livefyre 시스템을 통해 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 알아봅니다.
seo-title: 활동 스트림
solution: Experience Manager
title: 활동 스트림
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# 활동 스트림 {#activity-stream}

Livefyre 시스템을 통해 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 알아봅니다.

활동 스트림 API를 사용하여 네트워크 또는 사이트에서 Livefyre 시스템을 통해 사용자 생성 데이터를 사용합니다. 예:이 API의 데이터를 사용하여 등급을 기준으로 검색 색인을 업데이트하거나 자신의 활동에 따라 제3자 시스템의 사용자 배지를 관리할 수 있습니다.

활동 스트림 API:

사용 가능한 끝점의 전체 목록은 Livefyre API 참조 섹션을 참조하십시오.

## 리소스 {#section_aql_n4l_b1b}

스테이징 환경용 끝점과 프로덕션 끝점이 두 개 있습니다.

### 스테이징

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### 프로덕션

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### 매개 변수

* **resource:** ** string활동 데이터를 요청하는 개체의 URN입니다.

* **since:** ** integer마지막으로 받은 이벤트의 ID를 나타내는 64비트 정수입니다. 이전 데이터가 없는 경우 &#39;0&#39;을 지정합니다.

## URN 문자열 {#section_skl_q4l_b1b}

예:

* **urn:livefyre:** `example.fyre.co` 활동  `example.fyre.co`스트림입니다.
* **urn:livefyre:** `example.fyre.co:site=54321` 네트워크의 사이트 54321에 대한 활동  `example.fyre.co` 스트림입니다.

## 토큰 정책 {#section_nwh_c5j_11b}

활동 스트림 API는 인증에 OAuth 전달자 토큰을 사용합니다. 베어러 토큰은 OAuth 2.0 사양의 일부이며 공식적으로 [여기](https://tools.ietf.org/html/rfc6750#section-1.2)에 설명되어 있습니다.

토큰에는 다음과 같은 몇 가지 사항이 포함됩니다.

* 토큰을 만든 사람입니다.
* 토큰을 받은 사람.
* 더 이상 유효하지 않은 시간입니다.
* 우리가 하고 있는 일
* 부여된 권한 목록입니다.

### 단계

OAuth 전달자 토큰을 만드는 단계는 다음과 같습니다.

* 발급자, 대상, 대상, 만료 및 범위가 포함된 지도/사전을 만듭니다.
* JWT 라이브러리를 암호와 함께 사용하여 JWT 토큰을 인코딩합니다.
* &quot;인증:HTTP 요청에 전달&quot;을 참조하십시오.

아래 코드 샘플에서는 위의 Python 단계를 보여 줍니다.

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

베어러 토큰 키가 다음과 같이 정의된 경우:

* **is** *(발급자)* 토큰을 생성할 권한이 있는 개체 사이트 또는 네트워크인 Livefyre일 수 있습니다. (학교에 지각하기 위한 메모는 너의 부모이다.)
* **aud** *(대상)* 이 토큰이 생성된 사람입니다. 직접 토큰을 만드는 경우 사이트 또는 네트워크입니다.
* **sub** *(Subject)* 권한을 부여할 제목입니다. 예를 들어 컬렉션에서 작업하는 경우 주체가 컬렉션의 식별자여야 합니다. (학교 예제의 메모에는, 바로 자신입니다.)
* **exp** *(만료)* 토큰이 더 이상 유효하지 않은 시간입니다.
* **scope** *(범위)* 제목에 부여된 권한 목록입니다. &#39;학교에 지각한다&#39;는 말이 그 예다. API의 이름은 다른 예입니다.

## 예 {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## 응답 {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

마지막 요청 이후 새 데이터가 있는 응답:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## 참고 {#section_hj3_crj_11b}

* API를 성공적으로 호출하면 HTTP 200 상태 코드가 생성됩니다. 다른 모든 상태 코드는 오류로 간주됩니다.
* null이 아닌 경우 다음 요청의 `since` 매개 변수로 `data.meta.cursor.next`의 값을 사용합니다.
* `data.meta.cursor.next`의 값이 null이면 사용할 새 데이터가 없음을 의미합니다. 나중에 동일한 `since` 값으로 다시 요청하여 새 데이터가 도착했는지 확인해야 합니다.
* 실제로 `data.meta.cursor.next` 값이 null이 아닌 경우 추가 데이터를 즉시 요청해야 합니다.
* 제작 중인 이 API를 통해 약 2시간 분량의 최근 데이터를 사용할 수 있습니다.
* 누락된 데이터를 방지하기 위해 cronjob에서 이 끝점을 자주 폴링하도록 프로세스를 설정해야 합니다. 5분 간격은 대부분의 구현에 완벽하게 적절해야 합니다.
