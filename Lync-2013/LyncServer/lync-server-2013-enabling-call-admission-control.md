---
title: 'Lync Server 2013: 通話受付制御を有効にする'
description: 'Lync Server 2013: 通話受付制御を有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling call admission control
ms:assetid: 015f5c8f-2f90-4b9e-8149-b33767e90582
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520942(v=OCS.15)
ms:contentKeyID: 48183228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f5737f83a1965b920f2a23e1aabbbaec2af7b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399296"
---
# <a name="enabling-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="a94f2-103">Lync Server 2013 での通話受付制御の有効化</span><span class="sxs-lookup"><span data-stu-id="a94f2-103">Enabling call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a94f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a94f2-104">

<span> </span></span></span>

<span data-ttu-id="a94f2-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a94f2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a94f2-106">通話受付管理 (CAC) は、地域、サイト、およびサブネットで構成されるネットワークで、使用可能な帯域幅に基づいてオーディオおよびビデオ伝送に制限を課すことができます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-106">Call admission control (CAC) is a network of regions, sites, and subnets that enable you to place restrictions on audio and video transmissions based on available bandwidth.</span></span> <span data-ttu-id="a94f2-107">CAC ネットワークを構成したら、CAC を有効にして帯域幅の制限を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a94f2-107">After you configure the CAC network, you must enable CAC to enforce the bandwidth limitations.</span></span> <span data-ttu-id="a94f2-108">Lync Server コントロールパネルを使うと、この操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-108">You can use Lync Server Control Panel to do this.</span></span>

<div>

## <a name="to-enable-cac-from-lync-server-control-panel"></a><span data-ttu-id="a94f2-109">Lync Server コントロールパネルで CAC を有効にするには</span><span class="sxs-lookup"><span data-stu-id="a94f2-109">To enable CAC from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="a94f2-110">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a94f2-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a94f2-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a94f2-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a94f2-113">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **グローバル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-113">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="a94f2-114">[ **グローバル** ] ページで、[ **グローバル** 構成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-114">On the **Global** page, click the **Global** configuration.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a94f2-115">Microsoft Lync Server 2013 の展開用に1つのネットワークのみを構成できます。そのため、リストには複数のネットワーク構成を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a94f2-115">Only one network can be configured for any Microsoft Lync Server 2013 deployment, so there will never be more than one network configuration in the list.</span></span> <span data-ttu-id="a94f2-116">グローバル構成の名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="a94f2-116">You cannot rename the Global configuration.</span></span>

    
    </div>

5.  <span data-ttu-id="a94f2-117">[**編集**] メニューの [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-117">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="a94f2-118">[ **グローバル設定の編集** ] ページで、[ **通話受付制御を有効にする** ] チェックボックスをオンにし、[ **コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-118">On the **Edit Global Setting** page, select the **Enable call admission control** check box, and then click **Commit**.</span></span>

<span data-ttu-id="a94f2-119">[ **コミット**] をクリックすると、構成のテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-119">When you click **Commit**, you run a test of the configuration.</span></span> <span data-ttu-id="a94f2-120">[ **グローバル設定の編集** ] ダイアログボックスが閉じ、 **グローバル** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="a94f2-120">The **Edit Global Settings** dialog box closes, returning you to the **Global** page.</span></span> <span data-ttu-id="a94f2-121">ネットワーク構成でエラーや不整合が検出された場合、そのエラーや不整合が正常に動作しなくなる場合 (たとえば、すべての地域が相互に接続されているルートを介してすべての地域に接続されていない場合) は、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-121">You will receive a warning if any errors or inconsistencies are discovered in your network configuration that will prevent it from working correctly (for example, if every region is not connected to every other region through an interregion route).</span></span>

<span data-ttu-id="a94f2-122">ネットワーク構成を変更した場合は、[グローバル構成] を開き、[ **コミット**] をクリックして、検証チェックをもう一度実行できます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-122">If you make changes to your network configuration, you can run the validation check again by opening the Global configuration and clicking **Commit**.</span></span> <span data-ttu-id="a94f2-123">まず、CAC を無効にする必要はありません。チェックボックスをオンのままにして、[ **コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94f2-123">You do not need to disable CAC first: leave the check box checked and click **Commit**.</span></span> <span data-ttu-id="a94f2-124">この操作は、構成を変更することなくいつでも行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a94f2-124">You can do this at any time without making any configuration changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a94f2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a94f2-125">See Also</span></span>


[<span data-ttu-id="a94f2-126">Lync Server 2013 の通話受付制御の概要</span><span class="sxs-lookup"><span data-stu-id="a94f2-126">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  


[<span data-ttu-id="a94f2-127">Lync Server 2013 での通話受付管理の計画</span><span class="sxs-lookup"><span data-stu-id="a94f2-127">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)  
[<span data-ttu-id="a94f2-128">Lync Server 2013 での通話受付制御の構成</span><span class="sxs-lookup"><span data-stu-id="a94f2-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="a94f2-129">Get-Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="a94f2-129">Get-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkConfiguration)  
[<span data-ttu-id="a94f2-130">Set-Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="a94f2-130">Set-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkConfiguration)  
[<span data-ttu-id="a94f2-131">Remove-Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="a94f2-131">Remove-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkConfiguration)  
  

<span data-ttu-id="a94f2-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a94f2-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

