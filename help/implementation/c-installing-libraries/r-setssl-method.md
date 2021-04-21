---
description: API 호출에 대한 SSL을 켜거나 끕니다.
title: setSSL 네트워크 메서드
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL 네트워크 메서드{#setssl-network-method}

API 호출에 대한 SSL을 켜거나 끕니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| ssl | 부울 | 기본값은 true입니다. SSL을 켜려면 false를 반환합니다.<br><ul><li>True - SSL on </li><li>False - SSL 끄기</li></ul> |

## Java 예 {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python 예 {#section_dwg_gds_rz}

```
network.ssl = False 
```

## 루비의 예 {#section_enh_gds_rz}

```
network.ssl = false 
```
