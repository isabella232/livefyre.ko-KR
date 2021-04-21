---
description: GDPR 준비 개인 정보 보호 요청에 대한 FAQ에 대한 답변입니다.
title: 개인 정보 요청 FAQ
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# 개인 정보 요청 FAQ{#privacy-request-faqs}

GDPR 준비 개인 정보 보호 요청에 대한 FAQ에 대한 답변입니다.

* **사이트 방문자가 Livefyre 앱을 사용하는 사이트에서 추적되는 것을 어떻게 거부할 수 있습니까?** 사이트 방문자가 사이트를 옵트아웃할 때 고객 구현은 앱을 인스턴스화하기 전에 사용자가 옵트아웃했음을 Livefyre에 표시해야 합니다. Livefyre는 JavaScript 옵션인 `userPrivacyOptOut`을(를) 사용하여 이를 수행하는 방법을 만들었습니다. `userPrivacyOptOut` 사용 방법에 대한 자세한 내용은 [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)을 참조하십시오.

   `userPrivacyOptOut` 플래그가 true로 설정된 경우 페이지의 모든 앱은 쿠키 또는 다른 방법을 사용하여 Livefyre 서버로 데이터를 전송하지 않습니다. 그러면 Livefyre는 사이트 방문자를 추적하는 데 사용할 수 있는 데이터로 로컬 저장소를 업데이트할 수 없습니다. 소스가 프록시를 지원하지 않을 경우 사용자가 비디오를 클릭하고 해당 소스로부터 잠재적인 추적을 승인하지 않는 경우 Livefyre는 컨텐츠에 마스크를 표시합니다.

   Livefyre ID를 사용하는 경우 사용자는 자신의 프로필을 삭제하거나 사용자 계정에 대해 추적된 데이터 보고서를 만들 수 있습니다.

* **옵트아웃한 사이트 방문자로부터 향후 컨텐츠를 수집하지 못하도록 하려면 어떻게 해야 합니까?** Livefyre 앱 `userPrivacyOptOut`   `livefyre.js` 을 사용하는 웹 페이지에서 사용할 수 있습니다. `userPrivacyOptOut`에 대한 자세한 내용은 [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)을 참조하십시오.

* **앱 사용자 또는 소셜 계정 소유자에 대한 보고서를 생성하고 데이터를 삭제하려면 어떻게 해야 합니까?** [개인정보 ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 보호 요청에서 보고서를 생성하고 앱에서 사용자 데이터를 삭제합니다.

* **방문자의 모든 컨텐츠를 어떻게 제거합니까?** Livefyre는 Livecount 기능을 위해 사이트 방문자를 고유하게 식별하는 쿠키 형식을 제외하고는 사이트 방문자에 대한 지속적인 정보를 유지하지 않습니다. Liveccount는 사이트에 있는 방문자의 일시적 및 실시간 수입니다. 방문자가 쿠키를 떠나거나 삭제한 후에는 기록이 유지되지 않습니다.

   계정을 삭제하려면 [개인 정보 요청](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests)을(를) 만듭니다. Livefyre는 사용자 프로필 및 관련 레코드를 삭제하거나 익명으로 만듭니다.

* **등록된 사용자의 컨텐츠를 어떻게 제거합니까?** 계정을  [삭제하려면 ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 개인 정보 요청을 만듭니다. 사용자 프로필 및 관련 레코드는 완전히 삭제됩니다.

   >[!NOTE]
   >
   >이 작업은 실행 취소할 수 없습니다.

* **현재 직원 또는 이전 직원의 데이터 추적 보고서를 어떻게 생성합니까?** [개인 정보 ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) 보고서를 보고 사용자 계정에 대해 추적된 데이터 보고서를 생성합니다.

* **Livefyre 소셜 스트림이 준수됩니까?** 사용자가 소셜 네트워크에서 게시물 또는 트윗을 삭제하면 24시간 이내에 Livefyre의 모든 소스에서도 컨텐츠가 삭제됩니다. 이는 Twitter 및 Facebook에 적용됩니다.
