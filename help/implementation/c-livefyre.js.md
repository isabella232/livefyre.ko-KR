---
description: 사이트에서 Livefyre의 강력한 기능을 제공하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

사이트에서 Livefyre의 강력한 기능을 제공하는 데 사용되는 핵심 Livefyre 라이브러리입니다.

`Livefyre.js` 는 Livefyre가 활성화된 모든 웹 페이지에 설치할 수 있는 핵심 라이브러리입니다. 전역 `window.Livefyre` 개체 및 단일 공개 메서드 `Livefyre.require`를 정의합니다. 이 메서드는 [Livefyre 앱 포함](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [인증 공급자를 Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 등과 통합하는 데 도움이 되는 다른 Livefyre JavaScript 라이브러리를 로드하는 데 사용할 수 있습니다.

## 사이트 {#section_cst_twg_xz}에 추가

다음 `<script>` 태그를 웹 페이지 또는 웹 사이트 템플릿에 추가합니다. 가능한 경우 HTML 문서의 `<head>` 섹션에 추가하여 빠르게 로드합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>이 스크립트는 Livefyre.js 스카우트라는 매우 작은(~1Kb) 파일을 포함하게 되며 이 경우 나중에 웹 페이지가 액세스된 프로토콜(HTTP 또는 HTTPS)에 최신 버전의 Livefyre.js를 로드합니다.

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` 은  [curl.jsorRequireJS](https://github.com/cujojs/curl) 와 같은 사용자 지정 JavaScript 모듈  [로더입니다](https://requirejs.org/). Livefyre에서 게시한 대부분의 패키지를 로드하고 편리하고 직관적인 통합 경로를 제공하는 데 사용할 수 있습니다.

`Livefyre.require`을(를) 통해 액세스할 수 있는 패키지는 [의미 체계 버전 관리](https://semver.org/)를 사용하여 버전이 지정됩니다. 패키지는 특정 버전 또는 다양한 버전으로 필요할 수 있으므로 웹 페이지는 새로운 버그 수정 기능을 자동으로 활용할 수 있습니다. 이렇게 하면 사이트에서 Livefyre를 통합할 때 유연하게 대처할 수 있습니다. `Livefyre.require`에 사용할 수 있는 버전 핀의 3가지 수준이 있습니다.

* **package-name#1:** 주 버전 v1에 고정합니다. 이전 버전과 호환되는 API를 유지 관리하는 모든 새로운 업데이트가 제공됩니다. 해당 버전에 대한 버그 수정 및 사소한 기능 개선 사항을 받으려면 주요 버전에 고정하십시오.
* **package-name#1.1:** 부 버전 v1.1에 고정합니다. 이 부 버전에 대한 모든 버그 수정이 표시됩니다. 기본 동작이나 기능 범위가 변경되면 Livefyre 엔지니어링에서는 웹 페이지에 예기치 않은 새로운 동작을 발생시킬 수 있는 방식으로 패키지의 부 버전을 항상 충돌합니다. 자동 버그 수정을 받으려 하지만 추가 기능이나 기본 동작에 대한 변경 사항이 없는 경우 부 버전에 고정합니다.
* **package-name#1.1.1:** 패치 버전 v1.1.1에 고정합니다. 버그 수정이 있는 경우에도 이 포함 동작은 변경되지 않습니다. 변경할 수 있는 패키지의 마크업 구조에 따라 사이트에 대한 광범위한 CSS 사용자 지정이 있거나 실행 중인 Livefyre 버전이 변경되지 않도록 해야 할 다른 이유가 있는 경우 패치 버전에 고정합니다.

`Livefyre.require`을(를) 사용한 통합 예는 다음과 같습니다.

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## 사용 가능한 패키지 {#section_ygd_dwg_xz}

`Livefyre.require`을(를) 통해 사용할 수 있는 Livefyre JavaScript 패키지가 궁금하십니까? 지원되는 패키지의 최신 목록과 최신 버전은 다음과 같이 항상 참조할 수 있습니다.[packages.html](https://cdn.livefyre.com/packages.html).

## {#section_pgm_dpg_xz} 패키지의 시험판 버전 테스트

Livefyre 패키지의 향후 버전을 테스트하여 웹 사이트에서 제대로 작동하는지 확인하거나 요청에 따라 개발 중인 기능을 수락할지 여부를 테스트할 수 있습니다. 의미 버전 범위를 포함하는 것 외에도 베타 버전 UAT 환경을 지정할 수 있습니다.

예를 들어 다음은 `fyre.conv`, 댓글, 라이브 블로그 및 채팅 애플리케이션의 UAT 릴리스를 필요로 하는 경우입니다.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
