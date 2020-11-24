---
title: 'Lync Server 2013: サーバーおよびツールのオペレーティング システムのサポート'
description: 'Lync Server 2013: サーバーとツールのオペレーティングシステムサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server and tools operating system support
ms:assetid: b65a0956-f90d-48d0-ac61-558e67339084
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412883(v=OCS.15)
ms:contentKeyID: 48185214
ms.date: 12/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 67cf2e39e0c8f9e66f755b16be03af37dd9a946e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399500"
---
# <a name="server-and-tools-operating-system-support-in-lync-server-2013"></a><span data-ttu-id="32594-103">Lync Server 2013 でのサーバーおよびツールのオペレーティング システムのサポート</span><span class="sxs-lookup"><span data-stu-id="32594-103">Server and tools operating system support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32594-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32594-104">

<span> </span></span></span>

<span data-ttu-id="32594-105">_**最終更新日:** 2014-12-01_</span><span class="sxs-lookup"><span data-stu-id="32594-105">_**Topic Last Modified:** 2014-12-01_</span></span>

<span data-ttu-id="32594-106">Lync Server 2013 は、64ビットでのみ使用できます。これには、64ビットハードウェアと64ビット版の Windows Server が必要です。</span><span class="sxs-lookup"><span data-stu-id="32594-106">Lync Server 2013 is available only in 64-bit, which requires 64-bit hardware and 64-bit editions of Windows Server.</span></span> <span data-ttu-id="32594-107">つまり、Lync Server 2013 管理ツールを実行しているすべてのサーバーの役割とコンピューターは、64ビット版のオペレーティングシステムを実行します。</span><span class="sxs-lookup"><span data-stu-id="32594-107">This means that all server roles and computers running Lync Server 2013 administrative tools run a 64-bit edition operating system.</span></span>

<div>

## <a name="operating-systems-for-server-roles"></a><span data-ttu-id="32594-108">サーバーロールのオペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-108">Operating Systems for Server Roles</span></span>

