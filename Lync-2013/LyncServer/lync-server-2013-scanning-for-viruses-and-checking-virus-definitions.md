---
title: 'Lync Server 2013: ウイルスをスキャンし、ウイルス定義を確認する'
description: 'Lync Server 2013: ウイルスをスキャンし、ウイルス定義を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scanning for viruses and checking virus definitions
ms:assetid: 287c0f43-82d1-4c1d-b08f-77112fcb5bfa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720909(v=OCS.15)
ms:contentKeyID: 63969589
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c06b08b5e902857e95cdefc206cdbfa860ef748c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445009"
---
# <a name="scanning-for-viruses-and-checking-virus-definitions-in-lync-server-2013"></a><span data-ttu-id="10feb-103">Lync Server 2013 でウイルスのスキャンとウイルス定義の確認を行う</span><span class="sxs-lookup"><span data-stu-id="10feb-103">Scanning for viruses and checking virus definitions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10feb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10feb-104">

<span> </span></span></span>

<span data-ttu-id="10feb-105">_**最終更新日:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="10feb-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<span data-ttu-id="10feb-106">IM レベルのウイルス対策製品をインストールすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10feb-106">We highly recommend installing an IM-level antivirus product.</span></span> <span data-ttu-id="10feb-107">IM は、ウイルスと悪意のあるソフトウェアの両方を組織全体ですばやく展開するための既知のソースです。</span><span class="sxs-lookup"><span data-stu-id="10feb-107">IM is a well-known source for quickly spreading both virus and malicious software throughout an organization.</span></span> <span data-ttu-id="10feb-108">Microsoft Forefront®の Lync Server のセキュリティにより、ウイルス、悪意のあるソフトウェア、ファイルとキーワードのフィルター保護、Office Communications Server とのシームレスな統合などのマルチエンジンスキャンが提供されます。</span><span class="sxs-lookup"><span data-stu-id="10feb-108">Microsoft Forefront® Security for Lync Server provides multi-engine scanning with virus, malicious software, file and keyword filter protection and seamless integration with Office Communications Server.</span></span>

<span data-ttu-id="10feb-109">Lync Server の Forefront Security に加えて、サーバーのファイルシステムを保護するために、ファイルレベルのウイルス対策ソリューションをインストールすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10feb-109">In addition to Forefront Security for Lync Server, we also highly recommend installing a file-level, antivirus solution to protect the server’s file system.</span></span>

<span data-ttu-id="10feb-110">スキャナーエンジンとウイルス定義を最新の状態に保つことは非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="10feb-110">Keeping scanner engines and virus definitions updated is very important.</span></span> <span data-ttu-id="10feb-111">更新プログラムの正常性を構成および監視することで、Office Communications Server とファイルシステムの両方の保護に最新のスキャン情報が使用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="10feb-111">Configuring and monitoring the health of the updates makes sure that the most current scanning information is being used to protect both Office Communications Server and file-system.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10feb-112">Lync Server 2013 と lync server の Forefront Security を実行しているサーバーでサードパーティのファイルレベルのウイルス対策ソフトウェアを使用している場合は、Lync Server と Lync server がインストールされているフォルダーがスキャンされないようにして、破損しないようにします。</span><span class="sxs-lookup"><span data-stu-id="10feb-112">When using a third-party, file-level antivirus software on a server that runs Lync Server 2013 and Forefront Security for Lync Server, make sure that the folders in which Forefront Security for Lync Server and the Lync Server are installed are not scanned, to prevent their corruption.</span></span> <span data-ttu-id="10feb-113">除外の完全な一覧については、を参照してください <A class=uri href="https://support.microsoft.com/kb/943620">https://support.microsoft.com/kb/943620</A> 。</span><span class="sxs-lookup"><span data-stu-id="10feb-113">For the full list of exclusions, see <A class=uri href="https://support.microsoft.com/kb/943620">https://support.microsoft.com/kb/943620</A>.</span></span>



<span data-ttu-id="10feb-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10feb-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

