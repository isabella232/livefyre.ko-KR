---
description: 블로그 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여
  빌드 프로세스를 완료합니다.
seo-description: 블로그 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여
  빌드 프로세스를 완료합니다.
seo-title: Buildblogcollection 사이트 메서드
solution: Experience Manager
title: Buildblogcollection 사이트 메서드
uuid: 6 A 5 EC 6 B 9-BC 32-467 A-ABE 6-A 57 C 6 DEFE 067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Buildblogcollection 사이트 메서드{#buildblogcollection-site-method}

블로그 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| Articleid | 문자열 | 사이트 내에서 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID 입니다. |
| URL | 문자열 | 이 컬렉션에 대한 기본 절대 URL 입니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Python 예제 {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

