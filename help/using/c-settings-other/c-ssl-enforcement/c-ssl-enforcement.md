---
description: 'null'
seo-description: 'null'
seo-title: SSL 적용
solution: Experience Manager
title: SSL 적용
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 2%

---


# SSL 적용{#ssl-enforcement}

데이터를 안전하게 유지하기 위해 HTTPS를 선호하는 HTTP를 사용하지 않는 것입니다. Adobe Livefyre는 2018년 8월 말까지 모든 HTTP 및 비보안 SSL/TLS 암호를 완전히 비활성화합니다. 이는 사용자와 사용자의 개인 정보를 보호하기 위해 고안된 Adobe 표준입니다.

## 누가 영향을 받습니까?{#section_jf2_4yz_kcb}

다음과 같은 Livefyre 고객에게 영향을 줄 수 있습니다.

* CRM, CMS, WordPress 또는 기타 클라이언트에서 서버 간 호출을 수행할 수 있습니다.
* 모바일 통합(Android 및 iOS 앱)
* 사용자 정의 애플리케이션 또는 사용자 정의 코드

## 해야 할 일{#section_unv_dc5_kcb}

1. 모든 Livefyre 고객은 다음을 포함한 모든 트래픽에 대해 HTTPS를 통해 모든 API와 통신해야 합니다.

   * 서버 간 통합(CRM, CMS, WordPress 등)
   * 모바일 통합(Android 및 iOS 앱)
   * 사용자 지정 응용 프로그램(Streamhub SDK 또는 직접 코딩됨).

1. 서버 간 서버 및 모바일 HTTP 클라이언트는 TLS 1.2를 지원해야 합니다.
1. 호스트 이름을 `{*}.<network>.fyre.co`에서 `<network>.{*}.fyre.co`(으)로 변경합니다. 예를 들어 호스트 이름 `example.network.fyre.co`이 `network.`example.fyre.co&quot;로 변경됩니다. 예:

   * `bootstrap.<network_name>.fyre.co` 에서 `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` 에서 `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` 에서 `<network_name>.admin.fyre.co`

## 변경 여부를 어떻게 알 수 있습니까?{#section_sqk_5d5_kcb}

이미 HTTPS를 사용하고 있지만, 특히 다음과 같은 경우 다시 확인하는 것이 좋습니다.

* CMS 또는 CRM에서 서버 간 호출
* 사용자 지정 코드 또는 Javascript 또는 Mobile의 사용자 지정 앱에 SDK를 사용합니다.
* 통합이 1년 이상 된 경우.
* 스택에 있는 기술이 1년 이상 오래된 경우

이미 HTTPS를 사용하고 있더라도 API 클라이언트가 TLS 1.2를 지원하는지 확인해야 합니다.

## 내 API 클라이언트가 TLS 1.2를 지원하는지 어떻게 확인할 수 있습니까?{#section_nd1_j25_kcb}

사이트 개발에 종사하는 사람은 다음을 수행할 수 있습니다.

* 클라이언트 소프트웨어를 확인합니다.
* 버전을 식별합니다.
* API 클라이언트가 TLS 1.2를 지원하는지 확인하려면 설명서를 참조하십시오.
* 필요한 경우 디버그 모드를 설정합니다.

## TLS 1.2에 대한 Java 지원 {#section_lwn_rwk_ycb}

Java 8 이상용 oracle 및 OpenJDK JVM은 기본적으로 모든 SSL 연결에 대해 TLS 1.2를 사용하도록 구성되어 있습니다. Java 8 이상을 사용하는 경우 추가 조치를 취할 필요가 없습니다.

Java 7 이전 버전의 사용자는 TLS 1.2를 활성화하는 방법에 대한 공개 설명서를 참조하십시오.

## 호스트 이름을 변경해야 하는 이유는 무엇입니까?{#section_d5q_p25_kcb}

Livefyre에는 `{*}.<network>.fyre.co` 도메인에 SSL 인증서가 없습니다. URL을 HTTPS로 변경하면 응용 프로그램이 중단됩니다.

## 최신 버전의 Livefyre SDK로 업그레이드해야 합니까?{#section_dw5_s25_kcb}

아니요. 대신 코드를 패치할 수 있습니다. 코드를 패치하려면 일부 정적 문자열을 수정하고 코드를 다시 작성합니다. HTTP 클라이언트가 최신 상태가 아니면 업그레이드하거나 다른 클라이언트를 사용해야 합니다.

## 얼마나 걸리나요?{#section_lgd_v25_kcb}

이 시간이 걸리는 시간은 설정에 따라 다릅니다. 간단한 구현을 통해 확인하는 데 시간이 거의 걸리지 않습니다. 많은 사용자 정의 사항이 있는 경우 업데이트된 코드를 테스트하고 서버 또는 새 앱을 앱 스토어에 배포해야 합니다. 최상의 결과를 위해 장기 작업을 계획할 수 있도록 작업물에 대한 초기 감사를 수행하는 것이 좋습니다.

## 이 작업을 완료하는 데 필요한 타임라인은 무엇입니까?{#section_kgk_w25_kcb}

Livefyre는 2018년 8월 말까지 Adobe 서비스에 대한 포트 80(HTTP)을 비활성화하고 443(HTTPS)으로의 연결만 지원합니다. HTTP를 사용하려고 하는 브라우저 및 기타 클라이언트는 실패합니다.

## 이 일은 언제 끝내야 하나요?{#section_rvb_x25_kcb}

모든 고객은 2018년 7월 말까지 HTTPS를 사용해야 합니다. 이 마감일을 충족시킬 수 없는 경우 Adobe 팀(prioritysupport@livefyre.com)에 문의하십시오.
