---
title: Lync Server 2010 サービスを停止する
description: Lync Server 2010 サービスを停止します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Stop Lync Server 2010 services
ms:assetid: bbb29565-819c-4f6f-a222-22494e56e91a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721863(v=OCS.15)
ms:contentKeyID: 49733796
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 668c3af0e37823c32fb59dfcc9af92fa3eff3c63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438737"
---
# <a name="stop-lync-server-2010-services"></a><span data-ttu-id="92c2c-103">Lync Server 2010 サービスを停止する</span><span class="sxs-lookup"><span data-stu-id="92c2c-103">Stop Lync Server 2010 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92c2c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92c2c-104">

<span> </span></span></span>

<span data-ttu-id="92c2c-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="92c2c-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="92c2c-106">Lync Server コントロールパネルを使用すると、特定のコンピューターで実行されているすべての Lync Server 2010 サービスを開始または停止したり、特定の Lync Server 2010 サービスを開始または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="92c2c-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2010 services running on a specific computer or to start or stop a specific Lync Server 2010 service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="92c2c-107">コンピューター上のすべての Lync Server サービスを開始または停止するには</span><span class="sxs-lookup"><span data-stu-id="92c2c-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="92c2c-108">[Lync Server コントロール パネル] を開きます。</span><span class="sxs-lookup"><span data-stu-id="92c2c-108">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="92c2c-109">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-109">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

3.  <span data-ttu-id="92c2c-110">[ **状態** ] ページで、必要に応じて一覧を並べ替えて検索するか、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-110">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

4.  <span data-ttu-id="92c2c-111">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-111">Click **Action**.</span></span>

5.  <span data-ttu-id="92c2c-112">[ **すべてのサービスの開始** ] または [ **すべてのサービスの停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-112">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="92c2c-113">特定のサービスを開始または停止するには</span><span class="sxs-lookup"><span data-stu-id="92c2c-113">To start or stop a specific service</span></span>

1.  <span data-ttu-id="92c2c-114">[Lync Server コントロール パネル] を開きます。</span><span class="sxs-lookup"><span data-stu-id="92c2c-114">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="92c2c-115">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-115">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

3.  <span data-ttu-id="92c2c-116">[ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-116">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

4.  <span data-ttu-id="92c2c-117">[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-117">Click **Properties**.</span></span>

5.  <span data-ttu-id="92c2c-118">必要に応じてサービスの一覧を並べ替え、開始または停止するサービスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-118">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

6.  <span data-ttu-id="92c2c-119">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-119">Click **Action**.</span></span>

7.  <span data-ttu-id="92c2c-120">[ **サービスの開始** ] または [ **サービスの停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-120">Click **Start service** or **Stop service**.</span></span>

8.  <span data-ttu-id="92c2c-121">[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92c2c-121">Click **Close**.</span></span>

<span data-ttu-id="92c2c-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92c2c-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

