---
title: 'Lync Server 2013: Lync PreCall ツール'
description: 'Lync Server 2013: Lync PreCall ツール。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync PreCall Diagnostics Tool
ms:assetid: 0ff291ec-cfb4-43eb-b5d6-a7a325681e3f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn451255(v=OCS.15)
ms:contentKeyID: 56708404
ms.date: 11/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c2c51551fe0991eb354a628b1d4660baa1532b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426336"
---
# <a name="lync-precall-diagnostics-tool-in-lync-server-2013"></a><span data-ttu-id="8b0d6-103">Lync の PreCall のすべての診断ツール (Lync Server 2013)</span><span class="sxs-lookup"><span data-stu-id="8b0d6-103">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b0d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b0d6-104">

<span> </span></span></span>

<span data-ttu-id="8b0d6-105">_**最終更新日:** 2016-11-04_</span><span class="sxs-lookup"><span data-stu-id="8b0d6-105">_**Topic Last Modified:** 2016-11-04_</span></span>

<span data-ttu-id="8b0d6-106">Lync PreCall Diagnostics ツール (PCD) はクライアントベースのアプリケーションであり、ネットワークの現在の状態が、今後のエンタープライズ音声通話での音声品質にどのように影響するかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-106">The Lync PreCall Diagnostics Tool (PCD) is a client-based application that allows you to see how the current state of your network might impact the audio quality in an upcoming Enterprise Voice call.</span></span>

<span data-ttu-id="8b0d6-107">PCD は、ネットワークの最後のホップが脆弱である可能性が高い場合 (たとえば、公共の WiFi ネットワークまたはホームユーザーのノート pc など) に最も役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-107">PCD is most useful in situations where the last hop of a network is likely to be the weakest (for example, with laptops on a public WiFi network or home users).</span></span> <span data-ttu-id="8b0d6-108">PCD は、ネットワークのこの最終区間を走査する小さなパケットストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-108">PCD creates a small packet stream that traverses this final leg of the network.</span></span> <span data-ttu-id="8b0d6-109">このツールは、パケットストリームを分析して、この区間でのジッターと損失が通話品質にどのように影響するかを予測し、レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-109">The tool then analyzes the packet stream to estimate how the jitter and loss along this leg might impact call quality, and then provides a report.</span></span> <span data-ttu-id="8b0d6-110">PCD は、通話が行われているときでも、クライアントで継続的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-110">You can run PCD continuously on the client, even while calls are being placed.</span></span> <span data-ttu-id="8b0d6-111">パケットストリームは、帯域幅に大きな影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-111">The packet stream does not have a significant effect on bandwidth.</span></span>

<span data-ttu-id="8b0d6-112">**PCD バージョン1.1 の最新のリリースには、次の機能強化が含まれています。**</span><span class="sxs-lookup"><span data-stu-id="8b0d6-112">**The latest release of the PCD, version 1.1, includes the following enhancements:**</span></span>

  - <span data-ttu-id="8b0d6-113">長いパスワードをサポートし、最大127文字まで使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-113">Support for longer passwords, which can now be up to 127 characters</span></span>

  - <span data-ttu-id="8b0d6-114">認証サインインの問題に関する追加診断</span><span class="sxs-lookup"><span data-stu-id="8b0d6-114">Additional diagnostics for authentication sign-in issues</span></span>

  - <span data-ttu-id="8b0d6-115">Lync ハイブリッド展開のサポートが向上</span><span class="sxs-lookup"><span data-stu-id="8b0d6-115">Better support for Lync hybrid deployments</span></span>

  - <span data-ttu-id="8b0d6-116">資格情報ピッカーの更新</span><span class="sxs-lookup"><span data-stu-id="8b0d6-116">Updates to credential picker</span></span>

  - <span data-ttu-id="8b0d6-117">安定性の向上</span><span class="sxs-lookup"><span data-stu-id="8b0d6-117">Stability improvements</span></span>

<span data-ttu-id="8b0d6-118">ご意見をお寄せいただき、ありがとうございます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-118">We appreciate any feedback.</span></span> <span data-ttu-id="8b0d6-119">すべてのサポート質問または問題を [PCD のフィードバック](mailto:pcdfb@microsoft.com) エイリアスに送信してください <pcdfb@microsoft.com> 。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-119">Please send all support questions or issues to the [PCD Feedback](mailto:pcdfb@microsoft.com) alias at <pcdfb@microsoft.com>.</span></span>

