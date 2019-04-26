---
description: API 호출에 대한 SSL 이 켜거나 꺼지도록 설정합니다.
seo-description: API 호출에 대한 SSL 이 켜거나 꺼지도록 설정합니다.
seo-title: Setssl 네트워크 메서드
solution: Experience Manager
title: Setssl 네트워크 메서드
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Setssl 네트워크 메서드{#setssl-network-method}

API 호출에 대한 SSL 이 켜거나 꺼지도록 설정합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| SSL | Boolean | 기본값은 true 입니다. SSL를 원하는 경우 false로 설정합니다. <br><ul><li>true - SSL 설정 </li><li>False - SSL 끄기</li></ul> |

## Java 예제 {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python 예제 {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby 예 {#section_enh_gds_rz}

```
network.ssl = false 
```
