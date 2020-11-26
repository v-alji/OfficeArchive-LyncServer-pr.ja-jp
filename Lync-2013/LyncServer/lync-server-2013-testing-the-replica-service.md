---
title: 'Lync Server 2013: レプリカサービスをテストする'
description: 'Lync Server 2013: レプリカサービスをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440977"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a><span data-ttu-id="7855f-103">Lync Server 2013 でのレプリカサービスのテスト</span><span class="sxs-lookup"><span data-stu-id="7855f-103">Testing the replica service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7855f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7855f-104">

<span> </span></span></span>

<span data-ttu-id="7855f-105">_**最終更新日:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="7855f-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7855f-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="7855f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7855f-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="7855f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7855f-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="7855f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7855f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7855f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7855f-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="7855f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7855f-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="7855f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="7855f-112">Windows PowerShell のリモートインスタンスを使用して実行する場合、ユーザーには、 <strong>CsReplica</strong> コマンドレットを実行するためのアクセス許可が与えられた RBAC の役割を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7855f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsReplica</strong> cmdlet.</span></span> <span data-ttu-id="7855f-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7855f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7855f-114">説明</span><span class="sxs-lookup"><span data-stu-id="7855f-114">Description</span></span>

<span data-ttu-id="7855f-115">**Test CsReplica** コマンドレットは、Lync Server 2013 レプリカサービスがローカルコンピューターで実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7855f-115">The **Test-CsReplica** cmdlet verifies that the Lync Server 2013 replica service is running on the local computer.</span></span> <span data-ttu-id="7855f-116">**Test CsReplica** コマンドレットは、次のようなタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="7855f-116">The **Test-CsReplica** cmdlet performs such tasks as:</span></span>

  - <span data-ttu-id="7855f-117">レプリケーターエージェントと集中ログエージェントサービスの状態を確認する</span><span class="sxs-lookup"><span data-stu-id="7855f-117">checking the status of the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="7855f-118">必要なポートが Windows ファイアウォールで開かれていることを確認する</span><span class="sxs-lookup"><span data-stu-id="7855f-118">verifying that the required ports were opened in the Windows Firewall</span></span>

  - <span data-ttu-id="7855f-119">必要な Active Directory とローカルコンピューターのセキュリティグループが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7855f-119">making sure that the necessary Active Directory and local computer security groups exist.</span></span>

<span data-ttu-id="7855f-120">このコマンドレットはローカルで実行する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7855f-120">Note that this cmdlet must be run locally.</span></span> <span data-ttu-id="7855f-121">つまり、レプリカサービスが実行されているコンピューターで実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7855f-121">That is, it must be run on the same computer where the replica service is running.</span></span> <span data-ttu-id="7855f-122">リモートサーバーに対してテスト用の **CsReplica** コマンドレットを実行するためのオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="7855f-122">There are no options for running the **Test-CsReplica** cmdlet against a remote server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7855f-123">テストの実行</span><span class="sxs-lookup"><span data-stu-id="7855f-123">Running the test</span></span>

<span data-ttu-id="7855f-124">例1に示すコマンドは、ローカルコンピューターの Lync Server 2013 レプリカサービスをテストします。</span><span class="sxs-lookup"><span data-stu-id="7855f-124">The command shown in Example 1 tests the Lync Server 2013 replica service on the local computer.</span></span> <span data-ttu-id="7855f-125">この例では、Verbose パラメーターを使用して、テストの最終的なエラー、テストの成否、テストによって生成されたレポートの場所など、テストに関する情報が画面に表示されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="7855f-125">In this example the Verbose parameter is used to guarantee that information about the test – including the eventual failure or success of the test and the location of the report generated by the test – is displayed on screen.</span></span>

    Test-CsReplica -Verbose

<span data-ttu-id="7855f-126">例2は、例1で示したコマンドの変形です。</span><span class="sxs-lookup"><span data-stu-id="7855f-126">Example 2 is a variation of the command shown in Example 1.</span></span> <span data-ttu-id="7855f-127">この場合、レポートパラメーターは、テストによって生成されたレポートのフォルダーパスと名前を指定するために含まれています。</span><span class="sxs-lookup"><span data-stu-id="7855f-127">In this case, the Report parameter is included to specify a folder path and name for the report generated by the test.</span></span> <span data-ttu-id="7855f-128">レポートパスを指定しない場合、次のような自動生成名がレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7855f-128">If you do not specify a report path the report will be given an auto-generated name similar to this:</span></span>

