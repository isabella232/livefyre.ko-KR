---
description: null
seo-description: null
seo-title: Buildcollection 사이트 메서드
solution: Experience Manager
title: Buildcollection 사이트 메서드
uuid: 52 ABC 42 A -9506-4492-B 219-F 2 E 05 EB 79 C 5 F
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Buildcollection 사이트 메서드{#buildcollection-site-method}

| 변수 | type | 설명 |
|--- |--- |--- |
| type | Collectiontype | 컬렉션의 유형입니다. |
| title | 문자열 | 컬렉션의 제목입니다. |
| Articleid | 문자열 | 사이트 내에서 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID 입니다. |
| URL | 문자열 | 이 컬렉션에 대한 기본 절대 URL 입니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python 예제 {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
