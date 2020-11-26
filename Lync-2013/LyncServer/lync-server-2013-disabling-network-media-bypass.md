---
title: 'Lync Server 2013: ネットワークメディアのバイパスを無効にする'
description: 'Lync Server 2013: ネットワークメディアのバイパスを無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429099"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="3d52d-103">Lync Server 2013 でネットワークメディアのバイパスを無効にする</span><span class="sxs-lookup"><span data-stu-id="3d52d-103">Disabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d52d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d52d-104">

<span> </span></span></span>

<span data-ttu-id="3d52d-105">_**最終更新日:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="3d52d-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="3d52d-106">メディアバイパスの設定は、Microsoft Lync Server 2013 の展開でグローバルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3d52d-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="3d52d-107">メディアのバイパスでは、仲介サーバーを経由せずに通話を発信できます。</span><span class="sxs-lookup"><span data-stu-id="3d52d-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="3d52d-108">メディアのバイパスを使用する場合の詳細については、「計画」セクションの「 [Lync Server 2013 でのメディアのバイパスの計画](lync-server-2013-planning-for-media-bypass.md) 」を参照してください。Lync Server コントロールパネルからメディアのバイパスを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3d52d-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.You can disable media bypass from the Lync Server Control Panel.</span></span> <span data-ttu-id="3d52d-109">Medial バイパスの有効化と構成の詳細については、「 [Lync Server 2013 でネットワークメディアのバイパスを有効にする](lync-server-2013-enabling-network-media-bypass.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d52d-109">For details on enabling and configuring medial bypass, see [Enabling network media bypass in Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span></span>

<div>

## <a name="to-disable-media-bypass"></a><span data-ttu-id="3d52d-110">メディアのバイパスを無効にするには</span><span class="sxs-lookup"><span data-stu-id="3d52d-110">To disable media bypass</span></span>

1.  <span data-ttu-id="3d52d-111">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="3d52d-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3d52d-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d52d-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3d52d-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3d52d-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3d52d-114">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **グローバル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d52d-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="3d52d-115">[ **グローバル** ] ページで、[ **グローバル** 構成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d52d-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="3d52d-116">構成は常に1つだけであり、常に Global という名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="3d52d-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="3d52d-117">[ **編集** ] メニューの [ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d52d-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="3d52d-118">[ **グローバル設定の編集** ] ページで、[ **メディアバイパスを有効にする** ] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="3d52d-118">On the **Edit Global Setting** page, clear the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="3d52d-119">[ **コミット** ] をクリックして変更内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="3d52d-119">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3d52d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d52d-120">See Also</span></span>


[<span data-ttu-id="3d52d-121">Lync Server 2013 でネットワークメディアのバイパスを有効にする</span><span class="sxs-lookup"><span data-stu-id="3d52d-121">Enabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-network-media-bypass.md)  
  

<span data-ttu-id="3d52d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d52d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

