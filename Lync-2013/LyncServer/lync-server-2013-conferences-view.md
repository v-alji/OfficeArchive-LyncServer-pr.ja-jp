---
title: 'Lync Server 2013: 会議ビュー'
description: 'Lync Server 2013: 会議ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434425"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="b4b78-103">Lync Server 2013 での会議ビュー</span><span class="sxs-lookup"><span data-stu-id="b4b78-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4b78-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4b78-104">

<span> </span></span></span>

<span data-ttu-id="b4b78-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b4b78-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b4b78-106">会議ビューには、会議に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="b4b78-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="b4b78-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="b4b78-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4b78-108">列</span><span class="sxs-lookup"><span data-stu-id="b4b78-108">Column</span></span></th>
<th><span data-ttu-id="b4b78-109">データ型</span><span class="sxs-lookup"><span data-stu-id="b4b78-109">Data Type</span></span></th>
<th><span data-ttu-id="b4b78-110">詳細</span><span class="sxs-lookup"><span data-stu-id="b4b78-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b4b78-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b4b78-113">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="b4b78-113">Time of session request.</span></span> <span data-ttu-id="b4b78-114">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4b78-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="b4b78-115">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4b78-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-117">int</span><span class="sxs-lookup"><span data-stu-id="b4b78-117">int</span></span></p></td>
<td><p><span data-ttu-id="b4b78-118">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="b4b78-118">ID number to identify the session.</span></span> <span data-ttu-id="b4b78-119">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4b78-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="b4b78-120">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4b78-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b4b78-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-123">会議の URI。</span><span class="sxs-lookup"><span data-stu-id="b4b78-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b4b78-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-126">会議 URI の種類。</span><span class="sxs-lookup"><span data-stu-id="b4b78-126">Type of the conference URI.</span></span> <span data-ttu-id="b4b78-127">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4b78-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-129">長さ</span><span class="sxs-lookup"><span data-stu-id="b4b78-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="b4b78-130">定期的な会議に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4b78-130">Used for recurring conferences.</span></span> <span data-ttu-id="b4b78-131">定期的な会議の各インスタンスには、同じ ConferenceUri がありますが、ConfInstance は異なります。</span><span class="sxs-lookup"><span data-stu-id="b4b78-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-133">datetime</span><span class="sxs-lookup"><span data-stu-id="b4b78-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="b4b78-134">会議の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="b4b78-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-136">datetime</span><span class="sxs-lookup"><span data-stu-id="b4b78-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="b4b78-137">会議の終了時刻。</span><span class="sxs-lookup"><span data-stu-id="b4b78-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-138"><strong>オーガナイザーの Uri</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b4b78-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-140">会議を開催したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="b4b78-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-141"><strong>オーガナイザーの種類</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b4b78-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-143">会議を開催したユーザーの URI の種類です。</span><span class="sxs-lookup"><span data-stu-id="b4b78-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="b4b78-144">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4b78-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-145"><strong>組織のテナント</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b4b78-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-147">会議を開催したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="b4b78-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="b4b78-148">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4b78-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b78-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b4b78-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b4b78-151">会議をホストしているプールの完全修飾ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="b4b78-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b78-152"><strong>フラッグ</strong></span><span class="sxs-lookup"><span data-stu-id="b4b78-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b78-153">smallint</span><span class="sxs-lookup"><span data-stu-id="b4b78-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="b4b78-154">会議の属性が含まれているビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b4b78-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="b4b78-155">値の例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b4b78-155">Possible values are:</span></span></p>
<p><span data-ttu-id="b4b78-156">0X01 –代理トランザクション</span><span class="sxs-lookup"><span data-stu-id="b4b78-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b4b78-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4b78-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

