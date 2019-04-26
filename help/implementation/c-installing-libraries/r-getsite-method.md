---
description: 새 사이트 개체를 반환합니다.
seo-description: 새 사이트 개체를 반환합니다.
seo-title: Getsite 네트워크 메서드
solution: Experience Manager
title: Getsite 네트워크 메서드
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Getsite 네트워크 메서드{#getsite-network-method}

새 사이트 개체를 반환합니다.
| 변수 | 유형 | 설명|
|— |— |— |
| Siteid | 문자열 | Livefyre 컬렉션이 속한 웹 사이트 또는 응용 프로그램에 대한 ID 입니다. 예를 들면 다음과 같습니다. 303617. |
| sitekey | 문자열 | Siteid에 대한 Livefyre 비밀 키. |

## Java 예제 {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python 예제 {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby 예 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

