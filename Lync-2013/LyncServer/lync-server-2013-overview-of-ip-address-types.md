---
title: 'Lync Server 2013: IP アドレス タイプの概要'
description: 'Lync Server 2013: IP アドレスの種類の概要。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of IP address types for Lync Server
ms:assetid: ee9a695f-5cf5-441e-94fb-6adeca50e8d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205363(v=OCS.15)
ms:contentKeyID: 48185759
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81492b2e006a6f44f6deb78e6a0560f6e319992f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445135"
---
# <a name="overview-of-ip-address-types-for-lync-server-2013"></a><span data-ttu-id="feab9-103">Lync Server 2013 の IP アドレス タイプの概要</span><span class="sxs-lookup"><span data-stu-id="feab9-103">Overview of IP address types for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="feab9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="feab9-104">

<span> </span></span></span>

<span data-ttu-id="feab9-105">_**最終更新日:** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="feab9-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="feab9-106">Lync Server 2013 で IP アドレスを構成する際には、次の3つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="feab9-106">You have three options when configuring IP addresses in Lync Server 2013.</span></span> <span data-ttu-id="feab9-107">Lync Server 2013 は、IP バージョン 4 (IPv4)、IP バージョン 6 (IPv6)、またはその両方の組み合わせ ( *デュアルスタック* とも呼ばれます) をサポートするように構成できます。</span><span class="sxs-lookup"><span data-stu-id="feab9-107">You can configure Lync Server 2013 to support only IP version 4 (IPv4), only IP version 6 (IPv6), or a combination of both (known as a *dual stack*).</span></span> <span data-ttu-id="feab9-108">各種の構成には、いくつか考慮すべき問題があります。</span><span class="sxs-lookup"><span data-stu-id="feab9-108">There are several issues to consider with each type of configuration:</span></span>

  - <span data-ttu-id="feab9-109">**IPv4 のみ**   IPv6 は IPv4 アドレスが不足しているために作成されました。</span><span class="sxs-lookup"><span data-stu-id="feab9-109">**IPv4 only**   IPv6 was created because the world is running out of IPv4 addresses.</span></span> <span data-ttu-id="feab9-110">最終的には、IPv6 は世界中で完全にサポートされますが、現時点では、企業が通信する必要がある多くの会社やデバイスは IPv6 をサポートしていませんが、しばらくの間、そうでない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="feab9-110">Ultimately, IPv6 will be fully supported worldwide, but at this time, many companies and devices that your enterprise might need to communicate with do not yet support IPv6, and may not for some time.</span></span> <span data-ttu-id="feab9-111">IPv4 のみの構成は、Lync Server の実装が、既存のほとんどのデバイスと通信できるようにするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="feab9-111">An IPv4-only configuration will help to ensure that your Lync Server implementation can communicate with most existing devices.</span></span>

  - <span data-ttu-id="feab9-112">**IPv6 のみ**   これに対して、現時点では、IPv6 を完全に実装すると、多くの既存のデバイスとの通信が除外されます。</span><span class="sxs-lookup"><span data-stu-id="feab9-112">**IPv6 only**   Conversely, a full IPv6 implementation, at this time, will exclude communication with many existing devices.</span></span>

  - <span data-ttu-id="feab9-113">**デュアルスタック**   デュアルスタックは、IPv4 アドレスと IPv6 アドレスの両方が有効になっているネットワークです。</span><span class="sxs-lookup"><span data-stu-id="feab9-113">**Dual Stack**   Dual stack is a network where both IPv4 and IPv6 addresses are enabled.</span></span> <span data-ttu-id="feab9-114">この構成は Lync Server 2013 でサポートされているため、ほとんどの場合、フル IPv4 からフル-IPv6 への移行は数年で完了します。</span><span class="sxs-lookup"><span data-stu-id="feab9-114">This configuration is supported in Lync Server 2013 because in most cases the transition from full-IPv4 to full-IPv6 will take several years.</span></span>

<span data-ttu-id="feab9-115">以下のセクションでは、Lync Server のさまざまな機能について、これらの3つの構成の互換性についての概要を示します。</span><span class="sxs-lookup"><span data-stu-id="feab9-115">The following sections outline the compatibility among these three configurations for various Lync Server features.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="feab9-p104">クライアントまたはサーバーを IPv6 のみの構成にすることは、試験や検証の目的でのみサポートされています。IPv6 のみの構成は運用展開ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="feab9-p104">Client or server configuration with IPv6 only is supported only for lab or validation purposes. IPv6 only configuration is not supported in the production deployment.</span></span>



</div>

<div>

