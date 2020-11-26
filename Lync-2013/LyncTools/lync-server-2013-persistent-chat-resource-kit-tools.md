---
title: Lync Server 2013 常設チャットリソースキットツール
description: Lync Server 2013 常設チャットリソースキットツール。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Persistent Chat Resource Kit Tools
ms:assetid: 7a34d2ba-eb25-4e22-92d1-b9baf81b102c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945599(v=OCS.15)
ms:contentKeyID: 51541423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 336e81c97da73da47eee654161a7d8d8956f9edb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438423"
---
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a><span data-ttu-id="e8d22-103">Lync Server 2013 常設チャットリソースキットツール</span><span class="sxs-lookup"><span data-stu-id="e8d22-103">Lync Server 2013 Persistent Chat Resource Kit Tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8d22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8d22-104">

<span> </span></span></span>

<span data-ttu-id="e8d22-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="e8d22-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="e8d22-106">Lync Server 2013 常設チャットリソースキットツールは、Lync Server 2013 常設チャットサーバーの展開と管理を行う IT 管理者にとって、日常的なタスクを簡単にするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-106">The Lync Server 2013 Persistent Chat Resource Kit tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="e8d22-107">このトピックでは、インストール手順に加えて、各ツールの目的とその用途の例について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-107">In addition to installation instructions, this topic describes the purpose of each tool, and examples of its use.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="e8d22-108">リソース キット ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="e8d22-108">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="e8d22-109">Lync Server 2013 のリソースキットツールをインストールするには、 **PersistentChatReskit.msi** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-109">To install the Lync Server 2013, Resource Kit Tools, download **PersistentChatReskit.msi**.</span></span> <span data-ttu-id="e8d22-110">簡単なインストールを実行するには、 **PersistentChatReskit.msi** を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-110">Run **PersistentChatReskit.msi** to do a simple installation.</span></span> <span data-ttu-id="e8d22-111">.Msi は、次のパスにあるすべてのツールをインストールします。 \\ **Program Files \\ Microsoft Lync Server 2013 \\ 常設チャットサーバーリソースキット**。</span><span class="sxs-lookup"><span data-stu-id="e8d22-111">The .msi installs all the tools in the following path: \\**Program Files\\ Microsoft Lync Server 2013\\Persistent Chat Server Resource Kit**.</span></span> <span data-ttu-id="e8d22-112">このフォルダーには、自己完結型のツールの実行可能ファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-112">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="e8d22-113">ファイルが自分のサブフォルダーにもあるツール。</span><span class="sxs-lookup"><span data-stu-id="e8d22-113">Tools that also have files are in their own subfolders.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e8d22-114">Lync Server 2013 のリソースキットツールをインストールした後、 <STRONG>PsExec.exe</STRONG>をインストールし、 <STRONG>PsExec.exe</STRONG>を次のパスにコピーする必要があります: \\ <STRONG>Program Files \ Lync Server 2013 \ 常設 Chat Server リソース Kit\ChatStressTool</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="e8d22-114">After installing the Lync Server 2013, Resource Kit Tools, you must install <STRONG>PsExec.exe</STRONG> and copy <STRONG>PsExec.exe</STRONG> to the following path: \\<STRONG>Program Files\ Microsoft Lync Server 2013\Persistent Chat Server Resource Kit\ChatStressTool</STRONG>.</span></span> <span data-ttu-id="e8d22-115"><STRONG>PsExec.exe</STRONG>をコピーしない場合、常設チャットのストレスツールでエラー例外がスローされ、正しく実行されません。</span><span class="sxs-lookup"><span data-stu-id="e8d22-115">If you do not copy <STRONG>PsExec.exe</STRONG>, the Persistent Chat Stress Tool will throw an error exception, and not perform correctly.</span></span> <span data-ttu-id="e8d22-116">ツールを実行する前に、必ずこの必須要件を満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e8d22-116">Make sure that you meet this prerequisite requirement prior to running the tool.</span></span> <span data-ttu-id="e8d22-117"><STRONG>PsExec.exe</STRONG>のインストールの詳細については、を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> 。</span><span class="sxs-lookup"><span data-stu-id="e8d22-117">For details about installing <STRONG>PsExec.exe</STRONG>, see <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="e8d22-118">サポートされる環境</span><span class="sxs-lookup"><span data-stu-id="e8d22-118">Supported Environments</span></span>

<span data-ttu-id="e8d22-119">最適なパフォーマンスを実現するには、Lync Server 2013、リソースキットツールを同じ環境にインストールして、Lync Server 2013 で必要とされる仕様と同じようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-119">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="e8d22-120">リソース キット ツールの概要</span><span class="sxs-lookup"><span data-stu-id="e8d22-120">Resource Kit Tools Overview</span></span>

