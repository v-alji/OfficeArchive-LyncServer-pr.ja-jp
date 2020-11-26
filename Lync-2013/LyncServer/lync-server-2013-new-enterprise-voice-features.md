---
title: 'Lync Server 2013: 新しいエンタープライズ VoIP 機能'
description: 'Lync Server 2013: 新しいエンタープライズ Voip 機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Enterprise Voice features
ms:assetid: db0ad7b9-e469-4c29-89d9-52fed018ef08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398964(v=OCS.15)
ms:contentKeyID: 48185591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1fc0c0970fe22fb6a56eaf0d950f1d49d210826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445422"
---
# <a name="new-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="93c67-103">Lync Server 2013 の新しいエンタープライズ VoIP 機能</span><span class="sxs-lookup"><span data-stu-id="93c67-103">New Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93c67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93c67-104">

<span> </span></span></span>

<span data-ttu-id="93c67-105">_**最終更新日:** 2013-05-01_</span><span class="sxs-lookup"><span data-stu-id="93c67-105">_**Topic Last Modified:** 2013-05-01_</span></span>

<span data-ttu-id="93c67-106">Lync Server 2013 には、エンタープライズ Voip を強化するための新しいルーティングと通話管理機能がいくつか導入されています。</span><span class="sxs-lookup"><span data-stu-id="93c67-106">Lync Server 2013 introduces several new routing and call management features that enhance Enterprise Voice.</span></span>

<span data-ttu-id="93c67-107">Lync Server 2013 は、仲介サーバーとゲートウェイ間での複数の trunks をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="93c67-107">Lync Server 2013 supports multiple trunks between Mediation Servers and gateways.</span></span> <span data-ttu-id="93c67-108">*トランク* は、ポート番号とゲートウェイの間の論理的な関連となります。</span><span class="sxs-lookup"><span data-stu-id="93c67-108">A *trunk* is a logical association between a port number and Mediation Server with a port number and gateway.</span></span> <span data-ttu-id="93c67-109">つまり、仲介サーバーは、異なるゲートウェイに対して複数の trunks を持つことができます。また、ゲートウェイは、別々の仲介サーバーに対して複数の trunks を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="93c67-109">This means that a Mediation Server can have multiple trunks to different gateways, and a gateway can have multiple trunks to different Mediation Servers.</span></span> <span data-ttu-id="93c67-110">自動トランクルーティングを使用すると、Lync Server 2013 は、IP PBX と公衆交換電話網 (PSTN) ゲートウェイ、または複数の IP PBX システムに接続することができます。</span><span class="sxs-lookup"><span data-stu-id="93c67-110">Intertrunk routing makes it possible for Lync Server 2013 to interconnect an IP-PBX to a public switched telephone network (PSTN) gateway or to interconnect multiple IP-PBX systems.</span></span> <span data-ttu-id="93c67-111">Lync Server 2013 は、異なるテレフォニーシステム間のグルー (つまり相互接続) として機能します。</span><span class="sxs-lookup"><span data-stu-id="93c67-111">Lync Server 2013 serves as the glue (that is, the interconnection) between different telephony systems.</span></span>

<span data-ttu-id="93c67-112">Microsoft Lync Server 2013 を使用すると、着信の転送、同時呼び出し、ボイスメール処理、発信者番号表示の各機能の機能が改善されます。</span><span class="sxs-lookup"><span data-stu-id="93c67-112">Microsoft Lync Server 2013 makes improvements in the areas of call forwarding, simultaneous ringing, voice mail handling, and caller ID presentation.</span></span> <span data-ttu-id="93c67-113">これらの機能により、エンタープライズ音声通話の操作性が向上します。</span><span class="sxs-lookup"><span data-stu-id="93c67-113">These features enrich the Enterprise Voice call experience.</span></span>

<span data-ttu-id="93c67-114">Lync Server 2013 では、エンタープライズ Voip の次のような新しい機能強化が導入されています。</span><span class="sxs-lookup"><span data-stu-id="93c67-114">Lync Server 2013 introduces the following new enhancements to Enterprise Voice:</span></span>

  - [<span data-ttu-id="93c67-115">Lync Server 2013 の新しい通話機能</span><span class="sxs-lookup"><span data-stu-id="93c67-115">New call features in Lync Server 2013</span></span>](lync-server-2013-new-call-features.md)

  - [<span data-ttu-id="93c67-116">Lync Server 2013 の新しい発信者番号の機能</span><span class="sxs-lookup"><span data-stu-id="93c67-116">New caller ID feature in Lync Server 2013</span></span>](lync-server-2013-new-caller-id-feature.md)

  - [<span data-ttu-id="93c67-117">Lync Server 2013 の新しいボイス メールの機能</span><span class="sxs-lookup"><span data-stu-id="93c67-117">New voice mail feature in Lync Server 2013</span></span>](lync-server-2013-new-voice-mail-feature.md)

  - [<span data-ttu-id="93c67-118">Lync Server 2013 の新しいトランク機能</span><span class="sxs-lookup"><span data-stu-id="93c67-118">New trunk feature in Lync Server 2013</span></span>](lync-server-2013-new-trunk-feature.md)

  - [<span data-ttu-id="93c67-119">Lync Server 2013 の新しいトランク間機能</span><span class="sxs-lookup"><span data-stu-id="93c67-119">New intertrunk feature in Lync Server 2013</span></span>](lync-server-2013-new-intertrunk-feature.md)

  - [<span data-ttu-id="93c67-120">Lync Server 2013 の新しい通話管理機能</span><span class="sxs-lookup"><span data-stu-id="93c67-120">New call management features in Lync Server 2013</span></span>](lync-server-2013-new-call-management-features.md)

<span data-ttu-id="93c67-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93c67-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

