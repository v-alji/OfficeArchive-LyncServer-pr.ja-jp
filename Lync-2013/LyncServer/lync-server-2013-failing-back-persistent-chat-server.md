---
title: 'Lync Server 2013: 常設チャット サーバーのフェールバック'
description: 'Lync Server 2013: 常設チャットサーバーをフェイルバックします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back Persistent Chat Server
ms:assetid: 67b91de4-6ddc-43e6-9812-5e1aa84a7980
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204970(v=OCS.15)
ms:contentKeyID: 48184396
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fa36562b3892c0e22960677ffcba4b862e708c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428308"
---
# <a name="failing-back-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="c4639-103">Lync Server 2013 常設チャット サーバーのフェールバック</span><span class="sxs-lookup"><span data-stu-id="c4639-103">Failing back Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4639-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4639-104">

<span> </span></span></span>

<span data-ttu-id="c4639-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="c4639-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="c4639-106">この手順では、常設チャットサーバーの障害から回復するために必要な手順と、プライマリデータセンターからの操作を再確立するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4639-106">This procedure outlines the steps necessary to recover from a Persistent Chat Server failure, and to reestablish operations from the primary data center.</span></span>

<span data-ttu-id="c4639-107">常設チャットサーバーの障害時に、プライマリデータセンターには完全な停止が発生し、プライマリデータベースとミラーデータベースは利用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="c4639-107">During Persistent Chat Server failure, the primary data center suffers complete outage, and the primary and mirror databases become unavailable.</span></span> <span data-ttu-id="c4639-108">プライマリ データ センターはバックアップ サーバーにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="c4639-108">The primary data center fails over to the backup server.</span></span>

<span data-ttu-id="c4639-109">以下の手順では、プライマリ データ センターがバックアップされ、サーバーが再構築された後、通常の動作を回復します。</span><span class="sxs-lookup"><span data-stu-id="c4639-109">The following procedure restores normal operation after the primary data center is back up, and the servers have been rebuilt.</span></span> <span data-ttu-id="c4639-110">この手順では、プライマリデータセンターが全体の停止から回復され、トポロジビルダーを使用して行うデータベースと、使い方が再構築されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c4639-110">The procedure assumes that the primary data center has been recovered from total outage, and that the mgc database and the mgccomp database have been rebuilt and reinstalled by using Topology Builder.</span></span>

<span data-ttu-id="c4639-111">この手順では、フェイルオーバー期間中に新しいミラーサーバーとバックアップサーバーが展開されていないこと、および、展開されている唯一のサーバーが、 [Lync server 2013 での常設チャットサーバーのフェイルオーバー](lync-server-2013-failing-over-persistent-chat-server.md)によって定義されたものであることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c4639-111">The procedure also assumes that no new mirror and backup servers were deployed during the failover period, and that the only server deployed is the backup server and its mirror server, as defined in [Failing over Persistent Chat Server in Lync Server 2013](lync-server-2013-failing-over-persistent-chat-server.md).</span></span>

<span data-ttu-id="c4639-112">この手順の意図は、プライマリ サーバーからバックアップ サーバーへのフェールオーバーの原因となった障害が発生する前の状態に構成を復旧することにあります。</span><span class="sxs-lookup"><span data-stu-id="c4639-112">These steps are designed to recover configuration as it existed prior to the disaster, resulting in failover from the primary server to the backup server.</span></span>

<div>

## <a name="to-fail-back-persistent-chat-server"></a><span data-ttu-id="c4639-113">常設チャットサーバーをフェイルバックするには</span><span class="sxs-lookup"><span data-stu-id="c4639-113">To fail back Persistent Chat Server</span></span>

