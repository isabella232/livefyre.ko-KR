---
description: GDPR 지원 개인 정보 보호 요청에 대한 FAQ에 대한 답변입니다.
seo-description: GDPR 지원 개인 정보 보호 요청에 대한 FAQ에 대한 답변입니다.
seo-title: 개인 정보 요청 FAQ
solution: Experience Manager
title: 개인 정보 요청 FAQ
uuid: 0 CD 6 F 0 D 2-504 D -46 E 9-AC 46-070536 CDA 086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 개인 정보 요청 FAQ{#privacy-request-faqs}

GDPR 지원 개인 정보 보호 요청에 대한 FAQ에 대한 답변입니다.

* **사이트 방문자가 Livefyre 앱을 사용하는 사이트에서 추적을 거부할 수 있는 방법은 무엇입니까?** 사이트 방문자가 옵트아웃하면, 고객 구현은 앱을 인스턴스화하기 전에 사용자가 옵트아웃했음을 Livefyre에 명시해야 합니다. Livefyre는 JavaScript 옵션을 사용하여 이 작업을 수행할 수 `userPrivacyOptOut`있는 방법을 만들었습니다. 사용 `userPrivacyOptOut`방법에 대한 자세한 내용은 [Userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)를 참조하십시오.

   `userPrivacyOptOut` 플래그가 true로 설정되면 페이지의 모든 앱은 쿠키 또는 다른 방법을 사용하여 Livefyre 서버로 데이터를 전송하지 않습니다. 그런 다음 Livefyre는 사이트 방문자를 추적하는 데 사용할 수 있는 데이터로 로컬 저장소를 업데이트하지 않습니다. 소스에서 프록시를 지원하지 않는 경우 사용자가 비디오를 클릭해서 해당 소스에서 잠재적 추적을 승인하지 않으면 Livefyre가 컨텐츠에 마스크를 표시합니다.

   Livefyre ID를 사용하는 경우 사용자는 프로필을 삭제하거나 사용자 계정에 대해 추적된 데이터 보고서를 만들 수 있습니다.

* **옵트아웃한 사이트 방문자의 향후 컨텐츠 수집을 방지하는 방법은 무엇입니까?** Livefyre `userPrivacyOptOut` 앱을 `livefyre.js` 사용하는 웹 페이지에서 사용할 수 있습니다. 에 대한 `userPrivacyOptOut`자세한 내용은 [Userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)를 참조하십시오.

* **어떻게 보고서를 생성하고 앱 사용자 또는 소셜 계정 소유자에 대한 데이터를 삭제합니까?**[개인정보 보호 요청을](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 사용하여 앱에서 보고서 생성 및 사용자 데이터 삭제.

* **방문자에 대한 모든 컨텐츠를 제거하려면 어떻게 해야 합니까?** Livecfyre는 Livecount 기능에 대해 고유하게 식별할 수 있는 쿠키 형태를 제외하고는 사이트 방문자에 대한 지속적인 정보를 유지 관리하지 않습니다. Livecount는 사이트에서 방문자의 일시적 및 실시간 수입니다. 방문자가 쿠키를 떠나거나 지운 후에는 내역이 유지됩니다.

   계정을 삭제하는 [개인 정보 요청을](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 만듭니다. Livefyre는 사용자 프로필 및 관련 레코드를 삭제하거나 익명으로 만듭니다.

* **등록된 사용자의 컨텐츠를 제거하려면 어떻게 해야 합니까?** 계정을 삭제하는 [개인 정보 요청을](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 만듭니다. 사용자 프로필 및 관련 레코드는 완전히 제거됩니다.

   >[!NOTE]
   >
   >이 작업은 실행 취소할 수 없습니다.

* **현재 또는 이전 직원의 데이터 보고서를 작성하는 방법은 무엇입니까?**[개인 정보 보고서를](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) 보고 사용자 계정에 대해 추적된 데이터 보고서를 생성합니다.

* **Livefyre는 소셜 스트림 규정을 준수합니까?** 사용자가 소셜 네트워크에서 게시물 또는 트윗을 삭제하면 24 시간 이내에 Livefyre의 모든 소스에서 컨텐츠가 삭제됩니다. Twitter 및 Facebook에 적용됩니다.

