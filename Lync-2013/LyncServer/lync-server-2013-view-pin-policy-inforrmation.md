---
title: 'Lync Server 2013: PIN ポリシーの inforrmation を表示する'
description: 'Lync Server 2013: PIN ポリシーの inforrmation を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View PIN policy inforrmation
ms:assetid: 1d48b060-d77f-44ee-b70f-3ce128aedac4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687985(v=OCS.15)
ms:contentKeyID: 49733575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d60125663bed2b79921de62663865c56b6a27786
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444099"
---
# <a name="view-pin-policy-inforrmation-in-lync-server-2013"></a><span data-ttu-id="712be-103">Lync Server 2013 で PIN ポリシーの inforrmation を表示する</span><span class="sxs-lookup"><span data-stu-id="712be-103">View PIN policy inforrmation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="712be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="712be-104">

<span> </span></span></span>

<span data-ttu-id="712be-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="712be-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="712be-106">[ **Pin ポリシー** ] タブを使って、IP 電話で Lync 2013 に接続しているユーザーの暗証番号 (pin) の認証を表示できます。</span><span class="sxs-lookup"><span data-stu-id="712be-106">You can use the **PIN Policy** tab to view personal identification number (PIN) authentication of users who are connecting to Lync 2013 with IP Phones.</span></span> <span data-ttu-id="712be-107">PIN 認証を使用するには、Web サービス設定で [**PIN 認証を有効にする**] が選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="712be-107">To use PIN authentication, make sure that **Enable PIN Authentication** is selected in Web Service settings.</span></span> <span data-ttu-id="712be-108">詳細については、「 [Lync Server 2013 で既存の Web サービスの構成の設定を変更](lync-server-2013-modify-existing-web-service-configuration-settings.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="712be-108">For details, see [Modify existing Web Service configuration settings in Lync Server 2013](lync-server-2013-modify-existing-web-service-configuration-settings.md).</span></span>

<span data-ttu-id="712be-109">ユーザー レベルまたはサイト レベルの PIN ポリシーを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712be-109">Follow these steps to modify a user-level or a site-level PIN policy.</span></span>

<div>

## <a name="to-view-information-about-a-pin-policy-in-lync-server-control-panel"></a><span data-ttu-id="712be-110">Lync Server コントロールパネルの PIN ポリシーに関する情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="712be-110">To view information about a PIN policy in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="712be-111">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="712be-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="712be-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="712be-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="712be-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="712be-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="712be-114">左側のナビゲーション バーで [**セキュリティ**] をクリックし、[**PIN ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="712be-114">In the left navigation bar, click **Security** and then click **PIN Policy**.</span></span>

4.  <span data-ttu-id="712be-115">[**PIN ポリシー**] ページでポリシーをクリックし、[**編集**] に続いて [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="712be-115">On the **PIN Policy** page, click a policy, click **Edit**, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-pin-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="712be-116">Windows PowerShell コマンドレットを使用した PIN ポリシーの表示</span><span class="sxs-lookup"><span data-stu-id="712be-116">Viewing PIN Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="712be-117">Windows PowerShell と Get-CsPinPolicy コマンドレットを使用して、PIN ポリシーを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="712be-117">You can also view PIN policies by using Windows PowerShell and the Get-CsPinPolicy cmdlet.</span></span> <span data-ttu-id="712be-118">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="712be-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="712be-119">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="712be-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-pin-policies"></a><span data-ttu-id="712be-120">PIN ポリシーを表示するには</span><span class="sxs-lookup"><span data-stu-id="712be-120">To view PIN policies</span></span>

  - <span data-ttu-id="712be-121">すべての PIN ポリシーに関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="712be-121">To view information about all your PIN policies, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsPinPolicy
    
    <span data-ttu-id="712be-122">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="712be-122">That will return information similar to this:</span></span>
    
        Identity             : Global
        Description          :
        MinPasswordLength    : 5
        PINHistoryCount      : 0
        AllowCommonPatterns  : False
        PINLifetime          : 0
        MaximumLogonAttempts :

</div>

<span data-ttu-id="712be-123">詳細については、 [CsPinPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsPinPolicy) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="712be-123">For more information, see the help topic for the [Get-CsPinPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsPinPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="712be-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="712be-124">See Also</span></span>


[<span data-ttu-id="712be-125">Lync Server 2013 で既存の Web サービス構成の設定を変更する</span><span class="sxs-lookup"><span data-stu-id="712be-125">Modify existing Web Service configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-existing-web-service-configuration-settings.md)  
[<span data-ttu-id="712be-126">Lync Server 2013 で新しい PIN ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="712be-126">Create a new PIN policy in Lync Server 2013</span></span>](lync-server-2013-create-a-new-pin-policy.md)  
  

<span data-ttu-id="712be-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="712be-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

