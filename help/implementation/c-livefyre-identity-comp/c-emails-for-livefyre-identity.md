---
description: null
seo-description: null
seo-title: Livefyre ID에 대한 이메일
solution: Experience Manager
title: Livefyre ID에 대한 이메일
uuid: 4 E 807803-687 E -4 DF 0-94 D 1-B 18 A 48 D 024 E 8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre ID에 대한 이메일{#emails-for-livefyre-identity}

Livefyre Identity는 다음 이메일을 전송합니다.

* [암호 재설정 이메일](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [확인 이메일](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [사용자를 위한 이메일 확인 보내기](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [환영 이메일](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [사용자에게 환영 이메일 보내기](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

모든 Livefyre ID 이메일의 모양과 느낌을 **[!UICONTROL Integration Settings > Email Notifications.]**

## 암호 재설정 이메일 {#section_nd1_whs_p1b}

사용자가 암호를 재설정하려고 하면 Livefyre에서 암호 재설정 이메일을 자동으로 보냅니다.

암호 재설정 이메일은 다음과 같습니다.

**제목:** 암호 재설정

**본문:**

안녕하세요. < *username >*님, 안녕하세요.

< 네트워크 이름 >에서 *프로필의 암호를 변경하라는 요청이*있었습니다.

요청한 경우 다음 링크를 클릭하여 새 암호를 선택하십시오. *< 암호 재설정 URL >*.

*< 사용자 이름 >*, *< 네트워크 이름 >*및 *< 암호 재설정 URL >* 는 모두 사이트 방문자 및 네트워크에 따라 동적으로 생성됩니다.

## 확인 이메일 {#section_ak5_xhs_p1b}

사용자의 이메일 주소를 확인하는 이메일을 보낼 수 있습니다. 확인 이메일을 전송하려면 통합 설정 > Livefyre ID에서 **옵션을**켜야 합니다.

확인 이메일은 다음과 같습니다.

**제목:** 이메일 확인

**본문:**

< *username > 님*, 안녕하세요.

계정을 확인하려면 다음 링크를 클릭하여 (또는 브라우저에 붙여넣으십시오): *< 확인 URL >*.

이 링크는 24 시간 후에 만료됩니다.

감사합니다.

< *Customer Name >* 팀

*< 사용자 이름 >*, *< 네트워크 이름 >*및 *< 확인 URL >* 는 모두 사이트 방문자 및 네트워크에 따라 동적으로 생성됩니다.

## 사용자에게 이메일 확인 보내기 {#section_vyv_yhs_p1b}

사용자에게 이메일을 보내어 계정에 등록하는 데 사용하는 이메일 주소를 확인할 수 있습니다. 확인 이메일을 전송하려면:

1. 스튜디오에서 기어 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. **통합 설정 > Livefyre ID를 클릭합니다.**

1. **로그인 유형으로 이동합니다**.
1. 계정에 **등록할 때 사용하는 이메일 주소를 확인하는 사용자에게 이메일을 보내려면 [이메일 확인** 필요] 를 클릭합니다.
1. **네트워크 이메일로** 이동하여 이메일의 **로고**, 보낸 사람 주소 (**보낸 사람 주소)**로 사용할 이메일 주소 및 이메일 주소 (**이메일 표시 이름**) 에 사용할 표시 이름을 구성합니다.

## 환영 이메일 {#section_z2v_zhs_p1b}

사용자에게 환영 이메일을 보낼 수 있습니다. 환영 이메일을 전송하려면 **통합 설정** > **Livefyre ID에서 옵션을**켜야 합니다.

환영 이메일은 다음과 같습니다.

**제목:** *< customer name > 님 환영합니다.*

**본문:**

< *username > 님*, 안녕하세요.

< customer name >에서 *사용자를 위해 계정이*생성되었습니다.

이 계정은 *< 참조 URL >* IP 주소 *< IP 주소 >에서 작성되었습니다*.

이 경우 이 이메일을 무시해도 됩니다.

이 작업을 수행하지 않은 경우 `support@livefyre.com`

thanks

" *고객 이름 "* 팀

*" 사용자 이름 "," 고객 이름 "," 참조 URL "* 및" IP 주소 "는 모두 사이트 방문자 및 네트워크를 기반으로 동적으로 생성됩니다.

## 사용자에게 환영 이메일 보내기 {#section_kjp_c3s_p1b}

사용자가 계정에 등록한 후 환영 이메일을 보낼 수 있습니다. 확인 이메일을 설정한 경우, Studio는 확인 이메일을 전송한 후 이 이메일을 보냅니다. 환영 이메일을 보내려면:

1. 스튜디오에서 기어 아이콘을 클릭하여 네트워크 설정을 수정합니다.
1. click **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 로 이동합니다 **[!UICONTROL Email Settings]**.

1. 을 클릭하여 **[!UICONTROL Send Welcome Emails To New Users]** 이메일 전송을 활성화합니다.
1. 탐색하여 **[!UICONTROL Network Email]** 이메일의 **로고, 보낸 사람 주소 (**보낸 사람 주소)**로 사용할 이메일 주소 및 이메일 주소 (**이메일 표시 이름**) 에 사용할 표시 이름을 구성합니다.
