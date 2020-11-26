---
title: 'Lync Server 2013: 会議、アプリケーション、および仲介サーバーのポート範囲を構成する'
description: 'Lync Server 2013: 会議、アプリケーション、および仲介サーバーのポート範囲を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Conferencing, Application, and Mediation servers
ms:assetid: 4d6eaa5d-0127-453f-be6a-e55384772d83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204872(v=OCS.15)
ms:contentKeyID: 48184074
ms.date: 05/01/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb3f51e42c86b667b6990f41640bf09e12e840c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432759"
---
# <a name="configuring-port-ranges-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="cd1b8-103">Lync Server 2013 での、会議、アプリケーション、および仲介サーバー向けのポート範囲の構成</span><span class="sxs-lookup"><span data-stu-id="cd1b8-103">Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd1b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd1b8-104">

<span> </span></span></span>

<span data-ttu-id="cd1b8-105">_**最終更新日:** 2015-04-30_</span><span class="sxs-lookup"><span data-stu-id="cd1b8-105">_**Topic Last Modified:** 2015-04-30_</span></span>

<span data-ttu-id="cd1b8-106">サービスの品質を実現するには、会議、アプリケーション、および仲介サーバー上で音声、ビデオ、およびアプリケーション共有用に同一のポート範囲を構成する必要があります。さらに、これらのポート範囲は、何らかの方法でオーバーラップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-106">In order to implement Quality of Service, you should configure identical port ranges for audio, video, and application sharing on your Conferencing, Application, and Mediation servers; furthermore, those port ranges must not overlap in any way.</span></span> <span data-ttu-id="cd1b8-107">簡単な例を使用するには、電話会議サーバー上のビデオに 1万 ~ 10999 のポートを使用しているとします。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-107">To use a simple example, suppose you use ports 10000 through 10999 for video on your Conferencing servers.</span></span> <span data-ttu-id="cd1b8-108">つまり、アプリケーションや仲介サーバー上のビデオ用に、1万 ~ 10999 のポートを予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-108">That means that you must also reserve ports 10000 through 10999 for video on your Application and Mediation servers.</span></span> <span data-ttu-id="cd1b8-109">そうしないと、QoS は期待どおりに動作しません。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-109">If you do not, QoS will not work as expected.</span></span>

<span data-ttu-id="cd1b8-110">同様に、1万 ~ 10999 のビデオ用にポートを予約していて、オーディオ用にポート10500から11999を予約したとします。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-110">Similarly, suppose you reserve ports 10000 through 10999 for video, but then reserve ports 10500 through 11999 for audio.</span></span> <span data-ttu-id="cd1b8-111">これにより、ポートの範囲が重複するため、サービスの品質に関する問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-111">This can create problems for Quality of Service, because the port ranges overlap.</span></span> <span data-ttu-id="cd1b8-112">QoS では、各モダリティに固有のポートセットが必要です。ビデオ用に 1万 ~ 10999 のポートを使用している場合は、別の範囲を使用する必要があります (たとえば、11000から11999を使用してください)。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-112">With QoS, each modality must have a unique set of ports: if you use ports 10000 through 10999 for video, then you'll have to use a different range (for example, 11000 through 11999 for audio).</span></span>

<span data-ttu-id="cd1b8-113">既定では、オーディオとビデオのポート範囲は Microsoft Lync Server 2013 では重複しません。ただし、アプリケーション共有に割り当てられているポート範囲は、オーディオポート範囲とビデオポート範囲の両方と重複しています。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-113">By default, audio and video port ranges do not overlap in Microsoft Lync Server 2013; however, the port ranges assigned to application sharing overlap with both the audio and video port ranges.</span></span> <span data-ttu-id="cd1b8-114">(これにより、これらの範囲のいずれも一意ではないことを意味します)。Lync Server 2013 管理シェル内から次の3つのコマンドを実行して、会議、アプリケーション、および仲介サーバーの既存のポート範囲を確認できます。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-114">(Which, in turn, means that none of these ranges are unique.) You can verify the existing port ranges for your Conferencing, Application, and Mediation servers by running the following three commands from within the Lync Server 2013 Management Shell:</span></span>

    Get-CsService -ConferencingServer | Select-Object Identity, AudioPortStart, AudioPortCount, VideoPortStart, VideoPortCount, AppSharingPortStart, AppSharingPortCount
    
    Get-CsService -ApplicationServer | Select-Object Identity, AudioPortStart, AudioPortCount
    
    Get-CsService -MediationServer | Select-Object Identity, AudioPortStart, AudioPortCount

<div>


