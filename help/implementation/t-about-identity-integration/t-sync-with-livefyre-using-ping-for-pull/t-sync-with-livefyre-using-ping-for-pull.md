---
description: 풀다운에 Ping를 사용하면 Livefyre를 사용자 관리 시스템과 동기화할 수 있습니다.
seo-description: 풀다운에 Ping를 사용하면 Livefyre를 사용자 관리 시스템과 동기화할 수 있습니다.
seo-title: Livefyre와 동기화 (풀다운에 Ping 사용)
solution: Experience Manager
title: Livefyre와 동기화 (풀다운에 Ping 사용)
uuid: 7 B 059064-1 CCA -46 D 7-8055-DFE 59 F 493 AC 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre와 동기화 (풀다운에 Ping 사용){#sync-with-livefyre-using-ping-for-pull}

풀다운에 Ping를 사용하면 Livefyre를 사용자 관리 시스템과 동기화할 수 있습니다.

일반적으로 웹 사이트/앱의 사용자가 언제든지 Livefyre ***를 ping 하면*** (표시 이름, 아바타 등) Livefyre가 해당 사용자의 업데이트된 프로필을 ***가져옵니다*** .

![](assets/Ping-for-Pull.png)

풀 시퀀스에 대한 Ping:

1. 고객은 Livefyre에 ping 요청을 보냅니다 (업데이트할 사용자를 포함).
1. Livefyre는 HTTP 200/Success의 Ping 수신을 확인합니다.
1. Livefyre는 당기기 요청을 처리합니다.
1. Livefyre 대기열이 요청을 풀링합니다.
1. Livefyre는 업데이트된 사용자 정보를 캡처하기 위해 종점에 가져오기 요청을 실행합니다.
1. 고객은 풀링 응답을 받고 유효성을 확인합니다.
1. Livefyre는 가져오기 끝점에 포함된 외부 프로필 정보로 원격 프로필을 업데이트합니다.

사용자가 프로필 정보를 업데이트할 때마다 Livefyre Ping. 풀 완료 시간 ping는 네트워크 로드에 따라 다를 수 있지만 1 분에서 10 분 사이의 사용자 정보를 업데이트합니다. Livefyre 스튜디오 > 사용자는 업데이트된 프로필 변경 사항을 먼저 표시합니다.

다음 두 개의 이벤트 후에 업데이트된 프로필 정보가 Livefyre 앱에 표시됩니다.

* 사용자가 로그아웃한 다음 다시 앱에 로그인합니다. Userauthtoken의 표시 이름 값이 가져오기 업데이트에 대한 ping 보다 우선합니다. 사용자 로그아웃/로그인이 토큰을 새로 고쳐 세션을 업데이트합니다.

   프로필 정보가 업데이트될 때 새 Userauthtoken를 생성하려면 SSO authdelegate를 사용하여 사용자를 다시 배경에 로그인합니다.

* 컬렉션에 대한 Bootstrap 업데이트는 업데이트된 정보를 가져옵니다 (대부분의 경우 5-10 분).

사용자 프로필 시스템에 대한 풀링을 구현하려면 다음을 수행하십시오.

1. [풀 끝점을 만듭니다](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >Livefyre 라이브러리에는 사용자 프로필을 최신 상태로 유지할 수 있는 syncuser 메서드가 포함되어 있습니다. Livefyre 라이브러리를 사용하는 경우 다음 두 단계를 건너뜁니다.

1. [Studio에서 풀 끝점을 등록합니다](#register_the_endpoint_with_studio).
1. [Ping](#t_build_the_ping)를 빌드합니다.
1. [풀 응답에 대한 Ping]를 빌드합니다.(# reference_ n 3 x_ pzb_ mz)