## <a name="client-registration"></a><span data-ttu-id="feab9-118">クライアントの登録</span><span class="sxs-lookup"><span data-stu-id="feab9-118">Client Registration</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feab9-119">クライアント エンドポイント ネットワーク</span><span class="sxs-lookup"><span data-stu-id="feab9-119">Client endpoint network</span></span></th>
<th><span data-ttu-id="feab9-120">サーバー ネットワーク</span><span class="sxs-lookup"><span data-stu-id="feab9-120">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feab9-121">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-121">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-122">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-122">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-123">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-123">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-124">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-124">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-125">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-125">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-126">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-126">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-127">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-127">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-128">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-128">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-129">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-129">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-130">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-130">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-131">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-131">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-132">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-132">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-133">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-133">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-134">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-134">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="peer-to-peer-client"></a><span data-ttu-id="feab9-135">ピアツーピア クライアント</span><span class="sxs-lookup"><span data-stu-id="feab9-135">Peer-to-Peer Client</span></span>

<span data-ttu-id="feab9-p105">ピアツーピア通信には、オーディオ、音声ビデオ、アプリケーション共有、ファイル転送などがあります。両方のクライアントが正常に登録された後、次の組み合わせがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="feab9-p105">Peer-to-peer communications include audio, audio/video, application sharing, and file transfer. After both clients have successfully registered, the following combinations are supported.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feab9-138">クライアント エンドポイント 1</span><span class="sxs-lookup"><span data-stu-id="feab9-138">Client endpoint 1</span></span></th>
<th><span data-ttu-id="feab9-139">クライアント エンドポイント 2</span><span class="sxs-lookup"><span data-stu-id="feab9-139">Client endpoint 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feab9-140">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-140">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-141">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-141">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-142">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-142">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-143">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-143">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-144">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-144">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-145">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-145">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-146">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-147">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-147">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-148">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-149">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="conferencing"></a><span data-ttu-id="feab9-150">会議</span><span class="sxs-lookup"><span data-stu-id="feab9-150">Conferencing</span></span>

<span data-ttu-id="feab9-151">会議には、音声/ビデオ、アプリケーション共有、データコラボレーション (whiteboarding とファイル共有) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feab9-151">Conferencing includes audio/video, application sharing, and data collaboration (whiteboarding and file sharing).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feab9-152">クライアント エンドポイント ネットワーク</span><span class="sxs-lookup"><span data-stu-id="feab9-152">Client endpoint network</span></span></th>
<th><span data-ttu-id="feab9-153">サーバー ネットワーク</span><span class="sxs-lookup"><span data-stu-id="feab9-153">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feab9-154">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-154">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-155">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-155">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-156">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-156">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-157">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-157">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-158">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-158">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-159">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-159">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-160">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-160">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-161">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-161">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-162">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-162">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-163">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-163">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-164">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-164">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-165">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-165">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-166">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-166">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-167">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-167">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="mediation-serverpstn"></a><span data-ttu-id="feab9-168">仲介サーバー/PSTN</span><span class="sxs-lookup"><span data-stu-id="feab9-168">Mediation Server/PSTN</span></span>

<span data-ttu-id="feab9-169">トラフィックが IPv6 インターフェイスを通過している場合、Lync Server 2013 は、公衆交換電話網 (PSTN) 通話のメディアバイパスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="feab9-169">Lync Server 2013 does not support media bypass for public switched telephone network (PSTN) calls if the traffic is through an IPv6 interface.</span></span> <span data-ttu-id="feab9-170">メディア バイパスが必要な場合は、PSTN ゲートウェイを IPv4 に構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="feab9-170">If media bypass is required, we recommend that the PSTN gateway is configured to IPv4.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feab9-171">プライマリ インターフェイス\*</span><span class="sxs-lookup"><span data-stu-id="feab9-171">Primary interface\*</span></span></th>
<th><span data-ttu-id="feab9-172">PSTN インターフェイス (仲介サーバー上)</span><span class="sxs-lookup"><span data-stu-id="feab9-172">PSTN interface (on Mediation Server)</span></span></th>
<th><span data-ttu-id="feab9-173">PSTN ゲートウェイの設定</span><span class="sxs-lookup"><span data-stu-id="feab9-173">PSTN gateway setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feab9-174">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-174">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-175">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-175">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-176">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-176">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-177">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-177">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-178">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-178">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-179">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-179">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-180">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-180">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-181">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-181">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-182">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-182">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="feab9-183">\* プライマリインターフェイスは、Lync Server コンポーネントと通信するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="feab9-183">\* The primary interface is the interface that communicates with the Lync Server components.</span></span>

</div>

<div>

