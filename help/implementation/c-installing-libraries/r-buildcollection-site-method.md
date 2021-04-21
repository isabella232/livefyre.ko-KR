---
title: buildCollection 사이트 메서드
description: buildCollection 사이트 메서드
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# buildCollection 사이트 메서드{#buildcollection-site-method}

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| 유형 | CollectionType | 컬렉션의 유형입니다. |
| title | 문자열 | 컬렉션의 제목입니다. |
| articleId | 문자열 | 사이트 내 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID. |
| url | 문자열 | 이 컬렉션에 대한 기본 절대 URL. |

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

## 루비의 예 {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
