---
title: 通話の記録とエクスペリエンスデータベースの品質を手動で削除する
description: 通話の記録とエクスペリエンスデータベースの品質を手動で消去します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manually purging the call detail recording and Quality of Experience databases
ms:assetid: 3a3a965b-b861-41a4-b9a8-27184d622c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204812(v=OCS.15)
ms:contentKeyID: 48183859
ms.date: 07/07/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c7903431d28bf1a829991ce35c2ee7351168b4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425823"
---
# <a name="manually-purging-the-call-detail-recording-and-quality-of-experience-databases-in-lync-server-2013"></a><span data-ttu-id="1b9e6-103">Lync Server 2013 で通話の記録とエクスペリエンスデータベースの記録を手動で削除する</span><span class="sxs-lookup"><span data-stu-id="1b9e6-103">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1b9e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1b9e6-104">

<span> </span></span></span>

<span data-ttu-id="1b9e6-105">_**最終更新日:** 2014-07-07_</span><span class="sxs-lookup"><span data-stu-id="1b9e6-105">_**Topic Last Modified:** 2014-07-07_</span></span>

<span data-ttu-id="1b9e6-p101">管理者は、データベースから以前のレコードを自動的に削除するように通話詳細記録 (CDR) か QoE (QoE) データベース、またはその両方を構成できます。これは、指定したデータベース (CDR または QoE) で削除が有効になっており、レコードが指定した時間以上、データベース内にあると実行されます。たとえば、毎日、午前 1 時 00 分に、60 日以上経った QoE レコードが QoE データベースから削除されるように、管理者がシステムを構成できます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-p101">Administrators can configure the Call Detail Recording (CDR) and/or the Quality of Experience (QoE) databases to automatically purge old records from the database; this occurs if purging has been enabled for the specified database (CDR or QoE) and if there are any records that have been in the database longer than the specified amount of time. For example, every day at 1:00 AM administrators might configure the system so that QoE records more than 60 days old will be deleted from the QoE database.</span></span>

<span data-ttu-id="1b9e6-108">自動的な消去に加えて、2つの新しいコマンドレット (Invoke-CsCdrDatabasePurge と Invoke-CsQoEDatbasePurge が Microsoft Lync Server 2013 に追加されています。これらのコマンドレットを使用すると、管理者はいつでも CDR と QoE データベースからレコードを手動で削除できます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-108">In addition to that automatic purging, two new cmdlets -- Invoke-CsCdrDatabasePurge and Invoke-CsQoEDatbasePurge -- have been added to Microsoft Lync Server 2013; these cmdlets allow administrators to manually purge records from the CDR and the QoE databases at any time.</span></span> <span data-ttu-id="1b9e6-109">たとえば、CDR データベースから10日以上経過しているすべてのレコードを手動で消去するには、次のようなコマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-109">For example, to manually purge all the records more than 10 days old from the CDR database you can use a command similar to this:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 10

<span data-ttu-id="1b9e6-110">上記のコマンドでは、両方の通話の詳細レコードと、10日以上経過した診断データレコードが atl-sql-001.litwareinc.com の監視データベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-110">In the preceding command both call detail records and diagnostic data records older than 10 days are deleted from the monitoring database on atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="1b9e6-111">(通話の詳細レコードは、ユーザー/セッションレポートです。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-111">(Call detail records are user/session reports.</span></span> <span data-ttu-id="1b9e6-112">診断データレコードは、Lync 2013 などのクライアントアプリケーションによってアップロードされた診断ログです。)</span><span class="sxs-lookup"><span data-stu-id="1b9e6-112">Diagnostic data records are diagnostic logs uploaded by client applications such as Lync 2013.)</span></span>

<span data-ttu-id="1b9e6-113">上に示すように、Invoke-CsCdrDatabasePurge コマンドレットを実行するときは、PurgeCallDetaiDataOlderThanDays と PurgeDiagnosticDataOlderThanDays の両方のパラメーターが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-113">As shown above, when you run the Invoke-CsCdrDatabasePurge cmdlet you must include both the PurgeCallDetaiDataOlderThanDays and the PurgeDiagnosticDataOlderThanDays parameters.</span></span> <span data-ttu-id="1b9e6-114">ただし、これらのパラメーターを同じ値に設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-114">However, these parameters do not have to be set to the same value.</span></span> <span data-ttu-id="1b9e6-115">たとえば、10 日より前の詳細通話記録を削除する一方で、すべての診断データ レコードをデータベースに残すことはできます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-115">For example, it's possible to purge call detail records more than 10 days old and yet, at the same time, leave all the diagnostic data records in the database.</span></span> <span data-ttu-id="1b9e6-116">そのためには、PurgeCallDetailDataOlderThanDays を10、PurgeDiagnosticDataOlderThanDays を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-116">To do that, set PurgeCallDetailDataOlderThanDays to 10 and PurgeDiagnosticDataOlderThanDays to 0.</span></span> <span data-ttu-id="1b9e6-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-117">For example:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 0

<span data-ttu-id="1b9e6-118">既定では、Invoke-CsCdrDatabasePurge を実行するたびに、削除する必要がある各データベース テーブルごとに、以下のようなメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-118">By default, any time you run Invoke-CsCdrDatabasePurge you will see a prompt similar to this one for each database table that must be purged:</span></span>

    Confirm
    Are you sure you want to perform this action?
    Performing operation "Stored procedure: RtcCleanupDiag" on Target "Target SQL Server:atl-sql-001.litwareinc.com\archinst Database: lcscdr".
    [Y] Yes  [A] Yes to All  [N] No  [L] No to All [S] Suspend  [?] Help (default is "Y"):

<span data-ttu-id="1b9e6-p105">データベース削除が実際に行われる前に、Y (はい) または A (すべてはい) を入力する必要があります。これらの確認メッセージを表示しないようにする場合は、Invoke-CsCdrDatabasePurge の呼び出しの最後に以下のパラメーターを追加します。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-p105">You must type either Y (for Yes) or A (for Yes to All) before the database purging will actually take place. If you would prefer to suppress these confirmation prompts, add the following parameter to the end of your call to Invoke-CsCdrDatabasePurge:</span></span>

    -Confirm:$False

<span data-ttu-id="1b9e6-121">例:</span><span class="sxs-lookup"><span data-stu-id="1b9e6-121">For example:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 10 -Confirm:$False

<span data-ttu-id="1b9e6-122">この操作を実行すると、確認メッセージは表示されず、データベースの削除がすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-122">If you do that, confirmation prompts will not be displayed, and database purging will immediately be performed.</span></span>

<span data-ttu-id="1b9e6-123">QoE データベースを削除するには、Invoke-CsQoEDatabasePurge コマンドレットを使用し、削除するレコードの保有期間を (日単位で) 指定します。</span><span class="sxs-lookup"><span data-stu-id="1b9e6-123">To purge the QoE database, use the Invoke-CsQoEDatabasePurge cmdlet and specify the age (in days) of the records to be deleted:</span></span>

    Invoke-CsQoEDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeQoEDataOlderThanDays 10

<span data-ttu-id="1b9e6-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1b9e6-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

