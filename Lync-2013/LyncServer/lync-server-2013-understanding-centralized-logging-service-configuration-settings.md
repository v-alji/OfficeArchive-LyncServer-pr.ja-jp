---
title: 集中ログサービスの構成設定について
description: 集中ログサービスの構成設定について。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Centralized Logging Service configuration settings
ms:assetid: 3c34e600-0b91-43dc-b4cc-90b6a70ee12e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688029(v=OCS.15)
ms:contentKeyID: 49733619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f99dbffe15c4b3f0dc13d231c3a2732a8554397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399495"
---
# <a name="understanding-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="23949-103">Lync Server 2013 の一元ログサービスの構成設定について</span><span class="sxs-lookup"><span data-stu-id="23949-103">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23949-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23949-104">

<span> </span></span></span>

<span data-ttu-id="23949-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="23949-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="23949-106">一元的なログサービスは、ログサービスの収集方法、収集方法、収集される場所、およびログ設定の内容を定義するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="23949-106">The Centralized Logging Service is configured to define what the logging service is intended to collect, how it collects, where it will collect from, and what the log settings are.</span></span> <span data-ttu-id="23949-107">これらの設定は、グローバル (展開全体) またはサイト (展開内で指定されたサイト) に対して定義します。</span><span class="sxs-lookup"><span data-stu-id="23949-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span></span> <span data-ttu-id="23949-108">定義するすべてのログで、ログを開始、停止、更新、および検索するコマンドに対して使用する ID に適した設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="23949-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span></span>

<div>

## <a name="to-display-the-current-centralized-logging-service-configuration"></a><span data-ttu-id="23949-109">現在の集中化ログサービスの構成を表示するには</span><span class="sxs-lookup"><span data-stu-id="23949-109">To display the current Centralized Logging Service configuration</span></span>