<span data-ttu-id="32594-109">Lync Server 2013 は、Lync Server 2013 のすべてのサーバーの役割について、次のオペレーティングシステムの64ビットエディションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="32594-109">Lync Server 2013 supports the 64-bit editions of the following operating systems for all server roles in Lync Server 2013:</span></span>

  - <span data-ttu-id="32594-110">Windows Server 2008 R2 Service Pack 1 (SP1) 標準オペレーティングシステム (必須) または最新の Service pack (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-110">The Windows Server 2008 R2 with Service Pack 1 (SP1) Standard operating system (required) or latest service pack (recommended)</span></span>

  - <span data-ttu-id="32594-111">Windows Server 2008 R2 SP1 Enterprise オペレーティングシステム (必須) または最新サービスパック (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-111">The Windows Server 2008 R2 with SP1 Enterprise operating system (required) or latest service pack (recommended)</span></span>

  - <span data-ttu-id="32594-112">Windows Server 2008 R2 SP1 Datacenter オペレーティングシステム (必須) または最新サービスパック (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-112">The Windows Server 2008 R2 with SP1 Datacenter operating system (required) or latest service pack (recommended)</span></span>

  - <span data-ttu-id="32594-113">Windows Server 2012 標準オペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-113">The Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="32594-114">Windows Server 2012 Datacenter オペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-114">The Windows Server 2012 Datacenter operating system</span></span>

  - <span data-ttu-id="32594-115">Windows Server 2012 R2 オペレーティングシステムは、Lync Server 2013: 2013 年10月の累積更新プログラムでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="32594-115">The Windows Server 2012 R2 operating systems are supported with the Cumulative Updates for Lync Server 2013: October 2013.</span></span>

<span data-ttu-id="32594-116">Lync Server 2013 は、次のようにサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="32594-116">Lync Server 2013 is not supported on the following:</span></span>

  - <span data-ttu-id="32594-117">Windows Server 2008 R2 または Windows Server 2012 の Server Core インストールオプション</span><span class="sxs-lookup"><span data-stu-id="32594-117">The Server Core installation option of Windows Server 2008 R2 or Windows Server 2012</span></span>

  - <span data-ttu-id="32594-118">Windows Web Server 2008 R2 オペレーティングシステムまたは Windows Web Server 2012 オペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-118">The Windows Web Server 2008 R2 operating system or the Windows Web Server 2012 operating system</span></span>

  - <span data-ttu-id="32594-119">Windows Server 2008 R2 HPC または Windows Server 2012 HPC エディション</span><span class="sxs-lookup"><span data-stu-id="32594-119">Windows Server 2008 R2 HPC Edition or Windows Server 2012 HPC Edition</span></span>

</div>

<div>

## <a name="additional-operating-systems-for-administrative-tools"></a><span data-ttu-id="32594-120">管理ツール用のその他のオペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-120">Additional Operating Systems for Administrative Tools</span></span>

<span data-ttu-id="32594-121">Lync server 2013 管理ツールは、Lync Server 2013 を実行しているサーバー上に既定でインストールされますが、Windows オペレーティングシステムを実行している他のコンピューターでは、管理ツールを個別にインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="32594-121">Lync Server 2013 administrative tools are installed by default on servers running Lync Server 2013, but you can install administrative tools separately on other computers running Windows operating systems.</span></span> <span data-ttu-id="32594-122">これには、次のオペレーティングシステムの64ビットバージョン、およびサーバーロールの展開をサポートするオペレーティングシステムの64ビットエディション (前のセクションで説明した) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="32594-122">These include the following 64-bit versions of the following operating systems, in addition to the 64-bit editions of the operating systems supported for deployment of server roles (as described in the previous section).</span></span>

  - <span data-ttu-id="32594-123">Windows 7 オペレーティングシステム SP1 オペレーティングシステム (必須) または最新サービスパック (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-123">The Windows 7 operating system with SP1 operating system (required) or latest service pack (recommended)</span></span>

  - <span data-ttu-id="32594-124">Windows 8 オペレーティングシステムまたは最新の service pack (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-124">The Windows 8 operating system or latest service pack (recommended)</span></span>

  - <span data-ttu-id="32594-125">Windows 8.1 オペレーティングシステムまたは最新の service pack (推奨)</span><span class="sxs-lookup"><span data-stu-id="32594-125">The Windows 8.1 operating system or latest service pack (recommended)</span></span>

</div>

<div>

## <a name="operating-systems-for-other-servers-in-your-deployment"></a><span data-ttu-id="32594-126">展開における他のサーバーのオペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="32594-126">Operating Systems for Other Servers in Your Deployment</span></span>

  - <span data-ttu-id="32594-127">バックエンドサーバーと他のデータベースサーバーの要件の詳細については、「 [Lync Server 2013 でのデータベースソフトウェアのサポート](lync-server-2013-database-software-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32594-127">For details about requirements for Back End Servers and other database servers, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span>

  - <span data-ttu-id="32594-128">リバースプロキシサーバー (Edge の展開用) の要件の詳細については、「 [Lync Server 2013 での IIS のサポート](lync-server-2013-iis-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32594-128">For details about requirements for reverse proxy servers (for Edge deployment), see [IIS support in Lync Server 2013](lync-server-2013-iis-support.md).</span></span>

  - <span data-ttu-id="32594-129">他のソフトウェア要件 (インフラストラクチャと仮想化のサポートなど) について詳しくは、「 [Lync server 2013 でのサーバーソフトウェアとインフラストラクチャのサポート](lync-server-2013-server-software-and-infrastructure-support.md)」の他のトピックをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="32594-129">For details about other software requirements, including infrastructure and virtualization support, see the other topics in the [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md).</span></span>

<span data-ttu-id="32594-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32594-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

