---
title: 'Lync Server 2013: 資格情報認証を使用するようにウォッチャーノードを構成する'
description: 'Lync Server 2013: 資格情報認証を使用するようにウォッチャーノードを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to use credential authentication
ms:assetid: 032e33f3-9483-42e6-a33c-347eb6779597
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204632(v=OCS.15)
ms:contentKeyID: 48183255
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b65d4e3f90b27aac69b8569472ac9896766e093e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433445"
---
# <a name="configuring-a-watcher-node-to-use-credential-authentication-in-lync-server-2013"></a><span data-ttu-id="3002e-103">Lync Server 2013 での資格情報認証を使用するためのウォッチャーノードの構成</span><span class="sxs-lookup"><span data-stu-id="3002e-103">Configuring a watcher node to use credential authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3002e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3002e-104">

<span> </span></span></span>

<span data-ttu-id="3002e-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="3002e-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="3002e-106">ウォッチャーノードのコンピューターが境界ネットワークの外側にある場合は、別の手順に従って、そのウォッチャーノードが代理トランザクションを実行するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3002e-106">If your watcher node computer lies outside the perimeter network, then you must follow a slightly different procedure in order to configure that watcher node to run synthetic transactions.</span></span> <span data-ttu-id="3002e-107">具体的には、信頼されたアプリケーションプールと信頼されたアプリケーションを作成しないようにする必要があります。また、監視ノードが、境界ネットワーク内のコンピューターに通知を送信できるようにする証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3002e-107">Specifically, you should not create a trusted application pool and a trusted application, and you must install a certificate that enables the watcher node to send alerts to a computer inside the perimeter network.</span></span> <span data-ttu-id="3002e-108">これは、次の2つの個別のタスクを完了する必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="3002e-108">This means that you will need to complete two separate tasks:</span></span>

  - <span data-ttu-id="3002e-109">コンピューターの RTC ローカルの読み取り専用管理者グループのメンバーシップを更新する</span><span class="sxs-lookup"><span data-stu-id="3002e-109">Update the membership in the computer's RTC Local Read-only Administrators Group</span></span>

  - <span data-ttu-id="3002e-110">ウォッチャーノード構成ファイルをインストールする</span><span class="sxs-lookup"><span data-stu-id="3002e-110">Install the watcher node configuration files</span></span>

<div>

## <a name="updating-membership-in-the-rtc-local-read-only-administrators-group"></a><span data-ttu-id="3002e-111">RTC ローカル Read-Only 管理者グループのメンバーシップを更新しています</span><span class="sxs-lookup"><span data-stu-id="3002e-111">Updating Membership in the RTC Local Read-Only Administrators Group</span></span>

<span data-ttu-id="3002e-112">ウォッチャーノードが境界ネットワークの外側にある場合は、ネットワークサービスアカウントを、ウォッチャーノードコンピューターの RTC ローカルの読み取り専用管理者グループに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3002e-112">If your watcher node lies outside the perimeter network, you must add the Network Service account to the RTC Local Read-only Administrators group on the watcher node computer.</span></span> <span data-ttu-id="3002e-113">これを行うには、ウォッチャーノードで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3002e-113">To do this, complete the following procedure on the watcher node:</span></span>

