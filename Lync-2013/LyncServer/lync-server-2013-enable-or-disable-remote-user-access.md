---
title: 'Lync Server 2013: リモート ユーザー アクセスの有効化または無効化'
description: 'Lync Server 2013: リモートユーザーアクセスを有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable remote user access
ms:assetid: cd9d3ddc-4839-457a-86d9-b15413e74002
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182586(v=OCS.15)
ms:contentKeyID: 48185660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dea2d58c1978ac2d52365a4a453c40b38dd89c44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428875"
---
# <a name="enable-or-disable-remote-user-access-in-lync-server-2013"></a><span data-ttu-id="e16be-103">Lync Server 2013 でのリモート ユーザー アクセスの有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="e16be-103">Enable or disable remote user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e16be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e16be-104">

<span> </span></span></span>

<span data-ttu-id="e16be-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e16be-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e16be-106">リモートユーザーは組織内のユーザーで、組織内に Active Directory id が固定されています。</span><span class="sxs-lookup"><span data-stu-id="e16be-106">Remote users are users in your organization who have a persistent Active Directory identity within the organization.</span></span> <span data-ttu-id="e16be-107">リモートユーザーは、組織のネットワークに接続されていないときに仮想プライベートネットワーク (VPN) を使用して、ネットワークの外部から Lync Server にサインインすることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="e16be-107">Remote users often sign in to Lync Server from outside your network by using a virtual private network (VPN) when they are not connected to your organization’s network.</span></span> <span data-ttu-id="e16be-108">リモートユーザーには、自宅や外出先で作業している従業員や、信頼できるベンダーなど、企業の資格情報が付与されている信頼できる社員が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e16be-108">Remote users include employees working at home or on the road and other remote workers, such as trusted vendors, who have been granted enterprise credentials.</span></span> <span data-ttu-id="e16be-109">リモートユーザーに対してリモートユーザーアクセスを有効にすると、サポートされているリモートユーザーはインターネット経由で接続し、Lync Server を使用して内部ユーザーと共同作業するために VPN を使用して接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e16be-109">If you enable remote user access for remote users, supported remote users connect over the Internet and do not have to connect using a VPN in order to collaborate with internal users using Lync Server.</span></span>

<span data-ttu-id="e16be-110">リモートユーザーアクセスをサポートするには、リモートユーザーアクセスを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e16be-110">To support remote user access, you must enable remote user access.</span></span> <span data-ttu-id="e16be-111">リモートユーザーアクセスを有効にすると、組織全体で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e16be-111">When you enable remote user access, you enable it for your entire organization.</span></span> <span data-ttu-id="e16be-112">後でリモートユーザーのアクセスを一時的または完全に禁止する必要がある場合は、組織に対して無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e16be-112">If you later want to temporarily or permanently prevent remote user access, you can disable it for your organization.</span></span> <span data-ttu-id="e16be-113">組織のリモートユーザーアクセスを有効または無効にするには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="e16be-113">Use the procedure in this section to enable or disable remote user access for your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e16be-114">リモートユーザーアクセスを有効にすることは、アクセスエッジサービスを実行しているサーバーがリモートユーザーとの通信をサポートしていることを示しますが、リモートユーザーアクセスの使用を管理するために少なくとも1つのポリシーを構成するまでは、リモートユーザーは組織のインスタントメッセージング (IM) または会議に参加できません。</span><span class="sxs-lookup"><span data-stu-id="e16be-114">Enabling remote user access only specifies that your servers running the Access Edge service support communications with remote users, but remote users cannot participate in instant messaging (IM) or conferences in your organization until you also configure at least one policy to manage the use of remote user access.</span></span> <span data-ttu-id="e16be-115">1つのポリシーレベルで適用される Lync Server ポリシーの設定は、別のポリシーレベルで適用されている設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="e16be-115">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="e16be-116">Lync Server ポリシーの優先順位: ユーザーポリシー (ほとんどの影響) によってサイトポリシーが上書きされ、サイトポリシーがグローバルポリシーを上書きします (最も影響が少なくなります)。</span><span class="sxs-lookup"><span data-stu-id="e16be-116">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="e16be-117">つまり、ポリシー設定が、そのポリシーの影響を受けるオブジェクトに近いほど、オブジェクトに及ぼす影響は大きくなります。</span><span class="sxs-lookup"><span data-stu-id="e16be-117">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span> <span data-ttu-id="e16be-118">リモートユーザーアクセスを使用するためのポリシーの構成の詳細については、「 <A href="lync-server-2013-configure-policies-to-control-remote-user-access.md">Lync Server 2013 でリモートユーザーアクセスを制御するためのポリシーを構成する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e16be-118">For details about configuring policies for the use of remote user access, see <A href="lync-server-2013-configure-policies-to-control-remote-user-access.md">Configure policies to control remote user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-remote-user-access-for-your-organization"></a><span data-ttu-id="e16be-119">組織のリモートユーザーアクセスを有効または無効にするには</span><span class="sxs-lookup"><span data-stu-id="e16be-119">To enable or disable remote user access for your organization</span></span>

