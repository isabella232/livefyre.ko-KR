---
description: Sidenotes 구성 개체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.
seo-description: Sidenotes 구성 개체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.
seo-title: Sidenotes 구성 옵션
solution: Experience Manager
title: Sidenotes 구성 옵션
uuid: 067 E 51 E 6-9720-4226-A 805-C 7 A 07 C 8 CDAA 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes 구성 옵션{#sidenotes-configuration-options}

Sidenotes 구성 개체는 Livefyre 앱이 페이지에서 렌더링하는 컨텐츠를 지정하는 데 사용되는 JSON 개체입니다.

개체에는 다음 매개 변수가 포함됩니다.

| 매개 변수 | type | 설명 |
|--- |--- |--- |
| Authdelegate | *필수* 개체 | 새 또는 이전 스타일 초기화된 인증 위임. |
| collectionmeta | *필수* 개체 | 자세한 내용은 Collectionmeta 토큰을 참조하십시오. |
| Customicon | *선택적* 문자열 | 사용자 정의 시작 아이콘의 URL를 설정합니다. 기본값은 Livefyre 버블입니다. |
| Customstyles | ** 선택적 개체 | 사용자 지정 스타일을 추가하여 Sidenotes의 모양과 느낌을 변경합니다. 자세한 내용은 사용자 지정 스타일을 참조하십시오. |
| Disablestream | *optional* boolean | true 인 경우 이 Sidenotes 인스턴스에서 실시간 스트리밍을 비활성화합니다 (다른 주석 스트림이 아님). 기본값은 false 입니다. |
| 환경 | *선택적* 문자열 | Livefyre UAT 환경을 지정합니다. 가능한 유일한 값은 `t402.livefyre.com`입니다. 프로덕션의 경우 이 매개 변수를 제거해야 합니다. |
| Iconvisibility | *선택적* 개체 또는 문자열 | 사이드나 정적일 때 Sidenotes 아이콘을 표시할지 여부를 정의합니다. 이 문자열이 문자열인 경우 두 버전 아이콘 (비어 있고 Sidenotes 포함) 에 모두 사용됩니다. 개체가 있으면 각 유형을 지정해야 합니다. {empty: ' hover ', num: ' static '} 입니다. 기본값은 정적입니다. |
| Inlinethreads | *optional* boolean | true 인 경우 관련 스레드가 연관된 블록 바로 다음에 삽입됩니다. 기본값은 false 입니다. |
| Numsidenotesel | *선택적* 개체, 문자열 또는 배열 | Sidenotes의 카운트 위젯이 장식할 요소를 지정합니다. (이 위젯은 페이지에 있는 sidenotes의 수와 sidenotes에 대한 정보를 보여줍니다.) 문자열 선택기에 두 개 이상의 요소가 일치하는 경우 첫 번째 요소가 선택됩니다. (CSS 3 DOM 선택기 사양을 사용합니다.) |
| position | *선택적* 문자열 | 활성화된 Sidenotes가 있는 요소를 클릭할 때 팝업의 위치를 결정합니다. 가능한 값은'smart ',' left ',' right ',' bottom'입니다. 기본값은 공간이 충분하지 않은 경우 (콘텐츠가 콘텐츠 아래로 이동할 경우) 페이지 오른쪽에 팝업을 정렬하는'스마트'입니다. |
| 선택기 | *필수* 개체, 문자열 또는 배열 | Launcher 아이콘이 표시될 요소를 지정합니다. (CSS 3 DOM 선택기 사양을 사용합니다.) 개체의 경우, 일치하는 항목에 CSS 선택기를 적용하고 제외와 일치하는 모든 요소를 제거하는 «포함» 섹션과 «제외» 섹션이 포함됩니다. 문자열에는 페이지에 일치하는 요소가 모두 포함됩니다. if array에 포함할 요소가 나열됩니다. |
| 문자열 | ** 선택적 개체 | 사용자 정의 텍스트 문자열을 추가하여 애플리케이션 전체에서 언어 또는 텍스트를 변경합니다. 자세한 내용은 사용자 지정 문자열을 참조하십시오. |
| Threadcontainerel | *선택적* 개체, 문자열 또는 배열 | Sidenotes의 스레드가 표시되는 요소를 지정합니다. 이 매개 변수를 사용하면 스레드의 위치를 변경할 수 있습니다. 문자열 선택기에 두 개 이상의 요소가 일치하는 경우 첫 번째 요소가 선택됩니다. (CSS 3 DOM 선택기 사양을 사용합니다.) |

