---
description: 페이지에 실시간 채팅 추가를 참조하십시오.
seo-description: 페이지에 실시간 채팅 추가를 참조하십시오.
seo-title: 채팅
solution: Experience Manager
title: 채팅
uuid: d 6761 a 69-efa 5-4 ad 3-abaf -1 ba 8 e 6 c 17 f 94
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 채팅{#chat}

페이지에 실시간 채팅 추가를 참조하십시오.

채팅을 통해 사용자는 실시간 이벤트 관련 대화를 실시간으로 처리할 수 있습니다. 컨텐츠는 연속 스트림으로 표시되므로 펼침 대화 상자에 빠르게 참여할 수 있습니다.

현재 버전: 채팅 사용 `fyre.conv v3.0.0.`

## 통합 {#concept_0A99792A7E89403F95D082D52D600F17}

채팅 앱을 임베드하면 시작하기 > 앱 [포함에 설명된 핵심 앱 임베드에 대한 프로세스가 따릅니다](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

예:

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

[Collectionmeta 토큰](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) 섹션에 명시된 대로 collectionmeta는 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT 인코딩하기 전에 다음 형식을 사용합니다.

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Networkconfig 오브젝트 {#c-networkconfig-object}

`NetworkConfig` 개체는 네트워크 사용자를 위한 인증 시스템을 사용자 정의하는 JSON 개체입니다.

`NetworkConfig` 개체는 다음 매개 변수를 포함하는 JSON 개체입니다.

| 매개 변수 | type | 설명 |
|---|---|---|
| Authdelegate | *필수* 개체 | 사용자 정의 네트워크 사용자에 대한 인증 시스템을 사용자 지정하는 데 사용됩니다. |
| 네트워크 | *필수* 문자열 | Livefyre에서 제공하는 네트워크 이름입니다. 예를 들면 다음과 같습니다. *yourname. fyre. co.* |
| Attachmentdelegate | 개체 | 앱 스트림에 표시되는 미디어 첨부 파일 유형을 지정하는 데 사용됩니다. 자세한 내용은 미디어 [제한을](../c-app-customizations/c-restrict-media.md#c_restrict_media)참조하십시오. |
| 문자열 | ** 선택적 개체 | Livefyre 코어 앱에서 HTML 요소의 텍스트 문자열을 사용자 정의하는 데 사용됩니다. 자세한 내용은 [문자열 사용자 정의를](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)참조하십시오. |

## Convconfig 오브젝트 {#c-convconfig-object}

`convConfig` 개체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.

>[!NOTE]
>
>여기에 나열된 `convConfig` 개체 매개 변수는 검토 앱에는 적용되지 않습니다. 개체를 사용하는 리뷰 앱에 대한 통합 정보는 `convConfig` 통합 검토를 참조하십시오.

`ConvConfig` 개체에는 다음과 같은 필수 매개 변수가 포함됩니다.

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| Articleid | *필수* 문자열 | 사이트 내 컬렉션을 고유하게 식별합니다. 일반적으로 CMS 내의 데이터베이스 기본 키나 게시물 ID에 해당합니다. 예를 들면 다음과 같습니다. «post -42». 255 자 제한. 참고: 아티클 URL를 articleid로 사용하는 경우, 문자열이 MD 5 또는 SHA -1 인코딩되어 있는지 확인하십시오. |
| collectionmeta | *필수* 문자열 | JWT 인코딩 메타데이터에 대한 메타데이터. 자세한 내용은 [Collectionmeta 객체를](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) 참조하십시오. |
| el | *필수* 문자열 | 컨텐츠 스트림이 렌더링할 DOM 요소의 ID. |
| Siteid | *필수* 문자열 | 컬렉션이 속한 웹 사이트 또는 응용 프로그램에 대한 livefyre 제공 ID. 예를 들면 다음과 같습니다. «303617». |

>[!NOTE]
>
>댓글 앱 구현에는 `app` 매개 변수가 필요하지 않습니다.

`ConvConfig` 개체는 다음과 같은 선택적 매개 변수를 포함할 수도 있습니다.

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| Actionbuttons | ** 선택적 배열 | 공유 및 플래그 단추 옆에 있는 컨텐츠 조각에 추가할 사용자 정의 작업 단추 배열입니다. 자세한 내용은 사용자 정의 단추 추가를 참조하십시오. |
| 애니메이션 | *optional* boolean | Livefyre 앱에서 애니메이션이 실행되는지 여부를 정의합니다. 애니메이션을 비활성화하려면 false로 설정합니다. 기본값은 true 입니다. |
| Anonymousflaggingenabled | *optional* boolean | 손님 사용자에게 콘텐츠에 플래그를 지정할 수 있는 옵션이 있는지 여부를 정의합니다. 기본값은 true 입니다. |
| Browsertype | *선택적* 문자열 | 표시 내용을 생성해야 하는 장치를 정의합니다. 이로 인해 CSS 및 일부 기능이 입력 장치 유형에 맞게 변경됩니다. 옵션은 데스크탑, 모바일 또는 태블릿입니다. (비워 두면 기본적으로 디스플레이 형식에 대한 Google 에이전트 결정이 표시됩니다.) |
| checksum | *권장* 문자열 (권장) | Collectionmeta의 현재 상태를 식별합니다. 이 값을 변경하면 Livefyre가 서버의 데이터를 collectionmeta의 새 값으로 업데이트합니다. |
| Datetimeformat | *선택적* 문자열 개체 함수 | 스트리밍 컨텐츠의 Datetime 형식을 지정합니다. 자세한 내용은 날짜 및 타임스탬프 사용자 지정을 참조하십시오. |
| Disableavatars | *optional* boolean | 아바타가 앱 스트림에 렌더링되지 않도록 하여 브라우저에 로드된 항목의 수를 줄일 수 있습니다. 기본값은 false 입니다. |
| disableIE8Shim | *optional* boolean | Livefyre에서 Polyfill Internet Explorer 8에 사용하는 기본 Shiv를 비활성화하여 HTML 5 요소가 지원됩니다. Livefyre는 다음 프로젝트를 사용합니다. [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). 기본값은 false 입니다. 참고: 이 값이 false 이면 Internet Explorer 8 지원에 대해 Livefyre Chat가 호출되기 전에 일부 Sort의 Polyfill를 사용해야 합니다. |
| Disablethirdpartyanalytics | *optional* bboolean | Livefyre가 내부 측정에 사용할 수 있는 타사 분석 시스템 (Quantserve 및 Google Analytics) 를 비활성화합니다. 기본값은 false 입니다. |
| Editorcss | ** 선택적 개체 | 주석 편집기 스타일링을 사용자 지정하는 데 사용됩니다. 편집기 내에 표시되는 텍스트의 글꼴 색상, 크기 및 글꼴은 물론 편집기의 필드 배경색을 스타일링할 수 있습니다. 예를 들면 다음과 같습니다. `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| Initialnumvisible | *선택적* 정수 | 로드 시 앱에 표시되는 기본 댓글 수를 설정할 수 있습니다. 1 부터 50 까지의 정수일 수 있습니다. |
| Initialnumvisiblelegacy | *선택적* 정수 | 로드 시 앱에 표시되는 기본 컨텐츠 항목의 수를 설정할 수 있습니다. 1 부터 50 까지의 정수일 수 있습니다. 이 매개 변수가 지정되지 않으면 기본값은 Initialnumvisible 입니다. 예를 들면 다음과 같습니다. 컬렉션에 활성 100 개 및 이전 댓글이 100 개 포함되는 경우 Initalnumvisible를 설정합니다. 10 및 Initialnumvisiblelegacy: 5. 10 개의 활성 댓글 (더 보기 단추 표시) 를 표시하려면 (더 보기 단추가 있는) 댓글을 보관합니다. |
| Maxvisible | *선택적* 정수 | 채팅 앱에서 최상위 수준의 볼 수 있는 콘텐츠 수를 설정합니다. 새 컨텐츠 스트림이 있는 경우 스트림 아래쪽의 컨텐츠가 페이지에서 제거됩니다. 더 보기... 단추를 클릭하면 매개 변수가 무시되고 사용자는 원하는 만큼 컨텐츠를 볼 수 있습니다. (고속 스트림의 페이지에 표시되는 항목의 수를 조정하려면 이 매개 변수를 사용합니다.) |
| Posttobuttons | ** 선택적 배열 | 라이브 블로그 앱을 포함할 때 표시되는 공급자를 구성하는 데 사용됩니다. 사용할 수 있는 옵션은 TW (Twitter), FB (Facebook) 및 LI (linkedin) 입니다. 기본값은 [ tw, fb ]입니다. |
| Readonly | *optional* boolean | 컬렉션에 대한 모든 대화형 기능을 비활성화합니다. true 이면 사용자가 스트림에 로그인할 수 없으며 컨텐츠를 게시, 편집, 답글 달기 또는 좋아할 수 없습니다. true 이면 사용자가 콘텐츠를 플래그 지정하고 공유할 수 있습니다. 기본값은 false 입니다. |
| stream | ** 선택적 개체 | 앱 스트리밍을 구성하는 옵션을 포함합니다. |
| stream. catchup | *선택적* 정수 | 스트림이 로드되어야 하는 현재 시간까지의 초 수를 지정합니다. 기본적으로 Livefyre는 50 개의 컨텐츠를 로드한 다음 이들 사이에 제출된 모든 컨텐츠를 로드합니다. 매우 빠른 사용 사례에서는 콘텐츠를 너무 빨리 게시하여 앱을 현재 상태로 전환할 수 있습니다. 이 설정을 사용하여 초기 컨텐츠 로드 후 컨텐츠가 게시될 이전 초 수를 정의합니다. |
| stream. delay | *선택적* 정수 | 스트리밍 요청 사이의 시간 (초) 를 지정합니다. 이 매개 변수를 사용하여 컨텐츠 흐름을 제어하고 DOM 이 업데이트되는 빈도를 지연시킬 수 있습니다. 참고: 너무 크면 스트림이 뒤쳐질 수 있습니다. |


>[!NOTE]
>
>앱 초기화 동안 하나 이상의 `convConfig` 개체를 전달하여 동일한 페이지에 여러 앱을 표시할 수 있습니다. 숫자가 증가하면 추가 앱이 브라우저 리소스를 사용하므로 성능이 저하될 수 있습니다.

## Collectionmeta 객체 {#c-collectionmeta-object}

`CollectionMeta` 개체는 컬렉션 내에 저장할 메타데이터를 지정하는 JSON 오브젝트입니다.

`CollectionMeta` 은 보안을 위해 Livefyre로 전달하기 전에 항상 인코딩됩니다. 인코딩된 값이 위에 표시된 `ConvConfig` 객체로 전달됩니다.

>[!NOTE]
>
>JSON 개체를 인코딩하려면 서버측 코드를 `CollectionMeta` 추가해야 합니다. 자세한 내용은 서버측 토큰 빌드를 참조하십시오.

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| Articleid | *필수* 문자열 | 컬렉션의 고유 ID 입니다. |
| title | *필수* 문자열 | 컬렉션에 적용할 제목입니다. 이것은 종종 앱을 표시하는 페이지의 제목과 일치합니다. 예를 들면 다음과 같습니다. «통합 기능은 정말 재미있습니다! » 참고: 제목의 최대 문자 길이는 255 자입니다. 제목 필드는 HTML 개체를 지원하지 않습니다. UTF -8를 사용하여 특수 문자를 인코딩하십시오. |
| URL | *필수* 문자열 | 이 컬렉션에 첨부할 기본 절대 URL 입니다. 이 URL는 Facebook 및 Twitter, 이메일 알림 및 Livefyre 스튜디오에서 공유한 콘텐츠에서 다시 앱을 연결하는 데 사용됩니다. 참고: Livefyre를 사용하려면 정규화된 도메인 이름을 사용해야 합니다. 로컬 설정을 해결하기 위한 포트 번호나 콜백은 필요하지 않습니다. 로컬로 테스트하는 경우 유효한 기본 URL 도메인을 사용해야 합니다. (예: `https://customer.com` is valid, while `https://localhost:5995` is not.) 로컬 웹 서버를 설정하여 정규화된 도메인 이름을 수락하면 콜백 또는 해상도가 필요하지 않으며 로컬 개발이 예상대로 진행될 수 있습니다. |
| type | *필수* 문자열 | 컬렉션 유형입니다. Livechat 이어야 합니다. |

`CollectionMeta` 개체는 다음 선택 매개 변수를 포함할 수도 있습니다.

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| 태그 | *선택적* 문자열 | 쉼표로 구분된 단일 키워드 또는 구문의 목록입니다. 스튜디오 내에서 또는 검색 API에서 태그별로 컬렉션을 검색할 수 있습니다. 참고: Studio를 통해 추가된 태그에는 공백이 있을 수 있지만 API를 통해 입력한 태그는 사용할 수 없습니다. 밑줄을 사용하여 UI에서 공백을 표시하는 태그를 정의합니다. (예: Monday_ Quarterback를 사용하여 Studio에서 Monday 쿼터백 표시) |

## 이벤트 핸들러 추가 {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

이벤트 핸들러를 등록하려면 앱의 콜백 함수 내에서 widget. on 호출을 사용합니다.

예를 들면 다음과 같습니다.

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

자세한 내용 및 사용 가능한 이벤트 목록은 [Javascript 이벤트를](../c-app-customizations/c-javascript-events.md#c_javascript_events)참조하십시오.
