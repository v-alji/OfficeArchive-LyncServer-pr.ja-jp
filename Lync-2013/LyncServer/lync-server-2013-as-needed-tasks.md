---
title: 'Lync Server 2013: 必要に応じてタスク'
description: 'Lync Server 2013: 必要に応じてタスクを実行します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440550"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a><span data-ttu-id="3bc90-103">Lync Server 2013 での必要なタスク</span><span class="sxs-lookup"><span data-stu-id="3bc90-103">As-needed tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3bc90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3bc90-104">

<span> </span></span></span>

<span data-ttu-id="3bc90-105">_**最終更新日:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="3bc90-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="3bc90-106">必要に応じて、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3bc90-106">Perform the following tasks as necessary.</span></span> <span data-ttu-id="3bc90-107">通常、標準の手順でもカバーされています。</span><span class="sxs-lookup"><span data-stu-id="3bc90-107">They are frequently also covered by standard procedures:</span></span>

  - <span data-ttu-id="3bc90-108">\* \* 完全なセキュリティ監査 \* \* この監査は、メッセージングシステムのアップグレードまたは再設計、または試みた (または成功した) セキュリティ侵害に対応して、定期的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-108">\*\*Full Security Auditing   \*\*You can perform this audit regularly, in response to an upgrade or redesign of the messaging system, or in response to an attempted (or successful) security breach.</span></span> <span data-ttu-id="3bc90-109">この手順では、サーバーやファイアウォールでのポートスキャン、セキュリティ修正プログラムの監査、サードパーティのペネトレーションテストなどを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-109">The procedure may involve port scans on servers and firewalls, audits of security fixes, and third-party penetration tests.</span></span>

  - <span data-ttu-id="3bc90-110">**証明書を期限切れに置き換える**   Lync Server の証明書を確認することは、通常の週間タスクの1つであり、管理者はすべての証明書の有効期限を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bc90-110">**Replace Certificates about to Expire**   Checking Lync Server Certificates is one of regular weekly tasks, and as part of the procedure an administrator should have a record of all certificates’ expiry dates.</span></span> <span data-ttu-id="3bc90-111">このレコードを使用すると、特定の証明書が期限切れになり、必要に応じて置き換えられるときに、管理者が通知を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-111">This record enables an administrator to create a notification when a particular certificate is about to be expired and replaced as needed.</span></span>

  - <span data-ttu-id="3bc90-112">**パフォーマンスベースラインの更新**   アップグレードまたは構成を変更した後で、パフォーマンスのベースラインを更新します。</span><span class="sxs-lookup"><span data-stu-id="3bc90-112">**Updating Performance Baselines**   Update performance baselines after an upgrade or configuration change.</span></span> <span data-ttu-id="3bc90-113">組織では、ベースラインを使用してパフォーマンスの変化を測定し、システムのパフォーマンスに影響する問題を検出することができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-113">Your organization can use baselines to measure performance changes and to detect issues that affect system performance.</span></span>

  - <span data-ttu-id="3bc90-114">**エンタープライズプールの管理**   エンタープライズプール、標準エディションサーバー、および組織内の他のすべてのサーバーの初期構成は、個々のサーバーの展開中に実行されました。</span><span class="sxs-lookup"><span data-stu-id="3bc90-114">**Managing Enterprise Pool**   Initial configuration of Enterprise pools, Standard Edition servers, and any other servers in your organization's environment were done during deployment of the individual servers.</span></span> <span data-ttu-id="3bc90-115">Standard Edition server とエンタープライズプールの展開後のサーバーとプールの管理には、次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-115">Post-deployment management of servers and pools for Standard Edition servers and Enterprise pools includes the following tasks:</span></span>
    
      - <span data-ttu-id="3bc90-116">フロントエンドサーバーの管理</span><span class="sxs-lookup"><span data-stu-id="3bc90-116">Managing Front End Servers</span></span>
    
      - <span data-ttu-id="3bc90-117">Web 会議を管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-117">Managing Web Conferencing</span></span>
    
      - <span data-ttu-id="3bc90-118">会議を管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-118">Managing Conferencing</span></span>
    
      - <span data-ttu-id="3bc90-119">サービスアカウントの資格情報を変更する</span><span class="sxs-lookup"><span data-stu-id="3bc90-119">Changing Service Account Credentials</span></span>
    
      - <span data-ttu-id="3bc90-120">データベースの管理</span><span class="sxs-lookup"><span data-stu-id="3bc90-120">Managing Databases</span></span>
    
      - <span data-ttu-id="3bc90-121">サービスを開始および停止し、サーバーの役割を非アクティブ化する</span><span class="sxs-lookup"><span data-stu-id="3bc90-121">Starting and Stopping Services and Deactivating Server Roles</span></span>
    
      - <span data-ttu-id="3bc90-122">サーバーとサーバーの役割の削除、プールの削除、サーバーとプールの無効化</span><span class="sxs-lookup"><span data-stu-id="3bc90-122">Removing Servers and Server Roles, Removing Pools, and Decommissioning Servers and Pools</span></span>

  - <span data-ttu-id="3bc90-123">**利用状況の管理**   Lync Server 2013 を構成して、組織に最も適した機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-123">**Managing Usage**   You can configure Lync Server 2013 to provide the features and functionality that are most appropriate for your organization.</span></span> <span data-ttu-id="3bc90-124">これには、次のポリシーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-124">This includes the following:</span></span>
    
      - <span data-ttu-id="3bc90-125">オンプレミスの Web 会議会議のサポートを管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-125">Managing Support for On-Premise Web Conferencing Meetings</span></span>
    
      - <span data-ttu-id="3bc90-126">インスタントメッセージを送信するための配布グループの使用を管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-126">Managing the Use of Distribution Groups to Send Instant Messages</span></span>
    
      - <span data-ttu-id="3bc90-127">連絡先、プレゼンス、およびクエリを管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-127">Managing Contacts, Presence, and Queries</span></span>
    
      - <span data-ttu-id="3bc90-128">クライアントのバージョンのフィルター処理を構成する</span><span class="sxs-lookup"><span data-stu-id="3bc90-128">Configuring Client Version Filtering</span></span>
    
      - <span data-ttu-id="3bc90-129">インテリジェント IM フィルターの設定</span><span class="sxs-lookup"><span data-stu-id="3bc90-129">Configuring Intelligent IM Filtering</span></span>
    
      - <span data-ttu-id="3bc90-130">アーカイブ、通話の詳細の記録、会議のコンプライアンスを構成する</span><span class="sxs-lookup"><span data-stu-id="3bc90-130">Configuring Archiving, Call Detail Recording, and Meeting Compliance</span></span>

  - <span data-ttu-id="3bc90-131">**エッジサーバーの接続の管理**   外部接続を提供するために必要なサーバーと設定の継続的な管理には、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-131">**Managing Edge Server Connectivity**   Ongoing management of the servers and settings required to provide external connectivity includes the following:</span></span>
    
      - <span data-ttu-id="3bc90-132">内部サーバーとエッジサーバー間の接続の管理</span><span class="sxs-lookup"><span data-stu-id="3bc90-132">Managing Connectivity between Internal Servers and Edge Servers</span></span>
    
      - <span data-ttu-id="3bc90-133">エッジサーバーの内部および外部インターフェイスと証明書の構成</span><span class="sxs-lookup"><span data-stu-id="3bc90-133">Configuring Internal and External Interfaces and Certificates for Edge Servers</span></span>
    
      - <span data-ttu-id="3bc90-134">フェデレーションパートナーへのアクセスを管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-134">Managing Federated Partner Access</span></span>

  - <span data-ttu-id="3bc90-135">**アドレス帳の管理**   アドレス帳サーバーの管理には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-135">**Administering the Address Book**   Administering Address Book Servers includes the following:</span></span>
    
      - <span data-ttu-id="3bc90-136">アドレス帳のサーバー電話の正規化を構成する</span><span class="sxs-lookup"><span data-stu-id="3bc90-136">Configuring Address Book Server phone normalization</span></span>
    
      - <span data-ttu-id="3bc90-137">コマンドラインからアドレス帳サーバーを管理する</span><span class="sxs-lookup"><span data-stu-id="3bc90-137">Managing the Address Book Server from the command line</span></span>

  - <span data-ttu-id="3bc90-138">**ユーザーアカウントを管理する**   ユーザーアカウントの管理には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-138">**Managing User Accounts**   Management of user accounts includes the following:</span></span>
    
      - <span data-ttu-id="3bc90-139">Lync Server のユーザーアカウントを有効にする</span><span class="sxs-lookup"><span data-stu-id="3bc90-139">Enabling User Accounts for Lync Server</span></span>
    
      - <span data-ttu-id="3bc90-140">ウィザードを使用して Lync Server ユーザーを構成する</span><span class="sxs-lookup"><span data-stu-id="3bc90-140">Configuring Lync Server Users using the Wizard</span></span>
    
      - <span data-ttu-id="3bc90-141">Lync Server の個々のユーザーアカウントのプロパティを構成する</span><span class="sxs-lookup"><span data-stu-id="3bc90-141">Configuring Individual Lync Server User Account Properties</span></span>
    
      - <span data-ttu-id="3bc90-142">Lync Server ユーザーを検索する</span><span class="sxs-lookup"><span data-stu-id="3bc90-142">Searching for Lync Server Users</span></span>
    
      - <span data-ttu-id="3bc90-143">Lync Server ユーザーを移動する</span><span class="sxs-lookup"><span data-stu-id="3bc90-143">Moving Lync Server Users</span></span>
    
      - <span data-ttu-id="3bc90-144">Lync Server ユーザーを削除する</span><span class="sxs-lookup"><span data-stu-id="3bc90-144">Deleting Lync Server Users</span></span>

  - <span data-ttu-id="3bc90-145">**Lync Server 2013 ログファイルを分析**   する  トラブルシューティングで一般的に使用される便利なツールの1つは、「lync server [2013 ログツールの使用](https://technet.microsoft.com/library/gg558599.aspx)について詳しく説明されている lync Server 2013 ログツール」です。</span><span class="sxs-lookup"><span data-stu-id="3bc90-145">**Analyzing Lync Server 2013 Log Files**   One very helpful tool, generally used for troubleshooting, is the Lync Server 2013 Logging Tool described in detail in [Using Lync Server 2013 Logging Tool](https://technet.microsoft.com/library/gg558599.aspx).</span></span>

<span data-ttu-id="3bc90-146">ログツールによって (サーバーごとに) ログファイルが生成されるため、Microsoft Office Server 12 リソースキットツールがコンピューターにインストールされている場合は、Snooper ツールを使用してこれらのログファイルを表示および分析することができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-146">Because the Logging Tool generates log files (on a per-server basis), these log files can be viewed and analyzed by using the Snooper tool, if the Microsoft Office Server 12 Resource Kit Tools are installed on the computer.</span></span> <span data-ttu-id="3bc90-147">そうしないと、ログもテキストエディターを使って分析することができます。これは、Snooper ユーティリティを使用する場合よりも透明で、より複雑なものになります。</span><span class="sxs-lookup"><span data-stu-id="3bc90-147">Otherwise, logs can also be analyzed by using a text editor, which is much less transparent and more complex than using the Snooper utility.</span></span>

<span data-ttu-id="3bc90-148">プロトコルメッセージの表示と分析を行うには</span><span class="sxs-lookup"><span data-stu-id="3bc90-148">To View and Analyze Protocol Messages</span></span>

<span data-ttu-id="3bc90-149">ログツールで、デバッグセッションを終了したら、[ログファイルの分析] をクリックし、Snooper ツールを使用してログファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="3bc90-149">In the Logging Tool, when you have ended the debug session, click Analyze Log Files to view the log files by using the Snooper tool.</span></span> <span data-ttu-id="3bc90-150">次のコンポーネントのプロトコルログを分析できます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-150">You can analyze protocol logs for the following components:</span></span>

  - <span data-ttu-id="3bc90-151">Lync Server SipStack (SIP)</span><span class="sxs-lookup"><span data-stu-id="3bc90-151">Lync Server SipStack (SIP)</span></span>

  - <span data-ttu-id="3bc90-152">Lync Server S4 (SIP)</span><span class="sxs-lookup"><span data-stu-id="3bc90-152">Lync Server S4 (SIP)</span></span>

  - <span data-ttu-id="3bc90-153">MCU インフラストラクチャ C3P とフォーカス C3P を含む Lync Server 会議のシグナリングトラフィック (C3P)</span><span class="sxs-lookup"><span data-stu-id="3bc90-153">Lync Server Conferencing signaling traffic (C3P), including MCU Infra C3P and Focus C3P</span></span>

  - <span data-ttu-id="3bc90-154">Lync Server Web 会議トラフィック (PSOM)</span><span class="sxs-lookup"><span data-stu-id="3bc90-154">Lync Server Web conferencing traffic (PSOM)</span></span>

  - <span data-ttu-id="3bc90-155">Lync Server ユニファイドコミュニケーションクライアントプラットフォームクライアント (UCCP)</span><span class="sxs-lookup"><span data-stu-id="3bc90-155">Lync Server Unified Communications Client Platform client (UCCP)</span></span>

  - <span data-ttu-id="3bc90-156">アーカイブデータベースからのエラーレポート</span><span class="sxs-lookup"><span data-stu-id="3bc90-156">Error reports from the archiving database</span></span>

<span data-ttu-id="3bc90-157">必要なタスクのパフォーマンスを整理するには、「As-Needed の操作チェックリスト」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3bc90-157">To help organize the performance of as-needed tasks, see As-Needed Operations Checklist.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3bc90-158">詳細な管理手順と管理手順については、「Microsoft Lync Server 2013 管理者ガイド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3bc90-158">For detailed administration and management procedures, see the Microsoft Lync Server 2013 Administration Guide.</span></span>



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a><span data-ttu-id="3bc90-159">バックアップ (および復元) ポリシーまたは構成設定</span><span class="sxs-lookup"><span data-stu-id="3bc90-159">Backup (and restore) policies or configuration settings</span></span>

<span data-ttu-id="3bc90-160">Lync Server 2013 を使用すると、システム全体のバックアップと復元を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-160">Lync Server 2013 lets you back up and restore the whole system.</span></span> <span data-ttu-id="3bc90-161">1つのポリシーまたは構成設定の単一のコレクションをバックアップして、適切なポリシーを取得し、そのオブジェクトを Export-Clixml コマンドレットにパイプして、ポリシー情報を XML ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="3bc90-161">Iif you want to back up (and then maybe someday restore) a single policy or a single collection of configuration settings, retrieve the appropriate policy, and then pipe that object to the Export-Clixml cmdlet, which saves the policy information as an XML file:</span></span>

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

<span data-ttu-id="3bc90-162">これで、RedmondClientPolicy を試して、設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="3bc90-162">You may now experiment with RedmondClientPolicy and change lots of the settings.</span></span> <span data-ttu-id="3bc90-163">以前のポリシーを復元する場合は、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3bc90-163">If you decide instead to restore the old policy, enter:</span></span>

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

<span data-ttu-id="3bc90-164">この方法はほとんどのポリシーと設定で動作しますが、より複雑な項目 (ルーティング構成設定など、複数の異なる音声ルートを含むアイテム) では動作しません。</span><span class="sxs-lookup"><span data-stu-id="3bc90-164">Note that this approach will work for most policies and settings but it won't work with some of the more complex items—items that contain multiple sub-objects (like routing configuration settings, which contain many separate voice routes).</span></span>

<span data-ttu-id="3bc90-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3bc90-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

