---
description: 채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드
  프로세스를 완료합니다.
seo-description: 채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여
  빌드 프로세스를 완료합니다.
seo-title: Buildchatcollection 사이트 메서드
solution: Experience Manager
title: Buildchatcollection 사이트 메서드
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# Buildchatcollection 사이트 메서드{#buildchatcollection-site-method}

채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| Articleid | 문자열 | 사이트 내에서 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID 입니다. |
| URL | 문자열 | 이 컬렉션에 대한 기본 절대 URL 입니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python 예제 {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
