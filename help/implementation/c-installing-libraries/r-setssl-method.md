---
description: API 호출에 대한 SSL을 켜거나 끕니다.
seo-description: API 호출에 대한 SSL을 켜거나 끕니다.
seo-title: setSSL 네트워크 메서드
solution: Experience Manager
title: setSSL 네트워크 메서드
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

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
