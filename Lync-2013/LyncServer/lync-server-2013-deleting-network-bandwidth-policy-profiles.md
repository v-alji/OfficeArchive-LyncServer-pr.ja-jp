---
title: 'Lync Server 2013: ネットワーク帯域幅ポリシープロファイルを削除する'
description: 'Lync Server 2013: ネットワーク帯域幅ポリシープロファイルを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network bandwidth policy profiles
ms:assetid: 4d6beda8-6aa5-4d5e-8a07-363598f0e0c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688050(v=OCS.15)
ms:contentKeyID: 49733643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69f460d9620158d1857dae41e0033f6d36078868
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430302"
---
# <a name="deleting-network-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="41a55-103">Lync Server 2013 でネットワーク帯域幅ポリシープロファイルを削除する</span><span class="sxs-lookup"><span data-stu-id="41a55-103">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41a55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41a55-104">

<span> </span></span></span>

<span data-ttu-id="41a55-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="41a55-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="41a55-106">通話受付制御 (CAC) の一部として、帯域幅ポリシーを使って、特定のモダリティの帯域幅の制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="41a55-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="41a55-107">Microsoft Lync Server 2013 では、オーディオとビデオのモダリティのみが帯域幅の制限を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="41a55-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="41a55-108">全体的な帯域幅の制限とセッションの制限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="41a55-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="41a55-109">Lync Server コントロールパネルを使用して、これらのポリシーのコンテナープロファイルを作成、変更、または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="41a55-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="41a55-110">ネットワーク帯域幅ポリシーのプロファイルを削除するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="41a55-110">Use the following procedures to delete a network bandwidth policy profiles.</span></span> <span data-ttu-id="41a55-111">ネットワーク帯域幅ポリシープロファイルの作成または変更の詳細については、「 [Lync Server 2013 での帯域幅ポリシープロファイルの作成または変更](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41a55-111">For details on creating or modifying a network bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-delete-a-bandwidth-policy-profile"></a><span data-ttu-id="41a55-112">帯域幅ポリシーのプロファイルを削除するには</span><span class="sxs-lookup"><span data-stu-id="41a55-112">To delete a bandwidth policy profile</span></span>

1.  <span data-ttu-id="41a55-113">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="41a55-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="41a55-114">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="41a55-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="41a55-115">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="41a55-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="41a55-116">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **帯域幅ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41a55-116">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="41a55-117">[ **帯域幅ポリシー** ] ページで、削除する帯域幅ポリシープロファイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="41a55-117">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="41a55-118">一度に複数のプロファイルを削除できます。</span><span class="sxs-lookup"><span data-stu-id="41a55-118">You can delete more than one profile at a time.</span></span> <span data-ttu-id="41a55-119">これを行うには、ctrl キーを押しながら、CTRL キーを押しながら複数のプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="41a55-119">To do this, press CTRL and select multiple profiles while holding down the CTRL key.</span></span> <span data-ttu-id="41a55-120">または、すべてのプロファイルを選択するには、[<STRONG>編集</STRONG>] メニューの [<STRONG>すべて選択</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41a55-120">Or, to select all profiles, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="41a55-121">[ **編集** ] メニューの [ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41a55-121">On the **Edit** menu, click **Delete**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="41a55-122">ネットワークサイトに関連付けられている帯域幅ポリシープロファイルを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="41a55-122">You cannot delete a bandwidth policy profile that is associated with a network site.</span></span> <span data-ttu-id="41a55-123">プロファイルを削除するには、最初にネットワークサイトとの関連付けを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41a55-123">You must first remove the association with the network site before you can delete the profile.</span></span> <span data-ttu-id="41a55-124">ネットワークサイトを変更する方法の詳細については、「 <A href="lync-server-2013-creating-or-modifying-network-sites.md">Lync Server 2013 でネットワークサイトを作成または変更</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41a55-124">For details about how to modify the network site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="41a55-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="41a55-125">See Also</span></span>


[<span data-ttu-id="41a55-126">Lync Server 2013 での帯域幅ポリシープロファイルの作成または変更</span><span class="sxs-lookup"><span data-stu-id="41a55-126">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="41a55-127">Lync Server 2013 でネットワーク帯域幅ポリシーのプロファイル情報を表示する</span><span class="sxs-lookup"><span data-stu-id="41a55-127">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-bandwidth-policy-profile-information.md)  


[<span data-ttu-id="41a55-128">Lync Server 2013 での通話受付制御の構成</span><span class="sxs-lookup"><span data-stu-id="41a55-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="41a55-129">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="41a55-129">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="41a55-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41a55-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

