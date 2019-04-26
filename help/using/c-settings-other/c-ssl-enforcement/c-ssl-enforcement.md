---
description: null
seo-description: null
seo-title: SSL 실행
solution: Experience Manager
title: SSL 실행
uuid: E 64 AF 8 C 2-3 AB 6-4034-B 385-0 E 552 D 828 C 6 E
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SSL 실행{#ssl-enforcement}

데이터를 안전하게 유지하기 위해 HTTPS를 사용하는 HTTP를 사용하지 않습니다. Adobe Livefyre는 모든 HTTP 및 비보안 SSL/TLS 암호를 2018 년 8 월말까지 완전히 비활성화합니다. 귀하 및 사용자의 개인 정보를 보호하기 위해 설계된 Adobe 표준입니다.

## 누가 영향을 받습니까? {#section_jf2_4yz_kcb}

다음과 같은 혜택을 제공하는 Livefyre 고객에게 영향을 줄 수 있습니다.

* CRM, CMS, Wordpress 또는 기타 클라이언트에서 서버 간 호출.
* 모바일 통합 (Android 및 iOS 앱)
* 맞춤형 애플리케이션 또는 맞춤형 코드

## 어떻게 해야 합니까? {#section_unv_dc5_kcb}

1. 모든 Livefyre 고객은 다음을 포함한 모든 트래픽에 대해 HTTPS를 통해 모든 API와 통신해야 합니다.

   * 서버 통합 (CRM, CMS, Wordpress 등)
   * 모바일 통합 (Android 및 iOS 앱)
   * 사용자 정의 애플리케이션 (Streamhub SDK 또는 직접 코딩됨).

1. 서버 및 모바일 HTTP 클라이언트에서 TLS 1.2를 지원해야 함
1. 호스트 이름을에서 `{*}.<network>.fyre.co``<network>.{*}.fyre.co`로 변경합니다. 예를 들어 호스트 이름이 `example.network.fyre.co``network.`example. fyre. co "로 변경됩니다. 예를 들면 다음과 같습니다.

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## 변경 내용을 적용했는지 어떻게 알 수 있습니까? {#section_sqk_5d5_kcb}

You may already use HTTPS, but livefyre recommended you have double check, 특히 if you have:

* CMS 또는 CRM에서 서버 간 호출.
* Javascript 또는 모바일에서 맞춤형 앱에 대한 SDK를 사용하거나 SDK를 사용합니다.
* 통합이 2 년 이상인 경우
* 스택의 기술이 1 년 이전의 기술입니다.

이미 HTTPS를 사용하고 있더라도 API 클라이언트가 TLS 1.2를 지원하는지 확인해야 합니다.

## 내 API 클라이언트가 TLS 1.2를 지원하는지 어떻게 확인할 수 있습니까? {#section_nd1_j25_kcb}

사이트 개발을 담당하는 사람은 다음을 수행할 수 있습니다.

* 클라이언트 소프트웨어 식별
* 버전을 확인합니다.
* API 클라이언트에서 TLS 1.2를 지원하는지 확인하려면 설명서를 참조하십시오.
* 필요한 경우 디버그 모드를 켭니다.

## TLS 1.2에 대한 Java 지원 {#section_lwn_rwk_ycb}

Java 8 이상 버전용 Oracle 및 openjdk jvms는 기본적으로 모든 SSL 연결에 대해 TLS 1.2를 사용하도록 구성되어 있습니다. Java 8 이상을 사용하는 경우 추가 조치를 취할 필요가 없습니다.

Java 7 또는 이전 버전 사용자는 TLS 1.2를 활성화하는 방법에 대한 공개 설명서를 참조하십시오.

## 호스트 이름을 변경해야 하는 이유는 무엇입니까? {#section_d5q_p25_kcb}

Livefyre에 `{*}.<network>.fyre.co` 도메인에 SSL 인증서가 없습니다. URL를 HTTPS로 변경하면 응용 프로그램이 중단됩니다.

## 최신 버전의 Livefyre SDK로 업그레이드해야 합니까? {#section_dw5_s25_kcb}

아니요. 대신 코드를 패치할 수 있습니다. 코드를 패치하려면 정적 문자열을 수정하고 코드를 다시 빌드합니다. HTTP 클라이언트가 만료된 경우 업그레이드하거나 다른 버전을 사용해야 합니다.

## 얼마나 걸립니까? {#section_lgd_v25_kcb}

이 시간이 걸리는 시간은 설정에 따라 다릅니다. 간단한 구현 작업이 있는 경우 확인하는 데 시간이 거의 걸리지 않습니다. 사용자 정의 기능이 많이 있는 경우 업데이트된 코드를 테스트하여 응용 프로그램 스토어에 새 응용 프로그램 또는 응용 프로그램 스토어에 배포해야 합니다. 최상의 결과를 얻을 수 있도록 작업물에 대한 초기 감사를 실시하는 것이 좋습니다.

## 이 작업을 완료하기 위한 타임라인은 무엇입니까? {#section_kgk_w25_kcb}

Livefyre는 2018 년 8 월말까지 Adobe 서비스에 포트 80 (HTTP) 를 비활성화하고 443 (HTTPS) 에 대한 연결만 지원합니다. HTTP를 사용하려는 브라우저 및 기타 클라이언트가 실패합니다.

## 이 작업을 언제까지 완료해야 합니까? {#section_rvb_x25_kcb}

모든 고객은 2018 년 7 월말까지 HTTPS를 사용해야 합니다. 이 마감일을 준수할 수 없는 경우 prioritysupport@livefyre.com로 문의하십시오.
