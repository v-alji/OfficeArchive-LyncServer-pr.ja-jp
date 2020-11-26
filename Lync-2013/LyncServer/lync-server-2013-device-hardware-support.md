---
title: 'Lync Server 2013: デバイス ハードウェアのサポート'
description: Lync Server 2013 デバイスハードウェアのサポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429453"
---
# <a name="device-hardware-support-in-lync-server-2013"></a>Lync Server 2013 でのデバイス ハードウェアのサポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-12-14_

IP 電話とアナログデバイスを展開する前に、特定のハードウェア構成を行う必要があります。

Lync Phone Edition を実行している IP 電話は、リンクレイヤー検出 Protocol-Media Endpoint Discovery (LLDP-MED) および Power over Ethernet (PoE) をサポートしています。 LLDP を利用するには、スイッチは IEEE 802.1 AB と ANSI/TIA-1057 をサポートしている必要があります。 PoE を活用するには、スイッチは PoE 802.3 AF または 802.3 at に対応している必要があります。

LLDP を有効にするには、管理者は、[コンソールの切り替え] ウィンドウを使って LLDP を有効にし、適切なボイス VLAN ID を使用して LLDP ネットワークポリシーを設定する必要があります。

また、展開にアナログデバイスが含まれている場合は、Lync Server を使用するようにアナログゲートウェイを設定する必要があります。また、ゲートウェイは以下のいずれかである必要があります。

  - アナログ電話アダプター (ATA)

  - PSTN アナログゲートウェイ

  - PSTN アナログゲートウェイを含む Survivable Branch アプライアンス

  - ATA と通信する PSTN ゲートウェイが含まれている Survivable Branch アプライアンス

アナログゲートウェイを構成する方法については、 [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) Lync Server 2010 TechNet ライブラリの「アナログデバイスの展開を計画する」を参照してください。 (アナログデバイス2010は、lync server 2013 での動作と同じように機能します)。

<div>


> [!IMPORTANT]  
> スイッチでサポートされている場合は、強化された 9-1-1 (E9) のスイッチを構成できます。



</div>

</div>

<span> </span>

</div>

</div>

</div>

