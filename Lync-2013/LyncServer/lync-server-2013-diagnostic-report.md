---
title: 'Lync Server 2013: 診断レポート'
description: 'Lync Server 2013: 診断レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Diagnostic Report
ms:assetid: b389dbd9-f2e8-4184-93d0-2e504796ac16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615445(v=OCS.15)
ms:contentKeyID: 48185159
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 198b836437285b464ba9172e59c9a60ed0a53b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429305"
---
# <a name="diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="45ed2-103">Lync Server 2013 の診断レポート</span><span class="sxs-lookup"><span data-stu-id="45ed2-103">Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45ed2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45ed2-104">

<span> </span></span></span>

<span data-ttu-id="45ed2-105">_**最終更新日:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="45ed2-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="45ed2-106">診断レポートは、失敗したセッションの診断とトラブルシューティングに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="45ed2-106">The Diagnostic Report provides diagnostic and troubleshooting information for a failed session.</span></span> <span data-ttu-id="45ed2-107">この情報には、診断 ID と、セッションが失敗したときに報告された診断ヘッダーの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="45ed2-107">This information includes both the Diagnostic ID and the Diagnostic header that were reported when the session failed.</span></span> <span data-ttu-id="45ed2-108">診断 ID は、SIP メッセージに添付される一意の識別子 (ms diagnostics ヘッダーの形式) ですが、診断ヘッダーには診断 ID の説明が示されます。</span><span class="sxs-lookup"><span data-stu-id="45ed2-108">The Diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) that gets attached to a SIP message, while the Diagnostic header provides an accompanying description for the Diagnostic ID.</span></span> <span data-ttu-id="45ed2-109">レポートには、レポートコンポーネントによって認識される貴重なトラブルシューティングの詳細情報が含まれている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="45ed2-109">The report might also contain valuable troubleshooting details that are known by the reporting component.</span></span> <span data-ttu-id="45ed2-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="45ed2-110">For example:</span></span>

  - <span data-ttu-id="45ed2-p102">エラーを生成した PSTN ゲートウェイによって提供された原因コード。発信通話が PSTN ネットワークで失敗すると、ISDN User Part (ISUP) の原因コードが自動的に生成されます。たとえば、PSTN ゲートウェイは原因コード 34 を送信して、通話を完了するための使用可能な回線またはチャネルが存在しないことを示す場合があります。</span><span class="sxs-lookup"><span data-stu-id="45ed2-p102">The cause code provided by the PSTN gateway that generated the failure. When an outgoing call fails on the PSTN network, an ISDN User Part (ISUP) cause code is automatically generated. For example, a PSTN gateway might send cause code 34 to indicate that no circuit or channel was available for completing the call.</span></span>

  - <span data-ttu-id="45ed2-114">接続エラーのピア FQDN、ポート、および Winsock エラー。</span><span class="sxs-lookup"><span data-stu-id="45ed2-114">Peer FQDN, port, and Winsock errors for connectivity failures.</span></span>

  - <span data-ttu-id="45ed2-p103">DNS 解決エラーで検索されている名前。DNS 解決は、クライアントがネーム サーバーに問い合わせ、指定されたデバイス名に対応する IP アドレスを要求するときにいつでも実行されます。</span><span class="sxs-lookup"><span data-stu-id="45ed2-p103">Names being looked up for DNS resolution failures. DNS resolution takes place any time a client contacts a name server and requests the IP address that corresponds to specified device name.</span></span>

<div>

## <a name="accessing-the-diagnostic-report"></a><span data-ttu-id="45ed2-117">診断レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="45ed2-117">Accessing the Diagnostic Report</span></span>

<span data-ttu-id="45ed2-118">診断レポートにアクセスするには、Lync Server 2013 または [会議の詳細] レポートの [ピアツーピアセッションの詳細レポート](lync-server-2013-peer-to-peer-session-detail-report.md) で診断レポート (詳細) のメトリックをクリックします。</span><span class="sxs-lookup"><span data-stu-id="45ed2-118">The Diagnostic Report can be accessed by clicking the Diagnostic Report (Detail) metric on either the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) or the Conference Detail Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="45ed2-119">フィルター</span><span class="sxs-lookup"><span data-stu-id="45ed2-119">Filters</span></span>

