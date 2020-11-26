---
title: 'Lync Server 2013: 監視サーバーレポートの表示と分析'
description: 'Lync Server 2013: 監視サーバーレポートの表示と分析。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing and analyzing monitoring server reports
ms:assetid: 4dd448f1-01d2-49b2-b109-0728f36566b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720332(v=OCS.15)
ms:contentKeyID: 63969599
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f2a1812d76a49d487bea35acae3e22ea403f105
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444008"
---
# <a name="viewing-and-analyzing-monitoring-server-reports-in-lync-server-2013"></a><span data-ttu-id="38e5a-103">Lync Server 2013 で監視サーバーレポートを表示および分析する</span><span class="sxs-lookup"><span data-stu-id="38e5a-103">Viewing and analyzing monitoring server reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38e5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38e5a-104">

<span> </span></span></span>

<span data-ttu-id="38e5a-105">_**最終更新日:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="38e5a-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="38e5a-106">サーバーレポートを監視すると、音声品質のさまざまな測定が行われ、エンドユーザーに配信される QoE が監視されます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-106">Monitoring Server reports provides several different measures of voice quality to monitor the QoE that is being delivered to end-users.</span></span> <span data-ttu-id="38e5a-107">さらに、Monitoring Server には、組織のネットワークの使用状況やメディア品質の傾向を監視したり、発生したメディアの品質に関する問題のトラブルシューティングに使用できる、いくつかの組み込みレポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="38e5a-107">Additionally, Monitoring Server includes several built-in reports that your organization can use to watch usage and media quality trends on your organization's network and troubleshoot media quality issues that arise.</span></span>

<span data-ttu-id="38e5a-108">毎日および毎週の操作でサーバーレポートの監視を行う主な部分は、次のようにメディア品質レポートを表示して分析することです。</span><span class="sxs-lookup"><span data-stu-id="38e5a-108">A primary part of keeping Monitoring Server Reports interesting for daily and weekly operations is viewing and analyzing Media Quality Reports, in particular:</span></span>

  - <span data-ttu-id="38e5a-109">QoE サマリー/トレンドレポート</span><span class="sxs-lookup"><span data-stu-id="38e5a-109">QoE Summary/Trend Reports</span></span>

  - <span data-ttu-id="38e5a-110">QoE のパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="38e5a-110">QoE Performance Reports</span></span>

<div>

## <a name="view-reports-from-the-monitoring-server"></a><span data-ttu-id="38e5a-111">監視サーバーからレポートを表示する</span><span class="sxs-lookup"><span data-stu-id="38e5a-111">View reports from the monitoring server</span></span>

1.  <span data-ttu-id="38e5a-112">Web ブラウザーから、SQL reporting services をホストしているサーバーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-112">From a web browser, locate your servers hosting the SQL reporting services.</span></span>

2.  <span data-ttu-id="38e5a-113">ブラウザー画面から必要なレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-113">View the required reports from the browser screen.</span></span>

3.  <span data-ttu-id="38e5a-114">省略エクスポートオプションと必要な出力形式を選択して、レポートをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-114">(Optional) Export a report by selecting the export option and the required output format.</span></span>

</div>

<div>

## <a name="configure-call-detail-recording-cdr"></a><span data-ttu-id="38e5a-115">通話の詳細記録 (CDR) を構成する</span><span class="sxs-lookup"><span data-stu-id="38e5a-115">Configure call detail recording (CDR)</span></span>

1.  <span data-ttu-id="38e5a-116">RTCUniversalServerAdmins グループのメンバーであるか (同等の権限を持つ)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントから、Lync Server 2013 を展開したネットワーク内の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent permissions), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="38e5a-117">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="38e5a-118">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**通話詳細記録**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="38e5a-119">[**通話詳細記録**] ページで、表から適切なサイトをクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-119">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="38e5a-120">[削除] を有効にするには、[ **監視サーバーに対して消去を有効** にする] を選択します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-120">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="38e5a-121">[ **通話の詳細記録を保持する期間 (日数)]:** 通話の詳細レコーディングの保持期間の最大値を選びます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-121">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="38e5a-122">[**エラー報告データの最大保持期間 (日)**] で、 エラー報告を保持する必要のある最大日数を選択します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-122">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="38e5a-123">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="configure-qoe"></a><span data-ttu-id="38e5a-124">QoE の構成</span><span class="sxs-lookup"><span data-stu-id="38e5a-124">Configure QoE</span></span>

