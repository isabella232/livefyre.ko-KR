---
description: Livefyre 서버측 작업을 위한 라이브러리 설치
seo-description: Livefyre 서버측 작업을 위한 라이브러리 설치
seo-title: 설치
solution: Experience Manager
title: 설치
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 설치{#installation}


## Java {#section_yd3_3zk_rz}

Java 라이브러리를 설치하려면 프로젝트의 POM에 이 종속성을 추가하십시오.

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

자세한 내용은 Java 문서를 읽거나 GitHub에서 소스를 [참조하십시오](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

NodeJS 라이브러리를 설치하려면 다음 줄을 실행합니다.

`$ npm install livefyre`

NodeJS 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

자세한 내용은 NodeJs 문서를 읽거나 GitHub에서 소스를 [참조하십시오](https://github.com/Livefyre/livefyre-nodejs-utils).

링크: [레슬러](https://github.com/danwrong/restler), [유효성 검사기](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Composer를 사용하여 PHP 라이브러리를 설치하려면 composer.json에 추가하십시오.

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

그런 다음 다음을 사용하여 설치합니다.

```
composer.phar install 
```

Composer를 사용하지 **않는** 경우 다음을 사용하여 최신 버전의 라이브러리를 가져옵니다.

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

라이브러리를 사용하려면 PHP 스크립트에 다음을 추가하십시오.

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

자세한 내용은 PHP 문서를 읽거나 GitHub에서 소스를 [참조하십시오](https://github.com/Livefyre/livefyre-php-utils).

링크: [ext-json](https://php.net/manual/en/book.json.php), [요청](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Python 라이브러리를 설치하려면 다음 줄을 실행하십시오.

`$ pip install livefyre`

Python 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

자세한 내용은 Python 문서를 참조하거나 GitHub에서 소스를 [참조하십시오](https://github.com/Livefyre/livefyre-python-utils).

링크:PyJWT [,](https://github.com/progrium/pyjwt)Py [](https://github.com/kennethreitz/requests)JWT [,](https://pypi.python.org/pypi/python-dateutil)Python-Dateutil, [](https://pypi.python.org/pypi/enum34)[Enum34 OrderedDict](https://pypi.python.org/pypi/ordereddict)

## 루비 {#section_fv2_tzq_rz}

Ruby 라이브러리를 설치하려면 다음 줄을 응용 프로그램의 Gemfile에 추가하십시오.

```
gem 'livefyre' 
```

또는 직접 설치:

`$ gem install livefyre`

Ruby 라이브러리에는 다음 모듈에 대한 종속성이 있습니다.

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

자세한 내용은 Ruby 문서를 읽거나 GitHub에서 소스를 [참조하십시오](https://github.com/Livefyre/livefyre-ruby-utils).

링크:Ruby [JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST 클라이언트](https://github.com/rest-client/rest-client/), [주소 지정 가능](https://github.com/sporkmonger/addressable)
