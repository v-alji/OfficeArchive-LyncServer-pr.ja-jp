---
title: 'Lync Server 2013: バックアップ サービスを使用した会議コンテンツの復元'
description: 'Lync Server 2013: バックアップサービスを使用して会議の内容を復元します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442545"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="b3e46-103">Lync Server 2013 でのバックアップ サービスを使用した会議コンテンツの復元</span><span class="sxs-lookup"><span data-stu-id="b3e46-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3e46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3e46-104">

<span> </span></span></span>

<span data-ttu-id="b3e46-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b3e46-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b3e46-106">フロントエンドプールのファイルストアに保存されている会議情報が利用できなくなった場合。</span><span class="sxs-lookup"><span data-stu-id="b3e46-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="b3e46-107">この情報を復元すると、プールをホームにしているユーザーが会議データを保持するようになります。</span><span class="sxs-lookup"><span data-stu-id="b3e46-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="b3e46-108">会議データを紛失したフロントエンドプールが別のフロントエンドプールとペアリングされている場合は、バックアップサービスを使ってデータを復元することができます。</span><span class="sxs-lookup"><span data-stu-id="b3e46-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="b3e46-109">また、プール全体で障害が発生し、ユーザーがバックアッププールにフェールオーバーしなければならない場合は、このタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3e46-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="b3e46-110">これらのユーザーが元のプールにフェールバックされた場合は、この手順を使用して、会議のコンテンツを元のプールにもコピーし直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3e46-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="b3e46-111">Pool1 が Pool2 とペアリングされていることを前提としていますが、Pool1 の会議データは失われます。</span><span class="sxs-lookup"><span data-stu-id="b3e46-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="b3e46-112">次のコマンドレットを使用して、バックアップサービスを呼び出して内容を復元できます。</span><span class="sxs-lookup"><span data-stu-id="b3e46-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="b3e46-113">会議の内容の復元には、サイズによっては時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3e46-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="b3e46-114">プロセスの状態を確認するには、次のコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3e46-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="b3e46-115">プロセスは、このコマンドレットがデータ会議モジュールの安定した状態の値を返すときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3e46-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="b3e46-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3e46-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

