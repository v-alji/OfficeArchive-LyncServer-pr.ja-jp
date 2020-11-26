---
title: Lync Server 2013 IPsec の例外
description: Lync Server 2013 IPsec の例外。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426726"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="96efd-103">Lync Server 2013 での IPsec の例外</span><span class="sxs-lookup"><span data-stu-id="96efd-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96efd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96efd-104">

<span> </span></span></span>

<span data-ttu-id="96efd-105">_**最終更新日:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="96efd-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="96efd-106">インターネットプロトコルセキュリティ (IPsec 4301-4309) が展開されているエンタープライズネットワークの場合、オーディオ、ビデオ、およびパノラマビデオの配信に使用するポートの範囲で IPsec を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96efd-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="96efd-107">この操作を行うと、IPsec のネゴシエーションによってメディア用ポートの割り当てに遅延が生じるのを避けることができます。</span><span class="sxs-lookup"><span data-stu-id="96efd-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="96efd-108">次の表に、推奨される IPsec 例外設定を示します。</span><span class="sxs-lookup"><span data-stu-id="96efd-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="96efd-109">推奨される IPSec 例外設定</span><span class="sxs-lookup"><span data-stu-id="96efd-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96efd-110">ルール名</span><span class="sxs-lookup"><span data-stu-id="96efd-110">Rule name</span></span></th>
<th><span data-ttu-id="96efd-111">発信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="96efd-111">Source IP</span></span></th>
<th><span data-ttu-id="96efd-112">送信先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="96efd-112">Destination IP</span></span></th>
<th><span data-ttu-id="96efd-113">プロトコル</span><span class="sxs-lookup"><span data-stu-id="96efd-113">Protocol</span></span></th>
<th><span data-ttu-id="96efd-114">送信元ポート</span><span class="sxs-lookup"><span data-stu-id="96efd-114">Source port</span></span></th>
<th><span data-ttu-id="96efd-115">宛先ポート</span><span class="sxs-lookup"><span data-stu-id="96efd-115">Destination port</span></span></th>
<th><span data-ttu-id="96efd-116">認証要件</span><span class="sxs-lookup"><span data-stu-id="96efd-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96efd-117">内部音声ビデオ エッジ サーバー/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-118">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-118">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-119">内部音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="96efd-120">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-121">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-121">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-122">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-122">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-123">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-124">外部音声ビデオ エッジ サーバー/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-125">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-125">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-126">外部音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="96efd-127">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-128">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-128">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-129">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-129">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-130">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-131">内部音声ビデオ エッジ サーバー/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-132">内部音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="96efd-133">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-133">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-134">UDP &amp; TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-135">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-135">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-136">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-136">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-137">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-138">外部音声ビデオ エッジ サーバー/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-139">外部音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="96efd-140">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-140">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-141">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-142">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-142">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-143">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-143">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-144">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-145">仲介サーバー/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-146">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-146">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-147">仲介</span><span class="sxs-lookup"><span data-stu-id="96efd-147">Mediation</span></span></p>
<p><span data-ttu-id="96efd-148">サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="96efd-149">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-150">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-150">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-151">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-151">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-152">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-153">仲介サーバー/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-154">仲介</span><span class="sxs-lookup"><span data-stu-id="96efd-154">Mediation</span></span></p>
<p><span data-ttu-id="96efd-155">サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="96efd-156">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-156">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-157">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-158">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-158">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-159">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-159">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-160">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-161">会議アテンダント/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-162">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-162">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-163">会議アテンダントを実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="96efd-164">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-165">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-165">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-166">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-166">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-167">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-168">会議アテンダント/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-169">会議アテンダントを実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="96efd-170">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-170">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-171">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-172">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-172">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-173">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-173">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-174">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-175">音声ビデオ会議サーバー/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-176">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-176">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-177">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="96efd-178">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-179">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-179">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-180">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-180">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-181">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-182">音声ビデオ会議/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-183">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="96efd-184">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-184">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-185">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-186">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-186">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-187">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-187">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-188">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-189">Exchange/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-190">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-190">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-191">Exchange ユニファイド メッセージング</span><span class="sxs-lookup"><span data-stu-id="96efd-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="96efd-192">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-193">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-193">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-194">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-194">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-195">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-196">アプリケーション共有サーバー/受信</span><span class="sxs-lookup"><span data-stu-id="96efd-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-197">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-197">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-198">アプリケーション共有サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="96efd-199">TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-200">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-200">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-201">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-201">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-202">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-203">アプリケーション共有サーバー/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-204">アプリケーション共有サーバー</span><span class="sxs-lookup"><span data-stu-id="96efd-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="96efd-205">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-205">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-206">TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-207">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-207">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-208">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-208">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-209">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96efd-210">Exchange/送信</span><span class="sxs-lookup"><span data-stu-id="96efd-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="96efd-211">Exchange ユニファイド メッセージング</span><span class="sxs-lookup"><span data-stu-id="96efd-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="96efd-212">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-212">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-213">UDP および TCP</span><span class="sxs-lookup"><span data-stu-id="96efd-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="96efd-214">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-214">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-215">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-215">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-216">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96efd-217">クライアント</span><span class="sxs-lookup"><span data-stu-id="96efd-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="96efd-218">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-218">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-219">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-219">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-220">UDP</span><span class="sxs-lookup"><span data-stu-id="96efd-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="96efd-221">指定メディア ポート範囲</span><span class="sxs-lookup"><span data-stu-id="96efd-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="96efd-222">任意</span><span class="sxs-lookup"><span data-stu-id="96efd-222">Any</span></span></p></td>
<td><p><span data-ttu-id="96efd-223">認証しない</span><span class="sxs-lookup"><span data-stu-id="96efd-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96efd-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96efd-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

