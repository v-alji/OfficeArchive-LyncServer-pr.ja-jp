---
title: 'Lync Server 2013: バックアップと復元の要件: データ'
description: 'Lync Server 2013: バックアップと復元の要件: データ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437988"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="b67fc-103">Lync Server 2013 でのバックアップと復元の要件: データ</span><span class="sxs-lookup"><span data-stu-id="b67fc-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b67fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b67fc-104">

<span> </span></span></span>

<span data-ttu-id="b67fc-105">_**最終更新日:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="b67fc-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="b67fc-106">Lync Server は、データベースに保存されている設定と構成情報、およびデータベースやファイルストアに保存されているデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="b67fc-107">このトピックでは、組織で障害や停止が発生した場合に、サービスを復元できるようにするためにバックアップする必要のあるデータについて説明します。また、個別にバックアップする必要がある Lync Server で使用されているデータとコンポーネントも識別します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="b67fc-108">設定と構成の要件</span><span class="sxs-lookup"><span data-stu-id="b67fc-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="b67fc-109">このトピックでは、Lync Server サービスの回復に必要な設定と構成情報をバックアップおよび復元する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="b67fc-110">構成情報は、中央管理ストア、または別のバックエンドデータベースまたは Standard Edition サーバーに保存されています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="b67fc-111">次の表は、バックアップと復元に必要な設定と構成情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="b67fc-112">設定データと構成データ</span><span class="sxs-lookup"><span data-stu-id="b67fc-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b67fc-113">データの種類</span><span class="sxs-lookup"><span data-stu-id="b67fc-113">Type of data</span></span></th>
<th><span data-ttu-id="b67fc-114">保存場所</span><span class="sxs-lookup"><span data-stu-id="b67fc-114">Where stored</span></span></th>
<th><span data-ttu-id="b67fc-115">説明/バックアップするタイミング</span><span class="sxs-lookup"><span data-stu-id="b67fc-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b67fc-116">トポロジ構成情報</span><span class="sxs-lookup"><span data-stu-id="b67fc-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="b67fc-117">一元管理ストア (データベース: Xds)</span><span class="sxs-lookup"><span data-stu-id="b67fc-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="b67fc-118">トポロジ、ポリシー、構成の設定。</span><span class="sxs-lookup"><span data-stu-id="b67fc-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="b67fc-119">通常のバックアップでバックアップを作成し、Lync Server コントロールパネルまたはコマンドレットを使用して、構成またはポリシーを変更します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b67fc-120">位置情報</span><span class="sxs-lookup"><span data-stu-id="b67fc-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="b67fc-121">一元管理ストア (データベース: Lis)</span><span class="sxs-lookup"><span data-stu-id="b67fc-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="b67fc-122">エンタープライズ Voip 拡張 9-1-1 (E9-1) 構成情報。</span><span class="sxs-lookup"><span data-stu-id="b67fc-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="b67fc-123">通常、この情報は静的です。</span><span class="sxs-lookup"><span data-stu-id="b67fc-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="b67fc-124">定期的なバックアップでバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b67fc-125">応答グループの構成情報</span><span class="sxs-lookup"><span data-stu-id="b67fc-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="b67fc-126">バックエンドサーバーまたは Standard Edition server (データベース: RgsConfig)</span><span class="sxs-lookup"><span data-stu-id="b67fc-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="b67fc-127">応答グループのエージェントグループ、キュー、ワークフロー。</span><span class="sxs-lookup"><span data-stu-id="b67fc-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="b67fc-128">定期的なバックアップに加えて、エージェントグループ、キュー、またはワークフローを追加または変更した後でバックアップします。</span><span class="sxs-lookup"><span data-stu-id="b67fc-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="b67fc-129">データ要件</span><span class="sxs-lookup"><span data-stu-id="b67fc-129">Data Requirements</span></span>

