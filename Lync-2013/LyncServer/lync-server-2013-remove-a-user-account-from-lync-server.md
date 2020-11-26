---
title: 'Lync Server 2013: Lync Server からユーザーアカウントを削除する'
description: 'Lync Server 2013: Lync Server からユーザーアカウントを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove a user account from Lync Server
ms:assetid: 2f512aba-e358-45ae-af58-74312ee9c514
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688008(v=OCS.15)
ms:contentKeyID: 49733596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201eb8a7ba620792b92e2c7983890047c249ce86
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436448"
---
# <a name="remove-a-user-account-from-lync-server-2013"></a><span data-ttu-id="a0ad7-103">Lync Server 2013 からユーザーアカウントを削除する</span><span class="sxs-lookup"><span data-stu-id="a0ad7-103">Remove a user account from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0ad7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0ad7-104">

<span> </span></span></span>

<span data-ttu-id="a0ad7-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="a0ad7-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="a0ad7-106">Lync Server 2013 で、以前に追加したユーザーアカウントを削除するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-106">You can use the following procedure to remove a previously added user account in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a0ad7-107">ユーザーを削除すると、ユーザーアカウントに対して構成した設定が失われます。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-107">Removing a user will cause you to lose any settings you configured for the user account.</span></span> <span data-ttu-id="a0ad7-108">代わりにユーザーアカウントを一時的に無効にする場合は、「 <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Lync Server 2013 のユーザーアカウントを無効にする、またはもう一度有効</A>にする」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-108">If you would like to temporarily disable a user account instead, see the topic <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-remove-a-user-account-by-using-lync-server-management-shell"></a><span data-ttu-id="a0ad7-109">Lync Server 管理シェルを使用してユーザーアカウントを削除するには</span><span class="sxs-lookup"><span data-stu-id="a0ad7-109">To remove a user account by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="a0ad7-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a0ad7-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a0ad7-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a0ad7-113">左側のナビゲーション バーで [**ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-113">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="a0ad7-114">[ **ユーザーの検索** ] ボックスで、無効または再度有効にするユーザーアカウントの表示名、名、姓、セキュリティアカウントマネージャー (SAM) アカウント名、SIP アドレス、または行の Uniform resource IDENTIFIER (URI) のすべてまたは最初の部分を入力して、[ **検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-114">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to disable or re-enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="a0ad7-115">テーブルで、削除するユーザーアカウントをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-115">In the table, click the user account that you want to remove.</span></span>

6.  <span data-ttu-id="a0ad7-116">[ **操作** ] メニューの [ **Lync Server から削除**] を選択すると、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-116">On the **Action** menu, select **Remove from Lync Server**, and a dialog box appears.</span></span>

7.  <span data-ttu-id="a0ad7-117">ダイアログボックスで、[ **OK** ] を選択してユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-117">From the dialog box, select **OK** to remove the user.</span></span>

</div>

<div>

## <a name="removing-user-accounts-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a0ad7-118">Windows PowerShell コマンドレットを使用してユーザーアカウントを削除する</span><span class="sxs-lookup"><span data-stu-id="a0ad7-118">Removing User Accounts by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a0ad7-119">Disable-CsUser コマンドレットを使用して、ユーザーアカウントを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-119">You can remove user accounts by using the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="a0ad7-120">このコマンドレットは、Lync Server 2013 Management Shell またはリモートセッション Windows PowerShell から実行できます。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="a0ad7-121">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-user-account"></a><span data-ttu-id="a0ad7-122">ユーザーアカウントを削除するには</span><span class="sxs-lookup"><span data-stu-id="a0ad7-122">To remove a user account</span></span>

  - <span data-ttu-id="a0ad7-123">ユーザーアカウントを削除するには、Disable-CsUser コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-123">To remove a user account, use the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="a0ad7-124">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-124">For example:</span></span>
    
        Disable-CsUser -Identity "Ken Myer"
    
    <span data-ttu-id="a0ad7-125">このコマンドが実行されると、アカウントとその前の設定を再び有効にする方法はありません。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-125">After this command has run there is no way to re-enable the account and its previous settings.</span></span> <span data-ttu-id="a0ad7-126">代わりに、Enable-CsUser コマンドレットを使用して、Ken Myer の新しいアカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-126">Instead, you will need to use the Enable-CsUser cmdlet to create a brand-new account for Ken Myer.</span></span>

</div>

<span data-ttu-id="a0ad7-127">詳細については、「 [ユーザーの無効化](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-127">For more information, see the help topic for the [Disable-CsUser](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a0ad7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0ad7-128">See Also</span></span>


[<span data-ttu-id="a0ad7-129">Lync Server 2013 のユーザーアカウントを無効にするか、再び有効にする</span><span class="sxs-lookup"><span data-stu-id="a0ad7-129">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  


[<span data-ttu-id="a0ad7-130">Lync Server 2013 のユーザーを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="a0ad7-130">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="a0ad7-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0ad7-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

