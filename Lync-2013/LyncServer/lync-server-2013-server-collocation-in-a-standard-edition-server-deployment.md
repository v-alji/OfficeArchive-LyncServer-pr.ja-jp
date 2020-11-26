---
title: Lync Server 2013 の Standard Edition サーバー展開でのサーバーの併置
description: Standard Edition server 展開の Lync Server 2013 Server collocation。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server collocation in a Standard Edition server deployment
ms:assetid: 0763ffab-4fd6-463a-8e62-d97876b376d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398131(v=OCS.15)
ms:contentKeyID: 48183314
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af44761d36c472de1a3da5cd3b3938dc1a130836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441894"
---
# <a name="server-collocation-in-a-standard-edition-server-deployment-for-lync-server-2013"></a><span data-ttu-id="1971e-103">Lync Server 2013 の Standard Edition サーバー展開でのサーバーの併置</span><span class="sxs-lookup"><span data-stu-id="1971e-103">Server collocation in a Standard Edition server deployment for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1971e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1971e-104">

<span> </span></span></span>

<span data-ttu-id="1971e-105">_**最終更新日:** 2013-01-20_</span><span class="sxs-lookup"><span data-stu-id="1971e-105">_**Topic Last Modified:** 2013-01-20_</span></span>

<span data-ttu-id="1971e-106">このセクションでは、Lync Server 2013 Standard Edition サーバーの展開で検索できるサーバーの役割、データベース、およびファイル共有について説明します。</span><span class="sxs-lookup"><span data-stu-id="1971e-106">This section describes the server roles, databases, and file shares that you can collocate in a Lync Server 2013 Standard Edition server deployment.</span></span>

<div>

## <a name="server-roles"></a><span data-ttu-id="1971e-107">サーバーの役割</span><span class="sxs-lookup"><span data-stu-id="1971e-107">Server Roles</span></span>

<span data-ttu-id="1971e-108">Lync Server 2013 では、A/V 会議サービス、仲介サービス、監視、およびアーカイブは Standard Edition サーバーに併置されますが、有効にするには追加の構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="1971e-108">In Lync Server 2013, A/V Conferencing service, Mediation service, Monitoring, and Archiving are collocated on the Standard Edition Server, but additional configuration is required to enable them.</span></span> <span data-ttu-id="1971e-109">別々のサーバーに仲介サービスを展開することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1971e-109">You can choose to deploy Mediation service on separate servers.</span></span>

<span data-ttu-id="1971e-110">標準エディションのサーバーを使用して、信頼できるアプリケーションサーバーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="1971e-110">You can collocate a trusted application server with a Standard Edition server.</span></span>

<span data-ttu-id="1971e-111">次のサーバーロールはそれぞれ別のコンピューターに展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1971e-111">The following server roles must each be deployed on a separate computer:</span></span>

  - <span data-ttu-id="1971e-112">ディレクター</span><span class="sxs-lookup"><span data-stu-id="1971e-112">Director</span></span>

  - <span data-ttu-id="1971e-113">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="1971e-113">Edge Server</span></span>

  - <span data-ttu-id="1971e-114">仲介サーバー (Standard Edition サーバーに付属していない場合)</span><span class="sxs-lookup"><span data-stu-id="1971e-114">Mediation Server (if not collocated with the Standard Edition server)</span></span>

  - <span data-ttu-id="1971e-115">Office Web Apps サーバー</span><span class="sxs-lookup"><span data-stu-id="1971e-115">Office Web Apps Server</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="1971e-116">データベース</span><span class="sxs-lookup"><span data-stu-id="1971e-116">Databases</span></span>

