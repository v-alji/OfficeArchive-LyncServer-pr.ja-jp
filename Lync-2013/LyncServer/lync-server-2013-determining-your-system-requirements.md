---
title: 'Lync Server 2013: システム要件の決定'
description: 'Lync Server 2013: システム要件を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determining your system requirements
ms:assetid: 620e81e2-42df-4eda-8498-bd56a14aa0e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398438(v=OCS.15)
ms:contentKeyID: 48184286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ceca8eabb234ae7fd483372ff5e611664ecc4fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429490"
---
# <a name="determining-your-system-requirements-for-lync-server-2013"></a><span data-ttu-id="2e415-103">Lync Server 2013 システム要件の決定</span><span class="sxs-lookup"><span data-stu-id="2e415-103">Determining your system requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e415-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e415-104">

<span> </span></span></span>

<span data-ttu-id="2e415-105">_**最終更新日:** 2014-01-02_</span><span class="sxs-lookup"><span data-stu-id="2e415-105">_**Topic Last Modified:** 2014-01-02_</span></span>

<span data-ttu-id="2e415-106">Lync Server を実行しているすべてのサーバーは、特定の最小システム要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e415-106">All servers running Lync Server must meet certain minimum system requirements.</span></span> <span data-ttu-id="2e415-107">Lync Server のシステム要件には、サーバーハードウェア、各サーバーにインストールされるオペレーティングシステム、および関連するソフトウェア要件 (Windows の更新プログラムや、サーバーにインストールする必要があるその他のソフトウェアなど) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e415-107">System requirements for Lync Server include the server hardware, the operating system to be installed on each server, and related software requirements, such as the Windows updates and other software that must be installed on the servers.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2e415-108">Lync Server は64ビット版でのみ利用できます。これには、64ビットのハードウェアと64ビット版の Windows Server が必要です。</span><span class="sxs-lookup"><span data-stu-id="2e415-108">Lync Server is available only in a 64-bit edition, which requires 64-bit hardware and a 64-bit edition of Windows Server.</span></span> <span data-ttu-id="2e415-109">この例外は、32ビット版で利用できる Microsoft Lync Server 2013、計画ツールです。</span><span class="sxs-lookup"><span data-stu-id="2e415-109">The exception is the Microsoft Lync Server 2013, Planning Tool, which is available in a 32-bit edition.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="2e415-110">Active Directory のサポート、サポートされているトポロジ、サーバーの配置、その他のサポートの問題について詳しくは、「 <A href="lync-server-2013-supportability.md">Lync server 2013 のサポート性</A>」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2e415-110">For details about Active Directory support, supported topologies, server collocation, and other supportability issues, see <A href="lync-server-2013-supportability.md">Supportability for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2e415-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="2e415-111">In This Section</span></span>

  - [<span data-ttu-id="2e415-112">Lync Server 2013 のサーバー ハードウェア プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="2e415-112">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)

  - [<span data-ttu-id="2e415-113">Lync Server 2013 でのサーバーおよびツールのオペレーティング システムのサポート</span><span class="sxs-lookup"><span data-stu-id="2e415-113">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)

  - [<span data-ttu-id="2e415-114">Lync Server 2013 でのデータベース ソフトウェアのサポート</span><span class="sxs-lookup"><span data-stu-id="2e415-114">Database software support in Lync Server 2013</span></span>](lync-server-2013-database-software-support.md)

  - [<span data-ttu-id="2e415-115">Lync Server 2013 の追加ソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="2e415-115">Additional software requirements for Lync Server 2013</span></span>](lync-server-2013-additional-software-requirements.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2e415-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e415-116">See Also</span></span>


[<span data-ttu-id="2e415-117">Lync Server 2013 のクライアントとデバイスのハードウェア サポート</span><span class="sxs-lookup"><span data-stu-id="2e415-117">Client and device hardware support in Lync Server 2013</span></span>](lync-server-2013-client-and-device-hardware-support.md)  
[<span data-ttu-id="2e415-118">Lync Server 2013 のサポート状況</span><span class="sxs-lookup"><span data-stu-id="2e415-118">Supportability for Lync Server 2013</span></span>](lync-server-2013-supportability.md)  
  

<span data-ttu-id="2e415-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e415-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

