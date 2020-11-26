---
title: 'Lync Server 2013: DNS の概要 - 拡張ディレクター プール、ハードウェア ロード バランサー'
description: 'Lync Server 2013: DNS サマリー-スケールされたディレクタープール、ハードウェアロードバランサー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled Director pool, hardware load balancer
ms:assetid: 08ba48e6-bfa1-4ab0-bc89-d58ddb9c20af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204655(v=OCS.15)
ms:contentKeyID: 48183340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7198e6a97feed8ce70cb16753ad1f21d58ef246c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428994"
---
# <a name="dns-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="44448-103">DNS の概要 - Lync Server 2013 の拡張ディレクター プール、ハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="44448-103">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44448-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44448-104">

<span> </span></span></span>

<span data-ttu-id="44448-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="44448-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="44448-106">次の表には、ハードウェア負荷分散ダイレクタをサポートするために必要な DNS レコードの概要が記載されています。</span><span class="sxs-lookup"><span data-stu-id="44448-106">The following table contains a summary of the DNS records that are required to support the hardware load balanced Director.</span></span> <span data-ttu-id="44448-107">ディレクターの役割には、フロントエンドサーバーと同様の DNS レコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="44448-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="44448-108">必要なレコードの数は、ディレクター証明書に必要なサブジェクトの代替名に反映されます。</span><span class="sxs-lookup"><span data-stu-id="44448-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="44448-109">フロントエンドサーバーとは異なり、ディレクタープールでは、ユーザーアカウントをホストしたり、モビリティサービスをホストしたりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="44448-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-a-hardware-load-balancer-and-dns-load-balancing"></a><span data-ttu-id="44448-110">ハードウェアロードバランサーと DNS の負荷分散を使用して、ディレクタープールに必要な DNS レコード</span><span class="sxs-lookup"><span data-stu-id="44448-110">DNS Records Required for the Director pool using a Hardware Load Balancer and DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44448-111">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="44448-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="44448-112">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="44448-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="44448-113">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="44448-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="44448-114">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="44448-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44448-115">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="44448-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="44448-117">ディレクター</span><span class="sxs-lookup"><span data-stu-id="44448-117">Director</span></span></p></td>
<td><p><span data-ttu-id="44448-118">レプリケーションとサーバー間通信に使用されるディレクターホストレコード</span><span class="sxs-lookup"><span data-stu-id="44448-118">Director host record used for replication and server to server communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44448-119">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="44448-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="44448-121">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="44448-121">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="44448-122">DNS 負荷分散ダイレクタプールのホストレコード</span><span class="sxs-lookup"><span data-stu-id="44448-122">Host record for the DNS load balanced Director pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44448-123">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="44448-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="44448-125">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="44448-125">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="44448-126">エッジサーバーの内部インターフェイスからの受信セッション開始プロトコル (SIP)</span><span class="sxs-lookup"><span data-stu-id="44448-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44448-127">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="44448-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="44448-129">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="44448-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="44448-130">リバースプロキシから発行されたハードウェア負荷分散の web サービス</span><span class="sxs-lookup"><span data-stu-id="44448-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44448-131">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="44448-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="44448-133">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="44448-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="44448-134">リバースプロキシの web サービスによって発行されるハードウェア負荷分散</span><span class="sxs-lookup"><span data-stu-id="44448-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44448-135">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="44448-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="44448-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="44448-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="44448-137">ディレクタープール HLB VIP</span><span class="sxs-lookup"><span data-stu-id="44448-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="44448-138">ハードウェアの負荷分散が発行され、そのリバースプロキシ Web チケットによって定義されます。ディレクタープールの外部 web サービス</span><span class="sxs-lookup"><span data-stu-id="44448-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="44448-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44448-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

