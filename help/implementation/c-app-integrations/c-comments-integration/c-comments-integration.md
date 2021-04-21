---
description: 페이지에서 실시간으로 주석을 달 수 있습니다.
title: 설명
exl-id: d62b3dc1-3c5e-45f6-9b21-ea1edcda9812
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 2%

---

# 설명{#comments}

페이지에서 실시간으로 주석을 달 수 있습니다. 주석을 사용하면 기본 주석 달기 시스템을 페이지의 실시간 대화로 대체할 수 있습니다.

## 통합 {#concept_4093E8BAA96A464BA74D263DA031C0B0}

댓글 앱 포함은 시작 > 앱 임베딩에 설명된 핵심 앱을 임베드하는 과정을 따릅니다.

### 예

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
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

CollectionMeta 빌드 섹션에 설명된 대로 CollectionMeta는 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT로 인코딩되기 전에 다음 형식을 사용합니다.

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## NetworkConfig 개체 {#c-networkconfig-object}

`NetworkConfig` 개체는 네트워크 사용자에 대한 인증 시스템을 사용자 지정하는 JSON 개체입니다.
`NetworkConfig` 개체는 다음 매개 변수를 포함하는 JSON 개체입니다.

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| **authDelegate** | **  requiremdobject | 사용자 지정 네트워크 사용자에 대한 인증 시스템을 사용자 지정하는 데 사용됩니다. |
| **network** | 문자열 *필수* | Livefyre가 제공한 네트워크 이름입니다. 예:*yourname.fyre.co.* |
| **attachmentDelegate** | ** optionalobject | 앱 스트림에 표시되는 미디어 첨부 파일 유형을 지정하는 데 사용됩니다. 자세한 내용은 [미디어 제한](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media)을 참조하십시오. |
| **문자열** | ** optionalobject | Livefyre 코어 앱에서 HTML 요소의 텍스트 문자열을 사용자 지정하는 데 사용됩니다. 자세한 내용은 [문자열 사용자 지정](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)을 참조하십시오. |

## ConvConfig 개체 {#c-convconfig-object}

`convConfig` 개체는 Livefyre 앱이 페이지에서 렌더링하는 콘텐츠를 지정하는 데 사용되는 JSON 개체입니다.

>[!NOTE]
>
>여기에 나열된 `convConfig` 개체 매개 변수는 평가 앱에 적용되지 않습니다. `convConfig` 개체를 사용하는 평가 앱에 대한 통합 정보는 검토 통합을 참조하십시오.

`ConvConfig` 객체에는 다음과 같은 필수 매개 변수가 포함되어 있습니다.

