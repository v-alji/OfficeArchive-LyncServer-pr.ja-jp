---
title: 'Lync Server 2013: ネットワークのサイト間ポリシーを作成する'
description: 'Lync Server 2013: ネットワークのサイト間ポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9666efcb9c6da459a8e50eeae66cd1a513b46f65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431940"
---
# <a name="create-network-intersite-policies-in-lync-server-2013"></a><span data-ttu-id="6b61e-103">Lync Server 2013 でネットワークのサイト間ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="6b61e-103">Create network intersite policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b61e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b61e-104">

<span> </span></span></span>

<span data-ttu-id="6b61e-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="6b61e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="6b61e-106">*ネットワークのサイト間ポリシー* は、それらの間に直接 WAN リンクがあるサイト間の帯域幅制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="6b61e-106">A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.</span></span>

<span data-ttu-id="6b61e-107">詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b61e-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="6b61e-108">新規-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="6b61e-108">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="6b61e-109">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="6b61e-109">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="6b61e-110">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="6b61e-110">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="6b61e-111">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="6b61e-111">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6b61e-112">ネットワークのサイト間ポリシーは、2つのネットワークサイト間に直接クロスリンクがある場合に <EM>のみ</EM> 必要です。</span><span class="sxs-lookup"><span data-stu-id="6b61e-112">A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.</span></span>



</div>

<span data-ttu-id="6b61e-113">North America 地域のトポロジの例では、Reno と Albuquerque のサイト間に直接リンクがあります。</span><span class="sxs-lookup"><span data-stu-id="6b61e-113">In the example topology North America region, there is a direct link between the Reno and Albuquerque sites.</span></span> <span data-ttu-id="6b61e-114">この2つのサイトでは、適切な帯域幅ポリシープロファイルを適用するサイト間ポリシーが必要です。</span><span class="sxs-lookup"><span data-stu-id="6b61e-114">These two sites require an intersite policy that applies an appropriate bandwidth policy profile.</span></span> <span data-ttu-id="6b61e-115">次の例では、20 ~ 20 のリンクプロファイルを適用し \_ ます。</span><span class="sxs-lookup"><span data-stu-id="6b61e-115">The following example applies the 20Mb\_Link profile.</span></span>

<div>

## <a name="to-create-a-network-intersite-policy"></a><span data-ttu-id="6b61e-116">ネットワークのサイト間ポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="6b61e-116">To create a network intersite policy</span></span>

1.  <span data-ttu-id="6b61e-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b61e-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="6b61e-118">ネットワークのサイト間ポリシーを作成して、ダイレクトクロスリンクを持つ2つのサイトに対して、適切な帯域幅ポリシープロファイルを適用するには、New-CsNetworkInterSitePolicy コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="6b61e-118">Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link.</span></span> <span data-ttu-id="6b61e-119">たとえば、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b61e-119">For example, run:</span></span>
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  <span data-ttu-id="6b61e-120">必要に応じて、手順2を繰り返して、ダイレクトクロスリンクを含むすべてのネットワークサイトペアのネットワークサイト間ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6b61e-120">Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.</span></span>

<span data-ttu-id="6b61e-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b61e-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

