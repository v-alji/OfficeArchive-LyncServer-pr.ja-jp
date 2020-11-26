---
title: 'Lync Server 2013: DNS の概要 - DNS と HLB 負荷分散'
description: 'Lync Server 2013: DNS の概要-DNS と HLB 負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - DNS and HLB load balanced
ms:assetid: d2132695-1956-4190-a98e-cd7255cbded6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205273(v=OCS.15)
ms:contentKeyID: 48185447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c191d653ce4025618e135b4c69bc673f79a6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437743"
---
# <a name="dns-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="5d7f4-103">DNS の概要 - Lync Server 2013 での DNS と HLB 負荷分散</span><span class="sxs-lookup"><span data-stu-id="5d7f4-103">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d7f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d7f4-104">

<span> </span></span></span>

<span data-ttu-id="5d7f4-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="5d7f4-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="5d7f4-106">次の表には、DNS の負荷分散とハードウェア負荷分散ディレクターをサポートするために必要な DNS レコードの概要が記載されています。</span><span class="sxs-lookup"><span data-stu-id="5d7f4-106">The following table contains a summary of the DNS records that are required to support the DNS load balanced and hardware load balanced Director.</span></span> <span data-ttu-id="5d7f4-107">ディレクターの役割には、フロントエンドサーバーと同様の DNS レコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="5d7f4-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="5d7f4-108">必要なレコードの数は、ディレクター証明書に必要なサブジェクトの代替名に反映されます。</span><span class="sxs-lookup"><span data-stu-id="5d7f4-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="5d7f4-109">フロントエンドサーバーとは異なり、ディレクタープールでは、ユーザーアカウントをホストしたり、モビリティサービスをホストしたりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="5d7f4-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-dns-load-balancing-and-hardware-load-balancer"></a><span data-ttu-id="5d7f4-110">DNS 負荷分散とハードウェアロードバランサーを使って、ディレクタープールに必要な DNS レコード</span><span class="sxs-lookup"><span data-stu-id="5d7f4-110">DNS Records Required for the Director Pool using DNS Load Balancing and Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d7f4-111">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="5d7f4-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5d7f4-112">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="5d7f4-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="5d7f4-113">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="5d7f4-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="5d7f4-114">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="5d7f4-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d7f4-115">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="5d7f4-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-117">ディレクター</span><span class="sxs-lookup"><span data-stu-id="5d7f4-117">Director</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-118">レプリケーションとサーバー間で使用されるディレクターホストレコード</span><span class="sxs-lookup"><span data-stu-id="5d7f4-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7f4-119">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="5d7f4-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-121">ディレクター プール</span><span class="sxs-lookup"><span data-stu-id="5d7f4-121">Director pool</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-122">サーバー間の DNS 負荷分散ダイレクタプールのホストレコード</span><span class="sxs-lookup"><span data-stu-id="5d7f4-122">Host record for the DNS load balanced Director pool for server to server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d7f4-123">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5d7f4-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-125">ディレクター プール</span><span class="sxs-lookup"><span data-stu-id="5d7f4-125">Director pool</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-126">エッジサーバーの内部インターフェイスからの受信セッション開始プロトコル (SIP)</span><span class="sxs-lookup"><span data-stu-id="5d7f4-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7f4-127">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5d7f4-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-129">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="5d7f4-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-130">リバースプロキシから発行されたハードウェア負荷分散の web サービス</span><span class="sxs-lookup"><span data-stu-id="5d7f4-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d7f4-131">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5d7f4-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-133">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="5d7f4-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-134">リバースプロキシの web サービスによって発行されるハードウェア負荷分散</span><span class="sxs-lookup"><span data-stu-id="5d7f4-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7f4-135">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5d7f4-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5d7f4-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-137">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="5d7f4-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="5d7f4-138">ハードウェアの負荷分散が発行され、そのリバースプロキシ Web チケットによって定義されます。ディレクタープールの外部 web サービス</span><span class="sxs-lookup"><span data-stu-id="5d7f4-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d7f4-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d7f4-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