1.  <span data-ttu-id="3002e-114">[ **スタート**] をクリックし、[ **コンピューター**] を右クリックして、[ **管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-114">Click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="3002e-115">サーバーマネージャーで、[ **構成**] を展開し、[ **ローカルユーザーとグループ**] を展開して、[ **グループ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-115">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="3002e-116">[グループ] ウィンドウで、[ **RTC ローカル読み取り専用管理者**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-116">In the Groups pane, double-click **RTC Local Read-only Administrators**.</span></span>

4.  <span data-ttu-id="3002e-117">[ **RTC のローカルの読み取り専用管理者のプロパティ** ] ダイアログボックスで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-117">In the **RTC Local Read-only Administrators Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="3002e-118">[ **ユーザー、コンピューター、サービスアカウント、またはグループの選択** ] ダイアログボックスで、[ **場所**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-118">In the **Select Users, Computers, Service Accounts, or Groups** dialog box, click **Locations**.</span></span>

6.  <span data-ttu-id="3002e-119">[ **場所** ] ダイアログボックスで、ウォッチャーノードのコンピューターの名前を選び、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-119">In the **Locations** dialog box, select the name of the watcher node computer, and then click **OK**.</span></span>

7.  <span data-ttu-id="3002e-120">[ **選択するオブジェクト名を入力してください** ] ボックスに「 **ネットワークサービス**」と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-120">In the **Enter object names to select** box, type **Network Service**, and then click **OK**.</span></span>

8.  <span data-ttu-id="3002e-121">[ **RTC のローカルの読み取り専用管理者のプロパティ** ] ダイアログボックスで、[ **OK**] をクリックし、[ **サーバーマネージャー**] を閉じます。</span><span class="sxs-lookup"><span data-stu-id="3002e-121">In the **RTC Local Read-only Administrators Properties** dialog box, click **OK**, and then close **Server Manager**.</span></span>

<span data-ttu-id="3002e-122">監視ノード コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="3002e-122">Restart the watcher node computer.</span></span>

</div>

<div>

## <a name="installing-the-watcher-node-configuration-files"></a><span data-ttu-id="3002e-123">ウォッチャーノード構成ファイルのインストール</span><span class="sxs-lookup"><span data-stu-id="3002e-123">Installing the Watcher Node Configuration Files</span></span>

<span data-ttu-id="3002e-124">ウォッチャーノードのコンピューターが再起動したら、次の手順として、ファイル Watchernode.msi を実行します。</span><span class="sxs-lookup"><span data-stu-id="3002e-124">After the watcher node computer has restarted, your next step is to run the file Watchernode.msi.</span></span> <span data-ttu-id="3002e-125">このファイルを実行するには、[ **スタート**]、[ **すべてのプログラム**]、[ **lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックして、lync server 2013 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3002e-125">To run this file, open the Lync Server 2013 Management Shell by clicking **Start**, clicking **All Programs**, clicking **Lync Server 2013**, and then clicking **Lync Server Management Shell**.</span></span> <span data-ttu-id="3002e-126">Lync Server 管理シェルで、次のコマンドを入力し、enter キーを押します (必ず、Watchernode.msi のコピーの実際のパスを指定してください)。</span><span class="sxs-lookup"><span data-stu-id="3002e-126">In the Lync Server Management Shell, type the following command and then press ENTER (be sure and specify the actual path to your copy of Watchernode.msi):</span></span>

    C:\Tools\Watchernode.msi Authentication=Negotiate

<div>


> [!NOTE]  
> <span data-ttu-id="3002e-127">前に説明したように、Watchernode.msi はコマンドウィンドウから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="3002e-127">As noted previously, Watchernode.msi can also be run from a command window.</span></span> <span data-ttu-id="3002e-128">コマンド ウィンドウを開くには、[<STRONG>スタート</STRONG>] メニューをクリックし、[<STRONG>コマンド プロンプト</STRONG>] を右クリックして、[<STRONG>管理者として実行</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3002e-128">To open a command window, click <STRONG>Start</STRONG>, right-click <STRONG>Command Prompt</STRONG>, and then click <STRONG>Run as administrator</STRONG>.</span></span> <span data-ttu-id="3002e-129">コマンドウィンドウが開いたら、前に示したのと同じコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="3002e-129">When the command window opens, type the same command as shown earlier.</span></span>



</div>

<span data-ttu-id="3002e-p105">監視ノードを信頼されたアプリケーション プールとしてセットアップできない場合はいつでも、ネゴシエート モードが使用されます。このモードでは、管理者が監視ノードのテスト ユーザー パスワードを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3002e-p105">The Negotiate mode is used any time the watcher node cannot be set up as a trusted application pool. In this mode, administrators will need to manage test user passwords on the watcher node.</span></span>

<span data-ttu-id="3002e-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3002e-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

