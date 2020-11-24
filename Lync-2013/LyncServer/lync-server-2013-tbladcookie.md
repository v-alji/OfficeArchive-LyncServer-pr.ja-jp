---
title: 'Lync Server 2013: tblADCookie'
description: 'Lync Server 2013: tblADCookie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398727"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="caa27-103">Lync Server 2013 の tblADCookie</span><span class="sxs-lookup"><span data-stu-id="caa27-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="caa27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="caa27-104">

<span> </span></span></span>

<span data-ttu-id="caa27-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="caa27-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="caa27-106">tblADCookie には、現在のライトウェイトディレクトリアクセスプロトコル (LDAP) 同期 cookie が含まれています。</span><span class="sxs-lookup"><span data-stu-id="caa27-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="caa27-107">行</span><span class="sxs-lookup"><span data-stu-id="caa27-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caa27-108">列</span><span class="sxs-lookup"><span data-stu-id="caa27-108">Column</span></span></th>
<th><span data-ttu-id="caa27-109">型</span><span class="sxs-lookup"><span data-stu-id="caa27-109">Type</span></span></th>
<th><span data-ttu-id="caa27-110">説明</span><span class="sxs-lookup"><span data-stu-id="caa27-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caa27-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="caa27-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="caa27-112">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="caa27-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="caa27-113">監視されているドメインのプリンシパル GUID。</span><span class="sxs-lookup"><span data-stu-id="caa27-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caa27-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="caa27-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="caa27-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="caa27-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="caa27-116">Active Directory ドメインサービスの同期に使用される、現在のドメインコントローラーの完全修飾ドメイン名 (FQDN) です。情報があります。</span><span class="sxs-lookup"><span data-stu-id="caa27-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caa27-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="caa27-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="caa27-118">image (バイナリ)</span><span class="sxs-lookup"><span data-stu-id="caa27-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="caa27-119">Active Directory 同期 cookie。</span><span class="sxs-lookup"><span data-stu-id="caa27-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caa27-120">最終更新日</span><span class="sxs-lookup"><span data-stu-id="caa27-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="caa27-121">datetime</span><span class="sxs-lookup"><span data-stu-id="caa27-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="caa27-122">行の更新時刻を含むタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="caa27-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caa27-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="caa27-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="caa27-124">datetime</span><span class="sxs-lookup"><span data-stu-id="caa27-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="caa27-125">変更のために行がロックされるまでの時間です。</span><span class="sxs-lookup"><span data-stu-id="caa27-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="caa27-126">これは、チャットサービスの1つだけが同時に Active Directory の同期を行うことができるようにするソフトウェアの連結メカニズムの一部です。</span><span class="sxs-lookup"><span data-stu-id="caa27-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="caa27-127">機能</span><span class="sxs-lookup"><span data-stu-id="caa27-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caa27-128">列</span><span class="sxs-lookup"><span data-stu-id="caa27-128">Column(s)</span></span></th>
<th><span data-ttu-id="caa27-129">説明</span><span class="sxs-lookup"><span data-stu-id="caa27-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caa27-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="caa27-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="caa27-131">主キー。</span><span class="sxs-lookup"><span data-stu-id="caa27-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caa27-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="caa27-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="caa27-133">プリンシパルで参照される外部キー (prinGuid テーブル)。</span><span class="sxs-lookup"><span data-stu-id="caa27-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="caa27-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="caa27-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