1.  <span data-ttu-id="23949-110">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="23949-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="23949-111">コマンド ライン プロンプトで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="23949-111">Type the following at a command-line prompt:</span></span>
    
        Get-CsClsConfiguration
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="23949-112">定義によって返される構成設定の範囲を絞り込んだり、展開したりすることができ <CODE>-Identity</CODE> ます。たとえば、"site: レドモンド" のように、サイトレドモンドの CsClsConfiguration のみを返すようにします。</span><span class="sxs-lookup"><span data-stu-id="23949-112">You can narrow or expand the scope of the configuration settings that are returned by defining <CODE>-Identity</CODE> and a scope, such as "Site:Redmond" to return only the CsClsConfiguration for the site Redmond.</span></span> <span data-ttu-id="23949-113">構成の特定の部分に関する詳細が必要な場合は、出力を別の Windows PowerShell コマンドレットにパイプすることができます。</span><span class="sxs-lookup"><span data-stu-id="23949-113">If you want details about a given portion of the configuration, you can pipe the output into another Windows PowerShell cmdlet.</span></span> <span data-ttu-id="23949-114">たとえば、サイト "Redmond" の構成で定義されているシナリオに関する詳細情報を取得するには、次のように入力します。 <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span><span class="sxs-lookup"><span data-stu-id="23949-114">For example, to get details about the scenarios defined in the configuration for site "Redmond", type: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span></span>

    
    </div>
    
    <span data-ttu-id="23949-115">![Get-CsClsConfiguration からのサンプル出力](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Get-CsClsConfiguration からのサンプル出力")</span><span class="sxs-lookup"><span data-stu-id="23949-115">![Sample output from Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Sample output from Get-CsClsConfiguration.")</span></span>
    
    <span data-ttu-id="23949-116">このコマンドレットの結果には、一元管理サービスの現在の構成が表示されます。</span><span class="sxs-lookup"><span data-stu-id="23949-116">The result from the cmdlet displays the current configuration of the Centralized Logging Service.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="23949-117">構成設定</span><span class="sxs-lookup"><span data-stu-id="23949-117">Configuration Setting</span></span></th>
    <th><span data-ttu-id="23949-118">説明</span><span class="sxs-lookup"><span data-stu-id="23949-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-119"><strong>Identity</strong></span><span class="sxs-lookup"><span data-stu-id="23949-119"><strong>Identity</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-p103">この構成のスコープと名前を識別します。存在するグローバル構成は 1 つのみで、サイトごとに 1 つの構成があります。</span><span class="sxs-lookup"><span data-stu-id="23949-p103">Identifies the scope and name for this configuration. There is only one Global configuration, and one configuration per site.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-122"><strong>Scenarios</strong></span><span class="sxs-lookup"><span data-stu-id="23949-122"><strong>Scenarios</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-123">この構成に対して定義されたシナリオの一覧。</span><span class="sxs-lookup"><span data-stu-id="23949-123">Listing of all scenarios that are defined for this configuration.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-124"><strong>SearchTerms</strong></span><span class="sxs-lookup"><span data-stu-id="23949-124"><strong>SearchTerms</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-125">構成の定義済み検索用語。</span><span class="sxs-lookup"><span data-stu-id="23949-125">Defined search terms for the configuration.</span></span> <span data-ttu-id="23949-126">Office 365 または Microsoft 365、オンプレミス展開ではありません。</span><span class="sxs-lookup"><span data-stu-id="23949-126">Office 365 or Microsoft 365, not on-premises deployments.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-127"><strong>SecurityGroups</strong></span><span class="sxs-lookup"><span data-stu-id="23949-127"><strong>SecurityGroups</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-128">コンピューターを確認できるユーザー (つまり、セキュリティ グループのメンバー) を、そのユーザーのサイトに基づいて制御する定義済みセキュリティ グループ。</span><span class="sxs-lookup"><span data-stu-id="23949-128">Defined security groups that control who (that is, members of the security groups) can see computers based on the site they are located in.</span></span> <span data-ttu-id="23949-129">このコンテキストのサイトは、トポロジビルダーで定義されているサイトです。</span><span class="sxs-lookup"><span data-stu-id="23949-129">Site, in this context, is the site as defined in Topology Builder.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-130"><strong>Regions</strong></span><span class="sxs-lookup"><span data-stu-id="23949-130"><strong>Regions</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-131">SecurityGroups を地域にまとめる際に定義済み地域が使用されます。</span><span class="sxs-lookup"><span data-stu-id="23949-131">Defined regions are used to collect SecurityGroups into a region, for example EMEA.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-132"><strong>EtlFileFolder</strong></span><span class="sxs-lookup"><span data-stu-id="23949-132"><strong>EtlFileFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-133">コンピューター上でログファイルが書き込まれる場所の定義パス。</span><span class="sxs-lookup"><span data-stu-id="23949-133">Defined path to the location where log files are written on computers.</span></span> <span data-ttu-id="23949-134">CLSAgent は、ログファイルを書き込み、ネットワークサービスのコンテキストで実行します。</span><span class="sxs-lookup"><span data-stu-id="23949-134">CLSAgent writes the log files and runs under the context of the Network Service.</span></span> <span data-ttu-id="23949-135">この場合、% TEMP% が%WINDIR%\ServiceProfiles\NetworkService\AppData\Local に拡張されます。</span><span class="sxs-lookup"><span data-stu-id="23949-135">In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-136"><strong>EtlFileRolloverSizeMB</strong></span><span class="sxs-lookup"><span data-stu-id="23949-136"><strong>EtlFileRolloverSizeMB</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-p107">パラメーターは、新しいイベント トレース ログ (.etl) ファイルが作成される前のログ ファイルの最大サイズを示します。定義したサイズに達すると、EtlFileRolloverMinutes で設定された最大時間に達していなくても、新しいログ ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="23949-p107">The parameter indicates the maximum size of the log file before a new event trace log (.etl) file is created. A new log file is created when the defined size is reached even if the maximum time set in EtlFileRolloverMinutes has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-139"><strong>EtlFileRolloverMinutes</strong></span><span class="sxs-lookup"><span data-stu-id="23949-139"><strong>EtlFileRolloverMinutes</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-p108">新しい .etl ファイルが作成されるまでのログの定義済み最大経過時間 (分単位)。指定した時間が過ぎると、EtlFileRolloverSizeMBE で設定された最大サイズに達していなくても、新しいログ ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="23949-p108">Defined maximum amount of time, in minutes, that a log can elapse before a new .etl file is created. A new log file is created when the timer expires even if the maximum size set in EtlFileRolloverSizeMB has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-142"><strong>TmfFileSearchPath</strong></span><span class="sxs-lookup"><span data-stu-id="23949-142"><strong>TmfFileSearchPath</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-143">トレース メッセージ形式のファイルを検索する場所。</span><span class="sxs-lookup"><span data-stu-id="23949-143">Location to search for the trace message format files.</span></span> <span data-ttu-id="23949-144">トレースメッセージ形式のファイルは、バイナリファイルを人間が読める形式に変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="23949-144">The trace message format files are used to convert the binary files into a human readable format.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-145"><strong>CacheFileLocalFolders</strong></span><span class="sxs-lookup"><span data-stu-id="23949-145"><strong>CacheFileLocalFolders</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-p110">キャッシュ ファイルが書き込まれるコンピューター上の場所への定義済みパス。CLSAgent はキャッシュ ファイルを書き込み、ネットワーク サービスとの関連で実行されます。この場合は、%TEMP% が %WINDIR%\ServiceProfiles\NetworkService\AppData\Local に展開されます。既定では、キャッシュ ファイルとログ ファイルは同じディレクトリに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="23949-p110">Defined path to the location where cache files are written on computers. CLSAgent writes the cache files and runs under the context of the Network Service. In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. By default, cache files and log files are written to the same directory.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-150"><strong>CacheFileNetworkFolder</strong></span><span class="sxs-lookup"><span data-stu-id="23949-150"><strong>CacheFileNetworkFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-151">汎用名前付け規則 (UNC) パスを定義すると、ログ操作中にキャッシュ ファイルを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="23949-151">You can define a universal naming convention (UNC) path to receive the cache files during logging operations.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-152"><strong>CacheFileLocalRetentionPeriod</strong></span><span class="sxs-lookup"><span data-stu-id="23949-152"><strong>CacheFileLocalRetentionPeriod</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-153">キャッシュ ファイルが保持される最大時間 (日単位) として定義されます。</span><span class="sxs-lookup"><span data-stu-id="23949-153">Defined as the maximum time, in days, that cache files are retained.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-154"><strong>CacheFileMaxDiskUsage</strong></span><span class="sxs-lookup"><span data-stu-id="23949-154"><strong>CacheFileMaxDiskUsage</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-155">キャッシュ ファイルで使用できるディスク容量の割合として定義されます。</span><span class="sxs-lookup"><span data-stu-id="23949-155">Defined as the percentage of disk space that can be used by the cache files.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-156"><strong>ComponentThrottleLimit</strong></span><span class="sxs-lookup"><span data-stu-id="23949-156"><strong>ComponentThrottleLimit</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-157">自動調整制限がトリガーされるまでの、コンポーネントが生成できる秒あたりの最大トレース数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="23949-157">Defined as the maximum number of traces per second that a component can produce before the automatic throttle limiter is triggered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="23949-158"><strong>ComponentThrottleSample</strong></span><span class="sxs-lookup"><span data-stu-id="23949-158"><strong>ComponentThrottleSample</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-159">ComponentThrottleLimit を超えることができる 60 秒単位の回数。</span><span class="sxs-lookup"><span data-stu-id="23949-159">Number of times in 60 seconds that the ComponentThrottleLimit can be exceeded.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="23949-160"><strong>MinimumClsAgentServiceVersion</strong></span><span class="sxs-lookup"><span data-stu-id="23949-160"><strong>MinimumClsAgentServiceVersion</strong></span></span></p></td>
    <td><p><span data-ttu-id="23949-161">実行が許可されている CLSAgent の最小バージョン。</span><span class="sxs-lookup"><span data-stu-id="23949-161">The minimum version of the CLSAgent allowed to run.</span></span> <span data-ttu-id="23949-162">この要素は、Office 365 または Microsoft 365 を対象としています。</span><span class="sxs-lookup"><span data-stu-id="23949-162">This element is intended for Office 365 or Microsoft 365.</span></span></p></td>
    </tr>
    </tbody>
    </table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="23949-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="23949-163">See Also</span></span>


[<span data-ttu-id="23949-164">Lync Server 2013 の一元管理されたログサービスの概要</span><span class="sxs-lookup"><span data-stu-id="23949-164">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  


<span data-ttu-id="23949-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="23949-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span></span>  
<span data-ttu-id="23949-166">[CsClsConfiguration の削除](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="23949-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span></span>  
<span data-ttu-id="23949-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="23949-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span></span>  
<span data-ttu-id="23949-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="23949-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span></span>  
  

<span data-ttu-id="23949-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23949-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

