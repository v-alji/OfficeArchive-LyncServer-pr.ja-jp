---
title: Lync Server 2013 の Enterprise Edition フロント エンド プール展開でのサーバーの併置
description: Enterprise Edition フロントエンドプールの展開での Lync Server 2013 サーバーの場所
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server collocation in an Enterprise Edition Front End pool deployment
ms:assetid: 0516b18d-14c0-4237-9279-0f92e341b1bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398102(v=OCS.15)
ms:contentKeyID: 48183287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a937cd2d58e41d56fec3c7898ebcf6725086d51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444911"
---
# <a name="server-collocation-in-an-enterprise-edition-front-end-pool-deployment-for-lync-server-2013"></a><span data-ttu-id="b0b24-103">Lync Server 2013 の Enterprise Edition フロント エンド プール展開でのサーバーの併置</span><span class="sxs-lookup"><span data-stu-id="b0b24-103">Server collocation in an Enterprise Edition Front End pool deployment for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0b24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0b24-104">

<span> </span></span></span>

<span data-ttu-id="b0b24-105">_**最終更新日:** 2013-11-11_</span><span class="sxs-lookup"><span data-stu-id="b0b24-105">_**Topic Last Modified:** 2013-11-11_</span></span>

<span data-ttu-id="b0b24-106">このセクションでは、Lync Server 2013 フロントエンドプールの展開で検索できるサーバーの役割、データベース、およびファイル共有について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0b24-106">This section describes the server roles, databases, and file shares that you can collocate in a Lync Server 2013 Front End pool deployment.</span></span>

<div>

## <a name="server-roles"></a><span data-ttu-id="b0b24-107">サーバーの役割</span><span class="sxs-lookup"><span data-stu-id="b0b24-107">Server Roles</span></span>

<span data-ttu-id="b0b24-108">Lync Server 2013 では、A/V 会議サービス、仲介サービス、監視、およびアーカイブはフロントエンドサーバーに併置されますが、有効にするには追加の構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0b24-108">In Lync Server 2013, A/V Conferencing service, Mediation service, Monitoring, and Archiving are collocated on the Front End Server, but additional configuration is required to enable them.</span></span> <span data-ttu-id="b0b24-109">フロントエンドサーバーで仲介サーバーを検索したくない場合は、スタンドアロンの仲介サーバーとして別のコンピューターに展開することができます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-109">If you do not want to collocate the Mediation Server with the Front End Server, you can deploy it as a stand-alone Mediation Server on a separate computer.</span></span>

<span data-ttu-id="b0b24-110">サーバーを使用して、信頼できるアプリケーションサーバーを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-110">You can collocate a trusted application server with the Front End Server.</span></span>

<span data-ttu-id="b0b24-111">次のサーバーロールはそれぞれ別のコンピューターに展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0b24-111">The following server roles must each be deployed on a separate computer:</span></span>

  - <span data-ttu-id="b0b24-112">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b0b24-112">Director</span></span>

  - <span data-ttu-id="b0b24-113">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="b0b24-113">Edge Server</span></span>

  - <span data-ttu-id="b0b24-114">仲介サーバー (フロントエンドサーバーに併置されていない場合)</span><span class="sxs-lookup"><span data-stu-id="b0b24-114">Mediation Server (if not collocated with the Front End Server)</span></span>

  - <span data-ttu-id="b0b24-115">Office Web Apps サーバー</span><span class="sxs-lookup"><span data-stu-id="b0b24-115">Office Web Apps Server</span></span>

<span data-ttu-id="b0b24-116">フロントエンドサーバーで常設チャットサーバーの役割を検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="b0b24-116">You cannot collocate Persistent Chat server role with the Front End Server.</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="b0b24-117">データベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-117">Databases</span></span>

<span data-ttu-id="b0b24-118">同じデータベースサーバー上で、次の各データベースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-118">You can collocate each of the following databases on the same database server:</span></span>

  - <span data-ttu-id="b0b24-119">バックエンドデータベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-119">Back-end database</span></span>

  - <span data-ttu-id="b0b24-120">監視データベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-120">Monitoring database</span></span>

  - <span data-ttu-id="b0b24-121">アーカイブ データベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-121">Archiving database</span></span>

  - <span data-ttu-id="b0b24-122">常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-122">Persistent Chat database</span></span>

  - <span data-ttu-id="b0b24-123">常設チャットのコンプライアンスデータベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-123">Persistent Chat compliance database</span></span>

<span data-ttu-id="b0b24-124">SQL Server の1つのインスタンスでこれらのデータベースのいずれかまたはすべてを検索することも、SQL Server の個別のインスタンスを使用することもできます。次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="b0b24-124">You can collocate any or any or all of these databases in a single instance of SQL Server or use a separate instance of SQL Server for each, with the following limitations:</span></span>

  - <span data-ttu-id="b0b24-125">SQL Server の各インスタンスには、1つのバックエンドデータベース、単一の監視データベース、単一のアーカイブデータベース、1つの常設チャットデータベース、1つの常設チャットのコンプライアンスデータベースのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-125">Each instance of SQL Server can contain only a single back-end database, a single Monitoring database, a single Archiving database, a single Persistent Chat database, and a single Persistent Chat compliance database.</span></span>

  - <span data-ttu-id="b0b24-126">データベースサーバーでは、複数のフロントエンドプール、1つのアーカイブ展開、および1つの監視展開をサポートすることはできませんが、データベースが SQL Server の同じインスタンスと SQL Server の別のインスタンスのどちらを使うかに関係なく、どちらか1つをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-126">The database server cannot support more than one Front End pool, one Archiving deployment, and one Monitoring deployment, but it can support one of each, regardless of whether the databases use the same instance of SQL Server or separate instances of SQL Server.</span></span>

