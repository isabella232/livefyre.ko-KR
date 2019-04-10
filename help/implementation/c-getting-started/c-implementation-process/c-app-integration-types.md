---
description: Livefyre 앱을 구현할 때 구현 스타일은 사용 사례에 따라 다릅니다. 이 페이지에서는 앱을 만들 수 있는 세 가지 방법에
  대해 설명합니다.
seo-description: Livefyre 앱을 구현할 때 구현 스타일은 사용 사례에 따라 다릅니다. 이 페이지에서는 앱을 만들 수 있는 세 가지
  방법에 대해 설명합니다.
seo-title: CMS 앱 통합
solution: Experience Manager
title: CMS 앱 통합
uuid: 14 fd 7 e 36-0 e 50-4 ae 3-97 f 0-2 de 731 c 184 f 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# CMS 앱 통합{#cms-app-integrations}

Livefyre 앱을 구현할 때 구현 스타일은 사용 사례에 따라 다릅니다. 이 페이지에서는 앱을 만들 수 있는 세 가지 방법에 대해 설명합니다.

Livefyre 통합은 모든 CMS 및 사용자 프로파일 및 인증 플랫폼과 무관합니다. 사용 사례와 요구 사항에 따라 하나 이상의 방법으로 Livefyre를 구현합니다.

기존 통합을 사용하여 사용자 지정 AEM 구성 요소를 만들 수 있습니다.

## CMS 앱 통합 유형 개요

| type | 개발 요구 사항 | 기능 | 전문가 | 제한 사항 |
|--- |--- |--- |--- |--- |
| App Designer | 매우 낮음 | 개발자 <br>제한 스타일링과 사용 가능한 </br>구성 사용 사례 없이 페이지에 추가할 JS를 Studio에 만듭니다. 단일 사용 페이지 (이벤트 커버리지, 캠페인, 허브) | 앱을 신속하게 시작할 수 있습니다. <br>구성은 기술 지식이 없는 구성원이 수행할 수 있습니다. <br>신속하게 구성 변경 | Livefyre Studio를 사용하여 먼저 앱을 <br>제작해야 하는 경우 |
| livefyre. js | MEDIUM | 페이지 사용 <br>사례: 재사용 가능한 템플릿 (편집 컨텐츠, 제품 평가) | 전체 앱 맞춤화 및 구성 <br>기능을 사용하면 CMS 내에서 앱을 동적으로 인스턴스화하는 프로세스를 자동화할 수 있습니다. | 개발자의 요구 사항 충족 |
| SDK API | 고급 | Livefyre에서 사용자 정의 애플리케이션에 <br>사용할 컨텐츠를 검색하면 지원되는 서비스 제공 <br>사례 이외의 프런트 엔드에서 맞춤화할 수 있습니다. 데이터/분석 통합 및 맞춤형 프런트 엔드 앱 | 앱의 모양과 느낌을 완벽하게 강화 | 개발이 필요합니다. <br>구현에 대한 높은 수준의 개발 노력. |