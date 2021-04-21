---
description: 만든 모든 컬렉션을 식별하는 고유한 토큰을 서버에 만듭니다.
title: CollectionMeta 토큰
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---

# CollectionMeta 토큰{#collectionmeta-token}

만든 모든 컬렉션을 식별하는 고유한 토큰을 서버에 만듭니다.

Livefyre는 제작한 모든 컬렉션에 고유한 식별자를 할당합니다. Livefyre는 제목, URL 및 다음을 비롯한 기타 매개 변수를 할당합니다.

## collectionMeta 토큰 매개 변수

| 매개 변수 | 유형 | 설명 |
|--- |--- |--- |
| networkName | 문자열(선택 사항) | Livefyre 네트워크의 이름( [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials]에서 사용 가능). 이 옵션은 라이브러리를 사용하여 collectionMeta 토큰을 만들 때 선택 사항입니다. |
| networkKey | 문자열(선택 사항) | 특정 네트워크의 비밀 키([스튜디오] > [설정] > [통합 설정] > [자격 증명]에서 사용 가능)입니다. 이 옵션은 라이브러리를 사용하여 collectionMeta 토큰을 만들 때 선택 사항입니다. |
| siteId | 문자열(선택 사항) | 사이트의 ID( [!UICONTROL Studio > Settings > Integration Settings > Credentials]에서 사용 가능). 라이브러리를 사용하여 collectionMeta 토큰을 만드는 경우 선택 사항입니다. |
| siteKey | 문자열(선택 사항) | 사이트의 비밀 키([!UICONTROL Studio > Settings > Integration Settings > Credentials]에서 사용 가능). |
| articleId | 문자열(선택 사항) | 컬렉션에 대한 고유 ID. |
| title | 문자열(선택 사항) | 컬렉션에 적용할 제목. 일반적으로 이것은 앱을 표시하는 페이지의 제목에 해당합니다. <br>예:&quot;통합이 매우 재미있습니다!&quot; <br>참고:제목의 최대 문자 길이는 255자입니다. 제목 필드는 HTML 엔티티를 지원하지 않습니다. UTF-8을 사용하여 특수 문자를 인코딩하십시오. |
| url | 문자열(선택 사항) | 이 컬렉션에 첨부하려는 기본 절대 URL. 이 URL은 Facebook 및 Twitter, 이메일 알림 및 Livefyre Studio에서 공유된 콘텐츠에서 앱으로의 링크를 만드는 데 사용됩니다. <br>참고:로컬에서 테스트하는 경우 유효한 기본 URL 도메인을 사용하십시오(예:유효한: `https://customer.com`;잘못된: `https://localhost:5995`). |
| 태그가 있는 세그먼트만 필터링할 수 있습니다 | 문자열(선택 사항) | 단일 키워드 또는 구문의 쉼표로 구분된 목록. Studio를 사용하여 태그로 컬렉션을 검색합니다.  </br>참고:태그에는 공백이 포함될 수 없습니다. UI에 공백을 표시하려면 밑줄을 사용합니다. |
| 확장 기능 | JSON(선택 사항) | 컬렉션에 전달할 JSON 형식 매개 변수 세트입니다. |

## Java {#section_orz_m4n_sz}

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

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre는 빌드하는 collectionMeta 토큰을 받고 siteId(Livefyre 제공)와 articleId(고객이 지정됨)를 결합하여 고유성을 결정합니다.
