---
description: 이 메서드는 이 네트워크 사용자의 URN을 반환합니다.
seo-description: 이 메서드는 이 네트워크 사용자의 URN을 반환합니다.
seo-title: getUrnForUser 네트워크 메서드
solution: Experience Manager
title: getUrnForUser 네트워크 메서드
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

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