<span data-ttu-id="b67fc-130">障害が発生した場合に Lync Server サービスを復元できるように、バックアップする必要がある Lync Server データの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="b67fc-131">データの種類によっては、回復には必要ないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b67fc-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="b67fc-132">このトピックには、次のような種類のデータをバックアップする手順は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="b67fc-133">エンドポイントとサブスクリプション、アクティブな会議サーバー、一時的な会議の状態などの一時的なユーザーデータ (データベース: RtcDyn)</span><span class="sxs-lookup"><span data-stu-id="b67fc-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="b67fc-134">アドレス帳データ (データベース: Rtcab と Rtcab1)。</span><span class="sxs-lookup"><span data-stu-id="b67fc-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="b67fc-135">アドレス帳データベースは、Active Directory ドメインサービスから自動的に再生成されます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="b67fc-136">コールパークアプリケーションの動的情報 (データベース: CpsDyn)</span><span class="sxs-lookup"><span data-stu-id="b67fc-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="b67fc-137">エージェントのサインイン状態や通話待機情報などの一時的応答グループデータ (データベース: RgsDyn)</span><span class="sxs-lookup"><span data-stu-id="b67fc-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="b67fc-138">常設チャットのコンプライアンスデータベース (データベース: の場合は、mdf)。</span><span class="sxs-lookup"><span data-stu-id="b67fc-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="b67fc-139">常設チャットのコンプライアンスを有効にしている場合、データベースから情報を読み取るように構成されたアダプターを使用していて、それを別の形式に変換できる限り、常設チャットのコンプライアンスデータベース内の情報は一時的です。</span><span class="sxs-lookup"><span data-stu-id="b67fc-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="b67fc-140">したがって、常設チャットのコンプライアンスデータベースは一時的なものと見なされます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="b67fc-141">Lync Server 2013 常設チャットサーバーには、XML アダプターが付属しています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="b67fc-142">このデータを使用するカスタムアダプターをインストールして、Exchange Hosted アーカイブなどの他のソースに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="b67fc-143">次の表は、バックアップと復元に必要なデータを示しています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="b67fc-144">データベースに格納されているデータ</span><span class="sxs-lookup"><span data-stu-id="b67fc-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b67fc-145">データの種類</span><span class="sxs-lookup"><span data-stu-id="b67fc-145">Type of data</span></span></th>
<th><span data-ttu-id="b67fc-146">保存場所</span><span class="sxs-lookup"><span data-stu-id="b67fc-146">Where stored</span></span></th>
<th><span data-ttu-id="b67fc-147">説明/バックアップするタイミング</span><span class="sxs-lookup"><span data-stu-id="b67fc-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b67fc-148">固定ユーザーデータ</span><span class="sxs-lookup"><span data-stu-id="b67fc-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="b67fc-149">バックエンドサーバーまたは Standard Edition server (データベース: RTCXDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="b67fc-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="b67fc-150">ユーザー権限、ユーザーの連絡先リスト、サーバーまたはプールのデータ、スケジュールされた会議など。</span><span class="sxs-lookup"><span data-stu-id="b67fc-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="b67fc-151">このユーザーデータには、会議にアップロードされたコンテンツは含まれません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="b67fc-152">定期的なバックアップでバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-152">Back up with your regular backups.</span></span> <span data-ttu-id="b67fc-153">この情報は動的ですが、最新の定期的なバックアップに復元する必要がある場合は、更新が失われることはありません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="b67fc-154">連絡先リストが組織にとって重要である場合は、このデータをより頻繁にバックアップできます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b67fc-155">データをアーカイブする</span><span class="sxs-lookup"><span data-stu-id="b67fc-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="b67fc-156">アーカイブデータベース (データベース: LcsLog)</span><span class="sxs-lookup"><span data-stu-id="b67fc-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="b67fc-157">このデータは、Microsoft Exchange 統合オプションを有効にしている場合、Exchange 2013 に保存される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="b67fc-158">そうしないと、このデータは Lync Server アーカイブデータベースに保存されます。これは、別の Lync Server データベースと併置されているか、別のデータベースサーバー上でスタンドアロンである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="b67fc-159">インスタントメッセージング (IM) と会議の内容。</span><span class="sxs-lookup"><span data-stu-id="b67fc-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="b67fc-160">このデータは、Lync Server にとっては重要ではありませんが、規制を目的として組織にとって重要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="b67fc-161">必要に応じてバックアップスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b67fc-162">データの監視</span><span class="sxs-lookup"><span data-stu-id="b67fc-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="b67fc-163">監視データベース (LcsCDR と QoeMetrics)</span><span class="sxs-lookup"><span data-stu-id="b67fc-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="b67fc-164">これらのデータベースは、別の Lync Server データベースと併置されている場合や、別のデータベースサーバー上でスタンドアロンである場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="b67fc-165">通話の詳細レコード (LcsCDR .mdf) と Quality of Experience (QoE) メトリック (QoeMetrics)。</span><span class="sxs-lookup"><span data-stu-id="b67fc-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="b67fc-166">通話の詳細レコードは動的であり、ビジネスにとって重要である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="b67fc-167">規制上の理由からこれらのレコードが必要かどうかを考慮して、バックアップのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="b67fc-168">エクスペリエンスの品質情報は動的です。</span><span class="sxs-lookup"><span data-stu-id="b67fc-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="b67fc-169">QoE データの損失は、Lync Server の運用には重要ではありませんが、ビジネスにとって重要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="b67fc-170">この情報が組織にとって重要であるかどうかに基づいて、バックアップのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b67fc-171">常設チャットデータ</span><span class="sxs-lookup"><span data-stu-id="b67fc-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="b67fc-172">常設チャットデータベース (持っています)。</span><span class="sxs-lookup"><span data-stu-id="b67fc-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="b67fc-173">このデータベースは、別の Lync Server データベースと併置されている場合や、別のデータベースサーバー上でスタンドアロンである場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="b67fc-174">常設チャットデータは、チャットルームに投稿された実際のチャットコンテンツです。</span><span class="sxs-lookup"><span data-stu-id="b67fc-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="b67fc-175">このデータは、多くの場合、ビジネスクリティカルです。</span><span class="sxs-lookup"><span data-stu-id="b67fc-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="b67fc-176">Lync Server に用意されている <strong>CsPersistentChatData</strong> コマンドレットを使用して、SQL Server バックアップを使用するか、データベースをエクスポートするかを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="b67fc-177">データを回復するには、最後の完全バックアップの時点までデータベースをインポートして復元することができます。つまり、障害が発生した時点にデータベースを復元することはできません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="b67fc-178">ファイルストアのデータ要件</span><span class="sxs-lookup"><span data-stu-id="b67fc-178">File Store Data Requirements</span></span>

