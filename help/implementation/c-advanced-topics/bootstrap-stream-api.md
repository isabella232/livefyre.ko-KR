---
description: Livefyre 앱에서 Bootstrap 및 스트림 API를 사용합니다.
title: 계정 세부 정보 보기
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Livefyre 앱에서 Bootstrap 및 스트림 API 사용 {#bootstrap-stream-api}

## Bootstrap API {#bootstrap-api}

### 최신 50개보다 오래된 컨텐츠를 검색하려면 어떻게 합니까? {#howcontentolder}

Bootstrap은 Livefyre 앱의 모든 컨텐츠입니다. 캐시된 데이터입니다. 일반적으로 12~20분 정도 됩니다. 이 조각은 50조각 청크로 전달되며 페이지 매김되므로 50조각 이상의 컨텐츠를 검색할 수 있습니다.

[API 참조](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[요청 예](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

위의 예제 요청은 컬렉션 설정 이 포함된 `init` 페이지와 최대 50개의 최신 컨텐츠 초기 세트가 들어 있는 페이지를 로드합니다. 이전 컨텐츠를 폴링하려면 페이지 번호가 `N`인 후속 부트스트랩 페이지를 로드해야 합니다.

요청: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

예를 들어 샘플 앱에는 120개의 콘텐츠가 있습니다. 컨텐츠 &quot;1&quot;은 가장 오래된 컨텐츠이고 컨텐츠 &quot;70&quot;은 최신 컨텐츠입니다.

* `Init` 는 ~120-70개의 컨텐츠를 내림차순으로 로드합니다.  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 은 다음과 같이 최대 1~50개의 컨텐츠를 오름차순으로 로드합니다.  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` 은(는) 51~100개의 컨텐츠를 오름차순으로 로드합니다.  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` 는 ~101-120개의 컨텐츠를 오름차순으로 로드합니다.`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[Bootstrap 폴링 순서도를 보려면 여기를 클릭하십시오.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 스트림 API {#stream-api}

Stream API란?
스트림은 디자인에 의해 약 30초 동안 열려 있도록 의도된 긴 설문 조사입니다. 긴 폴링 기법에 대한 설명은 다음과 같습니다. [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

이 긴 폴링 종단점은 Livefyre 앱에 새 컨텐츠(예: 사용자가 댓글을 게시함), 컨텐츠 상태 변경(예: 사용자가 댓글을 삭제하고, 좋아요) 및 컨텐츠에 대한 조정 변경 사항(예: 중재자가 컨텐츠 조각을 승인)을 스트리밍합니다.

Stream API에 대한 요청은 30초(긴 폴링)이어야 하며 새 컨텐츠 스트림이 없을 때 30초 후에 예상되는 시간 초과여야 합니다.

API 참조: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

요청 예:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

참고: 스트림 API 응답의 `maxEventId`은 이 응답에서 업데이트 중 가장 높은 이벤트 ID입니다. 다음 스트림 API 요청의 URL을 작성할 때 이 값을 `lastEventId` 경로 매개 변수로 사용하여 이 응답의 모든 업데이트 후에 발생하는 업데이트를 가져옵니다.

아래 예제는 댓글 앱을 기반으로 합니다.

첫 번째 댓글이 먼저 게시됐다. 이어 두 번째 코멘트를 올렸다.

첫 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

응답의 `maxEventId`은(는) &quot;1520289700953369&quot;이며, 이 응답의 모든 업데이트 후에 발생하는 업데이트(즉, 두 번째 주석)를 얻기 위해 종단점을 폴링합니다.`lastEventId`

두 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

응답의 `maxEventID` &quot;1520289700953369&quot;은 다음에 업데이트할 Stream API 응답을 작성하는 데 반드시 `lastEventID` 로 사용해야 합니다.
