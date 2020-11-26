---
title: 'Lync Server 2013: 容量と可用性の管理'
description: 'Lync Server 2013: 容量と可用性の管理。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity and availability management
ms:assetid: 207a2997-f482-4bee-892d-d2b112294481
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720325(v=OCS.15)
ms:contentKeyID: 63969586
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d498649651f8cfbccc65f5b1b5f010025ac418e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435601"
---
# <a name="capacity-and-availability-management-in-lync-server-2013"></a><span data-ttu-id="0fe96-103">Lync Server 2013 での容量と可用性の管理</span><span class="sxs-lookup"><span data-stu-id="0fe96-103">Capacity and availability management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fe96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fe96-104">

<span> </span></span></span>

<span data-ttu-id="0fe96-105">_**最終更新日:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="0fe96-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="0fe96-106">キャパシティ管理と可用性管理の目的は、システムのパフォーマンスを測定および制御することです。</span><span class="sxs-lookup"><span data-stu-id="0fe96-106">The purpose of capacity management and availability management is to measure and control system performance.</span></span> <span data-ttu-id="0fe96-107">システムのパフォーマンスを測定および制御できるように、キャパシティ管理と可用性管理の手順を実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0fe96-107">We recommend that you implement capacity management and availability management procedures so that you can measure and control system performance.</span></span> <span data-ttu-id="0fe96-108">システムが利用可能であるかどうか、および現在と予測されたニーズを処理できるかどうかを確認する必要があります。基準計画を設定して、傾向を確認するためにシステムを監視します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-108">You have to know whether the system is available and if it can handle the current and the projected demands by setting baselines and monitoring the system to look for trends.</span></span>

<div>

## <a name="capacity-management"></a><span data-ttu-id="0fe96-109">容量管理</span><span class="sxs-lookup"><span data-stu-id="0fe96-109">Capacity management</span></span>

<span data-ttu-id="0fe96-110">容量管理には、SLA で規定されている最小のパフォーマンスレベルが超過することを保証するために、サービスキャパシティの計画、サイズ変更、および制御が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-110">Capacity management involves planning, sizing, and controlling service capacity to help guarantee that the minimum performance levels specified in your SLA are exceeded.</span></span> <span data-ttu-id="0fe96-111">適切なキャパシティ管理によって、適切な料金で IT サービスを提供できるようになり、クライアントで Sla で定義されたパフォーマンスのレベルを満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-111">Good capacity management helps ensure that you can provide IT services at a reasonable cost and still meet the levels of performance defined in your SLAs with the client.</span></span> <span data-ttu-id="0fe96-112">これらの条件には、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-112">These criteria can include the following:</span></span>

  - <span data-ttu-id="0fe96-113">**システムの応答時間**   これは、システムが一般的な操作を実行するためにかかる測定時間です。</span><span class="sxs-lookup"><span data-stu-id="0fe96-113">**System Response Time**   This is the measured time that the system takes to do typical actions.</span></span> <span data-ttu-id="0fe96-114">例としては、オーディオ/ビデオサーバーの役割で音声/ビデオのトラフィックを処理するために必要な時間、クライアントが会議を作成して参加するために必要な時間、すべての watcher クライアントでプレゼンスが更新されるまでの時間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-114">Examples include the time that is required for the audio/video server role to process audio/video traffic, the time that is required for a client to create and join a conference, or the time taken for presence to be updated in all watcher clients.</span></span>

  - <span data-ttu-id="0fe96-115">**記憶域の容量**   これは、コンテンツデータベース、バックアップデバイス、ローカルドライブのいずれかであるかどうかにかかわらず、ストレージシステムの容量です。</span><span class="sxs-lookup"><span data-stu-id="0fe96-115">**Storage Capacity**   This is the capacity of a storage system, whether it is a content database, a backup device, or a local drive.</span></span> <span data-ttu-id="0fe96-116">例としては、サイトごとに提供される記憶域の最大容量と、バックアップが上書きされるまでにバックアップが保存される時間が挙げられます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-116">Examples include the maximum amount of storage space to be provided per site and the time that backups should be stored before they are overwritten.</span></span>

<span data-ttu-id="0fe96-117">キャパシティの調整は、多くの場合、ディスク容量やネットワークの帯域幅など、十分な物理リソースが利用可能であることを確認することになります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-117">Adjusting capacity is frequently a case of making sure that enough physical resources are available, such as disk space and network bandwidth.</span></span> <span data-ttu-id="0fe96-118">次の表に、容量に関連する問題の一般的な解決策を示します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-118">The following table lists typical resolutions for capacity-related issues.</span></span>

