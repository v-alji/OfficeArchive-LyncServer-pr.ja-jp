---
title: 'Lync Server 2013: ミラー化データベースのフェールオーバー'
description: 'Lync Server 2013: ミラー化されたデータベースのフェールオーバー'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a mirrored database
ms:assetid: 70185476-e3d4-440a-9316-fa24b226343e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204991(v=OCS.15)
ms:contentKeyID: 48184450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc7c401157c79762f674721ca717296c0fe502db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428294"
---
# <a name="failing-over-a-mirrored-database-in-lync-server-2013"></a><span data-ttu-id="7f86d-103">Lync Server 2013 でのミラー化データベースのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="7f86d-103">Failing over a mirrored database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f86d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f86d-104">

<span> </span></span></span>

<span data-ttu-id="7f86d-105">_**最終更新日:** 2014-03-14_</span><span class="sxs-lookup"><span data-stu-id="7f86d-105">_**Topic Last Modified:** 2014-03-14_</span></span>

<span data-ttu-id="7f86d-106">バックエンドデータベースが監視との同期ミラーリングを使用するように構成されている場合、フェールオーバーは自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f86d-106">If you have configured your back-end database to use synchronized mirroring with a witness, failover is automatic.</span></span> <span data-ttu-id="7f86d-107">ミラーリングを監視せずに同期ミラーリングを構成した場合は、次の手順を使用してデータベースのフェールオーバーとフェールバックを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7f86d-107">If you have configured synchronized mirroring without a witness, you can use the following procedures to failover and failback your database.</span></span> <span data-ttu-id="7f86d-108">また、監視を構成している場合でも、これらの手順を使用して手動でデータベースのフェールオーバーとフェールバックを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7f86d-108">You can also use these procedures to manually failover and failback your databases even if you have configured a witness.</span></span>

<div>

## <a name="to-fail-over-your-back-end-database"></a><span data-ttu-id="7f86d-109">バックエンドデータベースをフェールオーバーするには</span><span class="sxs-lookup"><span data-stu-id="7f86d-109">To fail over your back-end database</span></span>

1.  <span data-ttu-id="7f86d-110">フェールオーバーする前に、次のコマンドレットを入力して、どのバックエンドデータベースがプリンシパルであり、ミラーであるかを判断します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-110">Before failing over, determine which back-end database is the principal and which is the mirror by typing the following cmdlet:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType User

2.  <span data-ttu-id="7f86d-111">このプールで中央管理ストアがホストされている場合は、次のコマンドレットを入力して、どのプリンシパルが中央管理ストアのミラーであるかを判断します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-111">If the Central Management store is hosted in this pool, type the following cmdlet to determine which is the principal and which is the mirror for the Central Management store:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt

3.  <span data-ttu-id="7f86d-112">ユーザーデータベースのフェールオーバーを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-112">Perform the failover of the user database:</span></span>
    
      - <span data-ttu-id="7f86d-113">プライマリに障害が発生し、ミラーにフェイルオーバーする場合は、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-113">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="7f86d-114">ミラーが失敗し、プライマリにフェイルオーバーする場合は、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-114">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal primary -Verbose

4.  <span data-ttu-id="7f86d-115">プールで中央管理サーバーがホストされている場合は、中央管理ストアのフェールオーバーを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-115">If the pool hosts the Central Management Server, perform the failover of the Central Management store.</span></span>
    
      - <span data-ttu-id="7f86d-116">プライマリに障害が発生し、ミラーにフェイルオーバーする場合は、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-116">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="7f86d-117">ミラーが失敗し、プライマリにフェイルオーバーする場合は、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f86d-117">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal primary -Verbose

<span data-ttu-id="7f86d-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f86d-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