<span data-ttu-id="1971e-117">既定では、SQL Server Express バックエンドデータベースは Standard Edition サーバーに併置されます。</span><span class="sxs-lookup"><span data-stu-id="1971e-117">By default, the SQL Server Express back-end database is collocated on the Standard Edition server.</span></span> <span data-ttu-id="1971e-118">別のコンピュータに移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="1971e-118">You cannot move it to a separate computer.</span></span> <span data-ttu-id="1971e-119">1つの例外を除き、Standard Edition サーバー上で他のデータベースを検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="1971e-119">With one exception, you cannot collocate other databases on the Standard Edition server.</span></span> <span data-ttu-id="1971e-120">標準エディションのサーバーに常設チャットサーバーを展開することを選択した場合は、同一の Standard Edition サーバー上で常設チャットデータベースと常設チャットのコンプライアンスデータベースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="1971e-120">If you choose to deploy Persistent Chat Server on a Standard Edition server, you can collocate the Persistent chat database and the Persistent Chat Compliance database on the same Standard Edition server.</span></span>

<span data-ttu-id="1971e-121">1つのデータベースサーバー上で、次の各データベースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="1971e-121">You can collocate each of the following databases on a single database server:</span></span>

  - <span data-ttu-id="1971e-122">監視データベース</span><span class="sxs-lookup"><span data-stu-id="1971e-122">Monitoring database</span></span>

  - <span data-ttu-id="1971e-123">アーカイブ データベース</span><span class="sxs-lookup"><span data-stu-id="1971e-123">Archiving database</span></span>

  - <span data-ttu-id="1971e-124">Enterprise Edition フロントエンドプールのバックエンドデータベース</span><span class="sxs-lookup"><span data-stu-id="1971e-124">A back-end database for an Enterprise Edition Front End pool</span></span>

<span data-ttu-id="1971e-125">次の制限があります。これらのデータベースの任意または一部を1つの SQL インスタンスで検索したり、個別に SQL インスタンスを使用したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="1971e-125">You can collocate any or any or all of these databases in a single SQL instance or use a separate SQL instances for each, with the following limitations:</span></span>

  - <span data-ttu-id="1971e-126">各 SQL インスタンスには、1つのバックエンドデータベース (Enterprise Edition フロントエンドプール用)、単一の監視データベース、単一のアーカイブデータベース、単一の常設チャットデータベース、および1つの常設チャットのコンプライアンスデータベースのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1971e-126">Each SQL instance can contain only a single back-end database (for an Enterprise Edition Front End pool), single Monitoring database, single Archiving database, single persistent chat database, and single persistent chat compliance database.</span></span>

  - <span data-ttu-id="1971e-127">データベースサーバーでは、複数の Enterprise Edition フロントエンドプール、アーカイブを実行している1台のサーバー、単一の常設チャットデータベース、および単一の常設チャットのコンプライアンスデータベースをサポートすることはできませんが、データベースが SQL Server の同じインスタンスと SQL Server の別のインスタンスのどちらを使用するかに関係なく、いずれかをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="1971e-127">The database server cannot support more than one Enterprise Edition Front End pool, one server running Archiving, one server running Monitoring, single Persistent Chat database, and single Persistent Chat compliance database, but it can support one of each, regardless of whether the databases use the same instance of SQL Server or separate instances of SQL Server.</span></span>

<span data-ttu-id="1971e-128">このセクションの後半で説明するように、データベースとのファイル共有を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="1971e-128">You can collocate a file share with the databases, as described later in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1971e-129">Lync Server 2013 では、展開内の一部またはすべてのユーザーに対して、監視とアーカイブストレージを Exchange 2013 ストレージと統合するオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1971e-129">In Lync Server 2013, you have the option of integrating Monitoring and Archiving storage with Exchange 2013 storage for some or all users in your deployment.</span></span> <span data-ttu-id="1971e-130">Lync Server やコンポーネントを実行しているサーバーを Exchange ストレージと同じサーバー上に展開することはできません。</span><span class="sxs-lookup"><span data-stu-id="1971e-130">You cannot deploy any servers running Lync Server or components on the same servers as the Exchange storage.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1971e-131">データベースの collocation はサポートされていますが、データベースのサイズが急速に増大する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1971e-131">Although collocation of databases is supported, the size of the databases can grow quickly.</span></span> <span data-ttu-id="1971e-132">たとえば、アーカイブデータベースを他のデータベースとの間で検索することを検討している場合、アーカイブデータベースに必要なディスク領域が非常に大きくなる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1971e-132">For example, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large.</span></span> <span data-ttu-id="1971e-133">このため、エンタープライズプールのバックエンドデータベースを使用して、複数のデータベース、特にアーカイブデータベース、常設チャットデータベース、常設チャットのコンプライアンスデータベースを検索することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="1971e-133">For this reason, we do not recommend collocating multiple databases, especially the Archiving database, Persistent Chat database, and Persistent Chat compliance database with the back-end database of an Enterprise pool.</span></span>



