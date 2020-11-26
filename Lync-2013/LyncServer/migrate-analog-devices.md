---
title: アナログ デバイスの移行
description: アナログデバイスを移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443833"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="36ede-103">アナログ デバイスの移行</span><span class="sxs-lookup"><span data-stu-id="36ede-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36ede-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36ede-104">

<span> </span></span></span>

<span data-ttu-id="36ede-105">_**最終更新日:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="36ede-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="36ede-106">Lync Server は、アナログデバイスのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="36ede-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="36ede-107">特に、サポートされているアナログデバイスはアナログオーディオ電話とアナログ fax マシンです。</span><span class="sxs-lookup"><span data-stu-id="36ede-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="36ede-108">Lync Server 環境でのアナログデバイスの使用をサポートするために、修飾ゲートウェイを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="36ede-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="36ede-109">Lync Server 2010 から Lync Server 2013 に移行した後、アナログデバイスに関連付けられた連絡先オブジェクトも移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ede-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="36ede-110">Lync server 管理シェルを使用して、Lync Server 2010 アナログデバイスに関連付けられたすべての連絡先オブジェクトを取得してから、それらのオブジェクトを Lync Server 2013 プールに移動します。</span><span class="sxs-lookup"><span data-stu-id="36ede-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="36ede-111">アナログデバイスを移行するには</span><span class="sxs-lookup"><span data-stu-id="36ede-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="36ede-112">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="36ede-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="36ede-113">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="36ede-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="36ede-114">すべての連絡先オブジェクトが Lync Server 2013 プールに移動されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36ede-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="36ede-115">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="36ede-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="36ede-116">すべての連絡先オブジェクトが Lync Server 2013 プールと関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36ede-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="36ede-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36ede-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

