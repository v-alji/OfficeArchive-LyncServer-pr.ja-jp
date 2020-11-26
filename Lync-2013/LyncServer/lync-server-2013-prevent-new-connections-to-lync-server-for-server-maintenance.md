---
title: Lync Server への新しい接続でサーバーのメンテナンスができないようにする
description: サーバーメンテナンスのために Lync Server への新しい接続を禁止します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent new connections to Lync Server for server maintenance
ms:assetid: 22b27adf-a590-43bd-9306-a5789ae108d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520964(v=OCS.15)
ms:contentKeyID: 48183625
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd676467cdd6b5bb430f972e48c2f3a53f3f6f14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436898"
---
# <a name="prevent-new-connections-to-lync-server-2013-for-server-maintenance"></a><span data-ttu-id="0c896-103">Lync Server 2013 への新しい接続でサーバーのメンテナンスができないようにする</span><span class="sxs-lookup"><span data-stu-id="0c896-103">Prevent new connections to Lync Server 2013 for server maintenance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c896-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c896-104">

<span> </span></span></span>

<span data-ttu-id="0c896-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0c896-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0c896-106">Lync Server を使用すると、サービスが失われることなくサーバーをオフラインにすることができます (たとえば、ソフトウェアまたはハードウェアのアップグレードを適用することができます)。</span><span class="sxs-lookup"><span data-stu-id="0c896-106">Lync Server enables you to take a server offline (for example, to apply software or hardware upgrades) without any loss of service to users.</span></span>

<span data-ttu-id="0c896-107">プール内のサーバーへの新しい接続または呼び出しを禁止するオプションを指定すると、このオプションを実装するとすぐに、新しい接続と通話の取得が停止されます。</span><span class="sxs-lookup"><span data-stu-id="0c896-107">When you specify the option to prevent new connections or calls to a server in a pool, it stops taking any new connections and calls as soon as you implement this option.</span></span> <span data-ttu-id="0c896-108">これらの新しい接続と通話は、プール内の他のサーバーを経由してルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="0c896-108">These new connections and calls are routed through other servers in the pool.</span></span> <span data-ttu-id="0c896-109">新しい接続を禁止しているサーバーでは、既存の接続に対するセッションは自然に終了するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="0c896-109">A server that is preventing new connections allows its sessions on existing connections to continue until they naturally end.</span></span> <span data-ttu-id="0c896-110">既存のすべてのセッションが終了したら、サーバーをオフラインにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0c896-110">When all existing sessions have ended, the server is ready to be taken offline.</span></span>

<span data-ttu-id="0c896-111">フロントエンドサーバーへの新しい接続を禁止する場合、一部の Lync Server の機能とサービスは DNS の負荷分散を利用して適切に動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c896-111">When you prevent new connections to a Front End Server, some Lync Server features and services rely on DNS load balancing to ensure that it functions properly.</span></span> <span data-ttu-id="0c896-112">プールで DNS の負荷分散を使用していない場合、サーバーが新しい接続を妨害している期間中、これらのサービスを経由した接続が他のサーバーに再ルーティングされないことがあります。そのため、サーバーがオフラインになったときに、一部のセッションと通話が中断されることがあります。</span><span class="sxs-lookup"><span data-stu-id="0c896-112">If you are not using DNS load balancing on the pool, connections through these services may not be re-routed to other servers during the period that the server is preventing new connections, and thus when the server is taken offline some sessions and calls may be interrupted.</span></span> <span data-ttu-id="0c896-113">このオプションが適切に動作するように、DNS の負荷分散に依存する機能は次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="0c896-113">The features that rely on DNS load balancing to ensure that this option operates properly are as follows:</span></span>

  - <span data-ttu-id="0c896-114">Attendant</span><span class="sxs-lookup"><span data-stu-id="0c896-114">Attendant</span></span>

  - <span data-ttu-id="0c896-115">会議アナウンス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0c896-115">Conferencing Announcement application</span></span>

  - <span data-ttu-id="0c896-116">応答グループ アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0c896-116">Response Group application</span></span>

  - <span data-ttu-id="0c896-117">アナウンス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0c896-117">Announcement application</span></span>

  - <span data-ttu-id="0c896-118">コール パーク アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0c896-118">Call Park application</span></span>