<span data-ttu-id="e8d22-121">Lync Server 2013 常設チャットリソースキットには、次のツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e8d22-121">Here are the tools that are provided in the Lync Server 2013 Persistent Chat Resource Kit.</span></span> <span data-ttu-id="e8d22-122">次のセクションでは、要件や使用例など、各ツールの説明を示します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-122">The following section provides a description of each tool, including requirements and example usage.</span></span>

  - <span data-ttu-id="e8d22-123">影響チェック</span><span class="sxs-lookup"><span data-stu-id="e8d22-123">AffCheck</span></span>

  - <span data-ttu-id="e8d22-124">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="e8d22-124">ChatMonitoringSummary</span></span>

  - <span data-ttu-id="e8d22-125">ChatStress ツール</span><span class="sxs-lookup"><span data-stu-id="e8d22-125">ChatStress Tool</span></span>

  - <span data-ttu-id="e8d22-126">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="e8d22-126">ChatUpgradeVerifier</span></span>

  - <span data-ttu-id="e8d22-127">ChatUsageReport</span><span class="sxs-lookup"><span data-stu-id="e8d22-127">ChatUsageReport</span></span>

  - <span data-ttu-id="e8d22-128">ScheduleADSyncforPrincipal</span><span class="sxs-lookup"><span data-stu-id="e8d22-128">ScheduleADSyncforPrincipal</span></span>

</div>

<div>

## <a name="affcheck"></a><span data-ttu-id="e8d22-129">影響チェック</span><span class="sxs-lookup"><span data-stu-id="e8d22-129">AffCheck</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-130">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-130">Description</span></span>

<span data-ttu-id="e8d22-131">このツールは、常設チャットバックエンドデータベースユーザーとグループの所属レコードが Active Directory ドメインサービスのものと一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-131">The AffCheck tool confirms that the Persistent Chat back-end database user and group affiliation records match that of Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-132">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-132">Requirements</span></span>

<span data-ttu-id="e8d22-133">このツールは、ドメインに参加しているコンピューター上の PersistentChatResKit installer と共にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-133">The tool is installed with the PersistentChatResKit installer on a domain joined machine.</span></span>

<span data-ttu-id="e8d22-134">ツールが実行されるユーザーアカウントには、常設チャットのバックエンドデータベースと Active Directory ドメインサービスへの読み取りアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-134">The user account under which the tool is run must have Read access to the Persistent Chat back-end database and Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-135">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-135">Usage</span></span>

<span data-ttu-id="e8d22-136">構成ファイルに記載されている手順に従って AffCheck.exe.config ファイルを構成し、コマンドラインパラメーターを指定せずに、を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-136">Configure the AffCheck.exe.config file according to the instructions in the config file and run the AffCheck tool without command-line parameters.</span></span> <span data-ttu-id="e8d22-137">既定の AffCheck.exe.config の内容を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-137">Following are the contents of the default AffCheck.exe.config.</span></span>

