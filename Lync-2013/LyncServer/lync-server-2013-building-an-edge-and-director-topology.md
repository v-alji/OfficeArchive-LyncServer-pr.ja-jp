---
title: 'Lync Server 2013: エッジおよびディレクターのトポロジの作成'
description: 'Lync Server 2013: エッジとディレクターのトポロジを作成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435937"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a><span data-ttu-id="125a2-103">Lync Server 2013 でのエッジおよびディレクターのトポロジの作成</span><span class="sxs-lookup"><span data-stu-id="125a2-103">Building an edge and Director topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="125a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="125a2-104">

<span> </span></span></span>

<span data-ttu-id="125a2-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="125a2-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="125a2-106">トポロジを構築するには、次の計画と展開のタスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="125a2-106">Building the topology involves the following planning and deployment tasks:</span></span>

  - <span data-ttu-id="125a2-107">**計画**   組織の適切なトポロジを定義し、展開に必要なコンポーネントを特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="125a2-107">**Planning**   You need to define an appropriate topology for your organization and identify the components required to deploy it.</span></span> <span data-ttu-id="125a2-108">これは、計画プロセスの標準的な手順です。</span><span class="sxs-lookup"><span data-stu-id="125a2-108">These are standard steps in the planning process.</span></span> <span data-ttu-id="125a2-109">Lync Server 2013 と共に提供される Microsoft Lync Server 2013、計画ツールを使用すると、計画プロセスを簡単に開始したり、要件や計画が完了したときに簡単に変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="125a2-109">The Microsoft Lync Server 2013, Planning Tool provided with Lync Server 2013 makes it easy to start the planning process, as well as including the ability to easily make changes as your requirements and plans are finalized.</span></span>

  - <span data-ttu-id="125a2-110">**展開**   トポロジビルダーを使用して定義したトポロジは、Lync Server 2013 サーバーの展開に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="125a2-110">**Deployment**   The topology that you define using Topology Builder is essential to the deployment of any Lync Server 2013 server.</span></span> <span data-ttu-id="125a2-111">計画作業の一環としてトポロジビルダーを使用してトポロジの定義と発行が完了しない場合は、Edge サーバーを展開する前にトポロジを完成させて発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="125a2-111">If you do not finish defining and publishing your topology by using Topology Builder as part of your planning efforts, you must complete it and publish the topology before you deploy your Edge Servers.</span></span>

<span data-ttu-id="125a2-112">少なくとも1つの内部プールを展開してから、内部プールを展開するには、トポロジビルダーをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="125a2-112">You cannot deploy Edge Server components until you have deployed at least one internal pool, and you must install Topology Builder to deploy an internal pool.</span></span> <span data-ttu-id="125a2-113">このセクションでは、内部プールのインストールプロセスの一部であるトポロジビルダーのインストールについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="125a2-113">This section does not cover installation of Topology Builder because that is part of the installation process for the internal pool.</span></span>

<span data-ttu-id="125a2-114">これらのツールについて詳しくは、「 [Lync Server 2013 での外部ユーザーアクセスの展開チェックリスト](lync-server-2013-deployment-checklist-for-external-user-access.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="125a2-114">For details about these tools, see [Deployment checklist for external user access in Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="125a2-115">以前にトポロジビルダーを使用して、エッジトポロジを含む完全なトポロジを定義している場合は、このセクションの「microsoft lync server <A href="lync-server-2013-define-your-edge-topology.md">2013 での edge トポロジの定義</A> 」をスキップして、「lync server 2013 のタスク <A href="lync-server-2013-publish-your-topology.md">でトポロジを公開</A> する」の手順を <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">2013</A> 実行してください。</span><span class="sxs-lookup"><span data-stu-id="125a2-115">If you previously used Topology Builder to define a complete topology, including the edge topology, you do can skip the <A href="lync-server-2013-define-your-edge-topology.md">Define your edge topology in Lync Server 2013</A> and <A href="lync-server-2013-publish-your-topology.md">Publish your topology in Lync Server 2013</A> tasks in this section, but you do need to complete the <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A> task.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="125a2-116">このセクション中</span><span class="sxs-lookup"><span data-stu-id="125a2-116">In This Section</span></span>

  - [<span data-ttu-id="125a2-117">Lync Server 2013 でエッジ トポロジを定義する</span><span class="sxs-lookup"><span data-stu-id="125a2-117">Define your edge topology in Lync Server 2013</span></span>](lync-server-2013-define-your-edge-topology.md)

  - [<span data-ttu-id="125a2-118">Lync Server 2013 のトポロジにオプションのディレクター トポロジを定義する</span><span class="sxs-lookup"><span data-stu-id="125a2-118">Define optional Director topologies in your topology for Lync Server 2013</span></span>](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [<span data-ttu-id="125a2-119">Lync Server 2013 でのトポロジの公開</span><span class="sxs-lookup"><span data-stu-id="125a2-119">Publish your topology in Lync Server 2013</span></span>](lync-server-2013-publish-your-topology.md)

  - [<span data-ttu-id="125a2-120">エッジ インストール用の Lync Server 2013 のトポロジをエクスポートして外部メディアにコピーする</span><span class="sxs-lookup"><span data-stu-id="125a2-120">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

<span data-ttu-id="125a2-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="125a2-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

