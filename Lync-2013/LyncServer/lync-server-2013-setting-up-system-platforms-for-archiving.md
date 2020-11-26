---
title: 'Lync Server 2013: アーカイブのためにシステムプラットフォームを設定する'
description: 'Lync Server 2013: アーカイブ用にシステムプラットフォームをセットアップします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up system platforms for Archiving
ms:assetid: 2df40fdf-0e32-46d4-9fb2-1ce1d7bfa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204768(v=OCS.15)
ms:contentKeyID: 48183716
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f210083451ae8fcb87c53e52b5512de6f1f18d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441677"
---
# <a name="setting-up-system-platforms-for-archiving-in-lync-server-2013"></a><span data-ttu-id="44b64-103">Lync Server 2013 でアーカイブするためのシステムプラットフォームを設定する</span><span class="sxs-lookup"><span data-stu-id="44b64-103">Setting up system platforms for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44b64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44b64-104">

<span> </span></span></span>

<span data-ttu-id="44b64-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="44b64-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="44b64-106">アーカイブの展開を開始する前に、システム要件を満たすハードウェアに必要なオペレーティングシステムとその他の必須ソフトウェアをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="44b64-106">Before starting the deployment of Archiving, you must install the required operating system and any other prerequisite software on hardware that meets system requirements:</span></span>

  - <span data-ttu-id="44b64-107">**Lync Server 2013 プラットフォーム**   Lync Server 2013 の展開にはアーカイブサーバーがありません。</span><span class="sxs-lookup"><span data-stu-id="44b64-107">**Lync Server 2013 platform**   Lync Server 2013 deployments do not have Archiving Servers.</span></span> <span data-ttu-id="44b64-108">代わりに、統合されたデータ収集エージェントは、アーカイブのためにデータを取得するためにフロントエンドサーバーと標準エディションのサーバー上で実行されるため、アーカイブをホストするために別個のシステムプラットフォームは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="44b64-108">Instead, Unified Data Collection Agents run on Front End Servers and Standard Edition servers to capture data for archiving, so no separate system platform is required to host Archiving.</span></span>

  - <span data-ttu-id="44b64-109">**データストレージプラットフォーム**   Lync Server 2013 では、次のいずれかを使用してデータを保存できます。</span><span class="sxs-lookup"><span data-stu-id="44b64-109">**Data storage platform**   In Lync Server 2013, you can store data by using either of the following:</span></span>
    
      - <span data-ttu-id="44b64-110">**Microsoft Exchange の統合**   Exchange 2013 の展開を使用して Lync Server 2013 アーカイブデータを保存する場合、またはアーカイブデータの保存用に別のデータベースを設定するのではなく、exchange 2013 を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="44b64-110">**Microsoft Exchange integration**   If you want to store Lync Server 2013 Archiving data by using your Exchange 2013 deployment, instead of or in addition to setting up a separate database for storage of Archiving data, your Exchange deployment must be running Exchange 2013.</span></span> <span data-ttu-id="44b64-111">Exchange 2013 のシステムプラットフォームのセットアップの詳細については、Exchange の製品に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="44b64-111">For details about setting up system platforms for Exchange 2013, see the Exchange product documentation.</span></span>
    
      - <span data-ttu-id="44b64-112">**SQL Server**   Microsoft Exchange 統合の代わりに、または Microsoft Exchange 統合の使用に加えて、アーカイブデータの保存に別の SQL Server データベースを使用する場合は、アーカイブの展開前にデータベースのシステムプラットフォームを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44b64-112">**SQL Server**   If you want to use a separate SQL Server database for storage of archiving data, instead of or in addition to using Microsoft Exchange integration, you must set up the system platform for the database prior to deployment of Archiving.</span></span> <span data-ttu-id="44b64-113">特定のシステムプラットフォーム要件は、アーカイブデータベース用に Microsoft SQL Server 2008 R2 と Microsoft SQL Server 2012 のどちらを使用するかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="44b64-113">The specific system platform requirements depend on whether you use Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for the Archiving database.</span></span> <span data-ttu-id="44b64-114">これらのデータベースのシステムプラットフォームのセットアップの詳細については、Microsoft SQL Server 2008 R2 および Microsoft SQL Server 2012 の製品に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="44b64-114">For details about setting up system platforms for these databases, see the Microsoft SQL Server 2008 R2 and Microsoft SQL Server 2012 product documentation.</span></span>

  - <span data-ttu-id="44b64-115">**ファイルサーバープラットフォーム**   Lync server 2013 は、フロントエンドサーバーまたは Standard Edition サーバーのセットアップ時に、ファイルの保存場所と同じ場所に Lync Server のアーカイブファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="44b64-115">**File server platform**   Lync Server 2013 stores Lync Server archiving files in the same location that you specify for file storage when you set up your Front End Servers or Standard Edition servers.</span></span> <span data-ttu-id="44b64-116">アーカイブファイルの保存場所を個別に指定することはできません。そのため、ファイルストレージをアーカイブするために個別のシステムプラットフォームは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="44b64-116">You cannot specify a separate location for archiving file storage, so no separate system platform is required for Archiving file storage.</span></span> <span data-ttu-id="44b64-117">Microsoft Exchange 統合2013を使用している場合、アーカイブされた Lync 通信用のファイルは exchange 2013 サーバーに保存され、それらの Exchange サーバー上のユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="44b64-117">If you use Microsoft Exchange integration, Exchange 2013 the files for archived Lync communications are stored on Exchange 2013 servers for users homed on those Exchange servers.</span></span>

<span data-ttu-id="44b64-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44b64-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

