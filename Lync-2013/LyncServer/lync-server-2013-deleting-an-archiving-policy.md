---
title: 'Lync Server 2013: アーカイブポリシーを削除する'
description: 'Lync Server 2013: アーカイブポリシーを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving policy
ms:assetid: 4739a691-41cc-4128-8bb8-6d5a4c02107a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520989(v=OCS.15)
ms:contentKeyID: 48184043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ecf465a62cf8f54777b03a1634d9a95f1b565c9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430365"
---
# <a name="deleting-an-archiving-policy-in-lync-server-2013"></a><span data-ttu-id="d799e-103">Lync Server 2013 でアーカイブポリシーを削除する</span><span class="sxs-lookup"><span data-stu-id="d799e-103">Deleting an Archiving policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d799e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d799e-104">

<span> </span></span></span>

<span data-ttu-id="d799e-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d799e-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d799e-106">ユーザーポリシーまたはサイトポリシーを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="d799e-106">You can delete a user policy or site policy.</span></span> <span data-ttu-id="d799e-107">グローバルポリシーは削除できません。</span><span class="sxs-lookup"><span data-stu-id="d799e-107">The global policy cannot be removed.</span></span> <span data-ttu-id="d799e-108">グローバルポリシーを削除しようとすると、Lync Server 2013 によってポリシーが自動的に既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="d799e-108">If you try to delete the global policy, Lync Server 2013 automatically resets the policy to the default values.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d799e-109">展開に対して Microsoft Exchange の統合を有効にしている場合は、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかが Exchange ポリシーによって制御され、メールボックス In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="d799e-109">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="d799e-110">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d799e-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-policy-for-archiving"></a><span data-ttu-id="d799e-111">アーカイブのユーザーまたはサイトのポリシーを削除するには</span><span class="sxs-lookup"><span data-stu-id="d799e-111">To delete a user or site policy for archiving</span></span>

1.  <span data-ttu-id="d799e-112">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="d799e-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d799e-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d799e-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d799e-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d799e-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d799e-115">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d799e-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="d799e-116">アーカイブ ポリシーのリストで、削除するユーザー ポリシーまたはサイト ポリシーをクリックし、[**編集**] をクリックして、[**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d799e-116">In the list of archiving policies, click the user or site policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="d799e-117">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d799e-117">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d799e-118">Windows PowerShell コマンドレットを使用してアーカイブポリシーを削除する</span><span class="sxs-lookup"><span data-stu-id="d799e-118">Removing Archiving Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d799e-119">Windows PowerShell と **CsArchivingPolicy** コマンドレットを使用して、アーカイブポリシーを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="d799e-119">Archiving policies can be deleted by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="d799e-120">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="d799e-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d799e-121">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="d799e-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-archiving-policy"></a><span data-ttu-id="d799e-122">指定したアーカイブポリシーを削除するには</span><span class="sxs-lookup"><span data-stu-id="d799e-122">To remove a specified archiving policy</span></span>

  - <span data-ttu-id="d799e-123">例として、 **CsArchivingPolicy を削除** すると、id サイト: レドモンドのポリシーが削除されます。</span><span class="sxs-lookup"><span data-stu-id="d799e-123">As an example, **Remove-CsArchivingPolicy** deletes the policy with the Identity site:Redmond.</span></span> <span data-ttu-id="d799e-124">サイトの範囲で構成されたポリシーが削除されると、サイトポリシーによって以前管理されていたユーザーは、その代わりにグローバルアーカイブポリシーによって自動的に管理されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d799e-124">Note that, when a policy configured at the site scope is deleted, users previously managed by the site policy will automatically be governed by the global archiving policy instead.</span></span> <span data-ttu-id="d799e-125">次のコマンドは、Redmond サイトに適用されているアーカイブを削除します。</span><span class="sxs-lookup"><span data-stu-id="d799e-125">The following command removes the archiving applied to the Redmond site:</span></span>
    
        Remove-CsArchivingPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="d799e-126">ユーザーごとのスコープに適用されているすべてのアーカイブポリシーを削除するには</span><span class="sxs-lookup"><span data-stu-id="d799e-126">To remove all the archiving policies applied to the per-user scope</span></span>

  - <span data-ttu-id="d799e-127">このコマンドは、ユーザーごとのスコープに適用されたすべてのアーカイブポリシーを削除します。</span><span class="sxs-lookup"><span data-stu-id="d799e-127">This command removes all the archiving policies applied to the per-user scope:</span></span>
    
        Get-CsArchivingPolicy -Filter "tag:*" | Remove-CsArchivingPolicy

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-that-disable-internal-archiving"></a><span data-ttu-id="d799e-128">内部アーカイブを無効にするアーカイブポリシーをすべて削除するには</span><span class="sxs-lookup"><span data-stu-id="d799e-128">To remove all the archiving policies that disable internal archiving</span></span>

  - <span data-ttu-id="d799e-129">このコマンドでは、内部アーカイブが無効になっているすべてのアーカイブ ポリシーを削除します。</span><span class="sxs-lookup"><span data-stu-id="d799e-129">This command removes all the archiving policies where internal archiving has been disabled:</span></span>
    
        Get-CsArchivingPolicy | Where-Object {$_.ArchiveInternal -eq $False} | Remove-CsArchivingPolicy

</div>

<span data-ttu-id="d799e-130">詳細については、 [CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d799e-130">For more information, see the help topic for the [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d799e-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="d799e-131">See Also</span></span>


[<span data-ttu-id="d799e-132">Lync Server 2013 での内部および外部通信のアーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="d799e-132">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="d799e-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d799e-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

