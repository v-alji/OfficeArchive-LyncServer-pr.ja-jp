---
title: 'Lync Server 2013: フェデレーション ユーザー アクセスを制御するポリシーの構成'
description: 'Lync Server 2013: フェデレーションされたユーザーアクセスを制御するためのポリシーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure policies to control federated user access
ms:assetid: 5485e208-81e4-4e59-9aeb-1232c11dd8a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398359(v=OCS.15)
ms:contentKeyID: 48184180
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d69f35baa16086b0c4e93a2a015474f87e08b736
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398505"
---
# <a name="configure-policies-to-control-federated-user-access-in-lync-server-2013"></a><span data-ttu-id="fa5bb-103">Lync Server 2013 でのフェデレーション ユーザー アクセスを制御するポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="fa5bb-103">Configure policies to control federated user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa5bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa5bb-104">

<span> </span></span></span>

<span data-ttu-id="fa5bb-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="fa5bb-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="fa5bb-106">フェデレーションパートナーとの通信をサポートするようにポリシーを構成すると、フェデレーションドメインのユーザーにポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-106">When you configure policies to support communications with federated partners, the policies apply to users of federated domains.</span></span> <span data-ttu-id="fa5bb-107">フェデレーションドメインのユーザーが Lync Server 2013 ユーザーと共同作業できるかどうかを制御するために、1つ以上の外部ユーザーアクセスポリシーを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-107">You can configure one or more external user access policies to control whether users of federated domains can collaborate with your Lync Server 2013 users.</span></span> <span data-ttu-id="fa5bb-108">フェデレーションされたユーザーアクセスを制御するには、グローバル、サイト、ユーザーレベルでポリシーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-108">To control federated user access, you can configure policies at the global, site, and user level.</span></span> <span data-ttu-id="fa5bb-109">1つのポリシーレベルで適用される Lync Server ポリシーの設定は、別のポリシーレベルで適用されている設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-109">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="fa5bb-110">Lync Server ポリシーの優先順位: ユーザーポリシー (ほとんどの影響) によってサイトポリシーが上書きされ、サイトポリシーがグローバルポリシーを上書きします (最も影響が少なくなります)。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-110">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="fa5bb-111">つまり、ポリシー設定が、そのポリシーの影響を受けるオブジェクトに近いほど、オブジェクトに及ぼす影響は大きくなります。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-111">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fa5bb-112">組織でフェデレーションを有効にしていない場合でも、フェデレーションされたユーザーアクセスを制御するためのポリシーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-112">You can configure policies to control federated user access, even if you have not enabled federation for your organization.</span></span> <span data-ttu-id="fa5bb-113">ただし、構成したポリシーは、組織でフェデレーションが有効になっている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-113">However, the policies that you configure are in effect only when you have federation enabled for your organization.</span></span> <span data-ttu-id="fa5bb-114">フェデレーションを有効にする方法について詳しくは、展開ドキュメントまたは運用ドキュメントの「 <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Lync Server 2013 でのリモートユーザーアクセスを有効または無効</A> にする」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-114">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="fa5bb-115">また、フェデレーションされたユーザーアクセスを制御するユーザーポリシーを指定した場合、このポリシーは、Lync Server 2013 で有効になっていて、ポリシーを使用するように構成されているユーザーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-115">Additionally, if you specify a user policy to control federated user access, the policy applies only to users that are enabled for Lync Server 2013 and configured to use the policy.</span></span>



</div>

<div>

## <a name="to-configure-a-policy-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="fa5bb-116">フェデレーションドメインのユーザーによるアクセスをサポートするようにポリシーを構成するには</span><span class="sxs-lookup"><span data-stu-id="fa5bb-116">To configure a policy to support access by users of federated domains</span></span>

1.  <span data-ttu-id="fa5bb-117">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa5bb-118">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fa5bb-119">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fa5bb-120">左側のナビゲーションバーで、[ **外部ユーザーアクセス**] をクリックし、[ **外部アクセスポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-120">In the left navigation bar, click **External User Access**, and then click **External Access Policy**.</span></span>