> [!WARNING]  
> <span data-ttu-id="cd1b8-115">上に示したように、各ポートの種類 (オーディオ、ビデオ、およびアプリケーションの共有) には、ポートの開始とポート数という2つの個別のプロパティ値が割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-115">As you can see in the preceding commands, each port type – audio, video, and application sharing – is assigned two separate property values: the port start and the port count.</span></span> <span data-ttu-id="cd1b8-116">ポート start は、そのモダリティで使用される最初のポートを示します。たとえば、オーディオポートの start が5万に等しい場合、オーディオトラフィックに使われる最初のポートがポート5万であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-116">The port start indicates the first port used for that modality; for example, if the audio port start is equal to 50000 that means that the first port used for audio traffic is port 50000.</span></span> <span data-ttu-id="cd1b8-117">オーディオポート数が 2 (有効な値ではありませんが、ここでは説明のために使用されます) である場合、オーディオには2つのポートしか割り当てられないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-117">If the audio port count is 2 (which is not a valid value, but is used here for illustration purposes) that means that only 2 ports are allocated for audio.</span></span> <span data-ttu-id="cd1b8-118">第1のポートがポート5万であり、合計2つのポートがある場合は、2番目のポートがポート 50001 (ポート範囲は連続している必要があります) であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-118">If the first port is port 50000 and there are a total of two ports, that means the second port must be port 50001 (port ranges have to be contiguous).</span></span> <span data-ttu-id="cd1b8-119">その結果、オーディオのポート範囲は、5万 ~ 50001 のポートになります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-119">As a result, the port range for audio would be ports 50000 through 50001, inclusive.</span></span><BR><span data-ttu-id="cd1b8-120">また、アプリケーションサーバーと仲介サーバーは、オーディオの場合にのみ QoS をサポートしていることに注意してください。アプリケーションサーバーまたは仲介サーバーで、ビデオまたはアプリケーションの共有ポートを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-120">Note, too that Application server and Mediation server only support QoS for audio; you do not need to change video or application sharing ports in your Application servers or Mediation servers.</span></span>



</div>

<span data-ttu-id="cd1b8-121">上記の3つのコマンドを実行すると、Lync Server 2013 の既定のポート値が次のように構成されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-121">If you run the preceding three commands you'll see that the default port values for Lync Server 2013 are configured like this:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd1b8-122">プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd1b8-122">Property</span></span></th>
<th><span data-ttu-id="cd1b8-123">会議サーバー</span><span class="sxs-lookup"><span data-stu-id="cd1b8-123">Conferencing Server</span></span></th>
<th><span data-ttu-id="cd1b8-124">アプリケーションサーバー</span><span class="sxs-lookup"><span data-stu-id="cd1b8-124">Application Server</span></span></th>
<th><span data-ttu-id="cd1b8-125">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="cd1b8-125">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd1b8-126">AudioPortStart</span><span class="sxs-lookup"><span data-stu-id="cd1b8-126">AudioPortStart</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-127">49152</span><span class="sxs-lookup"><span data-stu-id="cd1b8-127">49152</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-128">49152</span><span class="sxs-lookup"><span data-stu-id="cd1b8-128">49152</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-129">49152</span><span class="sxs-lookup"><span data-stu-id="cd1b8-129">49152</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1b8-130">AudioPortCount</span><span class="sxs-lookup"><span data-stu-id="cd1b8-130">AudioPortCount</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-131">8348</span><span class="sxs-lookup"><span data-stu-id="cd1b8-131">8348</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-132">8348</span><span class="sxs-lookup"><span data-stu-id="cd1b8-132">8348</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-133">8348</span><span class="sxs-lookup"><span data-stu-id="cd1b8-133">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1b8-134">VideoPortStart</span><span class="sxs-lookup"><span data-stu-id="cd1b8-134">VideoPortStart</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-135">57501</span><span class="sxs-lookup"><span data-stu-id="cd1b8-135">57501</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1b8-136">VideoPortCount</span><span class="sxs-lookup"><span data-stu-id="cd1b8-136">VideoPortCount</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-137">8034</span><span class="sxs-lookup"><span data-stu-id="cd1b8-137">8034</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1b8-138">ApplicationSharingPortStart</span><span class="sxs-lookup"><span data-stu-id="cd1b8-138">ApplicationSharingPortStart</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-139">49152</span><span class="sxs-lookup"><span data-stu-id="cd1b8-139">49152</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1b8-140">ApplicationSharingPortCount</span><span class="sxs-lookup"><span data-stu-id="cd1b8-140">ApplicationSharingPortCount</span></span></p></td>
<td><p><span data-ttu-id="cd1b8-141">16383</span><span class="sxs-lookup"><span data-stu-id="cd1b8-141">16383</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd1b8-142">前に説明したように、QoS のために Lync Server のポートを構成する場合は、お客様の会議、アプリケーション、および仲介サーバーで、オーディオポートの設定が同じであることを確認する必要があります。and、2) ポート範囲は重なりません。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-142">As noted previously, when configuring Lync Server ports for QoS, you should ensure that: 1) audio port settings are identical across yours Conferencing, Application, and Mediation servers; and, 2) port ranges do not overlap.</span></span> <span data-ttu-id="cd1b8-143">上記の表をよく見ると、3種類のサーバー間でポート範囲が同じであることがわかります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-143">If you look closely at the preceding table, you will see that the port ranges are identical across the three server types.</span></span> <span data-ttu-id="cd1b8-144">たとえば、[開始オーディオ] ポートは各サーバーの種類で [port 49152] に設定されています。また、各サーバーのオーディオ用に予約されているポートの合計数も8348と同じです。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-144">For example, the starting audio port is set to port 49152 on each server type, and the total number of ports reserved for audio in each server is also identical: 8348.</span></span> <span data-ttu-id="cd1b8-145">ただし、ポートの範囲が重複しています。オーディオポートはポート49152から始まりますが、アプリケーション共有用にポートが設定されています。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-145">However, the port ranges overlap: audio ports start at port 49152, but so do the ports set aside for application sharing.</span></span> <span data-ttu-id="cd1b8-146">サービスの品質を最大限に活用するために、固有のポート範囲を使用するようにアプリケーション共有を再構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-146">In order to make optimal use of Quality of Service, application sharing should be reconfigured to use a unique port range.</span></span> <span data-ttu-id="cd1b8-147">たとえば、ポート40803で開始するようにアプリケーション共有を構成し、8348ポートを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-147">For example, you could configure application sharing to start at port 40803 and to use 8348 ports.</span></span> <span data-ttu-id="cd1b8-148">(8348 ポートの理由</span><span class="sxs-lookup"><span data-stu-id="cd1b8-148">(Why 8348 ports?</span></span> <span data-ttu-id="cd1b8-149">これらの値を一緒に追加した場合は 8348 40803、アプリケーションの共有でポート40803からポート49150が使用されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-149">If you add those values together -- 40803 + 8348 -- that means that application sharing will use ports 40803 through port 49150.</span></span> <span data-ttu-id="cd1b8-150">オーディオポートはポート49152まで開始されないため、重複するポート範囲はなくなります。)</span><span class="sxs-lookup"><span data-stu-id="cd1b8-150">Because audio ports do not begin until port 49152, you will no longer have any overlapping port ranges.)</span></span>