<span data-ttu-id="7855f-129">C: \\ \\ Litwareinc \\ AppData \\ ローカル \\ Temp \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span><span class="sxs-lookup"><span data-stu-id="7855f-129">C:\\Users\\Administrator.Litwareinc\\AppData\\Local\\Temp\\1\\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span></span>

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7855f-130">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="7855f-130">Determining success or failure</span></span>

<span data-ttu-id="7855f-131">セクションの本文をここに挿入します。</span><span class="sxs-lookup"><span data-stu-id="7855f-131">Insert section body here.</span></span>

<span data-ttu-id="7855f-132">冗長: 新しいログファイルの作成 "C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ Temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしています。</span><span class="sxs-lookup"><span data-stu-id="7855f-132">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="7855f-133">冗長: 新しいログファイルの作成 "C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ Temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしています。</span><span class="sxs-lookup"><span data-stu-id="7855f-133">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="7855f-134">VERBOSE: "Test-CsReplica" 処理は正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="7855f-134">VERBOSE: "Test-CsReplica" processing has completed successfully.</span></span>

<span data-ttu-id="7855f-135">詳細: 詳細な結果は、"C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ 一時 \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしている" という説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7855f-135">VERBOSE: Detailed results can be found at "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="7855f-136">VERBOSE: 新しいログファイルを作成しています</span><span class="sxs-lookup"><span data-stu-id="7855f-136">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="7855f-137">"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="7855f-137">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="7855f-138">d3bd0e4a083.xml] を選びます。</span><span class="sxs-lookup"><span data-stu-id="7855f-138">d3bd0e4a083.xml".</span></span>

<span data-ttu-id="7855f-139">VERBOSE: 新しいログファイルを作成しています</span><span class="sxs-lookup"><span data-stu-id="7855f-139">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="7855f-140">"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="7855f-140">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="7855f-141">d3bd0e4a083.html "。</span><span class="sxs-lookup"><span data-stu-id="7855f-141">d3bd0e4a083.html".</span></span>

<span data-ttu-id="7855f-142">警告: Test-CsReplica に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="7855f-142">WARNING: Test-CsReplica failed.</span></span>

<span data-ttu-id="7855f-143">警告: 詳細な結果は次のページでご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="7855f-143">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="7855f-144">"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="7855f-144">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="7855f-145">d3bd0e4a083.html "。</span><span class="sxs-lookup"><span data-stu-id="7855f-145">d3bd0e4a083.html".</span></span>

<span data-ttu-id="7855f-146">Test-CsReplica: コマンドの実行に失敗しました。要求されたレジストリアクセスがありません</span><span class="sxs-lookup"><span data-stu-id="7855f-146">Test-CsReplica : Command execution failed: Requested registry access is not</span></span>

<span data-ttu-id="7855f-147">禁止.</span><span class="sxs-lookup"><span data-stu-id="7855f-147">allowed.</span></span>

<span data-ttu-id="7855f-148">行: 1 char: 1</span><span class="sxs-lookup"><span data-stu-id="7855f-148">At line:1 char:1</span></span>

<span data-ttu-id="7855f-149">\+ Test-CsReplica-Verbose</span><span class="sxs-lookup"><span data-stu-id="7855f-149">\+ Test-CsReplica -Verbose</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="7855f-150">\+ カテゴリ情報: InvalidOperation: (:) \[テスト-CsReplica \] 、セキュリティ</span><span class="sxs-lookup"><span data-stu-id="7855f-150">\+ CategoryInfo : InvalidOperation: (:) \[Test-CsReplica\], Security</span></span>

<span data-ttu-id="7855f-151">エラー</span><span class="sxs-lookup"><span data-stu-id="7855f-151">Exception</span></span>

