---
description: Livefyre 앱에 Bootstrap 및 스트림 API를 사용할 수 있습니다.
seo-description: Livefyre 앱에 Bootstrap 및 스트림 API를 사용할 수 있습니다.
seo-title: Livefyre 앱에 Bootstrap 및 스트림 API 사용
solution: Experience Manager
title: 계정 세부 사항 보기
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# Livefyre 앱 {#bootstrap-stream-api}에 Bootstrap 및 스트림 API 사용

## Bootstrap API {#bootstrap-api}

### 최신 50개 조각보다 오래된 컨텐츠를 어떻게 검색할 수 있습니까?{#howcontentolder}

Bootstrap은 Livefyre 앱의 모든 콘텐츠입니다. 캐시된 데이터입니다(일반적으로 12-20분). 50개 이상의 조각으로 배달되며 페이지를 지정하여 50개 이상의 콘텐츠를 검색할 수 있습니다.

[API 참조](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[요청 예](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

위의 예제 요청은 컬렉션 설정과 ~50개의 최신 컨텐츠 중 유일하게 초기 세트가 포함된 `init` 페이지를 로드합니다. 이전 컨텐츠를 폴링하려면 페이지 번호가 `N`인 후속 부트스트랩 페이지를 로드해야 합니다.

요청: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

예를 들어 샘플 앱에는 120개의 콘텐츠가 있습니다. 컨텐츠 &quot;1&quot;은 가장 오래된 컨텐츠이며 컨텐츠 &quot;70&quot;은 최신 컨텐츠입니다.

* `Init` ~120-70개의 콘텐트를 내림차순으로 로드합니다. [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 콘텐츠의 오름차순 로드: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` 컨텐츠가 오름차순으로 최대 51-100개 로드됩니다. [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` ~101-120개의 콘텐트를 오름차순으로 로드합니다. [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Bootstrap 투표 흐름도를 보려면 여기를 클릭하십시오.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 스트림 API {#stream-api}

Stream API 소개
스트림은 디자인별로 약 30초 동안 열린 상태를 유지하려는 긴 설문 조사입니다. 긴 투표 기법에 대한 설명은 다음 링크를 참조하십시오.[https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

이 긴 폴링 끝점은 Livefyre 앱에 대한 새 컨텐츠(예: 사용자 게시물), 컨텐츠 상태 변경(예: 사용자 댓글 삭제, 좋아요) 및 컨텐츠 중재 변경(예: 컨텐츠 조각 중재자 승인)을 스트리밍합니다.

스트림 API에 대한 요청은 새로운 컨텐츠 스트림이 없는 경우 30초 후 예상되는 시간 초과와 함께 ~30초(긴 폴링)이어야 합니다.

API 참조:[https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

요청 예:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

참고:스트림 API 응답의 `maxEventId`은 이 응답의 업데이트 중 가장 높은 이벤트 ID입니다. 이 응답의 모든 업데이트 후에 발생하는 업데이트를 얻으려면 다음 스트림 API 요청의 URL을 작성할 때 이 값을 `lastEventId` 경로 매개 변수로 사용하십시오.

아래 예는 댓글 앱을 기반으로 합니다.

첫 번째 댓글부터 먼저 올렸다. &quot;두 번째 의견&quot;이 그 뒤에 게시되었다.

첫 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

응답의 `maxEventId`은 이 응답의 모든 업데이트 후에 발생하는 업데이트(즉, 두 번째 주석)를 얻기 위해 종단점을 폴링하는 데 사용되는 &quot;1520289700953369&quot;입니다.`lastEventId`

두 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

응답의 `maxEventID` &quot;1520289700953369&quot;은 다시 `lastEventID`로 사용하여 다음 업데이트에 대한 스트림 API 응답을 빌드해야 합니다.