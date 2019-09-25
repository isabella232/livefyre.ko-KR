---
description: 사용자가 미디어를 게시할 수 있는 소스와 미디어 게시물을 금지할 소스를 정의합니다.
seo-description: 사용자가 미디어를 게시할 수 있는 소스와 미디어 게시물을 금지할 소스를 정의합니다.
seo-title: 포함된 미디어 관리
title: 포함된 미디어 관리
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 포함된 미디어 관리{#manage-embedded-media}

사용자가 미디어를 게시할 수 있는 소스와 미디어 게시물을 금지할 소스를 정의합니다.

기본적으로 모든 미디어 첨부 파일을 주석에 포함할 수 있습니다. 지원되는 전체 공급자 목록은 embed.ly/providers을 참조하십시오.

Livefyre는 Embed.ly 및 표준 Embed 프로토콜을 사용하여 앱 스트림에 미디어를 포함시키고 소스에서 제공되는 모든 미디어 데이터를 전달합니다.

Embed.ly는 제공된 URL에 대한 미디어 제목, 설명, 축소판 및 포함 코드를 포함하여 사용 가능한 모든 정보를 전달합니다. 이러한 항목의 사용 가능 여부는 공급자에 따라 다릅니다. 예:Facebook은 비디오의 축소판을 반환하지 않고 임베드 가능한 비디오만 전달합니다. 재생을 클릭하면 비디오가 시작됩니다(YouTube의 표시 형식과 유사). Twitter는 정적 이미지만 전달하며 비디오를 아래로 전송하지 않습니다. 따라서 Twitter 기본 비디오는 Livefyre 스트림 내에서 재생되지 않을 수 있습니다.

주석 스트림을 포함할 때 특정 첨부 파일이 주석에 포함되지 않도록 할 수 있습니다. 또한 Studio를 사용하여 네트워크, 사이트 및 대화 수준에서 모든 Embed.ly 확장을 숨겨 미디어에 대한 링크만 표시하고 완전히 임베드된 미디어는 표시하지 않을 수 있습니다.

이 기능을 사용하는 앱:

* [기능 카드](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [맵](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

