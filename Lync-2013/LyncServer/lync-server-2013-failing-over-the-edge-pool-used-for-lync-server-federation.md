---
title: 'Lync Server 2013: Lync Server フェデレーションに使用するエッジ プールのフェールオーバー'
description: 'Lync Server 2013: Lync Server フェデレーションに使用されるエッジプールをフェールオーバーします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for Lync Server federation
ms:assetid: 5c9da0f2-7429-40bb-bb3c-5cc4ecb5a13d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688071(v=OCS.15)
ms:contentKeyID: 49733665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1e7e13ccd35a653d38174f55ace9dc6637ded04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398469"
---
# <a name="failing-over-the-edge-pool-used-for-lync-server-federation-in-lync-server-2013"></a><span data-ttu-id="2c571-103">Lync Server 2013 での Lync Server フェデレーションに使用するエッジ プールのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="2c571-103">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c571-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c571-104">

<span> </span></span></span>

<span data-ttu-id="2c571-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="2c571-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="2c571-106">Lync Server フェデレーションが構成されている Edge プールが停止している場合は、フェデレーションが機能するために別のエッジプールを使用するようにフェデレーションを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c571-106">If the Edge pool where you have Lync Server federation configured goes down, you must change federation to use a different Edge pool for federation to work.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-lync-server-federation"></a><span data-ttu-id="2c571-107">Lync Server Federation に使用されるエッジプールのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="2c571-107">Failing Over the Edge Pool Used for Lync Server Federation</span></span>

1.  <span data-ttu-id="2c571-108">フロントエンドサーバーで、[トポロジビルダー] を開きます。</span><span class="sxs-lookup"><span data-stu-id="2c571-108">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="2c571-109">[ **Edge プール**] を展開して、フェデレーション用に現在構成されているエッジサーバープールまたはエッジサーバープールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-109">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="2c571-110">[ **プロパティの編集**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="2c571-110">Select **Edit properties**.</span></span>

2.  <span data-ttu-id="2c571-111">[ **プロパティの編集** ] の [ **全般**] で、[ **このエッジプールに対してフェデレーションを有効にする (ポート 5061)**] をオフにします。</span><span class="sxs-lookup"><span data-stu-id="2c571-111">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="2c571-112">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-112">Click **OK**.</span></span>

3.  <span data-ttu-id="2c571-113">[ **Edge プール**] を展開して、フェデレーションに使用するエッジサーバーまたはエッジサーバープールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-113">Expand **Edge pools**, then right click the Edge server or Edge server pool that you now want to use for Federation.</span></span> <span data-ttu-id="2c571-114">[ **プロパティの編集**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="2c571-114">Select **Edit properties**.</span></span>

4.  <span data-ttu-id="2c571-115">[ **プロパティの編集** ] の [ **全般**] で、[ **このエッジプールに対してフェデレーションを有効にする (ポート 5061)**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c571-115">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="2c571-116">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-116">Click **OK**.</span></span>

5.  <span data-ttu-id="2c571-117">[ **アクション**] をクリックし、[ **トポロジ**] を選択し、[ **発行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c571-117">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="2c571-118">**トポロジの発行** を求められたら、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-118">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="2c571-119">発行が完了したら、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-119">When the Publish is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="2c571-120">エッジサーバーで、Lync Server 展開ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c571-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="2c571-121">[ **Lync Server System のインストールまたは更新**] をクリックし、[ **lync Server コンポーネントのセットアップまたは削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-121">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="2c571-122">[ **実行] をもう一度** クリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-122">Click **Run Again**.</span></span>

7.  <span data-ttu-id="2c571-123">Lync Server コンポーネントのセットアップで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c571-123">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="2c571-124">概要画面には、実行中の操作が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c571-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="2c571-125">展開が完了したら、[ **ログの表示** ] をクリックして、利用可能なログファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="2c571-125">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="2c571-126">[ **完了** ] をクリックして展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="2c571-126">Click **Finish** to complete the deployment.</span></span>
    
    <span data-ttu-id="2c571-127">問題のあるエッジプールを含むサイトにまだ実行されているフロントエンドサーバーが含まれている場合は、これらのフロントエンドプールの Web 会議サービスと A/V 会議サービスを更新して、まだ実行中のリモートサイトでエッジプールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c571-127">If the site containing the failed Edge pool contains Front End Servers that are still running, you must update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to use an Edge pool in a remote site that is still running.</span></span> <span data-ttu-id="2c571-128">詳細については、「 [Lync Server 2013 でフロントエンドプールに関連付けられているエッジプールを変更する](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c571-128">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2c571-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c571-129">See Also</span></span>


[<span data-ttu-id="2c571-130">Lync Server 2013 での、XMPP フェデレーションに使用するエッジ プールのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="2c571-130">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  
[<span data-ttu-id="2c571-131">Lync Server 2013 での Lync Server フェデレーションまたは XMPP フェデレーションに使用するエッジ プールのフェールバック</span><span class="sxs-lookup"><span data-stu-id="2c571-131">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)  


[<span data-ttu-id="2c571-132">Lync Server 2013 でのエッジ サーバーの障害復旧</span><span class="sxs-lookup"><span data-stu-id="2c571-132">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="2c571-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c571-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

