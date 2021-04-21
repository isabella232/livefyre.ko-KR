---
description: 이 메서드는 이 네트워크 사용자의 URN을 반환합니다.
title: getUrnForUser 네트워크 메서드
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# getUrnForUser 네트워크 메서드{#geturnforuser-network-method}

이 메서드는 이 네트워크 사용자의 URN을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| userId | 문자열 | URN에 사용할 userId입니다. |

## Java 예 {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python 예 {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## 루비의 예 {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
