---
description: 새 Site 객체를 반환합니다.
title: getSite Network 메서드
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite 네트워크 메서드{#getsite-network-method}

새 Site 객체를 반환합니다.
|변수|유형|설명|
|— |— |— |
|siteId|String|컬렉션이 속하는 웹 사이트 또는 응용 프로그램에 대한 Livefyre 제공 ID입니다. 예:303617.  |
|siteKey|String|siteId에 대한 Livefyre 제공 비밀 키입니다.  |

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

## 루비의 예 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
