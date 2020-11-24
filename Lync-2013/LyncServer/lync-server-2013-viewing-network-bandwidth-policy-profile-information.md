---
title: 'Lync Server 2013: ネットワーク帯域幅ポリシーのプロファイル情報を表示する'
description: 'Lync Server 2013: ネットワーク帯域幅ポリシーのプロファイル情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network bandwidth policy profile information
ms:assetid: eed453fc-04e9-4971-959c-6fad54bf1c96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721931(v=OCS.15)
ms:contentKeyID: 49733866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c72a3533ae6f49f91db91b2c3b515c0b5153ec27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398931"
---
# <a name="viewing-network-bandwidth-policy-profile-information-in-lync-server-2013"></a><span data-ttu-id="3085a-103">Lync Server 2013 でネットワーク帯域幅ポリシーのプロファイル情報を表示する</span><span class="sxs-lookup"><span data-stu-id="3085a-103">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3085a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3085a-104">

<span> </span></span></span>

<span data-ttu-id="3085a-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3085a-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3085a-106">通話受付制御 (CAC) の一部として、帯域幅ポリシーを使って、特定のモダリティの帯域幅の制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="3085a-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="3085a-107">Microsoft Lync Server 2013 では、オーディオとビデオのモダリティのみが帯域幅の制限を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3085a-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="3085a-108">全体的な帯域幅の制限とセッションの制限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3085a-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="3085a-109">Lync Server コントロールパネルを使用して、これらのポリシーのコンテナープロファイルを作成、変更、または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3085a-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="3085a-110">各帯域幅ポリシーのプロファイルは、1つ以上のネットワークサイトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="3085a-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="3085a-111">帯域幅ポリシーのプロファイルを表示するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3085a-111">Use the following procedures to view a bandwidth policy profile.</span></span> <span data-ttu-id="3085a-112">帯域幅ポリシープロファイルを作成または変更するには、「 [Lync Server 2013 での帯域幅ポリシープロファイルの作成または](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)変更」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3085a-112">To create or modify a bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-view-a-bandwidth-policy-profile"></a><span data-ttu-id="3085a-113">帯域幅ポリシーのプロファイルを表示するには</span><span class="sxs-lookup"><span data-stu-id="3085a-113">To view a bandwidth policy profile</span></span>

1.  <span data-ttu-id="3085a-114">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="3085a-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3085a-115">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3085a-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3085a-116">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3085a-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3085a-117">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **帯域幅ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3085a-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="3085a-118">[ **帯域幅ポリシー** ] ページで、表示する帯域幅ポリシープロファイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3085a-118">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to view.</span></span>

5.  <span data-ttu-id="3085a-119">[**編集**] メニューの [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3085a-119">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-bandwidth-policy-profile-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3085a-120">Windows PowerShell コマンドレットを使用してネットワーク帯域幅ポリシーのプロファイル情報を表示する</span><span class="sxs-lookup"><span data-stu-id="3085a-120">Viewing Network Bandwidth Policy Profile Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3085a-121">ネットワーク帯域幅プロファイルを表示するには、Windows PowerShell と Get-CsNetworkBandwidthPolicyProfile コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="3085a-121">Network bandwidth profiles can be viewed by using Windows PowerShell and the Get-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="3085a-122">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="3085a-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3085a-123">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="3085a-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-bandwidth-policy-profile-information"></a><span data-ttu-id="3085a-124">ネットワーク帯域幅ポリシーのプロファイル情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="3085a-124">To view network bandwidth policy profile information</span></span>

  - <span data-ttu-id="3085a-125">すべてのネットワーク帯域幅ポリシープロファイルに関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="3085a-125">To view information about all your network bandwidth policy profiles, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkBandwidthPolicyProfile
    
    <span data-ttu-id="3085a-126">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3085a-126">That will return information similar to this:</span></span>
    
        Identity          : RedmondBandwidthPolicy
        BWPolicy          : {BWLimit=200;BWSessionLimit=200;
                            BWPolicyModality=Audio, 
                            BWLimit=1400;BWSessionLimit=500;
                            BWPolicyModality=Video}
        BWPolicyProfileID : RedmondBandwidthPolicy
        Description       :

</div>

<span data-ttu-id="3085a-127">詳細については、 [CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3085a-127">For more information, see the help topic for the [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3085a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3085a-128">See Also</span></span>


[<span data-ttu-id="3085a-129">Lync Server 2013 での帯域幅ポリシープロファイルの作成または変更</span><span class="sxs-lookup"><span data-stu-id="3085a-129">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="3085a-130">Lync Server 2013 でネットワーク帯域幅ポリシープロファイルを削除する</span><span class="sxs-lookup"><span data-stu-id="3085a-130">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="3085a-131">Lync Server 2013 での通話受付制御の構成</span><span class="sxs-lookup"><span data-stu-id="3085a-131">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
  

<span data-ttu-id="3085a-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3085a-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

