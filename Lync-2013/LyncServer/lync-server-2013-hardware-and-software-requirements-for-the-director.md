---
title: 'Lync Server 2013: ディレクターのハードウェアおよびソフトウェア要件'
description: 'Lync Server 2013: ディレクターのハードウェアとソフトウェアの要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware and software requirements for the Director
ms:assetid: 747b701e-7f97-46fe-91c5-1e8d9addf9f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398560(v=OCS.15)
ms:contentKeyID: 48184517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dd868a3a566f1d89b4ada5a16695f8eb02b3b21
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427741"
---
# <a name="hardware-and-software-requirements-for-the-director-in-lync-server-2013"></a><span data-ttu-id="71178-103">Lync Server 2013 のディレクターのハードウェアおよびソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="71178-103">Hardware and software requirements for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71178-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71178-104">

<span> </span></span></span>

<span data-ttu-id="71178-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="71178-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="71178-106">このセクションでは、監督のハードウェアとソフトウェアの要件、およびディレクターのサポートされる collocation シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="71178-106">This section details the hardware and software requirements for the Director, and the supported collocation scenarios for the Director.</span></span>

<div>

## <a name="hardware-requirements-for-the-director"></a><span data-ttu-id="71178-107">ディレクターのハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="71178-107">Hardware Requirements for the Director</span></span>

<span data-ttu-id="71178-108">次の表に、ディレクターのハードウェア要件を示します。</span><span class="sxs-lookup"><span data-stu-id="71178-108">The following table lists the hardware requirements for the Director:</span></span>

### <a name="hardware-requirements-for-the-director"></a><span data-ttu-id="71178-109">ディレクターのハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="71178-109">Hardware Requirements for the Director</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71178-110">ハードウェア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="71178-110">Hardware component</span></span></th>
<th><span data-ttu-id="71178-111">最小要件</span><span class="sxs-lookup"><span data-stu-id="71178-111">Minimum requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71178-112">CPU</span><span class="sxs-lookup"><span data-stu-id="71178-112">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="71178-113">64ビットプロセッサ、クアッドコア、2.0 GHz 以上</span><span class="sxs-lookup"><span data-stu-id="71178-113">64-bit processor, quad-core, 2.0 GHz or higher</span></span></p></li>
<li><p><span data-ttu-id="71178-114">64ビットデュアルプロセッサ、デュアルコア、2.0 GHz 以上</span><span class="sxs-lookup"><span data-stu-id="71178-114">64-bit dual processor, dual-core, 2.0 GHz or higher</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71178-115">メモリ</span><span class="sxs-lookup"><span data-stu-id="71178-115">Memory</span></span></p></td>
<td><p><span data-ttu-id="71178-116">4ギガバイト (GB)</span><span class="sxs-lookup"><span data-stu-id="71178-116">4 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71178-117">ディスク</span><span class="sxs-lookup"><span data-stu-id="71178-117">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="71178-118">10K RPM ハードディスクドライブ (HDD)</span><span class="sxs-lookup"><span data-stu-id="71178-118">10K RPM hard disk drive (HDD)</span></span></p></li>
<li><p><span data-ttu-id="71178-119">高パフォーマンスのソリッドステートドライブ (SSD) と、10K RPM HDD と同等またはそれ以上のパフォーマンス。</span><span class="sxs-lookup"><span data-stu-id="71178-119">High-performance solid state drive (SSD) with performance equal to or better than 10K RPM HDD</span></span></p></li>
<li><p><span data-ttu-id="71178-120">データベースデータファイル用の2倍の RAID 10 (ストライピングとミラーリング) 15K RPM ディスク</span><span class="sxs-lookup"><span data-stu-id="71178-120">2x RAID 10 (striped and mirrored) 15K RPM disks for database data files</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71178-121">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71178-121">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="71178-122">デュアル1ギガビット/秒 (Gbps) ネットワークアダプター (推奨)</span><span class="sxs-lookup"><span data-stu-id="71178-122">Dual 1 gigabit per second (Gbps) network adapters (recommended)</span></span></p></li>
<li><p><span data-ttu-id="71178-123">1つの 1 Gbps ネットワークアダプター (サポートされています)</span><span class="sxs-lookup"><span data-stu-id="71178-123">Single 1 Gbps network adapter (supported)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="software-requirements-for-the-director"></a><span data-ttu-id="71178-124">ディレクターのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="71178-124">Software Requirements for the Director</span></span>

<span data-ttu-id="71178-125">ディレクターの役割は、Lync Server 2013 Enterprise Edition を実行しているサーバーにのみ展開できます。</span><span class="sxs-lookup"><span data-stu-id="71178-125">The Director role can be deployed only on servers running Lync Server 2013 Enterprise Edition.</span></span>

<span data-ttu-id="71178-126">ディレクターには、次のいずれかの64ビットオペレーティングシステムが必要です。</span><span class="sxs-lookup"><span data-stu-id="71178-126">One of the following 64-bit operating systems is required for the Directors:</span></span>

  - <span data-ttu-id="71178-127">Windows Server 2008 R2 Standard オペレーティングシステム (Service Pack 1)</span><span class="sxs-lookup"><span data-stu-id="71178-127">The Windows Server 2008 R2 Standard operating system with Service Pack 1</span></span>

  - <span data-ttu-id="71178-128">Windows Server 2008 R2 Enterprise オペレーティングシステム (Service Pack 1)</span><span class="sxs-lookup"><span data-stu-id="71178-128">The Windows Server 2008 R2 Enterprise operating system with Service Pack 1</span></span>

  - <span data-ttu-id="71178-129">Windows Server 2008 R2 Datacenter オペレーティングシステムと Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="71178-129">The Windows Server 2008 R2 Datacenter operating system with Service Pack 1</span></span>

  - <span data-ttu-id="71178-130">Windows Server 2012 標準オペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="71178-130">The Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="71178-131">Windows Server 2012 Datacenter オペレーティングシステム</span><span class="sxs-lookup"><span data-stu-id="71178-131">The Windows Server 2012 Datacenter operating system</span></span>

<span data-ttu-id="71178-132">また、lync Server 2013 には、「 [Lync server 2013 のその他のサーバーのサポートと要件](lync-server-2013-additional-server-support-and-requirements.md)」で説明されている、次のプログラムと更新プログラムのインストールが必要です。</span><span class="sxs-lookup"><span data-stu-id="71178-132">Lync Server 2013 also requires installation of the following programs and updates detailed in the topic [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span></span>

</div>

<div>

## <a name="supported-collocation"></a><span data-ttu-id="71178-133">サポートされている Collocation</span><span class="sxs-lookup"><span data-stu-id="71178-133">Supported Collocation</span></span>

<span data-ttu-id="71178-134">ディレクターサーバーの役割は、Lync Server 2013 の他のサーバーの役割とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="71178-134">The Director server role cannot be collocated with any other server role in Lync Server 2013.</span></span> <span data-ttu-id="71178-135">ただし、ディレクターを展開しない場合は、フロントエンドサーバーによって役割が想定されます。</span><span class="sxs-lookup"><span data-stu-id="71178-135">However, if you do not deploy a Director, the Front End Servers will assume the role.</span></span>

<span data-ttu-id="71178-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71178-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

