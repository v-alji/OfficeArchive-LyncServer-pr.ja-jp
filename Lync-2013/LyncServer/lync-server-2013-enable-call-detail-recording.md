---
title: 'Lync Server 2013: 通話の詳細の記録を有効にする'
description: 'Lync Server 2013: 通話の詳細の記録を有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable call detail recording
ms:assetid: 3b28e432-596f-45a5-a070-577d6fa748d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520980(v=OCS.15)
ms:contentKeyID: 48183865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d565c78571e34cead61777381875c9c8d23dae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399308"
---
# <a name="enable-call-detail-recording-in-lync-server-2013"></a><span data-ttu-id="3516b-103">Lync Server 2013 での通話の詳細記録を有効にする</span><span class="sxs-lookup"><span data-stu-id="3516b-103">Enable call detail recording in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3516b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3516b-104">

<span> </span></span></span>

<span data-ttu-id="3516b-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3516b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3516b-p101">通話詳細記録 (CDR) は、インスタント メッセージング、ボイス オーバー IP (VoIP) 通話、アプリケーション共有、ファイル送信などのピアツーピア アクティビティ、および会議に関する使用状況および診断情報を記録します。使用状況データは投資収益率 (ROI) の計算に、診断データはピアツーピア アクティビティおよび会議のトラブルシューティングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="3516b-p101">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings. The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span>

<span data-ttu-id="3516b-108">組織全体または組織内の各サイトで CDR を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3516b-108">Use the following procedure to enable CDR for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3516b-109">CDR を有効にするには、監視および監視データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3516b-109">In order to enable CDR you must configure monitoring and a monitoring database.</span></span> <span data-ttu-id="3516b-110">詳細については、「 <A href="lync-server-2013-deploying-monitoring.md">Lync Server 2013 での監視の展開</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3516b-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-cdr-with-lync-server-control-panel"></a><span data-ttu-id="3516b-111">Lync Server コントロールパネルで CDR を有効にするには</span><span class="sxs-lookup"><span data-stu-id="3516b-111">To enable CDR with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="3516b-112">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="3516b-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="3516b-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3516b-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3516b-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3516b-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3516b-115">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**通話詳細記録**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3516b-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="3516b-116">[**通話詳細記録**] ページで、表から該当するサイトをクリックして、[**アクション**] をクリックし、[**CDR の有効化**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3516b-116">On the **Call Detail Recording** page, click the appropriate site from the table, click **Action**, and then click **Enable CDR**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3516b-117">CDR は、既定では有効になっています。</span><span class="sxs-lookup"><span data-stu-id="3516b-117">CDR is enabled by default.</span></span>

    
    </div>

</div>

<div>

## <a name="enabling-cdr-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3516b-118">Windows PowerShell コマンドレットを使用して CDR を有効にする</span><span class="sxs-lookup"><span data-stu-id="3516b-118">Enabling CDR by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3516b-119">CDR を有効にするには、Windows PowerShell と **CsCdrConfiguration** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="3516b-119">You can enable CDR by using Windows PowerShell and the **Set-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="3516b-120">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="3516b-120">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3516b-121">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="3516b-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-cdr-for-a-single-location"></a><span data-ttu-id="3516b-122">1 つの場所の CDR を有効にするには</span><span class="sxs-lookup"><span data-stu-id="3516b-122">To enable CDR for a single location</span></span>

  - <span data-ttu-id="3516b-123">CDR を無効にするには、EnableCDR パラメーターを True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="3516b-123">To disable CDR, set the EnableCDR parameter to True ($True).</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $True

</div>

<div>

## <a name="to-disable-cdr-for-a-single-location"></a><span data-ttu-id="3516b-124">1 つの場所の CDR を無効にするには</span><span class="sxs-lookup"><span data-stu-id="3516b-124">To disable CDR for a single location</span></span>

  - <span data-ttu-id="3516b-p105">CDR を無効にするには、EnableCDR パラメーターを False ($False) に設定します。CDR を無効にしても、監視がアンインストールされることはありません。CDR データの収集と保存が一時停止されます。</span><span class="sxs-lookup"><span data-stu-id="3516b-p105">To disable CDR, set the EnableCDR parameter to False ($False). Disabling CDR does not uninstall monitoring. It pauses the collection and storage of CDR data.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-cdr-in-multiple-locations"></a><span data-ttu-id="3516b-128">1 つのコマンドで複数の場所にある CDR を有効にするには</span><span class="sxs-lookup"><span data-stu-id="3516b-128">To use a single command to enable CDR in multiple locations</span></span>

  - <span data-ttu-id="3516b-129">このコマンドによって、組織で現在使用されているすべての CDR 構成設定の CDR が有効になります。</span><span class="sxs-lookup"><span data-stu-id="3516b-129">This command enables CDR for all the CDR configuration settings currently in use in your organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration "site:Redmond" -EnableCDR $True

</div>

<span data-ttu-id="3516b-130">詳細については、 [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3516b-130">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3516b-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="3516b-131">See Also</span></span>


[<span data-ttu-id="3516b-132">Lync Server 2013 での監視の計画</span><span class="sxs-lookup"><span data-stu-id="3516b-132">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="3516b-133">Lync Server 2013 での監視の展開</span><span class="sxs-lookup"><span data-stu-id="3516b-133">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="3516b-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3516b-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

