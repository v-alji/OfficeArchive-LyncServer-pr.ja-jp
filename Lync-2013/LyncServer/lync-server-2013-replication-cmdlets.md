---
title: 'Lync Server 2013: レプリケーションコマンドレット'
description: 'Lync Server 2013: レプリケーションコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replication cmdlets
ms:assetid: e0c49601-d2a3-45a1-b05c-26c7ff820708
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415677(v=OCS.15)
ms:contentKeyID: 48185527
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b253176101de61a07630ec141a318dd114776392
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399813"
---
# <a name="replication-cmdlets-in-lync-server-2013"></a><span data-ttu-id="2d7a9-103">Lync Server 2013 のレプリケーションコマンドレット</span><span class="sxs-lookup"><span data-stu-id="2d7a9-103">Replication cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d7a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d7a9-104">

<span> </span></span></span>

<span data-ttu-id="2d7a9-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="2d7a9-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="2d7a9-106">レプリケーションコマンドレットを使用すると、Lync Server のレプリケーションを監視および管理することができます。</span><span class="sxs-lookup"><span data-stu-id="2d7a9-106">The replication cmdlets provide a way for you to both monitor and manage Lync Server replication.</span></span> <span data-ttu-id="2d7a9-107">これらのコマンドレットを使用して、レプリケーション設定を構成できます。レプリケーションの進行状況を監視するにはサーバー上のレプリケーションを手動で強制的に実行します。</span><span class="sxs-lookup"><span data-stu-id="2d7a9-107">You can use these cmdlets to configure replication settings; to monitor replication progress; and to manually force replication on a server.</span></span>

<div>

## <a name="replication-cmdlets"></a><span data-ttu-id="2d7a9-108">レプリケーションコマンドレット</span><span class="sxs-lookup"><span data-stu-id="2d7a9-108">Replication Cmdlets</span></span>

<span data-ttu-id="2d7a9-109">次に、レプリケーションの管理に直接関連するコマンドレットの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="2d7a9-109">The following is a list of cmdlets that relate directly to managing replication:</span></span>

<span data-ttu-id="2d7a9-110">**レプリケート**</span><span class="sxs-lookup"><span data-stu-id="2d7a9-110">**Replication**</span></span>

  - <span></span>  
    <span data-ttu-id="2d7a9-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2d7a9-112">[CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-112">[Invoke-CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2d7a9-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2d7a9-114">[CsReplica を有効にする](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-114">[Enable-CsReplica](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2d7a9-115">[CsReplica のテスト](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-115">[Test-CsReplica](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2d7a9-116">[CsUserReplicatorConfiguration の入手](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-116">[Get-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2d7a9-117">[New-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-117">[New-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2d7a9-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2d7a9-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2d7a9-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2d7a9-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d7a9-120">See Also</span></span>


[<span data-ttu-id="2d7a9-121">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="2d7a9-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="2d7a9-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d7a9-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