1.  <span data-ttu-id="e16be-120">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="e16be-120">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e16be-121">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="e16be-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e16be-122">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e16be-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e16be-123">左側のナビゲーション バーで [**フェデレーションと外部アクセス**] をクリックし、[**アクセス エッジ構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16be-123">In the left navigation bar, click **Federation and External Access**, and then click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="e16be-124">[ **アクセスエッジの構成** ] ページで [ **グローバル**] をクリックし、[ **編集**] をクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16be-124">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="e16be-125">[ **Access Edge 構成の編集**] で、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="e16be-125">In **Edit Access Edge Configuration**, do one of the following:</span></span>
    
      - <span data-ttu-id="e16be-126">組織のリモートユーザーアクセスを有効にするには、[ **リモートユーザーアクセスを有効** にする] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e16be-126">To enable remote user access for your organization, select the **Enable remote user access** check box.</span></span>
    
      - <span data-ttu-id="e16be-127">組織のリモートユーザーアクセスを無効にするには、[ **リモートユーザーアクセスを有効に** する] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="e16be-127">To disable remote user access for your organization, clear the **Enable remote user access** check box.</span></span>

6.  <span data-ttu-id="e16be-128">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16be-128">Click **Commit**.</span></span>

<span data-ttu-id="e16be-129">リモートユーザーが Lync Server を実行しているサーバーにサインインできるようにするには、リモートユーザーのアクセスをサポートするために、少なくとも1つの外部アクセスポリシーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e16be-129">To enable remote users to sign in to your servers running Lync Server, you must also configure at least one external access policy to support remote user access.</span></span> <span data-ttu-id="e16be-130">詳細については、「展開ドキュメントまたは運用ドキュメントの「 [Lync Server 2013 でリモートユーザーアクセスを制御するためのポリシーを構成する](lync-server-2013-configure-policies-to-control-remote-user-access.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e16be-130">For details, see [Configure policies to control remote user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-remote-user-access.md) in the Deployment documentation or the Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-remote-user-access-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e16be-131">Windows PowerShell コマンドレットを使用したリモートユーザーアクセスの有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="e16be-131">Enabling or Disabling Remote User Access by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e16be-132">リモートユーザーアクセスは、Windows PowerShell と Set-CsAccessEdgeConfiguration コマンドレットを使用して管理できます。</span><span class="sxs-lookup"><span data-stu-id="e16be-132">Remote user access can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="e16be-133">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="e16be-133">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e16be-134">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="e16be-134">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-remote-user-access"></a><span data-ttu-id="e16be-135">リモートユーザーアクセスを有効にするには</span><span class="sxs-lookup"><span data-stu-id="e16be-135">To enable remote user access</span></span>

  - <span data-ttu-id="e16be-136">リモートユーザーアクセスを有効にするには、 **Allowoutsideusers** プロパティの値を True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="e16be-136">To enable remote user access, set the value of the **AllowOutsideUsers** property to True ($True):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowOutsideUsers $True

</div>

<div>

## <a name="to-disable-remote-user-access"></a><span data-ttu-id="e16be-137">リモートユーザーアクセスを無効にするには</span><span class="sxs-lookup"><span data-stu-id="e16be-137">To disable remote user access</span></span>

  - <span data-ttu-id="e16be-138">リモートユーザーアクセスを無効にするには、 **Allowoutsideusers** プロパティの値を False ($False) に設定します。</span><span class="sxs-lookup"><span data-stu-id="e16be-138">To disable remote user access, set the value of the **AllowOutsideUsers** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowOutsideUsers $False

<span data-ttu-id="e16be-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e16be-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

