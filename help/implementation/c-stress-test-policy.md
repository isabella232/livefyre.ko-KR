---
description: Livefyre 플랫폼을 기반으로 스트레스 테스트를 실시합니다.
seo-description: Livefyre 플랫폼을 기반으로 스트레스 테스트를 실시합니다.
seo-title: 스트레스 테스트 정책
solution: Experience Manager
title: 스트레스 테스트 정책
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 스트레스 테스트 정책{#stress-test-policy}

Livefyre 플랫폼을 기반으로 스트레스 테스트를 실시합니다.

이 문서에서는 Livefyre 플랫폼에 대한 스트레스 테스트 실행에 대한 지침을 제공합니다. 통보 없이 고객의 애드혹 테스트는 엄격하게 금지됩니다. [금지 및 허용된 활동에](#c_stress_test_policy/section_mhs_bfz_vdb)대한 자세한 내용을 살펴보십시오.

>[!NOTE]
>
>스트레스 테스트는 선택 사항입니다. You are not required or expected to perform a stress test. Adobe Livefyre는 릴리스 프로세스의 일부로 정기적인 스트레스 테스트와 유효성 검사를 수행합니다. 테스트를 실행하도록 선택한 경우 이 문서에서는 스트레스 테스트를 수행하기 위한 요구 사항과 제한 사항을 간략히 설명합니다.

## notification {#section_ihs_bfz_vdb}

계획을 수립하기 전에 Livefyre 고객 성공 전문가와 Adobe 기술 컨설턴트에게 미리 3 주 이상 미리 알려야 합니다.

Livefyre에게 알리려면 Livefyre 고객 성공 전문가 및 Adobe 기술 컨설턴트에 다음 정보를 제출하십시오.

* 테스트의 목적 및 설명
* 사용 사례
* 테스트에 사용하려는 Livefyre API 목록
* 테스트의 날짜, 시간 및 기간
* 테스트를 시작할 IP 주소

## 요구 사항 {#section_khs_bfz_vdb}

다음 요구 사항을 충족하는 경우에만 테스트를 수행할 수 있습니다.

* 테스트를 시작하기 전에 Adobe 기술 컨설턴트로부터 서면 서면 승인을 받아야 합니다.
* **UAT 네트워크에서만 테스트를 수행할 수 있습니다.**
* 현실적인 시나리오에 대해 테스트해야 합니다. 예를 들어, 이것은 현실적인 시나리오가 아니기 때문에 귀하의 속성이 *매일 수백만* 건의 POST 요청을 서비스한다고 가정해서는 안됩니다. 시나리오가 사실인지 여부를 결정하는 데 도움이 필요한 경우 Livefyre 고객 성공 전문가 또는 Adobe 기술 컨설턴트에게 문의하십시오.
* 태평양 표준시 표준 시간대\ (UTC -7\) 에 대해 업무 시간 중에 테스트를 수행해야 합니다.
* 테스트를 위한 데이터와 근거를 만들어야 할 수 있습니다.

## 거버넌스 {#section_mhs_bfz_vdb}

테스트를 수행하는 경우 Livefyre는 언제든지 테스트를 종료할 권한을 가집니다.

* 프로덕션 네트워크에서
* Adobe 기술 컨설턴트의 서면 서면 승인 없이 3 주 이상 사전 승인
* 비정품 시나리오

Livefyre는 API에 대한 액세스를 차단하고, Livefyre 네트워크를 비활성화하고, 요구 사항을 충족하지 않을 경우 부하 테스트 요청을 거부하여 테스트를 종료합니다.
