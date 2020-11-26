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
# <a name="device-hardware-support-in-lync-server-2013"></a><span data-ttu-id="88808-103">Lync Server 2013 でのデバイス ハードウェアのサポート</span><span class="sxs-lookup"><span data-stu-id="88808-103">Device hardware support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88808-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88808-104">

<span> </span></span></span>

<span data-ttu-id="88808-105">_**最終更新日:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="88808-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="88808-106">IP 電話とアナログデバイスを展開する前に、特定のハードウェア構成を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="88808-106">Specific hardware configurations must be in place before you deploy IP phones and analog devices.</span></span>

<span data-ttu-id="88808-107">Lync Phone Edition を実行している IP 電話は、リンクレイヤー検出 Protocol-Media Endpoint Discovery (LLDP-MED) および Power over Ethernet (PoE) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="88808-107">IP phones running Lync Phone Edition support Link Layer Discovery Protocol-Media Endpoint Discovery (LLDP-MED) and Power over Ethernet (PoE).</span></span> <span data-ttu-id="88808-108">LLDP を利用するには、スイッチは IEEE 802.1 AB と ANSI/TIA-1057 をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="88808-108">To take advantage of LLDP-MED, the switch must support IEEE802.1AB and ANSI/TIA-1057.</span></span> <span data-ttu-id="88808-109">PoE を活用するには、スイッチは PoE 802.3 AF または 802.3 at に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="88808-109">To take advantage of PoE, the switch must support PoE802.3AF or 802.3at.</span></span>

<span data-ttu-id="88808-110">LLDP を有効にするには、管理者は、[コンソールの切り替え] ウィンドウを使って LLDP を有効にし、適切なボイス VLAN ID を使用して LLDP ネットワークポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88808-110">To enable LLDP-MED, the administrator must enable LLDP by using the switch console window and set the LLDP-MED network policy with the correct voice VLAN ID.</span></span>

<span data-ttu-id="88808-111">また、展開にアナログデバイスが含まれている場合は、Lync Server を使用するようにアナログゲートウェイを設定する必要があります。また、ゲートウェイは以下のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="88808-111">In addition, if your deployment includes analog devices, you must configure the analog gateway to use Lync Server, and the gateway must be one of the following:</span></span>

  - <span data-ttu-id="88808-112">アナログ電話アダプター (ATA)</span><span class="sxs-lookup"><span data-stu-id="88808-112">An analog telephone adapter (ATA)</span></span>

  - <span data-ttu-id="88808-113">PSTN アナログゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="88808-113">A PSTN analog gateway</span></span>

  - <span data-ttu-id="88808-114">PSTN アナログゲートウェイを含む Survivable Branch アプライアンス</span><span class="sxs-lookup"><span data-stu-id="88808-114">A Survivable Branch Appliance that includes a PSTN analog gateway</span></span>

  - <span data-ttu-id="88808-115">ATA と通信する PSTN ゲートウェイが含まれている Survivable Branch アプライアンス</span><span class="sxs-lookup"><span data-stu-id="88808-115">A Survivable Branch Appliance that includes a PSTN gateway that communicates with an ATA</span></span>

<span data-ttu-id="88808-116">アナログゲートウェイを構成する方法については、 [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) Lync Server 2010 TechNet ライブラリの「アナログデバイスの展開を計画する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88808-116">To learn how to configure an analog gateway, see "Planning to Deploy Analog Devices" at [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="88808-117">(アナログデバイス2010は、lync server 2013 での動作と同じように機能します)。</span><span class="sxs-lookup"><span data-stu-id="88808-117">(Analog devices work the same way in Lync Server 2013 as they do in Lync Server 2010.)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="88808-118">スイッチでサポートされている場合は、強化された 9-1-1 (E9) のスイッチを構成できます。</span><span class="sxs-lookup"><span data-stu-id="88808-118">You can configure the switch for Enhanced 9-1-1 (E9-1-1), if the switch supports this.</span></span>



<span data-ttu-id="88808-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88808-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

