---
description: Livefyre 앱과 함께 Bootstrap 및 스트림 API 사용
seo-description: Livefyre 앱과 함께 Bootstrap 및 스트림 API 사용
seo-title: Livefyre 앱과 함께 Bootstrap 및 스트림 API 사용
solution: Experience Manager
title: 계정 세부 사항 보기
uuid: BACE 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre 앱과 함께 Bootstrap 및 스트림 API 사용 {#bootstrap-stream-api}

## Bootstrap API {#bootstrap-api}

### 최신 50 개 조각보다 오래된 컨텐츠를 검색하려면 어떻게 해야 합니까? {#howcontentolder}

Bootstrap는 Livefyre 앱의 모든 컨텐츠입니다. 일반적으로 12-20 분 오래된 캐시된 데이터입니다. 50 개 조각으로 배달되고 페이지로 분할되므로 50 개 이상의 컨텐츠를 검색할 수 있습니다.

[API 참조](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[요청 예](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

위의 예제 요청은 컬렉션 설정이 포함된 `init` 페이지와 최대 50 개의 최신 컨텐츠 세트를 로드합니다. 이전 콘텐츠를 폴링하려면 페이지 번호가 `N` 있는 다음 Bootstrap 페이지를 로드해야 합니다.

요청: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

예를 들어 샘플 앱에는 120 개의 컨텐츠가 있습니다. 콘텐츠 "1" 는 가장 오래된 컨텐츠이고 컨텐츠 "70" 는 최신 컨텐츠입니다.

* `Init` ~ 120-70 개의 컨텐츠를 내림차순으로 로드합니다. [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` ~ 1-50 개의 컨텐츠를 오름차순으로 로드합니다. [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` ~ 51 ~ 100 개의 컨텐츠를 오름차순으로 로드합니다. [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` ~ 101 ~ 120 개의 콘텐츠를 오름차순으로 로드합니다.[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Bootstrap 투표 흐름도를 보려면 여기를 클릭하십시오.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 스트림 API {#stream-api}

스트림 API 란 무엇입니까?
Stream is a long poll which by design is intended for stay for approximately 30 seconds. 긴 투표 기술에 대한 설명은 다음 내용을 참조하십시오. [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

이 긴 폴링 끝점은 새 컨텐츠를 스트리밍합니다 (예: 사용자가 댓글을 게시한 경우). 컨텐츠 상태 변경 (예: 사용자가 댓글, 좋아요 삭제) 및 조정 변경 내용 (예: 중재자가 컨텐츠 일부를 승인함) 이 Livefyre 앱으로 변경됩니다.

API에 대한 요청은 새 컨텐츠가 스트리밍되지 않을 때 30 초 후 예상 시간 초과가 있는 ~ 30 초 (긴 폴링) 여야 합니다.

API 참조: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

예제 요청:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

참고: 스트림 API `maxEventId` 응답에서 이 응답의 가장 높은 이벤트 ID 입니다. 다음 스트림 API 요청의 URL를 빌드할 때 `lastEventId` 이 값을 경로 매개 변수로 사용하여 이 응답의 모든 업데이트 후에 발생하는 업데이트를 가져옵니다.

아래 예제는 댓글 앱을 기반으로 합니다.

댓글 "첫 번째 댓글" 이 먼저 게시되었습니다. " 두 번째 댓글 "이 다음에 게시되었습니다.

첫 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

In `maxEventId` the response is "1520289700953369" which will be used as `lastEventId` to be used as to get updates to get updates (i. e. 두 번째 댓글) 이 이 응답의 모든 업데이트 이후에 발생합니다.

두 번째 주석 스트림 API 응답:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

응답의 `maxEventID` "1520289700953369" 는 다음 업데이트에 대한 스트림 API 응답을 빌드하는 `lastEventID` 데 사용해야 합니다.