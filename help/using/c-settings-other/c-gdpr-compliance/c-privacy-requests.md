---
description: Livefyre에서 개인정보 보호 요청을 만듭니다.
title: 개인 정보 요청 만들기
exl-id: 117e1edb-becd-45f2-bfe5-12fb19ad01e0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# 개인 정보 요청 만들기{#create-a-privacy-request}

Livefyre에서 개인정보 보호 요청을 만듭니다.

사용자의 모든 데이터를 삭제하고, 사용자에 대한 모든 데이터의 보고서를 생성하고, 이 프로세스를 사용하여 옵트인 또는 옵트아웃 변경을 수행합니다.

사용자를 검색 및 찾고 해당 컨텐츠에 대한 보고서를 생성하려면 다음을 수행합니다.

1. **[!UICONTROL Settings > Privacy]**&#x200B;으로 이동한 다음 **[!UICONTROL Create Request]**&#x200B;을 클릭합니다.

   ![](assets/privacypage1.png)

1. **[!UICONTROL Submit Request]** 창에 정보를 입력합니다.

   * **[!UICONTROL Reference Id]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 나중에 참조할 수 있도록 사용할 식별자를 입력합니다. 예를 들어 텍스트, 티켓 번호, URL, 이메일 주소 또는 최대 255자의 기타 문자열을 추가할 수 있습니다
   * **[!UICONTROL Type]**

      * **액세스 권한**. 계정과 관련된 모든 사용 가능한 데이터를 수집합니다. 암호 또는 소셜 자격 증명과 같은 민감한 세부 사항은 난독화되거나 생략됩니다.

      * **삭제**. 계정과 관련된 모든 데이터를 삭제하거나 난독화합니다. **이 옵션을 선택하고 [제출]을 클릭하면 이 작업을 반전하거나 취소할 수 없으며  *삭제된 데이터를 복구할 수 없습니다.*** 계정이 Livefyre Studio 사용자의 계정인 경우 일부 데이터는 보존되어 비즈니스 레코드의 무결성을 유지합니다.

         >[!IMPORTANT]
         >
         >계정에 대한 데이터를 삭제하면 계정과 관련된 데이터가 영구적으로 삭제되거나 삭제됩니다. 이 작업은 되돌릴 수 없으며, 삭제한 후에는 데이터를 복구할 수 없습니다.

      * **옵트아웃**. Streams 또는 소셜 검색을 통해 Livefyre가 소셜 계정에서 데이터 또는 컨텐츠를 수동적으로 수집하지 못하도록 합니다. 옵트인 및 옵트아웃은 등록된 사용자에게 적용되지 않습니다.
      * **옵트인**. Livefyre를 다시 사용하면 이전에 Streams 또는 소셜 검색을 통해 옵트아웃한 소셜 계정에서 데이터나 컨텐츠를 수동적으로 수집할 수 있습니다. 옵트인 및 옵트아웃은 등록된 사용자에게 적용되지 않습니다.

      ![](assets/privacypage2.png)

   * **[!UICONTROL Identifier Type]** 및 **[!UICONTROL Identifier]**

      * **[!UICONTROL User Account]**

         * 사용자 관리 시스템 또는 Livefyre의 Studio 사용자 식별자로 생성된 사용자 계정 ID로 등록된 사용자의 계정을 식별합니다. **Livefyre** **사용자 설정**&#x200B;이나 **자산 라이브러리** 또는 **앱 컨텐츠**&#x200B;에 있는 내용의 세부 정보에서 사용자의 사용자 계정 ID를 찾을 수도 있습니다.

         * 허용된 값:최대 255자 영숫자 문자열. 이메일 주소가 올바른 입력이 아닙니다.
      * **[!UICONTROL Facebook User]**

         * facebook에서 제공한 숫자 ID로 계정을 식별합니다. 요청자가 이것을 제공해야 합니다. 숫자 Facebook ID [여기에서 ](https://www.facebook.com/help/1397933243846983?helpref=faq_content)을 찾는 방법에 대한 지침을 찾을 수 있습니다.
         * 허용된 값:6-16자 숫자
      * **[!UICONTROL Instagram User]**

         * instagram에서 제공한 숫자 ID로 계정을 식별합니다. 요청자가 이것을 제공해야 합니다. 온라인으로 검색하여 Instagram 계정에서 숫자 Instagram ID를 찾는 방법에 대한 지침을 찾을 수 있습니다
         * 허용된 값:5-16자 숫자
      * **[!UICONTROL Twitter User]**

         * twitter에서 제공한 숫자 ID로 계정을 식별합니다. 개인 정보 변경을 요청하는 사람이 제공해야 합니다. 온라인으로 검색하여 Twitter 계정의 숫자 Twitter ID를 찾는 방법에 대한 지침을 찾을 수 있습니다
         * 허용된 값:5-16자 숫자
      * **[!UICONTROL YouTube User]**

         * YouTube에서 제공한 숫자 ID로 계정을 식별합니다. 개인 정보 변경을 요청하는 사람이 제공해야 합니다. YouTube 계정 [여기](https://support.google.com/youtube/answer/3250431?hl=en)에서 숫자 YouTube ID를 찾는 방법에 대한 지침을 찾을 수 있습니다.
         * 허용된 값:5-16자 숫자
      * **[!UICONTROL Generic Author]**

         * Livefyre 작성자 ID(JID)로 계정을 식별합니다. RSS, Tumblr 또는 URL을 통해 소스를 받는 콘텐츠에 이 옵션을 사용합니다. 이 ID를 찾으려면 **앱 콘텐츠** 또는 **자산 라이브러리**&#x200B;에서 작성자에게 속하는 콘텐츠를 검색한 다음 항목을 선택합니다. ID는 **App Content** Info **아래** Info 또는 **Details** 섹션의 **Author** 아래의 **자산 라이브러리**&#x200B;에서 사용할 수 있습니다.

         * 허용된 값:최대 255자 영숫자 문자열

         ![](assets/privacypage3.png)








1. 클릭 **[!UICONTROL Finish]**.

   ![](assets/privacypage4.png)

1. (삭제 요청만 해당) 사용자의 모든 정보를 삭제할지 확인합니다.

   >[!IMPORTANT]
   >
   >계정에 대한 데이터를 삭제하면 계정과 관련된 데이터가 영구적으로 삭제되거나 삭제됩니다. 이 작업은 되돌릴 수 없으며, 삭제한 후에는 데이터를 복구할 수 없습니다.
