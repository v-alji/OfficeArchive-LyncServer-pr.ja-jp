---
title: 'Lync Server 2013: プライマリ管理サーバーを構成する'
description: 'Lync Server 2013: プライマリ管理サーバーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the primary management server
ms:assetid: 44e2e9a8-c130-4c66-9871-80b1ff11b27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204844(v=OCS.15)
ms:contentKeyID: 48183986
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43f986f4f03e96cafa27dfdd302bb98a00d8b2ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400035"
---
# <a name="configuring-the-primary-management-server-in-lync-server-2013"></a><span data-ttu-id="9ef7c-103">Lync Server 2013 でのプライマリ管理サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="9ef7c-103">Configuring the primary management server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ef7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ef7c-104">

<span> </span></span></span>

<span data-ttu-id="9ef7c-105">_**最終更新日:** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="9ef7c-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="9ef7c-106">Microsoft Lync Server 2013 に含まれている新しい正常性監視機能を最大限に活用するためには、まず、プライマリ管理サーバーとして動作するようにコンピューターを指定する必要があります。そのコンピューターで、System Center Operations Manager 2007 R2 または System Center Operations Manager 2012 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-106">In order to take full advantage of the new health monitoring capabilities included in Microsoft Lync Server 2013 administrators must first designate a computer to act as your primary management server; on that computer you must then install System Center Operations Manager 2007 R2 or System Center Operations Manager 2012.</span></span> <span data-ttu-id="9ef7c-107">さらに、サポートされているバージョンの SQL Server を、Operations Manager バックエンドデータベースとして機能するようにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-107">In addition, you must install a supported version of SQL Server to function as your Operations Manager back-end database.</span></span> <span data-ttu-id="9ef7c-108">System Center Operations Manager 2012 を使用している場合は、次のいずれかのバージョンの SQL Server をバックエンドデータベースとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-108">If you are using System Center Operations Manager 2012 you can use any of the following versions of SQL Server as your back-end database:</span></span>

  - <span data-ttu-id="9ef7c-109">SQL Server 2008 R2 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="9ef7c-109">SQL Server 2008 R2 Service Pack 1</span></span>

  - <span data-ttu-id="9ef7c-110">SQL Server 2008 R2 Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="9ef7c-110">SQL Server 2008 R2 Service Pack 2</span></span>

<span data-ttu-id="9ef7c-111">System Center Operations Manager 2007 R2 を使用している場合は、SQL Server 2005 Service Pack 4 または SQL Server 2008 Service Pack 3 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-111">If you are using System Center Operations Manager 2007 R2 it is recommended that you install either SQL Server 2005 Service Pack 4 or SQL Server 2008 Service Pack 3.</span></span> <span data-ttu-id="9ef7c-112">また、System Center Operations Manager 2007 R2 のバックエンドデータベースとして SQL Server 2008 R2 を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-112">You can also use SQL Server 2008 R2 as the backend database for System Center Operations Manager 2007 R2.</span></span> <span data-ttu-id="9ef7c-113">SQL Server 2008 R2 を System Center Operations Manager 2007 R2 と連携するように構成する方法については、このドキュメントの「付録1」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-113">See Appendix 1 of this documentation for more information on configuring SQL Server 2008 R2 to work with System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="9ef7c-114">System Center Operations Manager 2012 または System Center Operations Manager 2007 R2 をインストールするには、次のような製品のすべてのコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-114">When you install System Center Operations Manager 2012 or System Center Operations Manager 2007 R2 you need to install all the components of that product, including:</span></span>

  - <span data-ttu-id="9ef7c-115">オペレーション データベース</span><span class="sxs-lookup"><span data-stu-id="9ef7c-115">Operational database</span></span>

  - <span data-ttu-id="9ef7c-116">サーバー</span><span class="sxs-lookup"><span data-stu-id="9ef7c-116">Server</span></span>

  - <span data-ttu-id="9ef7c-117">コンソール</span><span class="sxs-lookup"><span data-stu-id="9ef7c-117">Console</span></span>

  - <span data-ttu-id="9ef7c-118">Windows PowerShell コマンドレット</span><span class="sxs-lookup"><span data-stu-id="9ef7c-118">Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="9ef7c-119">Web コンソール</span><span class="sxs-lookup"><span data-stu-id="9ef7c-119">Web console</span></span>

  - <span data-ttu-id="9ef7c-120">レポート</span><span class="sxs-lookup"><span data-stu-id="9ef7c-120">Reporting</span></span>

  - <span data-ttu-id="9ef7c-121">データ ウェアハウス</span><span class="sxs-lookup"><span data-stu-id="9ef7c-121">Data warehouse</span></span>

<span data-ttu-id="9ef7c-122">このドキュメントでは、これらのコンポーネントとそのインストールについて詳しくは説明しません。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-122">These components and their installation will not be discussed in detail in this document.</span></span> <span data-ttu-id="9ef7c-123">System Center Operations Manager 2007 R2 の詳細については、「Operations Manager 2007 R2 のドキュメント」 <https://go.microsoft.com/fwlink/p/?linkid=257526> および System Center Operations manager 2012 のドキュメントを参照してください <https://go.microsoft.com/fwlink/p/?linkid=257527> 。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-123">For details about System Center Operations Manager 2007 R2, see the Operations Manager 2007 R2 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257526> and the System Center Operations Manager 2012 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257527>.</span></span> <span data-ttu-id="9ef7c-124">SQL Server 2005 または SQL Server 2008 Service Pack 1 をバックエンドデータベースとして使用する場合は、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-124">You should follow those instructions if you are going to use SQL Server 2005 or SQL Server 2008 Service Pack 1 as your back-end database.</span></span>

<span data-ttu-id="9ef7c-125">System Center Operations Manager 2012 を使用している場合は、バックエンドデータベースとして SQL Server 2012 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-125">If you are using System Center Operations Manager 2012 then you can use SQL Server 2012 as your back-end database.</span></span> <span data-ttu-id="9ef7c-126">SQL Server 2012 の詳細については、「SQL Server 2012 のオンラインブック」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528) 。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-126">For details about SQL Server 2012, see Books Online for SQL Server 2012 at [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528).</span></span>

<span data-ttu-id="9ef7c-127">Lync Server の展開ごとに1つのプライマリ管理サーバーしか設定できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-127">Keep in mind that you can only have a single Primary Management Server per Lync Server deployment.</span></span> <span data-ttu-id="9ef7c-128">また、System Center Operations Manager 2012 または System Center Operations Manager 2007 R2 のいずれかを使用できますが、2つのアプリケーションを同時に実行することはできません。どちらか一方を選ぶ必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-128">Also, while you can use either System Center Operations Manager 2012 or System Center Operations Manager 2007 R2, you cannot run the two applications simultaneously—you must choose one or the other.</span></span> <span data-ttu-id="9ef7c-129">たとえば、System Center Operations Manager 2012 を実行している場合、System Center エージェントも System Center Operations Manager 2012 を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-129">For example, if you are running System Center Operations Manager 2012 then all your System Center agents must also be running System Center Operations Manager 2012.</span></span> <span data-ttu-id="9ef7c-130">System Center Operations Manager 2012 と System Center Operations Manager 2007 R2 を実行しているエージェントの一部を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="9ef7c-130">You cannot have some agents running System Center Operations Manager 2012 and other agents running System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="9ef7c-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ef7c-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

