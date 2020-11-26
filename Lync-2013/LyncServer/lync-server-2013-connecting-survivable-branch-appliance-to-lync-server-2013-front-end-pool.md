---
title: Lync Server 2013 のフロント エンド プールへの存続可能ブランチ アプライアンスの接続
description: Survivable Branch Appliance を Lync Server 2013 フロントエンドプールに接続します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432262"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a><span data-ttu-id="ad543-103">Lync Server 2013 のフロント エンド プールへの存続可能ブランチ アプライアンスの接続</span><span class="sxs-lookup"><span data-stu-id="ad543-103">Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad543-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad543-104">

<span> </span></span></span>

<span data-ttu-id="ad543-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="ad543-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="ad543-106">すべての Survivable Branch Appliance (SBA) は、SBA のバックアップレジストラーとして提供されるフロントエンドプールと関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="ad543-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool, which serves as a backup Registrar for the SBA.</span></span> <span data-ttu-id="ad543-107">フロントエンドプールが Lync Server 2013 にアップグレードされた場合、フロントエンドプールがアップグレードされている間、SBA はフロントエンドプールとの関連付けを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad543-107">When the Front End pool is upgraded to Lync Server 2013, the SBA must be disassociated from the Front End pool while the Front End pool is upgraded.</span></span> <span data-ttu-id="ad543-108">フロントエンドプールがアップグレードされた後は、フロントエンドプールを使用して SBA を reassociated できます。</span><span class="sxs-lookup"><span data-stu-id="ad543-108">After the Front End pool is upgraded, the SBA can be reassociated with the Front End pool.</span></span> <span data-ttu-id="ad543-109">これには、トポロジビルダーのトポロジから SBA を削除してから、もう一度 SBA をトポロジビルダーに追加することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad543-109">This involves deleting the SBA from the topology in Topology Builder and then adding the SBA, again, to Topology Builder.</span></span> <span data-ttu-id="ad543-110">トポロジから SBA を削除する前に、SBA をホームにしているユーザーを別のフロントエンドプールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad543-110">Users homed on the SBA must be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="ad543-111">SBA がトポロジに戻された後、それらのユーザーを SBA に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="ad543-111">After the SBA is added back to the topology, those users can be moved back to the SBA.</span></span>

<span data-ttu-id="ad543-112">以下に、これらの手順の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="ad543-112">These steps are summarized below:</span></span>

1.  <span data-ttu-id="ad543-113">SBA に置かれているブランチユーザーを別のフロントエンドプールに移動します。</span><span class="sxs-lookup"><span data-stu-id="ad543-113">Move branch users homed on SBA to another Front End pool.</span></span>

2.  <span data-ttu-id="ad543-114">トポロジから SBA を削除して、既存のフロントエンドプールとバックアップレジストラーの関連付けを解除します。</span><span class="sxs-lookup"><span data-stu-id="ad543-114">Remove SBA from your topology to disassociate the existing Front End pool as the backup Registrar.</span></span>

3.  <span data-ttu-id="ad543-115">フロントエンドプールを Microsoft Lync Server 2013 にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="ad543-115">Upgrade Front End pool to Microsoft Lync Server 2013.</span></span>

4.  <span data-ttu-id="ad543-116">SBA をトポロジに追加し直します。</span><span class="sxs-lookup"><span data-stu-id="ad543-116">Add SBA back into your topology.</span></span>

5.  <span data-ttu-id="ad543-117">新しいフロントエンドプールをバックアップレジストラーとして SBA に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ad543-117">Associate the new Front End pool to the SBA as a backup Registrar.</span></span>

6.  <span data-ttu-id="ad543-118">ブランチユーザーを SBA に戻します。</span><span class="sxs-lookup"><span data-stu-id="ad543-118">Move branch users back to the SBA.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ad543-119">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ad543-119">In This Section</span></span>

  - [<span data-ttu-id="ad543-120">トポロジへの Lync Server 2013 存続可能ブランチ アプライアンスのブランチ サイトの追加</span><span class="sxs-lookup"><span data-stu-id="ad543-120">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [<span data-ttu-id="ad543-121">トポロジへの Lync Server 2010 存続可能ブランチ アプライアンスのブランチ サイトの追加</span><span class="sxs-lookup"><span data-stu-id="ad543-121">Add Lync Server 2010 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

<span data-ttu-id="ad543-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad543-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

