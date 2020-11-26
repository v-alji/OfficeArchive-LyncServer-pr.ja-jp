---
title: アーカイブ サーバーと監視サーバーの移行
description: アーカイブと監視サーバーの移行。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443749"
---
# <a name="migrating-archiving-and-monitoring-servers"></a><span data-ttu-id="6fff1-103">アーカイブ サーバーと監視サーバーの移行</span><span class="sxs-lookup"><span data-stu-id="6fff1-103">Migrating Archiving and Monitoring servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fff1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fff1-104">

<span> </span></span></span>

<span data-ttu-id="6fff1-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="6fff1-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="6fff1-106">Lync Server 2010 環境でアーカイブサーバーと監視サーバーを展開した場合、フロントエンドプールを移行した後で、これらのサーバーを Lync Server 2013 環境に展開できます。</span><span class="sxs-lookup"><span data-stu-id="6fff1-106">If you deployed Archiving Server and Monitoring Server in your Lync Server 2010 environment, you can deploy these servers in your Lync Server 2013 environment after you migrate your Front End pools.</span></span> <span data-ttu-id="6fff1-107">ただし、アーカイブと監視の機能が組織にとって重要である場合は、移行を行う前に、アーカイブと監視を Lync Server 2013 パイロットプールに追加して、移行プロセス中に機能を利用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fff1-107">If archiving and monitoring functionality are critical to your organization, however, you should add archiving and monitoring to your Lync Server 2013 pilot pool before you migrate so that the functionality is available during the migration process.</span></span>

<span data-ttu-id="6fff1-108">移行プロセス中にアーカイブと監視機能が必要な場合は、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="6fff1-108">If you want archiving and monitoring functionality during the migration process, keep the following considerations in mind:</span></span>

  - <span data-ttu-id="6fff1-109">データのアーカイブとデータの監視は、Lync Server 2013 の展開には移行されません。</span><span class="sxs-lookup"><span data-stu-id="6fff1-109">Archiving data and monitoring data are not moved to the Lync Server 2013 deployment.</span></span> <span data-ttu-id="6fff1-110">従来の環境を廃止する前にバックアップしたデータは、Lync Server 2010 環境でのアクティビティの履歴となります。</span><span class="sxs-lookup"><span data-stu-id="6fff1-110">The data you back up prior to decommissioning the legacy environment will be your history of activity in the Lync Server 2010 environment.</span></span>

  - <span data-ttu-id="6fff1-111">アーカイブサーバーと監視サーバーの Lync Server 2010 バージョンは、Lync Server 2010 フロントエンドプールにのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6fff1-111">The Lync Server 2010 version of Archiving Server and Monitoring Server can be associated only with a Lync Server 2010 Front End pool.</span></span> <span data-ttu-id="6fff1-112">Lync Server 2013 では、アーカイブと監視はサーバーの役割ではなくなりましたが、Lync Server 2013 フロントエンドプールに統合されたサービスです。</span><span class="sxs-lookup"><span data-stu-id="6fff1-112">In Lync Server 2013, Archiving and Monitoring are no longer server roles, but services integrated into the Lync Server 2013 Front End pool.</span></span>

  - <span data-ttu-id="6fff1-113">従来の、および Lync Server 2013 の展開が共存する間、lync server 2010 バージョンのアーカイブサーバーと監視サーバーによって、Lync Server 2010 プールを使っているユーザーのデータが収集されます。</span><span class="sxs-lookup"><span data-stu-id="6fff1-113">During the time that your legacy and Lync Server 2013 deployments coexist, the Lync Server 2010 version of Archiving Server and Monitoring Server gather data for users homed on Lync Server 2010 pools.</span></span> <span data-ttu-id="6fff1-114">Lync Server 2013 でのアーカイブと監視 Lync Server 2013 プールに所属しているユーザーのデータを収集します。</span><span class="sxs-lookup"><span data-stu-id="6fff1-114">Archiving and Monitoring in Lync Server 2013 gather data for users homed on Lync Server 2013 pools.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6fff1-115">新しい Lync Server 2013 パイロットプールで従来のエッジサーバーを使用している場合、移行のフェーズ中に、lync server 2010 バージョンのアーカイブサーバーは、lync server 2010 プールを使っているユーザーのためにデータを収集し続けます。 lync server 2013 プールを使用しているユーザーのデータは、lync server 2013 で収集されます。</span><span class="sxs-lookup"><span data-stu-id="6fff1-115">During the phase of migration when you are still using your legacy Edge server with the new Lync Server 2013 pilot pool, the Lync Server 2010 version of Archiving Server continues to gather data for users homed on Lync Server 2010 pools and Archiving in Lync Server 2013 gathers data for users homed on Lync Server 2013 pools.</span></span>

    
    </div>

  - <span data-ttu-id="6fff1-116">サードパーティのアーカイブと監視ソリューションを Lync Server 2013 のアーカイブと監視と組み合わせて使用する場合は、サードパーティのソリューションと Lync Server 2013 を統合する時期とその方法について、ベンダーにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="6fff1-116">If you use a third-party archiving and monitoring solution in conjunction with Archiving and Monitoring in Lync Server 2013, consult with your vendor about when and how you need to integrate the third-party solution with Lync Server 2013.</span></span>

<span data-ttu-id="6fff1-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fff1-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

