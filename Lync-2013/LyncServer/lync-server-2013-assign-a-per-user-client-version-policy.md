---
title: 'Lync Server 2013: ユーザーごとのクライアントバージョンポリシーを割り当てる'
description: 'Lync Server 2013: ユーザーごとのクライアントバージョンポリシーを割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user client version policy
ms:assetid: f7e8ba2f-62dc-4e7d-8b63-682986f10240
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182607(v=OCS.15)
ms:contentKeyID: 48185868
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ec2fcbf9c005806a97dfbdceb22095fe0ff8f33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443189"
---
# <a name="assign-a-per-user-client-version-policy-in-lync-server-2013"></a><span data-ttu-id="5e5b5-103">Lync Server 2013 でユーザーごとのクライアントバージョンポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5e5b5-103">Assign a per-user client version policy in Lync Server 2013</span></span>

 


<span data-ttu-id="5e5b5-104">クライアントバージョンポリシーは、Lync Server コントロールパネルで構成できるユーザーアカウントの個別の設定の1つです。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-104">The client version policy is one of the individual settings of a user account that you can configure in the Lync Server Control Panel.</span></span>

<span data-ttu-id="5e5b5-105">1つまたは複数のユーザーごとのクライアントバージョンポリシーの展開は任意です。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-105">Deploying one or more per-user client version policies is optional.</span></span> <span data-ttu-id="5e5b5-106">グローバルレベルのクライアントバージョンポリシー、またはサイトレベルまたはプールレベルのクライアントバージョンポリシーのみを展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-106">You can also deploy only a global-level client version policy, or site-level or pool-level client version policies.</span></span> <span data-ttu-id="5e5b5-107">ユーザー単位のポリシーを展開する場合は、ポリシーをユーザー、グループ、または連絡先オブジェクトに明示的に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact object.</span></span> <span data-ttu-id="5e5b5-108">特定のサイトレベル、プールレベル、またはユーザーごとのポリシーが割り当てられていない場合、Lync Server 2013 への登録が許可されている既定のクライアントは、グローバルレベルクライアントのバージョンポリシーで定義されたものです。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-108">When no specific site-level, pool-level, or per-user policy is assigned, the default clients that are allowed to register with Lync Server 2013 are those defined in the global-level client version policy.</span></span>

<span data-ttu-id="5e5b5-109">ユーザーごとに1つ以上のバージョンのポリシーを作成した後、このトピックの手順を使用して、Lync Server への登録を許可するクライアントのバージョンを指定するポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-109">After creating at least one per-user client version policy, use the procedures in this topic to assign the policy that specifies the client versions that you want to allow to register with Lync Server.</span></span>

