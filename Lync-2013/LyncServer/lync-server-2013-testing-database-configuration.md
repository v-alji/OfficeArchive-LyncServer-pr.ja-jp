---
title: 'Lync Server 2013: データベース構成のテスト'
description: 'Lync Server 2013: データベース構成をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441040"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="49628-103">Lync Server 2013 でのデータベース構成のテスト</span><span class="sxs-lookup"><span data-stu-id="49628-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49628-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49628-104">

<span> </span></span></span>

<span data-ttu-id="49628-105">_**最終更新日:** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="49628-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49628-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="49628-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="49628-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="49628-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49628-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="49628-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="49628-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="49628-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49628-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="49628-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="49628-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーであり、SQL Server の管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49628-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="49628-112">Windows PowerShell のリモートインスタンスを使って実行する場合、ユーザーには、 <strong>テスト用のデータベース</strong> コマンドレットを実行する権限を持つ RBAC の役割を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="49628-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="49628-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="49628-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="49628-114">説明</span><span class="sxs-lookup"><span data-stu-id="49628-114">Description</span></span>

<span data-ttu-id="49628-115">**テスト用のデータベース** コマンドレットは、1つ以上の Lync Server 2013 データベースへの接続を確認します。</span><span class="sxs-lookup"><span data-stu-id="49628-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="49628-116">**テスト用のデータベース** コマンドレットを実行すると、Lync Server トポロジを読み取り、関連データベースに接続しようとし、各試行の成功または失敗を報告します。</span><span class="sxs-lookup"><span data-stu-id="49628-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="49628-117">接続できる場合は、コマンドレットによって、データベース名、SQL Server のバージョン情報、インストールされているミラーデータベースの場所などの情報も報告されます。</span><span class="sxs-lookup"><span data-stu-id="49628-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="49628-118">テストの実行</span><span class="sxs-lookup"><span data-stu-id="49628-118">Running the test</span></span>

<span data-ttu-id="49628-119">例1に示すコマンドは、サーバーの全体管理データベースの構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="49628-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="49628-120">使用例 2: コンピューター atl-sql-001.litwareinc.com にインストールされているすべての Lync Server データベースを確認します。</span><span class="sxs-lookup"><span data-stu-id="49628-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="49628-121">例3では、コンピューター atl-sql-001.litwareinc.com にインストールされているアーカイブデータベースに対してのみ確認が行われます。</span><span class="sxs-lookup"><span data-stu-id="49628-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="49628-122">SqlInstanceName パラメーターは、アーカイブデータベースが配置されている SQL Server インスタンス (アーキテクチャ) を指定するために含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="49628-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="49628-123">例4に示すコマンドは、ローカルコンピューターにインストールされているデータベースを確認します。</span><span class="sxs-lookup"><span data-stu-id="49628-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="49628-124">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="49628-124">Determining success or failure</span></span>

<span data-ttu-id="49628-125">データベース接続が適切に構成されている場合は、次のような出力が返されます。これは、成功プロパティが **True** とマークされていることになります。</span><span class="sxs-lookup"><span data-stu-id="49628-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="49628-126">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="49628-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="49628-127">SqlInstanceName: rtc</span><span class="sxs-lookup"><span data-stu-id="49628-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="49628-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="49628-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="49628-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="49628-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="49628-130">DatabaseName: xds</span><span class="sxs-lookup"><span data-stu-id="49628-130">DatabaseName : xds</span></span>

<span data-ttu-id="49628-131">データソース</span><span class="sxs-lookup"><span data-stu-id="49628-131">DataSource :</span></span>

<span data-ttu-id="49628-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="49628-132">SQLServerVersion :</span></span>

<span data-ttu-id="49628-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="49628-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="49628-134">バージョン:</span><span class="sxs-lookup"><span data-stu-id="49628-134">InstalledVersion :</span></span>

<span data-ttu-id="49628-135">成功: True</span><span class="sxs-lookup"><span data-stu-id="49628-135">Succeed : True</span></span>

