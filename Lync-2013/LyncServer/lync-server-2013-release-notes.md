---
title: 'Lync Server 2013: リリース ノート'
description: Lync Server 2013 のリリースノート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Release notes
ms:assetid: 9f9e864c-3365-4800-803c-5289bd8fd363
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205120(v=OCS.15)
ms:contentKeyID: 48184930
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fabb0912d7ea3defd91014df732368eced909e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436553"
---
# <a name="release-notes-for-lync-server-2013"></a><span data-ttu-id="c12d7-103">Lync Server 2013 のリリース ノート</span><span class="sxs-lookup"><span data-stu-id="c12d7-103">Release notes for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c12d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c12d7-104">

<span> </span></span></span>

<span data-ttu-id="c12d7-105">_**最終更新日:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="c12d7-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="c12d7-106">Lync Server 2013 のリリースノートへようこそ。</span><span class="sxs-lookup"><span data-stu-id="c12d7-106">Welcome to the Lync Server 2013 Release Notes.</span></span> <span data-ttu-id="c12d7-107">Lync Server 2013 に関する既知の問題については、このファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-107">Refer to this file for information regarding known issues about Lync Server 2013.</span></span>

<div>

## <a name="about-this-document"></a><span data-ttu-id="c12d7-108">このドキュメントについて</span><span class="sxs-lookup"><span data-stu-id="c12d7-108">About this document</span></span>

<span data-ttu-id="c12d7-109">このドキュメントには、Lync Server 2013 を展開して使用する前に知っておく必要がある重要な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-109">This document contains important information that you should know before you deploy and use Lync Server 2013.</span></span> <span data-ttu-id="c12d7-110">Lync Server 2013 の詳細については、「 [Microsoft Lync server 2013](microsoft-lync-server-2013.md) のドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-110">For details about Lync Server 2013, refer to the [Microsoft Lync Server 2013](microsoft-lync-server-2013.md) documentation.</span></span>

<span data-ttu-id="c12d7-111">このドキュメントには、次のセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-111">This document contains the following sections:</span></span>

  - <span data-ttu-id="c12d7-112">Lync 2013 クライアント</span><span class="sxs-lookup"><span data-stu-id="c12d7-112">Lync 2013 client</span></span>

  - <span data-ttu-id="c12d7-113">Lync Server</span><span class="sxs-lookup"><span data-stu-id="c12d7-113">Lync Server</span></span>

  - <span data-ttu-id="c12d7-114">インストール</span><span class="sxs-lookup"><span data-stu-id="c12d7-114">Installation</span></span>

  - <span data-ttu-id="c12d7-115">モビリティ</span><span class="sxs-lookup"><span data-stu-id="c12d7-115">Mobility</span></span>

  - <span data-ttu-id="c12d7-116">会議</span><span class="sxs-lookup"><span data-stu-id="c12d7-116">Conferencing</span></span>

  - <span data-ttu-id="c12d7-117">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="c12d7-117">Enterprise Voice</span></span>

  - <span data-ttu-id="c12d7-118">プレゼンス</span><span class="sxs-lookup"><span data-stu-id="c12d7-118">Presence</span></span>

  - <span data-ttu-id="c12d7-119">応答グループ アプリケーションとコール パーク アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c12d7-119">Response Group Application and Call Park Application</span></span>

  - <span data-ttu-id="c12d7-120">Lync Server コントロール パネル、トポロジ ビルダー、および計画ツール</span><span class="sxs-lookup"><span data-stu-id="c12d7-120">Lync Server Control Panel, Topology Builder, and Planning Tool</span></span>

  - <span data-ttu-id="c12d7-121">版</span><span class="sxs-lookup"><span data-stu-id="c12d7-121">Localization</span></span>

  - <span data-ttu-id="c12d7-122">著作</span><span class="sxs-lookup"><span data-stu-id="c12d7-122">Copyright</span></span>

</div>

<span id="LyncClient"></span>

<div>

## <a name="lync-2013-client"></a><span data-ttu-id="c12d7-123">Lync 2013 クライアント</span><span class="sxs-lookup"><span data-stu-id="c12d7-123">Lync 2013 client</span></span>

<div>

## <a name="transferring-a-file-in-an-instant-message-fails-if-the-file-is-open-in-another-application"></a><span data-ttu-id="c12d7-124">他のアプリケーションでファイルを開いている場合、インスタントメッセージでファイルを転送できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-124">Transferring a file in an instant message fails if the file is open in another application</span></span>

<span data-ttu-id="c12d7-125">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-125">**Issue:**</span></span>

<span data-ttu-id="c12d7-126">別の Lync ユーザーにインスタントメッセージを追加して、Word 文書などのファイルを転送しようとすると、転送は成功したように見えますが、実際にはファイルの転送に失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-126">If you attempt to transfer a file, such as a Word document, by including it in an instant message to another Lync user, the transfer will appear to succeed but may actually fail to transfer the file.</span></span> <span data-ttu-id="c12d7-127">ファイルの種類のアイコンは Lync クライアントに表示されますが、目的の受信者がファイルを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-127">An icon for the file type will be displayed in the Lync client, but the file cannot be opened by the intended receiver.</span></span> <span data-ttu-id="c12d7-128">送信に失敗したことを通知するエラーメッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-128">No error message is displayed to inform you that the transfer was not successfull.</span></span>

<span data-ttu-id="c12d7-129">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-129">**Workaround:**</span></span>

<span data-ttu-id="c12d7-130">この問題を回避するには、インスタントメッセージでファイルを転送する前に、開いている開いているファイルまたはアプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-130">To work around this issue, close the open file or application that has it open before attempting to transfer the file in an instant message.</span></span>

</div>

</div>

<span id="LyncServer"></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="c12d7-131">Lync Server</span><span class="sxs-lookup"><span data-stu-id="c12d7-131">Lync Server</span></span>

<div>

## <a name="if-lync-server-storage-service-data-replication-fails-administrators-will-need-to-check-performance-counters-for-stale-storage-service-queue-items"></a><span data-ttu-id="c12d7-132">Lync Server ストレージサービスのデータレプリケーションに失敗した場合、管理者は、古いストレージサービスキューアイテムのパフォーマンスカウンターを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-132">If Lync Server Storage Service data replication fails, administrators will need to check performance counters for stale Storage Service queue items</span></span>

<span data-ttu-id="c12d7-133">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-133">**Issue:**</span></span>

<span data-ttu-id="c12d7-134">Lync Server ストレージサービスは、Windows Fabric を使用してレプリケーションを行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-134">The Lync Server Storage Service uses Windows Fabric for replication.</span></span> <span data-ttu-id="c12d7-135">プライマリフロントエンドサーバーでデータが削除されたが、セカンダリフロントエンドサーバーでの削除に失敗した場合 (たとえば、フロントエンドサーバーに予期しないシャットダウンまたはエラーが発生した場合)、データを残して、"切り離された" 状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-135">If data is deleted on a primary Front End Server, but the deletion on a secondary Front End Server fails—for example, if there is an unexpected shutdown or error on the Front End Server—data can be left behind and "orphaned."</span></span> <span data-ttu-id="c12d7-136">孤立したデータは、パフォーマンスが低下したり、ドライブの空き領域を浪費したりする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-136">The orphaned data can cause performance to degrade and waste drive space.</span></span>

<span data-ttu-id="c12d7-137">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-137">**Workaround:**</span></span>

<span data-ttu-id="c12d7-138">この問題を回避するには、イベント (Id = 32058) と "いいね!" のように、 \_ \_ \_ \_ \_ \_ \_ CRITICAL (id = 32059) が使用されていることがイベントログで生成される場合、管理者は、"指定した期間が \_ **古いキュー項目の数を指定** した名前で、フロントエンドサーバーのパフォーマンスカウンターを確認 **LS:LYSS - Storage Service API** してください</span><span class="sxs-lookup"><span data-stu-id="c12d7-138">To work around this issue, if the events LYSS\_DB\_SPACE\_USED\_ERROR (Id=32058) and LYSS\_DB\_SPACE\_USED\_CRITICAL (Id=32059) are generated in the event log, administrators should check the performance counter on the Front End Server under **LS:LYSS - Storage Service API** with a name of **LYSS - Current number of Storage Service stale queue items**.</span></span> <span data-ttu-id="c12d7-139">このパフォーマンスカウンターが大きい値 (たとえば、50,000 より大きい) である場合、管理者は Lync Server 2013 リソースキットで CleanuUpStorageServiceData.exe ツールを実行する必要があります。これにより、すべての孤立したデータがプールから削除されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-139">If this performance counter has a high value—for example, greater than 50,000—then the administrator should run the CleanuUpStorageServiceData.exe tool in the Lync Server 2013 Resource Kit, which will delete all orphaned data from the pool.</span></span> <span data-ttu-id="c12d7-140">このツールの詳細については、「Lync Server 2013 リソースキットドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-140">For details about the tool, see the Lync Server 2013 Resource Kit documentation.</span></span>

</div>

<div>

## <a name="whenever-the-ip-address-configuration-is-changed-for-a-server-or-pool-lync-server-services-need-to-be-restarted"></a><span data-ttu-id="c12d7-141">サーバーまたはプールの IP アドレス構成が変更されるたびに、Lync Server サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-141">Whenever the IP Address configuration is changed for a server or pool, Lync Server services need to be restarted</span></span>

<span data-ttu-id="c12d7-142">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-142">**Issue:**</span></span>

<span data-ttu-id="c12d7-143">IPv4 からデュアルスタックへの変更、またはデュアルスタックから Ipv6 への変更など、Lync Server 2013 の展開用に IP アドレス構成が変更された場合、すべてのサーバーコンポーネントは、サービスが再起動されるまで構成の変更を選択します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-143">When the IP Address configuration is changed for a Lync Server 2013 deployment, such as changing from IPv4 to Dual Stack, or from Dual Stack to Ipv6, not all server components pick up the configuration change until the services are restarted.</span></span>

<span data-ttu-id="c12d7-144">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-144">**Workaround:**</span></span>

<span data-ttu-id="c12d7-145">この問題を回避するには、展開の IP アドレス構成を変更した後で Lync Server サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-145">To work around this issue, restart Lync Server services after changing the IP Address configuration for the deployment.</span></span> <span data-ttu-id="c12d7-146">そのためには、Lync Server 管理シェルで次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-146">To do so, run the following cmdlets in the Lync Server Management Shell:</span></span>

   ```PowerShell
    Stop-CsWindowsService -graceful
   ```

   ```PowerShell
    Start-CsWindowsService
   ```

</div>

<div>

## <a name="the-dial-in-conferencing-synthetic-transaction-cmdlet-is-no-longer-available-in-the-lync-server-2013-management-pack"></a><span data-ttu-id="c12d7-147">ダイヤルイン会議の代理トランザクションコマンドレットは、Lync Server 2013 管理パックでは利用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="c12d7-147">The dial-in conferencing synthetic transaction cmdlet is no longer available in the Lync Server 2013 Management Pack</span></span>

<span data-ttu-id="c12d7-148">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-148">**Issue:**</span></span>

<span data-ttu-id="c12d7-149">ダイヤルイン会議の統合トランザクションコマンドレット **テスト** 用の会議は、Lync Server 2013 管理パックでは利用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c12d7-149">The dial-in conferencing synthetic transaction cmdlet **Test-CsDialInConferencing** is no longer available in the Lync Server 2013 Management Pack.</span></span>

<span data-ttu-id="c12d7-150">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-150">**Workaround:**</span></span>

<span data-ttu-id="c12d7-151">ダイヤルイン会議の代理トランザクションコマンドレットの使用 **テスト-Csdial In会議** は、社内でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-151">Use of the Dial-In Conferencing Synthetic Transaction cmdlet **Test-CsDialInConferencing** is supported only internally to an enterprise.</span></span>

<span data-ttu-id="c12d7-152">トラブルシューティングのために、管理者は Lync Server 管理シェルのコマンドレットを引き続き使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-152">Administrators may continue to use the cmdlet in Lync Server Management Shell for troubleshooting purposes.</span></span> <span data-ttu-id="c12d7-153">必要に応じて、社内でコマンドレットを実行するためのプライベート管理パックを開発することもできます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-153">If required, an enterprise can also develop a private management pack to run the cmdlet internally.</span></span>

</div>

<div>

## <a name="the-centralized-logging-service-stops-if-network-traffic-is-disrupted-when-log-files-are-being-copied-to-network-share"></a><span data-ttu-id="c12d7-154">ログファイルがネットワーク共有にコピーされているときに、ネットワークトラフィックが中断されると、一元管理サービスは停止します</span><span class="sxs-lookup"><span data-stu-id="c12d7-154">The Centralized Logging Service stops if network traffic is disrupted when log files are being copied to network share</span></span>

<span data-ttu-id="c12d7-155">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-155">**Issue:**</span></span>

<span data-ttu-id="c12d7-156">中央集中ログサービスがネットワークパスを使用するよう **に構成さ** れている場合 (CacheFileNetworkFolder パラメーターの値は有効な UNC パスです)、キャッシュされたログファイルはネットワーク共有にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-156">When the Centralized Logging Service is configured to use a network path (the value of the CacheFileNetworkFolder parameter of the **Get-CsClsConfiguration** cmdlet is a valid UNC path), cached log files are copied to the network share.</span></span> <span data-ttu-id="c12d7-157">ファイルのコピー中にネットワークトラフィックが中断する場合は、集中化されたログサービスが停止する例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-157">If there is a disruption in network traffic while the files are being copied, an exception will occur that will cause the centralized logging service to stop.</span></span>

<span data-ttu-id="c12d7-158">サービスが最大3回自動的に再起動するように構成されているため、サービスは最初の3つの例外から回復します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-158">The service is configured to automatically restart up to three times, so the service will recover from the first three exceptions.</span></span>

<span data-ttu-id="c12d7-159">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-159">**Workaround:**</span></span>

<span data-ttu-id="c12d7-160">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-160">There is no workaround for this issue.</span></span> <span data-ttu-id="c12d7-161">問題を特定するには、"Lync Server 集中ログサービスエージェント" サービスが予期せず終了したときにログに記録する "サービスコントロールマネージャー" からイベント7031ログを監視します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-161">To identify the issue, monitor the event log for Event ID 7031 from the "Service Control Manager" that logs when the "Lync Server Centralized Logging Service Agent" service has terminated unexpectedly.</span></span> <span data-ttu-id="c12d7-162">この問題が3回以上発生する場合は、 **Start-CsWindowService** コマンドレットを使用してサービスを手動で再開します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-162">If this happens more than three times, manually restart the service by using the **Start-CsWindowService** cmdlet.</span></span>

</div>

<div>

## <a name="storage-service-queue-items-need-to-be-imported-manually"></a><span data-ttu-id="c12d7-163">ストレージサービスキューアイテムを手動でインポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="c12d7-163">Storage Service Queue Items need to be imported manually</span></span>

<span data-ttu-id="c12d7-164">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-164">**Issue:**</span></span>

<span data-ttu-id="c12d7-165">Lync Server 2013 は、アーカイブされたメッセージや通話の詳細記録 (CDR) など、各フロントエンドサーバー上のデータベース上の会議とインスタントメッセージに関するデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-165">Lync Server 2013 stores data about conferencing and instant messaging, such as archived messages and call detail recording (CDR), on a database on each Front End Server.</span></span> <span data-ttu-id="c12d7-166">指定された宛先に配信される前に、データはデータベースに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-166">The data is stored in the database while it is being processed before being delivered to the intended destination.</span></span> <span data-ttu-id="c12d7-167">Lync Server 2013 は、パフォーマンスを向上させるために、長期間に処理されていないローカルデータベースのキューアイテムを定期的にエクスポートし、ファイルストアに保存します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-167">To improve performance, Lync Server 2013 periodically exports the queue items from the local database that are not processed for an extended period of time, and saves them on the file store.</span></span> <span data-ttu-id="c12d7-168">ファイルストアを使用できない場合は、各フロントエンドサーバーにアイテムが格納されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-168">If the file store is unavailable, the items are stored on each Front End Server.</span></span> <span data-ttu-id="c12d7-169">プールのフェールオーバー中にデータが失われないように、同じ操作が発生します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-169">The same operation occurs to prevent data loss during pool failover.</span></span>