</div>

</div>

<div>

## <a name="file-shares"></a><span data-ttu-id="1971e-134">ファイル共有</span><span class="sxs-lookup"><span data-stu-id="1971e-134">File Shares</span></span>

<span data-ttu-id="1971e-135">ファイル共有は、個別のサーバーにすることも、次のいずれか、またはすべてを同じサーバー上に置いておくこともできます。</span><span class="sxs-lookup"><span data-stu-id="1971e-135">The file share can be a separate server or can be collocated on the same server as any or all of the following:</span></span>

  - <span data-ttu-id="1971e-136">データベースサーバー (Enterprise Edition フロントエンドプールのバックエンドサーバーを含む)</span><span class="sxs-lookup"><span data-stu-id="1971e-136">Database server, including the Back End Server of an Enterprise Edition Front End pool</span></span>

  - <span data-ttu-id="1971e-137">アーカイブ データベース</span><span class="sxs-lookup"><span data-stu-id="1971e-137">Archiving database</span></span>

  - <span data-ttu-id="1971e-138">監視データベース</span><span class="sxs-lookup"><span data-stu-id="1971e-138">Monitoring database</span></span>

  - <span data-ttu-id="1971e-139">常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="1971e-139">Persistent Chat database</span></span>

  - <span data-ttu-id="1971e-140">常設チャットのコンプライアンスデータベース</span><span class="sxs-lookup"><span data-stu-id="1971e-140">Persistent Chat compliance database</span></span>

<span data-ttu-id="1971e-141">1つのファイル共有は、複数のフロントエンドプール、標準エディションサーバー (すべて同じサイト内) に使用できます。</span><span class="sxs-lookup"><span data-stu-id="1971e-141">A single file share can be used for multiple Front End pools, Standard Edition servers (all in the same site).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1971e-142">Lync Server 2013 の [監視とアーカイブ] では、Lync Server のファイル共有を Standard Edition サーバーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="1971e-142">In Lync Server 2013, Monitoring and Archiving use the Lync Server file share as the Standard Edition server.</span></span>



</div>

</div>

<div>

## <a name="other-components"></a><span data-ttu-id="1971e-143">その他のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="1971e-143">Other Components</span></span>

<span data-ttu-id="1971e-144">Lync server 2013 コンポーネントではないリバースプロキシサーバーを検索することはできませんが、Lync Server 2013 サーバーの役割を持つフェデレーションユーザーの web コンテンツの共有をサポートする場合は、展開で必要になります。</span><span class="sxs-lookup"><span data-stu-id="1971e-144">You cannot collocate a reverse proxy server, which is not a Lync Server 2013 component, but is required in your deployment if you want to support sharing of web content for federated users with any Lync Server 2013 server role.</span></span> <span data-ttu-id="1971e-145">ただし、他のアプリケーションで使用されている既存のリバースプロキシサーバーのサポートを構成することによって、Lync Server 2013 の展開にリバースプロキシサポートを実装することはできます。</span><span class="sxs-lookup"><span data-stu-id="1971e-145">You can, however, implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span>

<span data-ttu-id="1971e-146">任意の Lync Server 2013 の役割を持つ Exchange UM コンポーネントまたは SharePoint コンポーネントを検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="1971e-146">You cannot collocate any Exchange UM component or SharePoint component with any Lync Server 2013 role.</span></span>

<span data-ttu-id="1971e-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1971e-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