<span data-ttu-id="5e5b5-110">ユーザーごとのクライアントバージョンポリシーの作成について詳しくは、「 [Lync Server 2013 へのログオンに使用できるクライアントアプリケーションの指定](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-110">For details about creating per-user client version policies, see [Specifying the client applications that can be used to log on to Lync Server 2013](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md).</span></span>

## <a name="to-assign-a-per-user-client-version-policy"></a><span data-ttu-id="5e5b5-111">ユーザーごとのクライアントバージョンポリシーを割り当てるには</span><span class="sxs-lookup"><span data-stu-id="5e5b5-111">To assign a per-user client version policy</span></span>

1.  <span data-ttu-id="5e5b5-112">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5e5b5-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5e5b5-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5e5b5-115">左側のナビゲーション バーで [**ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-115">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="5e5b5-116">ユーザーを探すには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-116">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="5e5b5-117">[**ユーザーの検索**] ボックスに、表示名、名、姓、セキュリティ アカウント マネージャー (SAM) のアカウント名、SIP アドレス、またはユーザー アカウントの回線 URI (Uniform Resource Identifier) の全体か先頭部分の文字列を入力して、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-117">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="5e5b5-118">保存したクエリがある場合は、[**クエリを開く**] アイコンをクリックして、[**開く**] ダイアログ ボックスを使用してそのクエリ (.usf ファイル) を取得してから、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-118">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="5e5b5-119">(オプション) 結果を絞り込むための追加の検索条件を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-119">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="5e5b5-120">[**フィルターの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-120">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="5e5b5-121">ユーザーのプロパティを入力するか、ドロップダウン リストの矢印をクリックして選択し、プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-121">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="5e5b5-122">[**次の値に等しい**] ドロップダウン リストで、演算子 (例: [**次の値に等しい**]、[**次の値に等しくない**]) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-122">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="5e5b5-123">選択したユーザー プロパティによっては、検索結果のフィルターに使用する条件を入力するか、ドロップダウン リストの矢印をクリックして指定します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-123">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="5e5b5-124">クエリにその他の検索句を追加するには、[<STRONG>フィルターの追加</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-124">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="5e5b5-125">[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-125">Click **Find**.</span></span>

6.  <span data-ttu-id="5e5b5-126">検索結果のユーザーをクリックして、[**アクション**] をクリックしてから、[**ポリシーの割り当て**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-126">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="5e5b5-127">同じユーザーごとのクライアントバージョンポリシーを複数のユーザーに適用する場合は、検索結果で複数のユーザーを選び、[ <STRONG>操作</STRONG>] をクリックして、[ <STRONG>ポリシーの割り当て</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-127">If you want the same per-user client version policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="5e5b5-128">[ **ポリシーの割り当て**] の [ **クライアントのバージョンポリシー**] で、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-128">In **Assign Policies**, under **Client version policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="5e5b5-129">[<STRONG>ポリシーの割り当て</STRONG>] ダイアログボックスを使って構成できる複数のポリシーがあるため、ダイアログボックスのすべてのポリシーで既定で [ <STRONG> &lt; その &gt; まま</STRONG>実行する] が選択されています。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-129">Because there are multiple policies that you can configure by using the <STRONG>Assign Policies</STRONG> dialog box, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="5e5b5-130">この設定を変更しないで、以前にユーザーに割り当てたポリシーを使用して続行します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-130">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="5e5b5-131">[グローバルレベルポリシー] または [定義されている場合は、サイトレベルポリシーまたはプールレベルポリシー] のいずれかを Lync Server に自動的に選択させることができます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-131">Allow Lync Server to automatically choose either the global-level policy or, if defined, the site-level policy or pool-level policy.</span></span>
    
      - <span data-ttu-id="5e5b5-132">[ **クライアントバージョンポリシー** ] ページで以前に定義したユーザーごとのクライアントバージョンポリシーの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-132">Click the name of a per-user client version policy you previously defined on the **Client Version Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="5e5b5-133">割り当てるポリシーの決定に役立てるために、ポリシー名をクリックしたら [<STRONG>表示</STRONG>] をクリックして、ポリシーで定義されているユーザー権限やアクセス許可を確認します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-133">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="5e5b5-134">終了したら、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-134">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-client-version-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="5e5b5-135">Windows PowerShell コマンドレットを使用して Per-User クライアントのバージョンポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5e5b5-135">Assigning a Per-User Client Version Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="5e5b5-136">Grant-CsClientVersionPolicy コマンドレットを使用して、ユーザーごとのクライアントバージョンポリシーを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-136">You can assign per-user client version policies by using the Grant-CsClientVersionPolicy cmdlet.</span></span> <span data-ttu-id="5e5b5-137">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-137">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="5e5b5-138">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-138">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-client-version-policy-to-a-single-user"></a><span data-ttu-id="5e5b5-139">ユーザーごとのクライアントバージョンポリシーを1人のユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="5e5b5-139">To assign a per-user client version policy to a single user</span></span>

  - <span data-ttu-id="5e5b5-140">次のコマンドは、ユーザーごとのバージョンのポリシー RedmondClientVersionPolicy を Ken Myer に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-140">The following command assigns the per-user client version policy RedmondClientVersionPolicy to the user Ken Myer.</span></span>
    
        Grant-CsClientVersionPolicy -Identity "Ken Myer" -PolicyName "RedmondClientVersionPolicy"

## <a name="to-assign-a-per-user-client-version-policy-to-multiple-users"></a><span data-ttu-id="5e5b5-141">ユーザーごとのクライアントバージョンポリシーを複数のユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="5e5b5-141">To assign a per-user client version policy to multiple users</span></span>

  - <span data-ttu-id="5e5b5-142">このコマンドは、ボイスポリシー RedmondVoicePolicy を現在割り当てられているすべてのユーザーに、ユーザー別クライアントバージョンポリシー RedmondClientVersionPolicy を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-142">This command assigns the per-user client version policy RedmondClientVersionPolicy to all the users who are currently assigned the voice policy RedmondVoicePolicy.</span></span> <span data-ttu-id="5e5b5-143">このコマンドで使用される Filter パラメーターの詳細については、「 [ユーザーの取得](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) 」コマンドレットのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-143">For more information on the Filter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -Filter {VoicePolicy -eq "RedmondVoicePolicy"} | Grant-CsClientVersionPolicy -PolicyName "RedmondClientVersionPolicy"

## <a name="to-unassign-a-per-user-client-version-policy"></a><span data-ttu-id="5e5b5-144">ユーザーごとのクライアントバージョンポリシーを割り当て解除するには</span><span class="sxs-lookup"><span data-stu-id="5e5b5-144">To unassign a per-user client version policy</span></span>

  - <span data-ttu-id="5e5b5-145">次のコマンドは、以前に Ken Myer に割り当てられていたユーザーごとのクライアントバージョンポリシーを割り当て解除します。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-145">The following command unassigns any per-user client version policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="5e5b5-146">ユーザーごとのポリシーが割り当てられていない場合、Ken Myer はグローバルポリシー、彼のローカルサイトポリシー (存在する場合)、またはレジストラーに割り当てられているサービススコープポリシーを使って、自動的に管理されます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-146">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy, his local site policy (if one exists), or the service-scope policy assigned to his Registrar.</span></span> <span data-ttu-id="5e5b5-147">サービスのスコープポリシーは、どのサイトポリシーよりも優先され、サイトポリシーはグローバルポリシーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-147">A service scope policy takes precedence over any site policy, and a site policy takes precedence over the global policy.</span></span>
    
        Grant-CsClientVersionPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="5e5b5-148">詳細については、「 [Grant-CsClientVersionPolicy](https://technet.microsoft.com/library/gg412903\(v=ocs.15\)) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e5b5-148">For more information, see the help topic for the [Grant-CsClientVersionPolicy](https://technet.microsoft.com/library/gg412903\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e5b5-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e5b5-149">See Also</span></span>


[<span data-ttu-id="5e5b5-150">Lync Server 2013 でのユーザーごとのポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="5e5b5-150">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)  
[<span data-ttu-id="5e5b5-151">Lync Server 2013 でのデバイス、電話、クライアント アプリケーションの管理</span><span class="sxs-lookup"><span data-stu-id="5e5b5-151">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)

