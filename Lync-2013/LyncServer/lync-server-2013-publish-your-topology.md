---
title: 'Lync Server 2013: トポロジの公開'
description: 'Lync Server 2013: トポロジを公開します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish your topology
ms:assetid: bfed3829-7a54-4b5c-a7cb-28871acd35e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412935(v=OCS.15)
ms:contentKeyID: 48185287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4d27d2d3644eb1f174e2f3fab47197f2c122a97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399038"
---
# <a name="publish-your-topology-in-lync-server-2013"></a><span data-ttu-id="96ae5-103">Lync Server 2013 でのトポロジの公開</span><span class="sxs-lookup"><span data-stu-id="96ae5-103">Publish your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96ae5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96ae5-104">

<span> </span></span></span>

<span data-ttu-id="96ae5-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="96ae5-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="96ae5-106">トポロジビルダーを使用してトポロジを構築するたびに、データを使用して Lync Server 2013 を展開できるように、トポロジを中央管理ストアのデータベースに発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96ae5-106">Each time you use Topology Builder to build your topology, you must publish the topology to a database in the Central Management store so that the data can be used to deploy Lync Server 2013.</span></span> <span data-ttu-id="96ae5-107">トポロジを公開するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="96ae5-107">Use the following procedure to publish your topology.</span></span>

<div>

## <a name="to-publish-the-topology"></a><span data-ttu-id="96ae5-108">トポロジを公開するには</span><span class="sxs-lookup"><span data-stu-id="96ae5-108">To publish the topology</span></span>

1.  <span data-ttu-id="96ae5-109">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-109">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="96ae5-110">[トポロジビルダー] のコンソールツリーで、[ **Lync 2013**] を右クリックし、[ **トポロジの公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-110">In Topology Builder, in the console tree, right-click **Lync 2013**, and then click **Publish Topology**.</span></span>

3.  <span data-ttu-id="96ae5-111">ウィザードの [**ようこそ**] ページで、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-111">On the **Welcome** page of the wizard, click **Next**.</span></span>

4.  <span data-ttu-id="96ae5-112">**トポロジビルダーで CMS ストア** のページが見つかったら、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-112">On the **Topology Builder found a CMS store** page, click **Next**.</span></span>

5.  <span data-ttu-id="96ae5-113">[**他のデータベースの作成**] ページで、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-113">On the **Create other databases** page, click **Next**.</span></span>

6.  <span data-ttu-id="96ae5-114">状態がデータベースの作成に成功したことを示す場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="96ae5-114">When the status indicates that database creation succeeded, do the following:</span></span>
    
      - <span data-ttu-id="96ae5-115">ログを表示するには、[**ログの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-115">To view the log, click **View log**.</span></span>
    
      - <span data-ttu-id="96ae5-116">ウィザードを閉じるには、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-116">To close the wizard, click **Finish**.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="96ae5-117">エッジサーバーまたはエッジプールの新規インストールの場合は、既存のフロントエンドサーバー、フロントエンドプール、または Standard Edition サーバーから Edge Server 構成をエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96ae5-117">If this is a new installation of an Edge Server or Edge pool, you must export the Edge Server configuration from an existing Front End Server, Front End pool, or Standard Edition server.</span></span> <span data-ttu-id="96ae5-118">構成をエクスポートするには、「 <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Lync Server 2013 トポロジをエクスポートして、edge インストール用の外部メディアにコピーする</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96ae5-118">To export the configuration, see <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A>.</span></span> <span data-ttu-id="96ae5-119">Lync Server 展開ウィザードを通じて、エッジサーバーのセットアップおよび展開フェーズ中に、外部メディアまたはネットワーク共有から構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="96ae5-119">You will import the configuration file from the external media or network share during the setup and deployment phase of the Edge Servers through the Lync Server Deployment Wizard.</span></span><BR><span data-ttu-id="96ae5-120">エッジサーバーが動作していて、ローカル構成管理ストアデータベースが内部展開によってレプリケートされると、それ以降の Lync Server 2013 構成の更新は公開され、エッジサーバーにレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="96ae5-120">Once the Edge Servers are operational and the local configuration management store database is replicating with the internal deployment, subsequent updates to the Lync Server 2013 configuration will be published and replicated to the Edge Servers.</span></span>

        
        <span data-ttu-id="96ae5-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96ae5-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

