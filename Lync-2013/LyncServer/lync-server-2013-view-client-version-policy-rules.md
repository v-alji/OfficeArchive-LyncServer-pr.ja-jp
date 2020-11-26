---
title: 'Lync Server 2013: クライアントのバージョンポリシールールを表示する'
description: 'Lync Server 2013: クライアントのバージョンポリシールールを表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View client version policy rules
ms:assetid: f3a0215f-f72f-4e9b-a07b-25858dc4203a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923060(v=OCS.15)
ms:contentKeyID: 50675350
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e04075f136d53fe149c6b0655699324a99e0a52
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443399"
---
# <a name="view-client-version-policy-rules-in-lync-server-2013"></a><span data-ttu-id="4ebf0-103">Lync Server 2013 でクライアントのバージョンポリシールールを表示する</span><span class="sxs-lookup"><span data-stu-id="4ebf0-103">View client version policy rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ebf0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ebf0-104">

<span> </span></span></span>

<span data-ttu-id="4ebf0-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="4ebf0-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="4ebf0-106">クライアントのバージョンポリシーは、一連のクライアントバージョンポリシールールで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-106">A client version policy is made up of a set of client version policy rules.</span></span> <span data-ttu-id="4ebf0-107">これらのルールでは、ユーザーが特定のクライアントおよびクライアント バージョンでログオンしようとしたときに実行するアクションが定義されています。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-107">These rules define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span> <span data-ttu-id="4ebf0-108">Lync Server 2013 コントロールパネルまたは Lync Server 2013 管理シェルからクライアントのバージョンポリシールールを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-108">You can view client version policy rules from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-view-client-version-policy-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="4ebf0-109">Lync Server コントロールパネルを使用してクライアントのバージョンポリシールールを表示するには</span><span class="sxs-lookup"><span data-stu-id="4ebf0-109">To view client version policy rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="4ebf0-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4ebf0-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4ebf0-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4ebf0-113">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **クライアントバージョンポリシー** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-113">In the left navigation bar, click **Clients**, and then click the **Client Version Policy** navigation button.</span></span>

4.  <span data-ttu-id="4ebf0-114">[ **クライアントのバージョンポリシー** ] ページで、表示するクライアントのバージョンポリシーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-114">On the **Client Version Policy** page, double-click a client version policy you want to view.</span></span>

5.  <span data-ttu-id="4ebf0-115">[ **クライアントのバージョンポリシーの編集** ] ページにルールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-115">The rules appear on the **Edit Client Version Policy** page.</span></span> <span data-ttu-id="4ebf0-116">ルールの詳細を表示するには、ルールを選択し、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-116">To view the details for a rule, select the rule, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-client-version-policy-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="4ebf0-117">Windows PowerShell コマンドレットを使用してクライアントのバージョンポリシールールを表示する</span><span class="sxs-lookup"><span data-stu-id="4ebf0-117">Viewing Client Version Policy Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="4ebf0-118">Lync Server 管理シェルと、 **CsClientVersionPolicyRule rule** コマンドレットを使用して、クライアントのバージョンポリシールールを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-118">You can view client version policy rules by using Lync Server Management Shell and the **Get-CsClientVersionPolicyRule** cmdlet.</span></span> <span data-ttu-id="4ebf0-119">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="4ebf0-120">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-client-version-policy-rules"></a><span data-ttu-id="4ebf0-121">クライアントのバージョンポリシールールを表示するには</span><span class="sxs-lookup"><span data-stu-id="4ebf0-121">To view client version policy rules</span></span>

  - <span data-ttu-id="4ebf0-122">クライアントのバージョンポリシールールを表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-122">To view the client version policy rules, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsClientVersionPolicyRule
    
    <span data-ttu-id="4ebf0-123">これは、構成されている各ルールについて、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-123">That will return information similar to this for each configured rule:</span></span>
    
        Identity          : Global/2336c611-a243-4c5d-994b-eea8a524d0e4
        Priority          : 0
        RuleId            : 2336c611-a243-4c5d-994b-eea8a524d0e4
        Description       :
        Action            : Block
        ActionUrl         :
        MajorVersion      : 1
        MinorVersion      : 3
        BuildNumber       :
        QfeNumber         :
        UserAgent         : RTC
        UserAgentFullName :
        Enabled           : True
        CompareOp         : LEQ

</div>

<span data-ttu-id="4ebf0-124">詳細については、「 [CsClientVersionPolicyRule rule](https://docs.microsoft.com/powershell/module/skype/Get-CsClientVersionPolicyRule) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ebf0-124">For details, see the help topic for the [Get-CsClientVersionPolicyRule](https://docs.microsoft.com/powershell/module/skype/Get-CsClientVersionPolicyRule) cmdlet.</span></span>

<span data-ttu-id="4ebf0-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ebf0-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