<span data-ttu-id="b0b24-127">このセクションの後半で説明するように、データベースとのファイル共有を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-127">You can collocate a file share with the databases, as described later in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0b24-128">Lync Server 2013 では、展開内の一部またはすべてのユーザーについて、アーカイブストレージと Exchange 2013 ストレージを統合するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b0b24-128">In Lync Server 2013, you have the option of integrating Archiving storage with Exchange 2013 storage for some or all users in your deployment.</span></span> <span data-ttu-id="b0b24-129">Lync Server やコンポーネントを実行しているサーバーを Exchange ストレージと同じサーバー上に展開することはできません。</span><span class="sxs-lookup"><span data-stu-id="b0b24-129">You cannot deploy any servers running Lync Server or components on the same servers as the Exchange storage.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b0b24-130">データベースの collocation はサポートされていますが、データベースのサイズが急速に増大する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b0b24-130">Although collocation of databases is supported, the size of the databases can grow quickly.</span></span> <span data-ttu-id="b0b24-131">たとえば、アーカイブデータベースを他のデータベースとの間で検索することを検討している場合、アーカイブデータベースに必要なディスク領域が非常に大きくなる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b0b24-131">For example, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large.</span></span> <span data-ttu-id="b0b24-132">このため、複数のデータベース、特にアーカイブデータベース、常設チャットデータベース、またはバックエンドデータベースを含む永続的なチャットのコンプライアンスデータベースを検索することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="b0b24-132">For this reason, we do not recommend collocating multiple databases, especially the Archiving database, the Persistent Chat database, or the Persistent Chat compliance database with the back-end database.</span></span>



</div>

</div>

<div>

## <a name="file-share"></a><span data-ttu-id="b0b24-133">ファイル共有</span><span class="sxs-lookup"><span data-stu-id="b0b24-133">File Share</span></span>

<span data-ttu-id="b0b24-134">ファイル共有は、個別のサーバーにすることも、次のいずれか、またはすべてを同じサーバー上に置いておくこともできます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-134">The file share can be a separate server or can be collocated on the same server as any or all of the following:</span></span>

  - <span data-ttu-id="b0b24-135">データベースサーバー (Enterprise Edition フロントエンドプールのバックエンドサーバーを含む)</span><span class="sxs-lookup"><span data-stu-id="b0b24-135">Database server, including the Back End Server of an Enterprise Edition Front End pool</span></span>

  - <span data-ttu-id="b0b24-136">アーカイブ データベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-136">Archiving database</span></span>

  - <span data-ttu-id="b0b24-137">監視データベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-137">Monitoring database</span></span>

  - <span data-ttu-id="b0b24-138">常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-138">Persistent Chat database</span></span>

  - <span data-ttu-id="b0b24-139">常設チャットのコンプライアンスデータベース</span><span class="sxs-lookup"><span data-stu-id="b0b24-139">Persistent Chat compliance database</span></span>

<span data-ttu-id="b0b24-140">1つのファイル共有は、複数のフロントエンドプール、標準エディションサーバー (すべて同じサイト内) に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-140">A single file share can be used for multiple Front End pools, Standard Edition servers (all in the same site).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0b24-141">Lync Server 2013 の [監視とアーカイブ] では、Lync Server のファイル共有をフロントエンドサーバーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="b0b24-141">In Lync Server 2013, Monitoring and Archiving use the Lync Server file share as the Front End Server.</span></span>



</div>

</div>

<div>

## <a name="other-components"></a><span data-ttu-id="b0b24-142">その他のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="b0b24-142">Other Components</span></span>

<span data-ttu-id="b0b24-143">Lync server 2013 コンポーネントではないリバースプロキシサーバーを検索することはできませんが、Lync Server 2013 サーバーの役割を持つフェデレーションユーザーの web コンテンツの共有をサポートする場合は、展開で必要になります。</span><span class="sxs-lookup"><span data-stu-id="b0b24-143">You cannot collocate a reverse proxy server, which is not a Lync Server 2013 component, but is required in your deployment if you want to support sharing of web content for federated users with any Lync Server 2013 server role.</span></span> <span data-ttu-id="b0b24-144">ただし、他のアプリケーションで使用されている既存のリバースプロキシサーバーのサポートを構成することによって、Lync Server 2013 の展開にリバースプロキシサポートを実装することはできます。</span><span class="sxs-lookup"><span data-stu-id="b0b24-144">You can, however, implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span>

<span data-ttu-id="b0b24-145">任意の SharePoint Server の役割で Exchange ユニファイドメッセージング (UM) コンポーネントまたは SharePoint コンポーネントを検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="b0b24-145">You cannot collocate any Exchange Unified Messaging (UM) component or SharePoint component with any SharePoint Server role.</span></span>

<span data-ttu-id="b0b24-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0b24-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

