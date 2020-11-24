---
title: 'Lync Server 2013: DNS の概要 - 単一ディレクター'
description: 'Lync Server 2013: DNS の概要-単一のディレクター。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78ef19383df45644ad951ca5da69ef893b231980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397940"
---
# <a name="dns-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="62a3b-103">DNS の概要 - Lync Server 2013 の単一ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-103">DNS summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62a3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62a3b-104">

<span> </span></span></span>

<span data-ttu-id="62a3b-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="62a3b-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="62a3b-106">次の表には、1つのディレクターをサポートするために必要な DNS レコードの概要が記載されています。</span><span class="sxs-lookup"><span data-stu-id="62a3b-106">The following table contains a summary of the DNS records that are required to support the single Director.</span></span> <span data-ttu-id="62a3b-107">ディレクターの役割には、フロントエンドサーバーと同様の DNS レコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="62a3b-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="62a3b-108">必要なレコードの数は、ディレクター証明書に必要なサブジェクトの代替名に反映されます。</span><span class="sxs-lookup"><span data-stu-id="62a3b-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="62a3b-109">フロントエンドサーバーとは異なり、ディレクターはユーザーアカウントをホストしないか、モビリティサービスをホストしません。</span><span class="sxs-lookup"><span data-stu-id="62a3b-109">Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director"></a><span data-ttu-id="62a3b-110">ディレクターに必要な DNS レコード</span><span class="sxs-lookup"><span data-stu-id="62a3b-110">DNS Records Required for the Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62a3b-111">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="62a3b-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="62a3b-112">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="62a3b-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="62a3b-113">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="62a3b-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="62a3b-114">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="62a3b-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62a3b-115">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="62a3b-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="62a3b-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="62a3b-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="62a3b-117">ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-117">Director</span></span></p></td>
<td><p><span data-ttu-id="62a3b-118">レプリケーションとサーバー間で使用されるディレクターホストレコード</span><span class="sxs-lookup"><span data-stu-id="62a3b-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a3b-119">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="62a3b-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="62a3b-120">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="62a3b-120">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="62a3b-121">ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-121">Director</span></span></p></td>
<td><p><span data-ttu-id="62a3b-122">エッジサーバーの内部エッジインターフェイスからの受信セッション開始プロトコル (SIP)</span><span class="sxs-lookup"><span data-stu-id="62a3b-122">Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a3b-123">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="62a3b-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="62a3b-124">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="62a3b-124">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="62a3b-125">ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-125">Director</span></span></p></td>
<td><p><span data-ttu-id="62a3b-126">リバースプロキシから公開されたダイヤルインの web サービス</span><span class="sxs-lookup"><span data-stu-id="62a3b-126">Published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a3b-127">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="62a3b-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="62a3b-128">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="62a3b-128">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="62a3b-129">ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-129">Director</span></span></p></td>
<td><p><span data-ttu-id="62a3b-130">リバースプロキシから発行された web サービス</span><span class="sxs-lookup"><span data-stu-id="62a3b-130">Published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a3b-131">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="62a3b-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="62a3b-132">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="62a3b-132">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="62a3b-133">ディレクター</span><span class="sxs-lookup"><span data-stu-id="62a3b-133">Director</span></span></p></td>
<td><p><span data-ttu-id="62a3b-134">リバースプロキシ Web チケットによって公開および定義されるディレクターの外部 web サービス</span><span class="sxs-lookup"><span data-stu-id="62a3b-134">Published and defined by the reverse proxy Web Ticket external web services for the Director</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="62a3b-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62a3b-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

