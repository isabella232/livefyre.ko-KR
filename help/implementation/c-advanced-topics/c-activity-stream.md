---
description: Livefyre 시스템을 통해 흐르는 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 살펴볼 수 있습니다.
seo-description: Livefyre 시스템을 통해 흐르는 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 살펴볼 수 있습니다.
seo-title: 활동 스트림
solution: Experience Manager
title: 활동 스트림
uuid: F 40 deec 1-58 ab -41 c 9-aac 4-d 2 d 8 c 9192 bb 9
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 활동 스트림 {#activity-stream}

Livefyre 시스템을 통해 흐르는 사용자 생성 콘텐츠를 모니터링하고 저장하는 방법을 살펴볼 수 있습니다.

Activity Stream API를 사용하여 네트워크나 사이트의 Livefyre 시스템을 통해 생성된 사용자 생성된 데이터를 소비합니다. 예를 들면 다음과 같습니다. 이 API의 데이터를 사용하여 등급을 기반으로 검색 색인을 업데이트하거나, 활동을 기반으로 타사 시스템에서 사용자의 배지를 관리할 수 있습니다.

Activity Stream API:

사용 가능한 끝점에 대한 전체 목록은 Livefyre API 참조 섹션을 참조하십시오.

## 리소스 {#section_aql_n4l_b1b}

스테이징 환경용과 프로덕션용이라는 두 개의 끝점이 있습니다.

### 스테이징

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### 프로덕션

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### 매개 변수

* **리소스:***활동* 데이터를 요청하는 개체의 URN 문자열입니다.

* **이후:***정수* 받은 마지막 이벤트의 ID를 나타내는 64 비트 정수입니다. 이전 데이터가 없는 경우 ' 0 ' 를 지정합니다.

## URN 문자열 {#section_skl_q4l_b1b}

예:

* **URN: Livefyre:**`example.fyre.co` 에 대한 활동 `example.fyre.co`스트림입니다.
* **URN: Livefyre:**`example.fyre.co:site=54321` 네트워크 아래의 사이트 54321에 대한 활동 `example.fyre.co` 스트림.

## 토큰 정책 {#section_nwh_c5j_11b}

Activity Stream API는 인증에 OAuth 베어러 토큰을 사용합니다. 베어러 토큰은 OAuth 2.0 사양에 포함되어 있으며 공식적으로 여기에 설명되어 [](https://tools.ietf.org/html/rfc6750#section-1.2)있습니다.

토큰에는 다음과 같은 여러 항목이 포함됩니다.

* 토큰을 만든 사용자
* 토큰을 받았습니다.
* 더 이상 유효하지 않은 시간입니다.
* 작업 중인 제품
* 부여된 권한 목록입니다.

### steps

OAuth 베어러 토큰을 만드는 단계는 다음과 같습니다.

* 발급자, 대상자, 주제, 만료 및 범위를 포함하는 맵/사전을 만듭니다.
* JWT 라이브러리를 사용하여 JWT 토큰을 인코딩합니다.
* «인증: Bearer» to your HTTP request.

아래의 코드 샘플에서는 Python의 위 단계를 보여 줍니다.

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

Bearer Token Keys가 다음과 같이 정의되는 위치:

* **ISS** *(발급자)* 토큰을 생성할 권한이 있는 엔티티. Livefyre, 사이트나 네트워크일 수 있습니다. (학교에 늦게 갈 수 있는 메모는 부모입니다.)
* **AUD** *(대상)* 이 토큰을 생성한 사람. 토큰을 직접 만드는 경우 사이트 또는 네트워크입니다.
* **하위** *(제목)* 권한을 부여할 주체의 제목입니다. 예를 들어 컬렉션에서 작업하는 경우 해당 주제는 컬렉션의 식별자여야 합니다. (School from School Example, it's Yours.)
* **exp** *(만료)* 토큰이 더 이상 유효하지 않은 시점을 나타냅니다.
* **범위** *(범위)* 제목에서 부여된 권한 목록입니다. «학교를 위한 Late» 는 한 예입니다. API의 이름은 또 다른 예입니다.

## 예 {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## response {#section_gs2_stj_11b}

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

마지막 요청 이후 새 데이터를 사용한 응답:

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

* API에 대한 호출이 성공하면 HTTP 200 상태 코드가 생성됩니다. 다른 모든 상태 코드는 오류로 간주해야 합니다.
* null 이 아닌 경우 다음 요청의 `data.meta.cursor.next``since` 매개 변수로 값을 사용합니다.
* 값이 `data.meta.cursor.next` null 이면 소비할 새 데이터가 없음을 의미합니다. 새 데이터가 도착했는지 확인하려면 나중에 동일한 `since` 값으로 다시 요청해야 합니다.
* 실제로는 값이 `data.meta.cursor.next` null 이 아닌 경우 더 많은 데이터를 즉시 요청해야 합니다.
* 프로덕션 시에는 약 2 시간 분량의 최신 데이터를 이 API를 통해 사용할 수 있습니다.
* 데이터가 누락된 경우를 방지하려면 Cronjob에서 이 끝점을 자주 폴링하도록 프로세스를 설정해야 합니다. 대부분의 구현에 대해 간격이 5 분 정도면 충분합니다.
