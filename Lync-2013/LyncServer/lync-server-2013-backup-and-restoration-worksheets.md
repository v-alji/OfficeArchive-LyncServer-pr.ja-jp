---
title: 'Lync Server 2013: バックアップと復元のワークシート'
description: 'Lync Server 2013: バックアップと復元のワークシート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437960"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="ed04a-103">Lync Server 2013 のバックアップと復元ワークシート</span><span class="sxs-lookup"><span data-stu-id="ed04a-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed04a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed04a-104">

<span> </span></span></span>

<span data-ttu-id="ed04a-105">_**最終更新日:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="ed04a-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="ed04a-106">組織のバックアップと復元の計画には、データと設定をバックアップする方法とタイミングについての詳細が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed04a-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="ed04a-107">ここに記載されているワークシートを使用して、特定の展開や組織のバックアップと復元の要件について、この情報を文書化することができます。</span><span class="sxs-lookup"><span data-stu-id="ed04a-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="ed04a-108">次のワークシートを使用して、Lync Server プールまたは Standard Edition サーバーのデータベース、ファイルストア、設定情報をバックアップおよび復元するために必要な情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="ed04a-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="ed04a-109">Lync Server を復元する必要がある場合は、これらのワークシートのコピーを安全な場所に保管して、簡単にアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="ed04a-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ed04a-110">このセクションのワークシートには、Lync Server データベースおよびサーバーのデータと設定を復元するために必要な情報のみが記載されています。</span><span class="sxs-lookup"><span data-stu-id="ed04a-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="ed04a-111">オペレーティングシステムやその他のソフトウェアの再インストールに関する情報など、他の復元情報を文書化する必要がある場合は、組織の展開計画とバックアップおよび復元計画を使用して、これらの要件に対応します。</span><span class="sxs-lookup"><span data-stu-id="ed04a-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="ed04a-112">データベースのバックアップと復元のワークシート</span><span class="sxs-lookup"><span data-stu-id="ed04a-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ed04a-113">次の表を使用して、Lync Server データベースのバックアップと復元に必要な情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="ed04a-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="ed04a-114">バックアップと復元に関するデータベース情報</span><span class="sxs-lookup"><span data-stu-id="ed04a-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed04a-115">データベース</span><span class="sxs-lookup"><span data-stu-id="ed04a-115">Database</span></span></th>
<th><span data-ttu-id="ed04a-116">サーバー名 (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ed04a-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ed04a-117">バックアップスケジュール</span><span class="sxs-lookup"><span data-stu-id="ed04a-117">Backup schedule</span></span></th>
<th><span data-ttu-id="ed04a-118">データベースバックアップツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-118">Database backup tool</span></span></th>
<th><span data-ttu-id="ed04a-119">バックアップセット</span><span class="sxs-lookup"><span data-stu-id="ed04a-119">Backup set</span></span></th>
<th><span data-ttu-id="ed04a-120">バックアップ先</span><span class="sxs-lookup"><span data-stu-id="ed04a-120">Backup destination</span></span></th>
<th><span data-ttu-id="ed04a-121">メモ</span><span class="sxs-lookup"><span data-stu-id="ed04a-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-122">バックエンドサーバー上の Rtc データベース (ユーザーデータの場合)</span><span class="sxs-lookup"><span data-stu-id="ed04a-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ed04a-123"><strong>エクスポート-CsUserData</strong> コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ed04a-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ed04a-124">氏名</span><span class="sxs-lookup"><span data-stu-id="ed04a-124">Name:</span></span></p>
<p><span data-ttu-id="ed04a-125">無期限</span><span class="sxs-lookup"><span data-stu-id="ed04a-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed04a-126">アーカイブデータベースサーバーの LcsLog (既定の名前) データベース</span><span class="sxs-lookup"><span data-stu-id="ed04a-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ed04a-127">SQL Server 管理ツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ed04a-128">氏名</span><span class="sxs-lookup"><span data-stu-id="ed04a-128">Name:</span></span></p>
<p><span data-ttu-id="ed04a-129">無期限</span><span class="sxs-lookup"><span data-stu-id="ed04a-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-130">通話詳細レコードのモニタリングデータベースサーバー上の LcsCdr データベース (CDRs)</span><span class="sxs-lookup"><span data-stu-id="ed04a-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ed04a-131">SQL Server 管理ツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ed04a-132">氏名</span><span class="sxs-lookup"><span data-stu-id="ed04a-132">Name:</span></span></p>
<p><span data-ttu-id="ed04a-133">無期限</span><span class="sxs-lookup"><span data-stu-id="ed04a-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed04a-134">Quality of Experience (QoE) データの監視データベースサーバー上の QoEMetrics データベース</span><span class="sxs-lookup"><span data-stu-id="ed04a-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ed04a-135">SQL Server 管理ツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ed04a-136">氏名</span><span class="sxs-lookup"><span data-stu-id="ed04a-136">Name:</span></span></p>
<p><span data-ttu-id="ed04a-137">無期限</span><span class="sxs-lookup"><span data-stu-id="ed04a-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-138">常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="ed04a-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ed04a-139">SQL Server management tool または <strong>Export-CsPersistentChatData</strong> コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ed04a-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ed04a-140">氏名</span><span class="sxs-lookup"><span data-stu-id="ed04a-140">Name:</span></span></p>
<p><span data-ttu-id="ed04a-141">無期限</span><span class="sxs-lookup"><span data-stu-id="ed04a-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed04a-142">次のデータベースのバックアップまたは復元は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed04a-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="ed04a-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="ed04a-143">Rtcdyn.</span></span> <span data-ttu-id="ed04a-144">このデータベースの一時的なユーザーデータは、サービスの復元には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed04a-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ed04a-145">Rtcab</span><span class="sxs-lookup"><span data-stu-id="ed04a-145">Rtcab.</span></span> <span data-ttu-id="ed04a-146">アドレス帳データベースは、Active Directory ドメインサービスのグローバルアドレス一覧 (GAL) から自動的に再作成されます。</span><span class="sxs-lookup"><span data-stu-id="ed04a-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="ed04a-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="ed04a-147">Rgsdyn.</span></span> <span data-ttu-id="ed04a-148">このデータベースの一時的な応答グループサービスデータは、サービスの復元には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed04a-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ed04a-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="ed04a-149">Cpsdyn.</span></span> <span data-ttu-id="ed04a-150">コールパークアプリケーションの動的な情報は、サービスの復元には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed04a-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ed04a-151">・カンプ</span><span class="sxs-lookup"><span data-stu-id="ed04a-151">MgcComp.</span></span> <span data-ttu-id="ed04a-152">常設チャットのコンプライアンスデータベースは、サービスの復元には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed04a-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="ed04a-153">ファイルストアのバックアップと復元のワークシート</span><span class="sxs-lookup"><span data-stu-id="ed04a-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ed04a-154">次の表を使用して、ファイルストアのバックアップと復元に必要な情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="ed04a-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="ed04a-155">ファイルストアには、会議コンテンツメタデータ、会議のコンプライアンスログ、デバイス更新プログラムの更新ログ、応答グループ、コールパーク、アナウンスメントアプリケーションのオーディオファイルなどのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed04a-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="ed04a-156">バックアップと復元に関するファイルストア情報</span><span class="sxs-lookup"><span data-stu-id="ed04a-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed04a-157">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="ed04a-157">Content</span></span></th>
<th><span data-ttu-id="ed04a-158">サーバー名 (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ed04a-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ed04a-159">バックアップスケジュール</span><span class="sxs-lookup"><span data-stu-id="ed04a-159">Backup schedule</span></span></th>
<th><span data-ttu-id="ed04a-160">ファイルシステムバックアップツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-160">File system backup tool</span></span></th>
<th><span data-ttu-id="ed04a-161">バックアップするファイル共有 \*</span><span class="sxs-lookup"><span data-stu-id="ed04a-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="ed04a-162">バックアップ先</span><span class="sxs-lookup"><span data-stu-id="ed04a-162">Backup destination</span></span></th>
<th><span data-ttu-id="ed04a-163">メモ</span><span class="sxs-lookup"><span data-stu-id="ed04a-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-164">Lync Server ファイルストア</span><span class="sxs-lookup"><span data-stu-id="ed04a-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ed04a-165">標準バックアップツール (Robocopy など)</span><span class="sxs-lookup"><span data-stu-id="ed04a-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="ed04a-166">Enterprise Edition のファイルサーバー。</span><span class="sxs-lookup"><span data-stu-id="ed04a-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="ed04a-167">Standard edition デプロイメントの場合は、標準エディションでは既定でオンになっています。</span><span class="sxs-lookup"><span data-stu-id="ed04a-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="ed04a-168">通常、サイトごとに1つ。</span><span class="sxs-lookup"><span data-stu-id="ed04a-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ed04a-169">" <strong>Meeting. Active</strong> " という名前のファイルはバックアップしないでください。</span><span class="sxs-lookup"><span data-stu-id="ed04a-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="ed04a-170">これらのファイルは使用中であり、会議の実行中にロックされます。</span><span class="sxs-lookup"><span data-stu-id="ed04a-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="ed04a-171">設定のバックアップと復元のワークシート</span><span class="sxs-lookup"><span data-stu-id="ed04a-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ed04a-172">次の表を使用して、設定のバックアップと復元に必要な情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="ed04a-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="ed04a-173">バックアップと復元の設定情報</span><span class="sxs-lookup"><span data-stu-id="ed04a-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed04a-174">データベース</span><span class="sxs-lookup"><span data-stu-id="ed04a-174">Database</span></span></th>
<th><span data-ttu-id="ed04a-175">サーバー名 (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ed04a-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ed04a-176">バックアップスケジュール</span><span class="sxs-lookup"><span data-stu-id="ed04a-176">Backup schedule</span></span></th>
<th><span data-ttu-id="ed04a-177">バックアップツール</span><span class="sxs-lookup"><span data-stu-id="ed04a-177">Backup tool</span></span></th>
<th><span data-ttu-id="ed04a-178">構成ファイル (.xml) 名</span><span class="sxs-lookup"><span data-stu-id="ed04a-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="ed04a-179">バックアップの場所</span><span class="sxs-lookup"><span data-stu-id="ed04a-179">Backup location</span></span></th>
<th><span data-ttu-id="ed04a-180">メモ</span><span class="sxs-lookup"><span data-stu-id="ed04a-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-181">トポロジ構成用の中央管理ストア内の Xds データベース (グローバル)</span><span class="sxs-lookup"><span data-stu-id="ed04a-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ed04a-182"><strong>エクスポート-CsConfiguration</strong> コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ed04a-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed04a-183">E9 の中央管理ストアの Lis データベース (グローバル) の場所情報 (グローバル)</span><span class="sxs-lookup"><span data-stu-id="ed04a-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ed04a-184"><strong>CsLisConfiguration</strong> コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ed04a-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed04a-185">応答グループ構成用のバックエンドサーバー上の RgsConfig データベース (プール)</span><span class="sxs-lookup"><span data-stu-id="ed04a-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ed04a-186"><strong>Export-CsRgsConfiguration</strong> コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ed04a-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="ed04a-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed04a-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

