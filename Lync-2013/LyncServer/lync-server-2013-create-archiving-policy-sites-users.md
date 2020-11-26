---
title: 'Lync Server 2013: 特定のサイトまたはユーザーに対して、内部または外部の通信のアーカイブを有効または無効にするアーカイブポリシーを作成する'
description: 'Lync Server 2013: 特定のサイトまたはユーザーに対して、内部または外部の通信のアーカイブを有効または無効にするアーカイブポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431989"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="ab2bf-103">Lync Server 2013 でアーカイブポリシーを作成して、特定のサイトまたはユーザーの内部または外部の通信のアーカイブを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="ab2bf-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab2bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab2bf-104">

<span> </span></span></span>

<span data-ttu-id="ab2bf-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ab2bf-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ab2bf-106">Lync Server 2013 では、ポリシーを使って、内部通信のアーカイブを有効または無効にしたり、Lync Server 2013 を使用しているユーザーの外部通信を有効にしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="ab2bf-107">これには、次のアーカイブポリシーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="ab2bf-108">Lync Server 2013 を展開するときに既定で作成されるグローバルポリシー。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="ab2bf-109">特定のサイトまたはユーザーに対するアーカイブの実装方法を指定するために作成および使用できる、オプションのサイトレベルとユーザーレベルのポリシー。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="ab2bf-110">アーカイブの展開時にアーカイブポリシーを最初に設定しましたが、展開後にポリシーの変更、追加、削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="ab2bf-111">Lync Server 2013 コントロールパネルで、[**アーカイブと監視**] グループの [**アーカイブポリシー** ] ページを使用して、グローバルレベル、サイトレベル、ユーザーレベルでポリシーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="ab2bf-112">Lync Server ストレージと Exchange 2013 ストレージを統合すると、Exchange ユーザーポリシーは Lync Server 2013 アーカイブポリシーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="ab2bf-113">ポリシーの実装方法 (ポリシーの階層を含む) について詳しくは、「計画ドキュメント、展開ドキュメント、または運用ドキュメント」の「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ab2bf-114">アーカイブの実装を制御するには、IM または会議のアーカイブ、重要モードの使用、削除オプションなど、アーカイブ構成のオプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="ab2bf-115">既定では、グローバルアーカイブ構成またはサイトまたはプールのアーカイブ構成では、どのオプションも有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="ab2bf-116">アーカイブポリシーで、内部または外部通信のアーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="ab2bf-117">詳細については、「 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 でアーカイブ構成オプションを管理</A> する」を参照してください。この操作のドキュメントでは、組織、サイト、プールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="ab2bf-118">展開に対して Microsoft Exchange の統合を有効にしている場合は、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかが Exchange ポリシーによって制御され、メールボックス In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ab2bf-119">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="ab2bf-120">サイトまたはユーザーのアーカイブポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="ab2bf-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="ab2bf-121">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ab2bf-122">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ab2bf-123">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ab2bf-124">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="ab2bf-125">[**新規**] をクリックし、次のいずれかの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="ab2bf-126">サイトレベルのアーカイブポリシーを作成するには、[ **サイトポリシー** ] をクリックし、[ **サイトの選択**] でポリシーを適用するサイトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="ab2bf-127">ユーザーレベルのアーカイブ ポリシーを作成するには、[**ユーザー ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="ab2bf-128">[**新しいアーカイブ ポリシー**] で、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="ab2bf-129">[**名前**] で、新しいポリシーの名前を指定します (externalContoso など)。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="ab2bf-130">[**説明**] に、そのポリシーの内容に関する詳細を入力します (「Contoso の外部ユーザー アーカイブ ポリシー」など)。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="ab2bf-131">内部ユーザーとの通信のアーカイブを制御するには、[**内部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="ab2bf-132">外部ユーザーとの通信のアーカイブを制御するには、[**外部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="ab2bf-133">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ab2bf-134">ユーザー ポリシーの設定は、そのポリシーを適用する特定のユーザーおよびユーザー グループにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="ab2bf-135">詳細については、「 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Lync Server 2013 のユーザーにアーカイブポリシーを適用する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ab2bf-136">Windows PowerShell コマンドレットを使用してアーカイブポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="ab2bf-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ab2bf-137">アーカイブポリシーを作成するには、Windows PowerShell と **CsArchivingPolicy** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="ab2bf-138">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ab2bf-139">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="ab2bf-140">サイトの範囲に新しいアーカイブポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="ab2bf-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="ab2bf-141">次のコマンドは、Redmond サイトの新しいアーカイブ ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="ab2bf-142">ユーザーごとのスコープで新しいアーカイブポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="ab2bf-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="ab2bf-143">ユーザーごとのスコープで新しいアーカイブポリシーを作成するには、ポリシーを作成するときに一意の Id を指定するだけです。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="ab2bf-144">内部通信セッションのアーカイブを有効にする新しいアーカイブ ポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="ab2bf-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="ab2bf-145">前の各コマンドでは (必須の ID パラメーター以外に) パラメーターが指定されていないため、新しいポリシーではすべてのプロパティで既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="ab2bf-146">別のプロパティ値を使用するポリシーを作成するには、該当するパラメーターとパラメーター値を含めます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="ab2bf-147">たとえば、内部のインスタントメッセージングセッションのアーカイブを許可するアーカイブポリシーを作成するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="ab2bf-148">内部と外部の両通信セッションのアーカイブを有効にする新しいアーカイブ ポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="ab2bf-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="ab2bf-149">複数のパラメーターを含めることで、複数のプロパティ値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="ab2bf-150">たとえば、次のコマンドは、内部と外部のインスタントメッセージングセッションの両方をアーカイブするための新しいポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="ab2bf-151">詳細については、 [CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab2bf-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ab2bf-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab2bf-152">See Also</span></span>


[<span data-ttu-id="ab2bf-153">Lync Server 2013 での内部および外部通信のアーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="ab2bf-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="ab2bf-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab2bf-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