<span data-ttu-id="c12d7-170">エクスポート操作の実行中、Lync Server ストレージサービスは、イベント 32075 Id (完全なフラッシュ操作が開始された状態)、32076 (完全なフラッシュが完了)、32082 (メンテナンスレベルのフラッシュの開始)、32083 (メンテナンスレベルのフラッシュの完了)、32089 (データベースの充填によるフラッシュ発生) の各ステージを記録します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-170">During the export operation, the Lync Server Storage Service records every stage in the event log with event IDs of 32075 (full flush operation is started), 32076 (full flush is completed), 32082 (maintenance level flush is started), 32083 (maintenance level flush is completed), 32089 (flush occurred due to filling up of database).</span></span> <span data-ttu-id="c12d7-171">このデータは、処理されて最終的な送信先 (SQL Server または Exchange Server) に配信されるように、システムに自動的にインポートされることはありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-171">This data will not automatically be imported back to the system to be processed and delivered to its final destination (SQL Server or Exchange Server).</span></span>

<span data-ttu-id="c12d7-172">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-172">**Workaround:**</span></span>

<span data-ttu-id="c12d7-173">システムにデータをインポートするには、管理者は Lync Server リソースキットの ImportStorageServiceData ツールを使用する必要があります。これにより、システムにデータが追加され、最終的な送信先に配信されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-173">To import the data to the system, administrators will need to use the ImportStorageServiceData tool in the Lync Server Resource Kit, which will add the data back into the system to be processed and delivered to its final destination.</span></span>

</div>

<div>

## <a name="address-book-web-query-searches-will-fail-if-the-default-value-for-usenormalizationrules-is-changed-to-false"></a><span data-ttu-id="c12d7-174">UseNormalizationRules の既定値が False に変更されている場合、アドレス帳の Web クエリの検索は失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-174">Address Book Web Query searches will fail if the default value for UseNormalizationRules is changed to False</span></span>

<span data-ttu-id="c12d7-175">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-175">**Issue:**</span></span>

<span data-ttu-id="c12d7-176">UseNormalizationRules の既定値が False に変更されると、アドレス帳の Web クエリの検索は失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-176">If the default value for UseNormalizationRules is changed to False, Address Book Web Query searches will fail.</span></span> <span data-ttu-id="c12d7-177">既定値が変更されると、Lync クライアントユーザーは Lync アドレス帳の web クエリを使ってユーザーを検索することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-177">After the default value is changed, Lync Client users will not be able to use Lync Address Book web query to search for users.</span></span>

<span data-ttu-id="c12d7-178">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-178">**Workaround:**</span></span>

<span data-ttu-id="c12d7-179">UseNormalizationRules の既定値が False に設定されている場合に、ユーザーが Lync Server 2013 で定義されている電話番号を使用できるようにするには、次の操作を行ってこの問題を回避します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-179">If the default value for UseNormalizationRules is set to False so that users can use phone numbers as defined in Active Directory Domain Services without Lync Server 2013 applying normalization rules, work around this issue by doing the following:</span></span>

1.  <span data-ttu-id="c12d7-180">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-180">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="c12d7-181">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-181">Do one of the following:</span></span>
    
      - <span data-ttu-id="c12d7-182">展開に Lync Server 2013 サーバーしか含まれていない場合は、次のコマンドレットをグローバルレベルで実行して、UseNormalizationRules と IgnoreGenericRules の値を True に変更します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-182">If your deployment includes only Lync Server 2013 servers, run the following cmdlet at the global level to change the values for UseNormalizationRules and IgnoreGenericRules to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="c12d7-183">展開に Lync Server 2013 および Lync Server 2010 または Office Communications Server 2007 R2 の組み合わせが含まれている場合は、次のコマンドレットを実行して、トポロジの各 Lync Server 2013 プールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-183">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            new-csAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="c12d7-184">CMS のレプリケーションがすべてのプールで行われるのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-184">Wait for CMS replication to occur on all pools.</span></span>

4.  <span data-ttu-id="c12d7-185">展開の電話の正規化規則ファイルを変更して、コンテンツをクリアします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-185">Modify the phone normalization rules file for your deployment to clear the content.</span></span> <span data-ttu-id="c12d7-186">ファイルは、各 Lync Server 2013 プールのファイル共有にあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-186">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="c12d7-187">ファイルが表示されていない場合は、"会社電話番号の正規化Rules.txt" という名前の空のファイルを作成し \_ \_ \_ \_ ます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-187">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt."</span></span>

5.  <span data-ttu-id="c12d7-188">すべてのフロントエンドプールが新しいファイルを読み取るまで数分待ちます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-188">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="c12d7-189">展開の各 Lync Server 2013 プールで次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-189">Run the following cmdlet on each Lync Server 2013 pool in your deployment.</span></span>
    
        Update-csAddressBook

</div>

<div>

## <a name="address-book-server-error-event-21054-is-generated-once-daily-for-each-lync-2013-pool"></a><span data-ttu-id="c12d7-190">アドレス帳サーバーエラーイベント21054が Lync 2013 プールごとに1回生成される</span><span class="sxs-lookup"><span data-stu-id="c12d7-190">Address Book Server error event 21054 is generated once daily for each Lync 2013 pool</span></span>

<span data-ttu-id="c12d7-191">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-191">**Issue:**</span></span>

<span data-ttu-id="c12d7-192">Lync Server 2013 アドレス帳サーバーでは、毎日のメンテナンス実行時に、毎日1回エラーイベント21054が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-192">Lync Server 2013 Address Book Server will generate error event 21054 once every day when performing daily maintenance.</span></span> <span data-ttu-id="c12d7-193">また、更新が成功した場合でも、管理者が **csAddressBook** コマンドレットを実行するたびにエラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-193">The error is also generated every time an administrator runs the **Update-csAddressBook** cmdlet, even when the update is successful.</span></span> <span data-ttu-id="c12d7-194">ただし、更新が成功した場合は、このエラーイベントを無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-194">However, this error event can safely be ignored when the update is successful.</span></span>

<span data-ttu-id="c12d7-195">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-195">**Workaround:**</span></span>

<span data-ttu-id="c12d7-196">このエラーイベントが発生した場合は、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-196">When you encounter this error event, run the following cmdlet:</span></span>

    Debug-csAddressBookReplication -Poolfqdn <Pool FQDN for which the event was generated>

<span data-ttu-id="c12d7-197">コマンドレットで、インデックスを作成しない、または破棄されたオブジェクトがないと報告された場合、エラーイベント21054は安全に無視できます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-197">If the cmdlet reports that there are no unindexed or abandoned objects, the error event 21054 can be safely ignored.</span></span>

<span data-ttu-id="c12d7-198">さらに、System Center Operations Manager では、キー正常性インジケータ (KHI) のアドレス帳のユーザーが正しくインデックス処理されていることを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-198">Additionally, the Key Health Indicator (KHI) "Address Book Users Correctly Indexed" should be turned off in System Center Operations Manager.</span></span>

</div>

<div>

## <a name="requests-may-fail-when-ipv6-is-configured-on-an-edge-pool"></a><span data-ttu-id="c12d7-199">エッジプールで IPv6 が構成されていると、要求が失敗することがある</span><span class="sxs-lookup"><span data-stu-id="c12d7-199">Requests may fail when IPv6 is configured on an Edge pool</span></span>

<span data-ttu-id="c12d7-200">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-200">**Issue:**</span></span>

<span data-ttu-id="c12d7-201">エッジプールで IPv6 が構成されている場合、エッジプールへの要求が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-201">When IPv6 is configured on an Edge pool, some requests to the Edge pool may fail.</span></span>

<span data-ttu-id="c12d7-202">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-202">**Workaround:**</span></span>

<span data-ttu-id="c12d7-203">この問題を回避するには、IPv6 でエッジプールを構成しないでください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-203">To work around this issue, do not configure an Edge pool with IPv6.</span></span>

</div>

<div>

## <a name="the-invoke-cspoolfailback-cmdlet-may-fail-during-pool-failback"></a><span data-ttu-id="c12d7-204">プールのフェイルバック中に csPoolFailback コマンドレットが失敗することがある</span><span class="sxs-lookup"><span data-stu-id="c12d7-204">The invoke-csPoolFailback cmdlet may fail during pool failback</span></span>

<span data-ttu-id="c12d7-205">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-205">**Issue:**</span></span>

<span data-ttu-id="c12d7-206">プールをフェイルバックしようとすると、 **csPoolFailback** コマンドレットが失敗することがあります。「再試行後に hydration プロセスを完了できませんでした」というエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-206">When attempting to fail back a pool, the **invoke-csPoolFailback** cmdlet may fail with the error, "Failed to complete hydration process after repeated attempts."</span></span>

<span data-ttu-id="c12d7-207">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-207">**Workaround:**</span></span>

<span data-ttu-id="c12d7-208">この問題を回避するには、もう一度コマンドレットを実行し、コマンドレットが正常に完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-208">To work around this issue, run the cmdlet again, and wait until the cmdlet succeeds.</span></span> <span data-ttu-id="c12d7-209">フェイルバックプロセスが完了するまで数分かかる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-209">Note that the failback process can take several minutes to complete.</span></span> <span data-ttu-id="c12d7-210">2万ユーザーがいるプールの場合、最大60分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-210">It may take up to 60 minutes for a pool with 20,000 users.</span></span>

</div>

<div>

## <a name="data-loss-may-occur-when-you-add-a-front-end-server-to-an-already-established-pool--hybrid-skype-for-business-online"></a><span data-ttu-id="c12d7-211">フロントエンドサーバーを既に確立されているプール (ハイブリッド、Skype for Business Online) に追加すると、データが失われることがある</span><span class="sxs-lookup"><span data-stu-id="c12d7-211">Data loss may occur when you add a Front End Server to an already established pool – Hybrid, Skype for Business Online</span></span>

<span data-ttu-id="c12d7-212">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-212">**Issue:**</span></span>

<span data-ttu-id="c12d7-213">この問題は、プールに複数のフロントエンドサーバーがある環境で、フロントエンドサーバーの1つを再起動するか、またはプールの一部ではない新しいフロントエンドサーバーを追加することによって発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-213">You may encounter this issue in an environment where a pool has more than one Front End Server, and you either restart one of the Front End Servers, or add a new Front End Server that was not previously part of the pool.</span></span>

<span data-ttu-id="c12d7-214">データがアーカイブされているユーザーは、プールのデータアーカイブの安定した分布が確立されるまで、データの損失が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-214">Users whose data is being archived may experience data loss until a stable distribution of data archiving is established for the pool.</span></span> <span data-ttu-id="c12d7-215">このデータ損失の可能性がある期間は、人同士の会話で15分に制限され、会議に30分の通話が可能です。</span><span class="sxs-lookup"><span data-stu-id="c12d7-215">This period of potential data loss is limited to 15 minutes for person-to-person conversations, and 30 minutes for conferences.</span></span>

<span data-ttu-id="c12d7-216">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-216">**Workaround:**</span></span>

<span data-ttu-id="c12d7-217">プール内のフロントエンドサーバーを1つずつ開始する代わりに、管理を実行する場合は、プールを別のプールにフェールオーバーして、サーバーの保守タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-217">When you perform maintenance, instead of starting Front End Servers in the pool one by one, you should fail over the pool to another pool, and then perform maintenance tasks on the servers.</span></span> <span data-ttu-id="c12d7-218">メンテナンスタスクを実行する前にサービスを利用できないようにすることもできます。メンテナンスが完了したら、空き時間情報を復元することもできます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-218">You can also make the service unavailable before performing maintenance tasks, and then restore availability when maintenance is complete.</span></span>

</div>

<div>

## <a name="administrators-cannot-get-licensee-count-by-using-the-get-csclientaccesslicense-cmdlet"></a><span data-ttu-id="c12d7-219">管理者が Get-CsClientAccessLicense コマンドレットを使用してライセンス数を取得できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-219">Administrators cannot get licensee count by using the Get-CsClientAccessLicense cmdlet</span></span>

<span data-ttu-id="c12d7-220">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-220">**Issue:**</span></span>

<span data-ttu-id="c12d7-221">管理者は、 **CsClientAccessLicense** コマンドレットを使用して、クライアントライセンスの正確な使用状況を取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-221">Administrators cannot get accurate client license usage by using the **Get-CsClientAccessLicense** cmdlet.</span></span>

<span data-ttu-id="c12d7-222">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-222">**Workaround:**</span></span>

<span data-ttu-id="c12d7-223">サーバーのライセンスの種類を確認するには、ユーザーの **取得サービス** コマンドレットを実行して、すべてのデータベースの完全修飾ドメイン名 (FDQNs) を取得します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-223">To check the server license type, you can run the **Get-CsService** cmdlet to retrieve the fully qualified domain names (FDQNs) of all databases.</span></span> <span data-ttu-id="c12d7-224">フロントエンドサーバーの FQDN がバックエンドデータベースの FQDN と同じである場合、ライセンスは標準エディションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="c12d7-224">If the FQDN of the Front End Server is the same as the FQDN of the back-end database, the license is a Standard edition license.</span></span> <span data-ttu-id="c12d7-225">それ以外の場合は、ライセンスは Enterprise edition ライセンスです。</span><span class="sxs-lookup"><span data-stu-id="c12d7-225">Otherwise, the license is an Enterprise edition license.</span></span>

</div>

<div>

## <a name="client-licensee-count-is-not-accurately-reported"></a><span data-ttu-id="c12d7-226">クライアントのライセンス数が正確に報告されていない</span><span class="sxs-lookup"><span data-stu-id="c12d7-226">Client licensee count is not accurately reported</span></span>

<span data-ttu-id="c12d7-227">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-227">**Issue:**</span></span>

<span data-ttu-id="c12d7-228">クライアントのライセンス数を確認するときに、次のような状況が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-228">When determining client license counts, you may experience the following conditions:</span></span>

1.  <span data-ttu-id="c12d7-229">**モバイルユーザーのライセンス数が正しくない**</span><span class="sxs-lookup"><span data-stu-id="c12d7-229">**Inaccurate license count for mobile users**</span></span>
    
    <span data-ttu-id="c12d7-230">ライセンス数は、デバイスベースのユーザーの一意の IP アドレスの数に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-230">The license count is based on the number of unique IP addresses for device-based users.</span></span> <span data-ttu-id="c12d7-231">ライセンス数は、次のように制限されています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-231">The license count will be limited in the following ways:</span></span>
    
      - <span data-ttu-id="c12d7-232">ユーザーの IP アドレスが Lync セッション中に変更されると、ライセンスは過大にカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-232">Licenses will be overcounted if the IP address for the user changes during Lync sessions.</span></span> <span data-ttu-id="c12d7-233">この問題は、ユーザーがデスクトップクライアントで複数の場所から Lync Server に接続したときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-233">This can occur when a user connects to Lync Server from more than one location with a desktop client.</span></span>
    
      - <span data-ttu-id="c12d7-234">ユーザーがモバイルクライアントに接続すると、デバイスの IP アドレスを確認できないため、ライセンスはカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-234">Licenses will be undercounted if a user connects with a mobile client, because the IP address for the device cannot be determined.</span></span>

2.  <span data-ttu-id="c12d7-235">**ライセンスは、公衆交換電話網 (PSTN) 通話、Lync クライアント、PSTN 回線への Lync クライアント通話、PSTN 回線に転送された Lync 通話に対して2回カウントされます。**</span><span class="sxs-lookup"><span data-stu-id="c12d7-235">**Licenses are counted twice for public switched telephone network (PSTN) calls to Lync client, Lync client calls to PSTN lines, and Lync calls forwarded to PSTN lines**</span></span>
    
    <span data-ttu-id="c12d7-236">次のシナリオでは、電話番号と Lync ユーザーの両方がカウントされ、使用されているライセンス数が判断されるため、2つの追加ライセンスは1つではなくカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-236">In the following scenarios, two additional licenses will be counted instead of one because both the phone number and the Lync user are counted to determine the number of licenses used.</span></span> <span data-ttu-id="c12d7-237">正確なライセンスデータを取得するには、電話番号によって生成されたライセンスを手動で削除します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-237">To obtain accurate licensing data, manually remove the licenses generated by a phone number.</span></span>
    
      - <span data-ttu-id="c12d7-238">Lync への PSTN 電話通話</span><span class="sxs-lookup"><span data-stu-id="c12d7-238">A PSTN phone call to Lync</span></span>
    
      - <span data-ttu-id="c12d7-239">PSTN 回線への Lync 通話</span><span class="sxs-lookup"><span data-stu-id="c12d7-239">A Lync call to a PSTN line</span></span>
    
      - <span data-ttu-id="c12d7-240">Lync への PSTN 通話。その後、Lync が着信を PSTN 回線に転送します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-240">A PSTN call to Lync, and then Lync forwards the call to a PSTN line.</span></span> <span data-ttu-id="c12d7-241">いずれかの PSTN 線がカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-241">One of the PSTN lines will be counted.</span></span>

