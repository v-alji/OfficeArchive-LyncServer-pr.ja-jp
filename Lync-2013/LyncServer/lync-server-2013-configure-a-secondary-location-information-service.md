---
title: 'Lync Server 2013: セカンダリの場所情報サービスを構成する'
description: 'Lync Server 2013: セカンダリの場所情報サービスを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a secondary Location Information service
ms:assetid: 083ffbc6-7c18-4141-85f9-8825b62c3d10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398138(v=OCS.15)
ms:contentKeyID: 48183334
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1721299a0c70535dff8dd05e31712ee6a8d93691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434215"
---
# <a name="configure-a-secondary-location-information-service-in-lync-server-2013"></a><span data-ttu-id="ec008-103">Lync Server 2013 でセカンダリ場所情報サービスを構成する</span><span class="sxs-lookup"><span data-stu-id="ec008-103">Configure a secondary Location Information service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec008-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec008-104">

<span> </span></span></span>

<span data-ttu-id="ec008-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="ec008-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="ec008-106">Lync Server 2013 には、位置情報サービスをセカンダリの場所のソース (SLS) データベースにポイントするために使用できる web サービスインターフェイスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="ec008-106">Lync Server 2013 provides a web service interface that you can use to point the Location Information service to a Secondary Location Source (SLS) database.</span></span> <span data-ttu-id="ec008-107">SLS データベースに接続する web サービスインターフェイスは、位置情報サービスの WSDL に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec008-107">The web service interface that connects to the SLS database must conform to Location Information service WSDL.</span></span> <span data-ttu-id="ec008-108">ロケーションデータベースとセカンダリロケーションデータベースの両方が構成されている場合、位置情報サービスは最初に位置情報データベースを照会し、一致が見つからない場合は、クライアントから SLS データベースに位置情報要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="ec008-108">If both a location database and secondary location database are configured, the Location Information service first queries the location database, and if no match is found, sends the location request from the client to the SLS database.</span></span> <span data-ttu-id="ec008-109">場所が SLS に存在する場合、位置情報サービスはその場所をクライアントに送り返します。</span><span class="sxs-lookup"><span data-stu-id="ec008-109">If the location exists in the SLS, the Location Information service then sends the location back to the client.</span></span>

<span data-ttu-id="ec008-110">詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec008-110">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="ec008-111">**Set-CsWebServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="ec008-111">**Set-CsWebServiceConfiguration**</span></span>

<div>

## <a name="to-configure-secondary-location-database"></a><span data-ttu-id="ec008-112">セカンダリの場所データベースを構成するには</span><span class="sxs-lookup"><span data-stu-id="ec008-112">To configure Secondary Location database</span></span>

1.  <span data-ttu-id="ec008-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec008-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ec008-114">次のコマンドレットを実行して、セカンダリ場所データベースの場所の URL を構成します。</span><span class="sxs-lookup"><span data-stu-id="ec008-114">Run the following cmdlet to configure the URL for the location of the secondary location database.</span></span>
    
        Set-CsWebServiceConfiguration -SecondaryLocationSourceURL "<web service url>" 

<span data-ttu-id="ec008-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec008-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

