---
description: Sidenotes 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를
  실행하여 빌드 프로세스를 완료합니다.
seo-description: Sidenotes 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update
  () 를 실행하여 빌드 프로세스를 완료합니다.
seo-title: Buildsitenotescollection 사이트 메서드
solution: Experience Manager
title: Buildsitenotescollection 사이트 메서드
uuid: 2 BFBC 032-4 C 0 C -48 D 2-8 CE 6-02460 B 38 BD 6 C
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildsitenotescollection 사이트 메서드{#buildsitenotescollection-site-method}

Sidenotes 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| Articleid | 문자열 | 사이트 내에서 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID 입니다. |
| URL | 문자열 | 이 컬렉션에 대한 기본 절대 URL 입니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Python 예제 {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
