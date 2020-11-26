---
title: 'Lync Server 2013: エッジサーバーのポート範囲の構成'
description: 'Lync Server 2013: エッジサーバーのポート範囲を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Edge Servers
ms:assetid: 6f0ae442-6624-4e3f-849a-5b9e387fb8cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204996(v=OCS.15)
ms:contentKeyID: 48184469
ms.date: 07/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c085a5dbc32bbf56842984eae2ef8896ab895c65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432745"
---
# <a name="configuring-port-ranges-for-your-edge-servers-in-lync-server-2013"></a><span data-ttu-id="4245f-103">Lync Server 2013 でエッジサーバーのポート範囲を構成する</span><span class="sxs-lookup"><span data-stu-id="4245f-103">Configuring port ranges for your Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4245f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4245f-104">

<span> </span></span></span>

<span data-ttu-id="4245f-105">_**最終更新日:** 2015-07-24_</span><span class="sxs-lookup"><span data-stu-id="4245f-105">_**Topic Last Modified:** 2015-07-24_</span></span>

<span data-ttu-id="4245f-106">エッジサーバーでは、音声、ビデオ、アプリケーション共有のために個別のポート範囲を構成する必要はありません。同様に、エッジサーバーに使われるポート範囲も、会議、アプリケーション、および仲介サーバーで使用されるポート範囲と一致する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4245f-106">With Edge servers you do not have to configure separate port ranges for audio, video, and application sharing; likewise, the port ranges used for Edge servers do not have to match the port ranges used with your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="4245f-107">例を始める前に、このオプションが存在している間、ポート範囲を変更しないことをお勧めします。これは、5万のポート範囲から移動した場合に、一部のシナリオに悪影響を与える可能性があるため、これを強調することが重要です。</span><span class="sxs-lookup"><span data-stu-id="4245f-107">Before we proceed with our example, it's important to stress that while this option exists, we do recommend you not change the port ranges, as this may adversely affect some scenarios if you move out of the 50000 port range.</span></span>

<span data-ttu-id="4245f-108">たとえば、次のようなポート範囲を使用するように会議、アプリケーション、および仲介業者を構成したとします。</span><span class="sxs-lookup"><span data-stu-id="4245f-108">For example, suppose you have configured your Conferencing, Application, and Mediation servers to use these port ranges:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4245f-109">パケットの種類</span><span class="sxs-lookup"><span data-stu-id="4245f-109">Packet Type</span></span></th>
<th><span data-ttu-id="4245f-110">開始ポート</span><span class="sxs-lookup"><span data-stu-id="4245f-110">Starting Port</span></span></th>
<th><span data-ttu-id="4245f-111">予約されているポートの数</span><span class="sxs-lookup"><span data-stu-id="4245f-111">Number of Ports Reserved</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4245f-112">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="4245f-112">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="4245f-113">40803</span><span class="sxs-lookup"><span data-stu-id="4245f-113">40803</span></span></p></td>
<td><p><span data-ttu-id="4245f-114">8348</span><span class="sxs-lookup"><span data-stu-id="4245f-114">8348</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4245f-115">オーディオ</span><span class="sxs-lookup"><span data-stu-id="4245f-115">Audio</span></span></p></td>
<td><p><span data-ttu-id="4245f-116">49152</span><span class="sxs-lookup"><span data-stu-id="4245f-116">49152</span></span></p></td>
<td><p><span data-ttu-id="4245f-117">8348</span><span class="sxs-lookup"><span data-stu-id="4245f-117">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4245f-118">ビデオ</span><span class="sxs-lookup"><span data-stu-id="4245f-118">Video</span></span></p></td>
<td><p><span data-ttu-id="4245f-119">57500</span><span class="sxs-lookup"><span data-stu-id="4245f-119">57500</span></span></p></td>
<td><p><span data-ttu-id="4245f-120">8034</span><span class="sxs-lookup"><span data-stu-id="4245f-120">8034</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4245f-121"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="4245f-121"><strong>Totals</strong></span></span></p></td>
<td><p>--</p></td>
<td><p><span data-ttu-id="4245f-122">24730</span><span class="sxs-lookup"><span data-stu-id="4245f-122">24730</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4245f-123">ご覧のとおり、オーディオ、ビデオ、およびアプリケーション共有のポート範囲は、ポート40803から始まり、24732ポートの合計をカバーしています。</span><span class="sxs-lookup"><span data-stu-id="4245f-123">As you can see, your port ranges for audio, video, and application sharing start at port 40803 and encompass a total of 24732 ports.</span></span> <span data-ttu-id="4245f-124">必要に応じて、次のようなポート値を使用するように特定のエッジサーバーを構成するには、Lync Server 管理シェルで、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4245f-124">If you prefer, you can configure a given Edge Server to use these overall port values by running a command similar to this one from within the Lync Server Management Shell:</span></span>

    Set-CsEdgeServer -Identity EdgeServer:atl-edge-001.litwareinc.com -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730

<span data-ttu-id="4245f-125">または、次のコマンドを使用して、組織内のすべてのエッジサーバーを同時に構成します。</span><span class="sxs-lookup"><span data-stu-id="4245f-125">Or, use the following command to simultaneously configure all the Edge Servers in your organization:</span></span>

    Get-CsService -EdgeServer | ForEach-Object {Set-CsEdgeServer -Identity $_.Identity -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730}

<span data-ttu-id="4245f-126">次の Lync Server 管理シェルコマンドを使用して、エッジサーバーの現在のポート設定を確認できます。</span><span class="sxs-lookup"><span data-stu-id="4245f-126">You can verify the current port settings for your Edge Servers by using this Lync Server Management Shell command:</span></span>

    Get-CsService -EdgeServer | Select-Object Identity, MediaCommunicationPortStart, MediaCommunicationPortCount

<span data-ttu-id="4245f-127">ここでも、これらのオプションを用意していますが、ポート構成のためにそのままにしておくことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4245f-127">Again, while we do provide these options, we strongly recommend you leave things as they are for the port configuration.</span></span>

<span data-ttu-id="4245f-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4245f-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

