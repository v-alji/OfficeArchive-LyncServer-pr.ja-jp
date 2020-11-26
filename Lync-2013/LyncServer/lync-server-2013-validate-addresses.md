---
title: 'Lync Server 2013: アドレスを確認する'
description: 'Lync Server 2013: アドレスを確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validate addresses
ms:assetid: aae557c9-e6f5-4d23-8af1-1d4cd7968c54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412808(v=OCS.15)
ms:contentKeyID: 48185108
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcbb8789912b3bcbcfb60dd79807f06c2957c1f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446319"
---
# <a name="validate-addresses-in-lync-server-2013"></a><span data-ttu-id="033e8-103">Lync Server 2013 で住所を検証する</span><span class="sxs-lookup"><span data-stu-id="033e8-103">Validate addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="033e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="033e8-104">

<span> </span></span></span>

<span data-ttu-id="033e8-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="033e8-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="033e8-106">位置情報データベースを公開する前に、SIP トランクまたは公衆交換電話網 (PSTN) E9 サービスプロバイダーによって維持されている、主要な住所ガイド (MSAG) に対して新しい場所を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="033e8-106">Before publishing the location database, you must validate new locations against the Master Street Address Guide (MSAG) that is maintained by your SIP trunk or public switched telephone network (PSTN) E9-1-1 service provider.</span></span>

<span data-ttu-id="033e8-107">SIP トランクの E9 サービスプロバイダの詳細については、「 [Lync Server 2013 の E9 サービスプロバイダーを選択する](lync-server-2013-choosing-an-e9-1-1-service-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="033e8-107">For details about SIP trunk E9-1-1 service providers, see [Choosing an E9-1-1 service provider for Lync Server 2013](lync-server-2013-choosing-an-e9-1-1-service-provider.md).</span></span>

<span data-ttu-id="033e8-108">住所の検証の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="033e8-108">For details about validating addresses, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="033e8-109">**Get-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="033e8-109">**Get-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="033e8-110">**Set-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="033e8-110">**Set-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="033e8-111">**Remove-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="033e8-111">**Remove-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="033e8-112">**Get-CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="033e8-112">**Get-CsLisCivicAddress**</span></span>

  - <span data-ttu-id="033e8-113">**テスト-CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="033e8-113">**Test-CsLisCivicAddress**</span></span>

<div>

## <a name="to-validate-addresses-located-in-the-location-database"></a><span data-ttu-id="033e8-114">場所データベースにある住所を確認するには</span><span class="sxs-lookup"><span data-stu-id="033e8-114">To validate addresses located in the location database</span></span>

1.  <span data-ttu-id="033e8-115">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="033e8-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="033e8-116">次のコマンドレットを実行して、緊急サービス プロバイダーとの接続を構成します。</span><span class="sxs-lookup"><span data-stu-id="033e8-116">Run the following cmdlets to configure the emergency service provider connection.</span></span>
    
        $pwd = Read-Host -AsSecureString <password>
        Set-CsLisServiceProvider -ServiceProviderName Provider1 -ValidationServiceUrl <URL provided by provider> -CertFileName <location of certificate provided by provider> -Password $pwd

3.  <span data-ttu-id="033e8-117">次のコマンドレットを実行して、場所データベース内の住所を確認します。</span><span class="sxs-lookup"><span data-stu-id="033e8-117">Run the following cmdlet to validate the addresses in the location database.</span></span>
    
        Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus
    
    <span data-ttu-id="033e8-118">また、**Test-CsLisCivicAddress** コマンドレットを使用して、個々の住所を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="033e8-118">You can also use the **Test-CsLisCivicAddress** cmdlet to validate individual addresses.</span></span>

<span data-ttu-id="033e8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="033e8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

