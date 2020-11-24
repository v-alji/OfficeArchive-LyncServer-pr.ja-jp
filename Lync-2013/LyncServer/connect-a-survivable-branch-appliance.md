---
title: 存続可能ブランチ アプライアンスの接続
description: Survivable Branch Appliance に接続します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect a Survivable Branch Appliance
ms:assetid: fe3167e2-d1b1-4cd4-bf30-262e0e7d14e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721948(v=OCS.15)
ms:contentKeyID: 49733886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5bbf9e1a4189d3c80d6dec449adf68b82cd3691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398348"
---
# <a name="connect-a-survivable-branch-appliance"></a><span data-ttu-id="20204-103">存続可能ブランチ アプライアンスの接続</span><span class="sxs-lookup"><span data-stu-id="20204-103">Connect a Survivable Branch Appliance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20204-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20204-104">

<span> </span></span></span>

<span data-ttu-id="20204-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="20204-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="20204-106">すべての Survivable Branch Appliance (SBA) は、SBA のバックアップレジストラーとして機能するフロントエンドプールと関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="20204-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool which serves as a backup registrar for the SBA.</span></span> <span data-ttu-id="20204-107">フロントエンドプールが Lync Server 2013 に移行された場合、SBA は Lync Server 2010 のフロントエンドプールから切り離されている必要があります。このプールが Lync server 2013 に移行されると、SBA はアップグレードされたフロントエンドプールに再関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="20204-107">When the Front End pool is migrated to Lync Server 2013, the SBA must be disassociated from the Lync Server 2010 Front End pool while the pool is upgraded, Once the pool has been migrated to Lync Server 2013, the SBA can be re-associated with the upgraded Front End pool.</span></span> <span data-ttu-id="20204-108">これには、トポロジビルダーで従来の Lync Server 2010 トポロジから SBA を削除してから、SBA を Lync Server 2013 トポロジに追加する作業が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20204-108">This involves deleting the SBA from the legacy Lync Server 2010 topology in Topology Builder and then adding the SBA to the Lync Server 2013 topology.</span></span> <span data-ttu-id="20204-109">従来の Lync Server 2010 SBA のホームユーザーは、SBA をトポロジから削除する前に、別のフロントエンドプールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20204-109">Users homed on the legacy Lync Server 2010 SBA must first be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="20204-110">SBA が Lync Server 2013 トポロジに追加されると、それらのユーザーを SBA に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="20204-110">Once the SBA is added to the Lync Server 2013 topology, those users can then be moved back to the SBA.</span></span> <span data-ttu-id="20204-111">以下に、これらの手順の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="20204-111">These steps are summarized below:</span></span>

1.  <span data-ttu-id="20204-112">従来の SBA Lync Server 2010 上に置かれたブランチユーザーを別のフロントエンドプールに移動します。</span><span class="sxs-lookup"><span data-stu-id="20204-112">Move branch users homed on the legacy SBA Lync Server 2010 to another Front End pool.</span></span>

2.  <span data-ttu-id="20204-113">従来の Lync Server 2010 トポロジから SBA を削除して、既存のフロントエンドプールをバックアップレジストラーとして切断します。</span><span class="sxs-lookup"><span data-stu-id="20204-113">Remove SBA from the legacy Lync Server 2010 topology to disconnect the existing Front End pool as a backup registrar.</span></span>

3.  <span data-ttu-id="20204-114">Lync Server 2013 トポロジに SBA を追加し、この新しいフロントエンドプールをバックアップレジストラーとして構成します。</span><span class="sxs-lookup"><span data-stu-id="20204-114">Add SBA to the Lync Server 2013 topology and configure this new Front End pool as the backup registrar.</span></span>

4.  <span data-ttu-id="20204-115">ブランチユーザーを新しい Lync Server 2013 SBA に移動します。</span><span class="sxs-lookup"><span data-stu-id="20204-115">Move the branch users to the new Lync Server 2013 SBA.</span></span>

