---
title: 'Lync Server 2013: 常設チャット サーバーのフェールオーバー'
description: 'Lync Server 2013: 常設チャットサーバーのフェイルオーバー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over Persistent Chat Server
ms:assetid: 2cd79ffd-fee6-44ce-96cf-b98bf25e2690
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204772(v=OCS.15)
ms:contentKeyID: 48183726
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42a3a8f5df203cc23be39a4a691ad713330eab59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398474"
---
# <a name="failing-over-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="6d26d-103">Lync Server 2013 での常設チャット サーバーのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="6d26d-103">Failing over Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d26d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d26d-104">

<span> </span></span></span>

<span data-ttu-id="6d26d-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="6d26d-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="6d26d-106">常設チャットサーバーのフェールオーバーは、主に手動で行うように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6d26d-106">Failover for Persistent Chat Server is designed to be mainly a manual process.</span></span>

<span data-ttu-id="6d26d-107">フェイルオーバー手順は、セカンダリデータセンターが稼働していることを前提としていますが、プライマリ常設チャットデータベースが配置されている常設チャットサーバーサービスは、次のように完全には使用できません。</span><span class="sxs-lookup"><span data-stu-id="6d26d-107">The failover procedure is based on the assumption that the secondary data center is up and running, but the Persistent Chat Server services where the primary Persistent Chat database is located are completely unavailable, including the following:</span></span>

  - <span data-ttu-id="6d26d-108">常設チャットサーバーのプライマリデータベースと常設チャットサーバーのミラーデータベースがダウンしています。</span><span class="sxs-lookup"><span data-stu-id="6d26d-108">Persistent Chat Server primary database and Persistent Chat Server mirror database are down.</span></span>

  - <span data-ttu-id="6d26d-109">Lync Server フロントエンドサーバーがダウンしています。</span><span class="sxs-lookup"><span data-stu-id="6d26d-109">Lync Server Front End Server is down.</span></span>

<span data-ttu-id="6d26d-110">この操作は次の 2 つの基本手順に基づいています。</span><span class="sxs-lookup"><span data-stu-id="6d26d-110">The procedure is based on two basic steps:</span></span>

  - <span data-ttu-id="6d26d-111">プライマリ常設チャットデータベース (行う) を回復します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-111">Recover the primary Persistent Chat database (mgc).</span></span>

  - <span data-ttu-id="6d26d-112">新しいプライマリ データベースのミラーリングを確立する。</span><span class="sxs-lookup"><span data-stu-id="6d26d-112">Establish mirroring for the new primary database.</span></span>

<span data-ttu-id="6d26d-113">常設チャットのコンプライアンスデータベース (会社間) は、フェールオーバーされません。</span><span class="sxs-lookup"><span data-stu-id="6d26d-113">The Persistent Chat compliance database (mgccomp) is not failed over.</span></span> <span data-ttu-id="6d26d-114">このデータベースの内容は一時的なものであり、コンプライアンス アダプターがデータを処理するときに削除されます。</span><span class="sxs-lookup"><span data-stu-id="6d26d-114">The contents of this database are transient and are purged as the compliance adapter processes the data.</span></span> <span data-ttu-id="6d26d-115">データの損失を防ぐために、アダプターの出力を適切に管理することは、常設チャット管理者の責任となります。</span><span class="sxs-lookup"><span data-stu-id="6d26d-115">It is your responsibility, as Persistent Chat Administrator, to correctly manage the adapter output to avoid data loss.</span></span>

<div>

## <a name="to-fail-over-persistent-chat-server"></a><span data-ttu-id="6d26d-116">常設チャットサーバーをフェイルオーバーするには</span><span class="sxs-lookup"><span data-stu-id="6d26d-116">To fail over Persistent Chat Server</span></span>

1.  <span data-ttu-id="6d26d-117">常設チャットサーバーバックアップログ配布データベースからログ配布を削除します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-117">Remove log shipping from the Persistent Chat Server Backup Log Shipping database.</span></span>
    
    1.  <span data-ttu-id="6d26d-118">SQL Server Management Studio を使用して、常設チャットサーバーバックアップ行うデータベースが配置されているデータベースインスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-118">Using SQL Server Management Studio, connect to the database instance where the Persistent Chat Server backup mgc database is located.</span></span>
    
    2.  <span data-ttu-id="6d26d-119">マスター データベースに対するクエリ ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d26d-119">Open a query window to the master database.</span></span>
    
    3.  <span data-ttu-id="6d26d-120">次のコマンドを使用して、ログ配布を削除します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-120">Use the following command to drop log shipping:</span></span>
        
            exec sp_delete_log_shipping_secondary_database mgc

2.  <span data-ttu-id="6d26d-121">バックアップ共有から、バックアップ サーバーのコピー先フォルダーへ、コピーしていないバックアップ ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6d26d-121">Copy any uncopied backup files from the backup share to the copy destination folder of the backup server.</span></span>

