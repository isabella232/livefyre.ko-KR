---
description: 사이트에서 Livefyre를 강화하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-description: 사이트에서 Livefyre를 강화하는 데 사용되는 핵심 Livefyre 라이브러리입니다.
seo-title: livefyre. js
solution: Experience Manager
title: livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# livefyre. js {#livefyre-js}

사이트에서 Livefyre를 강화하는 데 사용되는 핵심 Livefyre 라이브러리입니다.

`Livefyre.js` 는 모든 Livefyre 활성 웹 페이지에 설치할 수 있는 핵심 라이브러리입니다. 전역 `window.Livefyre` 개체 및 단일 공개 방법을 정의합니다. `Livefyre.require`이 방법은 Livefyre 앱을 임베드하는 데 [도움이 되는 다른 Livefyre JavaScript 라이브러리를 로드하는 데 사용할 수](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)있으며 [, 인증 제공업체는 Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 와 통합됩니다.

## 사이트에 추가 {#section_cst_twg_xz}

웹 페이지 또는 웹 사이트 템플릿에 다음 `<script>` 태그를 추가합니다. 가능한 경우 HTML 문서의 `<head>` 섹션에 추가하면 빠르게 로드됩니다.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>이 스크립트는 livefyre. js 라는 매우 작은 (~ 1 KB) 파일을 웹 페이지에 액세스한 프로토콜 (HTTP 또는 HTTPS) 에 대해 livefyre. js의 최신 버전을 로드하게 됩니다.

## Livefyre. require {#section_ipq_hwg_xz}

`Livefyre.require`[은 curl. js](https://github.com/cujojs/curl) 또는 [requirejs와 같은 사용자 지정 JavaScript 모듈 로더입니다](https://requirejs.org/). Livefyre에서 게시한 대부분의 패키지를 로드하는 데 사용할 수 있으며 편리하고 직관적인 통합 경로를 제공합니다.

액세스 `Livefyre.require` 가능한 패키지는 Semantic Versioning를 사용하여 [버전이 지정됩니다](https://semver.org/). 특정 버전 또는 여러 버전의 패키지에 패키지가 필요할 수 있으므로 새로운 버그 수정 기능을 통해 웹 페이지를 자동으로 이용할 수 있습니다. 이렇게 하면 사이트에서 Livefyre를 통합할 때 유연성이 높아집니다. 사용할 수 있는 버전 핀에는 세 가지 버전이 있습니다 `Livefyre.require`.

* **package-name # 1:** 주요 버전 v 1에 핀으로 고정합니다. 이전 버전과 호환되는 API를 유지하는 모든 새로운 업데이트를 이용할 수 있습니다. 주요 버전에 핀으로 고정하여 해당 버전에 대한 버그 수정 및 사소한 기능 개선 사항을 받을 수 있습니다.
* **package-name # 1.1:** 보조 버전 v 1.1에 핀으로 고정합니다. 이 보조 버전에 대한 모든 버그 수정이 표시됩니다. Livefyre 엔지니어링은 웹 페이지에서 예상치 못한 새로운 비헤이비어를 야기할 수 있는 기본 동작 또는 기능 범위가 변경될 경우 패키지의 보조 버전을 항상 돌립니다. 자동 버그 수정을 수신했지만 추가 기능이나 기본 비헤이비어를 변경하지 않으려면 보조 버전에 핀으로 고정합니다.
* **package-name # 1.1.1:** 패치 버전 v 1.1.1에 연결합니다. 버그 수정이 있더라도 이 포함의 동작은 변경되지 않습니다. 패키지의 마크업 구조를 변경하거나 실행 중인 Livefyre 버전이 어떤 방식으로든 변경되지 않을 다른 이유가 있는 경우 패치 버전에 핀으로 고정합니다.

사용 예는 다음과 `Livefyre.require` 같습니다.

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

어떤 Livefyre JavaScript 패키지를 통해 `Livefyre.require`사용할 수 있습니까? 언제든지 최신 버전의 지원되는 패키지 및 해당 최신 버전을 찾을 수 있습니다. [packages.html](https://cdn.livefyre.com/packages.html).

## 시험판 버전 테스트 테스트 {#section_pgm_dpg_xz}

경우에 따라 예정된 버전의 Livefyre 패키지를 테스트하여 웹 사이트에서 제대로 작동하도록 하거나 요청에 따라 개발 중인 기능을 허용할 수 있습니다. 의미론적 버전 범위를 포함하는 것 외에도 베타 버전 UAT 환경을 지정할 수 있습니다.

예를 들어, 다음을 위해서는 UAT 릴리스 `fyre.conv`, 댓글, 라이브 블로그 및 채팅 애플리케이션이 필요합니다.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
