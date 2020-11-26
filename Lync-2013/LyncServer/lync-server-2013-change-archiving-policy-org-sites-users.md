---
title: 'Lync Server 2013: アーカイブポリシーを変更して、組織、サイト、またはユーザーの内部または外部の通信のアーカイブを有効または無効にする'
description: 'Lync Server 2013: アーカイブポリシーを変更して、組織、サイト、またはユーザーの内部または外部の通信のアーカイブを有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435181"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="4b8cf-103">Lync Server 2013 でアーカイブポリシーを変更して、組織、サイト、またはユーザーの内部または外部の通信のアーカイブを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="4b8cf-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b8cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b8cf-104">

<span> </span></span></span>

<span data-ttu-id="4b8cf-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="4b8cf-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="4b8cf-106">Lync Server 2013 では、ポリシーを使って、内部通信のアーカイブを有効または無効にしたり、Lync Server 2013 を使用しているユーザーの外部通信を有効にしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="4b8cf-107">これには、次のアーカイブポリシーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="4b8cf-108">Lync Server 2013 を展開するときに既定で作成されるグローバルポリシー。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="4b8cf-109">特定のサイトまたはユーザーに対するアーカイブの実装方法を指定するために作成および使用できる、オプションのサイトレベルとユーザーレベルのポリシー。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="4b8cf-110">アーカイブの展開時にアーカイブポリシーを最初に設定しましたが、展開後にポリシーの変更、追加、削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="4b8cf-111">Lync Server 2013 コントロールパネルで、[**アーカイブと監視**] グループの [**アーカイブポリシー** ] ページを使用して、グローバルレベル、サイトレベル、ユーザーレベルでポリシーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="4b8cf-112">Lync Server ストレージと Exchange 2013 ストレージを統合すると、Exchange ユーザーポリシーは Lync Server 2013 アーカイブポリシーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="4b8cf-113">ポリシーの実装方法 (ポリシーの階層を含む) について詳しくは、「計画ドキュメント、展開ドキュメント、または運用ドキュメント」の「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4b8cf-114">展開に対して Microsoft Exchange の統合を有効にしている場合は、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかが Exchange ポリシーによって制御され、メールボックス In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="4b8cf-115">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="4b8cf-116">アーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="4b8cf-117">詳細については、「 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 でアーカイブ構成オプションを管理</A> する」を参照してください。この操作のドキュメントでは、組織、サイト、プールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="4b8cf-118">アーカイブポリシーを変更するには</span><span class="sxs-lookup"><span data-stu-id="4b8cf-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="4b8cf-119">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4b8cf-120">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4b8cf-121">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4b8cf-122">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="4b8cf-123">ポリシー一覧で、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="4b8cf-124">展開全体のポリシーを変更するには、ポリシー一覧の [**グローバル**] をクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="4b8cf-125">単一のサイトのポリシーを変更するには、ポリシー一覧のサイト名をクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="4b8cf-126">単一のユーザーまたはユーザー グループのポリシーを変更するには、ポリシー一覧のユーザー名またはユーザー グループ名をクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="4b8cf-127">[**アーカイブ ポリシーの編集**] ページで、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="4b8cf-128">ポリシーの内部アーカイブを有効または無効にするには、[**内部通信のアーカイブ**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="4b8cf-129">ポリシーの外部アーカイブを有効または無効にするには、[**外部通信のアーカイブ**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="4b8cf-130">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="4b8cf-131">ユーザー ポリシーの設定は、そのポリシーを適用する特定のユーザーおよびユーザー グループにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="4b8cf-132">詳細については、「 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Lync Server 2013 のユーザーにアーカイブポリシーを適用する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="4b8cf-133">Windows PowerShell コマンドレットを使用してアーカイブを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="4b8cf-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="4b8cf-134">**CsArchivingPolicy** コマンドレットを使用して、アーカイブを有効または無効にすることができます (内部と外部の通信セッションの両方で)。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="4b8cf-135">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="4b8cf-136">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="4b8cf-137">内部通信セッションのアーカイブを有効にするには</span><span class="sxs-lookup"><span data-stu-id="4b8cf-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="4b8cf-138">内部通信セッションのアーカイブを有効にするには、アーカイブ **内部** プロパティの値を True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="4b8cf-139">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="4b8cf-140">外部通信セッションのアーカイブを有効にするには</span><span class="sxs-lookup"><span data-stu-id="4b8cf-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="4b8cf-141">外部通信セッションのアーカイブを有効にするには、アーカイブ **外部** プロパティの値を True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="4b8cf-142">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="4b8cf-143">内部と外部の通信セッションの両方のアーカイブを有効にするには</span><span class="sxs-lookup"><span data-stu-id="4b8cf-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="4b8cf-144">内部と外部の両方の通信セッションのアーカイブを有効にするには、アーカイブ **内部** プロパティと **アーカイブ外部** プロパティの両方を True に設定します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="4b8cf-145">アーカイブを無効にするには</span><span class="sxs-lookup"><span data-stu-id="4b8cf-145">To disable archiving</span></span>

  - <span data-ttu-id="4b8cf-146">アーカイブを完全に無効にするには、アーカイブ **内部** プロパティと **アーカイブ外部** プロパティの両方を False ($False) に設定します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="4b8cf-147">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="4b8cf-148">詳細については、 [CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b8cf-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4b8cf-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b8cf-149">See Also</span></span>


[<span data-ttu-id="4b8cf-150">Lync Server 2013 での内部および外部通信のアーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="4b8cf-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="4b8cf-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b8cf-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

