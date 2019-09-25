---
description: 'null'
seo-description: 'null'
seo-title: Livefyre ID용 이메일
solution: Experience Manager
title: Livefyre ID용 이메일
uuid: 4e807803-68 파섹
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre ID용 이메일{#emails-for-livefyre-identity}

Livefyre Identity는 다음 이메일을 전송합니다.

* [암호 재설정 이메일](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [확인 이메일](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [사용자를 위한 이메일 확인 보내기](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [환영 이메일](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [사용자에게 환영 이메일 보내기](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

모든 Livefyre ID 이메일의 모양과 느낌을 **[!UICONTROL Integration Settings > Email Notifications.]**

## 암호 재설정 이메일 {#section_nd1_whs_p1b}

사용자가 암호를 재설정하려고 하면 Livefyre가 암호 재설정 이메일을 자동으로 전송합니다.

암호 재설정 이메일은 다음과 같습니다.

**** 제목:암호 재설정

**본문:**

여기 *&lt;사용자 이름&gt;*,

프로필 암호 *&lt;네트워크 이름&gt;*&#x200B;변경을 요청했습니다.

이 암호를 요청한 경우 다음 링크를 클릭하여 새 암호를 선택하십시오.&lt; *암호 재설정 URL&gt;*.

*&lt;사용자 이름&gt;*, *&lt;네트워크 이름&gt;*&#x200B;및 *&lt;암호 재설정 URL&gt;* 모두 사이트 방문자와 네트워크를 기반으로 동적으로 생성됩니다.

## 확인 이메일 {#section_ak5_xhs_p1b}

사용자의 이메일 주소를 확인하는 이메일을 보낼 수 있습니다. 확인 이메일을 보내려면 [통합 설정] &gt; [Livefyre ID]에서 옵션을 **켜야 합니다**.

확인 이메일은 다음과 같습니다.

**** 제목:이메일 확인

**본문:**

안녕하세요 *&lt;사용자 이름&gt;*,

계정을 확인하려면 다음 링크를 클릭하거나 브라우저에서 붙여넣으십시오.&lt; *확인 URL&gt;*.

이 링크는 24시간 후에 만료됩니다.

감사합니다.

&lt; *고객 이름&gt;* 팀

*&lt;사용자 이름&gt;*, *&lt;네트워크 이름&gt;*&#x200B;및 *&lt;확인 URL&gt;* 모두 사이트 방문자 및 네트워크를 기반으로 동적으로 생성됩니다.

## 사용자에게 이메일 확인 보내기 {#section_vyv_yhs_p1b}

사용자에게 이메일을 보내 계정에 등록하는 데 사용하는 이메일 주소를 확인할 수 있습니다. 확인 이메일을 보내려면:

1. Studio에서 톱니바퀴 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. 통합 **설정 &gt; Livefyre ID를 클릭합니다.**

1. 로그인 **유형으로 이동합니다**.
1. 계정에 **등록하는** 데 사용하는 이메일 주소를 확인하는 사용자에게 이메일을 보내려면 [이메일 확인 필요]를 클릭합니다.
1. 네트워크 **이메일을** 찾아 보낸 사람 **주소(전자 메일 보낸 사람**)로 사용할&#x200B;**로고,**&#x200B;이메일 주소(전자 메일 표시 이름&#x200B;****)에 사용할 표시 이름을 구성합니다.

## 환영 이메일 {#section_z2v_zhs_p1b}

사용자에게 환영 이메일을 보낼 수 있습니다. 환영 이메일을 전송하려면 [통합 설정] &gt; [ **Livefyre ID** ]에서 옵션을 **설정해야 합니다**.

환영 이메일은 다음과 같습니다.

**** 제목:&lt; *&lt;고객 이름&gt;님 환영합니다.*

**본문:**

안녕하세요 *&lt;사용자 이름&gt;*,

&lt; *고객 이름&gt;*&#x200B;에서 계정을 만들었습니다.

이 계정은 *&lt;참조 URL&gt;* IP 주소 *&lt;IP 주소&gt;에서*&#x200B;만들어졌습니다.

이 경우 이 이메일을 무시해도 됩니다.

이렇게 하지 않은 경우 `support@livefyre.com`

감사합니다.

" *고객 이름"* 팀

*"사용자 이름", "고객 이름",* "참조 URL" 및 "IP 주소"는 모두 사이트 방문자 및 네트워크를 기반으로 동적으로 생성됩니다.

## 사용자에게 환영 이메일 보내기 {#section_kjp_c3s_p1b}

사용자가 계정을 등록한 후 환영 이메일을 보낼 수 있습니다. 확인 이메일을 설정한 경우 Studio에서 확인 이메일을 보낸 후 이 이메일을 보냅니다. 환영 이메일을 보내려면:

1. Studio에서 톱니바퀴 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. Click **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 로 **[!UICONTROL Email Settings]**&#x200B;이동합니다.

1. 이메일 전송을 **[!UICONTROL Send Welcome Emails To New Users]** 활성화하려면 클릭합니다.
1. 전자 메일에 대한 **[!UICONTROL Network Email]** 로고, 보낸 사람 주소 *(전자 메일 보낸 사람)로 사용할 전자 메일 주소*&#x200B;및 보낸 사람&#x200B;**전자 메일 주소에 사용할 표시 이름(**&#x200B;전자 메일 표시 이름)을 구성하려면&#x200B;****&#x200B;탐색합니다.
