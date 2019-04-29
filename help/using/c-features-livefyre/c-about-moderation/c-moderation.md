---
description: Livefyre 스팸 및 남용 필터링 엔진 (안전) 는 모든 수신 컨텐츠를 분석하는 백그라운드 프로세스이며 모든 Livefyre
  고객이 사용할 수 있습니다.
seo-description: Livefyre 스팸 및 남용 필터링 엔진 (안전) 는 모든 수신 컨텐츠를 분석하는 백그라운드 프로세스이며 모든 Livefyre
  고객이 사용할 수 있습니다.
seo-title: 안전한 규칙
title: 안전한 규칙
uuid: 2 F 91 D 0 D 4-DFFE -4651-88 AF -79 BBB 96 C 1 B 5 C
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 안전한 규칙{#safe-rules}

Livefyre 스팸 및 남용 필터링 엔진 (안전) 는 모든 수신 컨텐츠를 분석하는 백그라운드 프로세스이며 모든 Livefyre 고객이 사용할 수 있습니다.



SAFE는 패턴 규칙뿐만 아니라 스팸, 남용, 모욕 및 벌크 (반복) 게시물을 감지하는 통계 모델을 사용합니다. 다른 Livefyre 제품, 특히 컨텐츠 중재 도구와 MODQ에서 참조되는 것이 보입니다.

>[!NOTE]
>
>SAFE는 일괄 메일링 분류를 제외하고 영어로만 제공됩니다. 다른 언어에 대한 지원이 필요한 경우 전략 계정 관리자에게 문의하십시오.

## SAFE를 사용하는 Studio 구성 요소 {#section_k34_4tx_vy}

SAFE로 적용된 플래그는 다음 Studio 구성 요소와 함께 사용할 수 있습니다.

* 규칙

   안전 규칙을 정의하여 컨텐츠를 자동으로 플래그 지정하며 플래그가 지정된 컨텐츠가에서 **[!UICONTROL Network Settings]** 처리되는 방식을 정의할 수 있습니다.

   예를 들어, 사이트에서 비등방성에 대한 매우 낮은 허용치를 설정하고, 보조 (Bozo) 로 플래그가 지정된 모든 컨텐츠를 설정하는 보호 규칙을 정의할 수 있습니다. 다른 사이트에서는 스트림에 들어가기 전에 미리 중재되도록 Profane 컨텐츠를 설정하는 규칙을 정의할 수 있습니다.

* MODQ

   안전 규칙 및 기타 중재 규칙 (예: 스팸, 모욕 등) 로 플래그가 지정된 컨텐츠를 MODQ에서 중재할 수 있습니다.

* 라이브러리의 앱 컨텐츠

   SAFE로 플래그가 지정된 컨텐츠는 **[!UICONTROL Library]** 탭의 앱 컨텐츠에 나열됩니다. 콘텐츠를 중재하기 위해 플래그를 플래그로 필터링할 수 있습니다.

## SAFE Filter Options {#section_pg5_ttx_vy}

SAFE는 필터링된 컨텐츠에 다음 플래그를 적용하고 Livefyre Studio 내에서 규칙을 만들고 컨텐츠를 중재하는 데 사용할 수 있습니다.

* **[!UICONTROL Profanity List]** : 일반적인 사용에 따른 영어 키워드 목록으로 정의되는 위조 컨텐트.

   비속어 필터는 테스트된 단어 목록을 기반으로 Profane 언어를 찾습니다. 감지되면 컨텐츠에 Profane 플래그가 지정됩니다.

   >[!NOTE]
   >
   >또한 Livefyre는 사이트와 네트워크 수준에서 사용자 정의할 수 있는 두 번째 비등방성 목록 필터를 제공합니다. 비속어 목록으로 작성된 규칙은 안전한 비등방성 필터에서 파생된 자동화된 규칙보다 우선합니다. 자세한 내용은 설정 설명서의 비속어 목록 섹션을 참조하십시오.

* **[!UICONTROL Mild Profanity]** : 단어 및 구는 일반적으로 예의바른 대화에서 허용되지 않지만 일반적으로 평상시의 대화에서 허용됩니다. 일반적으로 이러한 단어 및 구문은 네트워크 TV에서 사용할 수 있습니다.
* **[!UICONTROL Strong Profanity]** : 네트워크 TV에서 허용되지 않는 느낌과 구문과 같은 매우 강력한 언어, R 등급 영화 및 장성케이블 TV 쇼에 불분명하게 사용되었습니다. 일반적으로 이러한 단어는 정중하거나 우연한 대화에서 사용되지 않으며, 청취자에게 피해를 줄 의도로 무례한 대화로 거론됩니다.
* **[!UICONTROL SPAM]** : 자발적인 컨텐트. 또한 다양한 기능 (주석 컨텐츠 및 URL 포함) 에 의존하는 통계적 모델을 사용하여 컨텐츠를 스팸으로 플래그를 지정합니다. 스팸 임계값을 조정하여 요청별로 네트워크 또는 사이트의 스팸 태그 지정 비율을 사용자 정의할 수 있습니다.
* **[!UICONTROL Mild Insult]** : 키워드 및 구문 패턴 목록이 정의한 대로 컨텐츠 모욕.
* **[!UICONTROL Strong Insult]** : 키워드 및 구문 패턴 목록이 정의한 대로 컨텐츠 모욕.
* **[!UICONTROL Hate Speech]** : 특히 대상 그룹 그룹이 소수이거나 보호를 받는 경우 민족성 또는 종교를 기반으로 한 모욕
* **[!UICONTROL ALL CAPS]** : 모든 대문자 (소리지르기) 로 표시된 텍스트입니다.
* **[!UICONTROL Mild Threat]** : 일반적으로 다른 사람이 만든 약간의 가벼운 모독 행위를 포함하는 위협 또는 모욕. 이 옵션은 가능한 위협을 보다 자주 표시하지만, 보다 긍정-긍정 비율이 높습니다 **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]** : 한 명 이상의 사람들에게 실행 가능한 신체 손상을 언급하는 심각한 위협 또는 모욕. 이 옵션은 가능한 위협을 덜 자주 표시하고, 보다 낮은 false-positive 비율을 표시합니다 **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]** : 차이가 있을 수 있는 이미지입니다. 이 옵션은 미약한 정도를 덜 자주 플래그로 플래그를 지정하지만 낮은 긍정 비율을 나타냅니다 **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]** : 차이가 있을 수 있는 이미지입니다. 이 옵션은 보다 자주 소문자로 표시되지만, 보다 긍정-긍정 비율이 높습니다 **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (개인 식별 정보): 사용자를 식별할 수 있는 정보입니다. 이메일 주소, 실제 주소, 주민등록번호 (미국 고객의 경우), 신용 카드 번호, 암호 또는 누군가의 신원을 얻기 위해 사용할 수 있는 모든 것을 포함할 수 있습니다.
* **[!UICONTROL Livefyre Recommends Trash]**. 자동화된 중재 권장 사항이 거부용 컨텐츠를 식별할 때 시스템이 수행하는 작업을 설정합니다. ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >중재 권장 사항을 켜려면 Adobe Livefyre 지원 전문가에게 문의하십시오.

