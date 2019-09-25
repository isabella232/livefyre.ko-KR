---
description: 채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.
seo-description: 채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.
seo-title: buildChatCollection 사이트 메서드
solution: Experience Manager
title: buildChatCollection 사이트 메서드
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# buildChatCollection 사이트 메서드{#buildchatcollection-site-method}

채팅 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| articleId | 문자열 | 사이트 내 컬렉션을 식별하기 위해 선택한 고유 아티클 ID. |
| url | 문자열 | 이 컬렉션에 대한 기본 절대 URL입니다. |

## Java 예 {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python 예 {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