<span data-ttu-id="e8d22-138">**AffCheck.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="e8d22-138">**AffCheck.exe.config:**</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
        <!--Domain Controller IP Address-->
        <add key="LDAP" value="LDAP://0.0.0.0/"/>
        
        <!-- Domain DN  This is case sensitive, it must match exactly-->
        <add key="DomainComponent" value ="DC=DOMAIN,DC=COM"/>
        
        <!--Domain Administrator Login and Password-->
        <add key="DomainLogin" value="DOMAIN\Administrator"/>
        <add key="DomainPassword" value ="password"/>
        
        <!-- Connection string to Group Chat Database-->
        <add key="ConnectionString" value="data source=SQL_SERVER\INSTANCE;initial catalog=DATABASE_NAME;integrated security=SSPI"/>
        
        <!--Check group affiliations-->
        <add key="CheckGroups" value="true"/>
        
        <!--Check user affilations-->
        <add key="CheckUsers" value="true"/>
        
        <!--List all affiliations if there is a mismatch between database and active directory-->
        <add key="ListAffiliations" value="true"/>
    
        <!--If you need to offset the results of the number of affilations in AD(can be negative to add to AD parent count)-->
        <add key="Offset" value ="0"/>
    
        <!--If you need to ignore certain parents, provide a semi colon delimitted list.-->
        <add key="Ignore" value ="DC=uatest,DC=test,DC=contoso,DC=com;DC=test,DC=contoso,DC=com"/>
      </appSettings>
    </configuration>
  ```
</div>

</div>

<div>

## <a name="chatmonitoringsummary"></a><span data-ttu-id="e8d22-139">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="e8d22-139">ChatMonitoringSummary</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-140">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-140">Description</span></span>

<span data-ttu-id="e8d22-141">PersistentChatMonitoringSummary ツールは、一時的なチャット監視情報を監視データベースから指定された CSV ログファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-141">The PersistentChatMonitoringSummary tool moves Persistent Chat monitoring information from the monitoring database into a specified CSV log file.</span></span>

<span data-ttu-id="e8d22-142">CSV ファイルには、合計セッション数、成功セッション、予期しないエラー、予期したエラーの数、診断 ID、失敗数、障害の説明による予期しないエラーの内訳が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e8d22-142">The CSV file will contain a breakdown of Persistent Chat sessions by number of total sessions, successful sessions, unexpected failures, expected failures, and a breakdown of the unexpected failures by diagnostic ID, number of failures, and failure description.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-143">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-143">Requirements</span></span>

<span data-ttu-id="e8d22-144">固定チャットリソースキットツールを、監視データベースにアクセスできるドメインに参加しているコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-144">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Monitoring database.</span></span>

<span data-ttu-id="e8d22-145">ツールを実行するユーザーアカウントには、監視データベースへの読み取りアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-145">The user account under which the tool runs must have Read access to the Monitoring database.</span></span>

<span data-ttu-id="e8d22-146">PersistentChatMonitoringSummary.exe.config ファイルには、 \<connectionStrings\> 監視データベースへの接続文字列を定義するセクションが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-146">The file, PersistentChatMonitoringSummary.exe.config, must contain a \<connectionStrings\> section that defines the connection string to the Monitoring database.</span></span> <span data-ttu-id="e8d22-147">また、監視データを収集する PersistentChatEndpointUri のキーと、生成される CSV ファイルの場所へのファイルパスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-147">It must also contain a key for the PersistentChatEndpointUri that the monitoring data will be gathered for, and a file path to a location for the CSV file that will be generated.</span></span> <span data-ttu-id="e8d22-148">例については、インストールされている構成ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8d22-148">Refer to the installed config file for examples.</span></span> <span data-ttu-id="e8d22-149">このファイルは、ツールと同じディレクトリ内に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-149">The file must be located in the same directory as the tool.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-150">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-150">Usage</span></span>

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

<span data-ttu-id="e8d22-151">次のパラメーターでデータの選択を定義します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-151">These parameters define the selection of data:</span></span>

<span data-ttu-id="e8d22-152">**StartDateTime:** 必要に応じて、選択期間の開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-152">**StartDateTime:** Optionally specifies the start date of the selection period.</span></span> <span data-ttu-id="e8d22-153">既定値: 1/1/1753 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="e8d22-153">Default: 1/1/1753 12:00:00 AM</span></span>

<span data-ttu-id="e8d22-154">**Enddatetime:** オプションで、選択期間の最後の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-154">**EndDateTime:** Optionally specifies the last date of the selection period.</span></span> <span data-ttu-id="e8d22-155">既定値: 今すぐ</span><span class="sxs-lookup"><span data-stu-id="e8d22-155">Default: Now</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="e8d22-156">例</span><span class="sxs-lookup"><span data-stu-id="e8d22-156">Example</span></span>

```Batch
    C:\Users\Administrator.VDOMAIN>Desktop\PersistentChatMonitoringSummary.exe
    Reading database connection information, Persistent Chat endpoint uri, and csv output path information from the application config file...
    Connecting to Monitoring database with connection string specified in the application config file...
    Gathering Persistent Chat Session Summary information between "1/1/1753 12:00:00 AM" and "11/19/2012 10:11:25 AM" for Persistent Chat Endpoint Uri "persistentChatEndpointUri@domain.com"...
    Press enter to continue or hit ctr-c if these settings are incorrect...
    
    The summary information about Persistent Chat sessions from the Monitoring database has been output to C:\PersistentChatMonitoring_dd4ace24-4c8a-4a3d-8fd4-591bdfacf47b.csv
    Press enter to exit...
