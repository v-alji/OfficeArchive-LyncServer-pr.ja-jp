---
title: 'Lync Server 2013: Enhanced 9-1-1 (E9-1-1) と仲介サーバー'
description: 'Lync Server 2013: 強化された 9-1-1 (E9) および仲介サーバー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enhanced 9-1-1 (E9-1-1) and Mediation Server
ms:assetid: d231221f-5596-4a87-a463-269f5bcce65f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398903(v=OCS.15)
ms:contentKeyID: 48185448
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fb6da8e69883e321f23a53e8dc5067817d5aa66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428630"
---
# <a name="enhanced-9-1-1-e9-1-1-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="3ac06-103">Lync Server 2013 の Enhanced 9-1-1 (E9-1-1) と仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="3ac06-103">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ac06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ac06-104">

<span> </span></span></span>

<span data-ttu-id="3ac06-105">_**最終更新日:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="3ac06-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="3ac06-106">仲介サーバーは、拡張された 9-1-1 (E9) サービスプロバイダーと正しく対話できるように拡張された機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="3ac06-106">The Mediation Server has extended capabilities so that it can correctly interact with Enhanced 9-1-1 (E9-1-1) service providers.</span></span> <span data-ttu-id="3ac06-107">仲介サーバーには特別な構成は必要ありません。E9 の操作に必要な SIP 拡張機能は、既定では、仲介サーバーの SIP プロトコルに含まれており、ゲートウェイピア (PSTN ゲートウェイ、IP PBX、インターネットテレフォニーサービスプロバイダーの SBC など、E9 サービスプロバイダーを含む) の操作に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3ac06-107">No special configuration is needed on the Mediation Server; the SIP extensions required for E9-1-1 interaction are, by default, included in the Mediation Server’s SIP protocol for its interactions with a gateway peer (PSTN gateway, IP-PBX, or the SBC of an Internet Telephony Service Provider, including E9-1-1 Service Providers)</span></span>

<span data-ttu-id="3ac06-108">E9 サービスプロバイダーへの SIP トランクを既存の仲介サーバープールで終了できるかどうかは、E9 の SBC が仲介サーバーのプールを操作できるかどうかによって、スタンドアロンの仲介サーバーが必要になるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3ac06-108">Whether the SIP trunk to an E9-1-1 Service Provider can be terminated on an existing Mediation Server pool or will require stand-alone Mediation Servers will depend on whether the E9-1-1 SBC can interact with a pool of Mediation Servers.</span></span> <span data-ttu-id="3ac06-109">詳細については、「 [Lync Server 2013 の M:N トランク](lync-server-2013-m-n-trunk.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ac06-109">For details, see [M:N trunk in Lync Server 2013](lync-server-2013-m-n-trunk.md).</span></span>

<span data-ttu-id="3ac06-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ac06-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

