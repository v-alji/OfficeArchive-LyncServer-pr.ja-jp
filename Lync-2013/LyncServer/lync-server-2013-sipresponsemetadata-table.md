---
title: 'Lync Server 2013: SIPResponseMetaData テーブル'
description: 'Lync Server 2013: SIPResponseMetaData テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444624"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="4fcfc-103">Lync Server 2013 の SIPResponseMetaData テーブル</span><span class="sxs-lookup"><span data-stu-id="4fcfc-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4fcfc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4fcfc-104">

<span> </span></span></span>

<span data-ttu-id="4fcfc-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="4fcfc-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="4fcfc-106">SIPResponseMetaDataTable には、SIP 応答コードの一覧と、各コードの分類と定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="4fcfc-107">これらのコードは、SIP デバイスと SIP コミュニケーションセッションに影響を与えるイベントに対応して生成されます。たとえば、応答コード403は、SIP デバイスが要求を行ったときに、サーバーがその要求を受け入れることを拒否したときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="4fcfc-108">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fcfc-109">列</span><span class="sxs-lookup"><span data-stu-id="4fcfc-109">Column</span></span></th>
<th><span data-ttu-id="4fcfc-110">データ型</span><span class="sxs-lookup"><span data-stu-id="4fcfc-110">Data Type</span></span></th>
<th><span data-ttu-id="4fcfc-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="4fcfc-111">Key/Index</span></span></th>
<th><span data-ttu-id="4fcfc-112">詳細</span><span class="sxs-lookup"><span data-stu-id="4fcfc-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fcfc-113"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="4fcfc-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="4fcfc-114">int</span><span class="sxs-lookup"><span data-stu-id="4fcfc-114">int</span></span></p></td>
<td><p><span data-ttu-id="4fcfc-115">Primary</span><span class="sxs-lookup"><span data-stu-id="4fcfc-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="4fcfc-116">SIP 応答コードを表す数値。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fcfc-117"><strong>クラス</strong></span><span class="sxs-lookup"><span data-stu-id="4fcfc-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="4fcfc-118">int</span><span class="sxs-lookup"><span data-stu-id="4fcfc-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4fcfc-119">応答コードの一般的な分類。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-119">General classification for the response code.</span></span> <span data-ttu-id="4fcfc-120">分類には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="4fcfc-121">1–情報の返信</span><span class="sxs-lookup"><span data-stu-id="4fcfc-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="4fcfc-122">2–成功応答</span><span class="sxs-lookup"><span data-stu-id="4fcfc-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="4fcfc-123">3–リダイレクション応答</span><span class="sxs-lookup"><span data-stu-id="4fcfc-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="4fcfc-124">4–クライアントエラー応答</span><span class="sxs-lookup"><span data-stu-id="4fcfc-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="4fcfc-125">5--サーバー障害への応答</span><span class="sxs-lookup"><span data-stu-id="4fcfc-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="4fcfc-126">6–グローバルエラー応答</span><span class="sxs-lookup"><span data-stu-id="4fcfc-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fcfc-127"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="4fcfc-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="4fcfc-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4fcfc-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4fcfc-129">SIP 応答コードの説明。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-129">Description of the SIP response code.</span></span> <span data-ttu-id="4fcfc-130">たとえば、応答コード181には次の説明があります。</span><span class="sxs-lookup"><span data-stu-id="4fcfc-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="4fcfc-131">通話が転送されています</span><span class="sxs-lookup"><span data-stu-id="4fcfc-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4fcfc-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4fcfc-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

