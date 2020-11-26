---
title: 'Lync Server 2013: メディアビュー'
description: 'Lync Server 2013: メディアビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446038"
---
# <a name="media-view-in-lync-server-2013"></a><span data-ttu-id="a6a6f-103">Lync Server 2013 でのメディアの表示</span><span class="sxs-lookup"><span data-stu-id="a6a6f-103">Media view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6a6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6a6f-104">

<span> </span></span></span>

<span data-ttu-id="a6a6f-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a6a6f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a6a6f-106">メディアビューには、ピアツーピアセッションで使用される1つのメディアの種類に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-106">The Media view stores information about one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="a6a6f-107">複数のメディアの種類を使用している場合は、1つのセッションがテーブル内の複数のレコードで表されます。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span> <span data-ttu-id="a6a6f-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6a6f-109">メディア表示は、セッションのメディア再生時間の計算に使用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-109">The Media view should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="a6a6f-110">このビューには、セッションでのメディア交換の通知の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-110">This view contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="a6a6f-111">メディア交換は INVITE 要求によって実行され、StartTime は招待が送信された時間を示します。この招待時刻は、メディアの開始時刻を意味するわけではありません。これは、セッションが受け入れられた後にのみメディアが開始されるためです。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-111">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the session is accepted.</span></span>



</div>

<span data-ttu-id="a6a6f-112">メディアビューには、 [Lync Server 2013 の Sessiondetails ビュー](lync-server-2013-sessiondetails-view.md) のすべての列に加えて、以下に示すものが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-112">The Media view contains all of the columns in the [SessionDetails view in Lync Server 2013](lync-server-2013-sessiondetails-view.md) in addition the ones listed below.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6a6f-113">列</span><span class="sxs-lookup"><span data-stu-id="a6a6f-113">Column</span></span></th>
<th><span data-ttu-id="a6a6f-114">データ型</span><span class="sxs-lookup"><span data-stu-id="a6a6f-114">Data Type</span></span></th>
<th><span data-ttu-id="a6a6f-115">詳細</span><span class="sxs-lookup"><span data-stu-id="a6a6f-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6a6f-116"><strong>メディア</strong></span><span class="sxs-lookup"><span data-stu-id="a6a6f-116"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="a6a6f-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a6a6f-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a6a6f-118">メディアの種類。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-118">Media type.</span></span> <span data-ttu-id="a6a6f-119">詳細については、「 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 の Medialist の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-119">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6a6f-120"><strong>MediaStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="a6a6f-120"><strong>MediaStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a6a6f-121">datetime</span><span class="sxs-lookup"><span data-stu-id="a6a6f-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="a6a6f-122">メディア要求が送信された時刻。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-122">Time that a media request was sent out.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6a6f-123"><strong>MediaEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="a6a6f-123"><strong>MediaEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a6a6f-124">datetime</span><span class="sxs-lookup"><span data-stu-id="a6a6f-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="a6a6f-125">セッションの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="a6a6f-125">End time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a6a6f-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6a6f-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

