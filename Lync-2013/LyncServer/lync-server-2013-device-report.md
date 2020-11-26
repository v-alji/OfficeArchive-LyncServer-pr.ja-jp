---
title: 'Lync Server 2013: デバイスレポート'
description: 'Lync Server 2013: デバイスレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Report
ms:assetid: f42e4d60-699b-4870-8bb5-13b51bb6eb2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615049(v=OCS.15)
ms:contentKeyID: 48185807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8bff8e973d5c3e2d96c18992a2a2d917d4deb1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429427"
---
# <a name="device-report-in-lync-server-2013"></a><span data-ttu-id="270d5-103">Lync Server 2013 のデバイスレポート</span><span class="sxs-lookup"><span data-stu-id="270d5-103">Device Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="270d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="270d5-104">

<span> </span></span></span>

<span data-ttu-id="270d5-105">_**最終更新日:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="270d5-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="270d5-106">デバイス レポートは、通話に関連した指標 (低品質通話のパーセンテージ、エコー、音声切り替え時間など) を通話で使用されたマイクとスピーカーによってグループ化して取得するため、マイクとスピーカーのレポートと呼んだほうが良いかもしれません。</span><span class="sxs-lookup"><span data-stu-id="270d5-106">The Device Report might be better titled the Microphone and Speakers Report; that's because the Device Report retrieves call-related metrics (such as poor call percentage, echo, and voice switch time) grouped by the microphones and speakers used in the call.</span></span> <span data-ttu-id="270d5-107">IP 電話 (通常は "デバイス" とも呼ばれます) に関心がある場合は、代わりに [Lync Server 2013 の Ip 電話インベントリレポート](lync-server-2013-ip-phone-inventory-report.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="270d5-107">If you are interested in IP phones (also commonly referred to as "devices"), use the [IP Phone Inventory Report in Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md) instead.</span></span>

<span data-ttu-id="270d5-p102">デバイス レポートは、特定のタイプのデバイスで低品質通話が他のデバイスより多く発生しているかどうかを管理者が確認するのに非常に役立ちます。これは、新規デバイスの購入や既存デバイスの置き換えの場合の決定に影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="270d5-p102">The Device Report is extremely useful for administrators in determining if a specific type of device is experiencing high volumes of poor quality calls than others. In turn, this could influence any decisions you must make when it comes time to buy new devices or to replace existing devices.</span></span>

