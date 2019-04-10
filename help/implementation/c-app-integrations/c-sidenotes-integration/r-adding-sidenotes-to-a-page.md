---
description: null
seo-description: null
seo-title: 페이지에 Sidenotes 추가
solution: Experience Manager
title: 페이지에 Sidenotes 추가
uuid: 6499 C 45 A -3773-4 ADB-A 6 C 7-22 A 628309 AFD
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 페이지에 Sidenotes 추가 {#adding-sidenotes-to-a-page}

Livefyre는 페이지에 Sidenotes를 배치할 수 있는 몇 가지 구성 옵션을 제공합니다.

* 선택기 옵션은 Sidenotes가 표시될 요소를 정의합니다.
* 앵커는 타깃팅할 수 있는 요소를 나타냅니다.
* 사용자 지정 스레드 컨테이너를 사용하면 Sidenoted 콘텐츠와 관련하여 Sidenotes 스레드를 찾아야 하는 위치를 정의할 수 있습니다.
* [Sidenotes 수] 옵션을 사용하여 지정된 위치에 추가된 Sidenotes 수를 표시할 수 있습니다.
* 여러 `ConvConfig` 개체를 사용하여 한 페이지의 여러 스토리에 Sidenotes를 추가할 수 있습니다.

## 선택기 {#section_wyj_4sv_sy}

선택기 옵션을 사용하면 Sidenotes가 페이지에서 컨텐츠를 찾을 수 있습니다. 이 옵션의 값을 사용하여 사용할 요소를 동적으로 결정할 수 있습니다. 선택기 문자열 (예:' # content p, # content img '), jquery 객체 (예: `$(‘#content’)`), DOM 요소 배열 또는 두 가지 속성을 갖는 객체일 수 있습니다. 포함 및 제외. 그런 다음 Sidenotes 앱은 지정된 요소 또는 페이지에서 일치하는 요소를 사용합니다. 포함 및 제외 속성이 사용된 경우, Sidenotes가 먼저 페이지를 분석하여 포함 속성에 있는 모든 요소를 찾은 다음 exclude 속성에 있는 모든 요소를 제거합니다.

## 앵커 {#section_ehq_psv_sy}

앵커는 컨텐츠를 타깃팅할 수 있는 요소를 나타냅니다. 앵커 요소에는 텍스트나 이미지가 포함될 수 있습니다. 앱 빌드 중에 전달되는 선택기 옵션은 앵커 요소를 결정합니다.

## 앵커 ID {#section_rsb_rsv_sy}

페이지의 앵커는 A를 사용하여 `data-lf-anchor-id`식별됩니다.

앵커에 대한 ID를 직접 설정하려면 앵커에 매핑할 요소에 속성을 `data-lf-custom-anchor-id` 추가합니다. 이 기능은 앵커 자동 감지 기능이 실패하는 경우에 유용합니다.

예를 들어, 이미지의 데스크톱 및 모바일 버전에 대해 다른 URL를 사용하려는 경우 서로 다른 두 URL를 서로 다른 앵커로 매핑할 수 있습니다. 대신 HTML를 모바일 및 `data-lf-custom-anchor-id` 데스크탑에서 동일하게 제공하는 경우 이미지 요소가 단일 앵커로 처리됩니다.

앵커에는 동적으로 결정되는 유형이 있지만 `data-lf-custom-anchor-type` 특성을 사용하여 명시적으로 설정할 수도 있습니다.

>[!NOTE]
>
>열거형 번호 값을 사용해야 합니다.

사용 가능한 유형은 다음과 같습니다.

* **텍스트:** 1
* **이미지:** 2
* **미디어:** 3
* **풍부한 기능:** 4

메서드를 [사용하여 페이지에 Sidenote 내용을 동적으로 추가하는 방법에 대한 자세한](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) `updateAnchors` 내용은 updateanchors 메서드를 참조하십시오.

## 사용자 지정 스레드 컨테이너 {#section_jdh_btv_sy}

`threadContainerEl` 기본 위치가 아닌 Sidenotes 스레드의 위치를 지정하는 옵션을 사용합니다. 기본적으로 앵커가 활성화되면 관련 컨텐츠 옆이나 아래에 Sidenotes가 나타납니다. 이 기본값을 변경하려면을 `threadContainerEl` 사용하여 스레드가 표시될 요소를 지정합니다.

이 옵션의 값은 첫 번째 유효한 요소만 사용할 수 있는 선택기 옵션과 동일하게 작동합니다.

## Sidenotes 수 {#section_pld_ntv_sy}

페이지에 선택적 Sidenotes 수 위젯을 포함하려면 `numSidenotesEl` 옵션을 사용합니다. 이 옵션은 선택기 옵션과 동일한 입력을 허용하지만 입력 배열에서 첫 번째 유효한 요소만 사용합니다.

위젯은 제공되거나 일치하는 요소를 장식하며, Sidenotes 입력 아이콘, 이 위치에 입력한 Sidenotes 수 및 도움말 아이콘을 포함합니다.

위젯을 클릭하면 Sidenotes에 대한 간단한 설명과 사용 방법에 대한 팝업이 표시됩니다.

설명과 예제 텍스트는 모두 사용자 지정 문자열 ( `questionExplanation` 및 `questionMockText`, 각각) 를 사용하여 구성할 수 있습니다. 사용자 지정 스타일 ( `numSidenotes` 및 `numSidenotesPopover`각각) 를 사용하여 카운트 위젯의 모양과 팝업을 구성할 수도 있습니다.

## 여러 Sidenotes 컬렉션을 하나의 페이지에 추가 {#section_pjl_ptv_sy}

Livefyre를 사용하면 여러 개의 Sidenotes 컬렉션을 하나의 페이지에 추가할 수 있습니다. 예를 들어 페이지에 3 개의 뉴스 이야기가 포함된 경우 3 개의 Sidenotes 응용 프로그램을 별도로 포함시킬 수 있습니다. 이렇게 하려면 만들려는 Sidenotes의 각 인스턴스에 대해 별도의 `ConvConfig` 개체를 정의해야 합니다. 예를 들면 다음과 같습니다.

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
