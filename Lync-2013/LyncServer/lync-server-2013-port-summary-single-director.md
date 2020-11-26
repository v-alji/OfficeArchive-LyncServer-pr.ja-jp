---
title: 'Lync Server 2013: ポートの概要 - 単一のディレクター'
description: 'Lync Server 2013: ポートの概要-単一のディレクター。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436980"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="a3db4-103">ポートの概要 - Lync Server 2013 での単一のディレクター</span><span class="sxs-lookup"><span data-stu-id="a3db4-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3db4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3db4-104">

<span> </span></span></span>

<span data-ttu-id="a3db4-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="a3db4-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="a3db4-106">1つのディレクターのファイアウォールポート要件は、内部インターフェイスまたはリバースプロキシの内部通信ネットワークからディレクターとの通信を確立するために使用されるポートで構成されています。</span><span class="sxs-lookup"><span data-stu-id="a3db4-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="a3db4-107">Microsoft Lync Server 2013 は、既定では、ポート HTTP/TCP 8080 と HTTPS/TCP 4443 が、リバースプロキシからディレクターまで、およびフロントエンドプールとフロントエンドサーバーによって開かれることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="a3db4-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="a3db4-108">さらに、エッジサーバーの内部インターフェイスからディレクターへのセッション開始プロトコル (SIP) 通信と、フロントエンドプールとフロントエンドサーバーへの通信が必要です。</span><span class="sxs-lookup"><span data-stu-id="a3db4-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="a3db4-109">SIP プロトコルは、SIP/MTLS/TCP 5061 をエッジサーバーからフロントエンドプールとフロントエンドサーバーに使用します。</span><span class="sxs-lookup"><span data-stu-id="a3db4-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="a3db4-110">SIP/MTLS/TCP 5061 によるディレクター、フロントエンドプール、フロントエンドサーバーからエッジサーバーの内部インターフェイスへの通信を可能にするルールも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3db4-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="a3db4-111">ファイアウォールの定義用の単一のディレクターポートとプロトコル</span><span class="sxs-lookup"><span data-stu-id="a3db4-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3db4-112">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="a3db4-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="a3db4-113">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="a3db4-113">Source IP address</span></span></th>
<th><span data-ttu-id="a3db4-114">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="a3db4-114">Destination IP address</span></span></th>
<th><span data-ttu-id="a3db4-115">メモ</span><span class="sxs-lookup"><span data-stu-id="a3db4-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3db4-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="a3db4-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="a3db4-117">リバースプロキシ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-118">ディレクター</span><span class="sxs-lookup"><span data-stu-id="a3db4-118">Director</span></span></p></td>
<td><p><span data-ttu-id="a3db4-119">リバースプロキシの外部で最初に受信した通信は、ディレクターおよびフロントエンドサーバー web サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a3db4-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3db4-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="a3db4-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="a3db4-121">リバースプロキシ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-122">ディレクター</span><span class="sxs-lookup"><span data-stu-id="a3db4-122">Director</span></span></p></td>
<td><p><span data-ttu-id="a3db4-123">リバースプロキシの外部で最初に受信した通信は、ディレクターおよびフロントエンドサーバー web サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a3db4-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3db4-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="a3db4-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="a3db4-125">ディレクター</span><span class="sxs-lookup"><span data-stu-id="a3db4-125">Director</span></span></p></td>
<td><p><span data-ttu-id="a3db4-126">フロントエンドサーバーまたはフロントエンドプール</span><span class="sxs-lookup"><span data-stu-id="a3db4-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="a3db4-127">ディレクターとフロントエンドサーバーとの間のサーバー間通信</span><span class="sxs-lookup"><span data-stu-id="a3db4-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3db4-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="a3db4-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="a3db4-129">内部クライアント</span><span class="sxs-lookup"><span data-stu-id="a3db4-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="a3db4-130">ディレクター web サービス</span><span class="sxs-lookup"><span data-stu-id="a3db4-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="a3db4-131">ディレクターは、内部および外部のクライアントに web サービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a3db4-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3db4-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="a3db4-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="a3db4-133">内部クライアント</span><span class="sxs-lookup"><span data-stu-id="a3db4-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="a3db4-134">ディレクター web サービス</span><span class="sxs-lookup"><span data-stu-id="a3db4-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="a3db4-135">ディレクターは、内部および外部のクライアントに web サービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a3db4-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3db4-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="a3db4-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="a3db4-137">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-138">ディレクター</span><span class="sxs-lookup"><span data-stu-id="a3db4-138">Director</span></span></p></td>
<td><p><span data-ttu-id="a3db4-139">エッジサーバーからディレクターへの SIP コミュニケーションと、フロントエンドサーバー。</span><span class="sxs-lookup"><span data-stu-id="a3db4-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3db4-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="a3db4-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="a3db4-141">任意</span><span class="sxs-lookup"><span data-stu-id="a3db4-141">Any</span></span></p></td>
<td><p><span data-ttu-id="a3db4-142">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-143">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClasAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="a3db4-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3db4-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="a3db4-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="a3db4-145">任意</span><span class="sxs-lookup"><span data-stu-id="a3db4-145">Any</span></span></p></td>
<td><p><span data-ttu-id="a3db4-146">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-147">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClasAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="a3db4-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3db4-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="a3db4-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="a3db4-149">任意</span><span class="sxs-lookup"><span data-stu-id="a3db4-149">Any</span></span></p></td>
<td><p><span data-ttu-id="a3db4-150">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3db4-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a3db4-151">一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClasAgent.exe) コマンドとログ収集</span><span class="sxs-lookup"><span data-stu-id="a3db4-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a3db4-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3db4-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

