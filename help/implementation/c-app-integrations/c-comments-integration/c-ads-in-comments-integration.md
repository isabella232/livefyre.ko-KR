---
description: 댓글 스트림에 광고를 삽입합니다.
seo-description: 댓글 스트림에 광고를 삽입합니다.
seo-title: 댓글의 광고
solution: Experience Manager
title: 댓글의 광고
uuid: F 8 D 6372 F -4468-4884-A 384-116180 B 4 C 748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 댓글의 광고{#ads-in-comments}

댓글 스트림에 광고를 삽입합니다.

## 댓글의 광고 {#topic_CDD2ACF16AED4DE782725EE90089C04E}

댓글 스트림에 광고를 삽입합니다.

댓글 기능의 Livefyre 광고 기능을 사용하면 댓글 스트림에 광고를 삽입하고, 스트림에 광고가 표시되는 빈도를 정의하고, 동기 및 비동기 광고 삽입 위임 모두를 만들 수 있습니다.

Livefyre는 광고 관리 솔루션 공급자를 사용하여 광고를 삽입할 수 있는 컨테이너를 제공합니다.

광고를 주입하려면 Livefyre 두 값을 전달합니다.

* 댓글 스트림에 보급이 주입되어야 하는 빈도
* 적절한 광고를 제공하는 함수입니다.

>[!NOTE]
>
>광고는 광고 위치가 뷰포트에 있을 때에만 렌더링됩니다. 광고는 상위 댓글 (스레드 내 아님) 에만 표시되고 사용자는 이러한 광고에 대해 댓글을 달 수 없습니다. 이 API 에서는 광고가 배치될 요소의 크기를 지정할 수 없습니다.

## 통합 {#concept_C99029E618EC49779E3117D2C303E4F1}

이 기능을 사용하려면 광고가 배치될 페이지에 div 요소를 만든 다음 광고 공급자로부터 HTML를 전달합니다.

Livefyre는 다음 두 가지 광고 배치 유형을 제공합니다. 동기 및 비동기. 두 유형 모두 사용자가 페이지를 스크롤할 때만 광고를 로드하여 광고 위치가 보기에 있습니다. 두 가지 모두 DOM 요소 (iframe 또는 div) 를 반환해야 합니다.

광고를 획득하려면 동기식 메서드 호출이 로컬 리포지토리에 호출되지만 외부 서비스에 대한 비동기 호출은 호출되지 않습니다.

### 동기

동기 배치를 만들려면 광고에 광고를 포함시키고 광고 요소 자체를 반환합니다. 동기식 메서드 호출을 로컬 리포지토리에 호출하여 자체 광고 생성을 처리할 수 있습니다.

### 비동기

비동기 방법을 사용하려면 광고 공급자를 호출하기 전에 DOM에 요소가 삽입되어야 합니다. 그런 다음 제공업체는 전송할 광고를 결정하고 반환합니다.

비동기 광고를 구현하려면 광고가 배치될 요소를 반환하는 위임 및 광고 배치를 수행하는 콜백을 만듭니다. 대리점에서 반환되는 요소에는 타깃팅할 광고에 대한 고유 ID가 있어야 합니다. 콜백을 사용하면 고유한 ID가 제공하는 요소에 광고가 삽입됩니다.

>[!NOTE]
>
>광고 공급자에 따라 콜백이 다르게 동작합니다.

페이지가 로드되면, 주석의 광고가 위임, 요소를 주입한 다음, (이전에 정의한) 요소를 광고로 업데이트하는 콜백을 호출합니다.

## 매개 변수 {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

다음 매개 변수는 이 호출에서 사용할 수 있습니다.

광고 개체의 경우:

* **지연:****(선택 사항) 정수** - 첫 번째 광고가 표시될 주석 수를 설정합니다. 기본값은 10 입니다.
* **빈도: (선택 사항) 정수** - 이후의 각 광고가 표시될 주석 수를 설정합니다. 예를 들면 다음과 같습니다. 광고를 세 번째 댓글로 표시하려면 2를 입력합니다. 기본값은 10 입니다.
* **위임:*****필수* 함수** - 댓글 스트림에 광고를 주입하기 위해 호출된 함수입니다.

위임 개체는 동기 및 비동기 광고 호출을 모두 지원합니다. 위임 함수인 data에 지정되는 매개 변수는 다음을 포함합니다.

* **title:****문자열** - 컬렉션의 제목입니다.
* **태그:****배열** - 컬렉션과 연관된 태그의 목록입니다.
* **ID:****문자열** - 컬렉션의 아티클 식별자입니다.
* **URL:****문자열** - 컬렉션의 URL 입니다.
* **Networkid:****문자열** - 컬렉션의 네트워크 ID 입니다.
* **Siteid:****int** - 컬렉션의 사이트 ID 입니다.

이러한 항목은 예제의 Convconfig 개체를 통해 전달되며 [시작하기](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) 섹션에서 자세히 설명합니다.

### 동기

위임을 통해 다음을 포함한 개체가 반환됩니다.

* **요소:*****필수* DOM 요소** - 앱에 삽입할 광고가 포함된 요소입니다.

**비동기**: 위임을 통해 다음을 포함한 개체가 반환됩니다. 위임은 다음 두 개의 속성이 포함된 개체를 반환합니다. 요소 및 콜백:

* **요소:*****필수* DOM 요소** - 앱에 삽입할 광고가 포함된 요소입니다.
* **콜백:*****필수* 함수** - 위의 DOM 요소에 광고 삽입을 처리할 콜백입니다.

`Conv` 개체에 대해 광고 섹션의 제목을 나타내는 문자열을 전달할 수 있습니다.

* **문자열:****(선택 사항)** - 광고의 헤더 텍스트를 사용자 지정하는 데 사용됩니다. ' 스폰서'가 기본적으로 사용됩니다.

## 동기 예 {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## 비동기 예 {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
