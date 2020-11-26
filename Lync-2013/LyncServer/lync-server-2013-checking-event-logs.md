---
title: 'Lync Server 2013: イベントログを確認する'
description: 'Lync Server 2013: イベントログを確認しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking event logs
ms:assetid: 5500720d-c628-4dbd-84bc-a5becc39b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720914(v=OCS.15)
ms:contentKeyID: 63969602
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6617bde846fd38ab3282fd023b16e0a921f48920
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434929"
---
# <a name="checking-event-logs-in-lync-server-2013"></a><span data-ttu-id="5a09f-103">Lync Server 2013 でイベントログを確認する</span><span class="sxs-lookup"><span data-stu-id="5a09f-103">Checking event logs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a09f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a09f-104">

<span> </span></span></span>

<span data-ttu-id="5a09f-105">_**最終更新日:** 2014-08-06_</span><span class="sxs-lookup"><span data-stu-id="5a09f-105">_**Topic Last Modified:** 2014-08-06_</span></span>

<span data-ttu-id="5a09f-106">[Windows イベントビューアー](https://go.microsoft.com/fwlink/p/?linkid=314067)を使用して、イベントログを表示したり、サービスエラー、AD DS のレプリケーションエラー、仮想メモリやディスク容量などのシステムリソースに関する警告を表示したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-106">You can use [Windows Event Viewer](https://go.microsoft.com/fwlink/p/?linkid=314067) to view event logs and obtain information about service failures, replication errors in the AD DS, and warnings about system resources such as virtual memory and disk space.</span></span> <span data-ttu-id="5a09f-107">イベントビューアーは、Windows Server 2008 および2012に含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a09f-107">Event Viewer is included with Windows Server 2008 and 2012.</span></span>

<span data-ttu-id="5a09f-108">Lync Server 2013 ログツールで、デバッグセッションを終了するときに、[ **ログファイルの分析** ] をクリックして、ログファイルを表示するには、Snooper ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-108">In the Lync Server 2013 Logging Tool, when you end the debug session, click **Analyze Log Files** to view the log files by using the Snooper tool.</span></span>

<span data-ttu-id="5a09f-109">イベントビューアーは、コンピューター上のアプリケーション、セキュリティ、およびシステムイベントに関するログを保持します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-109">Event Viewer maintains logs about application, security, and system events on the computer.</span></span> <span data-ttu-id="5a09f-110">Lync Server 2013 と Windows は両方とも、イベントログの警告とエラー状態を報告します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-110">Both Lync Server 2013 and Windows report warnings and error conditions to the event logs.</span></span> <span data-ttu-id="5a09f-111">そのため、毎日イベントログを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-111">Therefore, review event logs daily.</span></span>

<span data-ttu-id="5a09f-112">イベントビューアーを使用して、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5a09f-112">Use Event Viewer to:</span></span>

  - <span data-ttu-id="5a09f-113">イベントログを表示して管理します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-113">View and manage event logs.</span></span>

  - <span data-ttu-id="5a09f-114">解決する必要があるハードウェア、ソフトウェア、およびシステムの問題に関する情報を入手します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-114">Obtain information about hardware, software, and system issues that must be resolved.</span></span>

  - <span data-ttu-id="5a09f-115">将来の対処が必要な傾向を特定します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-115">Identify trends that require future action.</span></span>

<span data-ttu-id="5a09f-116">Windows Server オペレーティングシステムで Lync Server を実行しているサーバーでは、次の4種類のログにイベントが記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-116">A server that is running Lync Server on a Windows Server operating system records events in four types of logs:</span></span>

  - <span data-ttu-id="5a09f-117">**アプリケーションログ**   アプリケーションログには、アプリケーションやプログラムによって記録されるイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-117">**Application logs**   The Application log contains events logged by applications or programs.</span></span> <span data-ttu-id="5a09f-118">記録するイベントは、開発者が決定します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-118">Developers determine which events to log.</span></span> <span data-ttu-id="5a09f-119">たとえば、データベースプログラムでは、アプリケーションログにファイルエラーが記録されることがあります。</span><span class="sxs-lookup"><span data-stu-id="5a09f-119">For example, a database program might record a file error in the Application log.</span></span> <span data-ttu-id="5a09f-120">ほとんどの Lync Server 2013 関連イベントは、アプリケーションログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-120">Most Lync Server 2013-related events appear in the Application log.</span></span>

  - <span data-ttu-id="5a09f-121">**セキュリティログ**   セキュリティログには、ファイルまたはその他のオブジェクトの作成、オープン、削除などのリソースの使用に関連するイベントに加えて、有効な、有効でないというイベントが記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-121">**Security logs**   The Security log records events such as valid and not valid logon tries in addition to events related to resource use such as creating, opening, or deleting files or other objects.</span></span> <span data-ttu-id="5a09f-122">たとえば、ログオン監査が有効になっている場合、システムへのログオン試行はセキュリティログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-122">For example, if logon auditing is enabled, attempts to log on to the system are recorded in the Security log.</span></span>

  - <span data-ttu-id="5a09f-123">**システムログ**   システムログには、Windows システムコンポーネントによってログ記録されるイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a09f-123">**System logs**   The System log contains events logged by Windows system components.</span></span> <span data-ttu-id="5a09f-124">たとえば、ドライバーなどのシステムコンポーネントの起動中に読み込みに失敗した場合、システムログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-124">For example, the failure of a driver or other system component to load during startup is recorded in the System log.</span></span> <span data-ttu-id="5a09f-125">システムコンポーネントによってログに記録されるイベントの種類は、サーバーで事前に定義されています。</span><span class="sxs-lookup"><span data-stu-id="5a09f-125">The event types logged by system components are predetermined by the server.</span></span>

  - <span data-ttu-id="5a09f-126">**Lync Server 2013**   ログツールには、認証、接続、ユーザー操作に関連する重要なイベントが記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-126">**Lync Server 2013**   The logging tool records significant events related to authentication, connections, and user actions.</span></span> <span data-ttu-id="5a09f-127">診断ログを有効にした後は、イベントビューアーでログエントリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-127">After enabling diagnostic logging, you can view the log entries in Event Viewer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5a09f-128">Microsoft カスタマサポートサービスによって指示されていない限り、最大ログ設定を使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="5a09f-128">We do not recommend that you use the maximum logging settings unless you are instructed to do this by Microsoft Customer Support Services.</span></span> <span data-ttu-id="5a09f-129">最大ログ記録によって、大量のリソースが消費され、多くの "誤検知" が発生することがあります。これは、最大のログ記録でのみ記録されるエラーであり、問題の原因ではありません。</span><span class="sxs-lookup"><span data-stu-id="5a09f-129">Maximum logging drains significant resources and can give many “false positives,” that is, errors that get logged only at maximum logging but are really expected and are not a cause of concern.</span></span> <span data-ttu-id="5a09f-130">また、診断ログを完全に有効にしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5a09f-130">We also recommend that you do not enable diagnostic logging permanently.</span></span> <span data-ttu-id="5a09f-131">トラブルシューティング時にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="5a09f-131">Use it only when troubleshooting.</span></span>



</div>

<span data-ttu-id="5a09f-132">各イベントビューアーログには、Lync Server 2013 で情報通知、警告イベント、エラーイベントが記録されます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-132">Within each Event Viewer log, Lync Server 2013 records informational, warning, and error events.</span></span> <span data-ttu-id="5a09f-133">これらのログを慎重に監視して、Lync Server 2013 サーバー上で実行されているトランザクションの種類を追跡します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-133">Monitor these logs closely to track the types of transactions being conducted on the Lync Server 2013 servers.</span></span> <span data-ttu-id="5a09f-134">ログを定期的にアーカイブするか、自動的なロールオーバーを使って領域が不足しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a09f-134">You should periodically archive the logs or use automatic rollover to avoid running out of space.</span></span> <span data-ttu-id="5a09f-135">ログファイルは、一定の量の領域を占有している可能性があるため、ログサイズを大きくし (たとえば、50 MB)、Lync Server 2013 サーバーが新しいイベントの書き込みを続行できるように、上書きするように設定します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-135">Because log files can occupy a finite amount of space, increase the log size (for example, to 50 MB) and set it to overwrite so that the Lync Server 2013 Server can continue to write new events.</span></span>

<span data-ttu-id="5a09f-136">次のツールとテクノロジを使用して、イベントログの管理を自動化することもできます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-136">You can also automate event log administration by using the following tools and technologies:</span></span>

  - <span data-ttu-id="5a09f-137">System Center Operations Manager は、Lync Server 2013 サーバーの正常性および使用状況を監視します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-137">System Center Operations Manager monitors the health and use of Lync Server 2013 servers.</span></span> <span data-ttu-id="5a09f-138">Lync Server 2013 Management Pack for Operations Manager は、Lync Server 2013 を実行しているサーバーの特別な監視機能を提供して、Operations Manager を拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-138">Lync Server 2013 Management Pack for Operations Manager extends Operations Manager by providing specialized monitoring for servers that are running Lync Server 2013.</span></span>

  - <span data-ttu-id="5a09f-139">Lync Server 2013 Management Pack for Operations Manager は、標準およびエンタープライズ版の Lync Server 2013 を監視します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-139">The Lync Server 2013 Management Pack for Operations Manager monitors Standard and Enterprise Edition of Lync Server 2013.</span></span> <span data-ttu-id="5a09f-140">このリリースには、以前は別の管理パックとして使用されていた Quality of Experience (QoE) 管理パックも組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="5a09f-140">This release also incorporates the Quality of Experience (QoE) Management Pack which was previously a separate management pack.</span></span>

<span data-ttu-id="5a09f-141">監視される型は、イベントログエントリ、パフォーマンスカウンター、QoE のステートフル監視です。</span><span class="sxs-lookup"><span data-stu-id="5a09f-141">Monitored types are event log entries, performance counters and stateful monitoring of QoE.</span></span> <span data-ttu-id="5a09f-142">このバージョンの管理パックは、Lync Server 2013 および2010のみを監視し、Office Communications Server 2007 を監視するために使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="5a09f-142">This version of the management pack only monitors Lync Server 2013 and 2010, and cannot be used to monitor Office Communications Server 2007.</span></span>

<span data-ttu-id="5a09f-143">管理パックは、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-143">The management pack provides the following features:</span></span>

  - <span data-ttu-id="5a09f-144">サービスに影響を与えるイベントを示すアラート</span><span class="sxs-lookup"><span data-stu-id="5a09f-144">Alerts indicating service affecting events</span></span>

  - <span data-ttu-id="5a09f-145">構成、およびその他のサービス以外の影響の問題を示すアラート</span><span class="sxs-lookup"><span data-stu-id="5a09f-145">Alerts indicating configuration, and other non-service impacting issues</span></span>

  - <span data-ttu-id="5a09f-146">Lync Server サービスの状態監視</span><span class="sxs-lookup"><span data-stu-id="5a09f-146">State monitoring of Lync Server services</span></span>

  - <span data-ttu-id="5a09f-147">製品情報: 特定された問題の原因と解決策</span><span class="sxs-lookup"><span data-stu-id="5a09f-147">Product knowledge: Cause and resolution of identified issues</span></span>

<span data-ttu-id="5a09f-148">Lync Server 2013 管理パックの詳細については、「 [System Center Operations Manager を使用して Lync server 2013 を監視](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a09f-148">For more information about Lync Server 2013 Management Pack, refer to [Monitoring Lync Server 2013 with System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md).</span></span>

<span data-ttu-id="5a09f-149">**イベントのマス**   目  イベントマス目ツールは、複数のコンピューターのイベントログから特定のイベントを1か所にまとめて収集します。</span><span class="sxs-lookup"><span data-stu-id="5a09f-149">**Event Comb**   The Event Comb tool collects specific events from the event logs of several computers to one central location.</span></span> <span data-ttu-id="5a09f-150">指定したイベント Id またはイベントソースのみをレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-150">It lets you report on only the event IDs or event sources it specifies.</span></span> <span data-ttu-id="5a09f-151">イベントのマス目の詳細については、 [アカウントのロックアウトと管理ツール](https://go.microsoft.com/fwlink/?linkid=35607) の web サイトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a09f-151">For more information about Event Comb, see the [Account Lockout and Management Tools](https://go.microsoft.com/fwlink/?linkid=35607) website.</span></span>

<span data-ttu-id="5a09f-152">**イベントトリガー**   Windows Server 2012 では、管理者がプログラムを実行するか、メールメッセージを送信するか、または画面上のメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-152">**Event triggers**   In Windows Server 2012 you can "Attach a Task to This Event" within the Windows Event Viewer—where an administrator can either run a program, send an email message or display an on-screen message.</span></span> <span data-ttu-id="5a09f-153">この機能の詳細については、Windows Server 2008 R2 のトピック「 [特定のイベントに応答してタスクを実行](https://technet.microsoft.com/library/cc748900.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a09f-153">For more information about this feature, see the Windows Server 2008 R2 topic [Run a Task in Response to a Given Event](https://technet.microsoft.com/library/cc748900.aspx).</span></span> <span data-ttu-id="5a09f-154">また、' Eventtrigger.exe ' などのコマンドラインツールを使用して、イベントログの作成と照会、および特定のログに記録されたイベントへのプログラムの関連付けを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-154">You can also use command-line tools such as ‘Eventtrigger.exe’ to create and query event logs and associate programs with particular logged events.</span></span> <span data-ttu-id="5a09f-155">Eventtriggers.exe を使うことで、特定のイベントが発生したときにプログラムを実行するイベントトリガーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5a09f-155">By using Eventtriggers.exe, you can create event triggers that run programs when specific events occur.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="5a09f-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a09f-156">See Also</span></span>


[<span data-ttu-id="5a09f-157">Windows イベントビューアー</span><span class="sxs-lookup"><span data-stu-id="5a09f-157">Windows Event Viewer</span></span>](https://go.microsoft.com/fwlink/p/?linkid=314067)  
  

<span data-ttu-id="5a09f-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a09f-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