<span data-ttu-id="0c896-119">DNS の負荷分散の詳細については、計画ドキュメントの「 [Lync Server 2013 での dns の負荷分散](lync-server-2013-dns-load-balancing.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c896-119">For details about DNS load balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<span data-ttu-id="0c896-120">Lync Server を実行しているサーバー上のすべてのサービスの新しい接続を防止するだけでなく、個々の Lync Server サービスへの新しい接続を防ぐこともできます。</span><span class="sxs-lookup"><span data-stu-id="0c896-120">In addition to preventing new connections for all services on a server running Lync Server, you can also prevent new connections for individual Lync Server services.</span></span> <span data-ttu-id="0c896-121">たとえば、この方法は、サーバー全体をシャットダウンする必要がない Lync Server の更新プログラムを適用する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0c896-121">For example, this method is useful in a situation where you need to apply a Lync Server update that does not require the whole server to be shut down.</span></span> <span data-ttu-id="0c896-122">1つのサービスに対する接続を禁止する場合は、サービスがグループ化され、サービスの一覧に表示されるサービスを選択する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0c896-122">Note that when you prevent connections for one service, you must select a service as it is grouped and displayed in the Windows list of services.</span></span> <span data-ttu-id="0c896-123">たとえば、Lync Server Front-End サービスと監視用のデータ収集エージェントは別々の Lync Server サービスであり、Windows services のリストでは統合され、Lync Server のフロントエンドサービスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c896-123">For example, the Lync Server Front-End service and the data collection agent for Monitoring are separate Lync Server services, but in the Windows services list they are consolidated and shown as the Lync Server Front End service.</span></span> <span data-ttu-id="0c896-124">Lync Server のフロントエンドサービスへの新しい接続を禁止することはできますが、この2つの基本的な Lync Server サービスへの新しい接続を個別に無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0c896-124">You can prevent new connections for the Lync Server Front End service, but you cannot prevent new connections for these two individual underlying Lync Server services separately.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="0c896-125">新しい接続を禁止するようにサーバーを設定してから、サーバーを再起動すると、既定では、サーバーは起動後に新しい接続の受け入れを直します。</span><span class="sxs-lookup"><span data-stu-id="0c896-125">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="0c896-126">これを防ぐには、サーバーを再起動する前に、手動で一時停止および再開するようにサーバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c896-126">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>



</div>

<div>

## <a name="to-prevent-new-connections-to-lync-server"></a><span data-ttu-id="0c896-127">Lync Server への新しい接続を禁止するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0c896-127">To prevent new connections to Lync Server:</span></span>

1.  <span data-ttu-id="0c896-128">Administrators グループのメンバーとして、ローカル コンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0c896-128">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="0c896-129">[サービス] スナップインコンソールを開きます。 [ **スタート**] をクリックし、[ **すべてのプログラム**] をポイントして、[ **管理ツール**] をポイントし、[ **サービス**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c896-129">Open the Services snap-in console: Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **Services**.</span></span>

3.  <span data-ttu-id="0c896-130">リストで、新しい接続を禁止する Lync Server Windows サービスをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c896-130">In the list, double-click the Lync Server Windows service to which you want to prevent new connections.</span></span>

4.  <span data-ttu-id="0c896-131">[プロパティ] ダイアログボックスの [ **サービスの状態: 開始**] で、[ **一時停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c896-131">In the Properties dialog box, under **Service status: Started**, click **Pause**.</span></span>

5.  <span data-ttu-id="0c896-132">必要に応じて、[ **スタートアップの種類**] の横にある [ **手動**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c896-132">Optionally, but recommended, next to **Startup type**, click **Manual**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="0c896-133">新しい接続を禁止するようにサーバーを設定してから、サーバーを再起動すると、既定では、サーバーは起動後に新しい接続の受け入れを直します。</span><span class="sxs-lookup"><span data-stu-id="0c896-133">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="0c896-134">これを防ぐには、サーバーを再起動する前に、手動で一時停止および再開するようにサーバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c896-134">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>

    
    </div>

6.  <span data-ttu-id="0c896-135">終了したら、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c896-135">When you are finished, click **OK**.</span></span>

<span data-ttu-id="0c896-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c896-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