<span data-ttu-id="8b0d6-120">このトピックには次のセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-120">This topic includes the following sections:</span></span>

  - <span data-ttu-id="8b0d6-121">Lync PCD のバージョン</span><span class="sxs-lookup"><span data-stu-id="8b0d6-121">Lync PCD Versions</span></span>

  - <span data-ttu-id="8b0d6-122">Lync PCD システム要件</span><span class="sxs-lookup"><span data-stu-id="8b0d6-122">Lync PCD System Requirements</span></span>

  - <span data-ttu-id="8b0d6-123">Lync PCD の機能</span><span class="sxs-lookup"><span data-stu-id="8b0d6-123">Lync PCD Features</span></span>

  - <span data-ttu-id="8b0d6-124">Lync PCD を実行する</span><span class="sxs-lookup"><span data-stu-id="8b0d6-124">Running Lync PCD</span></span>

  - <span data-ttu-id="8b0d6-125">Lync PCD をアンインストールする</span><span class="sxs-lookup"><span data-stu-id="8b0d6-125">Uninstalling Lync PCD</span></span>

<span id="Version"></span>

<div>

## <a name="lync-pcd-versions"></a><span data-ttu-id="8b0d6-126">Lync PCD のバージョン</span><span class="sxs-lookup"><span data-stu-id="8b0d6-126">Lync PCD Versions</span></span>

<span data-ttu-id="8b0d6-127">このトピックでは、無料でダウンロードできるツールの次のバージョンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-127">This topic describes the following versions of the tool, available for free download:</span></span>

  - <span data-ttu-id="8b0d6-128">Windows デスクトップアプリ ( [https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914) )</span><span class="sxs-lookup"><span data-stu-id="8b0d6-128">Windows Desktop App ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914))</span></span>

</div>

<span id="Requirements"></span>

<div>

## <a name="lync-pcd-system-requirements"></a><span data-ttu-id="8b0d6-129">Lync PCD システム要件</span><span class="sxs-lookup"><span data-stu-id="8b0d6-129">Lync PCD System Requirements</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8b0d6-130">PCD をご利用になるには、ユニファイドコミュニケーション Web API (UCWA) をインストールして、Lync Server の展開でモバイルクライアントをサポートするように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-130">PCD requires that Unified Communications Web API (UCWA) be installed and configured to support mobile clients in the Lync Server deployment.</span></span> <span data-ttu-id="8b0d6-131">UCWA は Lync Server と共にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-131">UCWA is installed with Lync Server.</span></span>



</div>

<div>

