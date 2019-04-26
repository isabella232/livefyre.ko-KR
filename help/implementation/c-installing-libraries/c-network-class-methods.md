---
description: 네트워크 개체를 만듭니다.
seo-description: 네트워크 개체를 만듭니다.
seo-title: 네트워크 클래스 메서드
solution: Experience Manager
title: 네트워크 클래스 메서드
uuid: 4130 beda-dd 09-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 네트워크 클래스 메서드{#network-class-methods}

네트워크 개체를 만듭니다.

네트워크 개체를 만들면 페이지의 나머지 부분에서는 세션에 인스턴스화된 네트워크 개체가 있다고 가정합니다.

## 네트워크 개체

| 매개 변수 | type | 설명 |
|---|---|---|
| *`network`* | 문자열 | Livefyre 네트워크. 예를 들면 다음과 같습니다. «`labs.fyre.co`». |
| *`networkKey`* | 문자열 | The Livefyre-provided secret key for the network. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
