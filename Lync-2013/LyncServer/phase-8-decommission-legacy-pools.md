---
title: 'フェーズ 8: レガシ プールの使用停止'
description: 'フェーズ 8: レガシプールを廃止します。'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 8: Decommission legacy pools'
ms:assetid: 1c68e5d8-fb5f-45e6-b6e3-27f5e830c966
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204724(v=OCS.15)
ms:contentKeyID: 48183557
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a6414fe97b54ed1b487ff722c6b02d4904443841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446087"
---
# <a name="phase-8-decommission-legacy-pools"></a><span data-ttu-id="ffcc5-103">フェーズ 8: レガシ プールの使用停止</span><span class="sxs-lookup"><span data-stu-id="ffcc5-103">Phase 8: Decommission legacy pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffcc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffcc5-104">

<span> </span></span></span>

<span data-ttu-id="ffcc5-105">_**最終更新日:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="ffcc5-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="ffcc5-106">次のトピックでは、Lync Server 2010 の従来の展開で、DNS エントリの更新、コンテンツ管理サーバーの移動、プールの廃止、サーバーとプールの無効化と削除に関するガイダンスを示します。</span><span class="sxs-lookup"><span data-stu-id="ffcc5-106">The following topic provides guidance in updating DNS entries, moving the Content Management Server, decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Lync Server 2010.</span></span> <span data-ttu-id="ffcc5-107">このセクションに記載されているすべての手順を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ffcc5-107">Not all of the procedures listed in this section are required.</span></span> <span data-ttu-id="ffcc5-108">ドキュメントを読み、使用する使用停止手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="ffcc5-108">Read the documentation and determine which decommissioning procedure to use.</span></span>

<span data-ttu-id="ffcc5-109">Lync Server 2010 サーバーとサーバーの役割、および Lync Server 2010 の展開を廃止するためのステップバイステップのガイドについては、「Microsoft Lync Server 2010 をアンインストールしてサーバーの役割を削除する」をご覧ください [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227) 。</span><span class="sxs-lookup"><span data-stu-id="ffcc5-109">For exhaustive coverage of removing Lync Server 2010 servers and server roles, and a step-by-step guide to decommissioning a Lync Server 2010 deployment, see "Uninstalling Microsoft Lync Server 2010 and Removing Server Roles," which can be downloaded at [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ffcc5-110">Microsoft ユニファイドコミュニケーションマネージ API (UCMA) アプリケーションの移行とアップグレードに関する情報については、「従来の環境を廃止する前に」を参照してください。 <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span><span class="sxs-lookup"><span data-stu-id="ffcc5-110">For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ffcc5-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ffcc5-111">In This Section</span></span>

  - <span></span>  
    [<span data-ttu-id="ffcc5-112">DNS SRV レコードの更新</span><span class="sxs-lookup"><span data-stu-id="ffcc5-112">Update DNS SRV records</span></span>](update-dns-srv-records.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-113">Lync Server 2010 Central Management Server を Lync Server 2013 に移動する</span><span class="sxs-lookup"><span data-stu-id="ffcc5-113">Move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>](move-the-lync-server-2010-central-management-server-to-lync-server-2013.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-114">会議ディレクトリの移動</span><span class="sxs-lookup"><span data-stu-id="ffcc5-114">Move Conference Directories</span></span>](move-lync-server-2010-conference-directories-to-lync-server-2013.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-115">アーカイブ サーバーの関連付けの削除</span><span class="sxs-lookup"><span data-stu-id="ffcc5-115">Remove the Archiving server association</span></span>](remove-the-archiving-server-association.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-116">監視サーバーの関連付けの削除</span><span class="sxs-lookup"><span data-stu-id="ffcc5-116">Remove the Monitoring server association</span></span>](remove-the-monitoring-server-association.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-117">Enterprise Edition フロントエンドサーバーまたは Standard Edition フロントエンドサーバーを削除する</span><span class="sxs-lookup"><span data-stu-id="ffcc5-117">Remove the Enterprise Edition Front End Server or Standard Edition Front End Server</span></span>](remove-the-enterprise-edition-front-end-server-or-standard-edition-front-end-server.md)

  - <span></span>  
    [<span data-ttu-id="ffcc5-118">バックエンド サーバー上の SQL Server インスタンスとデータベースの削除</span><span class="sxs-lookup"><span data-stu-id="ffcc5-118">Remove SQL Server instances and databases on the Back End Server</span></span>](remove-sql-server-instances-and-databases-on-the-back-end-server.md)

<span data-ttu-id="ffcc5-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffcc5-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