3.  <span data-ttu-id="c12d7-242">**ログオンしている Lync 携帯電話のライセンスはカウントされません**</span><span class="sxs-lookup"><span data-stu-id="c12d7-242">**A license will not be counted for a logged-on Lync phone**</span></span>
    
    <span data-ttu-id="c12d7-243">ユーザーが Lync 認定電話を使用している場合、電話のログイン後も接続されたままで、ログイン状態が維持されている場合は、ライセンスの照会が電話のログイン後に行われると、電話はライセンスを使用しているものとしてカウントされません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-243">When a user uses a Lync-certified phone, if the phone logs in and stays connected, which retains its logon status, the phone will not be counted as using a license if the query for licenses occurs after the phone logged in.</span></span>

4.  <span data-ttu-id="c12d7-244">**電話会議に参加している PSTN 電話にカウントされたライセンス**</span><span class="sxs-lookup"><span data-stu-id="c12d7-244">**Licenses counted for PSTN phones joining conferences**</span></span>
    
    <span data-ttu-id="c12d7-245">ユーザーが PSTN 電話を使って会議に参加すると、会議に参加するためのライセンスが誤ってカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-245">When a user joins a conference with a PSTN phone, a license will inaccurately be counted for joining the conference.</span></span> <span data-ttu-id="c12d7-246">ただし、PSTN 電話を使って会議に参加する場合はライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-246">However, no license is needed to join a conference with a PSTN phone.</span></span>

<span data-ttu-id="c12d7-247">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-247">**Workaround:**</span></span>

1.  <span data-ttu-id="c12d7-248">**モバイルユーザーのライセンス数が正しくない**</span><span class="sxs-lookup"><span data-stu-id="c12d7-248">**Inaccurate license count for mobile users**</span></span>
    
      - <span data-ttu-id="c12d7-249">同じデバイスに属している IP アドレスを手動で特定して、ライセンス数のいずれかを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-249">You can manually identify the IP addresses that belong to the same device and then remove one of them in the license count.</span></span>
    
      - <span data-ttu-id="c12d7-250">この問題の回避策は、Lync クライアントで接続しているモバイルデバイスには対応していません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-250">There is no workaround for this issue with mobile devices connecting with Lync client.</span></span>

2.  <span data-ttu-id="c12d7-251">**ライセンスは、Lync クライアントへの PSTN 通話、PSTN 回線への Lync クライアント通話、PSTN 回線への lync 通話の転送について2回カウントされます。**</span><span class="sxs-lookup"><span data-stu-id="c12d7-251">**Licenses are counted twice for PSTN calls to Lync client, Lync client calls to PSTN lines, and Lync calls forwarded to PSTN lines**</span></span>
    
    <span data-ttu-id="c12d7-252">PSTN 電話番号を手動で特定し、生成されたライセンス数を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-252">You will need to manually identify the PSTN phone number and remove the license count generated for it.</span></span>

3.  <span data-ttu-id="c12d7-253">**ログインしている Lync 携帯電話のライセンスはカウントされません**</span><span class="sxs-lookup"><span data-stu-id="c12d7-253">**A license will not be counted for a logged-in Lync phone**</span></span>
    
    <span data-ttu-id="c12d7-254">Lync 携帯電話を設定して、ログオフした後、3ヶ月ごとに定期的にログオンすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-254">You can configure the Lync phone to log off, and then log on again, at a regular interval, such as every 3 months.</span></span>

4.  <span data-ttu-id="c12d7-255">**電話会議に参加している PSTN 電話にカウントされたライセンス**</span><span class="sxs-lookup"><span data-stu-id="c12d7-255">**Licenses counted for PSTN phones joining conferences**</span></span>
    
    <span data-ttu-id="c12d7-256">電話会議に参加するために使用される PSTN 電話番号を手動で特定して、電話番号によって生成されたライセンスを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-256">You can manually identify the PSTN phone number that is used to join the conference and remove the license generated by the phone number.</span></span>

</div>

<div>

## <a name="the-lync-server-control-panel-stops-working-in-a-vmware-environment-after-upgrading-to-silverlight-5"></a><span data-ttu-id="c12d7-257">Silverlight 5 にアップグレードした後、Lync Server コントロールパネルが VMware 環境で動作しなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-257">The Lync Server Control Panel stops working in a VMware environment after upgrading to Silverlight 5</span></span>

<span data-ttu-id="c12d7-258">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-258">**Issue:**</span></span>

<span data-ttu-id="c12d7-259">VMware 環境で Lync Server コントロールパネルを使用すると、Microsoft Silverlight をバージョン5にアップグレードした後に Lync Server コントロールパネルが機能しなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-259">If you use the Lync Server Control Panel in a VMware environment, the Lync Server Control Panel may stop working after you upgrade Microsoft Silverlight to version 5.</span></span>

<span data-ttu-id="c12d7-260">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-260">**Workaround:**</span></span>

