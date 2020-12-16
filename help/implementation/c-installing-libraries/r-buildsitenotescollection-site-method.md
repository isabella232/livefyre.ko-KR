---
description: 사이드노트 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.
seo-description: 사이드노트 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.
seo-title: buildSitenotesCollection 사이트 메서드
solution: Experience Manager
title: buildSitenotesCollection 사이트 메서드
uuid: 2bfbc032-4c0c-48d2-8ce6-02460b38bd6c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildSitenotesCollection 사이트 메서드{#buildsitenotescollection-site-method}

사이드노트 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| articleId | 문자열 | 사이트 내 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID. |
| url | 문자열 | 이 컬렉션에 대한 기본 절대 URL. |

## Java 예 {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Python 예 {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## 루비의 예 {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
