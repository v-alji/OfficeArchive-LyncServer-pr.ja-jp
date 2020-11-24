---
title: 'Lync Server 2013: Lync Server サービスのテスト'
description: 'Lync Server 2013: Lync Server サービスのテスト'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Server services
ms:assetid: b564b450-a746-4ec9-aabb-e076309ccd5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689119(v=OCS.15)
ms:contentKeyID: 63969644
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f04cf5e0c098c671b6fb126d4607f3cdba107712
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398936"
---
# <a name="testing-lync-server-services-in-lync-server-2013"></a><span data-ttu-id="58760-103">Lync server 2013 での Lync Server サービスのテスト</span><span class="sxs-lookup"><span data-stu-id="58760-103">Testing Lync Server services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58760-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58760-104">

<span> </span></span></span>

<span data-ttu-id="58760-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="58760-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58760-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="58760-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="58760-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="58760-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58760-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="58760-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="58760-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="58760-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58760-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="58760-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="58760-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="58760-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="58760-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsComputer コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="58760-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsComputer cmdlet.</span></span> <span data-ttu-id="58760-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="58760-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsComputer&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="58760-114">説明</span><span class="sxs-lookup"><span data-stu-id="58760-114">Description</span></span>

<span data-ttu-id="58760-115">Test-CsComputer は、ローカルコンピューターで実行されているすべての Lync Server 2013 サービスの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="58760-115">Test-CsComputer verifies the status of all the Lync Server 2013 services that are running on the local computer.</span></span> <span data-ttu-id="58760-116">(Test-CsComputer はローカルでのみ実行できます。 Windows PowerShell のリモートインスタンスから実行することはできません)。このコマンドレットは、コンピューター上で適切なファイアウォールポートが開かれているかどうかを確認し、Lync Server 2013 のインストール時に作成された Active Directory グループが、対応するローカルグループに追加されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="58760-116">(Test-CsComputer can only be run locally, it cannot be run from a remote instance of Windows PowerShell.) The cmdlet also checks whether the appropriate firewall ports are opened on the computer, and determines whether the Active Directory groups that were created when you installed Lync Server 2013 were added to the corresponding local groups.</span></span> <span data-ttu-id="58760-117">たとえば、Test-CsComputer は、[Active Directory グループ RTCUniversalUserAdmins が管理者グループに追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="58760-117">For example, Test-CsComputer will verify that the Active Directory group RTCUniversalUserAdmins was added to the Administrators group.</span></span>

<span data-ttu-id="58760-118">詳細については、「 [CsComputer のテスト](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) 」コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58760-118">For more information, see the Help documentation for the [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="58760-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="58760-119">Running the test</span></span>

<span data-ttu-id="58760-120">Test-CsComputer コマンドレットはローカルコンピューターでのみ実行できます。 Windows PowerShell のリモートインスタンスから Test-CsComputer を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="58760-120">The Test-CsComputer cmdlet can only be run on the local computer, you can't call Test-CsComputer from a remote instance of Windows PowerShell.</span></span> <span data-ttu-id="58760-121">既定では、コマンドレットによって返される情報は HTML ファイルに書き込まれるので、画面上に表示されている出力はほとんどありません。 Test-CsComputer。</span><span class="sxs-lookup"><span data-stu-id="58760-121">By default, Test-CsComputer displays very little output on-screen, instead information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="58760-122">このため、テスト用のコンピューターを実行するときは、必ず Verbose パラメーターと Report パラメーターを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="58760-122">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsComputer.</span></span> <span data-ttu-id="58760-123">Verbose パラメーターは、コマンドレットが実行されている間、画面上により詳細な出力を提供します。</span><span class="sxs-lookup"><span data-stu-id="58760-123">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="58760-124">レポートパラメーターを使用すると、CsComputer によって生成された HTML ファイルのファイルパスとファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="58760-124">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsComputer.</span></span> <span data-ttu-id="58760-125">レポートパラメーターを指定しない場合、HTML ファイルは [ユーザー] フォルダーに自動的に保存され、次のような名前が付けられます (ce84964a-c4da-4622-ad34-c54ff3ed361f.html)。</span><span class="sxs-lookup"><span data-stu-id="58760-125">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="58760-126">次のサンプルコマンドは Test-CsComputer を実行し、C: LogsComputerTest.html という名前のファイルに出力を保存し \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="58760-126">The following sample command runs Test-CsComputer and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsComputer -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="58760-127">詳細については、「 [CsComputer のテスト](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) 」コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58760-127">For more information, see the Help documentation for the [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="58760-128">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="58760-128">Determining success or failure</span></span>

<span data-ttu-id="58760-129">テストによって実行される確認チェックの数が原因で、Test-CsComputer は、単純な Yes を報告しません。 **テストに成功** したか、 **いいえ、テストは失敗** します。</span><span class="sxs-lookup"><span data-stu-id="58760-129">Because of the number of verification checks that it performs, Test-CsComputer does not report back a simple **Yes, the test succeeded** or **No, the test failed**.</span></span> <span data-ttu-id="58760-130">代わりに、生成された HTML ファイルを Internet Explorer を使って表示し、各テストの成功または失敗を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58760-130">Instead, you have to view the generated HTML file by using Internet Explorer to determine the success or failure of each test.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="58760-131">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="58760-131">Reasons why the test might have failed</span></span>

<span data-ttu-id="58760-132">Test-CsComputer が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="58760-132">Here are some common reasons why Test-CsComputer might fail:</span></span>

  - <span data-ttu-id="58760-133">テストコンピューターが Lync Server で使用できるようになっていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58760-133">The test computer might not be enabled for use with Lync Server.</span></span> <span data-ttu-id="58760-134">この問題は、コンピューター上の Lync Server サービスまたはサーバーの役割が変更され、Enable-CsComputer コマンドレットが実行されなかった場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58760-134">This can occur if the Lync Server services or server roles on the computer have changed and the Enable-CsComputer cmdlet was not run.</span></span> <span data-ttu-id="58760-135">この問題を解決するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="58760-135">To resolve this issue, run the following command:</span></span>
    
        Enable-CsComputer

  - <span data-ttu-id="58760-136">テストコンピューターのレプリケーションが最新ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58760-136">Replication might not be up to date on the test computer.</span></span> <span data-ttu-id="58760-137">Get-CsManagementStoreReplicationStatus コマンドレットを実行して、コンピューターの現在のレプリケーションの状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="58760-137">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="58760-138">レプリケーションの状態が最新でない場合は、次のようなコマンドを使用して、手動でレプリケーションを強制的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="58760-138">If the replication status is not up to date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="58760-139">トポロジを有効にする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="58760-139">The topology might have to be enabled.</span></span> <span data-ttu-id="58760-140">Lync Server のトポロジ (ローカルコンピューターに影響を与える可能性のある変更) を変更する場合は、新しいトポロジを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="58760-140">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="58760-141">このコマンドを実行すると、いつでもトポロジーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="58760-141">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="58760-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58760-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