### <a name="typical-resolutions-for-capacity-related-issues"></a><span data-ttu-id="0fe96-119">容量に関連する問題の一般的な解決策</span><span class="sxs-lookup"><span data-stu-id="0fe96-119">Typical resolutions for capacity-related issues</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fe96-120">問題</span><span class="sxs-lookup"><span data-stu-id="0fe96-120">Issue</span></span></th>
<th><span data-ttu-id="0fe96-121">可能な解決策</span><span class="sxs-lookup"><span data-stu-id="0fe96-121">Possible resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fe96-122">音声/ビデオのパフォーマンスが低いリモートユーザー</span><span class="sxs-lookup"><span data-stu-id="0fe96-122">Remote users having poor audio/video performance</span></span></p></td>
<td><p><span data-ttu-id="0fe96-123">WAN リンクで適切な帯域幅が利用できるかどうか、および QoS が有効で適切に構成されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-123">Check to see whether appropriate bandwidth is available on the WAN links and if QoS is enabled and appropriately configured.</span></span> <span data-ttu-id="0fe96-124">QoE データを確認します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-124">Check QoE data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fe96-125">Lync 環境の全体的な応答速度は遅くなります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-125">Overall response of the Lync environment is slow.</span></span></p></td>
<td><p><span data-ttu-id="0fe96-126">テストを実行して、既存のフロントエンドサーバーが読み込みを処理できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-126">Run tests to check that the existing front-end servers can deal with the load.</span></span> <span data-ttu-id="0fe96-127">必要に応じて、新しいフロントエンドサーバーを導入します。SQL データベースの応答時間を確認し、遅延の原因 (ディスク i/o の向上など) を修正します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-127">Introduce a new front-end server if it is needed.Check SQL database response times and fix the causes for the delays (for example, improve disk I/O).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0fe96-128">詳細なトラブルシューティングについては、「Lync Server ネットワークガイド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0fe96-128">Troubleshooting in greater detail is covered in the Lync Server Networking Guide.</span></span>

<span data-ttu-id="0fe96-129">容量は、システム構成の影響を受けます。また、ネットワーク帯域幅などの物理リソースによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-129">Capacity is affected by system configuration and depends on physical resources such as network bandwidth.</span></span> <span data-ttu-id="0fe96-130">たとえば、Lync 環境が完全バックアップを夜間実行するように構成されている場合は、エンドユーザーによる対話型のパフォーマンスに対する影響が最小化されることを保証するために、細心の注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-130">For example, if a Lync environment is configured to perform a full backup nightly, care must be taken to help guarantee that the effect on the interactive performance experienced by end-users is minimized.</span></span>

<span data-ttu-id="0fe96-131">キャパシティ管理は、システムのキャパシティを許容できるレベルに維持し、次の問題に対処するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="0fe96-131">Capacity management is the process of keeping the capacity of a system within acceptable levels and addresses the following issues:</span></span>

  - <span data-ttu-id="0fe96-132">**要件の変化への**   対応  システムまたは組織での変更を考慮するために、容量の要件を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-132">**Reacting to changes in requirements**   Capacity requirements have to be adjusted to account for changes in the system or the organization.</span></span> <span data-ttu-id="0fe96-133">たとえば、環境がエンタープライズ Voip の実装を決定した場合、仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイの数と配置は非常に重要になります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-133">For example, if your environment decides to implement Enterprise Voice, the number and placement of Mediation Servers and public switched telephone network (PSTN) gateways will be very important.</span></span> <span data-ttu-id="0fe96-134">セッション開始プロトコル (SIP) トランクまたはダイレクト SIP を使用する場合は、最高のエンタープライズボイスパフォーマンスを実現するために全体的な設計が大幅に変更されます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-134">If you'll be doing Session Initiation Protocol (SIP) trunking or direct SIP, the overall design will be significantly changed to provide the best Enterprise Voice performance.</span></span>

  - <span data-ttu-id="0fe96-135">**将来の要件を予測**   する  一部の容量要件は、時間の経過によって予測可能です。</span><span class="sxs-lookup"><span data-stu-id="0fe96-135">**Predicting future requirements**   Some capacity requirements change predictably over time.</span></span> <span data-ttu-id="0fe96-136">傾向を追跡することで、アップグレードを事前に計画することができます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-136">By tracking trends you can plan upgrades in advance.</span></span> <span data-ttu-id="0fe96-137">たとえば、ベースラインを作成するには、さまざまな Lync サイト間で利用可能な帯域幅を監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-137">For example, available bandwidth between various Lync sites must be monitored to create a baseline.</span></span> <span data-ttu-id="0fe96-138">このベースラインでは、これらのリンクへの帯域幅の追加が必要になるタイミングを予測できます。これらのリモートサイトのユーザー数は、時間の経過と共に増加します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-138">This baseline will allow you to predict when you have to add more bandwidth to these links as user count in these remote sites increases with time.</span></span>

