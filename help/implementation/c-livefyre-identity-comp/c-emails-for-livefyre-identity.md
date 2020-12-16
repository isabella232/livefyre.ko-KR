---
description: 'null'
seo-description: 'null'
seo-title: Livefyre ID에 대한 이메일
solution: Experience Manager
title: Livefyre ID에 대한 이메일
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# Livefyre ID용 이메일{#emails-for-livefyre-identity}

Livefyre ID는 다음 이메일을 전송합니다.

* [암호 재설정 이메일](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [확인 이메일](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [사용자를 위해 이메일 확인 보내기](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [환영 이메일](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [사용자에게 환영 이메일 보내기](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

**[!UICONTROL Integration Settings > Email Notifications.]**&#x200B;에서 모든 Livefyre ID 이메일의 모양과 느낌을 사용자 지정할 수 있습니다.

## 암호 재설정 이메일 {#section_nd1_whs_p1b}

사용자가 암호를 재설정하려고 하면 Livefyre가 암호 재설정 이메일을 자동으로 전송합니다.

암호 재설정 이메일은 다음과 같습니다.

**제목:** 암호 재설정

**본문:**

*&lt;사용자 이름>*,

*&lt;네트워크 이름>*&#x200B;에서 프로필의 암호를 변경하도록 요청했습니다.

요청한 경우 다음 링크를 클릭하여 새 암호를 선택하십시오.*&lt;암호 재설정 URL>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>*&#x200B;그리고  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* 이 모두 사이트 방문자와 네트워크를 기반으로 동적으로 생성됩니다.

## 확인 이메일 {#section_ak5_xhs_p1b}

사용자의 이메일 주소를 확인하는 이메일을 보낼 수 있습니다. 확인 이메일을 보내려면 **통합 설정 > Livefyre ID**&#x200B;의 옵션을 켜야 합니다.

확인 이메일은 다음과 같습니다.

**제목:** 이메일 확인

**본문:**

*&lt;사용자 이름>*,

계정을 확인하려면 다음 링크를 클릭하거나 브라우저에 붙여 넣으십시오.*&lt;verification URL>*.

이 링크는 24시간 후에 만료됩니다.

감사합니다.

*&lt;고객 이름>* 팀

*&lt;username>*,  *&lt;network name=&quot;&quot;>*&#x200B;그리고  *&lt;verification URL=&quot;&quot;>* 이 모두 사이트 방문자와 네트워크를 기반으로 동적으로 생성됩니다.

## 사용자에게 이메일 확인 보내기 {#section_vyv_yhs_p1b}

사용자에게 이메일을 보내 계정 등록에 사용하는 이메일 주소를 확인할 수 있습니다. 확인 이메일을 보내려면:

1. Studio에서 톱니바퀴 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. **통합 설정 > Livefyre ID를 클릭합니다.**

1. **로그인 유형**&#x200B;으로 이동합니다.
1. 계정에 등록하는 데 사용하는 이메일 주소를 확인하는 사용자에게 이메일을 보내려면 **전자 메일 확인 필요**&#x200B;를 클릭합니다.
1. **네트워크 이메일**&#x200B;로 이동하여 **전자 메일에 대한 로고**, 보낸 사람 주소(**전자 메일 보낸 사람**)로 사용할 전자 메일 주소(**전자 메일 표시 이름**)를 구성합니다.

## 환영 이메일 {#section_z2v_zhs_p1b}

환영 이메일을 사용자에게 보낼 수 있습니다. 환영 이메일을 보내려면 **통합 설정** > **Livefyre ID**&#x200B;의 옵션을 켜야 합니다.

환영 이메일은 다음과 같습니다.

**제목:** 시작  *&lt;customer name=&quot;&quot;>*

**본문:**

*&lt;사용자 이름>*,

*&lt;고객 이름>*&#x200B;에 계정을 만들었습니다.

이 계정은 IP 주소 *&lt;IP 주소>*&#x200B;의 *&lt;참조 URL>*&#x200B;에서 만들어졌습니다.

이 이메일은 무시해도 됩니다.

이렇게 하지 않은 경우 `support@livefyre.com`에 문의하십시오.

감사합니다.

*&quot;고객 이름&quot;* 팀

*&quot;사용자 이름&quot;, &quot;고객 이름&quot;, &quot;참조 URL&quot;* 및 &quot;IP 주소&quot;는 모두 사이트 방문자와 네트워크를 기반으로 동적으로 생성됩니다.

## 시작 이메일을 {#section_kjp_c3s_p1b} 사용자에게 보내기

계정에 등록한 후 사용자에게 환영 이메일을 보낼 수 있습니다. 확인 이메일을 설정한 경우 Studio에서 확인 이메일을 보낸 후 이 이메일을 보냅니다. 환영 이메일을 보내려면:

1. Studio에서 톱니바퀴 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. 클릭 **[!UICONTROL Integration Settings > Livefyre Identity]**

1. **[!UICONTROL Email Settings]**&#x200B;으로 이동합니다.

1. **[!UICONTROL Send Welcome Emails To New Users]**&#x200B;을 클릭하여 이메일 전송을 활성화합니다.
1. **[!UICONTROL Network Email]**&#x200B;으로 이동하여 *이메일*&#x200B;용 로고, 보낸 사람 주소(**전자 메일 보낸 사람**)로 사용할 전자 메일 주소(**전자 메일 표시 이름**)를 구성합니다.
