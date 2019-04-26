---
description: 제작한 모든 컬렉션을 식별하는 고유한 토큰을 서버에 만듭니다.
seo-description: 제작한 모든 컬렉션을 식별하는 고유한 토큰을 서버에 만듭니다.
seo-title: Collectionmeta Token
solution: Experience Manager
title: Collectionmeta Token
uuid: D 5 DB 0 B 0 F -2807-4392-874 A -94 AC 3 C 1 E 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Collectionmeta Token{#collectionmeta-token}

제작한 모든 컬렉션을 식별하는 고유한 토큰을 서버에 만듭니다.

Livefyre는 사용자가 만든 모든 컬렉션에 고유한 식별자를 할당합니다. Livefyre는 다음을 포함한 제목, URL 및 기타 매개 변수를 지정합니다.

## Collectionmeta 토큰 매개 변수

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| Networkname | 문자열 (선택 사항) | Livefyre 네트워크 이름 ({! Uicontrol Studio > 설정 > 통합 설정 > 자격 증명을 참조하십시오. 이는 라이브러리를 사용하여 Collectionmeta 토큰을 만들 때 선택 사항입니다. |
| Networkkey | 문자열 (선택 사항) | 특정 네트워크의 비밀 키 ([Studio] > [설정] > [통합 설정] > [자격 증명] 에서 사용 가능) 이는 라이브러리를 사용하여 Collectionmeta 토큰을 만들 때 선택 사항입니다. |
| Siteid | 문자열 (선택 사항) | 사이트의 ID (에서 [!UICONTROL Studio > Settings > Integration Settings > Credentials] 사용 가능) 라이브러리를 사용하여 Collectionmeta 토큰을 만들 때 선택 사항입니다. |
| sitekey | 문자열 (선택 사항) | 사이트의 비밀 키 ({! Uicontrol Studio > 설정 > 통합 설정 > 자격 증명을 참조하십시오. |
| Articleid | 문자열 (선택 사항) | 컬렉션의 고유 ID 입니다. |
| title | 문자열 (선택 사항) | 컬렉션에 적용할 제목입니다. 일반적으로 이것은 앱을 표시하는 페이지의 제목과 일치합니다. <br>예를 들면 다음과 같습니다. «통합 기능은 정말 재미있습니다! » <br>참고: 제목의 최대 문자 길이는 255 자입니다. 제목 필드는 HTML 개체를 지원하지 않습니다. UTF -8를 사용하여 특수 문자를 인코딩하십시오. |
| URL | 문자열 (선택 사항) | 이 컬렉션에 첨부할 기본 절대 URL 입니다. 이 URL는 Facebook 및 Twitter, 이메일 알림 및 Livefyre 스튜디오에서 공유한 콘텐츠에서 다시 앱을 연결하는 데 사용됩니다. <br>참고: 로컬로 테스트하는 경우 유효한 기본 URL 도메인 (예: 유효: `https://customer.com`; 유효하지 않음: `https://localhost:5995`). |
| 태그 | 문자열 (선택 사항) | 쉼표로 구분된 단일 키워드 또는 구문의 목록입니다. 태그를 사용하여 태그를 태그로 검색 </br>참고: 태그는 공백을 포함할 수 없습니다. 공간이 UI에 표시되도록 하려면 밑줄을 사용합니다. |
| 익스텐션 | JSON (선택 사항) | 컬렉션으로 전달할 JSON 형식의 params 집합. |

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

## Nodejs {#section_kpk_44n_sz}

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

>[!NOTE] {importance = "high"}
>
>Livefyre는 사용자가 빌드하는 collectionmeta 토큰을 받고 siteid (livefyre) 와 articleid (고객 지정) 를 결합하여 고유성을 판단합니다.

