---
title: 'Lync Server 2013: 付録 B: 存続可能ブランチ アプライアンスの管理'
description: 'Lync Server 2013: 付録 B: Survivable Branch アプライアンスの管理'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Appendix B: Managing a Survivable Branch Appliance'
ms:assetid: 2ec9d505-6d39-491c-9524-8cf36866b855
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425797(v=OCS.15)
ms:contentKeyID: 48183773
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e66d97f538ee751d7bf12b0d0f70ff3a3f5576b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439941"
---
# <a name="appendix-b-managing-a-survivable-branch-appliance-in-lync-server-2013"></a><span data-ttu-id="adf6c-103">付録 B: Lync Server 2013 での存続可能ブランチ アプライアンスの管理</span><span class="sxs-lookup"><span data-stu-id="adf6c-103">Appendix B: Managing a Survivable Branch Appliance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adf6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adf6c-104">

<span> </span></span></span>

<span data-ttu-id="adf6c-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="adf6c-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="adf6c-106">このトピックでは、Survivable Branch アプライアンスを管理する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-106">This topic describes the procedures for managing a Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-107">具体的には、Survivable Branch アプライアンスの置き換えと名前の変更方法と、Survivable Branch Appliance が関連付けられている Lync Server 2013 フロントエンドプールの変更方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-107">Specifically, how to replace and rename a Survivable Branch Appliance, and how to change the Lync Server 2013 Front End pool that the Survivable Branch Appliance is associated with.</span></span>

<div>

## <a name="to-replace-a-survivable-branch-appliance"></a><span data-ttu-id="adf6c-108">Survivable Branch アプライアンスを交換するには</span><span class="sxs-lookup"><span data-stu-id="adf6c-108">To Replace a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="adf6c-109">Survivable Branch アプライアンスで、すべての Lync Server 2013 サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-109">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-110">(Survivable Branch Appliance ベンダーのマニュアルをご覧ください。)</span><span class="sxs-lookup"><span data-stu-id="adf6c-110">(See the Survivable Branch Appliance vendor documentation.)</span></span>

2.  <span data-ttu-id="adf6c-111">勧めSurvivable Branch アプライアンスをドメインから削除します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-111">(Recommended) Remove the Survivable Branch Appliance from the domain.</span></span>

3.  <span data-ttu-id="adf6c-112">次の手順に従って、Active Directory ドメインサービス内の Survivable Branch アプライアンスコンピューターオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-112">Delete the Survivable Branch Appliance computer object in Active Directory Domain Services, by following these steps:</span></span>
    
      - <span data-ttu-id="adf6c-113">Enterprise Admins グループのメンバーとしてメンバーサーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-113">Log on to a member server as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="adf6c-114">[ **スタート**] をクリックし、[ **管理ツール**] をクリックして、[ **Active Directory ユーザーとコンピューター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-114">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="adf6c-115">Survivable Branch Appliance オブジェクトを右クリックし、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-115">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

4.  <span data-ttu-id="adf6c-116">Survivable Branch Appliance コンピューターオブジェクトをもう一度追加します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-116">Add the Survivable Branch Appliance computer object again.</span></span> <span data-ttu-id="adf6c-117">(「 [Lync Server 2013 の Active Directory に Survivable Branch Appliance を追加する」を](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)参照してください。)</span><span class="sxs-lookup"><span data-stu-id="adf6c-117">(See [Add a Survivable Branch Appliance to Active Directory in Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md).)</span></span>

5.  <span data-ttu-id="adf6c-118">Active Directory の複製が行われるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="adf6c-118">Wait for Active Directory replication to take place.</span></span>

6.  <span data-ttu-id="adf6c-119">Lync Server 管理シェルを開き、「 **Enable-CSTopology** 機能」と入力します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-119">Open the Lync Server Management Shell, and type **Enable-CSTopology**.</span></span>

