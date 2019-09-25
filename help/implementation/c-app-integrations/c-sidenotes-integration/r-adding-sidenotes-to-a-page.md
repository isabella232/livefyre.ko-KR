---
description: 'null'
seo-description: 'null'
seo-title: 페이지에 사이드노트 추가
solution: Experience Manager
title: 페이지에 사이드노트 추가
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 페이지에 사이드노트 추가 {#adding-sidenotes-to-a-page}

Livefyre는 페이지에 Sidecenotes를 배치할 수 있는 몇 가지 구성 옵션을 제공합니다.

* 선택기 옵션은 사이드노트가 표시될 요소를 정의합니다.
* 앵커는 사이드 가능한 요소를 나타냅니다.
* 사용자 지정 스레드 컨테이너를 사용하면 사이드 노트 스레드의 위치를 사이드 컨텐츠와 관련하여 정의할 수 있습니다.
* [사이드노트 수] 옵션을 사용하면 지정된 위치에 추가된 시드노트 수를 표시할 수 있습니다.
* 여러 `ConvConfig` 개체를 사용하여 한 페이지에서 여러 스토리에 사이드노트를 추가할 수 있습니다.

## 선택기 {#section_wyj_4sv_sy}

선택기 옵션을 사용하면 사이드노트가 페이지에서 컨텐츠를 찾을 수 있습니다. 이 옵션의 값을 사용하면 사용할 요소를 동적으로 결정할 수 있습니다. 선택기 문자열(예: '#content p, #content img'), jQuery 객체(예: `$(‘#content’)`), DOM 요소 배열 또는 두 개의 속성이 있는 객체일 수 있습니다.포함 및 제외 그런 다음 사이드노트 앱은 지정된 요소나 페이지에 있는 일치하는 요소를 사용합니다. include 및 exclude 속성이 사용되는 경우 Sidecotes는 먼저 페이지를 분석하여 포함 속성의 모든 요소를 찾은 다음 제외 속성에 있는 모든 요소를 제거합니다.

## 앵커 {#section_ehq_psv_sy}

앵커는 컨텐츠를 사이드 지정할 수 있는 요소를 나타냅니다. 앵커 요소에는 텍스트나 이미지가 포함될 수 있습니다. 앱 구성 중에 전달되는 선택기 옵션에 따라 앵커 요소가 결정됩니다.

## 앵커 ID {#section_rsb_rsv_sy}

페이지의 앵커는 A를 사용하여 식별됩니다 `data-lf-anchor-id`.

앵커에 대한 ID를 직접 설정하려면 앵커에 매핑할 요소에 속성을 `data-lf-custom-anchor-id` 추가합니다. 이 기능은 앵커 자동 감지가 실패하는 경우에 유용합니다.

예를 들어, 이미지의 데스크톱 버전과 모바일 버전에 대해 다른 URL을 사용하려는 경우 서로 다른 두 URL이 다른 앵커에 매핑될 수 있습니다. 대신 HTML에서 모바일 및 데스크탑에서 `data-lf-custom-anchor-id` 동일한 이미지를 제공하면 이미지 요소가 단일 앵커로 처리됩니다.

앵커에는 동적으로 결정되는 유형이 있지만 `data-lf-custom-anchor-type` 속성을 사용하여 명시적으로 설정할 수도 있습니다.

>[!NOTE]
>
>열거형 번호 값을 사용해야 합니다.

사용 가능한 유형은 다음과 같습니다.

* **** 텍스트:1
* **** 이미지:2
* **** 미디어:3
* **** 리치:4

페이지에 [Sidenote 컨텐츠를 동적으로 추가하는](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) 방법을 자세히 알아보려면 updateAnchors 메서드를 `updateAnchors` 참조하십시오.

## 사용자 지정 스레드 컨테이너 {#section_jdh_btv_sy}

이 `threadContainerEl` 옵션을 사용하여 기본 위치가 아닌 사이드노트 스레드의 위치를 지정합니다. 기본적으로 앵커를 활성화하면 관련 컨텐츠 옆이나 아래에 사이드노트가 나타납니다. 이 기본값을 변경하려면 을 `threadContainerEl` 사용하여 스레드를 표시할 요소를 지정합니다.

이 옵션에 대한 이 값은 첫 번째 유효한 요소만 사용된다는 점을 제외하고 선택기 옵션과 동일하게 작동합니다.

## 사이드노트 수 {#section_pld_ntv_sy}

페이지에 선택적 사이드노트 수 위젯을 포함하려면 이 `numSidenotesEl` 옵션을 사용합니다. 이 옵션은 선택기 옵션과 동일한 입력을 허용하지만 입력 배열에서 첫 번째 유효한 요소만 사용합니다.

위젯은 제공된 요소 또는 일치하는 요소를 장식하며, 사이드노트 입력 아이콘, 이 위치에 입력된 시드노트 수 및 도움말 아이콘을 포함합니다.

위젯을 클릭하면 Sidenotes 및 사용 방법에 대한 간단한 설명과 함께 팝업이 표시됩니다.

설명과 예제 텍스트는 모두 사용자 지정 문자열( `questionExplanation` 및 `questionMockText`각각)을 사용하여 구성할 수 있습니다. 카운트 위젯과 팝업의 모양은 각각 사용자 지정 스타일( `numSidenotes` 및 `numSidenotesPopover`)을 사용하여 구성할 수도 있습니다.

## 단일 페이지에 여러 사이드노트 컬렉션 추가 {#section_pjl_ptv_sy}

Livefyre를 사용하면 하나의 페이지에 여러 개의 Sidecnotes 컬렉션을 추가할 수 있습니다. 예를 들어 페이지에 3개의 뉴스 스토리가 포함되어 있는 경우 Sidenotes 앱의 3개의 개별 반복을 포함할 수 있습니다. 이렇게 하려면 빌드하려는 각 Sidecnotes 인스턴스에 대해 별도의 `ConvConfig` 개체를 정의해야 합니다. 예:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