</div>

<div>

## <a name="availability-management"></a><span data-ttu-id="0fe96-139">可用性の管理</span><span class="sxs-lookup"><span data-stu-id="0fe96-139">Availability management</span></span>

<span data-ttu-id="0fe96-140">可用性管理は、お客様が必要とする一貫した信頼性の高いサービスのレベルを、IT サービスが一貫して適切に提供するためのプロセスです。</span><span class="sxs-lookup"><span data-stu-id="0fe96-140">Availability management is the process of making sure that any IT service consistently and cost effectively delivers the level of consistent, reliable service that is required by the customer.</span></span> <span data-ttu-id="0fe96-141">可用性管理では、サービスの損失を最小限に抑え、サービスが失われた場合に適切な対応措置が取られるようにします。</span><span class="sxs-lookup"><span data-stu-id="0fe96-141">Availability management deals with minimizing loss of service and with making sure that appropriate action is taken if service is lost.</span></span> <span data-ttu-id="0fe96-142">Lync 環境では、エンタープライズ Voip サービスが利用できるかどうか、ユーザーがスケジュールされた会議に参加できるかどうかなどを考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-142">In a Lync environment, you may be concerned about whether the Enterprise Voice service is available, whether users can join scheduled conferences, and so on.</span></span> <span data-ttu-id="0fe96-143">SLA では、許容可能な期間と停止時間を定義し、システムが計画されたメンテナンスで利用できない場合に一定の期間にわたって許可します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-143">An SLA defines an acceptable frequency and length of outages and allows for certain periods when the system is unavailable for planned maintenance.</span></span>

<span data-ttu-id="0fe96-144">システムの利用可能性について経営陣にレポートを提供する必要がある場合、または利用可能時間の目標に関連付けられていない財務またはその他の罰則がある場合は、可用性データを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-144">If you have to provide reports to your management about the availability of systems, or if you have financial or other penalties associated with missing availability targets, you must record availability data.</span></span> <span data-ttu-id="0fe96-145">このような正式な要件を満たしていない場合でも、少なくとも一定の期間にシステムが故障した頻度を把握しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0fe96-145">Even if you do not have such formal requirements, it is a good idea to at least know how frequently a system has failed in a certain time period.</span></span> <span data-ttu-id="0fe96-146">たとえば、過去12か月間のシステムの可用性と、各エラーからの回復にかかった時間を確認します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-146">For example, system availability in the last 12 months and how long it took to recover from each failure.</span></span> <span data-ttu-id="0fe96-147">この情報は、システム障害に対応するチームの有効性を測定し、向上させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-147">This information will help you measure and improve your team’s effectiveness in responding to a system failure.</span></span> <span data-ttu-id="0fe96-148">また、紛争がある場合は、有用な情報を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-148">It can also give you useful information if there is a dispute.</span></span>

<span data-ttu-id="0fe96-149">可用性に関連するメジャーは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-149">Measures related to availability are as follows:</span></span>

  - <span data-ttu-id="0fe96-150">**空き時間**   情報  通常、これは、停止している時間と比較して、システムまたはサービスにアクセスできる時刻として表されます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-150">**Availability**   This is typically expressed as the time that a system or service can be accessed compared to the time that it is down.</span></span> <span data-ttu-id="0fe96-151">通常、パーセンテージで表されます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-151">It is typically expressed as a percentage.</span></span> <span data-ttu-id="0fe96-152">("3 ナイン" または "5 ナイン") という参照が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-152">(You may see references to “three nines” or “five nines”.</span></span> <span data-ttu-id="0fe96-153">これらは、99.9% または99.999% の可用性を意味します。)</span><span class="sxs-lookup"><span data-stu-id="0fe96-153">These refer to 99.9 percent or 99.999 percent availability.)</span></span>

  - <span data-ttu-id="0fe96-154">**信頼性**   これは、システムが故障するまでの時間であり、エラー (MTBF) という平均時間 (平均) として表現される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-154">**Reliability**   This is a measure of the time between failures of a system and is sometimes expressed as mean (or average) time between failures (MTBF).</span></span>

  - <span data-ttu-id="0fe96-155">**修復時間**   これは、エラーが発生した後にサービスを回復するために要した時間であり、多くの場合は平均 (平均) 修復時間 (MTTR) として表されます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-155">**Time to Repair**   This is the time taken to recover a service after a failure has occurred and is often expressed as mean (meaning average) time to repair (MTTR).</span></span>