7.  <span data-ttu-id="adf6c-120">新しい Survivable Branch Appliance をネットワークに接続し、「 [Survivable Branch appliance またはサーバーを Lync server 2013 に展開](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) する」の手順に従ってください。また、 [lync server 2013-branch site のタスクを使用して、Survivable branch Appliance または server を展開](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-120">Connect the new Survivable Branch Appliance to the network, and follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

</div>

<div>

## <a name="to-rename-a-survivable-branch-appliance"></a><span data-ttu-id="adf6c-121">Survivable Branch アプライアンスの名前を変更するには</span><span class="sxs-lookup"><span data-stu-id="adf6c-121">To Rename a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="adf6c-122">ユーザーをセントラルサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-122">Move users to the central site.</span></span> <span data-ttu-id="adf6c-123">詳細については、「 [ユーザーを Lync Server 2013 の別のプールに移動する](lync-server-2013-move-users-to-another-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-123">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="adf6c-124">Survivable Branch アプライアンスで、すべての Lync Server 2013 サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-124">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-125">(Survivable Branch Appliance ベンダーのマニュアルをご覧ください。)</span><span class="sxs-lookup"><span data-stu-id="adf6c-125">(See the Survivable Branch Appliance vendor documentation.)</span></span>

3.  <span data-ttu-id="adf6c-126">次の手順に従って、トポロジから Survivable Branch アプライアンスを削除します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-126">Remove the Survivable Branch Appliance from the topology, by following these steps:</span></span>
    
      - <span data-ttu-id="adf6c-127">[ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-127">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="adf6c-128">コンソールツリーで、[ **ブランチサイト**] を展開し、Survivable ブランチアプライアンスをクリックして、操作ウィンドウで [ **削除** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-128">In the console tree, expand **Branch Sites**, click the Survivable Branch Appliance, and then click **Delete** on the Action pane.</span></span>

4.  <span data-ttu-id="adf6c-129">Survivable Branch アプライアンスをドメインから削除します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-129">Remove the Survivable Branch Appliance from the domain.</span></span>

5.  <span data-ttu-id="adf6c-130">次の手順に従って、Active Directory 内の Survivable Branch Appliance コンピューターオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-130">Delete the Survivable Branch Appliance computer object in Active Directory, by following these steps:</span></span>
    
      - <span data-ttu-id="adf6c-131">Enterprise Admins グループのメンバーとしてドメインコントローラーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-131">Log on to a domain controller as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="adf6c-132">[ **スタート**] をクリックし、[ **管理ツール**] をクリックして、[ **Active Directory ユーザーとコンピューター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-132">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="adf6c-133">Survivable Branch Appliance オブジェクトを右クリックし、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-133">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

6.  <span data-ttu-id="adf6c-134">Survivable Branch アプライアンスを工場出荷時のデフォルトに復元します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-134">Restore the Survivable Branch Appliance to factory defaults.</span></span> <span data-ttu-id="adf6c-135">(Survivable Branch Appliance ベンダーのマニュアルをご覧ください。)</span><span class="sxs-lookup"><span data-stu-id="adf6c-135">(See the Survivable Branch Appliance vendor documentation.)</span></span>

7.  <span data-ttu-id="adf6c-136">「 [Lync server 2013-セントラルサイトタスクを使用して Survivable Branch appliance またはサーバーを展開](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) する」の手順に従って、「 [lync server 2013 を使用して Survivable branch Appliance またはサーバーを展開する](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-136">Follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

8.  <span data-ttu-id="adf6c-137">名前を変更した Survivable Branch アプライアンスにユーザーを移動します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-137">Move users to the renamed Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-138">詳細については、「 [ユーザーを Lync Server 2013 の別のプールに移動する](lync-server-2013-move-users-to-another-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-138">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

</div>

<div>

## <a name="to-change-the-lync-server-front-end-pool-that-the-survivable-branch-appliance-is-associated-with"></a><span data-ttu-id="adf6c-139">Survivable Branch アプライアンスが関連付けられている Lync Server フロントエンドプールを変更するには</span><span class="sxs-lookup"><span data-stu-id="adf6c-139">To Change the Lync Server Front End Pool that the Survivable Branch Appliance Is Associated With</span></span>

1.  <span data-ttu-id="adf6c-140">Survivable Branch アプライアンスから中央サイトの Lync Server フロントエンドプールにユーザーを移動します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-140">Move users from the Survivable Branch Appliance to the Lync Server Front End pool at the central site.</span></span> <span data-ttu-id="adf6c-141">詳細については、「 [ユーザーを Lync Server 2013 の別のプールに移動する](lync-server-2013-move-users-to-another-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-141">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="adf6c-142">Survivable Branch アプライアンスで、すべての Lync Server サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-142">Stop all Lync Server services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-143">(Survivable Branch Appliance ベンダーのマニュアルをご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="adf6c-143">(See the Survivable Branch Appliance vendor documentation).</span></span>

3.  <span data-ttu-id="adf6c-144">次の手順に従って、Survivable Branch アプライアンスが関連付けられている Lync Server フロントエンドプールを更新します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-144">Update the Lync Server Front End pool that the Survivable Branch Appliance is associated with, by following these steps:</span></span>
    
      - <span data-ttu-id="adf6c-145">[ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-145">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="adf6c-146">[ **ブランチサイト** の展開] を選びます。</span><span class="sxs-lookup"><span data-stu-id="adf6c-146">Expand **Branch Sites**.</span></span>
    
      - <span data-ttu-id="adf6c-147">変更する Survivable Branch Appliance オブジェクトを右クリックして、[**プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-147">Right-click the Survivable Branch Appliance object to modify, and click **Edit Properties**</span></span>
    
      - <span data-ttu-id="adf6c-148">[復元性] で、Survivable Branch アプライアンスが関連付けられる新しいフロントエンドプールを選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-148">Under Resiliency, select the new Front End pool the Survivable Branch Appliance is to be associated to, and then click **Next**.</span></span>
    
      - <span data-ttu-id="adf6c-149">コンソールツリーで、新しい Survivable Branch アプライアンスを右クリックし、[ **Topology**] をクリックして、[ **発行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf6c-149">In the console tree, right-click the new Survivable Branch Appliance, click **Topology**, and then click **Publish**.</span></span>

4.  <span data-ttu-id="adf6c-150">Survivable Branch アプライアンスで、すべての Lync Server サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-150">Restart all Lync Server Services on the Survivable Branch Appliance.</span></span>

5.  <span data-ttu-id="adf6c-151">Survivable Branch アプライアンスをテストしてください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-151">Test the Survivable Branch Appliance.</span></span> <span data-ttu-id="adf6c-152">詳細について [は、「Lync Server 2013 での Survivable Branch Appliance または Server のホームユーザー](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf6c-152">For details, see [Home users on a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span></span>

6.  <span data-ttu-id="adf6c-153">セントラルサイトの Lync Server フロントエンドプールのユーザーを Survivable Branch Appliance に移動します。</span><span class="sxs-lookup"><span data-stu-id="adf6c-153">Move users from the Lync Server Front End pool at the central site to the Survivable Branch Appliance.</span></span>

<span data-ttu-id="adf6c-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adf6c-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