4.  <span data-ttu-id="fa5bb-121">[ **外部アクセスポリシー** ] ページで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-121">On the **External Access Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="fa5bb-122">フェデレーションされたユーザーアクセスをサポートするようにグローバルポリシーを構成するには、グローバルポリシーをクリックし、[ **編集**] をクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-122">To configure the global policy to support federated user access, click the global policy, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="fa5bb-123">新しいサイトポリシーを作成するには、[ **新規** 作成] をクリックし、[ **サイトポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-123">To create a new site policy, click **New**, and then click **Site policy**.</span></span> <span data-ttu-id="fa5bb-124">[ **サイトの選択**] で、一覧から該当するサイトをクリックし、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-124">In **Select a Site**, click the appropriate site from the list and then click **OK**.</span></span>
    
      - <span data-ttu-id="fa5bb-125">新しいユーザーポリシーを作成するには、[ **新規** 作成] をクリックし、[ **ユーザーポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-125">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="fa5bb-126">[ **新しい外部アクセスポリシー**] で、[ **名前** ] フィールドに、ユーザーポリシーがどのようなものであるかを示す一意の名前を作成します (たとえば、フェデレーションされたドメインユーザーの通信を有効にするユーザーポリシーの **EnableFederatedUsers** )。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-126">In **New External Access Policy**, create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableFederatedUsers** for a user policy that enables communications for federated domain users).</span></span>
    
      - <span data-ttu-id="fa5bb-127">既存のポリシーを変更するには、表に記載されている適切なポリシーをクリックし、[ **編集**] をクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-127">To change an existing policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fa5bb-128">省略説明を追加または編集する場合は、ポリシーの情報を [ **説明**] で指定します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-128">(Optional) If you want to add or edit a description, specify the information for the policy in **Description**.</span></span>

6.  <span data-ttu-id="fa5bb-129">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-129">Do one of the following:</span></span>
    
      - <span data-ttu-id="fa5bb-130">ポリシーのフェデレーションされたユーザーアクセスを有効にするには、[ **フェデレーションユーザーとの通信を有効** にする] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-130">To enable federated user access for the policy, select the **Enable communications with federated users** check box.</span></span>
    
      - <span data-ttu-id="fa5bb-131">ポリシーのフェデレーションされたユーザーアクセスを無効にするには、[フェデレーションされ **たユーザーとの通信を有効** にする] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-131">To disable federated user access for the policy, clear the **Enable communications with federated users** check box.</span></span>

7.  <span data-ttu-id="fa5bb-132">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-132">Click **Commit**.</span></span>

<span data-ttu-id="fa5bb-133">フェデレーションされたユーザーアクセスを有効にするには、組織のフェデレーションのサポートも有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-133">To enable federated user access, you must also enable support for federation in your organization.</span></span> <span data-ttu-id="fa5bb-134">詳細については、「 [Lync Server 2013 でフェデレーションとパブリック IM 接続を有効または無効](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-134">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md).</span></span>

<span data-ttu-id="fa5bb-135">ユーザーポリシーの場合は、フェデレーションされたユーザーと共同作業できるようにするユーザーにもポリシーを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-135">If this is a user policy, you must also apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="fa5bb-136">詳細については、「 [Lync Server 2013 で lync を有効にしたユーザーに外部ユーザーアクセスポリシーを割り当てる](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-136">For details, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md).</span></span>

</div>

<div>