<span data-ttu-id="b67fc-179">Enterprise Edition の展開では、Lync Server ファイルストアは通常、ファイルサーバー上にあります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="b67fc-180">Standard Edition の展開では、Lync Server ファイルストアは既定で Standard Edition サーバー上に配置されています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="b67fc-181">通常、サイトで共有される Lync Server ファイルストアは1つです。</span><span class="sxs-lookup"><span data-stu-id="b67fc-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="b67fc-182">常設チャットファイルストアでは、Lync Server ファイルストアと同じファイル共有が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="b67fc-183">ファイルストアの場所は、サーバーの共有名として識別され \\ \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="b67fc-184">ファイルストアの特定の場所を検索するには、[トポロジビルダー] を開き、[ **ファイルストア** ] ノードを確認します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="b67fc-185">次の表は、バックアップと復元を行う必要があるファイルストアを示しています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="b67fc-186">ファイルストア</span><span class="sxs-lookup"><span data-stu-id="b67fc-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b67fc-187">データの種類</span><span class="sxs-lookup"><span data-stu-id="b67fc-187">Type of data</span></span></th>
<th><span data-ttu-id="b67fc-188">保存場所</span><span class="sxs-lookup"><span data-stu-id="b67fc-188">Where stored</span></span></th>
<th><span data-ttu-id="b67fc-189">説明/バックアップするタイミング</span><span class="sxs-lookup"><span data-stu-id="b67fc-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b67fc-190">Lync Server ファイルストア</span><span class="sxs-lookup"><span data-stu-id="b67fc-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="b67fc-191">通常は、ファイルサーバー、ファイルクラスター、または Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="b67fc-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="b67fc-192">会議コンテンツ、会議コンテンツメタデータ、会議のコンプライアンスログ、アプリケーションデータファイル、デバイス更新のためのファイルの更新、応答グループのオーディオファイル、コールパーク、およびお知らせアプリケーション、および常設チャットルームに投稿されたファイル。</span><span class="sxs-lookup"><span data-stu-id="b67fc-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="b67fc-193">定期的なバックアップでバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="b67fc-194">その他のバックアップ要件</span><span class="sxs-lookup"><span data-stu-id="b67fc-194">Additional Backup Requirements</span></span>