1.  <span data-ttu-id="c4639-114">Lync Server 管理シェルのコマンドレットを使用して、常設チャットサーバーの Active Server リストからすべてのサーバーをクリアし `Set-CsPersistentChatActiveServer` ます。</span><span class="sxs-lookup"><span data-stu-id="c4639-114">Clear all servers from the Persistent Chat Server Active Server list by using the `Set-CsPersistentChatActiveServer` cmdlet from the Lync Server Management Shell.</span></span> <span data-ttu-id="c4639-115">これにより、すべての常設チャットサーバーが、フェイルバック中に行うデータベースとデータベースに接続できなくなります。</span><span class="sxs-lookup"><span data-stu-id="c4639-115">This stops all Persistent Chat Servers from connecting to the mgc database and the mgccomp database during failback.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c4639-116">セカンダリ常設チャットサーバーのバックエンドサーバー上の SQL Server エージェントは、特権を持つアカウントで実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4639-116">The SQL Server agent on the secondary Persistent Chat Server Back End Server should be running under a privileged account.</span></span> <span data-ttu-id="c4639-117">このアカウントには、次のアクセス許可が与えられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4639-117">Specifically, the account must include:</span></span> 
    > <UL>
    > <LI>
    > <P><span data-ttu-id="c4639-118">バックアップが置かれるネットワーク共有に対する読み取りアクセス</span><span class="sxs-lookup"><span data-stu-id="c4639-118">Read access to the network share that backups are being placed in.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="c4639-119">バックアップのコピー先となるローカル ディレクトリに対する書き込みアクセス</span><span class="sxs-lookup"><span data-stu-id="c4639-119">Write access to the specific local directory that the backups are being copied to.</span></span></P></LI></UL>

    
    </div>