## 안전하지 않은 컨텐츠 처리 {#section_pjy_5tx_vy}

이 필터에 의해 포착되지 않는 컨텐츠를 효과적으로 처리할 수 있는 방법에는 몇 가지가 있습니다. 아래 옵션은 권장되는 프로세스 순서로 나열되어 있습니다.

1. 중재자는 스트림에서 컨텐츠를 제거합니다.
1. 컨텐츠가 5 명의 사용자가 스팸이나 모욕으로 플래그가 지정된 경우 보조 (Bozo) 로 설정하면 플래그 규칙을 만듭니다.
1. 원하지 않는 컨텐츠를 게시하는 사용자를 금지하여 모든 콘텐츠가 Bozo 상태로 바로 이동합니다.
1. 항상 비속어 목록으로 필터링해야 하는 특정 단어를 추가할 수 있습니다.

>[!NOTE]
>
>중재자가 스팸 필터에 의해 포착된 컨텐츠를 게시하는 경우 여전히 스팸으로 플래그가 지정되지만 자동으로 승인되며 Bozo로 설정되지 않습니다.

컨텐츠가 안전하게 표시되지 않는 트렌드 또는 패턴을 발견하면 CSMS에 주석 ID 및 텍스트를 이메일로 전송합니다.



이 기능을 사용하는 앱:

* [회전판](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [채팅](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [댓글](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [미디어 담벼락](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [모자이크](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [평가](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [업로드 단추](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

