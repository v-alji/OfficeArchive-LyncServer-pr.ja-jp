---
title: 'Lync Server 2013: エージェントグループを削除する'
description: 'Lync Server 2013: エージェントグループを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an agent group
ms:assetid: df385fd1-62f4-42b7-a349-4eb38dea50c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182597(v=OCS.15)
ms:contentKeyID: 48185670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dded2db0957e37a624d7e8bf3a06e102f8d35cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430645"
---
# <a name="delete-an-agent-group-in-lync-server-2013"></a><span data-ttu-id="f8d67-103">Lync Server 2013 でエージェントグループを削除する</span><span class="sxs-lookup"><span data-stu-id="f8d67-103">Delete an agent group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8d67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8d67-104">

<span> </span></span></span>

<span data-ttu-id="f8d67-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f8d67-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f8d67-106">エージェントグループを削除するには、次のいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f8d67-106">Use one of the following procedures to delete an agent group.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-agent-group"></a><span data-ttu-id="f8d67-107">Lync Server コントロールパネルを使用してエージェントグループを削除するには</span><span class="sxs-lookup"><span data-stu-id="f8d67-107">To use Lync Server Control Panel to delete an agent group</span></span>

1.  <span data-ttu-id="f8d67-108">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="f8d67-109">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8d67-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f8d67-110">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f8d67-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f8d67-111">左側のナビゲーション バーで、[**応答グループ**] をクリックし、[**グループ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-111">In the left navigation bar, click **Response Groups**, and then click **Group**.</span></span>

4.  <span data-ttu-id="f8d67-112">[ **応答グループ** ] ページで、削除するエージェントグループの名前のすべてまたは一部を検索フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="f8d67-112">On the **Response Groups** page, type all or part of the name of the agent group that you want to delete in the search field.</span></span>

5.  <span data-ttu-id="f8d67-113">結果の一覧で、削除するグループをクリックし、[ **編集**] をクリックして、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-113">In the resulting list, click the group that you want to delete, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="f8d67-114">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-agent-group"></a><span data-ttu-id="f8d67-115">Windows PowerShell を使用してエージェントグループを削除するには</span><span class="sxs-lookup"><span data-stu-id="f8d67-115">To use Windows PowerShell to delete an agent group</span></span>

1.  <span data-ttu-id="f8d67-116">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="f8d67-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8d67-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f8d67-118">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f8d67-118">At the command line, run:</span></span>
    
        Get-CsRgsAgentGroup -Identity <Application Server service> -Name "<name of agent group>" | Remove-CsRgsAgentGroup
    
    <span data-ttu-id="f8d67-119">例:</span><span class="sxs-lookup"><span data-stu-id="f8d67-119">For example:</span></span>
    
        Get-CsRgsAgentGroup -Identity service:ApplicationServer:redmond.contoso.com -Name "Human Resources" | Remove-CsRgsAgentGroup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f8d67-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8d67-120">See Also</span></span>


[<span data-ttu-id="f8d67-121">Lync Server 2013 でエージェントグループを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="f8d67-121">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  


[<span data-ttu-id="f8d67-122">Remove-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="f8d67-122">Remove-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsAgentGroup)  
[<span data-ttu-id="f8d67-123">Get-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="f8d67-123">Get-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsAgentGroup)  
  

<span data-ttu-id="f8d67-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8d67-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

