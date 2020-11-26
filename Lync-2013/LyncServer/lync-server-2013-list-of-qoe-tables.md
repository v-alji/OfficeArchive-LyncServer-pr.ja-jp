---
title: 'Lync Server 2013: QoE テーブルの一覧'
description: 'Lync Server 2013: QoE テーブルの一覧。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of QoE tables
ms:assetid: 176194d7-d184-4e23-94bb-cb62b4db47f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398236(v=OCS.15)
ms:contentKeyID: 48183512
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 871babf246f616d306a03f84f9134605dd595999
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426572"
---
# <a name="list-of-qoe-tables-in-lync-server-2013"></a><span data-ttu-id="ea657-103">Lync Server 2013 の QoE テーブルの一覧</span><span class="sxs-lookup"><span data-stu-id="ea657-103">List of QoE tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea657-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea657-104">

<span> </span></span></span>

<span data-ttu-id="ea657-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ea657-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ea657-106">データベーススキーマは、次の表で構成されています。</span><span class="sxs-lookup"><span data-stu-id="ea657-106">The database schema consists of the following tables.</span></span>

<span data-ttu-id="ea657-107">**サポートテーブル**</span><span class="sxs-lookup"><span data-stu-id="ea657-107">**Supporting Tables**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea657-108"><strong>テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-108"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="ea657-109"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-109"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea657-110"><a href="lync-server-2013-appsharingmetricsthreshold-table.md">Lync Server 2013 の AppSharingMetricsThreshold テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-110"><a href="lync-server-2013-appsharingmetricsthreshold-table.md">AppSharingMetricsThreshold table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-111">アプリケーションの共有で使用されるエクスペリエンスメトリックの品質と受け入れ可能な値を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-111">Stores optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-112"><a href="lync-server-2013-codecdescription-table.md">Lync Server 2013 の CodecDescription テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-112"><a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-113">一意のコーデック識別子を対応するコーデックにマップします。</span><span class="sxs-lookup"><span data-stu-id="ea657-113">Maps unique codec identifiers to their corresponding codec.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-114"><a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-114"><a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-115">環境の品質データベースの別の場所で使用されている一意の IP アドレス識別子に IP アドレスをマッピングします。</span><span class="sxs-lookup"><span data-stu-id="ea657-115">Maps IP addresses to the unique IP address identifiers used elsewhere in the Quality of Experience database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-116"><a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 の NetworkConnectionDetail テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-116"><a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-117">ネットワーク接続の種類を、エクスペリエンスデータベースの他の場所で使用されていたネットワーク接続識別子にマップします。</span><span class="sxs-lookup"><span data-stu-id="ea657-117">Maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-118"><a href="lync-server-2013-purgesettings-table-qoe.md">Lync Server 2013 の PurgeSettings テーブル (QoE)</a></span><span class="sxs-lookup"><span data-stu-id="ea657-118"><a href="lync-server-2013-purgesettings-table-qoe.md">PurgeSettings table (QoE) in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-119">古い品質エクスペリエンスレコードが QoE データベースから自動的に削除されるかどうかを指定する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-119">Stores information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-120"><a href="lync-server-2013-traceroute-table.md">Lync Server 2013 の TraceRoute テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-120"><a href="lync-server-2013-traceroute-table.md">TraceRoute table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-121">通話のルーティング情報を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-121">Stores routing information for calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-122"><a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の UserAgentDef テーブル (QoE)</a></span><span class="sxs-lookup"><span data-stu-id="ea657-122"><a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-123">ユーザーエージェント識別子をエージェントのわかりやすい名前にマップします。</span><span class="sxs-lookup"><span data-stu-id="ea657-123">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-124"><a href="lync-server-2013-videometricsthreshold-table.md">Lync Server 2013 の VideoMetricsThreshold テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-124"><a href="lync-server-2013-videometricsthreshold-table.md">VideoMetricsThreshold table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-125">ビデオ通話で使用されるエクスペリエンスメトリックの品質を実現するのに最適な値を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-125">Stores optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-126"><a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-126"><a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-127">オーディオとビデオのセッションで使用されるセッション開始プロトコル (SIP) ユーザーエージェント (UA) 文字列と UA の種類が保存されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-127">Stores Session Initiation Protocol (SIP) User Agent (UA) strings and UA types used in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-128"><a href="lync-server-2013-user-table.md">Lync Server 2013 の User テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-128"><a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-129">オーディオとビデオのセッションで使用されるユーザー、会議、および電話の Uri を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-129">Stores user, conference, and phone URIs used in audio and video sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-130"><a href="lync-server-2013-endpoint-table.md">Lync Server 2013 の Endpoint テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-130"><a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-131">オーディオとビデオのセッションに参加しているエンドポイントの FQDN コンピューター名を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-131">Stores FQDN computer names of endpoints participating in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-132"><a href="lync-server-2013-pool-table.md">Lync Server 2013 の Pool テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-132"><a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-133">メトリックデータが属するプールの名前が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-133">Stores the names of pools to which metrics data belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-134"><a href="lync-server-2013-device-table.md">Lync Server 2013 の Device テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-134"><a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-135">オーディオ/ビデオ通話で使用されるキャプチャデバイスとレンダリングデバイスを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-135">Stores capture devices and render devices which are used in an audio/video calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-136"><a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 の DeviceDriver テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-136"><a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-137">オーディオ/ビデオ通話で使用されるキャプチャデバイスとレンダリングデバイスのドライバーを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-137">Stores driver for the capture device and the render device which are used in audio/video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-138"><a href="lync-server-2013-conference-table.md">Lync Server 2013 の Conference テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-138"><a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-139">会議のシナリオの会議の Uri、または他のシナリオのために、電話会議の Uri を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-139">Stores Conference URIs for conference scenarios or DialogID for other scenarios.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-140"><a href="lync-server-2013-sessioncorrelation-table.md">Lync Server 2013 の SessionCorrelation テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-140"><a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-141">PSTN 通話の CorrelationID を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-141">Stores CorrelationID for PSTN calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-142"><a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 の PayloadDescription テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-142"><a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-143">音声/ビデオ通話で使用されるコーデックを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-143">Stores the Codec used in audio/video calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-144"><a href="lync-server-2013-appliedbandwidthsource-table.md">Lync Server 2013 の AppliedBandwidthSource テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-144"><a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-145">音声/ビデオ通話で使用される帯域幅のソースを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-145">Stores the bandwidth source used in audio/video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-146"><a href="lync-server-2013-macaddress-table.md">Lync Server 2013 の MacAddress テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-146"><a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-147">オーディオとビデオのセッションに参加しているエンドポイントの MAC アドレスが格納されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-147">Stores the MAC address of the endpoints participating in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-148"><a href="lync-server-2013-dialog-table.md">Lync Server 2013 の Dialog テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-148"><a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-149">オーディオセッションとビデオセッションのダイアログ ID を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-149">Stores the Dialog ID of audio and video sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-150"><a href="lync-server-2013-region-table.md">Lync Server 2013 の Region テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-150"><a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-151">NCS 設定で定義されたネットワーク領域を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-151">Stores the network region defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-152"><a href="lync-server-2013-usersite-table.md">Lync Server 2013 の UserSite テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-152"><a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-153">NCS 設定で定義されたネットワークサイトを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-153">Stores the network site defined in NCS setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-154"><a href="lync-server-2013-subnet-table.md">Lync Server 2013 の Subnet テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-154"><a href="lync-server-2013-subnet-table.md">Subnet table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-155">NCS 設定で定義されているサブネットを格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-155">Stores the subnet defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-156"><a href="lync-server-2013-monitoredregionlink-table.md">Lync Server 2013 の MonitoredRegionLink テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-156"><a href="lync-server-2013-monitoredregionlink-table.md">MonitoredRegionLink table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-157">NCS 設定で定義されている地域リンクを格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-157">Stores the region link defined in NCS setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-158"><a href="monitoredusersitelink-table.md">MonitoredUserSiteLink テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-158"><a href="monitoredusersitelink-table.md">MonitoredUserSiteLink table</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-159">NCS 設定で定義されたネットワークサイトリンクを格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-159">Stores the network site links defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-160"><a href="lync-server-2013-endpointsubnet-table.md">Lync Server 2013 の EndpointSubnet テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-160"><a href="lync-server-2013-endpointsubnet-table.md">EndpointSubnet table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-161">オーディオおよびビデオセッションに参加しているエンドポイントのサブネットを格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-161">Stores the subnet of the endpoint participating in an audio and video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-162"><a href="lync-server-2013-server-table.md">Lync Server 2013 のサーバー テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-162"><a href="lync-server-2013-server-table.md">Server table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-163">メディアが移動するサーバーの FQDN または IP アドレスが格納されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-163">Stores the FQDN or IP address of the server the media goes through.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea657-164">**指標データのテーブル**</span><span class="sxs-lookup"><span data-stu-id="ea657-164">**Tables for metrics data**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea657-165"><strong>テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-165"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="ea657-166"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-166"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea657-167"><a href="lync-server-2013-appsharingstream-table.md">Lync Server 2013 の AppSharingStream テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-167"><a href="lync-server-2013-appsharingstream-table.md">AppSharingStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-168">アプリケーション共有に使用されるネットワークストリームのエクスペリエンスメトリックの品質を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-168">Stores Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="ea657-169">アプリケーション共有に使用されるネットワークストリームのエクスペリエンスのメトリックの評価。</span><span class="sxs-lookup"><span data-stu-id="ea657-169">Quality of Experience metrics for the network streams used for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-170"><a href="lync-server-2013-session-table.md">Lync Server 2013 の Session テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-170"><a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-171">オーディオまたはオーディオ/ビデオセッションに関する全体的な情報を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-171">Stores overall information about an audio or audio/video session.</span></span> <span data-ttu-id="ea657-172">セッションは、2つのエンドポイント間のオーディオまたはビデオ SIP ダイアログとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-172">A session is defined as an audio or video SIP dialog between two endpoints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-173"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-173"><a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-174">セッション内の各メディアラインに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-174">Stores information about each media line in a session.</span></span> <span data-ttu-id="ea657-175">メディアラインは、1つ以上のオーディオストリームとビデオストリームのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="ea657-175">A media line is a collection of one or more audio and video streams.</span></span> <span data-ttu-id="ea657-176">通常、1つのメディアラインには、オーディオまたはビデオの2つのストリームがあります。</span><span class="sxs-lookup"><span data-stu-id="ea657-176">Typically, a single media line will have two streams, either audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-177"><a href="lync-server-2013-audiostream-table.md">Lync Server 2013 の AudioStream テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-177"><a href="lync-server-2013-audiostream-table.md">AudioStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-178">メディアラインの各オーディオストリームのオーディオメディア品質指標を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-178">Stores audio media quality metrics for each audio stream in the media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-179"><a href="lync-server-2013-audiosignal-table.md">Lync Server 2013 の AudioSignal テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-179"><a href="lync-server-2013-audiosignal-table.md">AudioSignal table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-180">メディアラインにオーディオメディアの品質指標を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-180">Stores audio media quality metrics in the media line.</span></span> <span data-ttu-id="ea657-181">これには、アコースティックエコーキャンセル (AEC) と自動ゲイン制御 (AGC) メトリックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ea657-181">This includes acoustic echo cancellation (AEC) and automatic gain control (AGC) metrics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-182"><a href="lync-server-2013-videostream-table.md">Lync Server 2013 の VideoStream テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-182"><a href="lync-server-2013-videostream-table.md">VideoStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-183">メディアラインの各オーディオストリームについて、ビデオメディアの品質指標を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea657-183">Stores video media quality metrics for each audio stream in the media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-184"><a href="lync-server-2013-audioclientevent-table.md">Lync Server 2013 の AudioClientEvent テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-184"><a href="lync-server-2013-audioclientevent-table.md">AudioClientEvent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-185">クライアントイベントから収集されたオーディオメディア品質指標を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-185">Stores audio media quality metrics collected from the client event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-186"><a href="lync-server-2013-videoclientevent-table.md">Lync Server 2013 の VideoClientEvent テーブル</a></span><span class="sxs-lookup"><span data-stu-id="ea657-186"><a href="lync-server-2013-videoclientevent-table.md">VideoClientEvent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="ea657-187">クライアントイベントから収集されたビデオメディア品質指標を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-187">Stores video media quality metrics collected from the client event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-188"><strong>DiagnosticData テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-188"><strong>DiagnosticData Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-189">内部でのみ使用する診断データを格納します。</span><span class="sxs-lookup"><span data-stu-id="ea657-189">Stores diagnostic data which is for internal use only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea657-190">**集計データのテーブル**</span><span class="sxs-lookup"><span data-stu-id="ea657-190">**Tables for summary data**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea657-191"><strong>テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-191"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="ea657-192"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-192"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea657-193"><strong>ServerSummary テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-193"><strong>ServerSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-194">サーバーの概要データを保存します。これらのデータは、Quality of Experience (QoE) レポートのみに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-194">Stores summary data for the servers, these data is used for Quality of Experience (QoE) reporting only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-195"><strong>UserSummary テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-195"><strong>UserSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-196">ユーザーの概要データが保存されます。これらのデータは QoE レポート専用に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-196">Stores summary data for users, these data is used for QoE reporting only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-197"><strong>CallTypeSummary テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-197"><strong>CallTypeSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-198">このデータは、通話の種類の概要データを保存するために、QoE レポート専用に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea657-198">Store summary data for call types, these data is used for QoE reporting only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea657-199">**監視サーバーによる内部使用のテーブル**</span><span class="sxs-lookup"><span data-stu-id="ea657-199">**Tables for Internal Use by Monitoring Server**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea657-200"><strong>テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-200"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="ea657-201"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-201"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea657-202"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-202"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-203">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-203">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-204"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-204"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-205">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-205">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-206"><strong>フロントエンドテーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-206"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-207">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-207">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-208"><strong>タスクテーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-208"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-209">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-209">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-210"><strong>概要 tabltabl</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-210"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-211">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-211">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-212"><strong>DbErrorMessage</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-212"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-213">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-213">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-214"><strong>MetricsThreshold</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-214"><strong>MetricsThreshold</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-215">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-215">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-216"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-216"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-217">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-217">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-218"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-218"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-219">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-219">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-220"><strong>タイム</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-220"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-221">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-221">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-222"><strong>CallSummary の表</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-222"><strong>CallSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-223">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-223">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-224"><strong>DeviceCallSumary のテーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-224"><strong>DeviceCallSumary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-225">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-225">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-226"><strong>テナントテーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-226"><strong>Tenant Table</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-227">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-227">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea657-228"><strong>VideoCallSummaryTable</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-228"><strong>VideoCallSummaryTable</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-229">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-229">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea657-230"><strong>Ascall概要テーブル</strong></span><span class="sxs-lookup"><span data-stu-id="ea657-230"><strong>ASCallSummaryTable</strong></span></span></p></td>
<td><p><span data-ttu-id="ea657-231">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="ea657-231">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ea657-232">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea657-232">


</div>

<span> </span>

</div>

</div>

</span></span></div>