<span data-ttu-id="b67fc-195">障害が発生した場合に Lync Server サービスを復元できるようにするために、Lync Server 自体の一部ではない必要なコンポーネントをバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="b67fc-196">このドキュメントで説明されている Lync Server バックアップと復元プロセスの一環として、次のコンポーネントはバックアップまたは復元されません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="b67fc-197">**Active Directory ドメインサービス**   Lync Server のバックアップと同時に Active Directory ツールを使用して、AD DS のバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="b67fc-198">Ad ds と Lync Server の同期を維持することが重要です。この問題は、Lync Server で、AD DS で一致しない連絡先オブジェクトが想定されている場合に発生する可能性のある問題を回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b67fc-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="b67fc-199">AD DS には、Lync Server によって使用される次の設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="b67fc-200">ユーザー SIP URI とその他のユーザー設定。</span><span class="sxs-lookup"><span data-stu-id="b67fc-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="b67fc-201">応答グループ、会議アテンダントなどのアプリケーションの連絡先オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="b67fc-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="b67fc-202">中央管理ストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b67fc-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="b67fc-203">Kerberos 認証アカウント (オプションのコンピューターオブジェクト) と Lync Server セキュリティグループ。</span><span class="sxs-lookup"><span data-stu-id="b67fc-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="b67fc-204">Windows Server 2008 での AD DS のバックアップと復元の詳細については、「AD DS のバックアップと回復のステップバイステップガイド」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) 。</span><span class="sxs-lookup"><span data-stu-id="b67fc-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="b67fc-205">**証明機関と証明書**   組織のポリシーを使って、証明機関 (CA) と証明書をバックアップします。</span><span class="sxs-lookup"><span data-stu-id="b67fc-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="b67fc-206">エクスポート可能な秘密キーを使用している場合は、このドキュメントの手順を使用して Lync Server を復元すると、証明書と秘密キーをバックアップし、エクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="b67fc-207">内部 CA を使用している場合、Lync Server を復元する必要がある場合は、再登録することができます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="b67fc-208">コンピューターに障害が発生した場合に使用できるように、セキュリティで保護された場所で秘密キーを保持することが重要です。</span><span class="sxs-lookup"><span data-stu-id="b67fc-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="b67fc-209">**System Center Operations Manager**   Microsoft System Center Operations Manager (以前の Microsoft Operations Manager) を使って Lync Server の展開を監視している場合は、Lync Server を監視している間に、必要に応じて、作成したデータをバックアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="b67fc-210">標準の SQL Server バックアッププロセスを使用して System Center Operations Manager ファイルをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="b67fc-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="b67fc-211">これらのファイルは、回復時に復元されません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="b67fc-212">**公衆交換電話網 (PSTN) ゲートウェイの構成**   エンタープライズ Voip または Survivable Branch アプライアンスを使用している場合は、PSTN ゲートウェイ構成をバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="b67fc-213">PSTN ゲートウェイの構成のバックアップと復元の詳細については、ベンダーにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="b67fc-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="b67fc-214">**共存バージョンの Lync server または Office Communications server**   Lync server 2013 の展開 coexists で Lync Server 2010 または以前のバージョンの Office Communications Server を使用している場合、このドキュメントの手順を使用して、以前のバージョンをバックアップまたは復元することはできません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="b67fc-215">代わりに、以前のバージョンに対して特別に記載されているバックアップと復元の手順を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="b67fc-216">Lync Server 2010 のバックアップと復元の詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) 。</span><span class="sxs-lookup"><span data-stu-id="b67fc-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="b67fc-217">Microsoft Office Communications Server 2007 R2 のバックアップと復元の詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) 。</span><span class="sxs-lookup"><span data-stu-id="b67fc-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="b67fc-218">**インフラストラクチャ情報**   ファイアウォール構成、負荷分散構成、インターネットインフォメーションサービス (IIS) 構成、ドメインネームシステム (DNS) レコードと IP アドレス、動的ホスト構成プロトコル (DHCP) 構成など、インフラストラクチャに関する情報をバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="b67fc-219">これらのコンポーネントのバックアップの詳細については、それぞれのベンダーに確認してください。</span><span class="sxs-lookup"><span data-stu-id="b67fc-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="b67fc-220">**Microsoft exchange と Exchange ユニファイドメッセージング (UM)**   Microsoft Exchange のドキュメントに記載されているように、Microsoft Exchange と Exchange UM をバックアップして復元します。</span><span class="sxs-lookup"><span data-stu-id="b67fc-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="b67fc-221">Exchange Server 2013 のバックアップと復元の詳細については、を参照してください [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) 。</span><span class="sxs-lookup"><span data-stu-id="b67fc-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="b67fc-222">Exchange Server 2010 のバックアップと復元の詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) 。</span><span class="sxs-lookup"><span data-stu-id="b67fc-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="b67fc-223">Lync Server 2013 では、ユーザーの連絡先リスト、高解像度のユーザー写真、および Exchange 2013 に保存されているデータをアーカイブする機能が導入されています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="b67fc-224">これらの種類のデータをバックアップする方法については、次の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b67fc-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="b67fc-225">**高精細写真** は、Exchange Server バックアップの一部としてバックアップされています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="b67fc-226">**統合連絡先ストア** は、Lync Server 2013 で導入されています。</span><span class="sxs-lookup"><span data-stu-id="b67fc-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="b67fc-227">ユニファイド連絡先ストアを使用すると、ユーザーは Exchange 2013 ですべての連絡先情報を保存できます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="b67fc-228">ユーザーの連絡先がユニファイド連絡先ストアと Lync バックエンドサーバーのどちらに保存されているかについて、ユーザーが確実にバックアップを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="b67fc-229">次のシナリオでは、ユーザーの連絡先を統合連絡先ストアに移行することによって、バックアップと復元プロセスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="b67fc-230">**シナリオ 1:** ユーザーの連絡先はユニファイド連絡先ストアに移行され、ユーザーの連絡先の移行前に使用した Lync Server バックアップから復元が実行されます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="b67fc-231">このシナリオでは、Lync Server の移行タスクがユーザーの連絡先を Exchange に移行し始めるまで、ユーザーは最長で1日後に最新の連絡先の状態になります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="b67fc-232">(ユーザーの連絡先は以前にユニファイド連絡先ストアに移行されたため、Exchange の連絡先情報が使用されることに注意してください)。</span><span class="sxs-lookup"><span data-stu-id="b67fc-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="b67fc-233">このシナリオでは、管理者の介入は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="b67fc-234">**シナリオ 2:** ユーザーの連絡先は、以前はユニファイド連絡先ストアに保存されていましたが、ロールバックされました。</span><span class="sxs-lookup"><span data-stu-id="b67fc-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="b67fc-235">復元は、ユーザーの連絡先がユニファイド連絡先ストアに保存されているときに行われた Lync Server バックアップから実行されます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="b67fc-236">このシナリオで `Error: Incorrect Exchange Version` は、クライアントまたはサーバーのログにエラーメッセージが表示されることがあります。これは問題として示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="b67fc-237">ユーザーは、Exchange から直接 Lync 2013 の連絡先リストにアクセスできますが、クライアントの状態は Lync Server の状態と一致しません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="b67fc-238">この問題を解決するには、管理者が、影響を受けるユーザーに対して **CsUCSRollback** コマンドレットを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="b67fc-239">**アーカイブデータ** は Exchange 2013 に保存できます。</span><span class="sxs-lookup"><span data-stu-id="b67fc-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="b67fc-240">このデータは、Lync Server にとっては重要ではありませんが、規制を目的として組織にとって重要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b67fc-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="b67fc-241">アーカイブデータが Exchange に保存されており、組織にとって重要な場合は、Exchange のバックアップと復元の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b67fc-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="b67fc-242">Exchange に保存されているアーカイブデータは、Lync Server に戻すことができないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b67fc-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="b67fc-243">さらに、Lync アーカイブデータベースに既に保存されているデータを Exchange に移動する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="b67fc-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="b67fc-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b67fc-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