1.  <span data-ttu-id="38e5a-125">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-125">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="38e5a-126">詳細については、「Delegate Setup Permissions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38e5a-126">For details, see Delegate Setup Permissions.</span></span>

2.  <span data-ttu-id="38e5a-127">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="38e5a-128">左側のナビゲーション バーで [**監視とアーカイブ**] をクリックし、[**QoE データ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-128">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="38e5a-129">[**QoE データ**] ページで、表から該当するサイトをクリックして、[**編集**] をクリックし、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-129">On the **Quality of Experience Data** page, click the appropriate site from the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="38e5a-130">[削除] を有効にするには、[ **監視サーバーに対して消去を有効** にする] を選択します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-130">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="38e5a-131">[ **通話を継続する] の [最長時間 (日数)]:** qoe データを保持する最大日数を選びます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-131">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that QoE data should be retained.</span></span>

7.  <span data-ttu-id="38e5a-132">[コミット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-132">Click Commit.</span></span>

</div>

<div>

## <a name="change-the-archiving-policy"></a><span data-ttu-id="38e5a-133">アーカイブポリシーを変更する</span><span class="sxs-lookup"><span data-stu-id="38e5a-133">Change the archiving policy</span></span>

1.  <span data-ttu-id="38e5a-134">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-134">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="38e5a-135">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-135">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="38e5a-136">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-136">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="38e5a-137">ポリシーの一覧の [**グローバル**] をクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-137">Click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="38e5a-138">[**アーカイブ ポリシーの編集 - グローバル**] で、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-138">In **Edit Archiving Policy - Global**, do the following:</span></span>

6.  <span data-ttu-id="38e5a-139">展開の内部アーカイブを有効または無効にするには、[ **内部通信をアーカイブ** する] チェックボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-139">To enable or disable internal archiving for the deployment, select or clear the **Archive internal communications** check box.</span></span>

7.  <span data-ttu-id="38e5a-140">展開の外部アーカイブを有効または無効にするには、[ **外部の通信をアーカイブ** する] チェックボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-140">To enable or disable external archiving for the deployment, select or clear the **Archive external communications** check box.</span></span>

8.  <span data-ttu-id="38e5a-141">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-141">Click **Commit**.</span></span>

</div>

<div>

## <a name="apply-an-archiving-policy-to-a-user"></a><span data-ttu-id="38e5a-142">ユーザーにアーカイブポリシーを適用する</span><span class="sxs-lookup"><span data-stu-id="38e5a-142">Apply an archiving policy to a user</span></span>

1.  <span data-ttu-id="38e5a-143">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-143">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="38e5a-144">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="38e5a-144">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="38e5a-145">左側のナビゲーション バーで [**ユーザー**] をクリックし、構成するユーザー アカウントを検索します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-145">In the left navigation bar, click **Users**, and then search on the user account that you want to configure.</span></span>

4.  <span data-ttu-id="38e5a-146">検索結果一覧の表でユーザー アカウントをクリックし、[**編集**] をクリックして、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-146">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="38e5a-147">[**アーカイブポリシー**] の [ **Lync Server ユーザーの編集**] で、適用するアーカイブユーザーポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="38e5a-147">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>

6.  <span data-ttu-id="38e5a-148">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e5a-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="38e5a-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="38e5a-149">See Also</span></span>


[<span data-ttu-id="38e5a-150">Lync Server 2013 で監視レポートを使用する</span><span class="sxs-lookup"><span data-stu-id="38e5a-150">Using Monitoring Reports in Lync Server 2013</span></span>](lync-server-2013-using-monitoring-reports.md)  
[<span data-ttu-id="38e5a-151">Lync Server 2013 のサーバーパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="38e5a-151">Server Performance Report in Lync Server 2013</span></span>](lync-server-2013-server-performance-report.md)  
[<span data-ttu-id="38e5a-152">Lync Server 2013 のメディア品質比較レポート</span><span class="sxs-lookup"><span data-stu-id="38e5a-152">Media Quality Comparison Report in Lync Server 2013</span></span>](lync-server-2013-media-quality-comparison-report.md)  
  

<span data-ttu-id="38e5a-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38e5a-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