<span data-ttu-id="45ed2-p104">なし。診断レポートにフィルターを適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="45ed2-p104">None. You cannot filter the Diagnostic Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="45ed2-122">指標</span><span class="sxs-lookup"><span data-stu-id="45ed2-122">Metrics</span></span>

<span data-ttu-id="45ed2-123">次の表に、診断レポートで提供されるセッションごとの情報を示します。</span><span class="sxs-lookup"><span data-stu-id="45ed2-123">The following table lists the information provided in the Diagnostic Report for each session.</span></span>

### <a name="diagnostic-report-metrics"></a><span data-ttu-id="45ed2-124">診断レポートの指標</span><span class="sxs-lookup"><span data-stu-id="45ed2-124">Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45ed2-125">名前</span><span class="sxs-lookup"><span data-stu-id="45ed2-125">Name</span></span></th>
<th><span data-ttu-id="45ed2-126">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="45ed2-126">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="45ed2-127">説明</span><span class="sxs-lookup"><span data-stu-id="45ed2-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-128"><strong>レポート時刻</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-128"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-129">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-129">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-130">レポートが記録された日時。</span><span class="sxs-lookup"><span data-stu-id="45ed2-130">Date and time that the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-131"><strong>応答コード</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-131"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-132">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-132">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-133">セッションが失敗したときに送信された SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="45ed2-133">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-134"><strong>要求の種類</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-134"><strong>Request type</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-135">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-135">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-p105">失敗した SIP 要求の種類 (INVITE、BYE、SERVICE など)。</span><span class="sxs-lookup"><span data-stu-id="45ed2-p105">SIP request type that failed. For example, INVITE, BYE, or SERVICE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-138"><strong>ソース</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-138"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-139">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-139">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-140">エラーのソース。</span><span class="sxs-lookup"><span data-stu-id="45ed2-140">Source of the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-141"><strong>送信元ユーザー URI</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-141"><strong>From user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-142">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-142">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-143">セッションを開始したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="45ed2-143">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-144"><strong>送信元ユーザー エージェント</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-144"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-145">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-145">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-146">セッションを開始したユーザーのエンドポイントで使用されているソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="45ed2-146">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-147"><strong>診断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-147"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-148">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-148">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-149">SIP メッセージに (ms-diagnostics ヘッダーの形で) 添付された一意の識別子。多くの場合、この情報はトラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45ed2-149">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-150"><strong>コンテンツの種類</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-150"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-151">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-151">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-p106">失敗したメディア コンテンツの種類。たとえば、よく使われるコンテンツの種類は Application/sdp です。セッション記述プロトコル (SDP) は、セッションのアナウンス、セッションの招待、その他のマルチメディア セッション開始形式で使われる標準インターネット プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="45ed2-p106">Type of media content that failed. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-155"><strong>アプリケーション</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-155"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-156">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-156">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-157">エラーに関係するアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="45ed2-157">Application involved in the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-158"><strong>送信先ユーザー URI</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-158"><strong>To user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-159">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-159">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-160">セッションに招待されたユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="45ed2-160">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45ed2-161">会議参加時間 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="45ed2-161">Conference join times (ms)</span></span></p></td>
<td><p><span data-ttu-id="45ed2-162">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-162">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-163">ユーザーが会議に参加するのにかかった時間 (ミリ秒)。</span><span class="sxs-lookup"><span data-stu-id="45ed2-163">Amount of time (in milliseconds) it took for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ed2-164"><strong>診断ヘッダー</strong></span><span class="sxs-lookup"><span data-stu-id="45ed2-164"><strong>Diagnostic header</strong></span></span></p></td>
<td><p><span data-ttu-id="45ed2-165">不可</span><span class="sxs-lookup"><span data-stu-id="45ed2-165">No</span></span></p></td>
<td><p><span data-ttu-id="45ed2-166">診断 ID の説明。</span><span class="sxs-lookup"><span data-stu-id="45ed2-166">Diagnostic ID description.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45ed2-167">診断エラーの一覧は、[ [Ms 診断ヘッダー] ページ](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx)にあります。</span><span class="sxs-lookup"><span data-stu-id="45ed2-167">A list of diagnostic errors can be found on the [Ms-Diagnostics Header page](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span></span>

<span data-ttu-id="45ed2-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45ed2-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

