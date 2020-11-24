---
title: 'Lync Server 2013: コール パーク障害復旧の計画'
description: 'Lync Server 2013: コールパークの障害回復を計画しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Call Park disaster recovery
ms:assetid: f7cf3958-177b-4340-a864-35a6f44d6d88
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205395(v=OCS.15)
ms:contentKeyID: 48185867
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1d05503f1d8c30f4dd4446a995442d5e2500dbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397893"
---
# <a name="planning-for-call-park-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="5dab5-103">Lync Server 2013 でのコール パーク障害復旧の計画</span><span class="sxs-lookup"><span data-stu-id="5dab5-103">Planning for Call Park disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dab5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dab5-104">

<span> </span></span></span>

<span data-ttu-id="5dab5-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="5dab5-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="5dab5-106">このセクションでは、障害回復用のコールパークアプリケーションを準備する方法と、障害回復プロセスの考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dab5-106">This section describes some ways to prepare the Call Park application for disaster recovery and some considerations for the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-call-park-disaster-recovery"></a><span data-ttu-id="5dab5-107">コールパークの障害回復の準備</span><span class="sxs-lookup"><span data-stu-id="5dab5-107">Preparing for Call Park Disaster Recovery</span></span>

<span data-ttu-id="5dab5-108">障害回復の手順を準備して実行する場合は、次の点にご注意ください。</span><span class="sxs-lookup"><span data-stu-id="5dab5-108">Keep the following in mind when preparing for and carrying out disaster recovery procedures.</span></span>

  - <span data-ttu-id="5dab5-109">キャパシティ計画を行うときの障害回復計画を立てます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-109">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="5dab5-110">障害回復キャパシティの場合、ペア化されたプール内の各プールは、両方のプールのコールパークサービスの作業負荷を処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dab5-110">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of the Call Park services in both pools.</span></span> <span data-ttu-id="5dab5-111">通話パークキャパシティ計画の詳細については、「 [Lync Server 2013 でのコールパークのキャパシティ計画](lync-server-2013-capacity-planning-for-call-park.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5dab5-111">For details about Call Park capacity planning, see [Capacity planning for Call Park in Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span></span>

  - <span data-ttu-id="5dab5-112">障害回復中に、フェールオーバープロセスの一環としてバックアッププールにリダイレクトされたユーザーは、バックアッププールで実行されているコールパークサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="5dab5-112">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park service running in the backup pool.</span></span> <span data-ttu-id="5dab5-113">そのため、障害回復中のコールパークのサポートでは、プライマリプールとバックアッププールの両方でコールパークアプリケーションを展開して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dab5-113">Therefore, support for Call Park during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

  - <span data-ttu-id="5dab5-114">各プールには、そのプールに所属しているユーザーがパーキング通話に使用するために、有効な範囲の軌道番号が必要です。</span><span class="sxs-lookup"><span data-stu-id="5dab5-114">Each pool must have a valid range of orbit numbers for users who are homed in that pool to use for parking calls.</span></span>

  - <span data-ttu-id="5dab5-115">通話パーク用にアップロードされた、カスタマイズした音楽の個別のバックアップコピーを常に保持しておきます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-115">Always keep a separate backup copy of any customized music on hold that has been uploaded for Call Park.</span></span> <span data-ttu-id="5dab5-116">これらのファイルは、Lync Server 2013 の障害回復プロセスの一部としてはバックアップされません。また、プールにアップロードされたファイルが破損、破損、または消去された場合は、失われます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-116">These files are not backed up as part of the Lync Server 2013 disaster recovery process and will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>

</div>

<div>

## <a name="call-park-disaster-recovery-considerations"></a><span data-ttu-id="5dab5-117">コールパーク障害回復に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="5dab5-117">Call Park Disaster Recovery Considerations</span></span>

<span data-ttu-id="5dab5-118">1組のコールパークアプリケーションの構成設定と、1つのプールにつき1つのカスタマイズされた音楽オンホールドオーディオファイルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-118">You can define only one set of Call Park application configuration settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="5dab5-119">これらの設定には、タイムアウトしきい値、保留中の音楽、最大通話ピックアップ試行回数、タイムアウト URI が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-119">These settings include the timeout threshold, music on hold, maximum call pickup attempts, and timeout URI.</span></span> <span data-ttu-id="5dab5-120">これらの構成設定を表示するには、 **CsCpsConfiguration** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="5dab5-120">To view these configuration settings, run the **Get-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="5dab5-121">**CsCpsConfiguration** コマンドレットの詳細については、「 [get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5dab5-121">For details about the **Get-CsCpsConfiguration** cmdlet, see [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span></span>

<span data-ttu-id="5dab5-122">障害回復中に、コールパークはバックアッププールのコールパークアプリケーションを使用するため、プライマリプールの設定はバックアップされません。</span><span class="sxs-lookup"><span data-stu-id="5dab5-122">During disaster recovery, Call Park uses the Call Park application in the backup pool, so settings in the primary pool are not backed up.</span></span> <span data-ttu-id="5dab5-123">プライマリプールを復元できない場合に、プライマリプールの代わりに新しいプールを展開すると、プライマリプールの設定は失われ、新規プール内のコールパーク設定とカスタマイズされた音楽の保留中のオーディオファイルを再設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dab5-123">If the primary pool can't be recovered and you deploy a new pool to replace the primary pool, the settings from the primary pool are lost, and you need to reconfigure the Call Park settings and any customized music-on-hold audio files in the new pool.</span></span>

<span data-ttu-id="5dab5-124">別の完全修飾ドメイン名 (FQDN) で新しいプールを展開してプライマリプールを置き換える場合は、プライマリプールに関連付けられていたすべてのコールパークの範囲を、新しいプールの FQDN に再割り当てする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dab5-124">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Call Park orbit ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="5dab5-125">新しいプールに軌道範囲を再割り当てするには、Lync Server コントロールパネルまたは **CsCallParkOrbit** コマンドレットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5dab5-125">To reassign orbit ranges to the new pool, you can use either Lync Server Control Panel or the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="5dab5-126">**CsCallParkOrbit** コマンドレットの詳細については、「 [set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5dab5-126">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

<span data-ttu-id="5dab5-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dab5-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

