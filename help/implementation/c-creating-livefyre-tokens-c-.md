---
description: '''C#'' 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 학습합니다.'
title: Livefyre 토큰 'C#' 만들기
exl-id: 6360c325-0c3f-4ecb-90f7-951ef4e6f410
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 2%

---

# Livefyre 토큰 만들기 C\# {#creating-livefyre-tokens-c}

``C#`` 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 학습합니다.

이전 설명서 및 샘플 코드를 활용하여 `C#.NET`을 사용하여 토큰을 만드는 방법을 작성할 수 있습니다.

Livefyre의 공식 라이브러리를 참조하려면 `C#` 개발자를 위한 시작점으로 [Java 라이브러리](https://github.com/Livefyre/livefyre-java-utils)를 사용합니다.

또한 명령줄에서 [Node.js 라이브러리](https://github.com/Livefyre/livefyre-nodejs-utils)를 사용하여 자신을 위한 참조 토큰을 생성하고 메서드 구조에 익숙해지도록 할 수도 있습니다.

* [컬렉션 메타 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [인증 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 종속성 {#section_c15_fnh_xz}

* 토큰을 생성하려면 프로젝트에서 [JWT 번호 패키지](https://www.nuget.org/packages/JWT)가 필요합니다.
* 이 페이지의 코드 샘플은 [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) 패키지를 사용합니다.

## CollectionMeta 토큰 {#section_dzt_4mh_xz}

페이지에 주석을 포함할 때 CollectionMeta 토큰은 Livefyre로 전달되고 시스템에 새 컬렉션에 필요한 메타데이터를 제공합니다. 또한 이 데이터의 MD5 `checksum`을 만듭니다. 이 데이터는 메타데이터가 변경되었는지 확인하기 위해 Livefyre가 확인합니다. (예: 아티클의 제목 또는 url이 편집된 경우)

이 토큰은 Livefyre의 기술 계정 관리자가 제공한 `Site Key`으로 서명됩니다.

다음을 참조하십시오.

* 공식 컬렉션 메타 토큰 문서
* [예제 요점](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 컬렉션에 대한 메타데이터가 포함된 Diconary를 만듭니다. articleId를 추가하기 전에 이 개체의 체크섬을 만들려고 하므로 이 단계에서 필요한 필드 중 일부만 추가할 것입니다.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **필요한** *제목*:컬렉션의 제목(일반적으로 아티클의 제목) 최대 길이는 255자입니다. html 엔티티를 지원하지 않습니다. UTF-8을 사용하여 특수 문자를 인코딩하십시오.
   * **** *필수*:아티클의 기본 URL입니다. 이것은 주석 공유 및 소셜 동기화 기능과 관리 대시보드에서 아티클로의 링크에 사용됩니다. 로컬에서 테스트하는 경우 Livefyre는 &#39;localhost&#39;를 도메인으로 허용하지 않습니다.
   * **** *태그선택* 사항:Livefyre 대시보드의 컬렉션에 추가할 태그의 쉼표로 구분된 목록입니다. 태그에는 공백이 포함될 수 없습니다. 관리 대시보드에 공백을 표시하려면 밑줄을 사용합니다.
   * **** *일반* 사용자:만들 컬렉션의 유형을 나타내는 문자열. 유효한 값:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      지정하지 않으면 기본적으로 LiveComments 컬렉션이 생성됩니다.


1. JSON은 이 사전을 인코딩하고 해당 사전의 md5 체크섬을 생성합니다.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. 사전에 **articleId**&#x200B;를 추가합니다. **checksum**&#x200B;은 collectionMeta 토큰에 들어가지 않지만 convConfig 객체에서 별도의 매개 변수로 전송해야 합니다.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleIdrequired*:Livefyre 사이트 내 컬렉션에 대한 고유 식별자. 일반적으로 CMS에 사용되는 고유한 articleId (예: WordPress 게시물 ID) 이 값은 변경되지 않아야 합니다. Livefyre는 siteId와 articleId의 조합으로 고유한 컬렉션을 식별합니다.

1. Livefyre가 제공하는 사이트 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS256을 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 사용자 인증 토큰 {#section_g1d_43h_xz}

사용자 인증 토큰은 Livefyre에 사용자를 서명하는 데 사용됩니다. 사용자가 사이트에 로그인하면 사이트에서 페이지의 Livefyre 위젯에 전달된 사용자 인증 토큰을 생성합니다. 인증 프로세스에 대한 자세한 내용은 원격 프로필을 참조하십시오.

이 토큰은 네트워크 이름(network.fyre.co)이 필요하며 Livefyre의 기술 계정 관리자가 사용자에게 제공하는 네트워크 키로 서명됩니다.

다음을 참조하십시오.

* 공식 인증 토큰 문서
* [예제 요점](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. 필요한 정보가 포함된 사전을 만듭니다.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **도메인:** 네트워크의 이름입니다(Livefyre에서 제공). 예: mynetwork.fyre.co
   * **user_id:** 사이트의 프로필 시스템에서 사용자의 고유한 사용자 id입니다. 영숫자만 사용할 수 있습니다(A-Z, a-z, 0-9). 시스템 사용자 ID에 잘못된 문자가 포함되어 있는 경우 Livefyre를 사용자 ID의 md5 해시 또는 base64 인코딩 버전으로 보내십시오. (이 경우 계정 관리자에게 문의하십시오.)
   * **만료:** 토큰이 만료되는 날짜(Epoch 시간)입니다. Livefyre의 로그인 상태가 사이트의 로그인 상태와 동기화되도록 사이트에 로그인 시 세션 시간을 일치시켜야 합니다.
   * **display_name:** 주석 스트림에 표시되어야 하는 사용자의 프로필 시스템의 표시 이름입니다.

1. Livefyre가 제공하는 네트워크 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS256을 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
