---
title: 'Lync Server 2013: 会議デバイスを新しいレジストラープールに移動する'
description: 'Lync Server 2013: 会議デバイスを新しいレジストラープールに移動します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move a conferencing device to a new Registrar pool
ms:assetid: 26e02ca3-e881-4f90-8bf0-b13649108100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994025(v=OCS.15)
ms:contentKeyID: 51803934
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 852e6c53ce86129a25e5831d54b1afb2c87828d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425291"
---
# <a name="move-a-conferencing-device-to-a-new-registrar-pool-in-lync-server-2013"></a><span data-ttu-id="b4048-103">Lync Server 2013 で会議デバイスを新しいレジストラープールに移動する</span><span class="sxs-lookup"><span data-stu-id="b4048-103">Move a conferencing device to a new Registrar pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4048-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4048-104">

<span> </span></span></span>

<span data-ttu-id="b4048-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b4048-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b4048-106">「 **Csmove room** 」コマンドレットを使用して、1つのレジストラープールから別の場所に会議デバイスを移動します。</span><span class="sxs-lookup"><span data-stu-id="b4048-106">Move a conferencing device from one Registrar pool to another by using the **Move-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="b4048-107">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="b4048-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b4048-108">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4048-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="moving-a-conferencing-device-to-a-new-registrar-pool"></a><span data-ttu-id="b4048-109">会議デバイスを新しいレジストラープールに移動する</span><span class="sxs-lookup"><span data-stu-id="b4048-109">Moving a Conferencing Device to a New Registrar Pool</span></span>

  - <span data-ttu-id="b4048-110">会議デバイスを移動するには、移動するチャットルームの id を指定する必要があります。その後、ターゲットパラメーターに、デバイスの移動先のレジストラープールの完全修飾ドメイン名 (FQDN) を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4048-110">To move a conferencing device, you must specify the identity of the room to be moved, and then set the Target parameter to the fully qualified domain name (FQDN) of the Registrar pool the device will be moved to.</span></span> <span data-ttu-id="b4048-111">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b4048-111">For example:</span></span>
    
        Move-CsMeetingRoom -Target "atl-cs-001.litwareinc.com" -Identity "Room 14"

</div>

<span data-ttu-id="b4048-112">詳細については、「 [Csroom 会議室の移動](https://docs.microsoft.com/powershell/module/skype/Move-CsMeetingRoom) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4048-112">For details, see the Help topic for the [Move-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Move-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="b4048-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4048-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

