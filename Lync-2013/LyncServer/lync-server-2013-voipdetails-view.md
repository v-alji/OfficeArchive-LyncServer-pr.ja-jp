---
title: 'Lync Server 2013: VoIPDetails ビュー'
description: 'Lync Server 2013: VoIPDetails ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446185"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="e9015-103">Lync Server 2013 の VoIPDetails ビュー</span><span class="sxs-lookup"><span data-stu-id="e9015-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9015-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9015-104">

<span> </span></span></span>

<span data-ttu-id="e9015-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e9015-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e9015-106">VoIPDetails ビューには、ピアツーピアセッションに関する情報が格納されます。これは、少なくとも1人のユーザーが VoIP ユーザーである場合です。</span><span class="sxs-lookup"><span data-stu-id="e9015-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="e9015-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e9015-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e9015-108">VoIPDetails ビューには、 <A href="lync-server-2013-sessiondetails-view.md">Lync Server 2013 の Sessiondetails ビュー</A> のすべての列に加えて、以下の列も含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9015-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9015-109">列</span><span class="sxs-lookup"><span data-stu-id="e9015-109">Column</span></span></th>
<th><span data-ttu-id="e9015-110">データ型</span><span class="sxs-lookup"><span data-stu-id="e9015-110">Data Type</span></span></th>
<th><span data-ttu-id="e9015-111">詳細</span><span class="sxs-lookup"><span data-stu-id="e9015-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9015-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e9015-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="e9015-114">セッションを開始したユーザーの電話の URI。</span><span class="sxs-lookup"><span data-stu-id="e9015-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9015-115"><strong>電話番号</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e9015-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="e9015-117">セッションに参加したユーザーの電話の URI。</span><span class="sxs-lookup"><span data-stu-id="e9015-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9015-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e9015-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="e9015-120">セッションを切断したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="e9015-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9015-121"><strong>Uritん</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-123">セッションを切断したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="e9015-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="e9015-124">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9015-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9015-125"><strong>テナント</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-127">セッションを切断したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="e9015-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9015-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e9015-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="e9015-130">セッションを切断したユーザーの電話の URI。</span><span class="sxs-lookup"><span data-stu-id="e9015-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9015-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-133">セッションを開始したユーザーによって使用された仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="e9015-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9015-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-136">セッションに参加したユーザーが使用した仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="e9015-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9015-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-139">セッションを開始したユーザーによって使用されたゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="e9015-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9015-140"><strong>ToGateway</strong></span><span class="sxs-lookup"><span data-stu-id="e9015-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="e9015-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e9015-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e9015-142">セッションに参加したユーザーが使用したゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="e9015-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e9015-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9015-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

