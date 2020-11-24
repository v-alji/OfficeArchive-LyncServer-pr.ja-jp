---
title: 'Lync Server 2013: SQL Server のファイアウォール要件について'
description: 'Lync Server 2013: SQL Server のファイアウォール要件について説明します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399483"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="86c29-103">Lync Server 2013 での SQL Server のファイアウォール要件について</span><span class="sxs-lookup"><span data-stu-id="86c29-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86c29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86c29-104">

<span> </span></span></span>

<span data-ttu-id="86c29-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="86c29-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="86c29-106">Standard Edition の展開の場合、ファイアウォールの例外は Lync Server 2013 のセットアップ中に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="86c29-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="86c29-107">ただし、Enterprise Edition の展開の場合は、SQL Server バックエンドサーバーでファイアウォールの例外を手動で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c29-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="86c29-108">TCP/IP プロトコルでは、特定の IP アドレスに対して1つのポートを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="86c29-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="86c29-109">つまり、SQL Server ベースのサーバーの場合、既定のデータベースインスタンスに既定の TCP ポート1433を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="86c29-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="86c29-110">その他の場合は、SQL Server 構成マネージャーを使って、一意の未使用のポートを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c29-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="86c29-111">ここでは、次の内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="86c29-111">This topic covers:</span></span>

  - <span data-ttu-id="86c29-112">既定のインスタンスを使用する場合のファイアウォール例外の要件</span><span class="sxs-lookup"><span data-stu-id="86c29-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="86c29-113">SQL Server Browser サービスのファイアウォール例外の要件</span><span class="sxs-lookup"><span data-stu-id="86c29-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="86c29-114">名前付きインスタンスを使用するときの静的リッスンポートの要件</span><span class="sxs-lookup"><span data-stu-id="86c29-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="86c29-115">既定のインスタンスを使用する場合のファイアウォール例外の要件</span><span class="sxs-lookup"><span data-stu-id="86c29-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="86c29-116">Lync Server 2013 を展開するときに、任意のデータベースに対して SQL Server の既定のインスタンスを使用している場合、フロントエンドプールから SQL Server の既定のインスタンスへの通信を確実にするために、次のファイアウォール規則要件が使用されます。</span><span class="sxs-lookup"><span data-stu-id="86c29-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86c29-117">プロトコル</span><span class="sxs-lookup"><span data-stu-id="86c29-117">Protocol</span></span></th>
<th><span data-ttu-id="86c29-118">ポート</span><span class="sxs-lookup"><span data-stu-id="86c29-118">Port</span></span></th>
<th><span data-ttu-id="86c29-119">方向</span><span class="sxs-lookup"><span data-stu-id="86c29-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86c29-120">TCP</span><span class="sxs-lookup"><span data-stu-id="86c29-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="86c29-121">1433</span><span class="sxs-lookup"><span data-stu-id="86c29-121">1433</span></span></p></td>
<td><p><span data-ttu-id="86c29-122">SQL Server への受信</span><span class="sxs-lookup"><span data-stu-id="86c29-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="86c29-123">SQL Server Browser サービスのファイアウォール例外の要件</span><span class="sxs-lookup"><span data-stu-id="86c29-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="86c29-124">SQL Server Browser サービスは、データベースインスタンスを探し、インスタンス (名前付きまたは既定) が使用するように構成されているポートを伝えます。</span><span class="sxs-lookup"><span data-stu-id="86c29-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86c29-125">プロトコル</span><span class="sxs-lookup"><span data-stu-id="86c29-125">Protocol</span></span></th>
<th><span data-ttu-id="86c29-126">ポート</span><span class="sxs-lookup"><span data-stu-id="86c29-126">Port</span></span></th>
<th><span data-ttu-id="86c29-127">方向</span><span class="sxs-lookup"><span data-stu-id="86c29-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86c29-128">UDP</span><span class="sxs-lookup"><span data-stu-id="86c29-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="86c29-129">1434</span><span class="sxs-lookup"><span data-stu-id="86c29-129">1434</span></span></p></td>
<td><p><span data-ttu-id="86c29-130">トラフィック</span><span class="sxs-lookup"><span data-stu-id="86c29-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="86c29-131">名前付きインスタンスを使用するときの静的リッスンポートの要件</span><span class="sxs-lookup"><span data-stu-id="86c29-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="86c29-132">Lync Server 2013 をサポートするデータベースの SQL Server 構成で名前付きインスタンスを使用している場合は、SQL Server 構成マネージャーを使って静的ポートを構成します。</span><span class="sxs-lookup"><span data-stu-id="86c29-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="86c29-133">名前付きインスタンスごとに静的ポートを割り当てると、ファイアウォールの各静的ポートに対して例外が作成されます。</span><span class="sxs-lookup"><span data-stu-id="86c29-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86c29-134">プロトコル</span><span class="sxs-lookup"><span data-stu-id="86c29-134">Protocol</span></span></th>
<th><span data-ttu-id="86c29-135">ポート</span><span class="sxs-lookup"><span data-stu-id="86c29-135">Port</span></span></th>
<th><span data-ttu-id="86c29-136">方向</span><span class="sxs-lookup"><span data-stu-id="86c29-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86c29-137">TCP</span><span class="sxs-lookup"><span data-stu-id="86c29-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="86c29-138">静的に定義された</span><span class="sxs-lookup"><span data-stu-id="86c29-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="86c29-139">トラフィック</span><span class="sxs-lookup"><span data-stu-id="86c29-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="86c29-140">SQL Server ドキュメント</span><span class="sxs-lookup"><span data-stu-id="86c29-140">SQL Server Documentation</span></span>

<span data-ttu-id="86c29-141">Microsoft SQL Server 2012 ドキュメントは、データベースのファイアウォールアクセスを構成する方法についての詳細なガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="86c29-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="86c29-142">Microsoft SQL Server 2012 の詳細については、「」の「SQL Server へのアクセスを許可するように Windows ファイアウォールを構成する」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) 。</span><span class="sxs-lookup"><span data-stu-id="86c29-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="86c29-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86c29-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

