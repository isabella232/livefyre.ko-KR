---
description: Sidecotes 구성 객체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.
title: 사이드노트 구성 옵션
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# 사이드노트 구성 옵션{#sidenotes-configuration-options}

Sidecotes 구성 객체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.

객체에는 다음과 같은 매개 변수가 포함되어 있습니다.

| 매개 변수 | 유형 | 설명 |
|--- |--- |--- |
| authDelegate | ** requiremdobject | 새 스타일 또는 이전 스타일이 초기화된 인증 위임입니다. |
| collectionMeta | ** requiremdobject | 자세한 내용은 collectionMeta 토큰을 참조하십시오. |
| customIcon | ** 옵션_문자열 | 사용자 정의 시작 관리자 아이콘의 URL을 설정합니다. 기본값은 Livefyre 버블입니다. |
| customStyles | ** optionalobject | 사용자 정의 스타일을 추가하여 사이드노트의 모양과 느낌을 변경합니다. 자세한 내용은 사용자 지정 스타일을 참조하십시오. |
| disableStream | ** optionalBoolean | true이면 이 Sidecotes 인스턴스에서 실시간 스트리밍을 비활성화합니다(다른 주석 스트림에서는 아님). 기본값은 false입니다. |
| 환경에만 해당되는 결과를 반환합니다 | ** 옵션_문자열 | Livefyre UAT 환경을 지정합니다. 가능한 유일한 값은 `t402.livefyre.com`입니다. 프로덕션의 경우 이 매개 변수를 제거해야 합니다. |
| iconVisibility | ** optionalobject 또는 문자열 | 마우스로 가리키거나 정적으로 사이드노트 아이콘을 표시할지 여부를 정의합니다. 이 문자열이 문자열이면 두 버전의 블록 아이콘(비어 있고 사이드노트가 있음)에 사용됩니다. 객체가 있는 경우 각 유형을 지정해야 합니다.{비어 있음:&#39;hover&#39;, num:&#39;static&#39;}. 기본값은 정적입니다. |
| inlineThreads | ** 선택 사항 부울 | true이면 연결된 블록 바로 뒤에 Sidenote 스레드가 삽입됩니다. 기본값은 false입니다. |
| numSidecotesEl | *선택* 사항객체, 문자열 또는 배열 | 사이드노트 수 위젯이 장식할 요소를 지정합니다. (이 위젯은 페이지에 있는 사이드노트 수와 사이드노트에 대한 정보를 보여줍니다.) 문자열 선택기가 둘 이상의 요소와 일치하는 경우 첫 번째 요소가 선택됩니다. (CSS3 DOM 선택기 사양을 사용합니다.) |
| position | ** 옵션_문자열 | 사이드노트가 활성화된 요소를 클릭할 때 팝업의 위치를 결정합니다. 가능한 값은 &#39;smart&#39;, &#39;left&#39;, &#39;right&#39;, &#39;bottom&#39;입니다. 공간이 충분하지 않은 경우(컨텐츠의 아래로 이동할 경우) 팝업을 페이지의 오른쪽에 정렬하는 &#39;스마트&#39;가 기본값입니다. |
| 선택기 | ** requiredobject, string 또는 array | 실행 프로그램 아이콘을 표시할 요소를 지정합니다. (CSS3 DOM 선택기 사양을 사용합니다.) 개체의 경우 일치하는 모든 포함에 대해 CSS 선택기를 적용할 &quot;includes&quot; 섹션 및 &quot;excludes&quot; 섹션이 포함되며 제외와 일치하는 모든 요소를 제거합니다. 문자열인 경우, 페이지에 일치하는 모든 요소가 포함됩니다. 배열인 경우 포함할 요소를 나열합니다. |
| 문자열 | ** optionalobject | 사용자 정의 텍스트 문자열을 추가하여 애플리케이션 전체의 모든 언어 또는 텍스트를 변경합니다. 자세한 내용은 사용자 지정 문자열을 참조하십시오. |
| threadContainerEl | *선택* 사항객체, 문자열 또는 배열 | 사이드노트의 스레드가 표시되는 요소를 지정합니다. 이 매개 변수를 사용하면 스레드의 위치를 변경할 수 있습니다. 문자열 선택기가 둘 이상의 요소와 일치하는 경우 첫 번째 요소가 선택됩니다. (CSS3 DOM 선택기 사양을 사용합니다.) |
