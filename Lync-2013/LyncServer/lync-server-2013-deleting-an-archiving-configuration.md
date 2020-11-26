---
title: 'Lync Server 2013: アーカイブ構成の削除'
description: 'Lync Server 2013: アーカイブ構成を削除しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving configuration
ms:assetid: a8744d39-5cf2-474c-9a99-a0f3a37f846f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205167(v=OCS.15)
ms:contentKeyID: 48185093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bb267c119b49c9bbf06f365c3bdf2cbab459628
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430379"
---
# <a name="deleting-an-archiving-configuration-in-lync-server-2013"></a><span data-ttu-id="80ad2-103">Lync Server 2013 でアーカイブ構成を削除する</span><span class="sxs-lookup"><span data-stu-id="80ad2-103">Deleting an Archiving configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80ad2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80ad2-104">

<span> </span></span></span>

<span data-ttu-id="80ad2-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="80ad2-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="80ad2-106">サイト構成またはプール構成を削除できます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-106">You can delete a site configuration or pool configuration.</span></span> <span data-ttu-id="80ad2-107">グローバル構成を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="80ad2-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="80ad2-108">グローバル構成を削除すると、グローバル構成は自動的に既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-108">If you delete the global configuration, it is automatically reset to the default values.</span></span> <span data-ttu-id="80ad2-109">アーカイブ構成の実装方法について詳しくは、「指定できるオプションやアーカイブ構成の階層」をご覧ください。「計画ドキュメント、展開ドキュメント、または操作のドキュメントでの [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80ad2-109">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>

## <a name="to-delete-a-site-or-pool-configuration-for-archiving"></a><span data-ttu-id="80ad2-110">アーカイブ用のサイトまたはプールの構成を削除するには</span><span class="sxs-lookup"><span data-stu-id="80ad2-110">To delete a site or pool configuration for archiving</span></span>

1.  <span data-ttu-id="80ad2-111">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="80ad2-111">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="80ad2-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="80ad2-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="80ad2-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="80ad2-114">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ad2-114">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="80ad2-115">アーカイブ構成のリストで、削除するサイトまたはプールの構成をクリックし、[**編集**] をクリックして、[**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ad2-115">In the list of archiving configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="80ad2-116">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ad2-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="80ad2-117">Windows PowerShell コマンドレットを使用してアーカイブ構成設定を削除する</span><span class="sxs-lookup"><span data-stu-id="80ad2-117">Removing Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="80ad2-118">アーカイブ構成設定は、Windows PowerShell と **CsArchivingConfiguration** コマンドレットを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-118">Archiving configuration settings can be deleted by using Windows PowerShell and the **Remove-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="80ad2-119">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="80ad2-120">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="80ad2-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-archiving-configuration-settings"></a><span data-ttu-id="80ad2-121">指定したアーカイブ構成設定のコレクションを削除するには</span><span class="sxs-lookup"><span data-stu-id="80ad2-121">To remove a specified collection of archiving configuration settings</span></span>

  - <span data-ttu-id="80ad2-122">次のコマンドは、Redmond サイトに適用されているアーカイブ構成設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="80ad2-122">The following command removes the archiving configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-archiving-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="80ad2-123">サイトの範囲に適用されているすべてのアーカイブ構成設定を削除するには</span><span class="sxs-lookup"><span data-stu-id="80ad2-123">To remove all the archiving configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="80ad2-124">このコマンドにより、サービスの範囲に適用されているすべてのアーカイブ構成設定が削除されます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-124">This command removes all the archiving configuration settings applied to the service scope:</span></span>
    
        Get-CsArchivingConfiguration -Filter "site:*" | Remove-CsArchivingConfiguration

</div>

<div>

## <a name="to-remove-archiving-configuration-settings-based-on-a-specified-property-value"></a><span data-ttu-id="80ad2-125">指定したプロパティ値に基づいてアーカイブ構成設定を削除するには</span><span class="sxs-lookup"><span data-stu-id="80ad2-125">To remove archiving configuration settings based on a specified property value</span></span>

  - <span data-ttu-id="80ad2-126">このコマンドを実行すると、Exchange アーカイブが無効になっているアーカイブ構成の設定がすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="80ad2-126">This command removes all the archiving configuration settings where Exchange archiving has been disabled:</span></span>
    
        Get-CsArchivingConfiguration | Where-Object {$_.EnableExchangeArchiving -eq $False} | Remove-CsArchivingConfiguration

</div>

<span data-ttu-id="80ad2-127">詳細については、 [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="80ad2-127">For more information, see the help topic for the [Remove-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80ad2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="80ad2-128">See Also</span></span>


[<span data-ttu-id="80ad2-129">Lync Server 2013 でのアーカイブのしくみ</span><span class="sxs-lookup"><span data-stu-id="80ad2-129">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="80ad2-130">Lync Server 2013 での内部および外部通信のアーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="80ad2-130">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="80ad2-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80ad2-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

