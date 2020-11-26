---
title: 'Lync Server 2013: Lync Server 2013 管理パックのインポート'
description: 'Lync Server 2013: Lync Server 2013 管理パックをインポートします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Importing the Lync Server 2013 management packs
ms:assetid: 846287e1-660f-453f-bdba-b2137b5f0ea1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205052(v=OCS.15)
ms:contentKeyID: 48184690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9615e559baf2f1c8b99015f1e407230559ff770
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427328"
---
# <a name="importing-the-lync-server-2013-management-packs"></a><span data-ttu-id="70155-103">Lync Server 2013 管理パックのインポート</span><span class="sxs-lookup"><span data-stu-id="70155-103">Importing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70155-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70155-104">

<span> </span></span></span>

<span data-ttu-id="70155-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="70155-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="70155-106">管理パック (System Center Operations Manager が監視できる項目を決定するソフトウェア、およびそれらの項目を監視する方法、およびアラートをトリガーおよび報告する方法を規定するソフトウェア) をインストールすることで、System Center Operations Manager の機能を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="70155-106">You can extend the capabilities of System Center Operations Manager by installing management packs—software that dictates which items System Center Operations Manager can monitor, and how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="70155-107">Lync Server 2013 には、次の機能を提供する System Center Operations Manager の2つの管理パックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="70155-107">Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="70155-108">コンポーネントとユーザー管理パック (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) は、イベントログに記録された Lync Server の問題を追跡し、パフォーマンスカウンターで登録するか、通話の詳細レコード (CDR) または Quality of Experience (QoE) データベースに記録します。</span><span class="sxs-lookup"><span data-stu-id="70155-108">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="70155-109">重大な問題については、System Center Operations Manager を構成して、メール、インスタントメッセージ、またはショートメッセージサービス (SMS) メッセージングを使って管理者にすぐに通知することができます。</span><span class="sxs-lookup"><span data-stu-id="70155-109">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="70155-110">SMS は、あるモバイルデバイスから別のモバイルデバイスにテキストメッセージを送信するために使用されるテクノロジです。)</span><span class="sxs-lookup"><span data-stu-id="70155-110">SMS is the technology used to send text messages from one mobile device to another.)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="70155-111">Operations Manager の通知の構成の詳細については、TechNet ライブラリの「通知を設定する」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?LinkId=268785</A> 。</span><span class="sxs-lookup"><span data-stu-id="70155-111">For details about configuring Operations Manager notification, see the Configuring Notification in the TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?LinkId=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="70155-112">アクティブな監視管理パック (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) は、システムにサインインしたり、インスタントメッセージを交換したり、公衆交換電話網 (PSTN) にある電話への通話を発信したりするなど、Lync Server の主要コンポーネントを事前にテストします。</span><span class="sxs-lookup"><span data-stu-id="70155-112">The Active Monitoring Management Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as signing into to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="70155-113">これらのテストは、Lync Server の代理トランザクションコマンドレットを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="70155-113">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="70155-114">たとえば、テスト **用の cgi** コマンドレットを使用して、1組のテストユーザー間のインスタントメッセージング (IM) 会話をシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="70155-114">For example, you can use the **Test-CsIM** cmdlet to simulate an instant messaging (IM) conversation between a pair of test users.</span></span> <span data-ttu-id="70155-115">このシミュレートされたメッセージの会話に失敗した場合は、アラートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="70155-115">If this simulated messaging conversation fails an alert is generated.</span></span>

<span data-ttu-id="70155-116">管理パックをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70155-116">You need to import the management packs.</span></span> <span data-ttu-id="70155-117">管理パックをインポートしない場合、Operations Manager を使用して Lync Server イベントを監視したり、Lync Server の代理トランザクションを実行したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="70155-117">If you do not import the management packs, you cannot use Operations Manager to monitor Lync Server events or run Lync Server synthetic transactions.</span></span>

<span data-ttu-id="70155-118">コンポーネントとユーザー管理パックは、Lync Server 2013 を監視するためだけに使用されます。</span><span class="sxs-lookup"><span data-stu-id="70155-118">The Component and User Management Pack is only used to monitor Lync Server 2013.</span></span> <span data-ttu-id="70155-119">Lync Server 2013 と Lync Server 2010 の両方がインストールされている共存シナリオを使用している場合は、引き続き lync server 2010 コンピューター用の Lync Server 2010 管理パックを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70155-119">If you are in a coexistence scenario, where you have both Lync Server 2013 and Lync Server 2010 installed, you should continue to use the Lync Server 2010 management packs for your Lync Server 2010 computers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="70155-120">Lync server 2010 用の管理パックには、Lync Server 2010 監視管理パックと Lync Server 2010 グループチャット監視管理パックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="70155-120">Management packs for Lync Server 2010 include the Lync Server 2010 Monitoring Management Pack and the Lync Server 2010 Group Chat Monitoring Management Pack.</span></span>



