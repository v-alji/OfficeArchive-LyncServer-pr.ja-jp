---
title: 'Lync Server 2013: Session テーブル'
description: 'Lync Server 2013: セッションテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441817"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="9c91d-103">Lync Server 2013 の Session テーブル</span><span class="sxs-lookup"><span data-stu-id="9c91d-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c91d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c91d-104">

<span> </span></span></span>

<span data-ttu-id="9c91d-105">_**最終更新日:** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="9c91d-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="9c91d-106">各レコードは、オーディオまたはオーディオとビデオを含む1つのセッションを表します。</span><span class="sxs-lookup"><span data-stu-id="9c91d-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="9c91d-107">セッションに関する全体的な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c91d-107">It contains overall information about the session.</span></span> <span data-ttu-id="9c91d-108">セッションは、2つのエンドポイント間のオーディオまたはビデオセッションの開始プロトコル (SIP) ダイアログとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c91d-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9c91d-110"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9c91d-111"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9c91d-112"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="9c91d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c91d-115">Primary</span><span class="sxs-lookup"><span data-stu-id="9c91d-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="9c91d-116"><a href="lync-server-2013-dialog-table.md">Lync Server 2013 のダイアログテーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-118">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-118">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-119">Primary</span><span class="sxs-lookup"><span data-stu-id="9c91d-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="9c91d-120"><a href="lync-server-2013-dialog-table.md">Lync Server 2013 のダイアログテーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-122">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-122">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-123">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-124">会議キー。</span><span class="sxs-lookup"><span data-stu-id="9c91d-124">Conference key.</span></span> <span data-ttu-id="9c91d-125"><a href="lync-server-2013-conference-table.md">Lync Server 2013 の会議テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-127">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-127">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-128">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-129">相関関係キー。</span><span class="sxs-lookup"><span data-stu-id="9c91d-129">Correlation key.</span></span> <span data-ttu-id="9c91d-130"><a href="lync-server-2013-sessioncorrelation-table.md">Lync Server 2013 の Sessioncorrelation テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-131"><strong>このカテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-132">bit</span><span class="sxs-lookup"><span data-stu-id="9c91d-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9c91d-133">ダイアログカテゴリ0は Lync Server、仲介サーバーの区間、1は、PSTN ゲートウェイ区間への仲介サーバーです。</span><span class="sxs-lookup"><span data-stu-id="9c91d-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-135">bit</span><span class="sxs-lookup"><span data-stu-id="9c91d-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9c91d-136">通話がバイパスされたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="9c91d-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-137"><strong>Mediabypasswarnings フラグ</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-138">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9c91d-139">このフィールドは、バイパス Id が一致した場合でも、着信がバイパスされなかった理由を示します (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="9c91d-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="9c91d-140">Lync Server の場合、1つの値のみが定義されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="9c91d-141">0x0001 –既定のネットワークアダプターの不明なバイパス ID。</span><span class="sxs-lookup"><span data-stu-id="9c91d-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-143">datetime</span><span class="sxs-lookup"><span data-stu-id="9c91d-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9c91d-144">通話開始時刻。</span><span class="sxs-lookup"><span data-stu-id="9c91d-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-146">datetime</span><span class="sxs-lookup"><span data-stu-id="9c91d-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9c91d-147">通話終了時刻。</span><span class="sxs-lookup"><span data-stu-id="9c91d-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-149">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-149">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-150">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-151">発信者のプール。</span><span class="sxs-lookup"><span data-stu-id="9c91d-151">The pool of the caller.</span></span> <span data-ttu-id="9c91d-152"><a href="lync-server-2013-pool-table.md">Lync Server 2013 のプールテーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-154">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-154">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-155">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-156">通話受信者のプール。</span><span class="sxs-lookup"><span data-stu-id="9c91d-156">The pool of the call receiver.</span></span> <span data-ttu-id="9c91d-157"><a href="lync-server-2013-pool-table.md">Lync Server 2013 のプールテーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-159">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-159">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-160">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-161">受信エンドポイントの SIP p-アサートされた id (PAI) の SIP URI。</span><span class="sxs-lookup"><span data-stu-id="9c91d-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="9c91d-162"><a href="lync-server-2013-user-table.md">Lync Server 2013 のユーザーテーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-164">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-164">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-165">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-166">発信者の URI。</span><span class="sxs-lookup"><span data-stu-id="9c91d-166">Caller’s URI.</span></span> <span data-ttu-id="9c91d-167"><a href="lync-server-2013-user-table.md">Lync Server 2013 のユーザーテーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-169">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-169">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-170">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-171">発信者のエンドポイント。</span><span class="sxs-lookup"><span data-stu-id="9c91d-171">Caller’s endpoint.</span></span> <span data-ttu-id="9c91d-172"><a href="lync-server-2013-endpoint-table.md">Lync Server 2013 のエンドポイントテーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-174">bit</span><span class="sxs-lookup"><span data-stu-id="9c91d-174">bit</span></span></p></td>
<td><p><span data-ttu-id="9c91d-175">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-176">発信者のユーザーエージェント。</span><span class="sxs-lookup"><span data-stu-id="9c91d-176">Caller’s user agent.</span></span> <span data-ttu-id="9c91d-177"><a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="9c91d-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-179">smallint</span><span class="sxs-lookup"><span data-stu-id="9c91d-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9c91d-180">この通話の優先度。</span><span class="sxs-lookup"><span data-stu-id="9c91d-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-182">bit</span><span class="sxs-lookup"><span data-stu-id="9c91d-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9c91d-183">この列は廃止され、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="9c91d-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="9c91d-184">代わりに、この情報はメディアラインベースごとに報告されます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="9c91d-185">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 で MediaLine の表</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c91d-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-187">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-187">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-188">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-189">P-アサート済み-通話を発信したユーザーの Id です。</span><span class="sxs-lookup"><span data-stu-id="9c91d-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="9c91d-190">P がアサートされた Id (PAI) を使って、通話を発信したユーザーの実際の id を伝えます。</span><span class="sxs-lookup"><span data-stu-id="9c91d-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-192">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-192">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-193">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-194">通話を受信したエンドポイント。</span><span class="sxs-lookup"><span data-stu-id="9c91d-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c91d-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-196">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-196">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-197">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-198">通話を受信したユーザーが採用したユーザーエージェント。</span><span class="sxs-lookup"><span data-stu-id="9c91d-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="9c91d-199">ユーザーエージェントは、クライアントエンドポイントデバイスを表します。</span><span class="sxs-lookup"><span data-stu-id="9c91d-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c91d-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c91d-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c91d-201">int</span><span class="sxs-lookup"><span data-stu-id="9c91d-201">int</span></span></p></td>
<td><p><span data-ttu-id="9c91d-202">外部</span><span class="sxs-lookup"><span data-stu-id="9c91d-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c91d-203">通話を受信したユーザーの SIP URI。</span><span class="sxs-lookup"><span data-stu-id="9c91d-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9c91d-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c91d-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

