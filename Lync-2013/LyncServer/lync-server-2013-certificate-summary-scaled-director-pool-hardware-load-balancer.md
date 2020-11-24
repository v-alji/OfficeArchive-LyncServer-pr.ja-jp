---
title: 証明書の概要 - 拡張ディレクター プール、ハードウェア ロード バランサー
description: 証明書の概要-スケールされたディレクタープール、ハードウェアロードバランサー。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399411"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="76efe-103">証明書の概要 - Lync Server 2013 の拡張ディレクター プール、ハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="76efe-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76efe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76efe-104">

<span> </span></span></span>

<span data-ttu-id="76efe-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="76efe-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="76efe-106">ハードウェアロードバランサーを備えたディレクターの証明書要件は、ディレクタープールが受け取ることのできるサービスのサブジェクト名とサブジェクトの代替名を持つ既定の証明書を使います。</span><span class="sxs-lookup"><span data-stu-id="76efe-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="76efe-107">プール内の各ディレクターに対して証明書が要求されます。</span><span class="sxs-lookup"><span data-stu-id="76efe-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="76efe-108">また、各サーバーにインストールされるサーバー認証用の OAuth トークン証明書もあります。</span><span class="sxs-lookup"><span data-stu-id="76efe-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="76efe-109">ハードウェアロードバランサーを使用した、スケーリングされたディレクター用の証明書</span><span class="sxs-lookup"><span data-stu-id="76efe-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76efe-110">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="76efe-110">Component</span></span></th>
<th><span data-ttu-id="76efe-111">サブジェクト名 (SN)</span><span class="sxs-lookup"><span data-stu-id="76efe-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="76efe-112">サブジェクトの代替名 (SAN)</span><span class="sxs-lookup"><span data-stu-id="76efe-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="76efe-113">コメント</span><span class="sxs-lookup"><span data-stu-id="76efe-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76efe-114">Default</span><span class="sxs-lookup"><span data-stu-id="76efe-114">Default</span></span></p></td>
<td><p><span data-ttu-id="76efe-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="76efe-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="76efe-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="76efe-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="76efe-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="76efe-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="76efe-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="76efe-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="76efe-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="76efe-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="76efe-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="76efe-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="76efe-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="76efe-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="76efe-122">(必要に応じて) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="76efe-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="76efe-123">ディレクター証明書は、内部管理の証明機関 (CA) またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="76efe-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="76efe-124">ディレクターは、境界サーバーまたはエッジサーバーのリバースプロキシからの要求に応答します。</span><span class="sxs-lookup"><span data-stu-id="76efe-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="76efe-125">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="76efe-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76efe-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="76efe-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="76efe-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="76efe-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="76efe-128">エントリがありません</span><span class="sxs-lookup"><span data-stu-id="76efe-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="76efe-129">最小のキー長は1024ですが、最小の推奨されるキーの長さは2048ビットであるという警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="76efe-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="76efe-130">OAuthTokenIssuer 証明書は、大規模な環境でサーバーを認証することを目的とした単一目的の証明書であり、内部 CA またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="76efe-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="76efe-131">証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="76efe-131">The certificate is required.</span></span></p><span data-ttu-id="76efe-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76efe-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

