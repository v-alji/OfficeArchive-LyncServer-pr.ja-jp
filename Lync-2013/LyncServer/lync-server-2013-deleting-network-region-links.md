---
title: 'Lync Server 2013: ネットワーク領域のリンクを削除する'
description: 'Lync Server 2013: ネットワーク領域のリンクを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network region links
ms:assetid: 839273cd-d23f-4b38-84e6-d2dc972f49cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688114(v=OCS.15)
ms:contentKeyID: 49733712
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a17c1ec64460e0f7cb447597f94aadd7fd2a9ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430288"
---
# <a name="deleting-network-region-links-in-lync-server-2013"></a><span data-ttu-id="69b7d-103">Lync Server 2013 でのネットワーク領域リンクの削除</span><span class="sxs-lookup"><span data-stu-id="69b7d-103">Deleting network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69b7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69b7d-104">

<span> </span></span></span>

<span data-ttu-id="69b7d-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="69b7d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="69b7d-106">通話受付制御 (CAC) の一部として、2つのネットワーク領域間のリンクを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="69b7d-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="69b7d-107">ネットワーク内の領域は、物理ワイドエリアネットワーク (WAN) 接続によってリンクされています。</span><span class="sxs-lookup"><span data-stu-id="69b7d-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="69b7d-108">Lync Server コントロールパネルを使用して、2つのネットワーク領域間の既存のリンクを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="69b7d-108">You can use the Lync Server Control Panel to delete an existing link between two network regions.</span></span> <span data-ttu-id="69b7d-109">ネットワーク領域へのリンクの作成または変更の詳細については、「 [Lync Server 2013 でのネットワーク領域のリンクの構成](lync-server-2013-configuring-network-region-links.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69b7d-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span></span>

<div>

## <a name="to-delete-a-network-region-link"></a><span data-ttu-id="69b7d-110">ネットワーク領域のリンクを削除するには</span><span class="sxs-lookup"><span data-stu-id="69b7d-110">To delete a network region link</span></span>

1.  <span data-ttu-id="69b7d-111">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="69b7d-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="69b7d-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="69b7d-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="69b7d-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="69b7d-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="69b7d-114">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **地域] リンク** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69b7d-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="69b7d-115">[ **領域のリンク** ] ページで、削除する地域のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="69b7d-115">On the **Region Link** page, click the region link that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="69b7d-116">一度に複数の領域のリンクを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="69b7d-116">You can delete more than one region link at a time.</span></span> <span data-ttu-id="69b7d-117">これを行うには、ctrl キーを押しながら、CTRL キーを押しながら複数の領域のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="69b7d-117">To do this, press CTRL and select multiple region links while holding down the CTRL key.</span></span> <span data-ttu-id="69b7d-118">または、すべての地域リンクを選択するには、[<STRONG>編集</STRONG>] メニューの [<STRONG>すべて選択</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69b7d-118">Or, to select all region links, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="69b7d-119">[ **編集** ] メニューの [ **削除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="69b7d-119">From the **Edit** menu, select **Delete**.</span></span>

6.  <span data-ttu-id="69b7d-120">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69b7d-120">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="69b7d-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="69b7d-121">See Also</span></span>


[<span data-ttu-id="69b7d-122">Lync Server 2013 でのネットワーク領域のリンクの構成</span><span class="sxs-lookup"><span data-stu-id="69b7d-122">Configuring network region links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-region-links.md)  
  

<span data-ttu-id="69b7d-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69b7d-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

