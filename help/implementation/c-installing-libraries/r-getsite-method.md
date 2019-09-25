---
description: 새 사이트 개체를 반환합니다.
seo-description: 새 사이트 개체를 반환합니다.
seo-title: getSite 네트워크 메서드
solution: Experience Manager
title: getSite 네트워크 메서드
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getSite 네트워크 메서드{#getsite-network-method}

새 사이트 개체를 반환합니다.
|변수|유형|설명||—|—|—||siteId|String|컬렉션이 속한 웹 사이트 또는 응용 프로그램에 대한 Livefyre 제공 ID입니다. 예:303617.  ||siteKey|String|siteId에 대한 Livefyre 제공 암호 키  |

## Java 예 {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python 예 {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby 예 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