<span data-ttu-id="49628-136">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="49628-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="49628-137">SqlInstanceName: rtc</span><span class="sxs-lookup"><span data-stu-id="49628-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="49628-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="49628-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="49628-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="49628-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="49628-140">DatabaseName: lis</span><span class="sxs-lookup"><span data-stu-id="49628-140">DatabaseName : lis</span></span>

<span data-ttu-id="49628-141">データソース</span><span class="sxs-lookup"><span data-stu-id="49628-141">DataSource :</span></span>

<span data-ttu-id="49628-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="49628-142">SQLServerVersion :</span></span>

<span data-ttu-id="49628-143">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="49628-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="49628-144">バージョン:</span><span class="sxs-lookup"><span data-stu-id="49628-144">InstalledVersion :</span></span>

<span data-ttu-id="49628-145">成功: True</span><span class="sxs-lookup"><span data-stu-id="49628-145">Succeed : True</span></span>

<span data-ttu-id="49628-146">データベースが正しく構成されていても利用可能な場合は、"成功" フィールドに **False** と表示され、追加の警告と情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="49628-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="49628-147">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="49628-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="49628-148">SqlInstanceName: rtc</span><span class="sxs-lookup"><span data-stu-id="49628-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="49628-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="49628-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="49628-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="49628-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="49628-151">DatabaseName: xds</span><span class="sxs-lookup"><span data-stu-id="49628-151">DatabaseName : xds</span></span>

<span data-ttu-id="49628-152">データソース</span><span class="sxs-lookup"><span data-stu-id="49628-152">DataSource :</span></span>

<span data-ttu-id="49628-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="49628-153">SQLServerVersion :</span></span>

<span data-ttu-id="49628-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="49628-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="49628-155">バージョン:</span><span class="sxs-lookup"><span data-stu-id="49628-155">InstalledVersion :</span></span>

<span data-ttu-id="49628-156">成功: False</span><span class="sxs-lookup"><span data-stu-id="49628-156">Succeed : False</span></span>

<span data-ttu-id="49628-157">SqlServerFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="49628-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="49628-158">SqlInstanceName: rtc</span><span class="sxs-lookup"><span data-stu-id="49628-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="49628-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="49628-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="49628-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="49628-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="49628-161">DatabaseName: lis</span><span class="sxs-lookup"><span data-stu-id="49628-161">DatabaseName : lis</span></span>

<span data-ttu-id="49628-162">データソース</span><span class="sxs-lookup"><span data-stu-id="49628-162">DataSource :</span></span>

<span data-ttu-id="49628-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="49628-163">SQLServerVersion :</span></span>

<span data-ttu-id="49628-164">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="49628-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="49628-165">バージョン:</span><span class="sxs-lookup"><span data-stu-id="49628-165">InstalledVersion :</span></span>

<span data-ttu-id="49628-166">成功: False</span><span class="sxs-lookup"><span data-stu-id="49628-166">Succeed : False</span></span>

<span data-ttu-id="49628-167">警告: Test-CsDatabase にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="49628-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="49628-168">ログファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="49628-168">Consult the log file for a</span></span>

<span data-ttu-id="49628-169">詳細な分析と、すべてのエラー (2) と警告 (0) が対応していることを確認する</span><span class="sxs-lookup"><span data-stu-id="49628-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="49628-170">続行してください。</span><span class="sxs-lookup"><span data-stu-id="49628-170">before continuing.</span></span>

<span data-ttu-id="49628-171">警告: 詳細な結果は次のページでご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="49628-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="49628-172">"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csdatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="49628-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="49628-173">04d593cce8e6.html "。</span><span class="sxs-lookup"><span data-stu-id="49628-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="49628-174">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="49628-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="49628-175">次に **、テスト用のデータベース** が失敗する一般的な理由をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="49628-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="49628-176">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="49628-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="49628-177">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="49628-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="49628-178">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="49628-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="49628-179">データベースが正しく構成されていないか、まだ配置されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="49628-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="49628-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="49628-180">See Also</span></span>


[<span data-ttu-id="49628-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="49628-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="49628-182">CsService の入手</span><span class="sxs-lookup"><span data-stu-id="49628-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="49628-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="49628-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="49628-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49628-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