## <a name="remote-user-peer-to-peer-communications"></a><span data-ttu-id="feab9-184">リモート ユーザーのピアツーピア通信</span><span class="sxs-lookup"><span data-stu-id="feab9-184">Remote User Peer-to-Peer Communications</span></span>

<span data-ttu-id="feab9-185">リモート ユーザーとのピアツーピア通信には、インスタント メッセージング、音声ビデオ、アプリケーション共有、およびファイル転送が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feab9-185">Peer-to-peer communications with remote users include instant messaging, audio/video, application sharing, and file transfer.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feab9-186">リモート ユーザー ネットワーク</span><span class="sxs-lookup"><span data-stu-id="feab9-186">Remote user network</span></span></th>
<th><span data-ttu-id="feab9-187">エッジ サーバー (外部エッジ)</span><span class="sxs-lookup"><span data-stu-id="feab9-187">Edge server (External edge)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feab9-188">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-188">IPv4</span></span></p></td>
<td><p><span data-ttu-id="feab9-189">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-189">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-190">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-190">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-191">IPv4</span><span class="sxs-lookup"><span data-stu-id="feab9-191">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-192">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-192">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="feab9-193">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-193">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-194">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-194">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-195">デュアル スタック</span><span class="sxs-lookup"><span data-stu-id="feab9-195">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-196">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-196">IPv6</span></span></p></td>
<td><p><span data-ttu-id="feab9-197">IPv6</span><span class="sxs-lookup"><span data-stu-id="feab9-197">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-pool-and-edge-pool-configuration"></a><span data-ttu-id="feab9-198">フロントエンド プールとエッジ プールの構成</span><span class="sxs-lookup"><span data-stu-id="feab9-198">Front End Pool and Edge Pool Configuration</span></span>

<span data-ttu-id="feab9-199">次の表は、フロントエンドサーバープールと内部エッジサーバープールの間のサポートマトリックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="feab9-199">The following table shows the support matrix between the Front End Server pool and the internal Edge Server pool.</span></span>

### <a name="front-end-pool-and-edge-pool-internal-edge-matrix"></a><span data-ttu-id="feab9-200">フロントエンド プールとエッジ プール (内部エッジ) のマトリックス</span><span class="sxs-lookup"><span data-stu-id="feab9-200">Front End Pool and Edge Pool (Internal Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="feab9-201"><strong>エッジ プール: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-201"><strong>Edge Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-202"><strong>エッジ プール: デュアル スタック</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-202"><strong>Edge Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-203"><strong>エッジ プール: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-203"><strong>Edge Pool: IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-204"><strong>フロントエンド プール: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-204"><strong>Front End Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-205">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-205">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-206">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-207">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-208"><strong>フロントエンド プール: デュアル スタック</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-208"><strong>Front End Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-209">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-210">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-211">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-212"><strong>フロントエンド プール: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-212"><strong>Front End Pool: IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-213">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-213">No</span></span></p></td>
<td><p><span data-ttu-id="feab9-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-214">No</span></span></p></td>
<td><p><span data-ttu-id="feab9-215">はい\*</span><span class="sxs-lookup"><span data-stu-id="feab9-215">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="feab9-216">\* この組み合わせは、ラボ環境でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="feab9-216">\* Use this combination only in a lab environment.</span></span>

<span data-ttu-id="feab9-217">次のテーブルは、内部エッジ インターフェイスと外部エッジ インターフェイスの組み合わせのサポート マトリックスです。</span><span class="sxs-lookup"><span data-stu-id="feab9-217">The following table is a matrix of the supported combinations of internal and external edge interfaces.</span></span>

### <a name="edge-pool-internal-edge-and-edge-pool-external-edge-matrix"></a><span data-ttu-id="feab9-218">エッジ プール (内部エッジ) とエッジ プール (外部エッジ) のマトリックス</span><span class="sxs-lookup"><span data-stu-id="feab9-218">Edge Pool (Internal Edge) and Edge pool (External Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="feab9-219"><strong>エッジ プール (外部エッジ): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-219"><strong>Edge Pool (External Edge) : IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-220"><strong>エッジ プール (外部エッジ): デュアル スタック</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-220"><strong>Edge Pool (External Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-221"><strong>エッジ プール (外部エッジ): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-221"><strong>Edge Pool (External Edge): IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-222"><strong>エッジ プール (内部エッジ): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-222"><strong>Edge Pool (Internal Edge): IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-223">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-223">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-224">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-225">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-225">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feab9-226"><strong>エッジ プール (内部エッジ): デュアル スタック</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-226"><strong>Edge Pool (Internal Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-227">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-227">No</span></span></p></td>
<td><p><span data-ttu-id="feab9-228">はい</span><span class="sxs-lookup"><span data-stu-id="feab9-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="feab9-229">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-229">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feab9-230"><strong>エッジ プール (内部エッジ): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="feab9-230"><strong>Edge Pool (Internal Edge): IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="feab9-231">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-231">No</span></span></p></td>
<td><p><span data-ttu-id="feab9-232">いいえ</span><span class="sxs-lookup"><span data-stu-id="feab9-232">No</span></span></p></td>
<td><p><span data-ttu-id="feab9-233">はい\*</span><span class="sxs-lookup"><span data-stu-id="feab9-233">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="feab9-234">\* この組み合わせは、ラボ環境でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="feab9-234">\* Use this combination only in a lab environment.</span></span>

