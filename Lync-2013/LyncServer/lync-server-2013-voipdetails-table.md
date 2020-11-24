---
title: 'Lync Server 2013: VoipDetails テーブル'
description: 'Lync Server 2013: VoipDetails テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397887"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="6cc4e-103">Lync Server 2013 の VoipDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="6cc4e-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cc4e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cc4e-104">

<span> </span></span></span>

<span data-ttu-id="6cc4e-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6cc4e-106">各レコードは、少なくとも1人のユーザーが VoIP ユーザーである 1 2 パーティーの通話を表します。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cc4e-107">列</span><span class="sxs-lookup"><span data-stu-id="6cc4e-107">Column</span></span></th>
<th><span data-ttu-id="6cc4e-108">データ型</span><span class="sxs-lookup"><span data-stu-id="6cc4e-108">Data Type</span></span></th>
<th><span data-ttu-id="6cc4e-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="6cc4e-109">Key/Index</span></span></th>
<th><span data-ttu-id="6cc4e-110">詳細</span><span class="sxs-lookup"><span data-stu-id="6cc4e-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cc4e-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-112">datetime</span><span class="sxs-lookup"><span data-stu-id="6cc4e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-113">Primary</span><span class="sxs-lookup"><span data-stu-id="6cc4e-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-114">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-114">Time of session request.</span></span> <span data-ttu-id="6cc4e-115">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6cc4e-116">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc4e-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-118">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-118">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-119">Primary</span><span class="sxs-lookup"><span data-stu-id="6cc4e-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-120">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-120">ID number to identify the session.</span></span> <span data-ttu-id="6cc4e-121">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6cc4e-122">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc4e-123"><strong>Fromnumber Id</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-124">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-124">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-125">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-126">発信者の<strong>PhoneId</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="6cc4e-127">詳細については、「 <a href="lync-server-2013-phones-table.md">Lync Server 2013 で電話の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="6cc4e-128">Not NULL と <strong>Fromgatewayid</strong> が null でない場合は、発信者は PSTN ユーザーです。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc4e-129"><strong>Connected番号 Id</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-130">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-130">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-131">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-132">通話受信者の<strong>PhoneId</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="6cc4e-133">詳細については、「 <a href="lync-server-2013-phones-table.md">Lync Server 2013 で電話の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="6cc4e-134">Not NULL と <strong>Togatewayid</strong> が null でない場合は、通話レシーバーは PSTN ユーザーでした。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc4e-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-136">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-136">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-137">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-138">通話が発信される仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="6cc4e-139">詳細については、「 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 の Mediationservers の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc4e-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-141">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-141">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-142">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-143">仲介サーバーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="6cc4e-144">詳細については、「 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 の Mediationservers の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc4e-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-146">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-146">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-147">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-148">ゲートウェイ通話の発信元です。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-148">Gateway the call is coming from.</span></span> <span data-ttu-id="6cc4e-149">詳細については、「 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 のゲートウェイテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc4e-150"><strong>ToGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-151">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-151">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-152">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-153">通話の発信先のゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-153">Gateway the call is going to.</span></span> <span data-ttu-id="6cc4e-154">詳細については、「 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 のゲートウェイテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc4e-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-156">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-156">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-157">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-158">ユーザーが URI を持っている場合に、通話を切断したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="6cc4e-159">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc4e-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="6cc4e-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc4e-161">int</span><span class="sxs-lookup"><span data-stu-id="6cc4e-161">int</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-162">外部</span><span class="sxs-lookup"><span data-stu-id="6cc4e-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6cc4e-163">通話を切断した電話の ID が電話から切断されました。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="6cc4e-164">詳細については、「 <a href="lync-server-2013-phones-table.md">Lync Server 2013 で電話の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc4e-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6cc4e-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cc4e-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

