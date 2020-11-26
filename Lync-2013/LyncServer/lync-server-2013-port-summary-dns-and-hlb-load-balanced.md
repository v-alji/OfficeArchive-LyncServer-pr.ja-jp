---
title: 'Lync Server 2013: ポートの概要 - DNS および HLB による負荷分散'
description: 'Lync Server 2013: ポートの概要-DNS と HLB 負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424339"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="08601-103">ポートの概要 - Lync Server 2013 における DNS および HLB による負荷分散</span><span class="sxs-lookup"><span data-stu-id="08601-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08601-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08601-104">

<span> </span></span></span>

<span data-ttu-id="08601-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="08601-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="08601-106">1つのディレクターのファイアウォールポート要件は、内部インターフェイスまたはリバースプロキシの内部通信ネットワークからディレクターとの通信を確立するために使用されるポートで構成されています。</span><span class="sxs-lookup"><span data-stu-id="08601-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="08601-107">Microsoft Lync Server 2013 は、既定では、ポート HTTP/TCP 8080 と HTTPS/TCP 4443 が、リバースプロキシからディレクターまで、およびフロントエンドプールとフロントエンドサーバーによって開かれることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="08601-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="08601-108">さらに、エッジサーバーの内部インターフェイスからディレクターへのセッション開始プロトコル (SIP) 通信と、フロントエンドプールとフロントエンドサーバーへの通信が必要です。</span><span class="sxs-lookup"><span data-stu-id="08601-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="08601-109">SIP プロトコルは、SIP/MTLS/TCP 5061 をエッジサーバーからフロントエンドプールとフロントエンドサーバーに使用します。</span><span class="sxs-lookup"><span data-stu-id="08601-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="08601-110">SIP/MTLS/TCP 5061 によるディレクター、フロントエンドプール、フロントエンドサーバーからエッジサーバーの内部インターフェイスへの通信を可能にするルールも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08601-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="08601-111">ファイアウォールの定義用の単一のディレクターポートとプロトコル</span><span class="sxs-lookup"><span data-stu-id="08601-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08601-112">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="08601-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="08601-113">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="08601-113">Source IP address</span></span></th>
<th><span data-ttu-id="08601-114">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="08601-114">Destination IP address</span></span></th>
<th><span data-ttu-id="08601-115">メモ</span><span class="sxs-lookup"><span data-stu-id="08601-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08601-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="08601-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="08601-117">リバースプロキシ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="08601-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="08601-118">ディレクターハードウェアロードバランサー VIP</span><span class="sxs-lookup"><span data-stu-id="08601-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="08601-119">リバースプロキシの外部で最初に受信された通信は、ディレクター HLB VIP とフロントエンドサーバー web サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="08601-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08601-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="08601-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="08601-121">リバースプロキシ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="08601-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="08601-122">ディレクターハードウェアロードバランサー VIP</span><span class="sxs-lookup"><span data-stu-id="08601-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="08601-123">リバースプロキシの外部で最初に受信された通信は、ディレクター HLB VIP とフロントエンドサーバー web サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="08601-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08601-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="08601-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="08601-125">ディレクター</span><span class="sxs-lookup"><span data-stu-id="08601-125">Director</span></span></p></td>
<td><p><span data-ttu-id="08601-126">フロントエンドプールまたはフロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="08601-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="08601-127">ディレクター HLB VIP とフロントエンドサーバーまたはフロントエンドサーバー間のサーバー間通信。</span><span class="sxs-lookup"><span data-stu-id="08601-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08601-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="08601-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="08601-129">内部クライアント</span><span class="sxs-lookup"><span data-stu-id="08601-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="08601-130">ディレクターハードウェアロードバランサー VIP</span><span class="sxs-lookup"><span data-stu-id="08601-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="08601-131">ディレクターは、内部および外部クライアントに web サービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="08601-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08601-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="08601-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="08601-133">内部クライアント</span><span class="sxs-lookup"><span data-stu-id="08601-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="08601-134">ディレクターハードウェアロードバランサー VIP</span><span class="sxs-lookup"><span data-stu-id="08601-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="08601-135">ディレクターは、内部および外部クライアントに web サービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="08601-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08601-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="08601-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="08601-137">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="08601-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="08601-138">ディレクター</span><span class="sxs-lookup"><span data-stu-id="08601-138">Director</span></span></p></td>
<td><p><span data-ttu-id="08601-139">エッジサーバーからディレクターまでの SIP コミュニケーションと、フロントエンドサーバー。</span><span class="sxs-lookup"><span data-stu-id="08601-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08601-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="08601-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="08601-141">任意</span><span class="sxs-lookup"><span data-stu-id="08601-141">Any</span></span></p></td>
<td><p><span data-ttu-id="08601-142">ディレクター</span><span class="sxs-lookup"><span data-stu-id="08601-142">Director</span></span></p></td>
<td><p><span data-ttu-id="08601-143">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="08601-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08601-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="08601-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="08601-145">任意</span><span class="sxs-lookup"><span data-stu-id="08601-145">Any</span></span></p></td>
<td><p><span data-ttu-id="08601-146">ディレクター</span><span class="sxs-lookup"><span data-stu-id="08601-146">Director</span></span></p></td>
<td><p><span data-ttu-id="08601-147">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="08601-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08601-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="08601-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="08601-149">任意</span><span class="sxs-lookup"><span data-stu-id="08601-149">Any</span></span></p></td>
<td><p><span data-ttu-id="08601-150">ディレクター</span><span class="sxs-lookup"><span data-stu-id="08601-150">Director</span></span></p></td>
<td><p><span data-ttu-id="08601-151">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="08601-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="08601-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08601-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

