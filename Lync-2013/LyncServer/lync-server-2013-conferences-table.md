---
title: 'Lync Server 2013: Conferences テーブル'
description: 'Lync Server 2013: 会議テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399381"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="f7ebd-103">Lync Server 2013 の Conferences テーブル</span><span class="sxs-lookup"><span data-stu-id="f7ebd-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7ebd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7ebd-104">

<span> </span></span></span>

<span data-ttu-id="f7ebd-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f7ebd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f7ebd-106">この表の各レコードには、1人の会議に関する通話の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7ebd-107">列</span><span class="sxs-lookup"><span data-stu-id="f7ebd-107">Column</span></span></th>
<th><span data-ttu-id="f7ebd-108">データ型</span><span class="sxs-lookup"><span data-stu-id="f7ebd-108">Data Type</span></span></th>
<th><span data-ttu-id="f7ebd-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="f7ebd-109">Key/Index</span></span></th>
<th><span data-ttu-id="f7ebd-110">詳細</span><span class="sxs-lookup"><span data-stu-id="f7ebd-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7ebd-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-112">datetime</span><span class="sxs-lookup"><span data-stu-id="f7ebd-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-113">Primary</span><span class="sxs-lookup"><span data-stu-id="f7ebd-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-114">会議出席依頼が CDR エージェントによってキャプチャされた時刻。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="f7ebd-115">会議インスタンスを一意に識別するために、主キーとしてのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7ebd-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-117">int</span><span class="sxs-lookup"><span data-stu-id="f7ebd-117">int</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-118">Primary</span><span class="sxs-lookup"><span data-stu-id="f7ebd-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-119">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-119">ID number to identify the session.</span></span> <span data-ttu-id="f7ebd-120">電話会議インスタンスを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7ebd-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-122">int</span><span class="sxs-lookup"><span data-stu-id="f7ebd-122">int</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-123">外部</span><span class="sxs-lookup"><span data-stu-id="f7ebd-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-124">会議の URI。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-124">Conference URI.</span></span> <span data-ttu-id="f7ebd-125">詳細については、「 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 の ConferenceUris テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7ebd-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-127">長さ</span><span class="sxs-lookup"><span data-stu-id="f7ebd-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f7ebd-128">定期的な会議に便利。定期的な会議の各インスタンスには、同じ <strong>ConferenceUri</strong>がありますが、別の <strong>confinstance</strong>があります。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7ebd-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-130">datetime</span><span class="sxs-lookup"><span data-stu-id="f7ebd-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f7ebd-131">会議の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7ebd-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-133">datetime</span><span class="sxs-lookup"><span data-stu-id="f7ebd-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f7ebd-134">会議の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7ebd-135"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-136">int</span><span class="sxs-lookup"><span data-stu-id="f7ebd-136">int</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-137">外部</span><span class="sxs-lookup"><span data-stu-id="f7ebd-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-138">会議がキャプチャされたプールを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="f7ebd-139">詳細については、「 <a href="lync-server-2013-pools-table.md">Lync Server 2013 のプールテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7ebd-140"><strong>オーガナイザー Erid</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-141">Int</span><span class="sxs-lookup"><span data-stu-id="f7ebd-141">Int</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-142">外部</span><span class="sxs-lookup"><span data-stu-id="f7ebd-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f7ebd-143">この会議の開催者の URI を識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="f7ebd-144">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7ebd-145"><strong>フラッグ</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-146">smallint</span><span class="sxs-lookup"><span data-stu-id="f7ebd-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f7ebd-147">会議の属性が含まれているビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="f7ebd-148">値の例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f7ebd-149">0X01</span><span class="sxs-lookup"><span data-stu-id="f7ebd-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="f7ebd-150">Synthetic</span><span class="sxs-lookup"><span data-stu-id="f7ebd-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="f7ebd-151">トランザクション</span><span class="sxs-lookup"><span data-stu-id="f7ebd-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7ebd-152"><strong>処理</strong></span><span class="sxs-lookup"><span data-stu-id="f7ebd-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="f7ebd-153">bit</span><span class="sxs-lookup"><span data-stu-id="f7ebd-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f7ebd-154">監視サービスで使用される内部フィールド。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="f7ebd-155">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f7ebd-156">\* ほとんどのセッションでは、SessionIdSeq の値は1になります。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="f7ebd-157">2つのセッションがまったく同じ時刻に開始された場合、1つのセッションの SessionIdSeq は1になり、残りのセッションは2になります。</span><span class="sxs-lookup"><span data-stu-id="f7ebd-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="f7ebd-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7ebd-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

