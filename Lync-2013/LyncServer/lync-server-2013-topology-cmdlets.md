---
title: 'Lync Server 2013: トポロジコマンドレット'
description: 'Lync Server 2013: トポロジコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology cmdlets
ms:assetid: 3ed739a7-d58d-475d-8240-fa8d2c6dc7e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415648(v=OCS.15)
ms:contentKeyID: 48183942
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f77febaa3beb4acc25bc5bc54dd0d5585fe18fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444141"
---
# <a name="topology-cmdlets-jn-lync-server-2013"></a><span data-ttu-id="89d90-103">トポロジコマンドレット、Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89d90-103">Topology cmdlets jn Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89d90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89d90-104">

<span> </span></span></span>

<span data-ttu-id="89d90-105">_**最終更新日:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="89d90-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="89d90-106">Microsoft Lync Server 2013 に含まれているトポロジコマンドレットの多くは、セットアップおよびトポロジビルダーでの使用を目的として設計されています。そのため、多くの場合、管理者が直接呼び出すことがほとんどないトポロジのコマンドレットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="89d90-106">Many of the topology cmdlets included in Microsoft Lync Server 2013 are designed for use with Setup and Topology Builder; because of that, there are a number of topology cmdlets that administrators will rarely call directly.</span></span> <span data-ttu-id="89d90-107">ただし、管理者がこれらのコマンドレットを使用することが必要になる場合もあります。たとえば、新しい Kerberos アカウントを作成した後、変更を有効にするには、 [CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) コマンドレットを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d90-107">However, there will be times when administrators will be required to use these cmdlets; for example, after creating new Kerberos accounts you must run the [Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) cmdlet to cause the changes to take effect.</span></span> <span data-ttu-id="89d90-108">さらに、管理者は、Lync Server 2013 が正しくインストールされ、予期したとおりに動作していることを確認するために、 [テスト用の CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) ツールやテスト用の [コンピューター](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) などのコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="89d90-108">In addition, administrators will likely run cmdlets such as [Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) and [Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) to help ensure that Lync Server 2013 has been correctly installed and is working as expected.</span></span>

<div>

## <a name="topology-cmdlets"></a><span data-ttu-id="89d90-109">トポロジのコマンドレット</span><span class="sxs-lookup"><span data-stu-id="89d90-109">Topology Cmdlets</span></span>

<span data-ttu-id="89d90-110">Lync Server トポロジの直接管理に関連するコマンドレットの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="89d90-110">The following is a list of cmdlets that relate directly managing your Lync Server topology:</span></span>

<span data-ttu-id="89d90-111">**トポロジ**</span><span class="sxs-lookup"><span data-stu-id="89d90-111">**Topology**</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-112">[取得-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-112">[Get-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-113">[CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-113">[Get-CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-114">[Set-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-114">[Set-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-115">[有効にする-CsTopology テクノロジー](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-115">[Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-116">[CsTopology テクノロジー](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-116">[Get-CsTopology](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-117">[公開-CsTopology テクノロジー](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-117">[Publish-CsTopology](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-118">[テスト-CsTopology テクノロジー](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-118">[Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-119">[エクスポート-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-119">[Export-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-120">[インポート-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-120">[Import-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-122">[CsComputer を無効にする](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-122">[Disable-CsComputer](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-123">[CsComputer を有効にする](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-123">[Enable-CsComputer](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-124">[CsComputer の入手](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-124">[Get-CsComputer](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="89d90-125">[CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-125">[Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="89d90-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="89d90-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="89d90-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="89d90-127">See Also</span></span>


[<span data-ttu-id="89d90-128">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="89d90-128">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="89d90-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89d90-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

