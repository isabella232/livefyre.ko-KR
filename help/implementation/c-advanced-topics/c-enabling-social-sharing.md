---
description: 사용자가 다양한 소셜 네트워크에 컨텐츠를 공유할 수 있도록 해주는 자격 증명을 설정합니다.
seo-description: 사용자가 다양한 소셜 네트워크에 컨텐츠를 공유할 수 있도록 해주는 자격 증명을 설정합니다.
seo-title: 소셜 공유 활성화
solution: Experience Manager
title: 소셜 공유 활성화
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# 소셜 미디어 공유 활성화 {#enabling-social-sharing}

사용자가 다양한 소셜 네트워크에 컨텐츠를 공유할 수 있도록 해주는 자격 증명을 설정합니다.

사용자가 소셜 미디어 사이트에서 컨텐츠를 공유할 수 있도록 하려면 Livefyre의 소셜 공유 기능을 구현하고 이러한 사이트에 적합한 인증을 제공하는 OAuth 시스템을 만듭니다. 이 시스템을 통해 Livefyre는 소셜 미디어를 통해 컨텐츠를 공유하기로 선택할 때 사용자를 대신하여 작동합니다.

>[!NOTE]
>
>서로 다른 공급자마다 OAuth 요구 사항이 다릅니다. OAuth 구현과 관련된 정보를 얻으려면 제공자와 문의하십시오.

## 필수 소셜 자격 증명 {#section_gff_cjm_b1b}

사용자 정의 사용자 ID 시스템을 사용하는 경우 사용자가 Livefyre 앱에서 Twitter, Facebook 또는 LinkedIn에 공유할 수 있도록 소셜 자격 증명을 제공해야 합니다.

>[!NOTE]
>
>Janrain Engage를 사용하는 고객은 Engage Domain 및 Engage API 키만 제공해야 합니다.

다음 소셜 자격 증명을 입력하거나 업데이트하려면 Admin Console의 통합 설정 패널을 사용합니다.

### 필수 자격 증명:

* **** FacebookClient ID 클라이언트 암호 OAuth 프록시 리디렉션
* **** LinkedInAPI 키 API 암호
* **** TwitterAccess 토큰 액세스 토큰 비밀 API 키 API 암호

## Twitter {#section_qp5_1yl_b1b}

Twitter 자격 증명은 Twitter 앱 대시보드에서 사용할 수 있습니다. 다음 자격 증명을 찾으려면:

* [Twitter의 앱 개발 페이지](https://dev.twitter.com/apps)를 앱 소유자로 열고 애플리케이션을 찾은 다음 제목을 클릭합니다.
* &quot;액세스 토큰&quot;으로 스크롤하여 &quot;액세스 토큰&quot; 및 &quot;액세스 토큰 비밀&quot;의 값을 찾습니다.

다음을 수행해야 합니다.

* Twitter 앱에서 콜백 URL 필드에 값을 입력합니다. 이 필드는 단순 자리 표시자일 수 있지만 비워 둘 수 없습니다.
* 응용 프로그램 유형을 **read** 및 **write** 액세스 권한을 모두 갖도록 설정합니다.
* Twitter 앱 웹 사이트 URL이 Livefyre 코어 앱과 동일한 호스트 도메인에 있는지 확인합니다.

>[!NOTE]
>
>Twitter 컨텐츠를 표시하는 모든 애플리케이션은 표시 요구 사항을 준수해야 합니다. 자세한 내용은 [Twitter 표시 지침](https://dev.twitter.com/terms/display-requirements)을 참조하십시오.

## LinkedIn {#section_lfz_zxl_b1b}

LinkedIn 자격 증명은 LinkedIn 응용 프로그램 API 키의 OAuth 키 섹션에서 사용할 수 있습니다.

* LinkedIn의 개발자 페이지 [https://developer.linkedin.com/](https://developer.linkedin.com/)에서 계정에 로그인합니다.
* 오른쪽 상단에서 자신의 이름을 가리키고 드롭다운 메뉴에서 API 키를 선택합니다.
* 애플리케이션 제목을 클릭합니다.
* OAuth 키 섹션에서 API 키 및 비밀 키 값 가져오기

## Facebook {#section_zyb_gpl_b1b}

Facebook 자격 증명은 개발자 앱 페이지에서 사용할 수 있습니다.

* [Facebook의 개발자 앱 페이지](https://developers.facebook.com/apps)를 앱 소유자로 열고 애플리케이션을 찾은 다음 제목을 클릭합니다.
* 앱 ID 및 앱 암호 값을 선택합니다. 앱 비밀의 경우 표시 버튼을 클릭하여 표시할 수 있습니다.

Facebook에 공유하려면 Facebook 요청을 가져오기 위해 리디렉션 페이지를 설정하고 [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/)에 필요한 도메인 방침을 준수해야 합니다. 페이지가 도메인에 호스팅되어야 Facebook에서 요청이 합법적인 소스에서 왔는지를 확인할 수 있습니다.

### Facebook 리디렉션

호스팅된 페이지에는 다음 코드가 포함되어야 합니다.

### 루비

Ruby 및 Rails를 사용하여 Facebook OAuth 리디렉션을 수행하는 예입니다.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### 파이톤

Python 및 Dango를 사용하여 Facebook OAuth 리디렉션을 수행하는 예입니다.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

NodeJS 및 Sail/Express를 사용하여 Facebook OAuth 리디렉션을 수행하는 예입니다.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Java 및 Spring 컨트롤러를 사용하여 Facebook OAuth 리디렉션을 수행하는 예입니다.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## &quot;게시물 위치&quot; 공급자 구성 {#section_rdk_dpl_b1b}

기본적으로 Facebook, LinkedIn 및 Twitter &quot;게시물 위치&quot; 단추가 Livefyre 코어 응용 프로그램에 표시됩니다. postToButtons 매개 변수를 사용하여 Livefyre 앱을 임베드할 때 표시할 공급자를 구성합니다.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` 는 다음 옵션 중 일부를 포함하는 배열입니다.

* tw:Twitter
* fb:Facebook
* li:LinkedIn
