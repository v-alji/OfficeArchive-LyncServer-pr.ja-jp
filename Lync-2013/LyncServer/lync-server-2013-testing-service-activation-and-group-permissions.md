---
title: 'Lync Server 2013: サービスのアクティブ化とグループのアクセス許可をテストする'
description: 'Lync Server 2013: サービスのアクティブ化とグループのアクセス許可をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440984"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="d3c27-103">Lync Server 2013 でのサービスのアクティブ化とグループのアクセス許可のテスト</span><span class="sxs-lookup"><span data-stu-id="d3c27-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3c27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3c27-104">

<span> </span></span></span>

<span data-ttu-id="d3c27-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="d3c27-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3c27-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="d3c27-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d3c27-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="d3c27-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3c27-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="d3c27-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d3c27-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d3c27-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c27-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="d3c27-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d3c27-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3c27-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d3c27-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsTopology コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3c27-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="d3c27-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3c27-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d3c27-114">説明</span><span class="sxs-lookup"><span data-stu-id="d3c27-114">Description</span></span>

<span data-ttu-id="d3c27-115">Test-CsTopology コマンドレットを使用すると、Lync Server 2013 がグローバルスコープで正常に機能しているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="d3c27-116">既定では、コマンドレットは Lync Server インフラストラクチャ全体をチェックし、必要なサービスが実行されていること、およびこれらのサービスに適切な権限が設定されていること、および Lync Server のインストール時に作成されたユニバーサルセキュリティグループに対して適切な権限が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3c27-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="d3c27-117">Lync Server のインストールの有効性を確認するだけでなく、Test-CsTopology 特定のサービスの有効性を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="d3c27-118">たとえば、次のコマンドは、プール atl-cs-001.litwareinc.com で A/V 会議サーバーの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="d3c27-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d3c27-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="d3c27-119">Running the test</span></span>

<span data-ttu-id="d3c27-120">既定では、画面に表示される出力はほとんどありません。 Test-CsTopology ます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="d3c27-121">代わりに、コマンドレットによって返される情報は、HTML ファイルに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="d3c27-122">Report パラメーターを使用すると、テスト用に生成された HTML ファイルのファイルパスとファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="d3c27-123">レポートパラメーターを指定しない場合、HTML ファイルは [ユーザー] フォルダーに自動的に保存され、次のような名前が付けられます (ce84964a-c4da-4622-ad34-c54ff3ed361f.html)。</span><span class="sxs-lookup"><span data-stu-id="d3c27-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="d3c27-124">次のサンプルコマンドは Test-CsTopology を実行し、C: LogsComputerTest.html という名前のファイルに出力を保存し \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="d3c27-125">詳細については、「 [テスト-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) ツールレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3c27-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d3c27-126">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="d3c27-126">Determining success or failure</span></span>

<span data-ttu-id="d3c27-127">ほとんどのテストコマンドレットとは異なり、Test-CsTopology はバックの成功または失敗を報告します。</span><span class="sxs-lookup"><span data-stu-id="d3c27-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="d3c27-128">一部では、コマンドレットが実行されるたびに実行する必要がある多数の確認チェックが行われるためです。</span><span class="sxs-lookup"><span data-stu-id="d3c27-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="d3c27-129">代わりに、Internet Explorer を使用して表示できる HTML レポートにデータが保存されます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d3c27-130">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="d3c27-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="d3c27-131">Test-CsTopology が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d3c27-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="d3c27-132">テストコンピューターのレプリケーションは最新ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d3c27-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="d3c27-133">Get-CsManagementStoreReplicationStatus コマンドレットを実行して、コンピューターの現在のレプリケーションの状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="d3c27-134">レプリケーションの状態が最新でない場合は、次のようなコマンドを使用して、手動でレプリケーションを強制的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="d3c27-135">トポロジを有効にする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3c27-135">The topology might have to be enabled.</span></span> <span data-ttu-id="d3c27-136">Lync Server のトポロジ (ローカルコンピューターに影響を与える可能性のある変更) を変更する場合は、新しいトポロジを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3c27-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="d3c27-137">このコマンドを実行すると、いつでもトポロジーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3c27-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="d3c27-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3c27-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

