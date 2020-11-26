---
title: 'Lync Server 2013: ユーザーごとの会議ポリシーを割り当てる'
description: 'Lync Server 2013: ユーザーごとの会議ポリシーを割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user conferencing policy
ms:assetid: 72f12c72-65f7-44fe-ab81-0f57cb2f87d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521015(v=OCS.15)
ms:contentKeyID: 48184475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819d1431a2a7a921ff8c306c47c8b5f86bf5d5bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440515"
---
# <a name="assign-a-per-user-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="1517b-103">Lync Server 2013 でユーザーごとの会議ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="1517b-103">Assign a per-user conferencing policy in Lync Server 2013</span></span>

 


<span data-ttu-id="1517b-104">会議ポリシーは、Lync Server コントロールパネルで構成できるユーザーアカウントの個別の設定の1つです。</span><span class="sxs-lookup"><span data-stu-id="1517b-104">The conferencing policy is one of the individual settings of a user account that you can configure in Lync Server Control Panel.</span></span>

<span data-ttu-id="1517b-105">ユーザーごとの会議のポリシーの展開は任意です。</span><span class="sxs-lookup"><span data-stu-id="1517b-105">Deploying one or more per-user conferencing policies is optional.</span></span> <span data-ttu-id="1517b-106">グローバルレベルの会議ポリシーまたはサイトレベルの会議ポリシーのみを展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="1517b-106">You can also deploy only a global-level conferencing policy or site-level conferencing policy.</span></span> <span data-ttu-id="1517b-107">ユーザーごとのポリシーを展開する場合は、ユーザー、グループ、または連絡先オブジェクトに明示的に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1517b-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span> <span data-ttu-id="1517b-108">特定のサイトレベルまたはユーザーごとのポリシーが割り当てられていないときに、グローバルレベルの会議ポリシーで定義されているユーザーに対して、既定で自動的に会議のユーザー権限と権限が付与されます。</span><span class="sxs-lookup"><span data-stu-id="1517b-108">Conferencing user rights and permissions automatically default to those defined in the global-level conferencing policy when no specific site-level or per-user policy is assigned.</span></span>

<span data-ttu-id="1517b-109">ユーザーごとの会議ポリシーを1つ以上作成したら、このトピックの手順を使用して、特定のユーザーが開催した会議に対してサーバーに付与するユーザー権限と権限を指定するポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1517b-109">After creating at least one per-user conferencing policy, use the procedures in this topic to assign the policy that specifies the user rights and permissions that you want the server to grant to the meetings organized by a particular user.</span></span>