```

</div>

</div>

<div>

## <a name="persistent-chat-stress-tool"></a><span data-ttu-id="e8d22-157">常設チャット応力ツール</span><span class="sxs-lookup"><span data-stu-id="e8d22-157">Persistent Chat Stress Tool</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-158">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-158">Description</span></span>

<span data-ttu-id="e8d22-159">常設チャットのストレスツールでは、継続的なチャットの使用をシミュレートして、さまざまなユーザーモデルを含め、想定される用途のシナリオに合わせてリアルタイムのパフォーマンスをテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-159">The Persistent Chat Stress tool provides an easy way to simulate usage of Persistent Chat to test real-world performance, including varied user models to better fit your expected usage scenarios.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-160">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-160">Requirements</span></span>

<span data-ttu-id="e8d22-161">常設チャットリソースキットツールを、常設チャットのバックエンドデータベースにアクセスできるドメインに参加しているコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-161">Install the Persistent Chat Resource Kit tools onto a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="e8d22-162">この *コントローラー* マシンに加えて、いくつかの *ローダー* マシンが必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-162">In addition to this *controller* machine, you will need several *loader* machines.</span></span> <span data-ttu-id="e8d22-163">ユーザーモデル内のすべての10K ユーザーに対して、ローダーコンピューターで少なくとも 4 GB の空き RAM が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-163">For every 10K users in your user model, you will need at least 4GB of free RAM on a loader machine.</span></span> <span data-ttu-id="e8d22-164">たとえば、80K ユーザーとの実行には、すべてのローダーコンピューターで分散した RAM の 32 GB が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-164">For example, a run with 80K users will require about 32GB of RAM spread across all loader machines.</span></span> <span data-ttu-id="e8d22-165">予想される負荷に関係なく、少なくとも3つのローダーコンピューターを持っていることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-165">We recommend that you have at least three loader machines, regardless of expected load.</span></span>

<span data-ttu-id="e8d22-166">ローダーコンピューターには、.NET 4.5 フレームワークに加えて、Visual C++ 2012 再頒布可能パッケージがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-166">Loader machines must have the .NET 4.5 Framework as well as the Visual C++ 2012 Redistributable installed.</span></span>

</div>

<div>

## <a name="configuration"></a><span data-ttu-id="e8d22-167">構成</span><span class="sxs-lookup"><span data-stu-id="e8d22-167">Configuration</span></span>

<span data-ttu-id="e8d22-168">すべてのローダーコンピューターからアクセスできる共有フォルダーに ChatStressTool ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-168">Copy ChatStressTool files into a shared folder accessible from all loader machines.</span></span>

<span data-ttu-id="e8d22-169">ストレスの実行で使用するユーザーとチャネルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-169">Create users and channels for use in the stress run:</span></span>

  - <span data-ttu-id="e8d22-170">ユーザーモデルを使って通話を発信し、Lync で有効にして、常設チャットポリシーを [有効] に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-170">Create as many users as your user model calls for, enable them for Lync, and set their Persistent Chat policy to Enabled.</span></span>

  - <span data-ttu-id="e8d22-171">応力チャネルのカテゴリを作成し、そのカテゴリに必要なだけのルームを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-171">Create a category for your stress channels, and then create as many rooms as are needed under that category.</span></span> <span data-ttu-id="e8d22-172">カテゴリには、(OU を追加することで) **許可** リスト内のすべてのストレスユーザーを含める必要があります。また、ストレスルームには、 **[開く**] のプライバシー設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-172">The category should have all stress users in its **Allowed** list (by way of adding their OU), and stress rooms should have a privacy setting of **Open**.</span></span>

  - <span data-ttu-id="e8d22-173">追加のストレス会議を作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-173">We recommend creating extra stress rooms.</span></span> <span data-ttu-id="e8d22-174">5万ルームを作成するには、次の Windows PowerShell コマンドラインインターフェイスコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-174">You can create 50,000 rooms with the following Windows PowerShell command-line interface command:</span></span>
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

<span data-ttu-id="e8d22-175">トポロジに合わせて構成ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-175">Edit the configuration files to fit your topology:</span></span>

<span data-ttu-id="e8d22-176">**LoaderProcess.exe.config** で、"controller.contoso.com" をコントローラーコンピューターの完全修飾ドメイン名 (FQDN) に変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-176">In **LoaderProcess.exe.config**, change “controller.contoso.com” to the controller machine’s fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="e8d22-177">**StressLauncher.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="e8d22-177">In **StressLauncher.exe.config:**</span></span>

1.  <span data-ttu-id="e8d22-178">"LoaderBinary" 設定値を共有フォルダーのパスに変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-178">Change the “LoaderBinary” setting value to the shared folder’s path.</span></span>

2.  <span data-ttu-id="e8d22-179">ローダーコンピューターへの管理者アクセス権を持つ資格情報に "AdminUser"/"Adminuser" を変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-179">Change “AdminUser”/”AdminPassword” to credentials that have admin access to loader machines.</span></span>

3.  <span data-ttu-id="e8d22-180">"ChannelCategory" を、ストレスチャンネルが作成されたカテゴリの名前に変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-180">Change “ChannelCategory” to the name of the category that stress channels have been created under.</span></span>

4.  <span data-ttu-id="e8d22-181">"UserNamePattern" と "UserPasswordPattern" を、ストレスユーザーの資格情報と一致するテンプレートに変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-181">Change “UserNamePattern” and “UserPasswordPattern” to a template that matches your stress user credentials.</span></span> <span data-ttu-id="e8d22-182">{0} は、ユーザーのインデックス番号に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-182">{0} is replaced with the user’s index number.</span></span>

5.  <span data-ttu-id="e8d22-183">"Domain" をテストトポロジの SIP ドメインに変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-183">Change “Domain” to the SIP domain of your test topology.</span></span>

6.  <span data-ttu-id="e8d22-184">"ConnectionString" を永続的なチャットのバックエンドデータベースの接続文字列に変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-184">Change “ConnectionString” to a connection string for your Persistent Chat back-end database.</span></span>

7.  <span data-ttu-id="e8d22-185">"UserIndexStart" を最初のストレスユーザーのインデックスに変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-185">Change “UserIndexStart” to the index of the first stress user.</span></span>

8.  <span data-ttu-id="e8d22-186">"LyncFQDN" をフロントエンドプールの FQDN に変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-186">Change “LyncFQDN” to the FQDN of your Front End pool.</span></span>

9.  <span data-ttu-id="e8d22-187">[マシン] の一覧を変更して、すべてのローダーコンピューターにコンピューター名を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-187">Modify the “Machines” list to include machine names for all of your loader machines.</span></span>

10. <span data-ttu-id="e8d22-188">サービスエンドポイントの baseAddress (既定は "controller.contoso.com") をコントローラーコンピューターの FQDN に変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-188">Change the baseAddress of the service endpoint (default is “controller.contoso.com”) to the FQDN of your controller machine.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-189">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-189">Usage</span></span>

<span data-ttu-id="e8d22-190">構成が完了したら、コントローラーコンピューターで StressLauncher.exe を開きます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-190">After configuration is complete, open StressLauncher.exe on the controller machine.</span></span> <span data-ttu-id="e8d22-191">StressLauncher は、任意のユーザーとして起動できます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-191">You can launch StressLauncher as any user.</span></span> <span data-ttu-id="e8d22-192">ローダーコンピューターで開始されるローダープロセスの資格情報は、構成ファイルで指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-192">The credentials under which the loader processes start on the loader machines must be specified in the config file.</span></span> <span data-ttu-id="e8d22-193">また、常設チャットバックエンドデータベースへの読み取りアクセス権を持つ接続文字列も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-193">You also must give a connection string that has Read access to the Persistent Chat back-end database.</span></span> <span data-ttu-id="e8d22-194">この接続文字列で統合 Windows 認証を使っている場合は、このアクセス権を持つユーザーとして StressLauncher を起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-194">If this connection string uses integrated Windows authentication, you must launch StressLauncher as a user that has this access.</span></span>

<span data-ttu-id="e8d22-195">必要に応じて、ユーザーモデルの設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-195">Alter the user model settings as needed.</span></span> <span data-ttu-id="e8d22-196">[ **読み込みの開始** ] をクリックして実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-196">Click **Start Load** to initiate a run.</span></span> <span data-ttu-id="e8d22-197">1分以上経過すると、ユーザーはサインインを開始し、進行状況バーの入力が開始されます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-197">After a minute or so, users will start being signed in, and the progress bar will begin to fill.</span></span> <span data-ttu-id="e8d22-198">この時点で、コントローラーマシンは動作し、パフォーマンスの測定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-198">At this point, you may can the controller machine working and take performance measurements.</span></span>

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a><span data-ttu-id="e8d22-199">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="e8d22-199">ChatUpgradeVerifier</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-200">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-200">Description</span></span>

<span data-ttu-id="e8d22-201">ChatUpgradeVerifier は、常設チャット固有のデータベース比較ツールです。</span><span class="sxs-lookup"><span data-stu-id="e8d22-201">ChatUpgradeVerifier is a Persistent Chat specific database comparison tool.</span></span> <span data-ttu-id="e8d22-202">このツールは、グループチャット 2007 R2 またはグループチャット2010データベース (2007/2010Db) を常設 Chat 2013 データベース (2010Db) に比較します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-202">The tool compares either the Group Chat 2007 R2 or Group Chat 2010 Database (2007/2010Db) to the Persistent Chat 2013 Database (2013Db).</span></span>

<span data-ttu-id="e8d22-203">ツールは、1つずつ、各カテゴリ、常設チャットルーム、および 2007/2010Db のアドインをチェックして、2010Db に表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-203">The tool will check, one by one, each category, Persistent Chat room, and add-in in 2007/2010Db to see if it appears in the 2013Db.</span></span> <span data-ttu-id="e8d22-204">比較では、カテゴリ、チャットルーム、アドイン、カテゴリの範囲に含まれるすべてのプリンシパル、カテゴリまたはチャットルームのいずれかのプリンシパルのすべての設定を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-204">The comparison includes checking all settings on the category, chat room, or add-in, any principals in scope on the category, and any principal in a role on either the category or the chat room.</span></span> <span data-ttu-id="e8d22-205">カテゴリまたはチャットルームが2013Db で正しく表示されない場合、相違点は競合ファイルに出力されます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-205">If a category or a chat room does not appear correctly in the 2013Db, the differences will be output to a conflicts file.</span></span> <span data-ttu-id="e8d22-206">アップグレードが行われた後に、2007/2010Db が変更され、このツールが実行されると、競合ファイルへの相違点が出力されます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-206">If, after the upgrade has occurred, the 2007/2010Db is changed and then this tool is run, there will be a differences output to the conflicts file.</span></span> <span data-ttu-id="e8d22-207">このアプリケーションはデータベースの比較ツールにすぎないことに注意してください。アップグレードプロセスを検証しません。</span><span class="sxs-lookup"><span data-stu-id="e8d22-207">Note that this application is a database comparison tool only and does not validate the upgrade process.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-208">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-208">Requirements</span></span>

<span data-ttu-id="e8d22-209">常設チャットリソースキットツールは、常設チャットのバックエンドデータベースにアクセスできるドメインに参加しているコンピューターにインストールします (これは、常設チャット用の以前のバージョンと現在のバージョンになります)。</span><span class="sxs-lookup"><span data-stu-id="e8d22-209">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end databases (previous and current versions for Persistent Chat).</span></span>

<span data-ttu-id="e8d22-210">ツールを実行するユーザーアカウントには、常設チャットデータベースへの読み取りアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-210">The user account under which the tool runs must have Read access to the Persistent Chat databases.</span></span>

<span data-ttu-id="e8d22-211">ChatUpgradeVerifier.exe.config ファイルには、適切なグループチャットデータベース (Groupchat 2007R2 または 2010) への接続文字列を含む、GroupChat2007R2Db パラメーターまたは GroupChat2010Db パラメーターのいずれかが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-211">The ChatUpgradeVerifier.exe.config file must contain either the GroupChat2007R2Db parameter or the GroupChat2010Db parameter, with a connection string to the appropriate Group Chat database (either Groupchat 2007R2 or 2010).</span></span> <span data-ttu-id="e8d22-212">また、常設 Chat 2013 データベースへの接続文字列を持つ PersistentChat2013Db パラメーターも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-212">It must also contain a PersistentChat2013Db parameter, with a connection string to the Persistent Chat 2013 database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-213">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-213">Usage</span></span>

<span data-ttu-id="e8d22-214">パラメーターなしで **Chatupgradeverifier** を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-214">Run **ChatUpgradeVerifier** without any parameters.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="e8d22-215">例</span><span class="sxs-lookup"><span data-stu-id="e8d22-215">Example</span></span>

<span data-ttu-id="e8d22-216">![ChatUpgradeVerifier.exe の実行](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "ChatUpgradeVerifier.exe の実行")</span><span class="sxs-lookup"><span data-stu-id="e8d22-216">![Running ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Running ChatUpgradeVerifier.exe.")</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a><span data-ttu-id="e8d22-217">常設チャットの使用状況レポート</span><span class="sxs-lookup"><span data-stu-id="e8d22-217">Persistent Chat Usage Report</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-218">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-218">Description</span></span>

<span data-ttu-id="e8d22-219">ChatUsageReport ツールは、常設チャットサービスの利用状況に関する HTML レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-219">The ChatUsageReport tool generates an HTML report of Persistent Chat service usage.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-220">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-220">Requirements</span></span>

<span data-ttu-id="e8d22-221">常設チャットリソースキットツールは、常設チャットのバックエンドデータベースにアクセスできるドメインに参加しているコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-221">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="e8d22-222">ツールが実行されるユーザーアカウントには、常設チャットのバックエンドデータベースへの読み取りアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-222">The user account under which the tool is run must have Read access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="e8d22-223">ChatUsageReport.exe.config ファイルには、 \<connectionStrings\> 常設チャットバックエンドデータベースへの接続文字列を定義するセクションが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-223">The file, ChatUsageReport.exe.config, must contain a \<connectionStrings\> section defining the connection string to the Persistent Chat back-end database.</span></span> <span data-ttu-id="e8d22-224">既定の構成ファイルの内容は、参照用にここに記載されています。</span><span class="sxs-lookup"><span data-stu-id="e8d22-224">The contents of the default config file are included here, for your reference.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-225">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-225">Usage</span></span>

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
<span data-ttu-id="e8d22-226">次のパラメーターでデータの選択を定義します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-226">These parameters define the selection of data:</span></span>

<span data-ttu-id="e8d22-227">**StartDate:** オプションで、選択期間の UTC 開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-227">**StartDate:** Optionally specifies the UTC start date of the selection period.</span></span> <span data-ttu-id="e8d22-228">既定値: 最も古い日付</span><span class="sxs-lookup"><span data-stu-id="e8d22-228">Default: Earliest Date</span></span>

<span data-ttu-id="e8d22-229">終了日 **:** オプションで、選択期間の UTC の終了日を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-229">**EndDate:** Optionally specifies the UTC end date of the selection period.</span></span> <span data-ttu-id="e8d22-230">既定値: 今すぐ</span><span class="sxs-lookup"><span data-stu-id="e8d22-230">Default: Now</span></span>

<span data-ttu-id="e8d22-231">これらのパラメーターは、どのように表示されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-231">These parameters define how and what data is displayed:</span></span>

<span data-ttu-id="e8d22-232">**Topactiveusers:** この値が指定されている場合、レポートには、選択した期間にユーザーがチャットルームに投稿したメッセージの数に基づいて、最もアクティブな n 人のユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-232">**TopActiveUsers:** If this is specified, the report will include the n most active users in terms of the number of messages the user has posted in the chat room for the selected period.</span></span> <span data-ttu-id="e8d22-233">既定値:10</span><span class="sxs-lookup"><span data-stu-id="e8d22-233">Default: 10</span></span>

<span data-ttu-id="e8d22-234">**TopActiveRooms:** この値が指定されている場合、レポートには、選択した期間のルームに投稿されたメッセージ数に基づいて、最もアクティブなチャットルームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-234">**TopActiveRooms:** If this is specified, the report will include the n most active chat rooms in terms of the number of messages posted in the room for the selected period.</span></span> <span data-ttu-id="e8d22-235">既定値:10</span><span class="sxs-lookup"><span data-stu-id="e8d22-235">Default: 10</span></span>

<span data-ttu-id="e8d22-236">**LeastActiveRooms:** この値を指定すると、選択した期間のチャットルームに投稿されたメッセージ数に基づいて、アクティブなチャットルームが少なくとも1つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-236">**LeastActiveRooms:** If this is specified, the report will include the n least active chat rooms in terms of the number of messages posted in the chat room for the selected period.</span></span> <span data-ttu-id="e8d22-237">ルームには、少なくとも1つのメッセージが投稿されます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-237">Rooms will have at least one message posted.</span></span> <span data-ttu-id="e8d22-238">既定値:10</span><span class="sxs-lookup"><span data-stu-id="e8d22-238">Default: 10</span></span>

<span data-ttu-id="e8d22-239">**RoomsInactiveSince:** 指定した場合、レポートには、指定した日付以降に無効になっているチャットルームのリストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-239">**RoomsInactiveSince:** If this is specified, the report will include a list of chat rooms that have been inactive since the specified date.</span></span> <span data-ttu-id="e8d22-240">既定値: 時間全体</span><span class="sxs-lookup"><span data-stu-id="e8d22-240">Default: Entire Time</span></span>

<span data-ttu-id="e8d22-241">**Outputfolder:** ChatUsageReport.html とグラフの画像が配置されているフォルダー。</span><span class="sxs-lookup"><span data-stu-id="e8d22-241">**OutputFolder:** The folder where the ChatUsageReport.html and the graph images will be placed.</span></span> <span data-ttu-id="e8d22-242">これは、構成ファイルまたはコマンドラインで定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d22-242">This must be defined in the config file or on the command line.</span></span>

<span data-ttu-id="e8d22-243">すべてのコマンドラインパラメーターの値は、ツールと同じディレクトリにある ChatUsageReport.exe.config ファイルでも指定できます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-243">All of the command line parameter values can also be specified in the ChatUsageReport.exe.config file that is located in the same directory as the tool.</span></span> <span data-ttu-id="e8d22-244">構成ファイルとコマンドラインの両方でいずれかの値が指定されている場合、コマンドライン値は構成ファイルの値を上書きします。</span><span class="sxs-lookup"><span data-stu-id="e8d22-244">If any value is specified in both the config file and the command line, the command line value will override the config file value.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="e8d22-245">出力</span><span class="sxs-lookup"><span data-stu-id="e8d22-245">Output</span></span>

<span data-ttu-id="e8d22-246">レポートには、常に次の出力が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-246">The report will always include the following output:</span></span>

  - <span data-ttu-id="e8d22-247">選択された期間のメッセージ投稿数に基づいて、最もアクティブなチャットルームの上位 n 個。</span><span class="sxs-lookup"><span data-stu-id="e8d22-247">Top n most active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="e8d22-248">選択した期間のメッセージ投稿数に基づいて、最もアクティブなユーザーの上位 n 個。</span><span class="sxs-lookup"><span data-stu-id="e8d22-248">Top n most active users by number of message posts for selected period.</span></span>

  - <span data-ttu-id="e8d22-249">選択された期間のメッセージ投稿数の多い、最もアクティブなチャットルーム。</span><span class="sxs-lookup"><span data-stu-id="e8d22-249">Top n least active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="e8d22-250">データベースの全期間にわたって、または指定した日付以降、非アクティブなチャットルーム。</span><span class="sxs-lookup"><span data-stu-id="e8d22-250">Chat rooms that are inactive for the entire life of the database, or since the specified date.</span></span>

  - <span data-ttu-id="e8d22-251">選択された期間の毎日のメッセージ投稿の傾向。</span><span class="sxs-lookup"><span data-stu-id="e8d22-251">Daily message post trend for selected period.</span></span>

  - <span data-ttu-id="e8d22-252">選択された期間の毎週のメッセージ投稿の傾向。</span><span class="sxs-lookup"><span data-stu-id="e8d22-252">Weekly message post trend for selected period.</span></span>

  - <span data-ttu-id="e8d22-253">選択された期間の月次メッセージ投稿のトレンド。</span><span class="sxs-lookup"><span data-stu-id="e8d22-253">Monthly message post trend for selected period.</span></span>

  - <span data-ttu-id="e8d22-254">選択された期間のメッセージ投稿の合計数です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-254">Total message posts for selected period.</span></span>

  - <span data-ttu-id="e8d22-255">有効なルームの合計数です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-255">Total number of enabled rooms.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="e8d22-256">例</span><span class="sxs-lookup"><span data-stu-id="e8d22-256">Example</span></span>

<span data-ttu-id="e8d22-257">次の例では、2001年全体の利用状況レポートを生成し、ChatUsageReport.exe.config で指定した OutputFolder にレポートを配置します。</span><span class="sxs-lookup"><span data-stu-id="e8d22-257">The following example generates a usage report for the entire year 2001 and places the report in the OutputFolder specified in the ChatUsageReport.exe.config.</span></span>

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
<span data-ttu-id="e8d22-258">ChatUsageReport.exe.config:</span><span class="sxs-lookup"><span data-stu-id="e8d22-258">ChatUsageReport.exe.config:</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <connectionStrings>
        <!-- The PersistentChat connection string must be defined in this file. -->
        <add name="PersistentChat" connectionString="Data Source=contoso.com\RTC;Initial Catalog=mgc;Integrated Security=SSPI"/>
      </connectionStrings>
      <appSettings>
        <!-- The OutputFolder must be defined here or on the command line. -->
        <add key="OutputFolder" value="."/>
        <!-- The values below are the same as the application defaults. -->
        <add key="StartDate" value="01/01/0001"/>
        <add key="EndDate" value="12/31/9999"/>
        <add key="TopActiveUsers" value="10"/>
        <add key="TopActiveRooms" value="10"/>
        <add key="LeastActiveRooms" value="10"/>
        <add key="RoomsInactiveSince" value="01/01/0001"/>
      </appSettings>
    </configuration></configuration>
```
</div>

