---
title: 'Lync Server 2013: 帯域幅ポリシープロファイルを作成または変更する'
description: 'Lync Server 2013: 帯域幅ポリシープロファイルを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying bandwidth policy profiles
ms:assetid: 08a2e18f-9b0d-4a2f-aa14-13bbf79ec745
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520945(v=OCS.15)
ms:contentKeyID: 48183336
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8450cf8f4da53bf4a7e096fd7618b7fc6d055b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431450"
---
# <a name="creating-or-modifying-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="64c6f-103">Lync Server 2013 での帯域幅ポリシープロファイルの作成または変更</span><span class="sxs-lookup"><span data-stu-id="64c6f-103">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64c6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64c6f-104">

<span> </span></span></span>

<span data-ttu-id="64c6f-105">_**最終更新日:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="64c6f-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="64c6f-106">通話受付制御 (CAC) の一部として、帯域幅ポリシーを使って、特定のモダリティの帯域幅の制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="64c6f-107">Microsoft Lync Server 2013 では、オーディオとビデオのモダリティのみが帯域幅の制限を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="64c6f-108">全体的な帯域幅の制限とセッションの制限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="64c6f-109">Lync Server コントロールパネルを使用して、これらのポリシーのコンテナープロファイルを作成、変更、または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="64c6f-110">各帯域幅ポリシーのプロファイルは、1つ以上のネットワークサイトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="64c6f-111">帯域幅ポリシープロファイルを作成または変更するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-111">Use the following procedures to create or modify a bandwidth policy profile.</span></span> <span data-ttu-id="64c6f-112">帯域幅ポリシーのプロファイルを削除する方法については、「 [Lync Server 2013 でネットワーク帯域幅ポリシープロファイルを削除](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64c6f-112">To delete a bandwidth policy profile, see [Deleting network bandwidth policy profiles in Lync Server 2013](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)</span></span>

<div>

## <a name="to-create-a-new-bandwidth-policy-profile"></a><span data-ttu-id="64c6f-113">新しい帯域幅ポリシープロファイルを作成するには</span><span class="sxs-lookup"><span data-stu-id="64c6f-113">To create a new bandwidth policy profile</span></span>

1.  <span data-ttu-id="64c6f-114">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="64c6f-115">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="64c6f-116">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="64c6f-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="64c6f-117">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **帯域幅ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="64c6f-118">[ **帯域幅ポリシー** ] ページで、[ **新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-118">On the **Bandwidth Policy** page, click **New**.</span></span>

5.  <span data-ttu-id="64c6f-119">**新しい帯域幅ポリシープロファイル** で、[**名前**] フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-119">In **New Bandwidth Policy Profile**, type a name in the **Name** field.</span></span> <span data-ttu-id="64c6f-120">この名前は、すべての帯域幅ポリシープロファイルの間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c6f-120">This name must be unique among all bandwidth policy profiles.</span></span>

6.  <span data-ttu-id="64c6f-121">[ **オーディオ制限** ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-121">In the **Audio limit** field, type a numeric value.</span></span> <span data-ttu-id="64c6f-122">この値は、すべてのオーディオ接続に割り当てることができる最大帯域幅です。 kbps で表されます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-122">This value is the maximum amount of bandwidth to allocate for all audio connections, expressed in kbps.</span></span>

7.  <span data-ttu-id="64c6f-123">[ **オーディオセッションの制限** ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-123">Enter a numeric value in the **Audio session limit** field.</span></span> <span data-ttu-id="64c6f-124">この値は、個々の音声接続に割り当てられる帯域幅の上限です。 kbps で表されます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-124">This value is the maximum amount of bandwidth to allocate for an individual audio connection, expressed in kbps.</span></span> <span data-ttu-id="64c6f-125">この値は40以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c6f-125">This value must be 40 or higher.</span></span>

8.  <span data-ttu-id="64c6f-126">[ **ビデオの制限** ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-126">Enter a numeric value in the **Video limit** field.</span></span> <span data-ttu-id="64c6f-127">この値は、すべてのビデオ接続に割り当てることができる最大帯域幅です。 kbps で表されます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-127">This value is the maximum amount of bandwidth to allocate for all video connections, expressed in kbps.</span></span>

9.  <span data-ttu-id="64c6f-128">[ **ビデオセッションの制限** ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-128">Enter a numeric value in the **Video session limit** field.</span></span> <span data-ttu-id="64c6f-129">この値は、個々のビデオ接続に割り当てることができる最大帯域幅です。 kbps で表されます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-129">This value is the maximum amount of bandwidth to allocate for an individual video connection, expressed in kbps.</span></span> <span data-ttu-id="64c6f-130">この値は100以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c6f-130">This value must be 100 or higher.</span></span>

10. <span data-ttu-id="64c6f-131">省略[ **説明** ] フィールドに値を入力して、この帯域幅ポリシープロファイルの詳細情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="64c6f-131">(Optional) Type a value in the **Description** field to provide more information about this bandwidth policy profile that cannot be expressed by the name alone.</span></span>

11. <span data-ttu-id="64c6f-132">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-132">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="64c6f-133">新しい帯域幅ポリシープロファイルを作成しても、帯域幅の制限は自動的に適用されません。</span><span class="sxs-lookup"><span data-stu-id="64c6f-133">Creating a new bandwidth policy profile does not automatically enforce bandwidth restrictions.</span></span> <span data-ttu-id="64c6f-134">最初にポリシープロファイルをサイトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c6f-134">You must first associate the policy profile with a site.</span></span> <span data-ttu-id="64c6f-135">ポリシープロファイルをサイトに関連付ける方法の詳細については、「 <A href="lync-server-2013-creating-or-modifying-network-sites.md">Lync Server 2013 でネットワークサイトを作成または変更</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64c6f-135">For details about how to associate a policy profile with a site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-bandwidth-policy-profile"></a><span data-ttu-id="64c6f-136">帯域幅ポリシーのプロファイルを変更するには</span><span class="sxs-lookup"><span data-stu-id="64c6f-136">To modify a bandwidth policy profile</span></span>

1.  <span data-ttu-id="64c6f-137">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="64c6f-138">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="64c6f-139">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="64c6f-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="64c6f-140">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **帯域幅ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-140">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="64c6f-141">[ **帯域幅ポリシー** ] ページで、変更する帯域幅ポリシープロファイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-141">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to modify.</span></span>

5.  <span data-ttu-id="64c6f-142">[**編集**] メニューの [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="64c6f-143">[ **帯域幅ポリシープロファイルの編集** ] ページで、必要に応じてフィールドを変更します (詳細については、このトピックの前の「帯域幅ポリシープロファイルを作成する」セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="64c6f-143">On the **Edit Bandwidth Policy Profile** page, modify the fields as necessary (for details, see the "To create a bandwidth policy profile" section earlier in this topic).</span></span>

7.  <span data-ttu-id="64c6f-144">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64c6f-144">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="64c6f-145">帯域幅ポリシーのプロファイルを変更すると、この帯域幅ポリシープロファイルに関連付けられたすべてのネットワークサイトの帯域幅の制限がすぐに更新されます。</span><span class="sxs-lookup"><span data-stu-id="64c6f-145">When you modify the bandwidth policy profile, it will immediately update the bandwidth limitations of all network sites associated with this bandwidth policy profile.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="64c6f-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="64c6f-146">See Also</span></span>


[<span data-ttu-id="64c6f-147">Lync Server 2013 でネットワーク帯域幅ポリシープロファイルを削除する</span><span class="sxs-lookup"><span data-stu-id="64c6f-147">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="64c6f-148">Lync Server 2013 での通話受付制御の構成</span><span class="sxs-lookup"><span data-stu-id="64c6f-148">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="64c6f-149">新規-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="64c6f-149">New-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkBandwidthPolicyProfile)  
[<span data-ttu-id="64c6f-150">Set-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="64c6f-150">Set-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkBandwidthPolicyProfile)  
[<span data-ttu-id="64c6f-151">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="64c6f-151">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="64c6f-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64c6f-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

