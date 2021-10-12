---
description: Livefyre 서버측 작업을 위한 라이브러리 설치
title: 설치
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# 설치{#installation}


## Java {#section_yd3_3zk_rz}

Java 라이브러리를 설치하려면 프로젝트의 POM에 다음 종속성을 추가합니다.

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

자세한 내용은 Java 문서를 읽어보거나 [GitHub](https://github.com/Livefyre/livefyre-java-utils)에서 소스를 참조하십시오.

## NodeJS {#section_swj_pwq_rz}

NodeJS 라이브러리를 설치하려면 다음 줄을 실행합니다.

`$ npm install livefyre`

NodeJS 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

자세한 내용은 NodeJs 문서를 읽어보거나 [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils)에서 소스를 참조하십시오.

링크: [Restler](https://github.com/danwrong/restler), [유효성 검사기](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)

## PHP {#section_txj_xwq_rz}

Composer와 함께 PHP 라이브러리를 설치하려면 composer.json에 추가합니다.

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

그런 다음 를 사용하여 를 설치합니다.

```
composer.phar install 
```

Composer를 사용하지 않는 **을 사용하는 경우 다음을 사용하여 라이브러리의 최신 버전을 얻습니다.**

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

라이브러리를 사용하려면 PHP 스크립트에 다음을 추가합니다.

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

자세한 내용은 PHP 문서를 읽어보거나 [GitHub](https://github.com/Livefyre/livefyre-php-utils)에서 소스를 참조하십시오.

링크: [ext-json](https://www.php.net/manual/en/book.json.php), [요청](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## 파이톤 {#section_irk_fxq_rz}

Python 라이브러리를 설치하려면 다음 행을 실행합니다.

`$ pip install livefyre`

Python 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

자세한 내용은 Python 문서를 읽어보거나 [GitHub](https://github.com/Livefyre/livefyre-python-utils)에서 소스를 참조하십시오.

링크: [PyJWT](https://github.com/progrium/pyjwt), [요청](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## 루비 {#section_fv2_tzq_rz}

Ruby 라이브러리를 설치하려면 응용 프로그램의 Gemfile에 다음 줄을 추가합니다.

```
gem 'livefyre' 
```

또는 직접 설치합니다.

`$ gem install livefyre`

Ruby 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

자세한 내용은 Ruby 문서를 읽어보거나 [GitHub](https://github.com/Livefyre/livefyre-ruby-utils)에서 소스를 참조하십시오.

링크: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST 클라이언트](https://github.com/rest-client/rest-client/), [대응 가능](https://github.com/sporkmonger/addressable)