<span data-ttu-id="c12d7-261">この問題を回避するには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-261">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="c12d7-262">Silverlight 5 をアンインストールし、から Silverlight 4 をインストール [https://go.microsoft.com/fwlink/p/?LinkID=149156](https://go.microsoft.com/fwlink/p/?linkid=149156) します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-262">Uninstall Silverlight 5, and install Silverlight 4 from [https://go.microsoft.com/fwlink/p/?LinkID=149156](https://go.microsoft.com/fwlink/p/?linkid=149156).</span></span>

  - <span data-ttu-id="c12d7-263">Lync Server コントロールパネルに、VMware 仮想コンピューターではないコンピューターからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-263">Access the Lync Server Control Panel from a computer that is not a VMware virtual computer.</span></span>
    
    <span data-ttu-id="c12d7-264">Lync server の管理ツールがコンピューターにインストールされている場合は、サーバーの Windows の [ **スタート** ] メニューから Lync Server コントロールパネルを起動することができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-264">To do so, you can start the Lync Server Control Panel from the Windows **Start** menu on the server, if the Lync Server Administration tools are installed on the computer.</span></span>
    
    <span data-ttu-id="c12d7-265">Lync Server コントロールパネルには、web ブラウザーを使用してアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-265">You can also access the Lync Server Control Panel by using a web browser.</span></span> <span data-ttu-id="c12d7-266">URL は https:///cscp. に似ています。 \<frontend\_pool\_fqdn\></span><span class="sxs-lookup"><span data-stu-id="c12d7-266">The URL will be similar to https://\<frontend\_pool\_fqdn\>/cscp.</span></span>

</div>

<div>

## <a name="user-information-in-the-address-book-service-is-not-updated-after-the-distinguished-name-for-the-user-is-modified-in-active-directory"></a><span data-ttu-id="c12d7-267">ユーザーの識別名が Active Directory で変更された後、アドレス帳サービスのユーザー情報が更新されない</span><span class="sxs-lookup"><span data-stu-id="c12d7-267">User information in the Address Book Service is not updated after the distinguished name for the user is modified in Active Directory</span></span>

<span data-ttu-id="c12d7-268">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-268">**Issue:**</span></span>

<span data-ttu-id="c12d7-269">Active Directory ドメインサービスでユーザーの識別名 (DN とも呼ばれます) が変更された場合、アドレス帳サービス (ABS) では、追加の変更は更新されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-269">If a user’s distinguished name (also known as DN) is changed in Active Directory Domain Services, any additional changes will not be updated in the Address Book Service (ABS).</span></span> <span data-ttu-id="c12d7-270">この操作を行っても、ユーザーのサインインやプレゼンスには影響はありませんが、SIP アドレスが変更された場合、ユーザーは、古い SIP アドレスを返します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-270">This does not affect sign-in or presence for the user, but it will prevent communication for the user if the SIP address is also changed, because searches will return an outdated SIP address.</span></span>

<span data-ttu-id="c12d7-271">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-271">**Workaround:**</span></span>

<span data-ttu-id="c12d7-272">この問題を回避するには、ユーザーの DN を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-272">To work around this issue, do not change a user’s DN.</span></span> <span data-ttu-id="c12d7-273">ユーザーの DN を以前の値に戻した場合、更新はアドレス帳サービスに反映されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-273">If you revert the DN for the user to the previous value, updates will be reflected in the Address Book Service.</span></span>

</div>

</div>

<span id="Installation"></span>

<div>

## <a name="installation"></a><span data-ttu-id="c12d7-274">インストール</span><span class="sxs-lookup"><span data-stu-id="c12d7-274">Installation</span></span>

<div>

## <a name="using-non-ascii-characters-may-result-in-lync-server-failing-to-start"></a><span data-ttu-id="c12d7-275">ASCII 以外の文字を使用すると、Lync server が起動しない場合がある</span><span class="sxs-lookup"><span data-stu-id="c12d7-275">Using non-ASCII characters may result in Lync server failing to start</span></span>

<span data-ttu-id="c12d7-276">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-276">**Issue:**</span></span>

<span data-ttu-id="c12d7-277">エクスポート先のフォルダー名に ASCII 以外の文字 (UNICODE、2バイト文字セット (DBCS)、UTF-8、UTF-16 など) が含まれている場合、セットアップは失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-277">Setup will fail if the destination folder name includes non-ASCII characters (including UNICODE, double-byte character set (DBCS), UTF-8, and UTF-16).</span></span> <span data-ttu-id="c12d7-278">また、セットアップは成功しますが、ASCII 以外の文字が次のいずれかに含まれている場合は、サーバーが起動しません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-278">In addition, Setup may succeed but the server will not start if non-ASCII characters are contained in any of the following:</span></span>

  - <span data-ttu-id="c12d7-279">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="c12d7-279">Computer name</span></span>

  - <span data-ttu-id="c12d7-280">ドメイン名</span><span class="sxs-lookup"><span data-stu-id="c12d7-280">Domain name</span></span>

  - <span data-ttu-id="c12d7-281">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="c12d7-281">User name</span></span>

  - <span data-ttu-id="c12d7-282">ユーザー SIP URI</span><span class="sxs-lookup"><span data-stu-id="c12d7-282">User SIP URI</span></span>

  - <span data-ttu-id="c12d7-283">サービスアカウント名</span><span class="sxs-lookup"><span data-stu-id="c12d7-283">Service account name</span></span>

<span data-ttu-id="c12d7-284">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-284">**Workaround:**</span></span>

<span data-ttu-id="c12d7-285">目的のフォルダー名、コンピューター名、ドメイン名、ユーザー名、ユーザー SIP URI、およびサービスアカウント名には ASCII 文字のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-285">Use only ASCII characters in the destination folder name, computer name, domain name, user name, user SIP URI, and service account names.</span></span>

</div>

<div>

## <a name="the-hotfix-for-heap-corruption-occurs-when-a-module-calls-the-insertentitybody-method-in-iis-75-must-be-installed-prior-to-installing-lync-server-2013"></a><span data-ttu-id="c12d7-286">"ヒープの破損" の修正プログラムは、Lync Server 2013 をインストールする前に、モジュールが IIS 7.5 の InsertEntityBody メソッドをインストールする必要がある場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-286">The hotfix for "Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5" must be installed prior to installing Lync Server 2013</span></span>

<span data-ttu-id="c12d7-287">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-287">**Issue:**</span></span>

<span data-ttu-id="c12d7-288">"ヒープの破損" の修正プログラムは、「モジュールが IIS 7.5 で InsertEntityBody メソッドを呼び出すときに発生し [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602) ます。」 (264886) は、 [https://go.microsoft.com/fwlink/p/?LinkId=268603](https://go.microsoft.com/fwlink/p/?linkid=268603) Lync Server 2013 をインストールする前にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-288">The hotfix for "Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5" ([https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602)), described in Microsoft Knowledge Base article 264886 ([https://go.microsoft.com/fwlink/p/?LinkId=268603](https://go.microsoft.com/fwlink/p/?linkid=268603)), must be installed prior to installing Lync Server 2013.</span></span>

<span data-ttu-id="c12d7-289">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-289">**Workaround:**</span></span>

<span data-ttu-id="c12d7-290">Microsoft ダウンロードセンターから修正プログラムをダウンロードしてインストールし [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602) ます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-290">Download and install the hotfix from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602).</span></span>

</div>

<div>

## <a name="lync-server-2013-fails-to-install-on-ita-windows-server-2012-os-rtm-version"></a><span data-ttu-id="c12d7-291">Lync Server 2013 が ITA Windows Server 2012 OS RTM バージョンでインストールできない</span><span class="sxs-lookup"><span data-stu-id="c12d7-291">Lync Server 2013 fails to install on ITA Windows Server 2012 OS RTM version</span></span>

<span data-ttu-id="c12d7-292">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-292">**Issue:**</span></span>

<span data-ttu-id="c12d7-293">Windows Fabric のインストールに失敗したため、ITA Windows Server 2012 で Lync Server 2013 のインストールが失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-293">Lync Server 2013 installation fails on ITA Windows Server 2012 due to Windows Fabric installation failing.</span></span>

<span data-ttu-id="c12d7-294">ファブリックトレースは、HH: MM: SS という時刻形式で作成されるため、Windows ファブリックインストールが失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-294">Windows Fabric installation fails because fabric traces are created with the time format of HH:MM:SS.</span></span> <span data-ttu-id="c12d7-295">ただし、ITA Windows Server では、時刻の形式は HH です。MM.SS。</span><span class="sxs-lookup"><span data-stu-id="c12d7-295">However, in ITA Windows Server, the time format is HH.MM.SS.</span></span>

<span data-ttu-id="c12d7-296">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-296">**Workaround:**</span></span>

<span data-ttu-id="c12d7-297">この問題を回避するには、Lync Server 2013 をインストールする前にシステムレジストリを更新します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-297">To work around this issue, update the system registry before installing Lync Server 2013.</span></span> <span data-ttu-id="c12d7-298">更新する必要があるレジストリキーは、HKEY \_ ユーザーです \\ 。既定 \\ のコントロールパネル \\ 国際 \\ 形式の書式。</span><span class="sxs-lookup"><span data-stu-id="c12d7-298">The registry key that needs to be updated is: HKEY\_USERS\\.DEFAULT\\Control Panel\\International\\sTimeFormat.</span></span> <span data-ttu-id="c12d7-299">次のように Windows PowerShell コマンドラインインターフェイスを使用して、"s" 形式の値を HH: mm: ss に変更します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-299">Change the value of sTimeFormat to HH:mm:ss by using the Windows PowerShell command-line interface as follows:</span></span>

1.  <span data-ttu-id="c12d7-300">Windows PowerShell を起動し、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-300">Start Windows PowerShell and run the following cmdlets:</span></span>
    
       ```PowerShell
        New-PSDrive -Name HKU -PSProvider Registry -Root HKEY_USERS
       ```
    
       ```PowerShell
        $a="HKU:\.Default\Control Panel\International"
       ```

2.  <span data-ttu-id="c12d7-301">現在の値を表示するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-301">To view the current value, run the following cmdlet:</span></span>
    
        Get-itemproperty $a -Name sTimeFormat
    
    <span data-ttu-id="c12d7-302">インストールの完了後に復元できるように、現在の形式の値をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-302">Make note of the current value for sTimeFormat so it can be restored after the installation is complete.</span></span>

3.  <span data-ttu-id="c12d7-303">新しい値に設定するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-303">To set to new value, run the following cmdlet:</span></span>
    
        Set-ItemProperty $a -Name sTimeFormat -Value "HH:mm:ss"

4.  <span data-ttu-id="c12d7-304">Lync Server 2013 が正常にインストールされた後、次のコマンドレットを実行して、その形式の元の値を復元します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-304">After Lync Server 2013 has been successfully installed, restore the original value for the sTimeFormat by running the following cmdlet:</span></span>
    
        - <span data-ttu-id="c12d7-305">手順3でメモした Set-ItemProperty $a 名、"<" という値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-305">Set-ItemProperty $a -Name sTimeFormat -Value "<Value noted down in Step 3.</span></span> <span data-ttu-id="c12d7-306">上の> "</span><span class="sxs-lookup"><span data-stu-id="c12d7-306">above>"</span></span>

</div>

</div>

<span id="Mobility"></span>

<div>

## <a name="mobility"></a><span data-ttu-id="c12d7-307">モビリティ</span><span class="sxs-lookup"><span data-stu-id="c12d7-307">Mobility</span></span>

<div>

## <a name="issues-for-mobile-clients-during-the-server-failover-process"></a><span data-ttu-id="c12d7-308">サーバーのフェールオーバープロセス中のモバイルクライアントの問題</span><span class="sxs-lookup"><span data-stu-id="c12d7-308">Issues for mobile clients during the server failover process</span></span>

<span data-ttu-id="c12d7-309">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-309">**Issue:**</span></span>

<span data-ttu-id="c12d7-310">Lync サーバーに障害が発生してフェールオーバープロセスが開始されると、次の問題がモバイルクライアントユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-310">When a Lync Server fails and the failover process begins, the following issues may affect mobile client users:</span></span>

  - <span data-ttu-id="c12d7-311">フェールオーバーの開始後、最長10分間、Lync の着信またはシグナルがありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-311">No incoming Lync call or signal for up to 10 minutes after failover begins.</span></span>

  - <span data-ttu-id="c12d7-312">着信チャット要求を受け入れることができません</span><span class="sxs-lookup"><span data-stu-id="c12d7-312">Cannot accept incoming Chat requests</span></span>

  - <span data-ttu-id="c12d7-313">障害が発生したサーバーがユーザーのホームサーバーである場合、会議に参加できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-313">Cannot join meetings if the failed server is the home server for the user</span></span>

<span data-ttu-id="c12d7-314">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-314">**Workaround:**</span></span>

<span data-ttu-id="c12d7-315">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-315">There is no workaround for this issue.</span></span> <span data-ttu-id="c12d7-316">フェールオーバープロセスが完了すると、通常の機能が復元されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-316">Normal functionality will be restored once the failover process is complete.</span></span>

</div>

<div>

## <a name="if-a-mobile-user-declines-an-incoming-call-from-another-lync-endpoint-the-call-is-displayed-as-a-missed-conversion-on-lync-mobile-clients"></a><span data-ttu-id="c12d7-317">モバイルユーザーが別の Lync エンドポイントからの着信を拒否した場合、その通話は Lync モバイルクライアントでの不在着信として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-317">If a mobile user declines an incoming call from another Lync endpoint, the call is displayed as a missed conversion on Lync Mobile clients</span></span>

<span data-ttu-id="c12d7-318">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-318">**Issue:**</span></span>

<span data-ttu-id="c12d7-319">モバイルユーザーが着信を拒否した場合に、別の Lync エンドポイントから発信された通話は、デバイス呼び出しリストの電話ではなく、Lync モバイルクライアントで不在着信した会話として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-319">If a mobile user declines an incoming call, and the call originated from another Lync endpoint, the call is displayed as a missed conversation in the Lync Mobile client instead of a call in the device call list.</span></span>

<span data-ttu-id="c12d7-320">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-320">**Workaround:**</span></span>

<span data-ttu-id="c12d7-321">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-321">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="the-mobile-client-may-not-display-a-federated-contacts-display-name-when-searching-for-contacts"></a><span data-ttu-id="c12d7-322">連絡先を検索するときに、モバイルクライアントでフェデレーション連絡先の表示名が表示されない場合がある</span><span class="sxs-lookup"><span data-stu-id="c12d7-322">The mobile client may not display a federated contact’s display name when searching for contacts</span></span>

<span data-ttu-id="c12d7-323">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-323">**Issue:**</span></span>

<span data-ttu-id="c12d7-324">フェデレーションされた連絡先の表示名は、連絡先リストでフェデレーション連絡先を検索する場合など、一部のシナリオでは表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-324">The display name for federated contacts may not be displayed in some scenarios, such as when searching for a federated contact in the contact list.</span></span> <span data-ttu-id="c12d7-325">この問題は、Lync モバイルクライアントからの連絡先に対してアクティブなプレゼンスサブスクリプションがない場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-325">This can occur when the there is no active presence subscription for the contact from the Lync mobile client.</span></span>

<span data-ttu-id="c12d7-326">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-326">**Workaround:**</span></span>

<span data-ttu-id="c12d7-327">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-327">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="in-the-mobile-client-invitee-and-timestamp-information-are-missing-from-a-missed-conversation-that-is-an-invitation-to-a-conference"></a><span data-ttu-id="c12d7-328">モバイルクライアントでは、会議に招待された不在着信した会話に出席者とタイムスタンプ情報が含まれていない</span><span class="sxs-lookup"><span data-stu-id="c12d7-328">In the mobile client, invitee and timestamp information are missing from a missed conversation that is an invitation to a conference</span></span>

<span data-ttu-id="c12d7-329">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-329">**Issue:**</span></span>

<span data-ttu-id="c12d7-330">モバイルクライアントで、不在着信した会話が会議に招待された場合、不在着信した会話メッセージに出席者とタイムスタンプ情報が表示されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-330">In the mobile client, when a missed conversation is an invitation to a conference, the invitee and timestamp information is missing from the missed conversation message.</span></span>

<span data-ttu-id="c12d7-331">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-331">**Workaround:**</span></span>

<span data-ttu-id="c12d7-332">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-332">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="mobile-client-users-making-calls-using-voip-are-not-be-able-to-leave-voice-mail-for-users-whose-voice-mail-is-configured-in-exchange-2010-or-earlier-versions"></a><span data-ttu-id="c12d7-333">VoIP を使用して電話をかけるモバイルクライアントユーザーが、Exchange 2010 以前のバージョンでボイスメールを構成しているユーザーのボイスメールを残すことができない</span><span class="sxs-lookup"><span data-stu-id="c12d7-333">Mobile client users making calls using VoIP are not be able to leave voice mail for users whose voice mail is configured in Exchange 2010 or earlier versions</span></span>

<span data-ttu-id="c12d7-334">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-334">**Issue:**</span></span>

<span data-ttu-id="c12d7-335">モバイルクライアントユーザーが VoIP を使用して通話を発信している場合、ユーザーは、Microsoft Exchange Server 2007 または Microsoft Exchange Server 2010 でボイスメールを使用するように構成されたユーザーのボイスメールメッセージを残すことはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-335">If a mobile client user is using VoIP to place calls, the user will not be able to leave voice mail messages for users configured to use voice mail in Microsoft Exchange Server 2007 or Microsoft Exchange Server 2010.</span></span>

<span data-ttu-id="c12d7-336">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-336">**Workaround:**</span></span>

<span data-ttu-id="c12d7-337">この問題を回避するには、Exchange 2010 と SP1 以降のバージョンの Microsoft Exchange Server を使用します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-337">To work around this issue, use Exchange 2010 with SP1 or later version of Microsoft Exchange Server.</span></span>

</div>

<div>

## <a name="when-using-block-with-url-for-client-version-configuration-on-mobile-clients-an-incorrect-error-message-may-be-displayed"></a><span data-ttu-id="c12d7-338">モバイルクライアントでクライアントのバージョン構成の URL がブロックされていると、誤ったエラーメッセージが表示されることがある</span><span class="sxs-lookup"><span data-stu-id="c12d7-338">When using Block with URL for Client Version Configuration on mobile clients, an incorrect error message may be displayed</span></span>

<span data-ttu-id="c12d7-339">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-339">**Issue:**</span></span>

<span data-ttu-id="c12d7-340">モバイルクライアントでクライアントバージョン構成の **URL をブロック** すると、クライアントバージョンがサポートされていない場合に誤ったエラーメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-340">When using **Block with URL** for Client Version Configuration on mobile clients, an incorrect error message may be displayed when the client version is not supported.</span></span>

<span data-ttu-id="c12d7-341">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-341">**Workaround:**</span></span>

<span data-ttu-id="c12d7-342">この問題を回避するには、 **URL を** 指定して block の代わりに **block** を使うようにクライアントのバージョン構成を構成します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-342">To work around this issue, configure Client Version Configuration to use **Block** instead of **Block with URL**.</span></span>

</div>

</div>

<span id="Conferencing"></span>

<div>

## <a name="conferencing"></a><span data-ttu-id="c12d7-343">会議</span><span class="sxs-lookup"><span data-stu-id="c12d7-343">Conferencing</span></span>

<div>

## <a name="antivirus-software-running-on-lync-server-2013-front-end-servers-can-cause-application-domain-recycling-which-temporarily-interrupts-service-for-lync-web-app-2013-lync-mobile-2010-and-lync-mobile-2013-clients"></a><span data-ttu-id="c12d7-344">Lync Server 2013 フロントエンドサーバーで実行されているウイルス対策ソフトウェアが原因で、アプリケーションドメインのリサイクルが発生し、Lync Web App 2013、Lync Mobile 2010、Lync Mobile 2013 クライアントのサービスが一時的に停止することがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-344">Antivirus software running on Lync Server 2013 Front End Servers can cause Application Domain recycling, which temporarily interrupts service for Lync Web App 2013, Lync Mobile 2010, and Lync Mobile 2013 clients</span></span>

<span data-ttu-id="c12d7-345">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-345">**Issue:**</span></span>

<span data-ttu-id="c12d7-346">ウイルス対策ソフトウェアを使用すると、アプリケーションドメインを再起動することができます。これにより、Lync Mobility Service 2013 および統合通信 (UC) Web API クライアントアプリケーション (Lync Web App 2013、Lync Mobile 2010、Lync Mobile 2013) が状態を失います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-346">Antivirus software can trigger application domain restarts, which can result in Lync Mobility Service 2013 and unified communications (UC) Web API client applications (Lync Web App 2013, Lync Mobile 2010, and Lync Mobile 2013) to lose their state.</span></span>

<span data-ttu-id="c12d7-347">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-347">**Workaround:**</span></span>

<span data-ttu-id="c12d7-348">この問題を回避するには、Web コンポーネントと .NET framework を含むフォルダーをウイルススキャンで除外します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-348">To work around this issue, exclude the folders containing Web components and .NET framework from antivirus scanning.</span></span> <span data-ttu-id="c12d7-349">詳細については、「Microsoft サポート技術情報の記事 312592 "PRB: ASP.NET で" アプリケーションが再起動します "というエラーが表示されて [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=312592](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=312592) います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-349">For details, see Microsoft Knowledge Base article 312592, "PRB: Random application restarts with 'Application is restarting' error in ASP.NET," at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=312592](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=312592).</span></span>

<span data-ttu-id="c12d7-350">次のフォルダーを除外する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-350">The following folders should be excluded:</span></span>

  - <span data-ttu-id="c12d7-351">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ mcx \\ Ext</span><span class="sxs-lookup"><span data-stu-id="c12d7-351">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Mcx\\Ext</span></span>

  - <span data-ttu-id="c12d7-352">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ mcx \\ Int</span><span class="sxs-lookup"><span data-stu-id="c12d7-352">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Mcx\\Int</span></span>

  - <span data-ttu-id="c12d7-353">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ ucwa \\ Int</span><span class="sxs-lookup"><span data-stu-id="c12d7-353">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Ucwa\\Int</span></span>

  - <span data-ttu-id="c12d7-354">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ ucwa \\ Ext</span><span class="sxs-lookup"><span data-stu-id="c12d7-354">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Ucwa\\Ext</span></span>

  - <span data-ttu-id="c12d7-355">% Windir% \\ Microsoft.NET \\ Framework64 \\ v 4.0.30319 \\ Config</span><span class="sxs-lookup"><span data-stu-id="c12d7-355">%Windir%\\Microsoft.NET\\Framework64\\v4.0.30319\\Config</span></span>

</div>

<div>

## <a name="activex-controls-or-native-xmlhttp-support-must-be-enabled-in-windows-internet-explorer-to-successfully-join-conferences"></a><span data-ttu-id="c12d7-356">会議に参加するには、Windows Internet Explorer で ActiveX コントロールまたはネイティブ XMLHTTP のサポートが有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-356">ActiveX Controls or native XMLHTTP support must be enabled in Windows Internet Explorer to successfully join conferences</span></span>

<span data-ttu-id="c12d7-357">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-357">**Issue:**</span></span>

<span data-ttu-id="c12d7-358">Windows Internet Explorer の Internet browser 設定で、ユーザーが ActiveX コントロールとネイティブ XMLHTTP のサポートを無効にしている場合、Internet Explorer が既定のブラウザーとして選択されていると、ユーザーは会議に参加できません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-358">If a user has disabled both ActiveX Controls and native XMLHTTP support in Windows Internet Explorer Internet browser settings, the user will not be able to join a meeting if Internet Explorer is selected as the default browser.</span></span>

<span data-ttu-id="c12d7-359">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-359">**Workaround:**</span></span>

<span data-ttu-id="c12d7-360">Internet Explorer で ActiveX コントロールまたは "ネイティブ XMLHTTP サポート" を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-360">Enable either ActiveX Controls or "native XMLHTTP support" in Internet Explorer.</span></span>

</div>

<div>

## <a name="lync-server-web-conferencing-service-cannot-recover-from-critical-mode"></a><span data-ttu-id="c12d7-361">Lync Server Web 会議サービスが、重要なモードから復元できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-361">Lync Server Web Conferencing service cannot recover from critical mode</span></span>

<span data-ttu-id="c12d7-362">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-362">**Issue:**</span></span>

<span data-ttu-id="c12d7-363">システム障害が発生した場合に、クリティカルモードが有効になっていると、重要モードが開始され、会議が参加者に対して機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-363">If critical mode is turned for archiving, in case of system failures, critical mode will start and the conferences will no longer work for the participants.</span></span> <span data-ttu-id="c12d7-364">管理者がシステムエラー (データベースの問題を修正するなど) を修正した後、データ会議サービスは自動的に回復しません。また、管理者は会議サービスを手動で再開して会議を再開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-364">After the administrator fixes the system failures (such as fixing a database issue), the data conferencing service doesn't automatically recover, and the administrator must manually restart the conferencing service for conferencing to resume.</span></span>

<span data-ttu-id="c12d7-365">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-365">**Workaround:**</span></span>

<span data-ttu-id="c12d7-366">システム障害が修正された後、管理者は会議サービスを手動で再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-366">An administrator needs to manually restart the conferencing service after the system failure is fixed.</span></span>

</div>

<div>

## <a name="web-conferencing-service-ignores-the-http-proxy-for-external-office-web-app-servers"></a><span data-ttu-id="c12d7-367">外部の Office Web App サーバーの HTTP プロキシを無視する web 会議サービス</span><span class="sxs-lookup"><span data-stu-id="c12d7-367">Web Conferencing service ignores the HTTP proxy for external Office Web App Servers</span></span>

<span data-ttu-id="c12d7-368">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-368">**Issue:**</span></span>

<span data-ttu-id="c12d7-369">Web 会議サービスの外部に Office Web Apps サーバーを展開している場合 (つまり、社内ネットワークに接続されていないサーバーである)、インターネット、境界ネットワーク、Web 会議サービスに接続するために HTTP プロキシが必要な場合、Office Web Apps サーバーの検出は失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-369">If you have deployed an Office Web Apps Server external to the Web Conferencing service (that is, a server that is not in the internal corporate network) in the Internet, perimeter network, and the Web Conferencing service requires an HTTP proxy to connect to this, the Office Web Apps Server discovery will fail.</span></span> <span data-ttu-id="c12d7-370">Web 会議サービスでは、[Office Web Apps サーバーセットアップ] の [トポロジビルダー] で定義されている HTTP プロキシ設定を無視します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-370">The Web Conferencing service ignores the HTTP proxy setting, as defined in Topology Builder for Office Web Apps Server setup.</span></span> <span data-ttu-id="c12d7-371">この結果、Lync クライアントは、会議の他の参加者と Microsoft PowerPoint 2010 共有を行うことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-371">As a result, the Lync client will not be able to do Microsoft PowerPoint 2010 sharing with other participants in the conference.</span></span> <span data-ttu-id="c12d7-372">オンプレミスの Lync Server をインストールしていて、内部ネットワークで Office Web Apps サーバーがオンプレミスにも構成されている場合、プロキシ構成は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-372">If you are installing Lync Server on-premises and also configure Office Web Apps Server on-premises in the internal network, a proxy configuration is not required.</span></span>

<span data-ttu-id="c12d7-373">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-373">**Workaround:**</span></span>

<span data-ttu-id="c12d7-374">唯一の回避策は、外部の Office Web Apps サーバーとの通信に HTTP プロキシを使用する必要がある展開構成を持たないことです。</span><span class="sxs-lookup"><span data-stu-id="c12d7-374">The only workaround is to not have a deployment configuration that requires the use of HTTP proxy to communicate with an external Office Web Apps Server.</span></span>

</div>

<div>

## <a name="adding-video-to-an-audio-conferencing-provider-conference-is-not-supported"></a><span data-ttu-id="c12d7-375">電話会議プロバイダーの会議へのビデオの追加はサポートされていません</span><span class="sxs-lookup"><span data-stu-id="c12d7-375">Adding video to an audio conferencing provider conference is not supported</span></span>

<span data-ttu-id="c12d7-376">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-376">**Issue:**</span></span>

<span data-ttu-id="c12d7-377">ユーザーが音声会議プロバイダーの電話会議に参加している場合、ビデオの追加はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-377">Adding a video is not supported if the user is joined to an audio conferencing provider conference for audio.</span></span>

<span data-ttu-id="c12d7-378">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-378">**Workaround:**</span></span>

<span data-ttu-id="c12d7-379">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-379">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="topologies-with-ipv6-enabled-force-the-lync-web-app-silverlight-plug-in-auto-update-to-ensure-screen-sharing-functionality-can-work-from-lync-web-app"></a><span data-ttu-id="c12d7-380">IPv6 が有効になっているトポロジ lync Web App Silverlight プラグインを自動更新して、Lync Web App から画面共有機能を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="c12d7-380">Topologies with IPv6 enabled force the Lync Web App Silverlight plug-in auto-update to ensure screen sharing functionality can work from Lync Web App</span></span>

<span data-ttu-id="c12d7-381">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-381">**Issue:**</span></span>

<span data-ttu-id="c12d7-382">IPv6 を有効にしてトポロジを構成すると、以前のバージョンの画面共有プラグインが既にインストールされている場合、ユーザーは Lync Web App クライアントから画面を共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-382">When a topology is configured with IPv6 enabled, users cannot share their screen from the Lync Web App client if an earlier version of the screen-sharing plug-in is already installed.</span></span>

<span data-ttu-id="c12d7-383">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-383">**Workaround:**</span></span>

<span data-ttu-id="c12d7-384">Lync Web App を使って会議に参加するときに、画面共有プラグインの最新バージョンに更新するには、次の2つ **のファイル** で "4.0.7457.0" から "4.0.7577.380" に変更します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-384">To force an update to the most recent version of the screen-sharing plug-in when joining meeting via Lync Web App, modify the value of **MinSupportedBuildVersion** from "4.0.7457.0" to "4.0.7577.380" in both of the following files:</span></span>

  - <span data-ttu-id="c12d7-385">% ProgramFiles% \\ Microsoft Lync Server 15 \\ Web コンポーネントは、 \\ \\ Int \\ クライアントプラグインにアクセス \\ \\ しますReachAppShPluginProperties.xml</span><span class="sxs-lookup"><span data-stu-id="c12d7-385">%ProgramFiles%\\Microsoft Lync Server 15\\Web Components\\Reach\\Int\\Client\\Plugins\\ReachAppShPluginProperties.xml</span></span>

  - <span data-ttu-id="c12d7-386">% ProgramFiles% \\ Microsoft Lync Server 15 \\ Web コンポーネントは、 \\ \\ Ext \\ クライアントプラグインにアクセス \\ \\ReachAppShPluginProperties.xml</span><span class="sxs-lookup"><span data-stu-id="c12d7-386">%ProgramFiles%\\Microsoft Lync Server 15\\Web Components\\Reach\\Ext\\Client\\Plugins\\ReachAppShPluginProperties.xml</span></span>

</div>

</div>

<span id="EnterpriseVoice"></span>

<div>

## <a name="enterprise-voice"></a><span data-ttu-id="c12d7-387">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="c12d7-387">Enterprise Voice</span></span>

<div>

## <a name="in-some-cases-a-lync-client-running-on-a-computer-configured-to-use-ipv4-and-ipv6-dual-stack-might-not-support-capabilities-that-rely-in-the-ip-subnet-of-the-computer-such-as-e911-media-bypass-call-admission-control-and-location-based-routing"></a><span data-ttu-id="c12d7-388">場合によっては、IPv4 と IPv6 を使用するように構成されているコンピューターで実行されている Lync クライアントで、E911、メディアのバイパス、通話受付制御、位置ベースのルーティングなど、コンピューターの IP サブネットに依存する機能がサポートされていないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-388">In some cases, a Lync client running on a computer configured to use IPv4 and IPv6 dual stack might not support capabilities that rely in the IP subnet of the computer such as E911, Media Bypass, Call Admission Control and Location Based Routing</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="c12d7-389">このセクションの情報は Lync Server 2013 の累積的な更新プログラム: 2013 年 2 月に関係します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-389">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="c12d7-390">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-390">**Issue:**</span></span>

<span data-ttu-id="c12d7-391">使用しているコンピューターで、IPv4 および IPv6 デュアルスタックが有効になっていて、プロキシサーバーの DNS 解決に基づいている場合、クライアントはコンピューターの IPv6 アドレスを使ってサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-391">When a Lync client is running on a computer that is enabled for IPv4 and IPv6 dual stack and based on the DNS resolution of the proxy server, the client may use the IPv6 address of the computer to sign in.</span></span> <span data-ttu-id="c12d7-392">この操作を行うと、Lync クライアントは IPv6 でサポートされている機能のみをサポートします。これにより、E911、メディアバイパス、通話受付制御、位置情報に基づくルーティングが除外されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-392">After doing so, the Lync Client will support only the capabilities supported for IPv6, which excludes E911, Media Bypass, Call Admission Control and Location Based Routing.</span></span>

<span data-ttu-id="c12d7-393">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-393">**Workaround:**</span></span>

<span data-ttu-id="c12d7-394">この問題を回避するには、クライアントコンピューターで IPv6 サポートを無効にします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-394">To work around this issue, disable IPv6 support on the client computer.</span></span>

</div>

<div>

## <a name="if-enterprise-voice-is-not-configured-for-a-user-the-user-will-need-to-use-e164-format-to-dial-out-from-a-conference"></a><span data-ttu-id="c12d7-395">エンタープライズ Voip がユーザーに対して構成されていない場合、ユーザーは [E164] 形式を使用して電話会議からダイヤルアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-395">If Enterprise Voice is not configured for a user, the user will need to use E164 format to dial out from a conference</span></span>

<span data-ttu-id="c12d7-396">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-396">**Issue:**</span></span>

<span data-ttu-id="c12d7-397">エンタープライズボイスがユーザーに対して構成されていない場合は、ユーザーは [E164] 形式を使用して会議からのダイヤルアウトを成功させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-397">If Enterprise Voice is not configured for a user, that user will need to use the E164 format to successfully dial out from a conference.</span></span> <span data-ttu-id="c12d7-398">E164 形式が使用されていない場合、ユーザーは電話会議からダイヤルアウトすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-398">If the E164 format is not used, the user will not be able to dial out from the conference.</span></span>

<span data-ttu-id="c12d7-399">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-399">**Workaround:**</span></span>

<span data-ttu-id="c12d7-400">この問題を回避するために、エンタープライズボイスを有効にしていないユーザーは、E164 形式の数字を使って会議からダイヤルアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-400">To work around this issue, users who are not enabled for Enterprise Voice should dial out from a conference by using numbers in the E164 format.</span></span>

</div>

</div>

<span id="Presence"></span>

<div>

## <a name="presence"></a><span data-ttu-id="c12d7-401">プレゼンス</span><span class="sxs-lookup"><span data-stu-id="c12d7-401">Presence</span></span>

<div>

## <a name="if-a-user-has-selected-block-all-invites-and-communications-while-the-unified-contact-store-is-turned-on-for-the-user-presence-status-is-not-rejected-when-it-should-be"></a><span data-ttu-id="c12d7-402">ユーザーが [すべての招待と通信をブロックする] をオンにした場合、統合連絡先ストアが有効になっているときにプレゼンス状態が拒否されない</span><span class="sxs-lookup"><span data-stu-id="c12d7-402">If a user has selected "Block all invites and communications" while the unified contact store is turned on for the user, Presence status is not rejected when it should be</span></span>

<span data-ttu-id="c12d7-403">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-403">**Issue:**</span></span>

<span data-ttu-id="c12d7-404">ユーザーが [すべての招待と通信をブロックする] をオンにした場合、統合連絡先ストアが有効になっている間、プレゼンス状態は拒否されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-404">If a user has selected "Block all invites and communications" while the unified contact store is turned on for the user, Presence status is not rejected when it should be.</span></span>

<span data-ttu-id="c12d7-405">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-405">**Workaround:**</span></span>

<span data-ttu-id="c12d7-406">この問題を回避するには、ユーザーに対してユニファイド連絡先ストアを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-406">To work around this issue, you can turn off the unified contact store for the user.</span></span> <span data-ttu-id="c12d7-407">そのためには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-407">To do so, run the following cmdlets:</span></span>

    Set-CsUserServicesPolicy -Identity "<user display name>" -UcsAllowed $False

<span data-ttu-id="c12d7-408">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-408">For example:</span></span>

    Set-CsUserServicesPolicy -Identity "Ken Myer" -UcsAllowed $False

</div>

<div>

## <a name="office-communications-server-2007-r2-users-homed-on-premises-are-not-able-to-see-the-presence-status-of-skype-for-business-online-users-in-hybrid-deployments---hybrid"></a><span data-ttu-id="c12d7-409">Office Communications Server 2007 R2 をオンプレミスで使用している場合、ハイブリッド展開での Skype for Business Online ユーザーのプレゼンス状態の表示はできません。ハイブリッド</span><span class="sxs-lookup"><span data-stu-id="c12d7-409">Office Communications Server 2007 R2 users homed on-premises are not able to see the Presence status of Skype for Business Online users in hybrid deployments - Hybrid</span></span>

<span data-ttu-id="c12d7-410">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-410">**Issue:**</span></span>

<span data-ttu-id="c12d7-411">この問題は、Lync Server 2013 ディレクターを使用している場合にハイブリッド展開で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-411">The issue may occur in a hybrid deployment when you are using a Lync Server 2013 Director.</span></span>

<span data-ttu-id="c12d7-412">Skype for Business Online を使用しているユーザーのプレゼンス状態は、オンプレミスのユーザーに対して不明なプレゼンスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-412">Presence status for users homed to Skype for Business Online is displayed as Presence Unknown for on-premises users.</span></span> <span data-ttu-id="c12d7-413">また、Skype for Business Online をホームとして使用しているユーザーは、Office Communications Server R2 オンプレミスユーザーのプレゼンス状態を表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-413">Also, users homed to Skype for Business Online are not able to see presence status for Office Communications Server R2 on-premises users.</span></span>

<span data-ttu-id="c12d7-414">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-414">**Workaround:**</span></span>

<span data-ttu-id="c12d7-415">この問題を部分的に回避するには、Lync Server 2013 ディレクターではなく、Lync Server 2013 のオンプレミスプールをポイントするように、Skype for Business Online ユーザーのホームサーバー (msrtcsip-userenabled true presencehomeserver) を変更します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-415">To partially work around this issue, change the Home Server (msrtcsip-presencehomeserver) of the Skype for Business Online users to point to a Lync Server 2013 on-premises pool instead of the Lync Server 2013 Director.</span></span> <span data-ttu-id="c12d7-416">オンプレミスフロントエンドサーバーでこの設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-416">You can modify this setting on the on-premises Front End Server.</span></span>

<span data-ttu-id="c12d7-417">この回避策では、Office Communications Server 2007 R2 に所属しているユーザーのプレゼンス状態が Skype for Business Online ユーザーに正しく表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-417">This workaround will correctly display the Presence status of users homed to Office Communications Server 2007 R2 to Skype for Business Online users.</span></span>

</div>

</div>

<span id="ResponseGroup"></span>

<div>

## <a name="response-group-application-call-park-application-and-group-call-pickup"></a><span data-ttu-id="c12d7-418">応答グループアプリケーション、コールパークアプリケーション、グループ通話のピックアップ</span><span class="sxs-lookup"><span data-stu-id="c12d7-418">Response Group application, Call Park application, and Group Call Pickup</span></span>

<div>

## <a name="a-caller-might-hear-one-second-of-music-on-hold-during-the-establishment-of-a-call-with-the-retrieving-party"></a><span data-ttu-id="c12d7-419">発信者は、相手を検索して通話を発信するときに、1秒間音楽の再生待ちを聞くことができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-419">A caller might hear one second of music-on-hold during the establishment of a call with the retrieving party</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="c12d7-420">このセクションの情報は Lync Server 2013 の累積的な更新プログラム: 2013 年 2 月に関係します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-420">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="c12d7-421">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-421">**Issue:**</span></span>

<span data-ttu-id="c12d7-422">グループ通話の集配を使用して通話を取得すると、発信者は、取得側で通話を発信するときに、1秒間音楽を保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-422">When a call is retrieved via Group Call Pickup, the caller might hear one second of music-on-hold during the establishment of the call with the retriever party.</span></span>

<span data-ttu-id="c12d7-423">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-423">**Workaround:**</span></span>

<span data-ttu-id="c12d7-424">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-424">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="a-response-group-agent-can-sign-in-and-sign-out-through-a-lync-server-2010-agent-console-to-lync-server-2010-formal-agent-groups-only"></a><span data-ttu-id="c12d7-425">応答グループエージェントは、Lync Server 2010 エージェントコンソールを使用して、Lync Server 2010 の正式なエージェントグループのみにサインインしてサインアウトすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-425">A Response Group agent can sign in and sign out through a Lync Server 2010 Agent Console to Lync Server 2010 formal Agent Groups only</span></span>

<span data-ttu-id="c12d7-426">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-426">**Issue:**</span></span>

<span data-ttu-id="c12d7-427">Lync server 2013 応答グループエージェントは、lync Server 2010 エージェントコンソールを使用して、lync server 2010 正式なエージェントグループに対してのみサインインし、サインアウトすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-427">A Lync Server 2013 Response Group agent can sign in and sign out through a Lync Server 2010 Agent Console to Lync Server 2010 formal Agent Groups only.</span></span> <span data-ttu-id="c12d7-428">Lync Server 2010 エージェントコンソールでは、ユーザーが所属している Lync Server の2010応答グループのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-428">In the Lync Server 2010 Agent Console, users can see only the Lync Server 2010 Response Group that they belong to.</span></span> <span data-ttu-id="c12d7-429">自分が属している Lync Server 2013 応答グループを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-429">They cannot see any of the Lync Server 2013 Response Groups that they belong to.</span></span>

<span data-ttu-id="c12d7-430">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-430">**Workaround:**</span></span>

<span data-ttu-id="c12d7-431">応答グループエージェントが Lync Server 2013 ユーザーであり、Lync Server 2013 の正式なエージェントグループの一部である場合、ユーザーはブラウザーの web リンクを通じて直接 Lync Server 2013 エージェントコンソールにアクセスし、Lync Server 2013 エージェントグループにサインインしてサインアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-431">If the Response Group agent is a Lync Server 2013 user, and part of a Lync Server 2013 formal Agent Group, the user must access the Lync Server 2013 Agent Console directly via a web link in a browser to sign in to and sign out from Lync Server 2013 Agent Groups.</span></span>

</div>

<div>

## <a name="a-lync-server-2010-response-group-agent-cannot-place-calls-on-behalf-of-a-lync-server-2013-response-group"></a><span data-ttu-id="c12d7-432">Lync server 2010 応答グループエージェントは、Lync Server 2013 応答グループの代理として通話を発信することはできません</span><span class="sxs-lookup"><span data-stu-id="c12d7-432">A Lync Server 2010 Response Group agent cannot place calls on behalf of a Lync Server 2013 Response Group</span></span>

<span data-ttu-id="c12d7-433">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-433">**Issue:**</span></span>

<span data-ttu-id="c12d7-434">Lync server 2013 応答グループのエージェントである Lync Server 2010 ユーザーは、応答グループの代理として通話を発信できません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-434">A Lync Server 2010 user who is an Agent of a Lync Server 2013 Response Group is not able to place a call on behalf of the Response Group.</span></span> <span data-ttu-id="c12d7-435">Lync Server 2013 応答グループは、通話を発信するために Lync クライアントでは利用できません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-435">The Lync Server 2013 Response Group will not be available in the Lync Client to place a call.</span></span>

<span data-ttu-id="c12d7-436">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-436">**Workaround:**</span></span>

<span data-ttu-id="c12d7-437">この問題を回避するには、Lync Server 2010 ユーザーを Lync Server 2013 に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-437">To work around this issue, you must move the Lync Server 2010 user to Lync Server 2013.</span></span>

</div>

<div>

## <a name="removing-a-response-group-from-lync-server-2010-after-it-has-been-migrated-to-lync-server-2013-will-prevent-the-response-group-from-accepting-any-incoming-calls"></a><span data-ttu-id="c12d7-438">Lync server 2013 に移行された後に、Lync Server 2010 から応答グループを削除すると、応答グループが着信を受け付けることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-438">Removing a Response Group from Lync Server 2010 after it has been migrated to Lync Server 2013 will prevent the Response Group from accepting any incoming calls</span></span>

<span data-ttu-id="c12d7-439">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-439">**Issue:**</span></span>

<span data-ttu-id="c12d7-440">Lync server 2010 から Lync server 2013 に移行された応答グループが lync server の [コントロールパネル] または [Lync Server 管理シェル] から2010削除された場合、Lync Server 2013 の応答グループは、着信の受信を停止します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-440">If a Response Group that has been migrated from Lync Server 2010 to Lync Server 2013 is removed from Lync Server 2010 through the Lync Server Control Panel or the Lync Server Management Shell, the Response Group in Lync Server 2013 will stop receiving any incoming calls.</span></span>

<span data-ttu-id="c12d7-441">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-441">**Workaround:**</span></span>

<span data-ttu-id="c12d7-442">この問題を回避するには、Lync Server 2010 から Lync Server 2013 に移行された返信グループを Lync server 2010 から削除しないようにします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-442">To work around this issue, do not remove any Response Groups from Lync Server 2010 that have been migrated from Lync Server 2010 to Lync Server 2013.</span></span>

<span data-ttu-id="c12d7-443">応答グループが既に削除されている場合は、Lync Server 2013 で再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-443">If the Response Group has already been removed, you should redeploy it in Lync Server 2013.</span></span>

</div>

<div>

## <a name="when-a-new-managed-workflow-is-set-to-inactive-when-created-deployment-of-the-workflow-will-fail"></a><span data-ttu-id="c12d7-444">作成時に新しいマネージワークフローが非アクティブに設定されると、ワークフローの展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-444">When a new managed workflow is set to inactive when created, deployment of the workflow will fail</span></span>

<span data-ttu-id="c12d7-445">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-445">**Issue:**</span></span>

<span data-ttu-id="c12d7-446">作成時に新しいマネージワークフローが非アクティブに設定されると、ワークフローの展開が失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-446">When a new managed workflow is set to inactive when created, deployment of the workflow will fail.</span></span> <span data-ttu-id="c12d7-447">この問題は、作成時にワークフローが [非アクティブ] に設定されているときに発生しますが、展開された後に [非アクティブ] に設定するように編集されたワークフローには影響しません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-447">This issue is encountered when the workflow is set to inactive when created, but does not affect a workflow that is edited to set it to inactive after is has been deployed.</span></span>

<span data-ttu-id="c12d7-448">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-448">**Workaround:**</span></span>

<span data-ttu-id="c12d7-449">ワークフローを作成して展開するときに、ワークフローをアクティブとして設定し、展開します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-449">When creating and deploying a workflow, set the workflow as active and then deploy it.</span></span> <span data-ttu-id="c12d7-450">ワークフローが正常に展開されると、ワークフローが編集可能になり、[非アクティブ] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-450">After the workflow is successfully deployed, the workflow can be edited and set to inactive.</span></span>

</div>

<div>

## <a name="removing-a-response-group-from-the-owner-pool-will-prevent-the-response-group-of-the-backup-pool-from-accepting-any-incoming-calls-during-failover-if-the-response-group-has-been-imported-to-the-backup-pool"></a><span data-ttu-id="c12d7-451">所有者プールから応答グループを削除すると、バックアッププールの応答グループがバックアッププールにインポートされた場合に、フェールオーバー中に着信を受け付けることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-451">Removing a Response Group from the Owner pool will prevent the Response Group of the Backup pool from accepting any incoming calls during failover if the Response Group has been imported to the Backup pool</span></span>

<span data-ttu-id="c12d7-452">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-452">**Issue:**</span></span>

<span data-ttu-id="c12d7-453">所有者を上書きせずに、プライマリプールによって所有されている応答グループがバックアッププールにインポートされていて、所有者プールから応答グループが削除された場合、バックアッププール内の応答グループは、フェールオーバー中に着信通話を受け入れません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-453">If a Response Group that is owned by the primary pool has been imported to the backup pool without overwriting the owner, and the Response Group is removed from the owner pool, the Response Group in the Backup pool will not accept any incoming calls during failover.</span></span>

<span data-ttu-id="c12d7-454">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-454">**Workaround:**</span></span>

<span data-ttu-id="c12d7-455">プライマリプールで応答グループを再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-455">You will need to redeploy the Response Group in the Primary pool.</span></span> <span data-ttu-id="c12d7-456">次に、プライマリプールから応答グループの構成をエクスポートして、もう一度バックアッププールにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-456">You will then need to export the Response Group configuration from the Primary pool and import it to the Backup pool again.</span></span>

<span data-ttu-id="c12d7-457">バックアッププールで応答グループを再作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-457">You can also recreate the Response Group in the Backup pool.</span></span> <span data-ttu-id="c12d7-458">この場合、バックアッププールは応答グループの所有者プールになります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-458">In this case, the Backup pool will be the owner pool of the Response Group.</span></span>

</div>

<div>

## <a name="a-parked-call-cant-be-retrieved-from-the-call-park-application-if-the-retrieve-request-is-done-on-behalf-of-a-response-group"></a><span data-ttu-id="c12d7-459">受信要求が応答グループの代理として実行されている場合は、保留中の通話をコールパークアプリケーションから取得できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-459">A parked call can't be retrieved from the Call Park application if the retrieve request is done on behalf of a Response Group</span></span>

<span data-ttu-id="c12d7-460">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-460">**Issue:**</span></span>

<span data-ttu-id="c12d7-461">次の条件が満たされている場合は、保留中の通話の取得要求が失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-461">When the following conditions are true, a retrieve request for a parked call will fail:</span></span>

  - <span data-ttu-id="c12d7-462">エージェントが匿名応答グループの一部である</span><span class="sxs-lookup"><span data-stu-id="c12d7-462">An agent is part of an anonymous Response Group</span></span>

  - <span data-ttu-id="c12d7-463">エージェントは、匿名応答グループを通じて、コールパークアプリケーションから保留中の通話を取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-463">The agent attempts to retrieve a parked call from the Call Park application through the anonymous Response Group</span></span>

  - <span data-ttu-id="c12d7-464">エージェントは、[代理人として呼び出し] オプションを通じて、または Lync アテンダントクライアントで同じオプションを使用して、軌道番号にダイヤルすることで、通話を取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-464">The agent attempts to retrieve the call by dialing the orbit number through the Call On Behalf option or through the same option in the Lync attendant client</span></span>

<span data-ttu-id="c12d7-465">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-465">**Workaround:**</span></span>

<span data-ttu-id="c12d7-466">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-466">There are no workarounds for this issue.</span></span> <span data-ttu-id="c12d7-467">保留中の呼び出しは、応答グループに代わって取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-467">The parked call should be retrieved without doing so on behalf of a Response Group.</span></span>

</div>

</div>

<span id="TopoBuilder"></span>

<div>

## <a name="lync-server-control-panel-topology-builder-and-planning-tool"></a><span data-ttu-id="c12d7-468">Lync Server コントロール パネル、トポロジ ビルダー、および計画ツール</span><span class="sxs-lookup"><span data-stu-id="c12d7-468">Lync Server Control Panel, Topology Builder, and Planning Tool</span></span>

<div>

## <a name="planning-tool-limitations"></a><span data-ttu-id="c12d7-469">計画ツールの制限</span><span class="sxs-lookup"><span data-stu-id="c12d7-469">Planning Tool Limitations</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="c12d7-470">このセクションの情報は Lync Server 2013 の累積的な更新プログラム: 2013 年 2 月に関係します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-470">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="c12d7-471">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-471">**Issue:**</span></span>

<span data-ttu-id="c12d7-472">展開を計画する場合、計画ツールには次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-472">The Planning Tool has the following limitations when planning for your deployment:</span></span>

  - <span data-ttu-id="c12d7-473">サポートされる最大10個のセントラルサイトがあります</span><span class="sxs-lookup"><span data-stu-id="c12d7-473">There is a maximum of 10 central sites supported</span></span>

  - <span data-ttu-id="c12d7-474">各セントラルサイトは、最大で14個のブランチサイトを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-474">Each central site can have a maximum of 14 branch sites</span></span>

  - <span data-ttu-id="c12d7-475">各セントラルサイトには、最大24万ユーザーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-475">Each central site can have a maximum of 240,000 users</span></span>

<span data-ttu-id="c12d7-476">また、推奨されるトポロジを計算するときに、計画ツールには次の値は含まれません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-476">In addition, the Planning Tool does not include values for the following when calculating the recommended topology:</span></span>

  - <span data-ttu-id="c12d7-477">オンラインになっているユーザーの数</span><span class="sxs-lookup"><span data-stu-id="c12d7-477">The number of users that are homed online</span></span>

  - <span data-ttu-id="c12d7-478">XMPP フェデレーションが有効になっているユーザーのパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="c12d7-478">The percentage of users that are enabled for XMPP federation</span></span>

  - <span data-ttu-id="c12d7-479">Lync Web App を使用しているユーザーのパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="c12d7-479">Percentage of users that are using Lync Web App</span></span>

<span data-ttu-id="c12d7-480">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-480">**Workaround:**</span></span>

<span data-ttu-id="c12d7-481">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-481">There is no workaround for these issues.</span></span> <span data-ttu-id="c12d7-482">計画ツールの詳細については、「 [計画ツールを使用して Lync Server 2013 のトポロジを設計](lync-server-2013-designing-the-topology-by-using-the-planning-tool.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-482">For more information about the Planning Tool, see [Designing the topology for Lync Server 2013 by using the Planning Tool](lync-server-2013-designing-the-topology-by-using-the-planning-tool.md).</span></span>

</div>

<div>

## <a name="planning-tool-may-not-use-previously-defined-ip-addresses-for-the-edge-network-when-updating-options"></a><span data-ttu-id="c12d7-483">オプションを更新するときに、計画ツールで、エッジネットワークに事前に定義された IP アドレスを使用できない場合がある</span><span class="sxs-lookup"><span data-stu-id="c12d7-483">Planning Tool may not use previously defined IP addresses for the Edge network when updating options</span></span>

<span data-ttu-id="c12d7-484">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-484">**Issue:**</span></span>

<span data-ttu-id="c12d7-485">計画ツールを使用して設計を完了した後、エッジネットワークのオプションを変更すると、既存の IP アドレスを更新する代わりに、追加の IP アドレスを設計に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-485">After you complete your design using the Planning Tool, if you make changes to the Edge Network options, additional IP addresses may be added to the design instead of updating the existing IP addresses.</span></span> <span data-ttu-id="c12d7-486">この問題は、Edge ネットワーク図の詳細を表示しているときに、[ **ここをクリックしてオプションを更新する**] を選択し、[構成オプション] ダイアログで、[edge ネットワーク] を選択します。 [ **同じ fqdn と IP アドレスを使用しますが、エッジサーバー上のエッジサービスには異なるポートを使用** します] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-486">This can occur when you are viewing the details of the Edge Network Diagram, select **Click here to update your options**, and then, on the Configuration Options dialog, you select Edge Network select **I want to use the same FQDNs and IP addresses, but different ports for the edge services on my Edge Server**.</span></span> <span data-ttu-id="c12d7-487">変更を適用すると、新しい IP アドレスとエッジサーバーがデザインに追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-487">Applying any changes may result in new IP addresses and Edge servers being added to the design.</span></span>

<span data-ttu-id="c12d7-488">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-488">**Workaround:**</span></span>

<span data-ttu-id="c12d7-489">現時点では、この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-489">There is no workaround for this issue at this time.</span></span>

</div>

<div>

## <a name="in-lync-server-control-panel-move-all-users-to-pool-may-not-work-as-expected"></a><span data-ttu-id="c12d7-490">Lync Server コントロールパネルの [すべてのユーザーをプールに移動] が期待どおりに動作しない場合がある</span><span class="sxs-lookup"><span data-stu-id="c12d7-490">In Lync Server Control Panel, "Move all users to pool" may not work as expected</span></span>

<span data-ttu-id="c12d7-491">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-491">**Issue:**</span></span>

<span data-ttu-id="c12d7-492">Lync Server コントロールパネルを使用して、1つのプールから、複数のドメインコントローラーと親/子ドメインを持つ複雑な Active Directory 環境の別のプールにすべてのユーザーを移動する場合、エラーメッセージが表示されることがあります。 "指定されたユーザーはレガシユーザーではないため、Move-CsUser コマンドレットを使用します。"</span><span class="sxs-lookup"><span data-stu-id="c12d7-492">When using the Lync Server Control Panel to move all users from one pool to another pool in a complex Active Directory environment, such as one with multiple Domain Controllers and parent/child domains, an error message may be returned that states, “Specified user is not a legacy user, use Move-CsUser cmdlet instead.”</span></span> <span data-ttu-id="c12d7-493">これは、複雑な Active Directory 環境でのレプリケーション時間が長くなったためです。</span><span class="sxs-lookup"><span data-stu-id="c12d7-493">This is a result of longer replication times in complex Active Directory environments.</span></span>

<span data-ttu-id="c12d7-494">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-494">**Workaround:**</span></span>

<span data-ttu-id="c12d7-495">この問題を回避するには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-495">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="c12d7-496">Lync Server コントロールパネルで [フィルター] を使用して、従来のユーザーを検索し、それらのユーザーを選択して、[**すべてのユーザーをプールに** 移動] ではなく、[**選択したユーザーをプールに移動] コマンド** を使用します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-496">Use filters in the Lync Server Control Panel to search for legacy users, select those users, and then use the **Move selected users to pool command** instead of **Move all users to pool**.</span></span>

  - <span data-ttu-id="c12d7-497">Lync server 管理シェルを使用して、Lync Server コマンドレットを使用して、従来のユーザーをまとめて移動します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-497">Use the Lync Server Management Shell to move legacy users in batches by using Lync Server cmdlets.</span></span>

</div>

<div>

## <a name="the-lync-server-control-panel-stops-working-in-a-vmware-environment-after-the-microsoft-silverlight-browser-plug-in-is-updated-to-version-5"></a><span data-ttu-id="c12d7-498">Microsoft Silverlight ブラウザープラグインをバージョン5に更新した後に、Lync Server コントロールパネルが VMware 環境で動作を停止する</span><span class="sxs-lookup"><span data-stu-id="c12d7-498">The Lync Server Control Panel stops working in a VMware environment after the Microsoft Silverlight browser plug-in is updated to version 5</span></span>

<span data-ttu-id="c12d7-499">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-499">**Issue:**</span></span>

<span data-ttu-id="c12d7-500">VMware 環境で Lync Server コントロールパネルを使用すると、Silverlight をバージョン5にアップグレードした後に Lync Server コントロールパネルが機能しなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-500">If you use the Lync Server Control Panel in a VMware environment, the Lync Server Control Panel may stop working after you upgrade Silverlight to version 5.</span></span>

<span data-ttu-id="c12d7-501">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-501">**Workaround:**</span></span>

<span data-ttu-id="c12d7-502">この問題を回避するには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-502">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="c12d7-503">Silverlight 5 をアンインストールしてから、Silverlight 4 をからインストールし [https://go.microsoft.com/fwlink/p/?LinkID=149156\&v=4.0](https://go.microsoft.com/fwlink/p/?linkid=149156%26v=4.0) ます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-503">Uninstall Silverlight 5, and then install Silverlight 4 from [https://go.microsoft.com/fwlink/p/?LinkID=149156\&v=4.0](https://go.microsoft.com/fwlink/p/?linkid=149156%26v=4.0).</span></span>

  - <span data-ttu-id="c12d7-504">Lync Server コントロールパネルを、VMware 仮想コンピューターではないコンピューターから開きます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-504">Open the Lync Server Control Panel from a computer that is not a VMware virtual computer.</span></span>
    
    <span data-ttu-id="c12d7-505">リモートコンピューターから Lync Server コントロールパネルを開くには、コンピューターに Lync Server 管理ツールをインストールして、Windows の [ **スタート** ] メニューから Lync Server コントロールパネルを起動します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-505">To open the Lync Server Control Panel from a remote computer, install Lync Server Administration tools on the computer, and then start the Lync Server Control Panel from the Windows **Start** menu.</span></span>
    
    <span data-ttu-id="c12d7-506">Web ブラウザーで URL を入力して、Lync Server コントロールパネルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-506">You can also open the Lync Server Control Panel by entering the URL in a web browser.</span></span> <span data-ttu-id="c12d7-507">URL は https:///cscp. に似ています。 \<frontend\_pool\_fqdn\></span><span class="sxs-lookup"><span data-stu-id="c12d7-507">The URL will be similar to https://\<frontend\_pool\_fqdn\>/cscp.</span></span>

</div>

<div>

## <a name="an-administrator-cannot-run-the-uninstall-csmirrordb-cmdlet-after-removing-the-mirroring-database-in-topology-builder"></a><span data-ttu-id="c12d7-508">トポロジビルダーでミラーリングデータベースを削除した後に、管理者がアンインストール-csMirrorDB コマンドレットを実行できない</span><span class="sxs-lookup"><span data-stu-id="c12d7-508">An administrator cannot run the Uninstall-csMirrorDB cmdlet after removing the mirroring database in Topology Builder</span></span>

<span data-ttu-id="c12d7-509">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-509">**Issue:**</span></span>

<span data-ttu-id="c12d7-510">管理者がトポロジビルダーでミラーリングデータベースを無効にして、トポロジビルダーでミラーリングデータベースを削除すると、管理者が **csMirrorDatabase** コマンドレットを実行して SQL Server からミラーリングを削除するようにメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-510">When an administrator disables a mirroring database in Topology Builder, and then deletes the mirroring database in Topology Builder, a message is displayed in the To do list for the administrator to run the **Uninstall-csMirrorDatabase** cmdlet to remove mirroring from SQL Server.</span></span> <span data-ttu-id="c12d7-511">管理者がコマンドレットを実行しようとすると、失敗します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-511">When the administrator attempts to run the cmdlet, it fails.</span></span>

<span data-ttu-id="c12d7-512">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-512">**Workaround:**</span></span>

<span data-ttu-id="c12d7-513">トポロジビルダーでプールの SQL ミラーリングを削除するには、最初にコマンドレットを使用して、SQL Server のミラーを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-513">To remove SQL mirroring of a pool in Topology Builder, you must first use a cmdlet to remove the mirror in SQL Server.</span></span> <span data-ttu-id="c12d7-514">次に、トポロジ ビルダーを使用して、トポロジからミラーを削除できます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-514">You can then use Topology Builder to remove the mirror from the topology.</span></span> <span data-ttu-id="c12d7-515">SQL Server でミラーを削除するには、次のコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-515">To remove the mirror in SQL Server, use the following cmdlet:</span></span>

    Uninstall-CsMirrorDatabase -SqlServerFqdn <SQLServer FQDN> [-SqlInstanceName <SQLServer instance name>] -DatabaseType <Application | Archiving | CentralMgmt | Monitoring | User | BIStaging | PersistentChat | PersistentChatCompliance> [-DropExistingDatabasesOnMirror] [-Verbose]

<span data-ttu-id="c12d7-516">たとえば、ミラーリングを削除してユーザーデータベースのデータベースをドロップするには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-516">For example, to remove mirroring and drop the databases for the user databases, type the following:</span></span>

    Uninstall-CsMirrorDatabase -SqlServerFqdn primaryBE.contoso.com -SqlInstanceName rtc -Verbose -DatabaseType User -DropExistingDatabasesOnMirror

<span data-ttu-id="c12d7-517">*Dropexistingdatabases Onmirror* パラメーターを使うと、影響を受けたデータベースがミラーから削除されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-517">The *DropExistingDatabasesOnMirror* parameter causes the affected databases to be deleted from the mirror.</span></span> <span data-ttu-id="c12d7-518">その後、トポロジからミラーを削除するために次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-518">Then, to remove the mirror from the topology, do the following:</span></span>

1.  <span data-ttu-id="c12d7-519">トポロジ ビルダーで、プールを右クリックし、[**プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-519">In Topology Builder, right-click the pool and click **Edit Properties**.</span></span>

2.  <span data-ttu-id="c12d7-520">[ **SQL ストアミラーリングを有効にする** ] をオフにし、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-520">Clear **Enable SQL Store Mirroring** and click **OK**.</span></span>

3.  <span data-ttu-id="c12d7-521">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-521">Publish the topology.</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="c12d7-522">バックエンドデータベースミラーリングの関係を変更する場合は、必ずプール内のすべてのフロントエンドサーバーを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-522">Whenever you make a change to a back-end database mirroring relationship, you must restart all the Front End Servers in the pool.</span></span>



</div>

</div>

<div>

## <a name="validation-errors-are-returned-in-topology-builder-when-an-administrator-attempts-to-remove-a-deployment-with-a-front-end-pool-that-has-an-associated-witness-store"></a><span data-ttu-id="c12d7-523">管理者が、関連付けられている監視ストアを持つフロントエンドプールを使用して展開を削除しようとすると、検証エラーがトポロジビルダーで返される</span><span class="sxs-lookup"><span data-stu-id="c12d7-523">Validation errors are returned in Topology Builder when an administrator attempts to remove a deployment with a Front End pool that has an associated witness store</span></span>

<span data-ttu-id="c12d7-524">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-524">**Issue:**</span></span>

<span data-ttu-id="c12d7-525">管理者が、関連付けられている監視ストアでフロントエンドプールを含む展開を削除するために、管理者がトポロジビルダーで [ **展開の削除** ] を使用しようとした場合、トポロジビルダーに検証エラーが表示され、操作は続行されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-525">If an administrator attempts to use the **Remove Deployment** command in Topology Builder to remove a deployment that includes a Front End pool with an associated witness store, a validation error is displayed in Topology Builder and the action will not proceed.</span></span>

<span data-ttu-id="c12d7-526">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-526">**Workaround:**</span></span>

<span data-ttu-id="c12d7-527">この問題を回避するには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c12d7-527">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="c12d7-528">展開を削除する前に、監視ストアを削除します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-528">Remove the witness store before attempting to remove the deployment.</span></span>

  - <span data-ttu-id="c12d7-529">フロントエンドプールの監視ストアを追加してから、削除します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-529">Add a witness store for the Front End pool and then remove it.</span></span>

</div>

<div>

## <a name="persistent-chat-server-deployment-information-is-inconsistent-between-the-planning-tool-and-topology-builder"></a><span data-ttu-id="c12d7-530">計画ツールとトポロジビルダーとの間の常設チャットサーバーの展開情報に一貫性がない</span><span class="sxs-lookup"><span data-stu-id="c12d7-530">Persistent Chat Server deployment information is inconsistent between the Planning Tool and Topology Builder</span></span>

<span data-ttu-id="c12d7-531">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-531">**Issue:**</span></span>

<span data-ttu-id="c12d7-532">Lync Server 2013、計画ツールが、永続的なチャットサーバーの展開のために、障害回復を有効にしてサイトトポロジ図を出力すると、サイトトポロジ図には複数の (物理) サイトが含まれ、各サイトには均等に割り当てられた常設チャットサーバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-532">When the Lync Server 2013, Planning Tool outputs the site topology diagram for a Persistent Chat Server deployment with disaster recovery enabled, the site topology diagram includes multiple (physical) sites, with evenly assigned Persistent Chat Servers at each site.</span></span> <span data-ttu-id="c12d7-533">Topology Builder では、すべての常設チャットサーバーは1つの (論理) サイトに属しているものとして表され、同じ常設チャットサーバープールノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-533">In Topology Builder, all Persistent Chat Servers are represented as belonging to a single (logical) site, and are listed under the same Persistent Chat Server pool node.</span></span>

<span data-ttu-id="c12d7-534">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-534">**Workaround:**</span></span>

<span data-ttu-id="c12d7-535">現時点では、この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-535">Currently, we do not have a workaround for this issue.</span></span> <span data-ttu-id="c12d7-536">ユーザーは、常設チャットサーバー展開の計画ツールの出力を分析し、特定のニーズに合わせてプランを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-536">The user should analyze the output of the Planning Tool for the Persistent Chat Server deployment, and modify the plan to meet their specific needs.</span></span>

</div>

</div>

<span id="Localization"></span>

<div>

## <a name="localization"></a><span data-ttu-id="c12d7-537">版</span><span class="sxs-lookup"><span data-stu-id="c12d7-537">Localization</span></span>

<div>

## <a name="monitoring"></a><span data-ttu-id="c12d7-538">監視</span><span class="sxs-lookup"><span data-stu-id="c12d7-538">Monitoring</span></span>

<div>

## <a name="the-deploy-monitoring-reports-wizard-displays-incorrect-characters-under-certain-circumstances-when-using-the-east-asian-version-of-lync-server"></a><span data-ttu-id="c12d7-539">東アジアバージョンの Lync Server を使用すると、監視レポートの展開ウィザードで特定の状況で誤った文字が表示される</span><span class="sxs-lookup"><span data-stu-id="c12d7-539">The Deploy Monitoring Reports wizard displays incorrect characters under certain circumstances when using the East Asian version of Lync Server</span></span>

<span data-ttu-id="c12d7-540">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-540">**Issue:**</span></span>

<span data-ttu-id="c12d7-541">日本語版の Lync Server 2013 (中国語 (簡体字)、中国語 (繁体字)、日本語、韓国語など) を使用している場合、システムロケールが東アジア言語に設定されていないオペレーティングシステムでは、[監視レポートの展開] ウィザードでは、ローカライズされたメッセージの代わりに疑問符などの文字が表示されます</span><span class="sxs-lookup"><span data-stu-id="c12d7-541">When using an East Asian version of Lync Server 2013—for example, Chinese (Simplified), Chinese (Traditional), Japanese, or Korean—on an operating system that has the system locale not set to an East Asian language, the Deploy Monitoring Reports wizard will display question marks or other characters instead of localized messages.</span></span>

<span data-ttu-id="c12d7-542">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-542">**Workaround:**</span></span>

<span data-ttu-id="c12d7-543">この問題を解決するには、オペレーティングシステムと Lync Server 2013 のロケールを同じ言語に設定します。これにより、すべてのメッセージが正しく表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-543">To correct this issue, set the locale for the operating system and Lync Server 2013 to the same language, which will display all messages correctly.</span></span>

</div>

</div>

<div>

## <a name="lync-server-control-panel"></a><span data-ttu-id="c12d7-544">Lync Server コントロール パネル</span><span class="sxs-lookup"><span data-stu-id="c12d7-544">Lync Server Control Panel</span></span>

<div>

## <a name="in-certain-cases-the-first-item-in-the-top-navigation-bar-on-a-page-of-lync-server-control-panel-disappears-when-the-last-item-in-the-top-navigation-bar-is-clicked"></a><span data-ttu-id="c12d7-545">特定の状況では、トップナビゲーションバーの最後のアイテムがクリックされると、Lync Server コントロールパネルのページ上のトップナビゲーションバーの最初のアイテムが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-545">In certain cases, the first item in the top navigation bar on a page of Lync Server Control Panel disappears when the last item in the top navigation bar is clicked</span></span>

<span data-ttu-id="c12d7-546">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-546">**Issue:**</span></span>

<span data-ttu-id="c12d7-547">Lync Server コントロールパネルのページの上部にあるナビゲーションバーで最後のアイテムをクリックすると、トップナビゲーションバーの最初のアイテムが非表示になるという3つの既知の場合があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-547">There are three known cases where clicking the last item in the top navigation bar on a page of the Lync Server Control Panel will cause the first item in the top navigation bar to disappear:</span></span>

  - <span data-ttu-id="c12d7-548">フランス語版のページ "Féderation et accès externe" で、"Partenaires d'accès XMPP" がクリックされると、"項目" Stratégie externe fédérés "が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-548">In the French of version, on the page "Féderation et accès externe," the item "Stratégie d'accès externe" will disappear when "Partenaires fédérés XMPP" is clicked.</span></span>

  - <span data-ttu-id="c12d7-549">ドイツ語版の [クライアント] ページで、"Pushbenachrichtigungskonfiguration" がクリックされると、"Clientversionskonfiguration" 項目が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-549">In the German version, on the "Clients" page, the item "Clientversionskonfiguration" disappears when "Pushbenachrichtigungskonfiguration" is clicked.</span></span>

  - <span data-ttu-id="c12d7-550">ロシア語版の "Конфигурациясети" ページでは、"Маршрутрегиона" がクリックされると、項目 "Глобально" が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-550">In the Russian version, on "Конфигурация сети" page, the item "Глобально" disappears when "Маршрут региона" is clicked.</span></span>

<span data-ttu-id="c12d7-551">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-551">**Workaround:**</span></span>

<span data-ttu-id="c12d7-552">この問題を回避するには、ブラウザーで Lync Server コントロールパネルのページを更新します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-552">To work around this issue, refresh the page of the Lync Server Control Panel in your browser.</span></span> <span data-ttu-id="c12d7-553">ページは、上部のナビゲーションバーに表示されているすべてのアイテムと共にブラウザーに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-553">The page will load in the browser with all of the items in the top navigation bar displayed.</span></span>

</div>

</div>

<div>

## <a name="address-book"></a><span data-ttu-id="c12d7-554">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="c12d7-554">Address Book</span></span>

<div>

## <a name="indexing-in-the-address-book-does-not-work-as-expected-in-some-languages"></a><span data-ttu-id="c12d7-555">一部の言語で、アドレス帳のインデックス処理が予期したとおりに機能しない</span><span class="sxs-lookup"><span data-stu-id="c12d7-555">Indexing in the Address Book does not work as expected in some languages</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="c12d7-556">このセクションの情報は Lync Server 2013 の累積的な更新プログラム: 2013 年 2 月に関係します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-556">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="c12d7-557">ユーザーのプロパティにインデックス付きフィールドが含まれており、そのフィールドにインデックスを作成できない文字しか含まれていない場合、そのユーザーはアドレス帳で実行された検索には表示されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-557">If a user’s properties contain an indexed field, and that field contains only characters that cannot be indexed, then the user will not appear in searches performed in the Address Book.</span></span>

<span data-ttu-id="c12d7-558">次の文字とロケールのインデックスを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-558">The following characters and locales cannot be indexed:</span></span>

  - <span data-ttu-id="c12d7-559">大文字のキリル文字、ギリシャ文字、およびアルメニア文字</span><span class="sxs-lookup"><span data-stu-id="c12d7-559">Upper-case Cyrillic, Greek, and Armenian characters</span></span>

  - <span data-ttu-id="c12d7-560">大文字アクセント記号付き文字</span><span class="sxs-lookup"><span data-stu-id="c12d7-560">Upper-case accented characters</span></span>

  - <span data-ttu-id="c12d7-561">タイ語</span><span class="sxs-lookup"><span data-stu-id="c12d7-561">Thai</span></span>

  - <span data-ttu-id="c12d7-562">ラオス</span><span class="sxs-lookup"><span data-stu-id="c12d7-562">Lao</span></span>

  - <span data-ttu-id="c12d7-563">ミャンマー</span><span class="sxs-lookup"><span data-stu-id="c12d7-563">Myanmar</span></span>

  - <span data-ttu-id="c12d7-564">バナー</span><span class="sxs-lookup"><span data-stu-id="c12d7-564">Devanagari</span></span>

  - <span data-ttu-id="c12d7-565">語</span><span class="sxs-lookup"><span data-stu-id="c12d7-565">Ethiopic</span></span>

  - <span data-ttu-id="c12d7-566">語</span><span class="sxs-lookup"><span data-stu-id="c12d7-566">Tibetan</span></span>

  - <span data-ttu-id="c12d7-567">ベンガル語</span><span class="sxs-lookup"><span data-stu-id="c12d7-567">Bengali</span></span>

  - <span data-ttu-id="c12d7-568">グジャラート語</span><span class="sxs-lookup"><span data-stu-id="c12d7-568">Gujarati</span></span>

  - <span data-ttu-id="c12d7-569">テルグ語</span><span class="sxs-lookup"><span data-stu-id="c12d7-569">Telugu</span></span>

  - <span data-ttu-id="c12d7-570">その他のすべてのインド系言語スクリプト</span><span class="sxs-lookup"><span data-stu-id="c12d7-570">All other Indic scripts</span></span>

</div>

</div>

<div>

## <a name="lync-web-app-web-scheduler-and-web-components"></a><span data-ttu-id="c12d7-571">Lync Web App、Web Scheduler、Web コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c12d7-571">Lync Web App, Web Scheduler, and Web components</span></span>

<div>

## <a name="language-fallback-for-certain-languages-in-lync-web-scheduler-dial-in-join-launcher-persistent-chat-room-management-and-octab-might-not-work-as-expected"></a><span data-ttu-id="c12d7-572">Lync Web Scheduler、ダイヤルイン、参加起動ツール、常設チャットルーム管理、および OCTab の一部の言語の言語のフォールバックは、期待どおりに動作しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-572">Language fallback for certain languages in Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab might not work as expected</span></span>

<span data-ttu-id="c12d7-573">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-573">**Issue:**</span></span>

<span data-ttu-id="c12d7-574">Web ブラウザーでニュートラルロケールを選択する場合 (Internet Explorer の場合) たとえば、 \[ \] 言語、スクリプト、ロケール ("ノルウェー語、ブークモール (ノルウェー語) NB-いいえ" など) を指定しない言語名は、 \[ \] Lync web Scheduler、ダイヤルイン、参加起動ツール、常設チャットルーム管理、および octab の特定の言語に対して予期しない表示動作を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-574">When selecting a neutral locale in a web browser (in Internet Explorer, for example, the language name without further specification, like "Norwegian \[no\]") instead of a locale specifying language, script and locale (such as "Norwegian, Bokmål (Norway) \[nb-NO\]") might lead to unexpected display behavior for certain languages in Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab.</span></span> <span data-ttu-id="c12d7-575">たとえば、次のいずれかの言語が選択されている場合、ユーザーに英語のページが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-575">For example, users might see the English page when one of the following languages is selected:</span></span>

  - <span data-ttu-id="c12d7-576">ノルウェー語</span><span class="sxs-lookup"><span data-stu-id="c12d7-576">Norwegian</span></span>

  - <span data-ttu-id="c12d7-577">ポルトガル語</span><span class="sxs-lookup"><span data-stu-id="c12d7-577">Portuguese</span></span>

  - <span data-ttu-id="c12d7-578">セルビア語</span><span class="sxs-lookup"><span data-stu-id="c12d7-578">Serbian</span></span>

<span data-ttu-id="c12d7-579">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-579">**Workaround:**</span></span>

<span data-ttu-id="c12d7-580">ニュートラルロケールの言語を選択する場合は、ブラウザーの [言語設定] ボックスの一覧で、特定のロケール (スクリプトおよび国コードを含む) の言語も追加であることを必ず確認してください。</span><span class="sxs-lookup"><span data-stu-id="c12d7-580">If you want to select a language with a neutral locale, always make sure that you also add the language with a specific locale (with script and/or country code) as an additional language in your browser's language preference list.</span></span>

</div>

<div>

## <a name="there-is-limited-support-for-azeri-and-uzbek-locales-when-using-lync-web-scheduler-dial-in-join-launcher-persistent-chat-room-management-and-octab-in-some-web-browsers"></a><span data-ttu-id="c12d7-581">Lync Web Scheduler、ダイヤルイン、参加起動ツール、常設チャットルーム管理、および一部の Web ブラウザーでの OCTab を使用している場合、アゼルバイジャン語とウズベク語のサポートは制限されています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-581">There is limited support for Azeri and Uzbek locales when using Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab in some web browsers</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="c12d7-582">このセクションの情報は Lync Server 2013 の累積的な更新プログラム: 2013 年 2 月に関係します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-582">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="c12d7-583">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-583">**Issue:**</span></span>

<span data-ttu-id="c12d7-584">Internet Explorer 8 または Internet Explorer 9 を使用して、ブラウザーの言語をアゼルバイジャン語 (ラテン) またはウズベク語 (ラテン) に設定すると、ダイヤルインと参加起動ツールのページは、英語またはブラウザーで設定した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-584">When you use Internet Explorer 8 or Internet Explorer 9, and set the browser language to Azeri (Latin) or Uzbek (Latin), the Dial-in and Join Launcher pages will be displayed in English or the preferred language set in the browser.</span></span>

<span data-ttu-id="c12d7-585">Firefox または Chrome ブラウザーを使用しているときに、ブラウザーの言語を [アゼルバイジャン (ラテン)] または [ウズベク語 (ラテン)] に設定すると、Lync Web App、Lync Web Scheduler、および RGS OCTab が、英語で表示されるか、ブラウザーの優先言語セットとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-585">When you use Firefox or Chrome browsers, and you set the browser language to Azeri (Latin) or Uzbek (Latin), the Lync Web App, Lync Web Scheduler, and RGS OCTab will be shown in English or the preferred language set for the browser.</span></span>

<span data-ttu-id="c12d7-586">Safari ブラウザーでは、ウズベク語 (ラテン) ロケールはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-586">The Uzbek (Latin) locale is not supported in the Safari browser.</span></span>

<span data-ttu-id="c12d7-587">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-587">**Workaround:**</span></span>

<span data-ttu-id="c12d7-588">この問題の回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-588">There is not workaround for these issues.</span></span>

</div>

</div>

<div>

## <a name="the-drop-down-arrow-is-missing-for-join-meeting-from-list-in-the-romanian-version-of-lync-web-app"></a><span data-ttu-id="c12d7-589">ルーマニア語版の Lync Web App の [会議に参加する] リストのドロップダウン矢印が表示されない</span><span class="sxs-lookup"><span data-stu-id="c12d7-589">The drop-down arrow is missing for "Join meeting from" list in the Romanian version of Lync Web App</span></span>

<span data-ttu-id="c12d7-590">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-590">**Issue:**</span></span>

<span data-ttu-id="c12d7-591">ルーマニア語版の Lync Web App を使用しているユーザーが次の手順を実行すると、ドロップダウンリストに **会議に参加** するためのドロップダウン矢印が表示されません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-591">When a user who is using the Romanian version of Lync Web App performs the following steps, the drop-down arrow is not displayed for **Join meeting** in drop-down list:</span></span>

1.  <span data-ttu-id="c12d7-592">[**全般**] タブの [**このコンピューター上でパスワードを記憶** する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-592">Select **Remember me on this computer** on the **General** tab.</span></span>

2.  <span data-ttu-id="c12d7-593">[ **電話** ] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c12d7-593">Select the **Phone** tab.</span></span>

3.  <span data-ttu-id="c12d7-594">[ **会議に参加** する] のドロップダウンリストをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12d7-594">Click the drop-down list for **Join meeting from**.</span></span>
    
    <span data-ttu-id="c12d7-595">ユーザーには、既定の **Lync Web App** よりも多くのオプションが含まれていることを示す矢印が表示されません。これには、 **オーディオに参加しない** (ルーマニア語、"ニュー se asociaža la componenta Audio") と **新しい番号**"(ルーマニア語で" Număr nou ") が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-595">Users will not see an arrow that indicates that there are more options than the default **Lync Web App**, which include: **Don't join audio** (in Romanian, "Nu se asociaža la componenta audio") and **New number**" (in Romanian, "Număr nou").</span></span>

<span data-ttu-id="c12d7-596">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-596">**Workaround:**</span></span>

<span data-ttu-id="c12d7-597">このドロップダウンリストの矢印が表示されていない場合でも、ユーザーは既定値をクリックして、リスト内の追加の設定を選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-597">Even though the arrow for this drop-down list is not displayed, users can still select the additional settings in the list by clicking on the default value.</span></span>

</div>

<div>

## <a name="when-using-the-turkish-version-of-lync-web-scheduler-a-meeting-cannot-be-saved-when-using-the-people-i-choose-option-under-who-is-a-presenter"></a><span data-ttu-id="c12d7-598">トルコ語版の Lync Web Scheduler を使用している場合、[発表者になる人] の下にある [選択したユーザー] オプションを使用すると、会議を保存できません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-598">When using the Turkish version of Lync Web Scheduler, a meeting cannot be saved when using the "People I choose" option under "Who is a presenter"</span></span>

<span data-ttu-id="c12d7-599">**点**</span><span class="sxs-lookup"><span data-stu-id="c12d7-599">**Issue:**</span></span>

<span data-ttu-id="c12d7-600">トルコ語版の Lync Web Scheduler で会議を作成または編集している場合、[発表者になるユーザー] の下の [選択したユーザー] オプションはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-600">When creating or editing a meeting in the Turkish version of the Lync Web Scheduler, the option "People I choose" under "Who is a presenter" is not supported.</span></span> <span data-ttu-id="c12d7-601">このオプションが選択されている場合、会議を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-601">When this option is selected, the meeting can't be saved.</span></span> <span data-ttu-id="c12d7-602">代わりに、1人以上のユーザーが発表者を作成できないことを示すエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-602">Instead, an error message appears, indicating that one or more people cannot be made presenters.</span></span>

<span data-ttu-id="c12d7-603">**ところ**</span><span class="sxs-lookup"><span data-stu-id="c12d7-603">**Workaround:**</span></span>

<span data-ttu-id="c12d7-604">この問題を回避するために、ユーザーは、"社内のユーザー" の既定のオプション、または [開催者のみ] や [社外のユーザーを含むすべてのユーザー] などの任意の選択肢を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-604">To work around this issue, users can use the default option of "People from my company," or any other choice, such as "Only Organizer" or "Everyone including people outside of my company."</span></span> <span data-ttu-id="c12d7-605">開催者は、会議に参加した後で、後でユーザーを適切なロールに降格または昇格させることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-605">The organizer can demote or promote people to their correct roles later, after they have joined the meeting.</span></span>

<span data-ttu-id="c12d7-606">または、別の言語を理解しているユーザーは、ブラウザーでの言語の選択を、サポートされている他の43言語のいずれかに変更して、[選択したユーザー] オプションを使用しようとすることができます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-606">Alternatively, users who understand another language can change the language selection in their browser to one of the other 43 supported languages and attempt to use the “People I choose” option.</span></span>

</div>

</div>

<span id="Copyright"></span>

<div>

## <a name="copyright"></a><span data-ttu-id="c12d7-607">著作</span><span class="sxs-lookup"><span data-stu-id="c12d7-607">Copyright</span></span>

<span data-ttu-id="c12d7-608">このドキュメントでは、最終的な商用リリースの前に実質的に変更される可能性があるソフトウェア製品の暫定的なリリースをサポートしています。また、Microsoft Corporation の機密情報でもあります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-608">This document supports a preliminary release of a software product that may be changed substantially prior to final commercial release, and is the confidential and proprietary information of Microsoft Corporation.</span></span> <span data-ttu-id="c12d7-609">この情報は、受信者と Microsoft との間の非開示契約に基づいて公開されます。</span><span class="sxs-lookup"><span data-stu-id="c12d7-609">It is disclosed pursuant to a non-disclosure agreement between the recipient and Microsoft.</span></span> <span data-ttu-id="c12d7-610">このドキュメントは、情報提供のみを目的として提供されています。このドキュメントでは、Microsoft は明示または黙示のいずれの保証も行いません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-610">This document is provided for informational purposes only and Microsoft makes no warranties, either express or implied, in this document.</span></span> <span data-ttu-id="c12d7-611">このドキュメントに記載されている情報 (URL などのインターネット web サイトへの参照を含む) は、予告なしに変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-611">Information in this document, including URL and other Internet website references, is subject to change without notice.</span></span> <span data-ttu-id="c12d7-612">このドキュメントの使用、またはこのドキュメントの使用による結果のすべてのリスクは、ユーザーに残ります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-612">The entire risk of the use or the results from the use of this document remains with the user.</span></span> <span data-ttu-id="c12d7-613">特に記載がない限り、ここに記載されている会社、組織、製品、ドメイン名、メールアドレス、ロゴ、人物、場所、およびイベントは架空のものです。</span><span class="sxs-lookup"><span data-stu-id="c12d7-613">Unless otherwise noted, the companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted in examples herein are fictitious.</span></span> <span data-ttu-id="c12d7-614">実際の会社、組織、製品、ドメイン名、メールアドレス、ロゴ、人物、場所、またはイベントに関連するものではありません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-614">No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.</span></span> <span data-ttu-id="c12d7-615">すべての該当する著作権法を遵守することは、ユーザーにとっての責任となります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-615">Complying with all applicable copyright laws is the responsibility of the user.</span></span> <span data-ttu-id="c12d7-616">著作権の下にある権利を制限することなく、このドキュメントの一部は、Microsoft Corporation の書面による許可なしに、どのような形でも、または何らかの方法 (電子的、機械的、複写、記録など) または任意の目的で送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-616">Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.</span></span>

<span data-ttu-id="c12d7-617">Microsoft には、このドキュメントの内容について、特許、特許申請、商標、著作権、またはその他の知的財産権が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="c12d7-617">Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document.</span></span> <span data-ttu-id="c12d7-618">Microsoft の書面によるライセンス契約で明示的に記載されている場合を除き、このドキュメントの提供により、これらの特許、商標、著作権、またはその他の知的財産権の許諾を得ることはできません。</span><span class="sxs-lookup"><span data-stu-id="c12d7-618">Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.</span></span>

<span data-ttu-id="c12d7-619">© 2012 Microsoft Corporation。</span><span class="sxs-lookup"><span data-stu-id="c12d7-619">© 2012 Microsoft Corporation.</span></span> <span data-ttu-id="c12d7-620">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="c12d7-620">All rights reserved.</span></span>

<span data-ttu-id="c12d7-621">Microsoft、Windows、Windows Live、Active Directory、Internet Explorer、MSN、Outlook、および SQL Server は、米国およびその他の国/地域で、Microsoft Corporation の登録商標または商標です。</span><span class="sxs-lookup"><span data-stu-id="c12d7-621">Microsoft, Windows, Windows Live, Active Directory, Internet Explorer, MSN, Outlook, and SQL Server are either registered trademarks or trademarks of Microsoft Corporation in the United States and/or other countries/regions.</span></span>

<span data-ttu-id="c12d7-622">その他のすべての商標は、各所有者の財産権を持っています。</span><span class="sxs-lookup"><span data-stu-id="c12d7-622">All other trademarks are property of their respective owners.</span></span>

<span data-ttu-id="c12d7-623"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c12d7-623"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

