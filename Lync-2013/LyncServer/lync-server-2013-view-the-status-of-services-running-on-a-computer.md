---
title: 'Lync Server 2013: コンピューターで実行されているサービスの状態を表示する'
description: 'Lync Server 2013: コンピューターで実行されているサービスの状態を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View the status of services running on a computer
ms:assetid: f41918e7-4c02-431e-840a-88a1f36ae499
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182606(v=OCS.15)
ms:contentKeyID: 48185804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22aeb13f2beb5d3b0ee5eec8109eceeb14e40213
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399200"
---
# <a name="view-the-status-of-services-running-on-a-computer-in-lync-server-2013"></a><span data-ttu-id="dd528-103">Lync Server 2013 のコンピューターで実行されているサービスの状態を表示する</span><span class="sxs-lookup"><span data-stu-id="dd528-103">View the status of services running on a computer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd528-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd528-104">

<span> </span></span></span>

<span data-ttu-id="dd528-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="dd528-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="dd528-106">Lync Server 2013 コントロールパネルを使用して、Lync Server トポロジで特定のコンピューターで実行されているすべてのサービスを表示し、各サービスの状態を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="dd528-106">You can use Lync Server 2013 Control Panel to view all the services that are running on a specific computer in your Lync Server topology and see the status of each service.</span></span>

<div>

## <a name="to-view-the-status-of-services-running-on-a-computer"></a><span data-ttu-id="dd528-107">コンピューターで実行されているサービスの状態を表示するには</span><span class="sxs-lookup"><span data-stu-id="dd528-107">To view the status of services running on a computer</span></span>

1.  <span data-ttu-id="dd528-108">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="dd528-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="dd528-109">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="dd528-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="dd528-110">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="dd528-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="dd528-111">左側のナビゲーションバーで、[ **トポロジ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd528-111">In the left navigation bar, click **Topology**.</span></span>

4.  <span data-ttu-id="dd528-112">[ **状態** ] ページで、必要に応じてリストを並べ替えるか検索して、目的のコンピューターを見つけ、コンピューター名をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd528-112">On the **Status** page, sort or search the list, as required, to find the computer you’re interested in, and then click the computer name.</span></span>

5.  <span data-ttu-id="dd528-113">次のいずれかの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="dd528-113">Do any of the following:</span></span>
    
      - <span data-ttu-id="dd528-114">コンピューター上で実行されているサービスの最新の状態を表示するには、[ **サービスの状態を取得** する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd528-114">To see the latest status of services running on the computer, click **Get service status**.</span></span>
    
      - <span data-ttu-id="dd528-115">コンピューター上で実行されている特定のサービスの一覧と各サービスの状態を表示するには、[ **プロパティ**] をクリックし、[ **閉じる** ] をクリックしてリストに戻ります。</span><span class="sxs-lookup"><span data-stu-id="dd528-115">To see a list of specific services running on the computer and the status of each service, click **Properties**, and then click **Close** to return to the list.</span></span>

</div>

<div>

## <a name="viewing-service-status-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="dd528-116">Windows PowerShell コマンドレットを使用してサービスの状態を表示する</span><span class="sxs-lookup"><span data-stu-id="dd528-116">Viewing Service Status by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="dd528-117">また、Windows PowerShell と、ユーザーの **取得-CsWindowsService** コマンドレットを使用して、サービスの状態を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd528-117">You can also view service status by using Windows PowerShell and the **Get-CsWindowsService** cmdlet.</span></span> <span data-ttu-id="dd528-118">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="dd528-118">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="dd528-119">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd528-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-service-status"></a><span data-ttu-id="dd528-120">サービスの状態を表示するには</span><span class="sxs-lookup"><span data-stu-id="dd528-120">To view service status</span></span>

  - <span data-ttu-id="dd528-121">コンピューターでサービスの状態を表示するには、Lync Server 管理シェルで次のようなコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="dd528-121">To view service status on a computer, type a command similar to the following in the Lync Server Management Shell and then press Enter:</span></span>
    
        Get-CsWindowsService -ComputerName atl-cs-001.litwareinc.com | Select-Object RoleName, Status
    
    <span data-ttu-id="dd528-122">このコマンドは、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="dd528-122">This command returns information similar to the following:</span></span>
    
        RoleName                                  Status
        --------                                  ------
        {W3SVC}                                   Running
        {CentralManagement}                       Running
        {ClsAgent}                                Running
        {Registrar, UserServer, EdgeServer}       Running
        {ApplicationServer}                       Running
        {ConferencingServer}                      Running
        {MediationServer}                         Running

</div>

<span data-ttu-id="dd528-123">詳細については、「 [CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd528-123">For details, see [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dd528-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd528-124">See Also</span></span>


[<span data-ttu-id="dd528-125">Lync Server 2013 でのデバイス、電話、クライアント アプリケーションの管理</span><span class="sxs-lookup"><span data-stu-id="dd528-125">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="dd528-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd528-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