</div>

<span data-ttu-id="70155-121">次のいずれかのツールを使用して、管理パックをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="70155-121">You can use one of the following tools to import management packs:</span></span>

  - <span data-ttu-id="70155-122">**System Center Operations Manager**   この方法では、Operations Manager を使って Lync Server の監視を追加します。</span><span class="sxs-lookup"><span data-stu-id="70155-122">**System Center Operations Manager**   With this method, you use the Operations Manager to add monitoring for Lync Server.</span></span>

  - <span data-ttu-id="70155-123">**Operations Manager Shell**   Operations Manager Shell を使用して直接インポートすることも、System Center Operations Manager コンソールを使用して管理パックをインポートするときに発生する問題のトラブルシューティングを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="70155-123">**Operations Manager Shell**   You can use the Operations Manager Shell to import directly or to troubleshoot any issues you encounter when you import management packs by using the System Center Operations Manager console.</span></span>

<div>

## <a name="importing-the-management-packs-by-using-system-center-operations-manager"></a><span data-ttu-id="70155-124">System Center Operations Manager を使用した管理パックのインポート</span><span class="sxs-lookup"><span data-stu-id="70155-124">Importing the Management Packs by Using System Center Operations Manager</span></span>

1.  <span data-ttu-id="70155-125">Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp と Microsoft.LS.2013.Monitoring.ComponentAndUser.mp ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="70155-125">Download the files Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp and Microsoft.LS.2013.Monitoring.ComponentAndUser.mp.</span></span>

