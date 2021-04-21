---
description: Livefyre의 소셜 사용자 관리 시스템 사용
title: Livefyre ID
exl-id: 1e6149b6-dcdb-4e2a-a19d-06b24fe1288a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Livefyre ID 사용{#livefyre-identity}

사용자 지정 또는 타사 사용자 관리 시스템을 사용하는 경우 이 섹션을 건너뜁니다.

사용자는 소셜 미디어 계정 또는 사이트용으로 만들어진 이메일 기반 계정을 사용하여 앱에 로그인할 수 있습니다.

Livefyre ID 패키지에는 인증을 위임하는 데 필요한 정보가 들어 있습니다. (따라서 Livefyre ID에는 명시적 인증 위임이 필요하지 않습니다.)

Livefyre 통합에 소셜 사인온을 추가하려면:

1. 소셜 앱 만들기
1. Livefyre에 앱 연결
1. Livefyre.js를 페이지에 추가합니다.
1. Livefyre ID를 초기화합니다.

>[!NOTE]
>
>이 문서에서는 소셜 공급자의 앱 만들기 프로세스에 대한 Livefyre 특정 측면을 설명합니다. Livefyre는 인터페이스의 변경 사항에 대해 책임을 지지 않으며, Livefyre는 이러한 앱 제작 또는 승인 프로세스에 대한 지원을 제공할 수 없습니다. 사용 가능한 Twitter, Facebook, Yahoo! 및 Google 개발자 정보를 사용하여 이러한 앱을 만들고 승인 프로세스를 탐색하십시오(필요한 경우).
