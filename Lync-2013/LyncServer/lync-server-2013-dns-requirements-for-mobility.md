---
title: 'Lync Server 2013: モビリティの DNS 要件'
description: 'Lync Server 2013: モビリティの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437806"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="dc110-103">Lync Server 2013 を使ったモビリティの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="dc110-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc110-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc110-104">

<span> </span></span></span>

<span data-ttu-id="dc110-105">_**最終更新日:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="dc110-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="dc110-106">Lync Server 2013 モビリティ機能を展開するときに、Microsoft Lync Server 2013 自動検出サービスで利用できる新しい Url を使用したり、既存の Web サービスの Url を使用したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="dc110-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="dc110-107">既存の Url を使用している場合、ユーザーは自分のモバイルデバイス設定に Url を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="dc110-108">通常、このオプションはトラブルシューティングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc110-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="dc110-109">新しい Url を使用すると、モバイルクライアントは Lync Server 2013 のリソースを自動的に検出できます。</span><span class="sxs-lookup"><span data-stu-id="dc110-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="dc110-110">自動検出をサポートしている場合は、新しいドメインネームシステム (DNS) レコードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="dc110-111">このセクションでは、自動検出に必要な DNS レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="dc110-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="dc110-112">自動検出をサポートするには、SIP ドメインごとに次の DNS レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="dc110-113">組織のネットワーク内から接続するモバイルユーザーをサポートするための内部 DNS レコード</span><span class="sxs-lookup"><span data-stu-id="dc110-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="dc110-114">インターネットから接続するモバイルユーザーをサポートするための、外部またはパブリックの DNS レコード</span><span class="sxs-lookup"><span data-stu-id="dc110-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="dc110-115">内部の自動検出 URL は、ネットワークの外部からのアドレス指定を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="dc110-115">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="dc110-116">外部の自動検出 URL は、ネットワーク内からアドレス指定できません。</span><span class="sxs-lookup"><span data-stu-id="dc110-116">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="dc110-117">ただし、外部 URL に対してこの要件を満たしていない場合は、モバイルクライアントの機能が影響を受けないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-117">However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="dc110-118">DNS レコードには、CNAME レコードまたは (ホスト) レコードのいずれかを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="dc110-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="dc110-119">**内部 DNS レコード**</span><span class="sxs-lookup"><span data-stu-id="dc110-119">**Internal DNS records**</span></span>

<span data-ttu-id="dc110-120">次の内部 DNS レコードのいずれかを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc110-121">レコードの種類</span><span class="sxs-lookup"><span data-stu-id="dc110-121">Record type</span></span></th>
<th><span data-ttu-id="dc110-122">ホスト名または SRV 定義</span><span class="sxs-lookup"><span data-stu-id="dc110-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="dc110-123">解決先</span><span class="sxs-lookup"><span data-stu-id="dc110-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc110-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="dc110-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="dc110-125">lyncdiscoverinternal。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dc110-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="dc110-126">ディレクタープールの場合は、内部 Web サービスの完全修飾ドメイン名 (FQDN)、ディレクターを持っていない場合は、フロントエンドプールの FQDN</span><span class="sxs-lookup"><span data-stu-id="dc110-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc110-127">A (ホスト)</span><span class="sxs-lookup"><span data-stu-id="dc110-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="dc110-128">lyncdiscoverinternal。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dc110-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="dc110-129">ディレクターを持っていない場合は、ディレクタープールの内部 Web サービス IP アドレス (ロードバランサーを使用している場合は仮想 IP (VIP) アドレス) (ディレクターを持っていない場合は、フロントエンドプールを持っている場合)</span><span class="sxs-lookup"><span data-stu-id="dc110-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc110-130">**外部 DNS レコード**</span><span class="sxs-lookup"><span data-stu-id="dc110-130">**External DNS records**</span></span>

<span data-ttu-id="dc110-131">次のいずれかの外部 DNS レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc110-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc110-132">レコードの種類</span><span class="sxs-lookup"><span data-stu-id="dc110-132">Record type</span></span></th>
<th><span data-ttu-id="dc110-133">ホスト名</span><span class="sxs-lookup"><span data-stu-id="dc110-133">Host name</span></span></th>
<th><span data-ttu-id="dc110-134">解決先</span><span class="sxs-lookup"><span data-stu-id="dc110-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc110-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="dc110-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="dc110-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="dc110-136">lyncdiscover.</span></span> <span data-ttu-id="dc110-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dc110-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="dc110-138">ディレクタープールを所有している場合は、そのディレクタープールの外部 Web サービス FQDN (ディレクターを持っていない場合は、フロントエンドプール用)</span><span class="sxs-lookup"><span data-stu-id="dc110-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc110-139">A (ホスト)</span><span class="sxs-lookup"><span data-stu-id="dc110-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="dc110-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="dc110-140">lyncdiscover.</span></span> <span data-ttu-id="dc110-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dc110-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="dc110-142">リバースプロキシの外部またはパブリック IP アドレス (ロードバランサーを使用している場合は VIP アドレス)</span><span class="sxs-lookup"><span data-stu-id="dc110-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc110-143">SRV</span><span class="sxs-lookup"><span data-stu-id="dc110-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="dc110-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="dc110-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="dc110-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dc110-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="dc110-146">アクセスエッジサービスの host (A または AAAA) レコードに解決されます。</span><span class="sxs-lookup"><span data-stu-id="dc110-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="dc110-147">プッシュ通知サービスと Apple プッシュ通知サービスをサポートするには、Microsoft Lync モバイルクライアントを含む SIP ドメインごとに SRV レコードを1つ作成します。</span><span class="sxs-lookup"><span data-stu-id="dc110-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="dc110-148">この要件は、Apple または Microsoft ベースのモバイルデバイス上の Microsoft Lync モバイルクライアントにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="dc110-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="dc110-149">Andriod および Nokia Symbian デバイスでは、プッシュ通知は使用されません。</span><span class="sxs-lookup"><span data-stu-id="dc110-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="dc110-150">Lyncdiscover は、自動検出とも呼ばれます。トラフィックはリバースプロキシを通過します。</span><span class="sxs-lookup"><span data-stu-id="dc110-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="dc110-151">SRV レコードは、アクセスエッジサービスを通じて解決されるレコードを指します。</span><span class="sxs-lookup"><span data-stu-id="dc110-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="dc110-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc110-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

