---
description: 이 메서드는 이 컬렉션에 대한 URN을 반환합니다. 이 메서드를 실행하기 전에 createOrUpdate()를 실행해야 합니다.
seo-description: 이 메서드는 이 컬렉션에 대한 URN을 반환합니다. 이 메서드를 실행하기 전에 createOrUpdate()를 실행해야 합니다.
seo-title: getUrn 컬렉션 메서드
solution: Experience Manager
title: getUrn 컬렉션 메서드
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrn 컬렉션 메서드{#geturn-collection-method}

이 메서드는 이 컬렉션에 대한 URN을 반환합니다. 이 메서드를 실행하기 전에 createOrUpdate()를 실행해야 합니다.

## Java 예 {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

샘플 출력:

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python 예 {#section_dwg_gds_rz}

```
collection.urn() 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby 예 {#section_enh_gds_rz}

```
collection.urn
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