</div>

<div>

## <a name="scheduleadsyncforprincipal"></a><span data-ttu-id="e8d22-259">ScheduleADSyncForPrincipal</span><span class="sxs-lookup"><span data-stu-id="e8d22-259">ScheduleADSyncForPrincipal</span></span>

<div>

## <a name="description"></a><span data-ttu-id="e8d22-260">説明</span><span class="sxs-lookup"><span data-stu-id="e8d22-260">Description</span></span>

<span data-ttu-id="e8d22-261">ScheduleADSyncForPrincipal は、常設チャットバックエンドデータベースに接続しているときに、SQL Server Management Studio 内から直接実行する必要がある Microsoft SQL Server 2012 スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="e8d22-261">ScheduleADSyncForPrincipal is a Microsoft SQL Server 2012 script that must be run directly from within SQL Server Management Studio when connected to the Persistent Chat back-end database.</span></span> <span data-ttu-id="e8d22-262">このスクリプトを使用すると、強制チャットによって、スケジュールされた同期時間を待つのではなく、Active Directory ドメインサービスのユーザーのレコードを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="e8d22-262">This script enables you to force Persistent Chat to synchronize its records of a user with those of Active Directory Domain Services, rather than waiting for the scheduled synchronization time.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="e8d22-263">要件</span><span class="sxs-lookup"><span data-stu-id="e8d22-263">Requirements</span></span>

