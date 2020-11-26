---
title: 'Lync Server 2013: メディアポート範囲の設定を構成する'
description: 'Lync Server 2013: メディアポート範囲設定を構成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring media port range settings
ms:assetid: 2c4b7c0b-0dce-48f4-a489-336d6e526f7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204770(v=OCS.15)
ms:contentKeyID: 48183723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a7670284c593197068c366f43bbb3faaaad8f63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432914"
---
# <a name="configuring-media-port-range-settings-in-lync-server-2013"></a><span data-ttu-id="e9ebe-103">Lync Server 2013 でメディアポート範囲設定を構成する</span><span class="sxs-lookup"><span data-stu-id="e9ebe-103">Configuring media port range settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9ebe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9ebe-104">

<span> </span></span></span>

<span data-ttu-id="e9ebe-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e9ebe-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e9ebe-106">メディアポート範囲の設定は、クライアントのパフォーマンスに大きな影響を与え、構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-106">Media port range settings can significantly impact client performance and should be configured.</span></span> <span data-ttu-id="e9ebe-107">Lync Server 管理シェルを使用して、これらの設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-107">You can configure these settings by using Lync Server Management Shell.</span></span>

### <a name="media-port-range-settings"></a><span data-ttu-id="e9ebe-108">メディアポート範囲の設定</span><span class="sxs-lookup"><span data-stu-id="e9ebe-108">Media Port Range Settings</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9ebe-109">設定</span><span class="sxs-lookup"><span data-stu-id="e9ebe-109">Setting</span></span></th>
<th><span data-ttu-id="e9ebe-110">説明</span><span class="sxs-lookup"><span data-stu-id="e9ebe-110">Description</span></span></th>
<th><span data-ttu-id="e9ebe-111">Lync Server Management Shell コマンドレット</span><span class="sxs-lookup"><span data-stu-id="e9ebe-111">Lync Server Management Shell cmdlet</span></span></th>
<th><span data-ttu-id="e9ebe-112">コマンドレットのパラメーター</span><span class="sxs-lookup"><span data-stu-id="e9ebe-112">Cmdlet parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ebe-113">Portrange\ Enabled</span><span class="sxs-lookup"><span data-stu-id="e9ebe-113">Portrange\Enabled</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-114">サーバーによって送信されるポート範囲を、メディアとシグナリングのクライアントで使うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-114">Specifies whether the port ranges sent by the server should be used by the client for media and signaling.</span></span> <span data-ttu-id="e9ebe-115">Subvalues MinMediaPort と MaxMediaPort と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-115">Used in conjunction with the subvalues MinMediaPort and MaxMediaPort.</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-116"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="e9ebe-116"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="e9ebe-117">ClientMediaPortRangeEnabled</span><span class="sxs-lookup"><span data-stu-id="e9ebe-117">ClientMediaPortRangeEnabled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ebe-118">Portrange\MinMediaPort</span><span class="sxs-lookup"><span data-stu-id="e9ebe-118">Portrange\MinMediaPort</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-119">メディアに使用する開始ポート番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-119">Specifies the starting port number to use for media.</span></span> <span data-ttu-id="e9ebe-120">MaxMediaPort と組み合わせて、ポートの範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-120">Combines with MaxMediaPort to specify the range of ports.</span></span> <span data-ttu-id="e9ebe-121">推奨される最小範囲は、40ポートです。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-121">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-122"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="e9ebe-122"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="e9ebe-123">ClientMediaPort (クライアントメディアに使用する開始ポート番号を表します)</span><span class="sxs-lookup"><span data-stu-id="e9ebe-123">ClientMediaPort (represents the starting port number to use for client media)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9ebe-124">Portrange\MaxMediaPort</span><span class="sxs-lookup"><span data-stu-id="e9ebe-124">Portrange\MaxMediaPort</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-125">メディアに使用する最大のポート番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-125">Specifies the highest port number to use for media.</span></span> <span data-ttu-id="e9ebe-126">MinMediaPort と組み合わせて、ポートの範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-126">Combines with MinMediaPort to specify the range of ports.</span></span> <span data-ttu-id="e9ebe-127">推奨される最小範囲は、40ポートです。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-127">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="e9ebe-128"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="e9ebe-128"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="e9ebe-129">ClientMediaPortRange (クライアントメディアで利用できるポートの合計数を示します。既定は 40)</span><span class="sxs-lookup"><span data-stu-id="e9ebe-129">ClientMediaPortRange (indicates the total number of ports available for client media; default is 40)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-media-port-range-settings"></a><span data-ttu-id="e9ebe-130">メディアポート範囲の設定を構成するには</span><span class="sxs-lookup"><span data-stu-id="e9ebe-130">To Configure Media Port Range Settings</span></span>

1.  <span data-ttu-id="e9ebe-131">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="e9ebe-132">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-132">Run the following cmdlet:</span></span>
    
        Get-CsConferencingConfiguration
    
    <span data-ttu-id="e9ebe-133">このコマンドレットは会議の構成設定を返します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-133">This cmdlet returns the conferencing configuration settings.</span></span>

3.  <span data-ttu-id="e9ebe-134">変更するパラメーターと値を使用して、次のコマンドレットを実行します (このコマンドレットのパラメーターの詳細については、「Lync Server 管理シェルドキュメント」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-134">Run the following cmdlet with the parameters and values you want to change (for details about the parameters for this cmdlet, see the Lync Server Management Shell documentation):</span></span>
    
        Set-CsConferencingConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9ebe-135">特定のサイトの会議構成設定の追加のセットを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-135">You can create additional sets of conferencing configuration settings for specific sites.</span></span> <span data-ttu-id="e9ebe-136">サイト id を使用して <STRONG>CsConferencingConfiguration</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-136">Use the <STRONG>New- CsConferencingConfiguration</STRONG> cmdlet with a site identity.</span></span> <span data-ttu-id="e9ebe-137">サイトの新しい会議構成設定を作成する場合、サイトの設定はグローバル設定よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-137">When you create new conferencing configuration settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="e9ebe-138">詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9ebe-138">For details, see the Lync Server Management Shell documentation.</span></span>

    
    <span data-ttu-id="e9ebe-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9ebe-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

