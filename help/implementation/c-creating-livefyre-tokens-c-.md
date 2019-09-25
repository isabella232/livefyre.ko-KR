---
description: '''C#'' 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 알아봅니다.'
seo-description: '''C#'' 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 알아봅니다.'
seo-title: Livefyre 토큰 'C#' 만들기
solution: Experience Manager
title: Livefyre 토큰 'C#' 만들기
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creating Livefyre Tokens C\# {#creating-livefyre-tokens-c}

``C#`` 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 학습합니다.

이전 설명서 및 샘플 코드를 활용하여 메서드를 작성하여 토큰을 만드는 `C#.NET` 데 사용할 수 있습니다.

Livefyre의 공식 라이브러리를 참조하려면 Java [라이브러리를](https://github.com/Livefyre/livefyre-java-utils) 개발자를 위한 시작점으로 `C#` 사용하십시오.

또한 명령줄에서 Node.js [라이브러리를](https://github.com/Livefyre/livefyre-nodejs-utils) 사용하여 자신을 위한 참조 토큰을 생성하고 메서드 구조에 익숙해지도록 고려할 수 있습니다.

* [컬렉션 메타 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [인증 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 종속성 {#section_c15_fnh_xz}

* 토큰을 생성하려면 프로젝트에서 [JWT 번호](https://www.nuget.org/packages/JWT) 패키지가 필요합니다.
* 이 페이지의 코드 샘플은 Newtonsoft JSON [패키지를](https://www.nuget.org/packages/newtonsoft.json/) 사용합니다.

## CollectionMeta 토큰 {#section_dzt_4mh_xz}

CollectionMeta 토큰은 페이지에 주석을 포함할 때 Livefyre로 전달되고 시스템에 새 컬렉션에 필요한 메타데이터를 제공합니다. 또한 이 데이터의 MD5 `checksum` 를 만들어 Livefyre가 메타데이터가 변경되었는지 확인합니다. (예: 아티클의 제목 또는 URL을 편집한 경우)

이 토큰은 `Site Key`사용자의 Livefyre 기술 계정 관리자가 제공한 것입니다.

다음을 참조하십시오.

* 공식 컬렉션 메타 토큰 문서
* [예제 요점](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 컬렉션에 대한 메타데이터가 포함된 사전을 만듭니다. articleId를 추가하기 전에 이 개체의 체크섬을 만들려고 하므로 이 단계에서 필요한 필드 중 일부만 추가하려고 합니다.

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

   * **title** required **: 컬렉션의 제목(일반적으로 아티클의 제목)입니다. 최대 길이는 255자입니다. html 엔터티를 지원하지 않습니다. UTF-8을 사용하여 특수 문자를 인코딩하십시오.
   * **url** *필수*: 아티클의 기본 URL입니다. 이 기능은 댓글 공유 및 소셜 동기화 기능과 관리 대시보드에서 아티클로의 링크에 사용됩니다. 로컬에서 테스트하는 경우 Livefyre는 'localhost'를 도메인으로 허용하지 않습니다.
   * **태그** 선택 사항 **: Livefyre 대시보드에서 컬렉션에 추가할 태그의 쉼표로 구분된 목록입니다. 태그에는 공백을 포함할 수 없습니다. 관리 대시보드에 공백을 표시하려면 밑줄을 사용합니다.
   * **type** *optional*: 만들 컬렉션의 유형을 나타내는 문자열입니다. 유효한 값:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      지정하지 않으면 기본적으로 LiveComments 컬렉션이 만들어집니다.


1. JSON은 이 사전을 인코딩하여 md5 체크섬을 생성합니다.

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

1. 사전에 **articleId** 추가를 참조하십시오. checksum **은** collectionMeta 토큰으로 이동하지 않지만 convConfig js 개체에서 별도의 매개 변수로 전송해야 합니다.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId** *필요*: Livefyre 사이트 내에서 컬렉션에 대한 고유한 식별자. 일반적으로 CMS에 사용되는 고유한 articleId입니다. (예: WordPress 게시물 ID) 이 값은 절대 변경되지 않습니다. Livefyre는 siteId와 articleId의 조합으로 고유한 컬렉션을 식별합니다.

1. Livefyre가 제공한 사이트 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS256을 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 사용자 인증 토큰 {#section_g1d_43h_xz}

사용자 인증 토큰은 Livefyre에 사용자를 서명하는 데 사용됩니다. 사용자가 사이트에 로그인하면 사이트에서 페이지의 Livefyre 위젯에 전달된 사용자 인증 토큰을 생성합니다. 인증 프로세스에 대한 자세한 내용은 원격 프로필을 참조하십시오.

이 토큰은 네트워크 이름(network.fyre.co)이 필요하며 Livefyre의 기술 계정 관리자가 제공하는 네트워크 키로 서명됩니다.

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

   * **** 도메인:네트워크 이름(Livefyre에서 제공) 예: mynetwork.fyre.co
   * **** user_id:사이트의 프로필 시스템에서 사용자의 고유 사용자 ID입니다. 영숫자만 사용할 수 있습니다(A-Z, a-z, 0-9). 시스템 사용자 ID에 잘못된 문자가 포함되어 있는 경우 Livefyre를 사용자 ID의 md5 해시 또는 base64 인코딩 버전으로 전송하는 것이 좋습니다. (이 경우 계정 관리자에게 알리십시오.)
   * **** 만료:토큰이 만료되는 날짜(Epoch 시간)입니다. Livefyre의 로그인 상태가 사이트의 로그인 상태와 동기화되도록 사이트의 로그인 세션 시간과 일치해야 합니다.
   * **** display_name:댓글 스트림에 표시되어야 하는 사용자의 프로필 시스템에 표시되는 이름입니다.

1. Livefyre가 제공한 네트워크 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS256을 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
