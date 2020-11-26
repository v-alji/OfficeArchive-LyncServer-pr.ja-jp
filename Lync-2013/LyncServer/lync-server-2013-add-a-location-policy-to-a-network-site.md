---
title: 'Lync Server 2013: 場所のポリシーをネットワークサイトに追加する'
description: 'Lync Server 2013: 場所のポリシーをネットワークサイトに追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add a location policy to a network site
ms:assetid: 43bfab8a-3d6b-4ca4-8425-879fd910502e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425936(v=OCS.15)
ms:contentKeyID: 48183980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20f71d3144e2ef730de5dae46be16138b5d36c42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439397"
---
# <a name="add-a-location-policy-to-a-network-site-in-lync-server-2013"></a><span data-ttu-id="05010-103">Lync Server 2013 でネットワークサイトに位置情報ポリシーを追加する</span><span class="sxs-lookup"><span data-stu-id="05010-103">Add a location policy to a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05010-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05010-104">

<span> </span></span></span>

<span data-ttu-id="05010-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="05010-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="05010-106">次の例は、 [Lync Server 2013 の [場所ポリシーの作成](lync-server-2013-create-location-policies.md)] で定義されている **redmond** の場所ポリシーを既存のネットワークサイトに追加する方法と、 **redmond** の場所ポリシーを使用する新しいネットワークサイトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="05010-106">The following examples show how to add the **Redmond** location policy defined in [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) to an existing network site and how to create a new network site that uses the **Redmond** location policy.</span></span>

<span data-ttu-id="05010-107">ネットワークサイトの操作の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="05010-107">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="05010-108">**新しい-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="05010-108">**New-CsNetworkSite**</span></span>

  - <span data-ttu-id="05010-109">**Get-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="05010-109">**Get-CsNetworkSite**</span></span>

  - <span data-ttu-id="05010-110">**Set-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="05010-110">**Set-CsNetworkSite**</span></span>

  - <span data-ttu-id="05010-111">**CsNetworkSite の削除**</span><span class="sxs-lookup"><span data-stu-id="05010-111">**Remove-CsNetworkSite**</span></span>

<div>

## <a name="to-assign-a-location-policy-to-an-existing-network-site"></a><span data-ttu-id="05010-112">場所のポリシーを既存のネットワーク サイトに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="05010-112">To assign a location policy to an existing network site</span></span>

1.  <span data-ttu-id="05010-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="05010-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="05010-114">既存のネットワーク サイトを変更するには、以下のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="05010-114">Run the following cmdlets to modify an existing network site.</span></span>
    
    <span data-ttu-id="05010-115">**Redmond** とマークされている場所のポリシーを、**Redmond** という名前の既存のネットワーク サイトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="05010-115">Assign the **Redmond** tagged Location policy to an existing network site named **Redmond**.</span></span>
    
        Set-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

</div>

<div>

## <a name="to-assign-a-location-policy-to-a-new-network-site"></a><span data-ttu-id="05010-116">場所のポリシーを新しいネットワーク サイトに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="05010-116">To assign a location policy to a new network site</span></span>

1.  <span data-ttu-id="05010-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="05010-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="05010-118">新しいネットワーク サイトを作成するには、以下のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="05010-118">Run the following cmdlet to create a new network site.</span></span>
    
    <span data-ttu-id="05010-119">ネットワーク地域の新しいネットワーク サイトを作成して、**Redmond** とマークされた場所のポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="05010-119">Create a new network site in the network region and assign the **Redmond** tagged Location policy.</span></span>
    
        New-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

<span data-ttu-id="05010-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05010-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

