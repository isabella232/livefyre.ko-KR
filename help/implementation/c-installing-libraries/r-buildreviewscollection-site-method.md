---
description: 검토 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드
  프로세스를 완료합니다.
seo-description: 검토 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여
  빌드 프로세스를 완료합니다.
seo-title: Buildreviewscollection 사이트 메서드
solution: Experience Manager
title: Buildreviewscollection 사이트 메서드
uuid: 88 AF 4 C 68-57 DE -4 AE 9-9394-550 C 94 EDE 48 F
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildreviewscollection 사이트 메서드{#buildreviewscollection-site-method}

검토 유형으로 인스턴스화된 컬렉션 개체를 반환합니다. 컬렉션 개체에서 create_ or_ update () 를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| Articleid | 문자열 | 사이트 내에서 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID 입니다. |
| URL | 문자열 | 이 컬렉션에 대한 기본 절대 URL 입니다. |


## Java 예제 {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Python 예제 {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