## <a name="windows-desktop-app-requirements"></a><span data-ttu-id="8b0d6-132">Windows デスクトップアプリの要件</span><span class="sxs-lookup"><span data-stu-id="8b0d6-132">Windows Desktop App Requirements</span></span>

  - <span data-ttu-id="8b0d6-133">Windows 7 または Windows 8 オペレーティングシステムの任意のエディション</span><span class="sxs-lookup"><span data-stu-id="8b0d6-133">Any edition of the Windows 7 or Windows 8 operating system</span></span>

  - <span data-ttu-id="8b0d6-134">Microsoft .NET Framework 4.5 は、で入手できます。 [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span><span class="sxs-lookup"><span data-stu-id="8b0d6-134">Microsoft .NET Framework 4.5 available at [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span></span>

</div>

</div>

<span id="features"></span>

<div>

## <a name="lync-pcd-features"></a><span data-ttu-id="8b0d6-135">Lync PCD の機能</span><span class="sxs-lookup"><span data-stu-id="8b0d6-135">Lync PCD Features</span></span>

<span data-ttu-id="8b0d6-136">Lync PCD には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-136">Lync PCD includes the following features:</span></span>

  - <span data-ttu-id="8b0d6-137">既定ではオンデマンドで実行する (2 分バースト)</span><span class="sxs-lookup"><span data-stu-id="8b0d6-137">Run in default On Demand (2 minute bursts)</span></span>

  - <span data-ttu-id="8b0d6-138">Always On (スナップビューで最大24時間) モードで実行する</span><span class="sxs-lookup"><span data-stu-id="8b0d6-138">Run in Always On (up to 24 hours in snapped view) mode</span></span>

  - <span data-ttu-id="8b0d6-139">テストの実行の履歴ビュー</span><span class="sxs-lookup"><span data-stu-id="8b0d6-139">Historical view of your test runs</span></span>

  - <span data-ttu-id="8b0d6-140">サインインエラーの診断 (Windows 8 向け Lync PCD)</span><span class="sxs-lookup"><span data-stu-id="8b0d6-140">Diagnose sign-in failures (Lync PCD for Windows 8 only)</span></span>

<span data-ttu-id="8b0d6-141">![Lync PCD 機能のサインインの進行状況を示すスクリーンショット](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD 機能のサインインの進行状況を示すスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="8b0d6-141">![Lync PCD features Sign in progress screen shot](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD features Sign in progress screen shot")</span></span>

  - <span data-ttu-id="8b0d6-142">ネットワークメトリックのグラフィカル表示–ネットワーク MOS、パケット損失、および全画面表示とスナップビューでの着信のジッター。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-142">Graphical view of network metrics – Network MOS, Packet Loss and Interarrival Jitter in full screen and snapped view.</span></span>

<span data-ttu-id="8b0d6-143">**全画面表示**</span><span class="sxs-lookup"><span data-stu-id="8b0d6-143">**Full screen view**</span></span>

<span data-ttu-id="8b0d6-144">![PreCall 診断ツールのテスト結果のグラフ](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall 診断ツールのテスト結果のグラフ")</span><span class="sxs-lookup"><span data-stu-id="8b0d6-144">![PreCall Diagnostic Tool test result graphs](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic Tool test result graphs")</span></span>

<span data-ttu-id="8b0d6-145">**スナップビュー**</span><span class="sxs-lookup"><span data-stu-id="8b0d6-145">**Snapped view**</span></span>

<span data-ttu-id="8b0d6-146">![PreCall 診断ツール、使用状況テストの結果](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall 診断ツール、使用状況テストの結果")</span><span class="sxs-lookup"><span data-stu-id="8b0d6-146">![PreCall Diagnostic Tool Utilization test results](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic Tool Utilization test results")</span></span>

</div>

<span id="running"></span>

<div>

## <a name="running-lync-pcd"></a><span data-ttu-id="8b0d6-147">Lync PCD を実行する</span><span class="sxs-lookup"><span data-stu-id="8b0d6-147">Running Lync PCD</span></span>

<div>

## <a name="running-windows-desktop-app"></a><span data-ttu-id="8b0d6-148">Windows デスクトップアプリを実行している場合</span><span class="sxs-lookup"><span data-stu-id="8b0d6-148">Running Windows Desktop App</span></span>

1.  <span data-ttu-id="8b0d6-149">Windows 7 システムで PCD を開始するには、[**スタート**] メニューから [**すべての診断** を事前に実行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-149">To start the PCD on a Windows 7 system, select **PreCall Diagnostics** from the **Start** menu.</span></span>
    
    <span data-ttu-id="8b0d6-150">Windows 8 システムで PCD を開始するには、スタート画面でアイコンを選ぶか、"すべての診断" を検索します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-150">To start the PCD on a Windows 8 system, select the icon on your Start screen, or search for “PreCall Diagnostics.”</span></span>
    
    <span data-ttu-id="8b0d6-151">![PreCall 診断ツール アイコン](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall 診断ツール アイコン")</span><span class="sxs-lookup"><span data-stu-id="8b0d6-151">![PreCall Diagnostic tool icon](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic tool icon")</span></span>

2.  <span data-ttu-id="8b0d6-152">ツールが起動したら、資格情報を提供するための推奨される方法を選択し、[ **すべての診断ツールのオプション** ] ダイアログボックスでネットワークの動作モードを選択して、[ **OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-152">When the tool starts, select your preferred method of providing credentials and select the network operating mode in the **PreCall Diagnostics Tool Options** dialog box, then select **OK**:</span></span>

3.  <span data-ttu-id="8b0d6-153">[ **テストの開始** ] ボタンを選択して診断の実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-153">Select the **Start Test** button to start running diagnostics.</span></span>
    
    <span data-ttu-id="8b0d6-154">[ **ネットワーク資格情報を使用** する] オプションを選択した場合、テストは直ちに開始されます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-154">If you selected the **Use network credentials** option, the test begins immediately.</span></span>
    
    <span data-ttu-id="8b0d6-155">[ **資格情報を入力** する] オプションを選んだ場合は、[ **Windows セキュリティ** ] ダイアログボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-155">If you selected the **Let me enter my credentials** option, the **Windows Security** dialog box opens.</span></span> <span data-ttu-id="8b0d6-156">資格情報を入力すると、テストが開始されます。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-156">After you enter your credentials, the test starts.</span></span>

</div>

</div>

<span id="uninstall"></span>

<div>

## <a name="uninstalling-lync-pcd"></a><span data-ttu-id="8b0d6-157">Lync PCD をアンインストールする</span><span class="sxs-lookup"><span data-stu-id="8b0d6-157">Uninstalling Lync PCD</span></span>

<span data-ttu-id="8b0d6-158">Lync PCD を削除するには、使用しているオペレーティングシステムの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-158">To remove Lync PCD, follow the procedure for your operating system:</span></span>

  - <span data-ttu-id="8b0d6-159">Windows 7 システムでは、 **コントロールパネル** を開き、[ **プログラムと機能**] を選択して、[ **Lync 2013 precall Diagnostics**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-159">On a Windows 7 system, open the **Control Panel**, select **Programs and Features**, and double-click **Lync 2013 PreCall Diagnostics**.</span></span>

  - <span data-ttu-id="8b0d6-160">Windows 8 システムでは、PCD タイルを右クリックして、スタート画面の下部にあるアプリバーから [ **アンインストール** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b0d6-160">On a Windows 8 system, right-click on the PCD tile and click **Uninstall** from the app bar at the bottom of the start screen.</span></span>

<span data-ttu-id="8b0d6-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b0d6-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

