---
title: 'Lync Server 2013: 一元ログサービスからのキャプチャログの読み取り'
description: 'Lync Server 2013: 中央のログサービスからキャプチャログを読み取ります。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reading capture logs from the Centralized Logging Service
ms:assetid: c86ccf61-d86f-4ebd-b8d1-984a1b73005d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721879(v=OCS.15)
ms:contentKeyID: 49733813
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcdd70c924b49098814e80a375ae34d2bf48dc41
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436772"
---
# <a name="reading-capture-logs-from-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="88de5-103">Lync Server 2013 の一元ログサービスからのキャプチャログの読み取り</span><span class="sxs-lookup"><span data-stu-id="88de5-103">Reading capture logs from the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88de5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88de5-104">

<span> </span></span></span>

<span data-ttu-id="88de5-105">_**最終更新日:** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="88de5-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="88de5-106">検索を実行した後で一元管理サービスの実際の利点を実感し、報告された問題を追跡するために使用できるファイルを用意しています。</span><span class="sxs-lookup"><span data-stu-id="88de5-106">You realize the real benefit of the Centralized Logging Service after you run the search and you have a file that you can use to track down a reported problem.</span></span> <span data-ttu-id="88de5-107">このファイルは、さまざまな方法で読むことができます。</span><span class="sxs-lookup"><span data-stu-id="88de5-107">There are a number of ways that you can read the file.</span></span> <span data-ttu-id="88de5-108">出力ファイルは標準のテキスト形式なので、メモ帳など、テキスト ファイルを開いて読むことができる任意のプログラムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-108">The output file is in a standard text format and you can use Notepad.exe or any other programs that will allow you to open and read a text file.</span></span> <span data-ttu-id="88de5-109">大規模なファイルとより複雑な問題については、集中ログサービスからのログ出力の読み取りと解析を目的とした Snooper.exe などのツールを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="88de5-109">For larger files and more complex issues, you could use a tool like Snooper.exe that is designed to read and parse the logging output from the Centralized Logging Service.</span></span> <span data-ttu-id="88de5-110">Snooper は、個別のダウンロードとして利用できる Lync Server 2013 デバッグツールに含まれています。</span><span class="sxs-lookup"><span data-stu-id="88de5-110">Snooper is included with the Lync Server 2013 Debug Tools that are available as a separate download.</span></span> <span data-ttu-id="88de5-111">Lync Server 2013 デバッグツールは、次のページからダウンロードでき [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257) ます。</span><span class="sxs-lookup"><span data-stu-id="88de5-111">You can download the Lync Server 2013 Debug Tools here: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257).</span></span> <span data-ttu-id="88de5-112">Lync Server 2013 デバッグツールをインストールすると、短い切り取りとメニュー項目は作成されません。</span><span class="sxs-lookup"><span data-stu-id="88de5-112">When you install the Lync Server 2013 Debug Tools, short cuts and menu items are not created.</span></span> <span data-ttu-id="88de5-113">Lync Server 2013 デバッグツールをインストールしたら、Windows エクスプローラー、コマンドラインウィンドウ、または Lync Server Management Shell を開いて、ディレクトリ (既定の場所) C: \\ Program Files \\ Microsoft Lync Server 2013 \\ デバッグツールを開きます。</span><span class="sxs-lookup"><span data-stu-id="88de5-113">After you install the Lync Server 2013 Debug Tools, open Windows Explorer, a command-line window, or Lync Server Management Shell and go to the directory (default location) C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="88de5-114">[Snooper.exe または Snooper.exe をダブルクリックして、コマンドラインまたは Lync Server Management Shell を使用している場合は、ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="88de5-114">Double-click Snooper.exe or type Snooper.exe, and then press ENTER if you are using the command line or Lync Server Management Shell.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="88de5-115">このトピックの目的は、トラブルシューティングの手法を詳細に説明したり議論したりすることではありません。</span><span class="sxs-lookup"><span data-stu-id="88de5-115">The intent of this topic is not to detail and discuss troubleshooting techniques.</span></span> <span data-ttu-id="88de5-116">トラブルシューティングとそれに関連するプロセスは、複雑な問題です。</span><span class="sxs-lookup"><span data-stu-id="88de5-116">Troubleshooting and the processes around it is a complex subject.</span></span> <span data-ttu-id="88de5-117">基本的なトラブルシューティングと特定のワークロードのトラブルシューティングの詳細については、「Microsoft Lync Server 2010 リソースキット」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A> 。</span><span class="sxs-lookup"><span data-stu-id="88de5-117">For details about troubleshooting basics and troubleshooting specific workloads, see the Microsoft Lync Server 2010 Resource Kit book at <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A>.</span></span> <span data-ttu-id="88de5-118">プロセスと手順は、引き続き Lync Server 2013 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-118">The processes and procedures still apply to Lync Server 2013.</span></span>



</div>

<span data-ttu-id="88de5-119">Lync Server 2013 には、いくつかの新機能が含まれている Snooper の更新バージョンが導入されています。</span><span class="sxs-lookup"><span data-stu-id="88de5-119">Lync Server 2013 introduces an updated version of Snooper that includes some new features.</span></span> <span data-ttu-id="88de5-120">次のスクリーンショットは、Office Communications Server 2007 からの Snooper のバージョンを示しています。</span><span class="sxs-lookup"><span data-stu-id="88de5-120">The following screen shot shows the version of Snooper from Office Communications Server 2007.</span></span>

<span data-ttu-id="88de5-121">![Office Communications 2007 バージョンの Snooper。](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Office Communications 2007 バージョンの Snooper。")</span><span class="sxs-lookup"><span data-stu-id="88de5-121">![Office Communications 2007 version of Snooper.](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Office Communications 2007 version of Snooper.")</span></span>

<span data-ttu-id="88de5-122">次のスクリーンショットは、Lync Server 2013 デバッグツールに含まれている Snooper の新しいバージョンを示しています。</span><span class="sxs-lookup"><span data-stu-id="88de5-122">The following screen shot shows the new version of Snooper included in the Lync Server 2013 Debug Tools.</span></span>

<span data-ttu-id="88de5-123">![Snooper の Lync Server 2013 バージョン。](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Snooper の Lync Server 2013 バージョン。")</span><span class="sxs-lookup"><span data-stu-id="88de5-123">![Lync Server 2013 version of Snooper.](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Lync Server 2013 version of Snooper.")</span></span>

<span data-ttu-id="88de5-124">次のスクリーンショットは、よく使われる関数を含むツールバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="88de5-124">The following screen shot shows the toolbar with frequently used functions.</span></span>

<span data-ttu-id="88de5-125">![Snooper 2013 ツールバー。](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Snooper 2013 ツールバー。")</span><span class="sxs-lookup"><span data-stu-id="88de5-125">![Snooper 2013 toolbar.](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Snooper 2013 toolbar.")</span></span>

<span data-ttu-id="88de5-126">また、値を追加する最新の機能は、フローチャート (コールフロー) ダイアグラムビューです。</span><span class="sxs-lookup"><span data-stu-id="88de5-126">And, the newest feature that adds value is the Flow Chart (call flow) diagram view.</span></span> <span data-ttu-id="88de5-127">[ **メッセージ** ] タブでメッセージフローを選択し、[ **通話フロー** ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-127">You select a message flow in the **Message** tab and click the **Call Flow** button.</span></span> <span data-ttu-id="88de5-128">メッセージを移動すると、コールフローダイアグラムが新しいデータで更新されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-128">As you proceed through the messages, the call flow diagram updates with new data.</span></span>

<span data-ttu-id="88de5-129">![Snooper 2013 コールフロー図。](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Snooper 2013 コールフロー図。")</span><span class="sxs-lookup"><span data-stu-id="88de5-129">![Snooper 2013 call flow diagram.](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Snooper 2013 call flow diagram.")</span></span>

<span data-ttu-id="88de5-130">ダイアグラムビューの上にマウスポインターを移動すると、メッセージや、フローとメッセージの内容、およびサーバー要素に関する詳細情報を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="88de5-130">You can hover over the diagram view and get details about the messages and content of the flows and messages as well as the server elements.</span></span> <span data-ttu-id="88de5-131">いずれかの通話フローの矢印をクリックして、[メッセージ] ビューのメッセージに移動します。</span><span class="sxs-lookup"><span data-stu-id="88de5-131">Click on any call flow arrow to go to the message in the Messages view.</span></span>

<span data-ttu-id="88de5-132">![コールフロー図のメッセージの詳細。](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "コールフロー図のメッセージの詳細。")</span><span class="sxs-lookup"><span data-stu-id="88de5-132">![Call flow diagram message details.](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "Call flow diagram message details.")</span></span>

<div>

## <a name="to-open-a-log-file-in-snooper"></a><span data-ttu-id="88de5-133">Snooper でログ ファイルを開くには</span><span class="sxs-lookup"><span data-stu-id="88de5-133">To open a log file in Snooper</span></span>

1.  <span data-ttu-id="88de5-p106">Snooper を使用してログ ファイルを開くためには、ログ ファイルへの読み取りアクセス権が必要です。Snooper を使用してログ ファイルにアクセスするためには、役割ベースのアクセス制御 (RBAC) のセキュリティ グループである CsAdministrator または CsServerAdministrator のメンバーであるか、これらの 2 つのグループのいずれかを含むカスタムの RBAC の役割のメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-p106">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files you must be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="88de5-136">Lync Server デバッグツール (LyncDebugTools.msi) をインストールした後、Windows エクスプローラーまたはコマンドラインを使用して、ディレクトリを Snooper.exe の場所に変更します。</span><span class="sxs-lookup"><span data-stu-id="88de5-136">After the installation of the Lync Server Debugging Tools (LyncDebugTools.msi), change directory to the location of Snooper.exe using Windows Explorer or from the command line.</span></span> <span data-ttu-id="88de5-137">既定では、デバッグツールは C: \\ Program Files \\ Microsoft Lync Server 2013 デバッグツールに含まれてい \\ ます。</span><span class="sxs-lookup"><span data-stu-id="88de5-137">By default, the debugging tools are located in C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="88de5-138">Snooper.exe をダブルクリックするか、実行します。</span><span class="sxs-lookup"><span data-stu-id="88de5-138">Double-click or run Snooper.exe.</span></span>

3.  <span data-ttu-id="88de5-139">Snooper を開いたら、[**ファイル**] を右クリックして [**OpenFile**] をクリックします。ログ ファイルを探し、[**開く**] ダイアログ ボックスでファイルを選択して [**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-139">After Snooper is open, right-click **File**, click **OpenFile**, find your log files, select a file in the **Open** dialog box, and then click **Open**.</span></span>

4.  <span data-ttu-id="88de5-140">ログ ファイルの **トレース** メッセージは、[**トレース**] タブに表示されます。収集されたトレースのメッセージの内容を表示するには、[**メッセージ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-140">The log file’s **Trace** messages are displayed on the **Trace** tab. Click the **Messages** tab to view the message contents of the collected traces.</span></span>

</div>

<div>

## <a name="to-display-a-call-flow-diagram"></a><span data-ttu-id="88de5-141">通話フロー図を表示するには</span><span class="sxs-lookup"><span data-stu-id="88de5-141">To display a call flow diagram</span></span>

1.  <span data-ttu-id="88de5-p108">Snooper を使用してログ ファイルを開くためには、ログ ファイルへの読み取りアクセス権が必要です。Snooper を使用してログ ファイルにアクセスするためには、役割ベースのアクセス制御 (RBAC) のセキュリティ グループである CsAdministrator または CsServerAdministrator のメンバーであるか、これらの 2 つのグループのいずれかを含むカスタムの RBAC の役割のメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-p108">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files, you need to be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="88de5-144">ログ ファイルを開いて [**メッセージ**] タブをクリックし、メッセージ ビューで会話を選択するか、[**トレース**] タブでトレース コンポーネントを選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-144">Open a log file and click the **Messages** tab, select a conversation in the messages view or select a trace component on the **Trace** tab.</span></span>

3.  <span data-ttu-id="88de5-145">[**通話フロー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-145">Click **Call Flow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88de5-p109">通話フローに含まれていないメッセージまたはトレースをクリックした場合、図は表示されず、Snooper の最下部に "This message is not eligible for callfow" (このメッセージは通話フローの対象ではありません) というステータス メッセージが表示されます。別のメッセージまたはトレースを選択すると、そのメッセージまたはトレースが通話フローに含まれている場合は通話フローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-p109">If you click on a message or trace that is not part of a call flow, the diagram will not appear and a status message appears at the bottom of Snooper stating “This message is not eligible for callfow”. Choose another message or trace and the call flow will appear if the message or trace is part of a call flow.</span></span>

    
    </div>

4.  <span data-ttu-id="88de5-148">メッセージ間またはトレース線を移動して、通話フロー図が更新されるか変化して、新しい図が表示されるかどうかに注目してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-148">Move through the Messages or the Trace lines and note whether the call flow diagram updates or changes to display a new diagram.</span></span>

5.  <span data-ttu-id="88de5-149">要素にマウスをポイントすると、通話メッセージ、エンドポイント、その他のコンポーネントに関する情報を表示されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-149">Hover over elements to get information about call messages, endpoints, and other components.</span></span>

<span data-ttu-id="88de5-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88de5-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

