---
title: 'Lync Server 2013: ネットワークサブネット情報の表示'
description: 'Lync Server 2013: ネットワークサブネット情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network subnet information
ms:assetid: 46f165f2-efe3-4cc1-9fee-a78b7f2ed41e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688044(v=OCS.15)
ms:contentKeyID: 49733636
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 313135c43318817391d54f2fa3e73dd318f7a11f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438856"
---
# <a name="viewing-network-subnet-information-in-lync-server-2013"></a><span data-ttu-id="4f8ca-103">Lync Server 2013 でのネットワークサブネット情報の表示</span><span class="sxs-lookup"><span data-stu-id="4f8ca-103">Viewing network subnet information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f8ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f8ca-104">

<span> </span></span></span>

<span data-ttu-id="4f8ca-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="4f8ca-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="4f8ca-106">次の手順を使用して、ネットワークサブネットを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-106">You can use the following procedure to view a network subnet.</span></span> <span data-ttu-id="4f8ca-107">Lync Server コントロールパネルから、ネットワークサブネットの作成、変更、または削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="4f8ca-108">ネットワークサブネットの作成または変更の詳細については、「 [Lync Server 2013 でネットワークサブネットを作成または変更](lync-server-2013-create-or-modify-network-subnets.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-108">For details about creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<div>

## <a name="to-view-a-network-subnet"></a><span data-ttu-id="4f8ca-109">ネットワークサブネットを表示するには</span><span class="sxs-lookup"><span data-stu-id="4f8ca-109">To view a network subnet</span></span>

1.  <span data-ttu-id="4f8ca-110">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4f8ca-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4f8ca-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4f8ca-113">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **サブネット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-113">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="4f8ca-114">[ **Subnet** ] ページで、表示するサブネットをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-114">On the **Subnet** page, click the subnet that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4f8ca-115">一度に1つのサブネットしか表示できません。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-115">You can only view one subnet at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="4f8ca-116">[ **編集** ] メニューの [ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-116">On the **Edit** menu, click **Show details…**.</span></span>

</div>

<div>

## <a name="viewing-network-subnet-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="4f8ca-117">Windows PowerShell コマンドレットを使用したネットワークサブネット構成情報の表示</span><span class="sxs-lookup"><span data-stu-id="4f8ca-117">Viewing Network Subnet Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="4f8ca-118">ネットワークサブネット情報は、Windows PowerShell と Get-CsNetworkSubnet コマンドレットを使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-118">Network subnet information can be viewed by using Windows PowerShell and the Get-CsNetworkSubnet cmdlet.</span></span> <span data-ttu-id="4f8ca-119">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="4f8ca-120">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-subnet-information"></a><span data-ttu-id="4f8ca-121">ネットワークサブネット情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="4f8ca-121">To view network subnet information</span></span>

  - <span data-ttu-id="4f8ca-122">すべてのネットワークサブネットに関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-122">To view information about all your network subnets, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSubnet
    
    <span data-ttu-id="4f8ca-123">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-123">That will return information similar to this:</span></span>
    
        Identity      : 172.11.15.0
        MaskBits      : 28
        Description   :
        NetworkSiteID : Redmond
        SubnetID      : 172.11.15.0

</div>

<span data-ttu-id="4f8ca-124">詳細については、「 [CsNetworkSubnet の取得](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f8ca-124">For more information, see the help topic for the [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4f8ca-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f8ca-125">See Also</span></span>


[<span data-ttu-id="4f8ca-126">Lync Server 2013 でネットワークサブネットを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="4f8ca-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
[<span data-ttu-id="4f8ca-127">Lync Server 2013 でのネットワークサブネットの削除</span><span class="sxs-lookup"><span data-stu-id="4f8ca-127">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  
  

<span data-ttu-id="4f8ca-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f8ca-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