<span data-ttu-id="20204-116">**Lync Server 2010 SBA ブランチサイトをトポロジに追加する**</span><span class="sxs-lookup"><span data-stu-id="20204-116">**Add Lync Server 2010 SBA Branch Site to Your Topology**</span></span>

1.  <span data-ttu-id="20204-117">**トポロジビルダー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="20204-117">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="20204-118">左側のウィンドウで、[ **ブランチサイト**] を右クリックし、[ **新しいブランチサイト**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-118">In the left pane right-click **Branch sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="20204-119">[ **新しい分岐サイトの定義** ] ダイアログボックスで、[ **名前**] をクリックし、ブランチサイトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20204-119">In the **Define New Branch Site** dialog box, click **Name**, and then type the name of the branch site.</span></span>

4.  <span data-ttu-id="20204-120">省略[ **説明**] をクリックし、ブランチサイトにわかりやすい説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="20204-120">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="20204-121">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-121">Click **Next**.</span></span>

6.  <span data-ttu-id="20204-122">省略[次の **新しいブランチサイトの定義** ] ダイアログボックスで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="20204-122">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
    1.  <span data-ttu-id="20204-123">[ **市区町村**] をクリックし、ブランチサイトが配置されている都市の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20204-123">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
    2.  <span data-ttu-id="20204-124">[ **状態/地域**] をクリックして、ブランチサイトが配置されている状態または地域の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20204-124">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
    3.  <span data-ttu-id="20204-125">[ **国コード**] をクリックし、ブランチサイトが配置されている国/地域の2桁の通話コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="20204-125">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="20204-126">[ **次へ**] をクリックし、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="20204-126">Click **Next**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="20204-127">このサイトで Lync 2010 Survivable Branch Appliance または Server を使用している場合は、[ **このウィザードを終了するときに、新しい Survivable ウィザードを開く** ] チェックボックスをオフにしてください。</span><span class="sxs-lookup"><span data-stu-id="20204-127">If you are using a Lync 2010 Survivable Branch Appliance or Server at this site, be sure to uncheck the **Open the New Survivable Wizard when this wizard closes** option.</span></span> <span data-ttu-id="20204-128">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-128">Click **Finish**.</span></span>

8.  <span data-ttu-id="20204-129">従来の Lync Server 2010 SBA を Lync Server 2013 フロントエンドプールに関連付けるには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="20204-129">To associate the legacy Lync Server 2010 SBA to the Lync Server 2013 Front End pool:</span></span>
    
    1.  <span data-ttu-id="20204-130">作成されたブランチサイトを展開します。</span><span class="sxs-lookup"><span data-stu-id="20204-130">Expand the branch site that has been created.</span></span>
    
    2.  <span data-ttu-id="20204-131">**Lync Server 2010** を右クリックし、[**新規作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-131">Right click on **Lync Server 2010** and then click **New**.</span></span>
    
    3.  <span data-ttu-id="20204-132">[ **Survivable Branch Appliance] を** クリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-132">Click **Survivable Branch Appliance…**</span></span>

9.  <span data-ttu-id="20204-133">表示されるウィザードの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="20204-133">Follow the directions in the wizard that opens.</span></span> <span data-ttu-id="20204-134">ウィザード項目の詳細について [は、「Lync Server 2013 で Survivable Branch Appliance または Server を定義する](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20204-134">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="20204-135">Lync Server 2010 Survivable Branch Appliance は、Lync Server 2010 Monitoring Store にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="20204-135">A Lync Server 2010 Survivable Branch Appliance can only be associated with a Lync Server 2010 Monitoring Store.</span></span>

    
    </div>

10. <span data-ttu-id="20204-136">このサイトで Survivable Branch アプライアンスまたはサーバーを使っていない場合は、[ **このウィザードを終了するときに、新しい Survivable ウィザードを開く** ] チェックボックスをオフにして、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20204-136">If you are not using a Survivable Branch Appliance or Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box, and then click **Finish**.</span></span>

11. <span data-ttu-id="20204-137">トポロジに追加する各ブランチサイトについて、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="20204-137">Repeat the previous steps for each branch site you want to add to the topology.</span></span>

<span data-ttu-id="20204-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20204-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

