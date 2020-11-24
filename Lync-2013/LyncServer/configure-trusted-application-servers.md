---
title: 信頼済みアプリケーション サーバーの構成
description: 信頼されたアプリケーションサーバーを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398859"
---
# <a name="configure-trusted-application-servers"></a><span data-ttu-id="07297-103">信頼済みアプリケーション サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="07297-103">Configure trusted application servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07297-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07297-104">

<span> </span></span></span>

<span data-ttu-id="07297-105">_**最終更新日:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="07297-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="07297-106">混在環境では、新しい信頼できるアプリケーションサーバーを作成する場合は、次ホッププールを Lync Server 2013 プールとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07297-106">In a mixed environment, if you create a new trusted application server, you must set the next hop pool to be a Lync Server 2013 pool.</span></span> <span data-ttu-id="07297-107">混在環境では、従来の Lync Server 2010 プールと Lync Server 2013 プールの両方がドロップダウンリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="07297-107">In a mixed environment, both the legacy Lync Server 2010 pool and the Lync Server 2013 pool appear in the drop down list.</span></span> <span data-ttu-id="07297-108">従来のプールの選択はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="07297-108">Selecting the legacy pool is not supported.</span></span>

<span data-ttu-id="07297-109">**信頼できるアプリケーションサーバーを作成するときに、[Lync Server 2013 (次ホップ)] を選択します。**</span><span class="sxs-lookup"><span data-stu-id="07297-109">**Select Lync Server 2013 as next hop when creating a Trusted application server**</span></span>

1.  <span data-ttu-id="07297-110">トポロジビルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="07297-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="07297-111">左側のウィンドウで、[ **信頼されたアプリケーションサーバー** ] を右クリックし、[ **新しい信頼できるアプリケーションプール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07297-111">In the left pane, right click **Trusted application servers** and click **New Trusted Application Pool**.</span></span>

3.  <span data-ttu-id="07297-112">信頼されているアプリケーションプールの **プール FQDN** を入力し、それが単一サーバーか複数サーバーかを選択します。</span><span class="sxs-lookup"><span data-stu-id="07297-112">Enter the **Pool FQDN** of the trusted application pool and select whether it will be a single-server or multiple-server.</span></span>

4.  <span data-ttu-id="07297-113">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07297-113">Click **Next**.</span></span>

5.  <span data-ttu-id="07297-114">**[次ホップの選択**] ページで、一覧から Lync Server 2013 フロントエンドプールを選びます。</span><span class="sxs-lookup"><span data-stu-id="07297-114">On the **Select the next hop** page, from the list, select the Lync Server 2013 Front End pool.</span></span>

6.  <span data-ttu-id="07297-115">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07297-115">Click **Finish**.</span></span>

7.  <span data-ttu-id="07297-116">トップノードの **Lync サーバー** を選択し、[ **操作** ] メニューの [ **発行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="07297-116">Select the top node **Lync Server** and from the **Action** menu, select **Publish**.</span></span>
    
    <span data-ttu-id="07297-117">信頼された **アプリケーションプール** が正常に作成され、正しいフロントエンドプールに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="07297-117">Verify the **Trusted Application Pool** has been created successfully and is associated with the correct Front End pool.</span></span>

<span data-ttu-id="07297-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07297-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