<span data-ttu-id="270d5-p103">既定では、デバイス レポートに表示される情報は、通話で使用されたマイク (キャプチャ デバイス) とスピーカー/ヘッドセット (レンダー デバイス) にも基づいています。たとえば、以下のキャプチャ デバイスとレンダー デバイスを使用する複数のユーザーがいるとします。</span><span class="sxs-lookup"><span data-stu-id="270d5-p103">By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device: By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device:</span></span>

  - <span data-ttu-id="270d5-113">キャプチャ デバイス -- マイク (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-113">Capture device -- Microphone (SoundMAX Integrated Digital HD Audio)</span></span>

  - <span data-ttu-id="270d5-114">レンダー デバイス -- ヘッドセット イヤホン (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="270d5-114">Render device -- Headset Earphone (Microsoft LifeChat LX-3000)</span></span>

<span data-ttu-id="270d5-115">これらのユーザーが合計 254 回の通話を行ったとすると、レポートには以下のようなエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="270d5-115">If those users made a total of 254 calls you'll see an entry like this in the report:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="270d5-116">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-116">Capture device</span></span></th>
<th><span data-ttu-id="270d5-117">レンダー デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-117">Render device</span></span></th>
<th><span data-ttu-id="270d5-118">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="270d5-118">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="270d5-119">マイク (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-119">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="270d5-120">ヘッドセット イヤホン (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="270d5-120">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="270d5-121">254</span><span class="sxs-lookup"><span data-stu-id="270d5-121">254</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="270d5-p104">次に、同じキャプチャ デバイスを使用するがレンダー デバイスは異なる複数のユーザーがいるとします。その場合、レポートにはキャプチャ デバイスとレンダー デバイスのその独自の組み合わせに関する 2 行目のエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="270d5-p104">Now, suppose you have a number of users who use that same capture device but a different render device. In that case, you'll have a second line entry in the report, one for that unique combination of capture device and render device:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="270d5-124">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-124">Capture device</span></span></th>
<th><span data-ttu-id="270d5-125">レンダー デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-125">Render device</span></span></th>
<th><span data-ttu-id="270d5-126">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="270d5-126">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="270d5-127">マイク (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-127">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="270d5-128">ヘッドセット イヤホン (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="270d5-128">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="270d5-129">254</span><span class="sxs-lookup"><span data-stu-id="270d5-129">254</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-130">マイク (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-130">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="270d5-131">スピーカー (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-131">Speakers (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="270d5-132">319</span><span class="sxs-lookup"><span data-stu-id="270d5-132">319</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="270d5-p105">特定のデバイスに関する合計 (たとえば、使用されたレンダー デバイスにかかわらず SoundMAX キャプチャ デバイスに関する合計) を表示するには、[デバイスの種類] ドロップダウン リストから適切なオプション ([キャプチャ デバイス] か [レンダー デバイス]) を選択します。この例で [キャプチャ デバイス] を選択すると、出力は以下のようになります。</span><span class="sxs-lookup"><span data-stu-id="270d5-p105">If you would rather see combined totals for a given device (for example, for the SoundMAX capture device, regardless of the render device used), select the appropriate option from the Device type dropdown list (either Capture device or Render device). If you select Capture device in this example, that will give you output similar to this:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="270d5-135">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-135">Capture device</span></span></th>
<th><span data-ttu-id="270d5-136">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="270d5-136">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="270d5-137">マイク (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="270d5-137">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="270d5-138">573</span><span class="sxs-lookup"><span data-stu-id="270d5-138">573</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="accessing-the-device-report"></a><span data-ttu-id="270d5-139">デバイス レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="270d5-139">Accessing the Device Report</span></span>

<span data-ttu-id="270d5-140">デバイス レポートは通常、監視レポート ホーム ページからアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="270d5-140">The Device Report is typically accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="270d5-141">ただし、 [Lync Server 2013 で [通話の詳細] レポート](lync-server-2013-call-detail-report.md) を表示している場合は、次の指標のいずれかをクリックして、特定のデバイスのデバイスレポートにドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="270d5-141">However, if you are viewing the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) you can drill down to the Device Report for a specific device by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="270d5-142">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-142">Capture Device</span></span>

  - <span data-ttu-id="270d5-143">レンダー デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-143">Render Device</span></span>

<span data-ttu-id="270d5-144">デバイスレポートでは、次の指標のいずれかをクリックして、 [Lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md) にドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="270d5-144">From the Device Report you can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="270d5-145">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="270d5-145">Call volume</span></span>

  - <span data-ttu-id="270d5-146">低品質通話のパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="270d5-146">Poor call percentage</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-device-report"></a><span data-ttu-id="270d5-147">デバイス レポートの活用</span><span class="sxs-lookup"><span data-stu-id="270d5-147">Making the Best Use of the Device Report</span></span>

<span data-ttu-id="270d5-148">デバイス名に関して、デバイス レポートは非常に詳細です。たとえば、以下のキャプチャ デバイスがあるとします。</span><span class="sxs-lookup"><span data-stu-id="270d5-148">When it comes to device names, the Device Report is extremely detailed; for example, suppose you have the following capture devices:</span></span>

  - <span data-ttu-id="270d5-149">Aastra 3002 マイク (2- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="270d5-149">Aastra 3002 Microphone (2- Aastra 3002)</span></span>

  - <span data-ttu-id="270d5-150">Aastra 3002 マイク (3- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="270d5-150">Aastra 3002 Microphone (3- Aastra 3002)</span></span>

  - <span data-ttu-id="270d5-151">Aastra 3002 マイク (Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="270d5-151">Aastra 3002 Microphone (Aastra 3002)</span></span>

  - <span data-ttu-id="270d5-152">Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="270d5-152">Aastra 6725ip</span></span>

  - <span data-ttu-id="270d5-153">Aastra 6725ip マイク (10- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-153">Aastra 6725ip Microphone (10- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-154">Aastra 6725ip マイク (10- Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="270d5-154">Aastra 6725ip Microphone (10- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="270d5-155">Aastra 6725ip マイク (2- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-155">Aastra 6725ip Microphone (2- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-156">Aastra 6725ip マイク (3- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-156">Aastra 6725ip Microphone (3- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-157">Aastra 6725ip マイク (4- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-157">Aastra 6725ip Microphone (4- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-158">Aastra 6725ip マイク (5- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-158">Aastra 6725ip Microphone (5- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-159">Aastra 6725ip マイク (6- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-159">Aastra 6725ip Microphone (6- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-160">Aastra 6725ip マイク (7- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-160">Aastra 6725ip Microphone (7- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-161">Aastra 6725ip マイク (9- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-161">Aastra 6725ip Microphone (9- Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-162">Aastra 6725ip マイク (9-Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="270d5-162">Aastra 6725ip Microphone (9- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="270d5-163">Aastra 6725ip マイク (Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="270d5-163">Aastra 6725ip Microphone (Aastra 6725ip)</span></span>

  - <span data-ttu-id="270d5-164">Aastra 6725ip マイク (Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="270d5-164">Aastra 6725ip Microphone (Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="270d5-165">Aastra 6725ip マイク (USB オーディオデバイス)</span><span class="sxs-lookup"><span data-stu-id="270d5-165">Aastra 6725ip Microphone (USB Audio Device)</span></span>

  - <span data-ttu-id="270d5-166">Aastra 6725ip マイク (USB オーディオデバイス)-V0</span><span class="sxs-lookup"><span data-stu-id="270d5-166">Aastra 6725ip Microphone (USB Audio Device)-V0</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="270d5-167">ローカライズされたバージョンの Lync Server 2013 を実行している場合、デバイス名のキャプチャは同じではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="270d5-167">Keep in mind that capture device names might not be the same if you are running localized versions of Lync Server 2013.</span></span> <span data-ttu-id="270d5-168">Aastra 6725ip マイク (Aastra 6725ip) という名前のデバイス (米国英語の V0 はフランス語またはスペイン語で異なる名前を持つ場合があります)。</span><span class="sxs-lookup"><span data-stu-id="270d5-168">A device named Aastra 6725ip Microphone (Aastra 6725ip)-V0 in US English could have a different name in French or Spanish.</span></span>



</div>

<span data-ttu-id="270d5-169">多くの場合、詳細レベルが必要になります。ただし、モデル番号に関係なく、複数の通話で Aastra マイクを使用することに関心がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="270d5-169">Often times you'll want that level of detail; at other times, however, you might only be interested in how many calls use any Aastra microphone, regardless of model number.</span></span> <span data-ttu-id="270d5-170">そのような情報を取得する方法の1つとして、デバイスレポートデータを Microsoft Excel にエクスポートし、そのデータをコンマ区切り値ファイル (たとえば、C: \\ データ \\ デバイスReport.csv) に保存し \_ ます。</span><span class="sxs-lookup"><span data-stu-id="270d5-170">One way to get information like that is to export the Device Report data to Microsoft Excel and then save that data to a comma-separated values file (for example, C:\\Data\\Devices\_Report.csv).</span></span> <span data-ttu-id="270d5-171">次のような一連のコマンドを使用して、をインポートできます。CSV ファイルを Windows PowerShell にコピーし、Aastra キャプチャデバイスを使って発信した通話の合計数を報告します。</span><span class="sxs-lookup"><span data-stu-id="270d5-171">You can then use a set of commands similar to these to import the .CSV file into Windows PowerShell and report back the total number of calls made using an Aastra capture device:</span></span>

    $devices = Import-Csv "C:\Data\Device_Report.csv
    $sum = $devices | Where-Object {$_."Capture device" -match "Aastra"}
    $sum | foreach-object {[Int]$x = [Int]$x + [Int]$_."call volume"}
    $x

<span data-ttu-id="270d5-172">これは、Aastra キャプチャデバイスを使って発信した通話の合計数を表す1つの値を返します。</span><span class="sxs-lookup"><span data-stu-id="270d5-172">That will return a single value representing the total number of calls made using an Aastra capture device.</span></span> <span data-ttu-id="270d5-173">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="270d5-173">For example:</span></span>

    384

</div>

<div>

## <a name="filters"></a><span data-ttu-id="270d5-174">フィルター</span><span class="sxs-lookup"><span data-stu-id="270d5-174">Filters</span></span>

<span data-ttu-id="270d5-175">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。</span><span class="sxs-lookup"><span data-stu-id="270d5-175">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="270d5-176">たとえば、デバイスレポートでは、通話の種類 (クライアント呼び出しの呼び出し)、電話会議、公衆交換電話網 (PSTN) 通話など、さまざまな機能についてフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="270d5-176">For example, the Device Report enables you to filter on such things as call type (that is, was the call a client call), a conference call, or a public switched telephone network (PSTN) call.</span></span> <span data-ttu-id="270d5-177">また、データをグループ化する方法を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="270d5-177">You can also choose how data should be grouped.</span></span> <span data-ttu-id="270d5-178">この場合、デバイスは時間、日、週、または月でグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="270d5-178">In this case, devices are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="270d5-179">次の表に、デバイスレポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="270d5-179">The following table lists the filters that you can use with the Device Report.</span></span>

### <a name="device-report-filters"></a><span data-ttu-id="270d5-180">デバイスレポートフィルター</span><span class="sxs-lookup"><span data-stu-id="270d5-180">Device Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="270d5-181">名前</span><span class="sxs-lookup"><span data-stu-id="270d5-181">Name</span></span></th>
<th><span data-ttu-id="270d5-182">説明</span><span class="sxs-lookup"><span data-stu-id="270d5-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="270d5-183"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-183"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-p111">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p111">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="270d5-186">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="270d5-186">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="270d5-p112">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p112">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="270d5-189">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="270d5-189">7/7/2012</span></span></p>
<p><span data-ttu-id="270d5-190">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="270d5-190">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="270d5-191">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="270d5-191">7/3/2012</span></span></p>
<p><span data-ttu-id="270d5-192">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="270d5-192">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-193"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-193"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-p113">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p113">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="270d5-196">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="270d5-196">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="270d5-p114">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p114">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="270d5-199">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="270d5-199">7/7/2012</span></span></p>
<p><span data-ttu-id="270d5-200">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="270d5-200">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="270d5-201">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="270d5-201">7/3/2012</span></span></p>
<p><span data-ttu-id="270d5-202">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="270d5-202">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-203"><strong>音声スイッチの原因</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-203"><strong>Voice switch cause</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-204">エコーを防ぐために、通話が半二重モードになっていた理由。</span><span class="sxs-lookup"><span data-stu-id="270d5-204">Reason why a call had to be placed into half duplex mode in order to prevent echo.</span></span> <span data-ttu-id="270d5-205">半二重モードでは、トランシーバーを使用して通信している場合と同じように、通信は一度に1つの方向にしか伝達されません。</span><span class="sxs-lookup"><span data-stu-id="270d5-205">In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span> <span data-ttu-id="270d5-206">次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-206">Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-207">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-207">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-208">なし</span><span class="sxs-lookup"><span data-stu-id="270d5-208">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-209">不正なタイムスタンプ</span><span class="sxs-lookup"><span data-stu-id="270d5-209">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-210">Echo</span><span class="sxs-lookup"><span data-stu-id="270d5-210">Echo</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-211">DNLP (動的非線形プロセッサ)</span><span class="sxs-lookup"><span data-stu-id="270d5-211">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-212">複雑さが低い</span><span class="sxs-lookup"><span data-stu-id="270d5-212">Low complexity</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-213">デバイスの状態が正しくない</span><span class="sxs-lookup"><span data-stu-id="270d5-213">Bad device state</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-214">AEC 後のエコー (アコースティックエコーキャンセル)</span><span class="sxs-lookup"><span data-stu-id="270d5-214">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-215"><strong>エコーの原因</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-215"><strong>Echo cause</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-216">通話で許可されたレベルより上のエコーが検出された理由。</span><span class="sxs-lookup"><span data-stu-id="270d5-216">Reason why echo above the accepted level was detected in a call.</span></span> <span data-ttu-id="270d5-217">(通信では、エコーはサウンドの反射になります。これと同じ現象が見られた場合は、通話の一番下まで移動しても聞こえます)。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-217">(In telecommunications, echo is a reflection of sound, the same phenomenon you will hear if you yell down to the bottom of a well.) Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-218">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-218">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-219">なし</span><span class="sxs-lookup"><span data-stu-id="270d5-219">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-220">不正なタイムスタンプ</span><span class="sxs-lookup"><span data-stu-id="270d5-220">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-221">AEC 後のエコー (アコースティックエコーキャンセル)</span><span class="sxs-lookup"><span data-stu-id="270d5-221">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-222">ANLP (アダプティブ非線形プロセッサ)</span><span class="sxs-lookup"><span data-stu-id="270d5-222">ANLP (adaptive nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-223">DNLP (動的非線形プロセッサ)</span><span class="sxs-lookup"><span data-stu-id="270d5-223">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-224">マイクのクリップ</span><span class="sxs-lookup"><span data-stu-id="270d5-224">Microphone clipping</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-225"><strong>通話の種類</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-225"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-226">行われた通話の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="270d5-226">Indicates the type of call that was made.</span></span> <span data-ttu-id="270d5-227">次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-227">Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-228">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-228">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-229">クライアント通話</span><span class="sxs-lookup"><span data-stu-id="270d5-229">Client call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-230">PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="270d5-230">PSTN call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-231">電話会議</span><span class="sxs-lookup"><span data-stu-id="270d5-231">Conference call</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-232"><strong>[アクセスの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-232"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-p118">クライアントが通話時に内部ネットワークにログオンしたか、外部ネットワークにログオンしたかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p118">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-235">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-235">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-236">内部</span><span class="sxs-lookup"><span data-stu-id="270d5-236">Internal</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-237">外部</span><span class="sxs-lookup"><span data-stu-id="270d5-237">External</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-238"><strong>[ネットワークの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-238"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-p119">通話時にクライアントが接続したネットワークの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p119">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-241">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-241">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-242">有線</span><span class="sxs-lookup"><span data-stu-id="270d5-242">Wired</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-243">ワイヤレス</span><span class="sxs-lookup"><span data-stu-id="270d5-243">Wireless</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-244"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-244"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-p120">通話時に外部クライアントが仮想プライベート ネットワーク (VPN) 接続を使用したかどうかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-p120">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-247">[すべて]</span><span class="sxs-lookup"><span data-stu-id="270d5-247">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-248">VPN</span><span class="sxs-lookup"><span data-stu-id="270d5-248">VPN</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-249">非 VPN</span><span class="sxs-lookup"><span data-stu-id="270d5-249">Non-VPN</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-250"><strong>デバイスの種類</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-250"><strong>Device type</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-251">デバイスの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="270d5-251">Indicates the type of device.</span></span> <span data-ttu-id="270d5-252">次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="270d5-252">Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-253">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-253">Capture device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-254">レンダー デバイス</span><span class="sxs-lookup"><span data-stu-id="270d5-254">Render device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="270d5-255">デバイスペアのキャプチャとレンダリング</span><span class="sxs-lookup"><span data-stu-id="270d5-255">Capture/Render device pair</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-256"><strong>デバイス名</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-256"><strong>Device name</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-257">キャプチャまたはレンダーデバイスの名前。</span><span class="sxs-lookup"><span data-stu-id="270d5-257">Name of the capture or render device.</span></span> <span data-ttu-id="270d5-258">完全なデバイス名、またはデバイス名の任意の部分を入力できます。</span><span class="sxs-lookup"><span data-stu-id="270d5-258">You can enter the complete device name or any portion of the device name.</span></span> <span data-ttu-id="270d5-259">たとえば、デバイスマイク (Microsoft LifeCam VX-1000) を見つけるには、次のように完全なデバイス名を入力します。</span><span class="sxs-lookup"><span data-stu-id="270d5-259">For example, to find the device Microphone (Microsoft LifeCam VX-1000.), you can enter the complete device name as follows:</span></span></p>
<p><span data-ttu-id="270d5-260">マイク (Microsoft LifeCam VX-1000)</span><span class="sxs-lookup"><span data-stu-id="270d5-260">Microphone (Microsoft LifeCam VX-1000.)</span></span></p>
<p><span data-ttu-id="270d5-261">または、名前の一部だけを入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="270d5-261">Or, you can enter just a portion of the name.</span></span> <span data-ttu-id="270d5-262">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="270d5-262">For example:</span></span></p>
<p><span data-ttu-id="270d5-263">LifeCam</span><span class="sxs-lookup"><span data-stu-id="270d5-263">LifeCam</span></span></p>
<p><span data-ttu-id="270d5-264">上のフィルターでは、 &quot; 名前の任意の場所に文字列 LifeCam が含まれているすべてのデバイスが返されることに注意して &quot; ください。</span><span class="sxs-lookup"><span data-stu-id="270d5-264">Note that the preceding filter returns any device that contains the string &quot;LifeCam&quot; anywhere in its name.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="270d5-265">指標</span><span class="sxs-lookup"><span data-stu-id="270d5-265">Metrics</span></span>

<span data-ttu-id="270d5-266">次の表は、デバイスレポートに表示される情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="270d5-266">The following table lists the information provided in the Device Report.</span></span>

### <a name="device-report-metrics"></a><span data-ttu-id="270d5-267">デバイスレポートのメトリック</span><span class="sxs-lookup"><span data-stu-id="270d5-267">Device Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="270d5-268">名前</span><span class="sxs-lookup"><span data-stu-id="270d5-268">Name</span></span></th>
<th><span data-ttu-id="270d5-269">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="270d5-269">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="270d5-270">説明</span><span class="sxs-lookup"><span data-stu-id="270d5-270">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="270d5-271"><strong>デバイスをキャプチャする</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-271"><strong>Capture device</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-272">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-272">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-273">デバイス (マイクや web カメラなど) を使ってオーディオを送信します。</span><span class="sxs-lookup"><span data-stu-id="270d5-273">Device (for example, a microphone or webcam) used for transmitting audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-274"><strong>レンダリングデバイス</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-274"><strong>Render device</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-275">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-275">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-276">オーディオを受信するために使用されるデバイス (ヘッドセットやスピーカーなど)。</span><span class="sxs-lookup"><span data-stu-id="270d5-276">Device (for example, a headset or speakers) used for receiving audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-277"><strong>通話ボリューム</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-277"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-278">可</span><span class="sxs-lookup"><span data-stu-id="270d5-278">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-279">発信された通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="270d5-279">Total number of calls placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-280"><strong>低品質通話のパーセンテージ</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-280"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-281">可</span><span class="sxs-lookup"><span data-stu-id="270d5-281">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-282">低品質として分類された通話の割合 &quot; 。 &quot; 低品質通話とは、測定されたメトリックの少なくとも1つが許可値 (過大なジッターを経験した呼び出しなど) を超えた呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="270d5-282">Percentage of calls that were classified as &quot;poor.&quot; A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-283"><strong>一意のユーザー</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-283"><strong>Unique users</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-284">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-285">デバイスを使用した一意のユーザー。</span><span class="sxs-lookup"><span data-stu-id="270d5-285">Unique users who used the device.</span></span> <span data-ttu-id="270d5-286">ユーザーがデバイスを13回使用した場合、1つの一意のユーザーとしてカウントされます。これは、そのデバイスを1回だけ使用したユーザーと同じです。</span><span class="sxs-lookup"><span data-stu-id="270d5-286">If a user used the device 13 times he or she would count as one unique user, the same as a user who only used the device a single time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-287"><strong>音声切り替え時間の比率</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-287"><strong>Ratio of voice switch time</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-288">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-289">エコーを防ぐために、半二重モードで実行する必要があった通話の割合。</span><span class="sxs-lookup"><span data-stu-id="270d5-289">Percentage of the call that had to be conducted in half duplex mode in order to prevent echo.</span></span> <span data-ttu-id="270d5-290">半二重モードでは、トランシーバーを使用して通信している場合と同じように、通信は一度に1つの方向にしか伝達されません。</span><span class="sxs-lookup"><span data-stu-id="270d5-290">In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-291"><strong>マイクの比率が機能しない</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-291"><strong>Ratio of microphone not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-292">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-293">キャプチャデバイスが許容レベルで機能していなかった通話の割合。</span><span class="sxs-lookup"><span data-stu-id="270d5-293">Percentage of the call in which the capture device was not functioning at an acceptable level.</span></span> <span data-ttu-id="270d5-294">大きい値を指定すると、主に、キャプチャデバイスが予期したとおりに動作しないことが原因で、通話の品質の問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="270d5-294">A high values suggests that quality issues with the call were primarily due to the capture device not working as expected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-295"><strong>スピーカーが機能しない場合の比率</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-295"><strong>Ratio of speaker not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-296">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-297">レンダーデバイスが許容レベルで機能していなかった通話の割合。</span><span class="sxs-lookup"><span data-stu-id="270d5-297">Percentage of the call in which the render device was not functioning at an acceptable level.</span></span> <span data-ttu-id="270d5-298">高い値を指定すると、主に、レンダリングデバイスが予期したとおりに動作しないことが原因となって、通話の品質の問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="270d5-298">A high values suggests that quality issues with the call were primarily due to the render device not working as expected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-299"><strong>音声スイッチを使った通話 (%)</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-299"><strong>Calls with voice switch (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-300">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-300">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-301">半二重モードに設定された合計通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="270d5-301">Percentage of the total calls which had to be placed into half duplex mode.</span></span> <span data-ttu-id="270d5-302">半二重モードでは、トランシーバーを使用して通信している場合と同じように、通信は一度に1つの方向にしか伝達されません。</span><span class="sxs-lookup"><span data-stu-id="270d5-302">In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-303"><strong>エコーマイク (%)</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-303"><strong>Echo microphone in (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-304">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-305">マイクのキャプチャストリームでエコーが検出された時間の割合。</span><span class="sxs-lookup"><span data-stu-id="270d5-305">Percentage of time when echo was detected in the microphone capture stream.</span></span> <span data-ttu-id="270d5-306">一般的に、ヘッドセットまたはハンドセットの値は低く、スピーカーフォンやスタンドアロンスピーカーでは高くなります。</span><span class="sxs-lookup"><span data-stu-id="270d5-306">Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers.</span></span> <span data-ttu-id="270d5-307">オンボード音響エコーキャンセルをサポートしているデバイスでは、高値を指定するとエコーリークが発生します。</span><span class="sxs-lookup"><span data-stu-id="270d5-307">For devices that support on-board acoustic echo cancellation, high values indicate echo leak.</span></span> <span data-ttu-id="270d5-308">その他のデバイスでは、デバイスの品質を評価するためにこのメトリックを使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="270d5-308">For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="270d5-309"><strong>エコー送信 (%)</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-309"><strong>Echo send (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-310">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-311">他のユーザーに送信されたエコーのパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="270d5-311">Percentage of echo transmitted to other users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="270d5-312"><strong>エコー (%) で通話</strong></span><span class="sxs-lookup"><span data-stu-id="270d5-312"><strong>Calls with echo (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="270d5-313">はい</span><span class="sxs-lookup"><span data-stu-id="270d5-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="270d5-314">エコーが許容レベルを超えていた合計通話の割合。</span><span class="sxs-lookup"><span data-stu-id="270d5-314">Percentage of the total calls that had echo exceeding the acceptable level.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="270d5-315">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="270d5-315">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

