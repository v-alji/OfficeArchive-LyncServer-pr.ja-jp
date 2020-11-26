---
title: 'Lync Server 2013: デバイス更新構成設定の表示'
description: 'Lync Server 2013: デバイスの更新設定を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Device Update configuration settings
ms:assetid: aa6a70a9-bd77-4606-b797-ea6a3bab9cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994059(v=OCS.15)
ms:contentKeyID: 51803970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e686562d99da679149b6b977bd3cb9feb5c9a7fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443350"
---
# <a name="view-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="c8d57-103">Lync Server 2013 でのデバイス更新構成設定の表示</span><span class="sxs-lookup"><span data-stu-id="c8d57-103">View Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8d57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8d57-104">

<span> </span></span></span>

<span data-ttu-id="c8d57-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="c8d57-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="c8d57-106">Lync Server 管理シェルと、Windows PowerShell のリモートセッションから2013実行できる、 **CsDeviceUpdateConfiguration** コマンドレットを使用して、デバイス更新サービスの構成設定を表示できます (複数可)。</span><span class="sxs-lookup"><span data-stu-id="c8d57-106">You can view the Device Update Service configuration settings by using Lync Server Management Shell and the **Get-CsDeviceUpdateConfiguration** cmdlet, which you can run from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c8d57-107">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8d57-107">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>


  - <span data-ttu-id="c8d57-108">すべての音声ルートに関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="c8d57-108">To view information about all your voice routes, type the following command in the Lync Server Management Shell and press Enter:</span></span>
    
        Get-CsDeviceUpdateConfiguration
    
    <span data-ttu-id="c8d57-109">このコマンドは、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="c8d57-109">This command returns information similar to the following:</span></span>
    
        Identity               : Global
        ValidLogFileTypes      : {Watson, Config, Diaglog, CELog}
        ValidLogFileExtensions : {.dmp, .clg, .clg1, .clg2...}
        MaxLogFileSize         : 1024000
        MaxLogCacheLimit       : 512000
        LogCleanUpInterval     : 10.00:00:00
        LogFlushInterval       : 00:05:00
        LogCleanUpTimeOfDay    :

</div>

<span data-ttu-id="c8d57-110">このコマンドレットの詳細については、「 [CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateConfiguration)概要」のヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8d57-110">For details about this cmdlet, see Help topic at [Get-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateConfiguration).</span></span>

<span data-ttu-id="c8d57-111"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8d57-111"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