<span data-ttu-id="e8d22-264">スクリプトが実行されるユーザーアカウントには、常設チャットバックエンドデータベースへの所有者アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8d22-264">The user account under which the script is run must have owner access to the Persistent Chat back-end database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="e8d22-265">使用方法</span><span class="sxs-lookup"><span data-stu-id="e8d22-265">Usage</span></span>

<span data-ttu-id="e8d22-266">既定のスクリプトの内容は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e8d22-266">Following are the contents of the default script:</span></span>

```Powershell
    /*
    This script will schedule a principal for a forced AD synchronization cycle
    
    If you're using Sql Server Management Studio, pressing Ctrl+Shift+M will 
    allow you to specify values for the template parameter.
    */
    
        insert into
          tblPrincipalMeta
          (
           prinID
          ,prinAffiliationsDirty
          ,prinAttributesDirty
          ,prinDeleted
          )
          select
            prinID
           ,1
           ,1
           ,0
          from
            tblPrincipal
          where
            prinID not in (select prinID from tblPrincipalMeta) and
            prinID = <PrinID,int,0>
     
        update
          tblPrincipalMeta
        set
          prinAffiliationsDirty = 1
         ,prinAttributesDirty = 1
         ,tryCount = 0
         ,nextTry = null
        where
         prinID = <PrinID,int,0>
```

<span data-ttu-id="e8d22-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8d22-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

