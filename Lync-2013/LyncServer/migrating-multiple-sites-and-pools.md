---
title: 複数のサイトとプールの移行
description: 複数のサイトとプールを移行する。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating multiple sites and pools
ms:assetid: a6d726d2-564d-4b39-a97c-5656a673292a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205165(v=OCS.15)
ms:contentKeyID: 48185079
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7efaa6f038286ff9138e631f23da88bb445e20f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440375"
---
# <a name="migrating-multiple-sites-and-pools"></a><span data-ttu-id="41dc8-103">複数のサイトとプールの移行</span><span class="sxs-lookup"><span data-stu-id="41dc8-103">Migrating multiple sites and pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41dc8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41dc8-104">

<span> </span></span></span>

<span data-ttu-id="41dc8-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="41dc8-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="41dc8-106">Lync Server 2013 は、複数サイトと複数プールの展開をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="41dc8-106">Lync Server 2013 supports multi-site and multi-pool deployments.</span></span> <span data-ttu-id="41dc8-107">複数のプールを Lync Server 2010 から Lync Server 2013 に移行するには、次の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41dc8-107">The process of migrating multiple pools from Lync Server 2010 to Lync Server 2013 requires the following considerations:</span></span>

1.  <span data-ttu-id="41dc8-108">Lync Server 2013 パイロットプールを展開した後、Lync Server 2013 プールに移動されるパイロットユーザーのサブセットと、ユーザーの機能を検証するための方法を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41dc8-108">After deploying a Lync Server 2013 pilot pool, you need to define a subset of pilot users that will be moved to the Lync Server 2013 pool, and a methodology for validating the functionality of the users.</span></span> <span data-ttu-id="41dc8-109">たとえば、パイロットプールにユーザーを移動した後、ユーザーの会議ポリシーが Lync Server 2013 に移動されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="41dc8-109">For example, after moving a user to the pilot pool, verify the user’s conference policy has moved to Lync Server 2013.</span></span>

2.  <span data-ttu-id="41dc8-110">パイロットプールにエッジサーバーを展開した後、外部ユーザーが Lync Server 2013 プールと通信できることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41dc8-110">After deploying an Edge Server in the pilot pool, you need to validate that external users can communicate with the Lync Server 2013 pool.</span></span>

3.  <span data-ttu-id="41dc8-111">Lync Server 2010 エッジサーバーからのフェデレーションルートを試験的な Lync Server 2013 エッジサーバーに移行した後、フェデレーションされたユーザーが Lync Server 2013 プールと通信できることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41dc8-111">After transitioning the federated routes from Lync Server 2010 Edge Servers to the pilot Lync Server 2013 Edge Servers, you need to validate that federated users can communicate with the Lync Server 2013 pool.</span></span>

4.  <span data-ttu-id="41dc8-112">すべてのユーザーと非ユーザーの連絡先オブジェクトを移動した後、Lync Server 2010 プールが空であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41dc8-112">After moving all the users and non-user contact objects, you need to validate that the Lync Server 2010 pool is empty.</span></span>

5.  <span data-ttu-id="41dc8-113">Lync Server 2010 プールが空であることを確認した後、プールを非アクティブ化することができます。</span><span class="sxs-lookup"><span data-stu-id="41dc8-113">After verifying that the Lync Server 2010 pool is empty, you can then deactivate the pool.</span></span>
    
    <span data-ttu-id="41dc8-114">従来の Lync Server 2010 プールとサーバーを非アクティブ化する方法について詳しくは、「 [フェーズ 8: レガシプールの廃止](phase-8-decommission-legacy-pools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="41dc8-114">For details about how to deactivate the legacy Lync Server 2010 pool and servers, see [Phase 8: Decommission legacy pools](phase-8-decommission-legacy-pools.md).</span></span>

<span data-ttu-id="41dc8-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41dc8-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