2.  <span data-ttu-id="70155-126">System Center Operations Manager で、[ **管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-126">In System Center Operations Manager, click **Administration**.</span></span>

3.  <span data-ttu-id="70155-127">[管理 **] ウィンドウ** で、[ **管理パック**] を右クリックし、[ **管理パックのインポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-127">In the **Administration** pane, right-click **Management Packs**, and then click **Import Management Packs**.</span></span>

4.  <span data-ttu-id="70155-128">[**管理パックの選択**] ダイアログ ボックスで、[**追加**] をクリックし、[**ディスクから追加する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-128">In the **Select Management Packs** dialog box, click **Add**, and then click **Add from disk**.</span></span>

5.  <span data-ttu-id="70155-129">[ **オンラインカタログ接続** ] ダイアログボックスで、[ **キャンセル** ] をクリックして、Lync Server 管理パックの依存関係が存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="70155-129">In the **Online Catalog Connection** dialog box, click **Cancel** to prevent Operations Manager from going online to see if any dependencies exist for the Lync Server management packs.</span></span> <span data-ttu-id="70155-130">System Center Operations Manager 2012 を使っている場合は、[ **いいえ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-130">If you are using System Center Operations Manager 2012, click **No**.</span></span>

6.  <span data-ttu-id="70155-131">**[インポートする管理パックの選択**] ダイアログボックスで、 **Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp** と **Microsoft.LS.2013.Monitoring.ComponentAndUser.mp** ファイルを探して選び、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-131">In the **Select Management Packs to import** dialog box, locate and select the files **Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp** and **Microsoft.LS.2013.Monitoring.ComponentAndUser.mp** and then click **Open**.</span></span> <span data-ttu-id="70155-132">ダイアログボックスで複数のファイルを選択するには、最初のファイルをクリックし、Ctrl キーを押しながら2番目のファイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-132">To select multiple files in the dialog box, click the first file, hold down the Ctrl key and then click the second file.</span></span>

7.  <span data-ttu-id="70155-133">[**管理パックの選択**] ダイアログ ボックスで、[**インストール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-133">In the **Select Management Packs** dialog box, click **Install**.</span></span> <span data-ttu-id="70155-134">エラー メッセージが表示されてインストールが失敗する場合は、通常、管理パックのファイルが Windows ユーザー アカウント制御によって保護されているフォルダー内にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="70155-134">If you get an error message and installation fails, that typically means that the management pack files are in a folder protected by the Windows User Account Control.</span></span> <span data-ttu-id="70155-135">この問題が発生した場合は、ファイルを別のフォルダーにコピーし、インポートとインストールのプロセスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="70155-135">If this occurs, copy the files to a different folder and then restart the import and installation process.</span></span>

8.  <span data-ttu-id="70155-136">[**管理パックの選択**] ダイアログ ボックスで、[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-136">In the **Select Management Packs** dialog box, click **Close**.</span></span> <span data-ttu-id="70155-137">インポートとインストールのプロセスには数分かかる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="70155-137">Note that the import and installation process might require several minutes to complete.</span></span>

</div>

<div>

## <a name="importing-management-packs-by-using-the-operations-manager-shell"></a><span data-ttu-id="70155-138">Operations Manager シェルを使用して管理パックをインポートする</span><span class="sxs-lookup"><span data-stu-id="70155-138">Importing Management Packs by Using the Operations Manager Shell</span></span>

<span data-ttu-id="70155-139">通常、管理パックのインポートは、Operations Manager を使用して簡単に行うことができます。ただし、エラーが発生してインポートが失敗した場合は、コンソールが適切なエラーレポートを提供するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="70155-139">In general it is easier to import the management packs by using the Operations Manager.However, if an error occurs and the import fails, the console does not always provide adequate error reports.</span></span> <span data-ttu-id="70155-140">比較では、Operations Manager Shell に詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="70155-140">By comparison, the Operations Manager Shell, provides detailed information.</span></span> <span data-ttu-id="70155-141">Operations Manager を使用していて、管理パックのインポートで問題が発生した場合は、Operations Manager Shell を使用してパックをインポートします。</span><span class="sxs-lookup"><span data-stu-id="70155-141">If you are using Operations Manager and you run into problems importing a management pack, import the pack by using the Operations Manager Shell .</span></span> <span data-ttu-id="70155-142">Operations Manager Shell には、インポートが失敗した理由を特定するのに役立つ情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="70155-142">The Operations Manager Shell provides more information that might help you determine why the import failed.</span></span>

<span data-ttu-id="70155-143">System Center Operations Manager 2007 R2 を使用している場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="70155-143">If you are using System Center Operations Manager 2007 R2, complete the following procedure:</span></span>

1.  <span data-ttu-id="70155-144">[ **スタート**] をクリックし、[ **すべてのプログラム**] をクリックし、[ **System Center Operations Manager 2007 R2**] をクリックして、[ **Operations Manager Shell**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-144">Click **Start**, click **All Programs**, click **System Center Operations Manager 2007 R2**, and then click **Operations Manager Shell**.</span></span>

2.  <span data-ttu-id="70155-145">Operations Manager シェルで、コマンドプロンプトで、Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp ファイルの実際のパスを使用して、次のコマンドを入力し、ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="70155-145">In the Operations Manager Shell, type the following command at the command prompt, using the actual path to your copy of the file Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, and then press ENTER:</span></span>
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp

3.  <span data-ttu-id="70155-146">最初の管理パックをインポートした後、Microsoft.LS.2013.Monitoring.ComponentAndUser.mp ファイルのコピーへのパスを使用して、次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="70155-146">After you import the first management pack, repeat the process using the path to your copy of the file Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:</span></span>
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ComponentAndUser.mp

4.  <span data-ttu-id="70155-147">Operations Manager シェルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="70155-147">Close the Operations Manager Shell.</span></span>

<span data-ttu-id="70155-148">System Center Operations Manager 2012 を使用している場合は、代わりに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="70155-148">If you are using System Center Operations Manager 2012, complete this procedure instead:</span></span>

1.  <span data-ttu-id="70155-149">[**スタート**]、[**すべてのプログラム**]、[**Microsoft System Center 2012**]、[**Operations Manager**] の順にクリックし、[**Operations Manager シェル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70155-149">Click **Start**, click **All Programs**, click **Microsoft System Center 2012**, click **Operations Manager**, and then click **Operations Manager Shell**.</span></span>

2.  <span data-ttu-id="70155-150">Operations Manager シェルで、コマンドプロンプトで、Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp ファイルの実際のパスを使用して、次のコマンドを入力し、ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="70155-150">In the Operations Manager Shell, type the following command at the command prompt, using the actual path to your copy of the file Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, and then press ENTER:</span></span>
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp"

3.  <span data-ttu-id="70155-151">最初の管理パックをインポートした後、Microsoft.LS.2013.Monitoring.ComponentAndUser.mp ファイルのコピーへのパスを使用して、次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="70155-151">After you have imported the first management pack, repeat the process using the path to your copy of the file Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:</span></span>
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ComponentAndUser.mp"

<span data-ttu-id="70155-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70155-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

