---
description: 이 메서드는 이 네트워크의 사용자에 대한 URN를 반환합니다.
seo-description: 이 메서드는 이 네트워크의 사용자에 대한 URN를 반환합니다.
seo-title: Geturnforuser 네트워크 메서드
solution: Experience Manager
title: Geturnforuser 네트워크 메서드
uuid: B 70 B 8 B 0 F -2 B 3 A -4 A 1 D -90 D 0-93 A 97 A 137 AD 4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Geturnforuser 네트워크 메서드{#geturnforuser-network-method}

이 메서드는 이 네트워크의 사용자에 대한 URN를 반환합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| userid | 문자열 | urn에 사용할 userid. |

## Java 예제 {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Nodejs 예제 {#section_xkd_gds_rz}

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

## Python 예제 {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby 예 {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

샘플 출력:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