<span data-ttu-id="7855f-152">\+ FullyQualifiedErrorId: ProcessingFailed、Microsoft Rtc. .Deploy</span><span class="sxs-lookup"><span data-stu-id="7855f-152">\+ FullyQualifiedErrorId : ProcessingFailed,Microsoft.Rtc.Management.Deploy</span></span>

<span data-ttu-id="7855f-153">予約.TestReplicaCmdlet</span><span class="sxs-lookup"><span data-stu-id="7855f-153">ment.TestReplicaCmdlet</span></span>

<span data-ttu-id="7855f-154">PS C: \\ ユーザーの \\ テスト\></span><span class="sxs-lookup"><span data-stu-id="7855f-154">PS C:\\Users\\Testing\></span></span>

<span data-ttu-id="7855f-155">PS C: \\ \\ \> Test-CsUcwaConference-Targetfqdn "LyncTest" をテストする</span><span class="sxs-lookup"><span data-stu-id="7855f-155">PS C:\\Users\\Testing\> Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.M</span></span>

<span data-ttu-id="7855f-156">icrosoft.com "</span><span class="sxs-lookup"><span data-stu-id="7855f-156">icrosoft.com"</span></span>

<span data-ttu-id="7855f-157">警告: 指定した完全修飾のレジストラーポート番号の読み取りに失敗しました</span><span class="sxs-lookup"><span data-stu-id="7855f-157">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="7855f-158">ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="7855f-158">domain name (FQDN).</span></span> <span data-ttu-id="7855f-159">既定のレジストラーポート番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="7855f-159">Using default Registrar port number.</span></span> <span data-ttu-id="7855f-160">エラー</span><span class="sxs-lookup"><span data-stu-id="7855f-160">Exception:</span></span>

<span data-ttu-id="7855f-161">InvalidOperationException: トポロジで一致するクラスターが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="7855f-161">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="7855f-162">自宅</span><span class="sxs-lookup"><span data-stu-id="7855f-162">at</span></span>

<span data-ttu-id="7855f-163">SipSyntheticTransaction-TryRetri の同期を行います。</span><span class="sxs-lookup"><span data-stu-id="7855f-163">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="7855f-164">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="7855f-164">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="7855f-165">Test-CsUcwaConference: 割り当てられているテストユーザーはありません</span><span class="sxs-lookup"><span data-stu-id="7855f-165">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="7855f-166">\[LyncTest.SelfHost.Corp.Microsoft.com \] 。</span><span class="sxs-lookup"><span data-stu-id="7855f-166">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="7855f-167">テストユーザー構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="7855f-167">Verify test user configuration.</span></span>

<span data-ttu-id="7855f-168">行: 1 char: 1</span><span class="sxs-lookup"><span data-stu-id="7855f-168">At line:1 char:1</span></span>

<span data-ttu-id="7855f-169">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="7855f-169">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="7855f-170">\+ カテゴリ情報: ResourceUnavailable 使用できません: (:) \[テスト-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="7855f-170">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="7855f-171">、InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="7855f-171">, InvalidOperationException</span></span>

<span data-ttu-id="7855f-172">\+ FullyQualifiedErrorId: Notん Testusers、Microsoft Rtc。</span><span class="sxs-lookup"><span data-stu-id="7855f-172">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="7855f-173">TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="7855f-173">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7855f-174">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="7855f-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="7855f-175">次に **、テスト用のレプリカ** が機能しない場合の一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="7855f-175">Here are some common reasons why **Test-CsReplica** might fail:</span></span>

  - <span data-ttu-id="7855f-176">レプリケーターエージェントと集中ログエージェントサービスで、大きな問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="7855f-176">There may be a larger problem with the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="7855f-177">必要なポートが Windows ファイアウォールで開かれていない可能性がある</span><span class="sxs-lookup"><span data-stu-id="7855f-177">The required ports may not be open in the Windows Firewall</span></span>

  - <span data-ttu-id="7855f-178">必要な Active Directory とローカルコンピューターのセキュリティグループが存在しない可能性があります</span><span class="sxs-lookup"><span data-stu-id="7855f-178">The necessary Active Directory and local computer security groups may not exist</span></span>

<span data-ttu-id="7855f-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7855f-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

