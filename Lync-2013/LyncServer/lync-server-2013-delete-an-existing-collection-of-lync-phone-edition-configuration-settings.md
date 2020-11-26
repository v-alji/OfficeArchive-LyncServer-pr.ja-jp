---
title: Lync Phone Edition の構成設定の既存のコレクションを削除する
description: 既存の Lync Phone エディション構成設定を削除します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of Lync Phone Edition configuration settings
ms:assetid: 1bfc427d-4dcd-4199-b25f-8d5cfec2164f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687984(v=OCS.15)
ms:contentKeyID: 49733574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5137590a37b8bbb47f7445d20639157953597ca6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430556"
---
# <a name="delete-an-existing-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="e48cb-103">Lync Server 2013 で既存の Lync Phone エディション構成の設定を削除する</span><span class="sxs-lookup"><span data-stu-id="e48cb-103">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e48cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e48cb-104">

<span> </span></span></span>

<span data-ttu-id="e48cb-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e48cb-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e48cb-106">Lync Phone Edition を実行しているデバイスの設定のコレクションを使用する必要がなくなった場合は、削除します。</span><span class="sxs-lookup"><span data-stu-id="e48cb-106">If you no longer want to use a collection of settings for devices running Lync Phone Edition, delete it.</span></span> <span data-ttu-id="e48cb-107">サイトのコレクションを削除すると、そのサイトの電話にグローバル設定が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e48cb-107">If you delete a collection for a site, the global settings will apply to the phones in that site.</span></span> <span data-ttu-id="e48cb-108">グローバルコレクションは削除できません。</span><span class="sxs-lookup"><span data-stu-id="e48cb-108">You cannot delete the global collection.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e48cb-109">コレクションを削除する代わりに、設定の一部を変更することが必要になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="e48cb-109">Instead of deleting a collection, you might just want to change some of the settings.</span></span> <span data-ttu-id="e48cb-110">その方法の詳細については、「lync <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">Server 2013 で Lync Phone Edition 構成設定のコレクションを作成または変更</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cb-110">For details about how to do so, see <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-delete-a-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="e48cb-111">Lync Phone エディション構成設定のコレクションを削除するには</span><span class="sxs-lookup"><span data-stu-id="e48cb-111">To delete a collection of Lync Phone Edition configuration settings</span></span>

1.  <span data-ttu-id="e48cb-112">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="e48cb-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e48cb-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="e48cb-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e48cb-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e48cb-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e48cb-115">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **デバイス構成** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48cb-115">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="e48cb-116">[ **デバイスの構成** ] ページで、削除するコレクションをクリックし、[ **編集** ] メニューをクリックして、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48cb-116">On the **Device Configuration** page, click the collection you want to delete, click the **Edit** menu, and then click **Delete**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e48cb-117">グローバルコレクションを削除した場合、設定は既定の設定に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e48cb-117">If you delete the global collection, the settings just revert to the default settings.</span></span> <span data-ttu-id="e48cb-118">コレクションは移動しません。</span><span class="sxs-lookup"><span data-stu-id="e48cb-118">The collection does not go away.</span></span>

    
    </div>

5.  <span data-ttu-id="e48cb-119">確認ボックスで [ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48cb-119">In the confirmation box, click **OK**.</span></span>

</div>

<div>

## <a name="removing-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e48cb-120">Windows PowerShell コマンドレットを使用した、Lync Phone Edition 構成設定の削除</span><span class="sxs-lookup"><span data-stu-id="e48cb-120">Removing Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e48cb-121">Lync Phone Edition の構成設定は、Windows PowerShell と **CsUCConfiguration** コマンドレットを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="e48cb-121">You can delete Lync Phone Edition configuration settings by using Windows PowerShell and the **Remove-CsUCConfiguration** cmdlet.</span></span> <span data-ttu-id="e48cb-122">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="e48cb-122">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e48cb-123">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cb-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="e48cb-124">指定した Lync Phone エディション構成設定のコレクションを削除するには</span><span class="sxs-lookup"><span data-stu-id="e48cb-124">To remove a specified collection of Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="e48cb-125">このコマンドは、Redmond サイトに適用されている UC 電話構成設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="e48cb-125">This command deletes the UC phone configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsUCPhoneConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="e48cb-126">サイトの範囲に適用されているすべての Lync Phone エディション構成設定を削除するには</span><span class="sxs-lookup"><span data-stu-id="e48cb-126">To remove all of the Lync Phone Edition configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="e48cb-127">このコマンドにより、サービスの範囲に適用されているすべての UC 電話構成設定が削除されます。</span><span class="sxs-lookup"><span data-stu-id="e48cb-127">This command removes all the UC phone configuration settings applied to the service scope:</span></span>
    
        Get-CsUCPhoneConfiguration -Filter "site:*" | Remove-CsUCPhoneConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-where-phone-locking-is-disabled"></a><span data-ttu-id="e48cb-128">電話のロックが無効になっている Lync Phone エディションの構成設定をすべて削除するには</span><span class="sxs-lookup"><span data-stu-id="e48cb-128">To remove all of the Lync Phone Edition configuration settings where phone locking is disabled</span></span>

  - <span data-ttu-id="e48cb-129">このコマンドは、電話のロックが無効になっている UC 電話構成設定のコレクションをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="e48cb-129">This command deletes any collection of UC phone configuration settings where phone locking has been disabled:</span></span>
    
        Get-CsUCPhoneConfiguration | Where-Object {$_.EnforcePhoneLock -eq $False} | Remove-CsUCPhoneConfiguration

</div>

<span data-ttu-id="e48cb-130">詳細については、「 [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cb-130">For details, see [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span></span>

<span data-ttu-id="e48cb-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e48cb-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

