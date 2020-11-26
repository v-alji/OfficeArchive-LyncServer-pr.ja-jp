---
title: 'Lync Server 2013: デバイス更新ルールを復元する'
description: 'Lync Server 2013: デバイス更新ルールを復元します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restore a Device Update rule
ms:assetid: ac490baf-c7a0-48d9-8fd0-ba5729489341
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994061(v=OCS.15)
ms:contentKeyID: 51803972
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3696bc7e074bfd7bea04b08246f07e107d4d0b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442678"
---
# <a name="restore-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="99914-103">Lync Server 2013 でデバイス更新ルールを復元する</span><span class="sxs-lookup"><span data-stu-id="99914-103">Restore a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99914-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99914-104">

<span> </span></span></span>

<span data-ttu-id="99914-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="99914-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="99914-106">展開したデバイスからデバイス更新ルールをアンインストールするには、デバイスを復元します。</span><span class="sxs-lookup"><span data-stu-id="99914-106">To uninstall a device update rule from the devices in your deployment, restore it.</span></span> <span data-ttu-id="99914-107">デバイス更新ルールを復元すると、更新プログラムがアンインストールされ、そのルールの以前のバージョンが再インストールされます。</span><span class="sxs-lookup"><span data-stu-id="99914-107">Restoring a device update rule both uninstalls the update and reinstalls the previous version of that rule.</span></span>

<span data-ttu-id="99914-108">Lync Server コントロールパネルまたは Windows PowerShell を使用して、デバイス更新ルールを復元することができます。</span><span class="sxs-lookup"><span data-stu-id="99914-108">You can restore a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>

## <a name="to-restore-device-update-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="99914-109">Lync Server コントロールパネルを使用してデバイス更新ルールを復元するには</span><span class="sxs-lookup"><span data-stu-id="99914-109">To restore device update rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="99914-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="99914-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="99914-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="99914-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="99914-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="99914-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="99914-113">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **デバイスの更新** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="99914-113">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="99914-114">[ **デバイス更新** ] ページで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="99914-114">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="99914-115">1つのルールを復元するには、そのルールを選びます。</span><span class="sxs-lookup"><span data-stu-id="99914-115">To restore one rule, select that rule.</span></span>
    
      - <span data-ttu-id="99914-116">すべてのルールを復元するには、[ **編集**] をクリックし、[ **すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99914-116">To restore all rules, click **Edit**, and then click **Select All**.</span></span>

5.  <span data-ttu-id="99914-117">[ **操作** ] メニューをクリックし、[ **復元**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99914-117">Click the **Action** menu, and then click **Restore**.</span></span>

</div>

<div>

## <a name="restoring-device-update-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="99914-118">Windows PowerShell コマンドレットを使用してデバイス更新ルールを復元する</span><span class="sxs-lookup"><span data-stu-id="99914-118">Restoring Device Update Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="99914-119">デバイス更新ルールは、Windows PowerShell と **CsDeviceUpdateRule** コマンドレットを使用して復元することもできます。</span><span class="sxs-lookup"><span data-stu-id="99914-119">Device updates rules can also be restored by using Windows PowerShell and the **Restore-CsDeviceUpdateRule** cmdlet..</span></span> <span data-ttu-id="99914-120">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="99914-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="99914-121">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。</span><span class="sxs-lookup"><span data-stu-id="99914-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-restore-a-single-device-update-rule-on-a-server"></a><span data-ttu-id="99914-122">サーバー上の1つのデバイス更新ルールを復元するには</span><span class="sxs-lookup"><span data-stu-id="99914-122">To restore a single device update rule on a server</span></span>

  - <span data-ttu-id="99914-123">次のコマンドは、デバイス更新ルール d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 を Web サーバー atl-cs-001.litwareinc.com に復元します。</span><span class="sxs-lookup"><span data-stu-id="99914-123">The following command restores the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Restore-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-restore-all-the-device-update-rules-on-a-server"></a><span data-ttu-id="99914-124">サーバー上のすべてのデバイス更新ルールを復元するには</span><span class="sxs-lookup"><span data-stu-id="99914-124">To restore all the device update rules on a server</span></span>

  - <span data-ttu-id="99914-125">このコマンドは、web サーバー atl-cs-001.litwareinc.com 上のすべてのデバイス更新ルールを復元します。</span><span class="sxs-lookup"><span data-stu-id="99914-125">This command restores all the device update rules on the web server atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*" | Restore-CsDeviceUpdateRule

</div>

<span data-ttu-id="99914-126">詳細については、「 [CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Restore-CsDeviceUpdateRule) コマンドレットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99914-126">For details, see the Help topic for the [Restore-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Restore-CsDeviceUpdateRule) cmdlet.</span></span>

<span data-ttu-id="99914-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99914-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

