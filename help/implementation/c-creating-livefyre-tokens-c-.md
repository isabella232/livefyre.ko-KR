---
description: C # 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 알아봅니다.
seo-description: C # 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 알아봅니다.
seo-title: Livefyre 토큰 만들기'c #'
solution: Experience Manager
title: Livefyre 토큰 만들기'c #'
uuid: C 5 E 05625-8550-4 B 51-9211-134600 E 20 EC 7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre 토큰 만들기 C\ # {#creating-livefyre-tokens-c}

``C#`` 언어를 사용하여 Livefyre 토큰을 생성하는 방법을 학습합니다.

기존 설명서 및 샘플 코드를 활용하여 토큰을 만드는 `C#.NET` 방법을 작성할 수 있습니다.

Livefyre의 공식 라이브러리를 참조하려면 [Java 라이브러리를](https://github.com/Livefyre/livefyre-java-utils) 개발자를 위한 `C#` 시작점으로 사용하십시오.

명령줄에서 [node. js 라이브러리를](https://github.com/Livefyre/livefyre-nodejs-utils) 사용하여 직접 참조 토큰을 생성하고 메서드 구조에 익숙해지는 것을 고려할 수도 있습니다.

* [컬렉션 메타 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [인증 토큰으로 이동](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 종속성 {#section_c15_fnh_xz}

* 토큰을 생성하려면 프로젝트에서 [JWT nuget 패키지가](https://www.nuget.org/packages/JWT) 필요합니다.
* 이 페이지의 코드 샘플은 [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) 패키지를 사용합니다.

## Collectionmeta Token {#section_dzt_4mh_xz}

페이지에 주석을 포함할 때 Collectionmeta 토큰이 Livefyre로 전달되고, 새 컬렉션에 필요한 메타데이터가 포함된 시스템이 제공됩니다. 또한 이 데이터의 MD 5 `checksum` 를 만들면 Livefyre는 메타데이터가 변경되었는지 확인합니다. (예: 아티클의 제목 또는 URL 이 편집된 경우).

This token is signed with your `Site Key`, which was provided by your techncial account manager at Livefyre.

참고 항목:

* 공식 Collectionmeta 토큰 문서
* [예시](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 컬렉션에 대한 메타데이터가 포함된 Dictonary를 만듭니다. 이 단계에서는 필수 필드 중 일부를 추가하기만 하면 Articleid를 추가하기 전에 이 개체의 체크섬을 만들고자 합니다.

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

   * **Title** *Required*: 컬렉션의 제목 (일반적으로 아티클의 제목) 입니다. 최대 길이는 255 자입니다. HTML 엔티티를 지원하지 않습니다. UTF -8를 사용하여 특수 문자를 인코딩하십시오.
   * **필요한 URL****: 집필의 기본 URL 입니다. 이 기능은 주석 공유 및 소셜 동기화 기능 및 관리 대시보드에서 아티클에 대한 링크를 통해 사용됩니다. 로컬로 테스트하는 경우 Livefyre 는'localhost'를 도메인으로 수락하지 않습니다.
   * **태그** *선택*사항: Livefyre 대시보드의 컬렉션에 추가할 쉼표로 구분된 태그 목록입니다. 태그는 공백을 포함할 수 없습니다. 공백이 관리 대시보드에 나타나도록 하려면 밑줄을 사용합니다.
   * **선택** *사항*: 만들 컬렉션의 유형을 나타내는 문자열입니다. 유효한 값은 다음과 같습니다.

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      지정하지 않으면 기본적으로 Livecomments 컬렉션이 생성됩니다.


1. JSON 이 사전을 인코딩하고 MD 5 체크섬을 생성합니다.

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

1. **Articleid** 를 사전에 추가합니다. **checksum** 는 collectionmeta 토큰에 들어가지 않지만 convconfig JS 개체에서 seaprate 매개 변수로 보내야 합니다.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Articleid** *required*: Livefyre 사이트 내 컬렉션의 고유 식별자입니다. 일반적으로 CMS에서 사용되는 고유 articleid 입니다. (예: Wordpress 게시물 ID) 이 값은 절대 변경되지 않습니다. Livefyre는 siteid와 articleid의 결합으로 고유 컬렉션을 식별합니다.

1. Livefyre에서 제공하는 사이트 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS 256를 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 사용자 인증 토큰 {#section_g1d_43h_xz}

사용자 인증 토큰은 Livefyre에 사용자를 서명하는 데 사용됩니다. 사용자가 사이트에 로그인하면 사이트에서 Livefyre 위젯에 전달된 사용자 인증 토큰을 생성합니다. 인증 프로세스에 대한 자세한 내용은 원격 프로필을 참조하십시오.

이 토큰은 네트워크 이름 (network. fyre. co) 이 필요하며, Livefyre의 기술 계정 관리자가 제공하는 네트워크 키로 서명됩니다.

참고 항목:

* 공식 인증 토큰 문서
* [예시](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. 필요한 정보를 포함하는 디토ary를 만듭니다.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **도메인:** 네트워크 이름 (Livefyre 제공) E.G mynetwork. fyre. co
   * **user_ id:** 사이트의 프로필 시스템에서 사용자의 고유한 사용자 ID 입니다. 영숫자 문자만 (a-z, A-Z, 0-9) 이어야 합니다. 시스템 사용자 ID에 잘못된 Charaacter가 포함되어 있는 경우 Livefyre를 사용자 ID의 MD 5 해시 또는 Base 64 인코딩 버전으로 보내는 것을 고려해 보십시오. (계정 관리자가 이를 하는지 알려주십시오.)
   * **만료일:** 토큰이 만료되는 날짜 (epoch 시간) 입니다. 이는 Livefyre의 로그인 상태가 사이트의 로그인 상태와 동기화되도록 사이트의 로그인 세션 시간과 일치해야 합니다.
   * **display_ name:** 프로필 시스템에 표시되는 사용자의 표시 이름입니다.

1. Livefyre에서 제공하는 네트워크 키를 사용하여 사전의 서명된 JWT 토큰을 생성합니다. JWT 패키지는 기본적으로 HS 256를 사용하지 않으므로 올바른 해시 알고리즘을 지정해야 합니다.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
