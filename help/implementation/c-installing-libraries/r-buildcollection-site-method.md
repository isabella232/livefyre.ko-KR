---
description: 'null'
seo-description: 'null'
seo-title: buildCollection 사이트 메서드
solution: Experience Manager
title: buildCollection 사이트 메서드
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCollection 사이트 메서드{#buildcollection-site-method}

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| 유형 | CollectionType | 컬렉션의 유형입니다. |
| title | 문자열 | 컬렉션의 제목입니다. |
| articleId | 문자열 | 사이트 내 컬렉션을 식별하기 위해 선택한 고유 아티클 ID. |
| url | 문자열 | 이 컬렉션에 대한 기본 절대 URL입니다. |

## Java 예 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python 예 {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
