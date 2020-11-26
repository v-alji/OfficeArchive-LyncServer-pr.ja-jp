---
title: 複数のユーザーをパイロットプールに移動する
description: 複数のユーザーをパイロットプールに移動します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438494"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="15984-103">複数のユーザーをパイロットプールに移動する</span><span class="sxs-lookup"><span data-stu-id="15984-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15984-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15984-104">

<span> </span></span></span>

<span data-ttu-id="15984-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="15984-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="15984-106">Lync server 2013 コントロールパネルまたは Lync Server 2013 Management Shell を使用して、lync Server 2010 プールから Lync Server 2013 パイロットプールに複数のユーザーを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="15984-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="15984-107">Lync Server 2013 コントロールパネルを使用して複数のユーザーを移動するには</span><span class="sxs-lookup"><span data-stu-id="15984-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="15984-108">[**Lync Server コントロール パネル**] を開きます。</span><span class="sxs-lookup"><span data-stu-id="15984-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="15984-109">[**ユーザー**]、[検索] の順にクリックして、[**ユーザー検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15984-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="15984-110">Lync Server 2013 プールに移動する2人のユーザーを選びます。</span><span class="sxs-lookup"><span data-stu-id="15984-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="15984-111">この例では、Chen Yang sold と Claus というユーザーを移動します。</span><span class="sxs-lookup"><span data-stu-id="15984-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="15984-112">![ユーザーを特定のレジスタプールに移動する](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "ユーザーを特定のレジスタプールに移動する")</span><span class="sxs-lookup"><span data-stu-id="15984-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="15984-113">[ **アクション** ] メニューで、[ **選択したユーザーをプールに移動**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="15984-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="15984-114">ドロップダウンリストから、Lync Server 2013 プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="15984-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="15984-115">[**アクション**] をクリックし、[**選択されたユーザーをプールに移動**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15984-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="15984-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15984-116">Click OK.</span></span>
    
    <span data-ttu-id="15984-117">![[ユーザーの移動]、[宛先レジストラー pool] ダイアログボックス](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "[ユーザーの移動]、[宛先レジストラー pool] ダイアログボックス")</span><span class="sxs-lookup"><span data-stu-id="15984-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="15984-118">ユーザーの **レジストラー pool** 列に Lync Server 2013 プールが含まれていることを確認します。これは、ユーザーが正常に移動されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="15984-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="15984-119">Lync Server 2013 管理シェルを使用して複数のユーザーを移動するには</span><span class="sxs-lookup"><span data-stu-id="15984-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="15984-120">Lync Server 2013 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="15984-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="15984-121">コマンドラインで、次のように入力し、移動する特定のユーザー名で **User1** と **User2** を置き換えて、 **プールの \_ FQDN** を移行先プールの名前で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="15984-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="15984-122">この例では、ユーザーの Hao Chen と Katie ヨルダンを移動します。</span><span class="sxs-lookup"><span data-stu-id="15984-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="15984-123">![PowerShell Get-CsUser コマンドレットの例](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "PowerShell Get-CsUser コマンドレットの例")</span><span class="sxs-lookup"><span data-stu-id="15984-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="15984-124">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="15984-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="15984-125">これで、 **レジストラープール** id が、前の手順で **プールの \_ FQDN** として指定したプールをポイントするようになります。</span><span class="sxs-lookup"><span data-stu-id="15984-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="15984-126">この id の存在は、ユーザーが正常に移動されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="15984-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="15984-127">「 **User2** が移動されたことを確認する」の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="15984-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="15984-128">![PowerShell Get-UsUser-Identity コマンドレットの出力](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "PowerShell Get-UsUser-Identity コマンドレットの出力")</span><span class="sxs-lookup"><span data-stu-id="15984-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="15984-129">Lync Server 2013 管理シェルを使用してすべてのユーザーを同時に移動するには</span><span class="sxs-lookup"><span data-stu-id="15984-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="15984-130">この例では、すべてのユーザーが Lync Server 2010 プール (pool01.contoso.net) に戻されています。</span><span class="sxs-lookup"><span data-stu-id="15984-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="15984-131">Lync Server 2013 管理シェルを使用して、すべてのユーザーを Lync Server 2013 プール (pool02.contoso.net) に同時に移行します。</span><span class="sxs-lookup"><span data-stu-id="15984-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="15984-132">**Lync Server 2013 管理シェル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="15984-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="15984-133">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="15984-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="15984-134">![PowerShell コマンドレットと結果の管理シェル](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell コマンドレットと結果の管理シェル")</span><span class="sxs-lookup"><span data-stu-id="15984-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="15984-135">次に、パイロットユーザーの1人に対して、 **ユーザーの取得-CsUser** を実行します。</span><span class="sxs-lookup"><span data-stu-id="15984-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="15984-136">各ユーザーの **レジストラープール** id は、前の手順で "プール FQDN" として指定したプールを指すようになりました \_ 。</span><span class="sxs-lookup"><span data-stu-id="15984-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="15984-137">この id の存在は、ユーザーが正常に移動されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="15984-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="15984-138">さらに、Lync Server 2013 コントロールパネルでユーザーの一覧を表示し、[レジストラー Pool] の値が Lync Server 2013 プールを指すようになったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="15984-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="15984-139">![Lync Server 2013 コントロールパネルのユーザーリスト](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 コントロールパネルのユーザーリスト")</span><span class="sxs-lookup"><span data-stu-id="15984-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="15984-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15984-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

