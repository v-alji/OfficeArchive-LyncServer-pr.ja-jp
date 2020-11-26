---
title: 'Lync Server 2013: 証明書の概要 - DNS および HLB による負荷分散'
description: 'Lync Server 2013: 証明書の概要-DNS と HLB 負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - DNS and HLB load balanced
ms:assetid: 8318a1a4-b423-47b7-95e6-9541adfad391
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205047(v=OCS.15)
ms:contentKeyID: 48184676
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a89975af16b6e39625677f787d3726f00c76c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435321"
---
# <a name="certificate-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="ba1f8-103">証明書の概要 - Lync Server 2013 の DNS および HLB による負荷分散</span><span class="sxs-lookup"><span data-stu-id="ba1f8-103">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba1f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba1f8-104">

<span> </span></span></span>

<span data-ttu-id="ba1f8-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="ba1f8-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="ba1f8-106">DNS の負荷分散とハードウェアのロードバランサーを備えたディレクターの証明書要件は、監督が受信できるサービスのサブジェクト名とサブジェクトの代替名を持つ既定の証明書を使います。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-106">Certificate requirements for a Director with DNS load balancing and a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="ba1f8-107">プール内の各ディレクターに対して証明書が要求されます。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="ba1f8-108">ハードウェアロードバランサーでは、リバースプロキシからのトラフィックだけが負荷分散されることに注意することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-108">It is important to remember that the hardware load balancer is load balancing only the traffic from the reverse proxy.</span></span> <span data-ttu-id="ba1f8-109">さらに、サーバー間認証のための OAuth トークン証明書が、各サーバーにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-109">Additionally, there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="ba1f8-110">ディレクター用の証明書</span><span class="sxs-lookup"><span data-stu-id="ba1f8-110">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba1f8-111">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ba1f8-111">Component</span></span></th>
<th><span data-ttu-id="ba1f8-112">サブジェクト名 (SN)</span><span class="sxs-lookup"><span data-stu-id="ba1f8-112">Subject name (SN)</span></span></th>
<th><span data-ttu-id="ba1f8-113">サブジェクトの代替名 (SAN)</span><span class="sxs-lookup"><span data-stu-id="ba1f8-113">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="ba1f8-114">コメント</span><span class="sxs-lookup"><span data-stu-id="ba1f8-114">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba1f8-115">Default</span><span class="sxs-lookup"><span data-stu-id="ba1f8-115">Default</span></span></p></td>
<td><p><span data-ttu-id="ba1f8-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ba1f8-116">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ba1f8-117">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ba1f8-117">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="ba1f8-118">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ba1f8-118">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="ba1f8-119">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ba1f8-119">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="ba1f8-120">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ba1f8-120">meet.contoso.com</span></span></p>
<p><span data-ttu-id="ba1f8-121">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ba1f8-121">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="ba1f8-122">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ba1f8-122">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="ba1f8-123">(必要に応じて) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="ba1f8-123">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ba1f8-124">ディレクター証明書は、内部管理の証明機関 (CA) またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-124">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="ba1f8-125">ディレクターは、境界サーバーまたはエッジサーバーのリバースプロキシからの要求に応答します。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-125">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="ba1f8-126">内部クライアントでは、監督は使用されません。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-126">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="ba1f8-127">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="ba1f8-127">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba1f8-128">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="ba1f8-128">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="ba1f8-129">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ba1f8-129">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ba1f8-130">エントリがありません</span><span class="sxs-lookup"><span data-stu-id="ba1f8-130">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="ba1f8-131">最小のキー長は1024ですが、最小の推奨されるキーの長さは2048ビットであるという警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-131">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="ba1f8-132">OAuthTokenIssuer 証明書は、大規模な環境でサーバーを認証することを目的とした単一目的の証明書であり、内部 CA またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-132">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="ba1f8-133">証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="ba1f8-133">The certificate is required.</span></span></p><span data-ttu-id="ba1f8-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba1f8-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