<span data-ttu-id="0fe96-156">可用性、信頼性、修復時間は、次のように関連しています。</span><span class="sxs-lookup"><span data-stu-id="0fe96-156">Availability, reliability, and time to repair are related as follows:</span></span>

<span data-ttu-id="0fe96-157">**Availability = (MTBF ~ MTTR)/MTBF**   たとえば、サーバーが6か月の期間にわたって故障し、20分の平均値を使用できない場合、MTBF は3ヶ月または90日間であり、MTTR は20分になります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-157">**Availability = (MTBF – MTTR) / MTBF**   For example, if a server fails two times over a six-month period and is unavailable for an average of 20 minutes, the MTBF is three months or 90 days and the MTTR is 20 minutes.</span></span> <span data-ttu-id="0fe96-158">そのため、Availability = (90 日間–20分)/90 日 = 99.985 パーセント。</span><span class="sxs-lookup"><span data-stu-id="0fe96-158">Therefore, Availability = (90 days – 20 minutes) / 90 days = 99.985 percent.</span></span>

<span data-ttu-id="0fe96-159">可用性管理は、Sla で定義されているパラメーター内で、空き時間情報が最大化されていることを確認するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="0fe96-159">Availability management is the process of making sure that availability is maximized and kept within the parameters that are defined in SLAs.</span></span> <span data-ttu-id="0fe96-160">可用性管理には、次のプロセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fe96-160">Availability management includes the following processes:</span></span>

  - <span data-ttu-id="0fe96-161">**監視**    サービスを利用できない時間を確認します。</span><span class="sxs-lookup"><span data-stu-id="0fe96-161">**Monitoring**    Examining when and for how long services are unavailable.</span></span>

  - <span data-ttu-id="0fe96-162">**レポート**   可用性の数値は、管理、ユーザー、および運用チームに定期的に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-162">**Reporting**   Availability figures should be regularly provided to management, users, and operations teams.</span></span> <span data-ttu-id="0fe96-163">これらのレポートでは、傾向を強調表示し、適切に実行されている領域と注意が必要な領域を特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-163">These reports should highlight trends and identify areas that are doing well and areas that require attention.</span></span> <span data-ttu-id="0fe96-164">レポートは、Sla で設定されたターゲットに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-164">The report should summarize compliance with targets set in the SLAs.</span></span>

  - <span data-ttu-id="0fe96-165">**改善**   利用可能時間が Sla で定義されている目標を満たしていない場合、または、可用性が利用可能時間を減らしている場合は、可用性管理プロセスで改善手順を計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fe96-165">**Improvement**   If availability does not meet targets that are defined in the SLAs or where the trend is toward reduced availability, the availability management process should plan remedial steps.</span></span> <span data-ttu-id="0fe96-166">これには、停止の理由を強調する他の責任チームとの協力、および中断の繰り返しを防止するための改善措置を計画することが必要です。</span><span class="sxs-lookup"><span data-stu-id="0fe96-166">This should include working with other responsible teams to highlight reasons for outages and to plan remedial actions to prevent a recurrence of the outages.</span></span>

<span data-ttu-id="0fe96-167">容量と稼働時間の測定値は、このドキュメントの後半で説明する、Microsoft System Center Operations Manager (以前の Microsoft Operations Manager) などの自動化されたツールやスクリプトに最適な反復的なタスクです。</span><span class="sxs-lookup"><span data-stu-id="0fe96-167">Capacity and availability measurements are repetitive tasks that are ideally suited to automated tools and scripts such as Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which is discussed later in this document.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0fe96-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fe96-168">See Also</span></span>


[<span data-ttu-id="0fe96-169">System Center Operations Manager での Lync Server 2013 の監視</span><span class="sxs-lookup"><span data-stu-id="0fe96-169">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)  
  

<span data-ttu-id="0fe96-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fe96-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

