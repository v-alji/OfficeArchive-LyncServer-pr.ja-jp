---
title: 'Lync Server 2013: ユーザー PIN 情報の表示'
description: 'Lync Server 2013: ユーザーの PIN 情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View user PIN information
ms:assetid: 59e38117-8112-4851-82ac-a746ffa0f89d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688067(v=OCS.15)
ms:contentKeyID: 49733661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 56f0808e645a2589841ff70d4923fa2de2c020ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444022"
---
# <a name="view-user-pin-information-in-lync-server-2013"></a><span data-ttu-id="75686-103">Lync Server 2013 でユーザーの PIN 情報を表示する</span><span class="sxs-lookup"><span data-stu-id="75686-103">View user PIN information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75686-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75686-104">

<span> </span></span></span>

<span data-ttu-id="75686-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="75686-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="75686-106">認証されたユーザーとしてダイヤルイン会議に参加するには、Lync Server 2013 ユーザーの Active Directory ドメインサービス (AD DS) の資格情報に暗証番号 (PIN) が必要です。</span><span class="sxs-lookup"><span data-stu-id="75686-106">To join a dial-in conference as an authenticated user, a Lync Server 2013 user with Active Directory Domain Services (AD DS) credentials requires a personal identification number (PIN).</span></span> <span data-ttu-id="75686-107">ユーザーの PIN 情報は、Lync Server 2013 コントロールパネルから表示できます。</span><span class="sxs-lookup"><span data-stu-id="75686-107">You can view a user’s PIN information from Lync Server 2013 Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="75686-108">PIN が設定されているかどうかや PIN の最終変更日時などの PIN 状態情報を表示することはできますが、PIN の状態を調べても最新の PIN は確認できません。</span><span class="sxs-lookup"><span data-stu-id="75686-108">You can view PIN status information such as whether the PIN has been set or when the PIN was last changed, but you cannot see the current PIN by looking at the PIN status.</span></span> <span data-ttu-id="75686-109">ユーザーが PIN を紛失した場合は、「<A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">ユーザーのダイヤルイン会議 PIN を Lync Server 2013 で設定</A>する」の手順に従ってリセットできます。</span><span class="sxs-lookup"><span data-stu-id="75686-109">If a user has lost their PIN, you can reset it by following the procedures in <A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">Set a user's dial-in conferencing PIN in Lync Server 2013</A></span></span>



</div>

<div>

## <a name="to-view-a-users-pin-in-lync-server-control-panel"></a><span data-ttu-id="75686-110">Lync Server コントロールパネルでユーザーの PIN を表示するには</span><span class="sxs-lookup"><span data-stu-id="75686-110">To view a user’s PIN in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="75686-111">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="75686-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="75686-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="75686-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="75686-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="75686-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="75686-114">左側のナビゲーション バーで [**ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="75686-115">ユーザーを探すには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="75686-115">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="75686-116">[**ユーザーの検索**] ボックスに、表示名、名、姓、セキュリティ アカウント マネージャー (SAM) のアカウント名、SIP アドレス、またはユーザー アカウントの回線 URI (Uniform Resource Identifier) の全体か先頭部分の文字列を入力して、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-116">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="75686-117">保存したクエリがある場合は、[**クエリを開く**] アイコンをクリックして、[**開く**] ダイアログ ボックスを使用してそのクエリ (.usf ファイル) を取得してから、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-117">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="75686-118">(オプション) 結果を絞り込むための追加の検索条件を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="75686-118">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="75686-119">[**フィルターの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-119">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="75686-120">ユーザーのプロパティを入力するか、ドロップダウン リストの矢印をクリックして選択し、プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="75686-120">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="75686-121">[**次の値に等しい**] ドロップダウン リストで、演算子 (例: [**次の値に等しい**]、[**次の値に等しくない**]) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-121">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="75686-122">選択したユーザー プロパティに応じて、検索結果のフィルターに使用する条件を入力するか、ドロップダウン リストの矢印をクリックして指定します。</span><span class="sxs-lookup"><span data-stu-id="75686-122">Depending on the user property you selected, enter the criteria that you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="75686-123">クエリにその他の検索句を追加するには、[<STRONG>フィルターの追加</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-123">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="75686-124">[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-124">Click **Find**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="75686-p104">PIN がロックされている場合は、ロックを解除しないと PIN を設定できません。PIN のロックを解除するには、ユーザーをクリックし、[<STRONG>アクション</STRONG>] をクリックして、[<STRONG>PIN のロック解除</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-p104">If the PIN is locked, you must unlock the PIN before you can set it. To unlock the PIN, click the user, click <STRONG>Action</STRONG>, and then click <STRONG>Unlock PIN</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="75686-127">検索結果でユーザーをクリックし、[**アクション**] をクリックして、[**PIN の状態を表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75686-127">Click a user in the search results, click **Action**, and then click **View PIN status**.</span></span>

</div>

<div>

## <a name="viewing-user-pin-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="75686-128">Windows PowerShell コマンドレットを使用してユーザーの PIN 情報を表示する</span><span class="sxs-lookup"><span data-stu-id="75686-128">Viewing User PIN Information by Using Windows PowerShell cmdlets</span></span>

<span data-ttu-id="75686-129">Get-CsClientPinInfo コマンドレットを使用して、ユーザーの PIN 情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="75686-129">You can view user PIN information by using the Get-CsClientPinInfo cmdlet.</span></span> <span data-ttu-id="75686-130">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="75686-130">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="75686-131">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="75686-131">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-user-pin-information"></a><span data-ttu-id="75686-132">ユーザーの PIN 情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="75686-132">To view user PIN information</span></span>

  - <span data-ttu-id="75686-133">ユーザーの PIN 情報を表示するには、Lync Server 管理シェルで次のようなコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="75686-133">To view PIN information for a user, type a command similar to the following in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsClientPinInfo -Identity "Ken Myer"
    
    <span data-ttu-id="75686-134">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="75686-134">That will return information similar to this:</span></span>
    
        Identity          : sip:kenmyer@litwareinc.com
        IsPinSet          : False
        IsLockedOut       : False
        LastPinChangeTime : 9/25/2012 1:35:03 PM
        PinExpirationTime :

</div>

<span data-ttu-id="75686-135">詳細については、 [CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75686-135">For more information, see the help topic for the [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="75686-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="75686-136">See Also</span></span>


[<span data-ttu-id="75686-137">Lync Server 2013 でユーザーのダイヤルイン会議の PIN を設定する</span><span class="sxs-lookup"><span data-stu-id="75686-137">Set a user's dial-in conferencing PIN in Lync Server 2013</span></span>](lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md)  
[<span data-ttu-id="75686-138">Lync Server 2013 でユーザー PIN をロックまたはロック解除する</span><span class="sxs-lookup"><span data-stu-id="75686-138">Lock or unlock a user PIN in Lync Server 2013</span></span>](lync-server-2013-lock-or-unlock-a-user-pin.md)  
  

<span data-ttu-id="75686-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75686-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