| 매개 변수 | 유형 | 설명 |
|--- |--- |--- |
| **articleId** | ** requiremdstring | 사이트 내의 컬렉션을 고유하게 식별합니다. 일반적으로 이것은 CMS 내의 데이터베이스 기본 키 또는 게시물 ID에 해당합니다. 예:&quot;post-42&quot;. 255자로 제한됩니다.  참고: 아티클 URL을 articleId로 사용하는 경우 문자열이 MD5 또는 SHA-1로 인코딩되었는지 확인하십시오. |
| **authPageReload** | **  선택 사항 부울 | 댓글 앱에 적용:인증 프로세스 동안 사용자의 댓글이 로컬에 저장되는지 여부를 제어할 수 있습니다. true인 경우 사용자가 댓글을 입력한 다음 앱에 로그인하면 해당 댓글은 로컬에 저장되고 로그인 및 페이지 새로 고침 후 컨텐츠 필드에 다시 입력됩니다. false인 경우 로그인 프로세스 동안 입력한 내용이 지워지고 다시 입력해야 합니다. |
| **collectionMeta** | ** requiremdstring | 컬렉션에 대한 JWT 인코딩 메타데이터. 자세한 내용은 [CollectionMeta](#c_collectionmeta_object) 개체를 참조하십시오. |
| **el** | ** requiremdstring | 콘텐츠 스트림이 렌더링될 DOM 요소의 ID입니다. |
| **siteId** | ** requiremdstring | 컬렉션이 속하는 웹 사이트 또는 응용 프로그램에 대한 Livefyre 제공 ID. 예:&quot;303617&quot; |

>[!NOTE]
>
>댓글 앱 구현에는 `app` 매개 변수가 필요하지 않습니다.

`ConvConfig` 객체에는 다음과 같은 선택적 매개 변수도 포함될 수 있습니다.

| 매개 변수 | 유형 | 설명 |
|--- |--- |--- |
| **actionButtons** | *선택* 배열 | [공유] 및 [플래그] 단추 옆에 있는 컨텐츠 일부에 추가할 사용자 정의 작업 단추의 배열입니다. 자세한 내용은 사용자 지정 단추 추가를 참조하십시오. |
| **애니메이션** | ** 선택 사항 부울 | 애니메이션이 Livefyre 앱 내에서 실행되는지 여부를 정의합니다. 애니메이션을 비활성화하려면 false로 설정합니다. 기본값은 true입니다. |
| **anonymousFlagEnabled** | ** 선택 사항 부울 | 손님 사용자에게 컨텐츠에 플래그를 지정할 수 있는 옵션이 있는지 여부를 정의합니다. 기본값은 true입니다. |
| **browserType** | ** 옵션_문자열 | 표시 컨텐츠를 생성할 장치를 정의합니다. 이렇게 하면 CSS와 일부 기능이 입력 장치 유형에 맞게 변경됩니다. 옵션은 데스크탑, 모바일 또는 태블릿입니다. (비워 둘 경우, 기본적으로 표시 형식에 대해 Google 에이전트 결정이 결정됩니다.) |
| **checksum** | ** recommendedstring | CollectionMeta의 현재 상태를 식별합니다. 이 값을 변경하면 Livefyre가 CollectionMeta의 새 값으로 서버의 데이터를 업데이트합니다. |
| **datetimeFormat** | **  optionalstring 객체 함수 | 스트리밍된 내용의 날짜/시간 형식을 지정합니다. 자세한 내용은 날짜 및 시간 스탬프 사용자 정의를 참조하십시오. |
| **disable아바타** | ** 선택 사항 부울 | 아바타가 앱 스트림에서 렌더링되지 않도록 하여 브라우저에 로드된 항목 수를 줄입니다. 기본값은 false입니다. |
| **disableIE8Shim** | ** 선택 사항 부울 | HTML5 요소가 지원되도록 Livefyre가 Internet Explorer 8에 폴리칠하는 데 사용하는 기본 표시를 비활성화합니다. Livefyre는 다음 프로젝트를 사용합니다. [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). 기본값은 false입니다.  참고: 이 값이 false이면 Internet Explorer 8 지원을 위해 Livefyre 채팅을 호출하기 전에 일부 종류의 폴리채우기를 사용해야 합니다. |
| **disableThirdPartyAnalytics** | ** 선택 사항 부울 | Livefyre가 내부 측정에 사용할 수 있는 제3자 분석 시스템(Quantserve 및 Google Analytics)을 비활성화합니다. 기본값은 false입니다. |
| **editorCss** | ** optionalobject | 주석 편집기 스타일을 사용자 지정하는 데 사용됩니다. 편집기 필드 배경색뿐만 아니라 편집기 내에 표시되는 텍스트의 글꼴 색상, 크기 및 패밀리를 스타일을 지정할 수 있습니다.  예: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** 선택 사항 정수 | 로드 시 앱에 표시되는 기본 댓글 수를 설정할 수 있습니다. 1부터 50까지의 정수일 수 있습니다. |
| **initialNumVisibleLegacy** | ** 선택 사항 정수 | 로드 시 앱에 표시되는 이전 콘텐츠 항목의 기본 수를 설정할 수 있습니다. 1부터 50까지의 정수일 수 있습니다. 이 매개 변수를 지정하지 않으면 기본적으로 initialNumVisible이 사용됩니다.  예:컬렉션에 100개의 활성 및 100개의 기존 주석이 포함되어 있는 경우 initalNumVisible:10 및 initialNumVisibleLegacy:5를 설정하여 10개의 활성 주석(추가 표시 단추 포함) + 5개의 아카이브 주석(추가 표시 단추 포함)을 표시합니다. |
| **maxVisible** | ** 선택 사항 정수 | 채팅 앱에서 볼 수 있는 최상위 수준의 최대 컨텐츠 수를 설정합니다. 새 콘텐츠 스트림이 있는 경우 스트림 하단에 있는 컨텐츠는 페이지에서 제거됩니다. 자세히 보기.. 단추를 클릭하면 매개 변수가 무시되고 사용자가 원하는 만큼 컨텐츠를 표시할 수 있습니다. (이 매개 변수를 사용하여 고속 스트림의 페이지에 나타나는 항목 수를 제어할 수 있습니다.) |
| **postToButtons** | *선택* 배열 | 라이브 블로그 앱을 포함할 때 나타나는 공급자를 구성하는 데 사용됩니다. 사용 가능한 옵션은 2개(Twitter), fb(Facebook) 및 li(LinkedIn)입니다. 기본값은 [ tw , fb ]입니다. |
| **readOnly** | ** 선택 사항 부울 | 컬렉션에 대한 모든 상호 작용을 비활성화합니다. true인 경우 사용자는 스트림에 로그인할 수 없으며 컨텐츠를 게시, 편집, 회신 또는 좋아요 항목으로 게시할 수 없습니다. true이면 사용자가 컨텐츠에 플래그를 지정하고 공유할 수 있습니다. 기본값은 false입니다. |
| **stream** | ** optionalobject | 앱의 스트리밍을 구성하는 옵션이 포함되어 있습니다. |
| **stream.catchup** | ** 선택 사항 정수 | 스트림이 로드되어야 하는 현재 순간에 대한 이전 시간(초)을 지정합니다. 기본적으로 Livefyre는 50개의 콘텐츠를 로드한 다음 해당 콘텐츠와 현재 시간 사이에 제출된 모든 콘텐츠를 로드합니다. 매우 빠른 사용 사례에서, 콘텐츠가 너무 빨리 게시되어 앱이 현재를 &#39;따라잡기&#39;할 수 없습니다. 이 설정을 사용하여 초기 컨텐츠 로드 후 컨텐츠가 게시되는 이전 시간(초)을 정의합니다. |
| **stream.delay** | ** 선택 사항 정수 | 스트리밍 요청 간 시간(초)을 지정합니다. 이 매개 변수를 사용하여 콘텐츠의 흐름을 제어하고 DOM의 업데이트 빈도를 지연할 수 있습니다.  참고: 너무 크게 설정하면 스트림이 뒤로 넘어질 수 있습니다. |


>[!NOTE]
>
>앱 초기화 동안 하나 이상의 `convConfig` 개체를 전달하여 동일한 페이지에 여러 앱을 표시할 수 있습니다. 추가 앱은 브라우저 리소스를 사용하고, 숫자가 증가하면 성능이 저하될 수 있습니다.

## CollectionMeta 개체 {#c-collectionmeta-object}

`CollectionMeta` 개체는 컬렉션 내에 저장할 메타데이터를 지정하는 JSON 개체입니다.

`CollectionMeta` 는 항상 보안을 위해 Livefyre로 전달되기 전에 인코딩됩니다. 인코딩된 값은 위에 표시된 `ConvConfig` 객체로 전달됩니다.

>[!NOTE]
>
>`CollectionMeta` JSON 개체를 인코딩하려면 서버측 코드를 추가해야 합니다. 자세한 내용은 서버측 토큰 작성을 참조하십시오.

| 매개 변수 | 유형 | 설명 |
|--- |--- |--- |
| **articleId** | ** requiremdstring | 컬렉션에 대한 고유 ID. |
| **제목** | ** requiremdstring | 컬렉션에 적용할 제목. 이는 앱을 표시하는 페이지의 제목에 해당하는 경우가 많습니다.  예:&quot;통합이 매우 재미있습니다!&quot; <br>**참고: 제목**  의 최대 문자 길이는 255자입니다. 제목 필드는 HTML 엔티티를 지원하지 않습니다. UTF-8을 사용하여 특수 문자를 인코딩하십시오. |
| **url** | ** requiremdstring | 이 컬렉션에 첨부하려는 기본 절대 URL. 이 URL은 Facebook 및 Twitter, 이메일 알림 및 Livefyre Studio에서 공유된 콘텐츠에서 앱으로의 링크를 만드는 데 사용됩니다.  <br>**참고** Livefyre는 정규화된 도메인 이름을 사용해야 합니다.로컬 설정을 해결하기 위한 포트 번호 또는 콜백은 필요하지 않습니다. 로컬에서 테스트하는 경우 유효한 기본 URL 도메인을 사용해야 합니다. <br>예: `https://customer.com` 은 유효하지만  `https://localhost:5995` 은 유효하지 않습니다. 로컬 웹 서버를 설정하여 정규화된 도메인 이름을 승인하면 콜백이나 해상도가 필요하지 않으며 예상대로 로컬 개발을 진행할 수 있습니다. |
| **type** | ** requiremdstring | 컬렉션 유형입니다. `livechat`이어야 합니다. |

`CollectionMeta` 객체에는 다음과 같은 선택적 매개 변수도 포함될 수 있습니다.

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| **태그**&#x200B;가 있는 세그먼트만 필터링할 수 있습니다 | ** 옵션_문자열 | 단일 키워드 또는 구문의 쉼표로 구분된 목록. Studio 내 또는 검색 API를 사용하여 태그로 컬렉션을 검색합니다. <br> **참고: Studio를 통해 추가된 태그에는 공백이 포함될 수** 있지만 API를 통해 입력한 태그는 사용할 수 없습니다. UI에 공백을 표시하는 태그를 정의하려면 밑줄을 사용합니다. (예:`Monday_Quarterback`을 사용하여 Monday 쿼터백을 Studio에 표시합니다.) |

## 이벤트 핸들러 {#concept_06D8B811C98B4CC6B38C6340EBA176E5} 추가

이벤트 핸들러를 등록하려면 앱의 콜백 함수 내에서 widget.on 호출을 사용하십시오.

### 예

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
