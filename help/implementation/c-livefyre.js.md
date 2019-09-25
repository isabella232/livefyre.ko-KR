---
description: 사이트에서 Livefyre를 지원하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-description: 사이트에서 Livefyre를 지원하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

사이트에서 Livefyre를 지원하는 데 사용되는 핵심 Livefyre 라이브러리입니다.

`Livefyre.js` 는 Livefyre가 활성화된 모든 웹 페이지에 설치할 수 있는 핵심 라이브러리입니다. 전역 `window.Livefyre` 개체와 단일 공개 방법을 정의합니다. `Livefyre.require`이 메서드는 Livefyre 앱 임베드, [Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)와 인증 [공급자 통합 등과 관련된 다른 Livefyre JavaScript 라이브러리를 로드하는 데 사용할 수](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 있습니다.

## 사이트에 추가 {#section_cst_twg_xz}

웹 페이지 또는 웹 사이트 템플릿에 다음 `<script>` 태그를 추가합니다. 가능하면 HTML 문서의 `<head>` 섹션에 추가하여 빠르게 로드합니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>이 스크립트는 Livefyre.js라는 매우 작은 파일(~1Kb)을 임베드하여 이후 웹 페이지가 액세스된 프로토콜(HTTP 또는 HTTPS)에 최신 버전의 Livefyre.js를 로드합니다.

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` 은 curl.js 또는 RequireJS와 같은 사용자 지정 [JavaScript](https://github.com/cujojs/curl) 모듈 [로더입니다](https://requirejs.org/). Livefyre에서 게시한 대부분의 패키지를 로드하고 편리하고 직관적인 통합 경로를 제공하는 데 사용할 수 있습니다.

를 통해 액세스할 수 `Livefyre.require` 있는 패키지는 의미 체계 버전 관리를 [통해 실행됩니다](https://semver.org/). 패키지는 특정 버전 또는 다양한 버전에 필요할 수 있으므로 웹 페이지에서 새로운 버그 수정 기능을 자동으로 활용할 수 있습니다. 이를 통해 사이트에서 Livefyre를 통합할 때 유연성을 얻을 수 있습니다. 사용할 수 있는 버전 핀의 세 가지 수준이 `Livefyre.require`있습니다.

* **** package-name#1:주 버전 v1에 고정합니다. 이전 버전과 호환되는 API를 유지 관리하는 모든 새로운 업데이트가 제공됩니다. 주요 버전에 고정하여 해당 버전에 대한 버그 수정 및 사소한 기능 개선 사항을 받을 수 있습니다.
* **** package-name#1.1:부 버전 v1.1에 고정합니다.이 보조 버전에 대한 모든 버그 수정을 받을 수 있습니다. Livefyre Engineering은 기본 동작이나 기능 범위가 변경되면 웹 페이지에서 예기치 않은 새로운 동작을 발생시킬 수 있는 방식으로 패키지의 부 버전을 항상 혹사합니다. 자동 버그 수정을 받지만 추가 기능이나 기본 동작에 대한 변경 사항이 없는 경우 보조 버전에 고정합니다.
* **** package-name#1.1.1:패치 버전 v1.1.1에 고정합니다.버그 수정이 있는 경우에도 이 임베드 동작은 변경되지 않습니다. 변경할 수 있는 패키지의 마크업 구조에 따라 사이트에 대한 광범위한 CSS 사용자 지정이 있거나 실행 중인 Livefyre 버전이 변경되지 않도록 선호하는 다른 이유가 있는 경우 패치 버전에 고정합니다.

를 사용한 통합 예는 다음과 `Livefyre.require` 같습니다.

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

어떤 Livefyre JavaScript 패키지를 사용할 수 있는지 `Livefyre.require`궁금하십니까? 지원되는 최신 패키지 및 최신 버전 목록은 항상 여기에서 찾을 수 있습니다. [packages.html](https://cdn.livefyre.com/packages.html).

## 패키지의 시험판 버전 테스트 {#section_pgm_dpg_xz}

경우에 따라 Livefyre 패키지의 향후 버전을 테스트하여 웹 사이트에서 제대로 작동하는지 확인하거나 요청에 따라 개발 중인 기능을 수락할지 여부를 테스트할 수 있습니다. 의미 체계 버전 범위를 포함하는 것 외에도 베타 버전 UAT 환경을 지정할 수 있습니다.

예를 들어, 다음은 Comments, Live Blog 및 Chat 응용 프로그램의 UAT 릴리스를 필요로 `fyre.conv`하는 경우입니다.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