<span data-ttu-id="1517b-110">利用可能なすべての会議ポリシー設定の一覧については、「 [Lync Server 2013 の会議ポリシー設定リファレンス](lync-server-2013-conferencing-policy-settings-reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1517b-110">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<span data-ttu-id="1517b-111">会議ポリシーの作成の詳細については、「 [Lync Server 2013 で会議ポリシーを作成または変更](lync-server-2013-create-or-modify-a-conferencing-policy.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1517b-111">For details about creating conferencing policies, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy"></a><span data-ttu-id="1517b-112">ユーザーごとの会議ポリシーを割り当てるには</span><span class="sxs-lookup"><span data-stu-id="1517b-112">To assign a per-user conferencing policy</span></span>

1.  <span data-ttu-id="1517b-113">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1517b-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1517b-114">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1517b-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1517b-115">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="1517b-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1517b-116">左側のナビゲーション バーで [**ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="1517b-117">ユーザーを探すには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="1517b-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="1517b-118">[**ユーザーの検索**] ボックスに、表示名、名、姓、セキュリティ アカウント マネージャー (SAM) のアカウント名、SIP アドレス、またはユーザー アカウントの回線 URI (Uniform Resource Identifier) の全体か先頭部分の文字列を入力して、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="1517b-119">保存したクエリがある場合は、[**クエリを開く**] アイコンをクリックして、[**開く**] ダイアログ ボックスを使用してそのクエリ (.usf ファイル) を取得してから、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="1517b-120">(オプション) 結果を絞り込むための追加の検索条件を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="1517b-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="1517b-121">[**フィルターの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="1517b-122">ユーザーのプロパティを入力するか、ドロップダウン リストの矢印をクリックして選択し、プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="1517b-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="1517b-123">[**次の値に等しい**] ドロップダウン リストで、演算子 (例: [**次の値に等しい**]、[**次の値に等しくない**]) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="1517b-124">選択したユーザー プロパティによっては、検索結果のフィルターに使用する条件を入力するか、ドロップダウン リストの矢印をクリックして指定します。</span><span class="sxs-lookup"><span data-stu-id="1517b-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="1517b-125">クエリにその他の検索句を追加するには、[<STRONG>フィルターの追加</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="1517b-126">[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-126">Click **Find**.</span></span>

6.  <span data-ttu-id="1517b-127">検索結果のユーザーをクリックして、[**アクション**] をクリックしてから、[**ポリシーの割り当て**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="1517b-128">同じユーザーごとの会議ポリシーを複数のユーザーに適用する場合は、検索結果で複数のユーザーを選び、[ <STRONG>操作</STRONG>] をクリックして、[ <STRONG>ポリシーの割り当て</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-128">If you want the same per-user conferencing policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="1517b-129">[ **ポリシーの割り当て**] の [ **会議ポリシー**] で、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1517b-129">In **Assign Policies**, under **Conferencing policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="1517b-130">[<STRONG>ポリシーの割り当て</STRONG>] で構成できる複数のポリシーがあるため、ダイアログボックスのすべてのポリシーで既定で [ <STRONG> &lt; その &gt; まま保持</STRONG>] が選択されています。</span><span class="sxs-lookup"><span data-stu-id="1517b-130">Because there are multiple policies that you can configure in <STRONG>Assign Policies</STRONG>, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="1517b-131">この設定を変更しないで、以前にユーザーに割り当てたポリシーを使用して続行します。</span><span class="sxs-lookup"><span data-stu-id="1517b-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="1517b-132">[ **\<Automatic\>** Lync Server 2013 でグローバルレベルポリシー] または [定義されている場合はサイトレベルポリシー] のいずれかを自動的に選択することを選択します。</span><span class="sxs-lookup"><span data-stu-id="1517b-132">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="1517b-133">[ **会議ポリシー** ] ページで以前に定義したユーザーごとの会議ポリシーの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-133">Click the name of a per-user conferencing policy you previously defined on the **Conferencing Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="1517b-134">割り当てるポリシーの決定に役立てるために、ポリシー名をクリックしたら [<STRONG>表示</STRONG>] をクリックして、ポリシーで定義されているユーザー権限やアクセス許可を確認します。</span><span class="sxs-lookup"><span data-stu-id="1517b-134">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="1517b-135">終了したら、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1517b-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-conferencing-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="1517b-136">Windows PowerShell コマンドレットを使用して Per-User 会議ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="1517b-136">Assigning a Per-User Conferencing Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="1517b-137">ユーザーごとの会議ポリシーは、Windows PowerShell と Grant-CsConferencingPolicy コマンドレットを使用して割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="1517b-137">Per-user conferencing policies can be assigned by using Windows PowerShell and the Grant-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="1517b-138">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="1517b-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="1517b-139">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="1517b-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy-to-a-single-user"></a><span data-ttu-id="1517b-140">ユーザーごとの会議ポリシーを1人のユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="1517b-140">To assign a per-user conferencing policy to a single user</span></span>

  - <span data-ttu-id="1517b-141">次のコマンドを実行すると、ユーザーごとの会議ポリシー RedmondConferencingPolicy が Ken Myer に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1517b-141">The following command assigns the per-user conferencing policy RedmondConferencingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName "RedmondConferencingPolicy"

## <a name="to-assign-a-per-user-conferencing-policy-to-multiple-users"></a><span data-ttu-id="1517b-142">ユーザーごとの会議ポリシーを複数のユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="1517b-142">To assign a per-user conferencing policy to multiple users</span></span>

  - <span data-ttu-id="1517b-143">このコマンドを実行すると、ユーザーごとの会議ポリシー HRConferencingPolicy が人事部で作業するすべてのユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1517b-143">This command assigns the per-user conferencing policy HRConferencingPolicy to all the users who work for the Human Resources department.</span></span> <span data-ttu-id="1517b-144">このコマンドで使用される LdapFilter パラメーターの詳細については、「 [ユーザーの取得](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) 」コマンドレットのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1517b-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Human Resources" | Grant-CsConferencingPolicy -PolicyName "HRConferencingPolicy"

## <a name="to-unassign-a-per-user-conferencing-policy"></a><span data-ttu-id="1517b-145">ユーザーごとの会議ポリシーを割り当て解除するには</span><span class="sxs-lookup"><span data-stu-id="1517b-145">To unassign a per-user conferencing policy</span></span>

  - <span data-ttu-id="1517b-146">次のコマンドは、以前に Ken Myer に割り当てられているユーザーごとの会議ポリシーを割り当て解除します。</span><span class="sxs-lookup"><span data-stu-id="1517b-146">The following command unassigns any per-user conferencing policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="1517b-147">ユーザー単位の PIN ポリシーが割り当て解除された後、Ken Myer は、グローバル ポリシー、または存在する場合は Ken Myer のローカル サイト ポリシーによって、自動的に管理されます。</span><span class="sxs-lookup"><span data-stu-id="1517b-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="1517b-148">サイト ポリシーは、グローバル ポリシーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="1517b-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="1517b-149">詳細については、「 [Grant-set-csconferencingpolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1517b-149">For more information, see the help topic for the [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="1517b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="1517b-150">See Also</span></span>


[<span data-ttu-id="1517b-151">Lync Server 2013 で会議ポリシーを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="1517b-151">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)  


[<span data-ttu-id="1517b-152">Lync Server 2013 でのユーザーごとのポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="1517b-152">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

