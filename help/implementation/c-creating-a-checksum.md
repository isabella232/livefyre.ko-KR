---
description: Livefyre 라이브러리를 사용하여 체크섬을 만듭니다.
seo-description: Livefyre 라이브러리를 사용하여 체크섬을 만듭니다.
seo-title: 체크포인트 만들기
solution: Experience Manager
title: 체크포인트 만들기
uuid: 2 dddedaa -7 a 6 d -434 a -8 db 8-dc 179935 f 810
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 체크포인트 만들기 {#creating-a-checksum}

Livefyre 라이브러리를 사용하여 체크섬을 만듭니다.

## Java {#section_pfr_lqj_tz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## Nodejs {#section_hnx_jqj_tz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken();
```

## PHP {#section_kmt_3qj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken(); 
```

## Python {#section_y55_gqj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_a3y_ypj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```