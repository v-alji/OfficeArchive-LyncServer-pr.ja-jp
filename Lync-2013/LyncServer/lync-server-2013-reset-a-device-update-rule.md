---
title: 'Lync Server 2013: デバイス更新ルールをリセットする'
description: 'Lync Server 2013: デバイス更新ルールをリセットします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset a Device Update rule
ms:assetid: d1f597e7-dffd-4756-af07-10613a5d8729
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994069(v=OCS.15)
ms:contentKeyID: 51803980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a4d42b6aee8f4cb3fd93839b4a8575059ba71cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436371"
---
# <a name="reset-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="5aa5a-103">Lync Server 2013 でのデバイス更新ルールのリセット</span><span class="sxs-lookup"><span data-stu-id="5aa5a-103">Reset a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5aa5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5aa5a-104">

<span> </span></span></span>

<span data-ttu-id="5aa5a-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="5aa5a-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="5aa5a-106">テストデバイスで更新プログラムが動作しない場合は、デバイス更新ルールをリセットすることができます。これにより、ルールの保留状態が削除され、テストデバイスから更新プログラムがアンインストールされます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-106">If you don’t like the way that an update works on your test devices, you can reset the device update rule, which removes the rule’s pending status and uninstalls the update from the test devices.</span></span>

<span data-ttu-id="5aa5a-107">Lync Server コントロールパネルまたは Windows PowerShell を使用して、デバイス更新ルールを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-107">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5aa5a-108">既に承認済みの (ロールアウトされた) ルールを復元するには、それを復元します。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-108">To uninstall a rule that you’ve already approved (that is, rolled out), restore it.</span></span> <span data-ttu-id="5aa5a-109">詳細については、「 <A href="lync-server-2013-restore-a-device-update-rule.md">Lync Server 2013 でデバイス更新ルールを復元する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-109">For details, see <A href="lync-server-2013-restore-a-device-update-rule.md">Restore a Device Update rule in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="5aa5a-110">Lync Server コントロールパネルを使用してデバイス更新ルールをリセットするには</span><span class="sxs-lookup"><span data-stu-id="5aa5a-110">To reset a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="5aa5a-111">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5aa5a-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5aa5a-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5aa5a-114">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **デバイスの更新** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="5aa5a-115">[ **デバイス更新** ] ページで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-115">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="5aa5a-116">1つのルールをリセットするには、再設定するルールを選びます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-116">To reset one rule, select the rule you want to reset.</span></span>
    
      - <span data-ttu-id="5aa5a-117">すべてのルールをリセットするには、[ **編集** ] メニューの [ **すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-117">To reset all rules, on the **Edit** menu, click **Select All**.</span></span>
    
      - <span data-ttu-id="5aa5a-118">1つのブランドのすべてのルールをリセットするには、 **ブランド** の列メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-118">To reset all rules for one brand, use the **Brand** column menu.</span></span>

5.  <span data-ttu-id="5aa5a-119">[ **アクション**] をクリックし、[ **保留中の更新をキャンセル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-119">Click **Action**, and then click **Cancel pending updates**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="5aa5a-120">キャンセルしたデバイス更新ルールをロールアウトしたくない場合は、削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-120">If you’re sure you’ll never want to roll out the device update rule(s) that you cancelled, you might want to delete them.</span></span> <span data-ttu-id="5aa5a-121">詳細については、「 <A href="lync-server-2013-remove-a-device-update-rule.md">Lync Server 2013 でデバイス更新ルールを削除する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-121">For details, see <A href="lync-server-2013-remove-a-device-update-rule.md">Remove a Device Update rule in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="resetting-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="5aa5a-122">Windows PowerShell コマンドレットを使用してデバイス更新ルールをリセットする</span><span class="sxs-lookup"><span data-stu-id="5aa5a-122">Resetting a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="5aa5a-123">デバイス更新ルールは、Windows PowerShell と **CsDeviceUpdateRule** コマンドレットを使用してリセットすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-123">Device update rules can also be reset by using Windows PowerShell and the **Reset-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="5aa5a-124">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5aa5a-125">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-specific-device-update-rule-on-a-server"></a><span data-ttu-id="5aa5a-126">サーバー上の特定のデバイス更新ルールをリセットするには</span><span class="sxs-lookup"><span data-stu-id="5aa5a-126">To reset a specific device update rule on a server</span></span>

  - <span data-ttu-id="5aa5a-127">次のコマンドを実行すると、d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 の Web サーバーの atl-cs-001.litwareinc.com のデバイス更新ルールがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-127">The following command resets the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Reset-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-reset-all-the-device-update-rules-on-a-server"></a><span data-ttu-id="5aa5a-128">サーバー上のすべてのデバイス更新ルールをリセットするには</span><span class="sxs-lookup"><span data-stu-id="5aa5a-128">To reset all the device update rules on a server</span></span>

  - <span data-ttu-id="5aa5a-129">このコマンドを実行すると、Web サーバー atl-cs-001.litwareinc.com 上のすべてのデバイス更新ルールがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-129">This command resets all the device update rules on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"  | Reset-CsDeviceUpdateRule

</div>

<div>

## <a name="to-reset-all-the-device-updates-rules-that-have-a-specific-brand"></a><span data-ttu-id="5aa5a-130">特定のブランドを持つすべてのデバイス更新ルールをリセットするには</span><span class="sxs-lookup"><span data-stu-id="5aa5a-130">To reset all the device updates rules that have a specific brand</span></span>

  - <span data-ttu-id="5aa5a-131">この例では、組織全体で、Microsoft と同等のブランドを持つすべてのデバイス更新がリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-131">In this example, all the device updates throughout the organization that have a Brand equal to Microsoft are reset:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Reset-CsDeviceUpdateRule

</div>

<span data-ttu-id="5aa5a-132">詳細については、 [CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aa5a-132">For details, see the Help topic for the [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5aa5a-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="5aa5a-133">See Also</span></span>


[<span data-ttu-id="5aa5a-134">Lync Server 2013 でデバイス更新ルールを承認する</span><span class="sxs-lookup"><span data-stu-id="5aa5a-134">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="5aa5a-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5aa5a-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