3.  <span data-ttu-id="6d26d-122">セカンダリ データベースに、適用していないトランザクション ログ バックアップを順番に適用します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-122">Apply any unapplied transaction log backups in sequence to the secondary database.</span></span> <span data-ttu-id="6d26d-123">詳細については、「[方法: トランザクションログバックアップ (Transact-sql) を適用する方法」を参照してください https://go.microsoft.com/fwlink/p/?linkid=247428 。</span><span class="sxs-lookup"><span data-stu-id="6d26d-123">For details, see "How to: Apply a Transaction Log Backup (Transact-SQL)" at https://go.microsoft.com/fwlink/p/?linkid=247428.</span></span>

4.  <span data-ttu-id="6d26d-p103">バックアップ mgc データベースをオンラインにします。手順 1b. で開いたクエリ ウィンドウを使用して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-p103">Bring the backup mgc database online. Using the query window that opens in step 1b, do the following:</span></span>
    
    1.  <span data-ttu-id="6d26d-126">mgc データベースへのすべての接続を終了します (接続がある場合)。</span><span class="sxs-lookup"><span data-stu-id="6d26d-126">End all connections to the mgc database, if there are any:</span></span>
        
        1.  <span data-ttu-id="6d26d-127">行うデータベースへの接続を確認するには、 **\_ who2 sp** を実行します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-127">**exec sp\_who2** to identify connections to the mgc database.</span></span>
        
        2.  <span data-ttu-id="6d26d-128">**kill \<spid\>** を選び、これらの接続を終了します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-128">**kill \<spid\>** to end these connections.</span></span>
    
    2.  <span data-ttu-id="6d26d-129">データベースをオンラインにします。</span><span class="sxs-lookup"><span data-stu-id="6d26d-129">Bring the database online:</span></span>
        
        1.  <span data-ttu-id="6d26d-130">**restore database mgc with recovery** を実行します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-130">**restore database mgc with recovery**.</span></span>

5.  <span data-ttu-id="6d26d-131">Lync Server 管理シェルで、コマンド **セット CsPersistentChatState-Identity "service: 001.litwareinc.com" – PoolState FailedOver** を使用して、行う backup データベースにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="6d26d-131">In Lync Server Management Shell, use the command **Set-CsPersistentChatState -Identity "service:atl-cs-001.litwareinc.com" –PoolState FailedOver** to fail over to the mgc backup database.</span></span> <span data-ttu-id="6d26d-132">atl-cs-001.litwareinc.com の部分には、常設チャット プールの完全修飾ドメイン名を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-132">Be sure to substitute the fully qualified domain name of your Persistent Chat pool for atl-cs-001.litwareinc.com.</span></span>
    
    <span data-ttu-id="6d26d-133">mgc バックアップ データベースがプライマリ データベースとして動作するようになります。</span><span class="sxs-lookup"><span data-stu-id="6d26d-133">The mgc backup database now serves as the primary database.</span></span>

6.  <span data-ttu-id="6d26d-134">Lync Server 管理シェルで、 **CsMirrorDatabase** コマンドレットを使用して、プライマリデータベースとして機能するバックアップデータベースに対して高可用性ミラーを確立します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-134">In Lync Server Management Shell, use the **Install-CsMirrorDatabase** cmdlet to establish a high availability mirror for the backup database that now serves as the primary database.</span></span> <span data-ttu-id="6d26d-135">バックアップ データベース インスタンスをプライマリ データベースとして使用し、バックアップ ミラー データベース インスタンスをミラー インスタンスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-135">Use the backup database instance as the primary database and the backup mirror database instance as the mirror instance.</span></span> <span data-ttu-id="6d26d-136">これは、セットアップ時にプライマリ データベースに対して最初に構成したミラーと同じものではありません。</span><span class="sxs-lookup"><span data-stu-id="6d26d-136">This is not the same mirror as the one that was initially configured for the primary database during setup.</span></span> <span data-ttu-id="6d26d-137">詳細については、「 [lync server 2013 でのバックエンドサーバーの高可用性のための SQL ミラーリングの展開](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)」の「Lync Server 管理シェルコマンドレットの使用」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d26d-137">For details, see the section "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

7.  <span data-ttu-id="6d26d-138">常設チャットサーバーのアクティブなサーバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-138">Set the Persistent Chat Server active servers.</span></span> <span data-ttu-id="6d26d-139">Lync Server コマンドシェルで、 **CsPersistentChatActiveServer** コマンドレットを使用してアクティブなサーバーの一覧を設定します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-139">From the Lync Server Command Shell, use the **Set-CsPersistentChatActiveServer** cmdlet to set the list of active servers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="6d26d-140">すべてのアクティブ サーバーは、新しいプライマリ データベースと同じデータ センター内、またはデータベースへの接続が低待機時間/高帯域幅であるデータ センター内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d26d-140">All the active servers must be located within the same data center as the new primary database, or in a data center that has a low latency/high bandwidth connection to the database.</span></span>

    
    </div>
    
    <span data-ttu-id="6d26d-141">この時点で、常設チャットサーバーのプライマリデータベースから永続的なチャットサーバーバックアップデータベースへのフェールオーバーが正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="6d26d-141">At this point, the failover from the Persistent Chat Server primary database to the Persistent Chat Server backup database completes successfully.</span></span>

<span data-ttu-id="6d26d-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d26d-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

