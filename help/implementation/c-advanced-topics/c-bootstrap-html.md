---
description: 검색 엔진 크롤러에서 커뮤니티 콘텐츠를 사용할 수 있도록 합니다.
seo-description: 검색 엔진 크롤러에서 커뮤니티 콘텐츠를 사용할 수 있도록 합니다.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

검색 엔진 크롤러에서 커뮤니티 콘텐츠를 사용할 수 있도록 합니다.

사용 가능한 끝점의 전체 목록을 보려면 Livefyre API [참조 섹션을](https://api.livefyre.com/docs) 참조하십시오.

Livefyre 앱을 사용하려면 페이지에서 JavaScript를 실행하여 컬렉션에 대한 콘텐츠를 표시해야 합니다. 대부분의 검색 엔진 크롤러는 JavaScript를 실행할 수 없으므로 커뮤니티에서 게시한 컨텐츠를 볼 수 없습니다. Bootstrap HTML API를 사용하여 이 컨텐츠의 검색 가능한 조각을 페이지의 초기 HTTP 응답에 추가하여 컨텐츠와 키워드를 통해 검색 엔진 최적화를 향상시킬 수 있습니다.

>[!NOTE]
>
>이 API는 댓글 및 라이브 블로그 컬렉션 유형에만 사용할 수 있습니다.

## 통합

Livefyre의 Bootstrap HTML API는 페이지의 HTTP 응답에 포함될 수 있는 사용자 컨텐츠의 HTML 조각을 반환합니다. 이 응답은 JavaScript를 실행하지 않고 검색 엔진 크롤러가 읽을 수 있습니다. 페이지가 사용자의 브라우저에서 라이브되면 HTML 조각이 전체 대화형 위젯으로 대체되고 사용자는 컨텐츠를 게시할 수 있습니다.

Bootstrap HTML API를 구현하려면:

1. 아래 문서화된 Bootstrap HTML 끝점에 대한 서버 API 요청을 만듭니다.

   >[!NOTE]
   >
   >아직 존재하지 않는 대화를 위해 Bootstrap HTML을 이용하려고 하는 경우(즉, 앱을 임베드하거나 컬렉션을 제작하지 않은 경우), 200을 받게 되지만 다음과 같은 내용이 표시됩니다. `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 반환에 "404"가 포함된 컨텐츠가 없으면 문자열로 저장합니다. 나중에 사용할 수 있도록 이 응답을 캐시하여 모든 페이지 로드에서 Bootstrap HTML API를 요청하지 않을 수 있습니다.
1. 웹 페이지에 컨텐츠를 표시할 Bootstrap HTML 문자열을 삽입합니다.
1. 웹 페이지를 브라우저(또는 검색 엔진 크롤러)에 제공합니다.

## 리소스

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 매개 변수

* **networkName** Livefyre에서 네트워크 이름을 제공했습니다. 예: *labs* in `labs.fyre.co`the
* **siteId** 컬렉션의 사이트 ID입니다.
* **b64articleId** base64url 인코딩을 사용한 컬렉션의 아티클 ID

## 예

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## 응답

```
https://gist.github.com/ec5c2457322faf9cf515 
```
