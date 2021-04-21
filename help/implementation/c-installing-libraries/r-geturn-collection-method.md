---
description: 이 메서드는 이 컬렉션에 대한 URN을 반환합니다. 이 메서드를 실행하려면 먼저 createOrUpdate()를 실행해야 합니다.
title: getUrn 컬렉션 메서드
exl-id: bea04805-8f02-4c06-9a1a-6b057de831ab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getUrn 컬렉션 메서드{#geturn-collection-method}

이 메서드는 이 컬렉션에 대한 URN을 반환합니다. 이 메서드를 실행하려면 먼저 createOrUpdate()를 실행해야 합니다.

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

## 루비의 예 {#section_enh_gds_rz}

```
collection.urn
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```
