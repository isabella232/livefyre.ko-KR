---
description: 커뮤니티 콘텐츠를 검색 엔진 크롤러에 제공할 수 있습니다.
seo-description: 커뮤니티 콘텐츠를 검색 엔진 크롤러에 제공할 수 있습니다.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137 E 4382-4 E 7 B -4124-9 D 35-1 D 872 A 497 BC 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

커뮤니티 콘텐츠를 검색 엔진 크롤러에 제공할 수 있습니다.

사용 가능한 끝점에 대한 전체 목록은 Livefyre [API 참조](https://api.livefyre.com/docs) 섹션을 참조하십시오.

Livefyre 앱을 사용하려면 페이지에서 Javascript를 실행하여 컬렉션에 대한 콘텐츠를 표시해야 합니다. 대부분의 검색 엔진 크롤러는 JavaScript를 실행할 수 없으므로 커뮤니티 게시물에 대한 컨텐츠를 볼 수 없습니다. Bootstrap HTML API를 사용하여 이 컨텐츠의 검색 가능한 조각을 페이지의 초기 HTTP 응답에 추가하면 컨텐츠와 키워드가 검색 엔진 최적화를 개선할 수 있습니다.

>[!NOTE]
>
>이 API는 댓글 및 라이브 블로그 컬렉션 유형에만 사용할 수 있습니다.

## 통합

Livefyre의 Bootstrap HTML API는 페이지의 HTTP 응답에 포함될 수 있는 사용자 컨텐츠의 HTML 조각을 반환합니다. 이 응답은 JavaScript를 실행하지 않고 검색 엔진 크롤러에서 읽을 수 있습니다. 페이지가 사용자의 브라우저에서 라이브되면 HTML 조각이 완전한 대화형 위젯으로 교체되고 사용자가 컨텐츠를 게시할 수 있습니다.

Bootstrap HTML API를 구현하려면:

1. 아래 문서화된 Bootstrap HTML 종단에 서버를 서버 API 요청으로 만드십시오.

   >[!NOTE]
   >
   >아직 존재하지 않는 대화를 위해 Bootstrap HTML를 가져오려고 하는 경우 (즉, 앱을 내장하거나 컬렉션을 만들지 않은 경우), 200 개가 수신되지만 다음과 같은 컨텐츠가 표시됩니다. `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 반환에 «404» 가 포함된 컨텐츠가 포함되어 있지 않으면 문자열을 문자열에 저장합니다. 나중에 사용하도록 이 응답을 캐시하면 모든 페이지의 부트스트랩 HTML API 요청하지 않아도 됩니다.
1. Bootstrap HTML 문자열을 콘텐츠가 표시되기를 원하는 웹 페이지에 삽입합니다.
1. 브라우저 (또는 검색 엔진 크롤러) 에 웹 페이지를 제공할 수 있습니다.

## 리소스

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 매개 변수

* **네트워크livefyre** 네트워크 이름을 입력합니다. 예를 들면 다음과 같습니다. *Labs* `labs.fyre.co`의
* **Siteid** 컬렉션의 사이트 ID 입니다.
* **b 64 articleid** Base 64 URL 인코딩을 사용하는 컬렉션의 아티클 ID 입니다.

## 예

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## response

```
https://gist.github.com/ec5c2457322faf9cf515 
```