</div>

<div>

## <a name="advanced-enterprise-voice-support-for-ipv6"></a><span data-ttu-id="feab9-235">IPv6 の高度なエンタープライズ VoIP のサポート</span><span class="sxs-lookup"><span data-stu-id="feab9-235">Advanced Enterprise Voice Support for IPv6</span></span>

<span data-ttu-id="feab9-236">通話受付管理 (CAC)、拡張 9-1-1 (E9-1-1)、メディア バイパスなどの展開は、IPv4 のみ、またはデュアル スタック実装として構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="feab9-236">Deployments that include call admission control (CAC), Enhanced 9-1-1 (E9-1-1), or media bypass must be configured as IPv4 only or as a dual-stacked implementation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="feab9-237">デュアルスタック展開では、Lync クライアントが IPv6 を使って Lync サーバーに接続している場合でも、Lync では、E9-1 をサポートする適切な IPv4 アドレスをマッピングすることが最善に行われます。</span><span class="sxs-lookup"><span data-stu-id="feab9-237">In a dual-stacked deployment, even if a Lync client connects to a Lync Server by using IPv6, Lync will make a best effort to map an appropriate IPv4 address to support E9-1-1.</span></span>



</div>

<span data-ttu-id="feab9-238">IPv6 アドレスを使用した位置情報サービスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="feab9-238">Location Information service with IPv6 addresses is not supported.</span></span>

<span data-ttu-id="feab9-p107">Exchange ユニファイド メッセージング (UM) では IPv6 をサポートしていません。Exchange UM の場合は、DNS 解決が IPv6 アドレスを返さないことを確認します。IPv6 を使用すると、通話がボイス メールに送信されたときに障害が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="feab9-p107">Exchange Unified Messaging (UM) does not support IPv6. For Exchange UM, be sure that DNS resolution does not return an IPv6 address. Using IPv6 may cause failure when calls are sent to voice mail.</span></span>

</div>

<div>

## <a name="other-lync-server-2013-feature-support-for-ipv6"></a><span data-ttu-id="feab9-242">IPv6 向けのその他の Lync Server 2013 機能のサポート</span><span class="sxs-lookup"><span data-stu-id="feab9-242">Other Lync Server 2013 Feature Support for IPv6</span></span>

<span data-ttu-id="feab9-243">前に説明した機能とコンポーネントに加えて、Lync Server 2013 では、次の機能の IPv6 がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="feab9-243">In addition to the features and components mentioned previously, Lync Server 2013 supports IPv6 for the following features:</span></span>

  - <span data-ttu-id="feab9-244">**常設チャット**</span><span class="sxs-lookup"><span data-stu-id="feab9-244">**Persistent Chat**</span></span>
    
    <span data-ttu-id="feab9-245">"トポロジビルダー" を使用して、常設チャットの IPv6 を構成します。</span><span class="sxs-lookup"><span data-stu-id="feab9-245">You configure IPv6 for Persistent Chat by using Topology Builder.</span></span> <span data-ttu-id="feab9-246">常設チャットの設定の詳細については、「常設チャットサーバーのマニュアルの展開」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="feab9-246">For details about configuring Persistent Chat, see the Deploying Persistent Chat Server documentation.</span></span>

  - <span data-ttu-id="feab9-247">**Quality of Experience (QoE) と通話詳細記録 (CDR) のレポート**</span><span class="sxs-lookup"><span data-stu-id="feab9-247">**Quality of Experience (QoE) and call detail recording (CDR) reports**</span></span>
    
    <span data-ttu-id="feab9-248">IPv4 と IPv6 のいずれの場合でも、監視レポートには監視サーバー データベースに格納されている IP アドレスがそのまま含まれます。</span><span class="sxs-lookup"><span data-stu-id="feab9-248">Monitoring reports include the IP address as it is stored in the Monitoring Server database, whether of type IPv4 or IPv6.</span></span>

<span data-ttu-id="feab9-249"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="feab9-249"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