## <a name="to-configure-an-existing-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="fa5bb-137">Windows PowerShell を使用して既存のポリシーを構成し、フェデレーションドメインのユーザーによるアクセスをサポートするには</span><span class="sxs-lookup"><span data-stu-id="fa5bb-137">To configure an existing policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="fa5bb-138">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-138">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa5bb-139">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-139">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="fa5bb-140">Lync Server 管理シェルで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-140">Type the following in the Lync Server Management Shell:</span></span>
    
        Set-CsExternalAccessPolicy -Identity <name of global, site or user policy - policy must exist when using Set-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false> -EnablePublicCloudAccess <$true, $false> -EnablePublicCloudAudioVideoAccess <$true, $false> -EnableOutsideAccess <$true, $false>
    
    <span data-ttu-id="fa5bb-141">フェデレーションされたユーザーアクセスのグローバルポリシーを enabled に設定するコマンドの例。 XMPP ドメインへのアクセスは有効、リモートユーザーアクセスは有効、パブリックプロバイダーアクセスを有効にするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-141">An example command that will set the global policy for Federated user access to enabled, XMPP domain access to enabled, Remote user access to enabled, Public provider access to enabled, and grant the ability to use audio and video for public providers that support it:</span></span>
    
        Set-CsExternalAccessPolicy -Identity global -EnableFederationAccess $true -EnableXmppAccess $true -EnableOutsideAccess $true -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="fa5bb-142">パラメーター "EnablePublicCloudAudioVideoAccess" には、Lync Server のコントロールパネルで対応する選択がありません。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-142">The parameter “EnablePublicCloudAudioVideoAccess” does not have a corresponding selection in the Lync Server Control Panel</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-a-new-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="fa5bb-143">フェデレーションドメインのユーザーによるアクセスをサポートするために、Windows PowerShell を使用して新しいポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="fa5bb-143">To create a new policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="fa5bb-144">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-144">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa5bb-145">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-145">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="fa5bb-146">Lync Server 管理シェルで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-146">Type the following in the Lync Server Management Shell:</span></span>
    
        New-CsExtenalAccessPolicy -Identity <name of site or user policy - you cannot create a new global policy using New-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false> -EnablePublicCloudAccess <$true, $false> -EnablePublicCloudAudioVideoAccess <$true, $false> -EnableOutsideAccess <$true, $false>
    
    <span data-ttu-id="fa5bb-147">新しいサイトポリシーを作成する例:</span><span class="sxs-lookup"><span data-stu-id="fa5bb-147">An example of creating a new site policy:</span></span>
    
        New-CsExternalAccessPolicy -Identity site:Redmond -EnableFederationAccess $true -EnableXmppAccess $true -EnableOutsideAccess $true -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true

</div>

<div>

## <a name="to-delete-or-reset-a-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="fa5bb-148">フェデレーションドメインのユーザーによるアクセスをサポートするために Windows PowerShell を使用してポリシーを削除またはリセットするには</span><span class="sxs-lookup"><span data-stu-id="fa5bb-148">To delete or reset a policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="fa5bb-149">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-149">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa5bb-150">Lync Server 管理シェルで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-150">Type the following in the Lync Server Management Shell</span></span>
    
        Remove-CsExternalAccessPolicy -Identity <name of global, site or user policy> 
    
    <span data-ttu-id="fa5bb-151">グローバルポリシーをリセットする例です (グローバルポリシーではその設定のみを削除できます)。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-151">An example of resetting the global policy (The global policy can only have its setting removed.</span></span> <span data-ttu-id="fa5bb-152">ポリシーは削除できません):</span><span class="sxs-lookup"><span data-stu-id="fa5bb-152">The policy cannot be deleted):</span></span>
    
        Remove-CsExternalAccessPolicy -Identity global 
    
    <span data-ttu-id="fa5bb-153">サイトポリシーを削除するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-153">To remove a site policy, type:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity site:Redmond 
    
    <span data-ttu-id="fa5bb-154">サイトポリシーレドモンドを削除します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-154">Deletes the site policy Redmond.</span></span> <span data-ttu-id="fa5bb-155">UserEAPPolicy という名前のユーザーポリシーを削除するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fa5bb-155">To delete a user policy named UserEAPPolicy, type:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity UserEAPPolicy

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fa5bb-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa5bb-156">See Also</span></span>


[<span data-ttu-id="fa5bb-157">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="fa5bb-157">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
[<span data-ttu-id="fa5bb-158">Lync Server 2013 での Lync が有効なユーザーに対する外部ユーザー アクセス ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="fa5bb-158">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)  


[<span data-ttu-id="fa5bb-159">Lync Server 2013 での組織の SIP フェデレーション ドメインの管理</span><span class="sxs-lookup"><span data-stu-id="fa5bb-159">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="fa5bb-160">Lync Server 2013 での組織の SIP フェデレーション プロバイダーの管理</span><span class="sxs-lookup"><span data-stu-id="fa5bb-160">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
[<span data-ttu-id="fa5bb-161">Set-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5bb-161">Set-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy)  
[<span data-ttu-id="fa5bb-162">New-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5bb-162">New-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExternalAccessPolicy)  
[<span data-ttu-id="fa5bb-163">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5bb-163">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="fa5bb-164">Remove-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5bb-164">Remove-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy)  
[<span data-ttu-id="fa5bb-165">Grant-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5bb-165">Grant-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy)  
  

<span data-ttu-id="fa5bb-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa5bb-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