2.  <span data-ttu-id="c4639-120">バックアップ mgc データベースでのミラーリングを無効にします。</span><span class="sxs-lookup"><span data-stu-id="c4639-120">Disable mirroring on the backup mgc database:</span></span>
    
    1.  <span data-ttu-id="c4639-121">SQL Server Management Studio を使用して、backup 行うインスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="c4639-121">Using SQL Server Management Studio, connect to the backup mgc instance.</span></span>
    
    2.  <span data-ttu-id="c4639-122">mgc データベースを右クリックし、[**タスク**] をポイントしてから、[**ミラー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-122">Right-click the mgc database, point to **Tasks**, and then click **Mirror**.</span></span>
    
    3.  <span data-ttu-id="c4639-123">[**ミラーリングの削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-123">Click **Remove Mirroring**.</span></span>
    
    4.  <span data-ttu-id="c4639-124">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-124">Click **OK**.</span></span>
    
    5.  <span data-ttu-id="c4639-125">mgccomp データベースに対しても同じ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c4639-125">Perform the same steps with the mgccomp database.</span></span>

3.  <span data-ttu-id="c4639-126">mgc データベースをバックアップして、新しいプライマリ データベースに復元できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c4639-126">Back up the mgc database so that it can be restored to the new primary database:</span></span>
    
    1.  <span data-ttu-id="c4639-127">SQL Server Management Studio を使用して、backup 行うインスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="c4639-127">Using SQL Server Management Studio, connect to the backup mgc instance.</span></span>
    
    2.  <span data-ttu-id="c4639-p105">mgc データベースを右クリックし、[**タスク**] をポイントしてから、[**バックアップ**] をクリックします。[**データベースのバックアップ**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4639-p105">Right-click the mgc database, point to **Tasks**, and then click **Back Up**. The **Back Up Database** dialog box appears.</span></span>
    
    3.  <span data-ttu-id="c4639-130">[**バックアップの種類**] で、[**完全**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4639-130">In **Backup type**, select **Full**.</span></span>
    
    4.  <span data-ttu-id="c4639-131">[**バックアップ コンポーネント**] として、[**データベース**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-131">For **Backup component**, click **Database**.</span></span>
    
    5.  <span data-ttu-id="c4639-132">[**名前**] に表示される既定のバックアップ セット名をそのまま使用するか、バックアップ セット名として別の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4639-132">Either accept the default backup set name suggested in **Name**, or enter a different name for the backup set.</span></span>
    
    6.  <span data-ttu-id="c4639-133">*\<Optional\>* [ **説明**] にバックアップセットの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4639-133">*\<Optional\>* In **Description**, enter a description of the backup set.</span></span>
    
    7.  <span data-ttu-id="c4639-134">バックアップ先の一覧から既定のバックアップ場所を削除します。</span><span class="sxs-lookup"><span data-stu-id="c4639-134">Remove the default backup location from the destination list.</span></span>
    
    8.  <span data-ttu-id="c4639-p106">ログ配布用に設定した共有の場所へのパスを使用して、この一覧にファイルを追加します。このパスはプライマリ データベースとバックアップ データベースの両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4639-p106">Add a file to the list by using the path to the share location that you established for log shipping. This path is available to the primary database and to the backup database.</span></span>
    
    9.  <span data-ttu-id="c4639-137">[**OK**] をクリックします。ダイアログ ボックスが閉じられ、バックアップ プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c4639-137">Click **OK** to close the dialog box and begin the backup process.</span></span>

4.  <span data-ttu-id="c4639-138">上記のステップで作成されたバックアップ データベースを使用して、プライマリ データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="c4639-138">Restore the primary database by using the backup database created in the previous step.</span></span>
    
    1.  <span data-ttu-id="c4639-139">SQL Server Management Studio を使用して、プライマリ行うインスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="c4639-139">Using SQL Server Management Studio, connect to the primary mgc instance.</span></span>
    
    2.  <span data-ttu-id="c4639-p107">mgc データベースを右クリックし、[**タスク**]、[**復元**] の順にポイントしてから、[**データベース**] をクリックします。[**データベースの復元**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4639-p107">Right-click the mgc database, point to **Tasks**, point to **Restore**, and then click **Database**. The **Restore Database** dialog box appears.</span></span>
    
    3.  <span data-ttu-id="c4639-142">[**復元元デバイス**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4639-142">Select **From Device**.</span></span>
    
    4.  <span data-ttu-id="c4639-p108">[参照] ボタンをクリックします。[**バックアップの指定**] ダイアログ ボックスが表示されます。[**バックアップ メディア**] で、[**ファイル**] を選択します。[**追加**] をクリックし、ステップ 3 で作成したバックアップ ファイルを選択し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-p108">Click the browse button, which opens the **Specify Backup** dialog box. In **Backup media**, select **File**. Click **Add**, select the backup file that you created in step 3, and then click **OK**.</span></span>
    
    5.  <span data-ttu-id="c4639-146">[**復元するバックアップ セットの選択**] で、バックアップを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4639-146">In **Select the backup sets to restore**, select the backup.</span></span>
    
    6.  <span data-ttu-id="c4639-147">[**ページの選択**] ウィンドウで、[**オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4639-147">Click **Options** in the **Select a page** pane.</span></span>
    
    7.  <span data-ttu-id="c4639-148">[**復元オプション**] で、[**既存のデータベースを上書きする**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4639-148">In **Restore options**, select **Overwrite the existing database**.</span></span>
    
    8.  <span data-ttu-id="c4639-149">[**復旧状態**] で、[**データベースを使用可能な状態にする**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4639-149">In **Recovery State**, select **Leave the database ready to use**.</span></span>
    
    9.  <span data-ttu-id="c4639-150">[**OK**] をクリックします。復元プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c4639-150">Click **OK** to begin the restoration process.</span></span>

5.  <span data-ttu-id="c4639-151">プライマリデータベースの SQL Server ログの配布を構成します。</span><span class="sxs-lookup"><span data-stu-id="c4639-151">Configure SQL Server Log Shipping for the primary database.</span></span> <span data-ttu-id="c4639-152">「 [Lync server 2013 で高可用性と障害復旧のために常設チャットサーバーを構成](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) する」の手順に従って、プライマリ行うデータベースのログの配布を確立します。</span><span class="sxs-lookup"><span data-stu-id="c4639-152">Follow the procedures in [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) to establish log shipping for the primary mgc database.</span></span>

6.  <span data-ttu-id="c4639-153">常設チャットサーバーのアクティブなサーバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4639-153">Set the Persistent Chat Server active servers.</span></span> <span data-ttu-id="c4639-154">Lync Server 管理シェルで、 **CsPersistentChatActiveServer** コマンドレットを使用してアクティブなサーバーの一覧を設定します。</span><span class="sxs-lookup"><span data-stu-id="c4639-154">From the Lync Server Management Shell, use the **Set-CsPersistentChatActiveServer** cmdlet to set the list of active servers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c4639-155">すべてのアクティブ サーバーは、新しいプライマリ データベースと同じデータ センター内、またはデータベースへの接続が低待機時間/高帯域幅であるデータ センター内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4639-155">All the active servers must be located within the same data center as the new primary database, or in a data center that has a low latency/high bandwidth connection to the database.</span></span>

    
    </div>

<span data-ttu-id="c4639-156">プールを通常の状態に復元します。次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4639-156">The restore the pool to its normal state run the following Windows PowerShell command:</span></span>

    Set-CsPersistentChatState -Identity "service: lyncpc.dci.discovery.com" -PoolState Normal

<span data-ttu-id="c4639-157">詳細については、 [CsPersistentChatState](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatState) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4639-157">See the help topic for the [Set-CsPersistentChatState](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatState) cmdlet for more information.</span></span>

<span data-ttu-id="c4639-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4639-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