<span data-ttu-id="cd1b8-151">アプリケーション共有用の新しいポート範囲を選んだら、Set-CsConferencingServer コマンドレットを使用して変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-151">After you have selected the new port range for application sharing you can make your change by using the Set-CsConferencingServer cmdlet.</span></span> <span data-ttu-id="cd1b8-152">この変更は、アプリケーションサーバーまたは仲介サーバーで行う必要はありません。これらのサーバーは、アプリケーション共有トラフィックを処理しないためです。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-152">This change does not need to be made on your Application servers or on your Mediation servers, because these servers do not handle application sharing traffic.</span></span> <span data-ttu-id="cd1b8-153">オーディオトラフィック用に使用されているポートを再割り当てする場合は、これらのサーバーでポートの値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-153">You only need to change port values on these servers if you decide to reassign the ports used for audio traffic.</span></span>

<span data-ttu-id="cd1b8-154">単一の会議サーバーでアプリケーション共有のポート値を変更するには、Lync Server 管理シェルで次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-154">To modify the port values for application sharing on a single Conferencing server run a command similar to this from within the Lync Server Management Shell:</span></span>

    Set-CsConferenceServer -Identity ConferencingServer:atl-cs-001.litwareinc.com -AppSharingPortStart 40803 -AppSharingPortCount 8348

<span data-ttu-id="cd1b8-155">すべての会議サーバーでこれらの変更を行う場合は、代わりに次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-155">If you want to make these changes on all your Conferencing servers you can run this command instead:</span></span>

    Get-CsService -ConferencingServer | ForEach-Object {Set-CsConferenceServer -Identity $_.Identity -AppSharingPortStart 40803 -AppSharingPortCount 8348}

<span data-ttu-id="cd1b8-156">ポート設定を変更した後で、変更の影響を受ける各サービスを停止してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-156">After changing port settings you should stop and then restart each service affected by the changes.</span></span>

<span data-ttu-id="cd1b8-157">会議サーバー、アプリケーションサーバー、および仲介サーバーがまったく同じポート範囲を共有していることは必須ではありません。唯一の条件として、すべてのサーバーで固有のポート範囲を確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-157">It is not mandatory that your Conferencing servers, Application servers, and Mediation servers share the exact same port range; the only true requirement is that you set aside unique port ranges on all your servers.</span></span> <span data-ttu-id="cd1b8-158">ただし、すべてのサーバーで同じポートセットを使用すると、通常、管理が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="cd1b8-158">However, administration will typically be easier if you use the same set of ports on all your servers.</span></span>

<span data-ttu-id="cd1b8-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd1b8-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

