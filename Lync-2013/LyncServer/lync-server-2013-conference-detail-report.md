---
title: 'Lync Server 2013: 会議の詳細レポート'
description: 'Lync Server 2013: 会議の詳細レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398517"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="6451d-103">Lync Server 2013 の会議の詳細レポート</span><span class="sxs-lookup"><span data-stu-id="6451d-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6451d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6451d-104">

<span> </span></span></span>

<span data-ttu-id="6451d-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="6451d-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="6451d-p101">会議詳細レポートには、電話会議に参加したすべてのユーザーに関する詳細な情報が示されます。たとえば、ユーザーが会議に参加した日時、ユーザーが電話会議から退場した日時、ユーザーが電話会議に接続するときに使用したエンドポイントのユーザー エージェントなどの情報を確認できます。各電話会議におけるユーザーの役割 (発表者、参加者など) に関する情報も確認できます。おそらく最も重要なことは、会議への参加と終了が正常に行われたユーザーと正常に行われなかったユーザーを簡単に確認できることです。</span><span class="sxs-lookup"><span data-stu-id="6451d-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="6451d-110">会議詳細レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="6451d-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="6451d-111">会議詳細レポートには、次のレポートからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6451d-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="6451d-112">[Lync Server 2013 の通話受付制御レポート](lync-server-2013-call-admission-control-report.md)(会議の詳細な指標をクリック)</span><span class="sxs-lookup"><span data-stu-id="6451d-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="6451d-113">[Lync Server 2013 の [エラー一覧] レポート](lync-server-2013-failure-list-report.md)(会議のメトリックをクリック)</span><span class="sxs-lookup"><span data-stu-id="6451d-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="6451d-114">[Lync Server 2013 のユーザーアクティビティレポート](lync-server-2013-user-activity-report.md)(会議 URI メトリックをクリック)</span><span class="sxs-lookup"><span data-stu-id="6451d-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="6451d-115">[会議の詳細] レポートから、 [Lync Server 2013 で](lync-server-2013-diagnostic-report.md) 診断レポート (詳細) メトリックをクリックすると、診断レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6451d-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="6451d-116">フィルター</span><span class="sxs-lookup"><span data-stu-id="6451d-116">Filters</span></span>

<span data-ttu-id="6451d-p102">なし。会議詳細レポートにはフィルターを適用できません。</span><span class="sxs-lookup"><span data-stu-id="6451d-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="6451d-119">指標</span><span class="sxs-lookup"><span data-stu-id="6451d-119">Metrics</span></span>

<span data-ttu-id="6451d-120">次の表は、会議詳細レポートの [電話会議情報] セクションに提供される情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="6451d-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="6451d-121">電話会議情報の指標</span><span class="sxs-lookup"><span data-stu-id="6451d-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6451d-122">名前</span><span class="sxs-lookup"><span data-stu-id="6451d-122">Name</span></span></th>
<th><span data-ttu-id="6451d-123">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="6451d-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6451d-124">説明</span><span class="sxs-lookup"><span data-stu-id="6451d-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6451d-125"><strong>[会議 URI]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-p103">電話会議に割り当てられる URI。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6451d-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="6451d-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="6451d-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-129"><strong>[プールの FQDN]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-130">セッションに関係するレジストラー プールまたはエッジ サーバーの完全修飾名。</span><span class="sxs-lookup"><span data-stu-id="6451d-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-131"><strong>[開始時刻]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-132">会議が開始した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-133"><strong>[開催者]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-134">会議を開催したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="6451d-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-135"><strong>[終了時刻]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-136">会議が終了した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6451d-137">次の表は、会議詳細レポートの [電話会議の参加] セクションに提供される情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="6451d-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="6451d-138">電話会議参加の指標</span><span class="sxs-lookup"><span data-stu-id="6451d-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6451d-139">名前</span><span class="sxs-lookup"><span data-stu-id="6451d-139">Name</span></span></th>
<th><span data-ttu-id="6451d-140">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="6451d-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6451d-141">説明</span><span class="sxs-lookup"><span data-stu-id="6451d-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6451d-142"><strong>[ユーザー]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-143">会議に参加したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="6451d-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-144"><strong>[役割]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-145">電話会議の参加者が担った役割 (発表者など)。</span><span class="sxs-lookup"><span data-stu-id="6451d-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-146"><strong>[接続]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-147">参加者のネットワーク接続 (一般には内部送信元または外部送信元)。</span><span class="sxs-lookup"><span data-stu-id="6451d-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-148">[参加時間]</span><span class="sxs-lookup"><span data-stu-id="6451d-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-149">参加者が電話会議に参加した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-150"><strong>[退場時間]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-151">参加者が電話会議から退出した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-152"><strong>[ユーザー エージェント]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-153">参観者のエンドポイントで使用されるソフトウェアの識別子。</span><span class="sxs-lookup"><span data-stu-id="6451d-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-154"><strong>[診断レポート]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-p104">診断およびトラブルシューティングの情報を提供します。失敗したセッションの SIP 応答コード、診断ヘッダー、電話会議参加時間、診断 ID などがあります。</span><span class="sxs-lookup"><span data-stu-id="6451d-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6451d-157">次の表に、会議の詳細レポートの [会議のモダリティ] セクションに表示される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="6451d-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="6451d-158">電話会議のモダリティの指標</span><span class="sxs-lookup"><span data-stu-id="6451d-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6451d-159">名前</span><span class="sxs-lookup"><span data-stu-id="6451d-159">Name</span></span></th>
<th><span data-ttu-id="6451d-160">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="6451d-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6451d-161">説明</span><span class="sxs-lookup"><span data-stu-id="6451d-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6451d-162"><strong>[ユーザー]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-163">会議に参加したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="6451d-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-164"><strong>[参加時間]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-165">参加者が電話会議に参加した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-166"><strong>[退場時間]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-167">参加者が電話会議を退場した日時。</span><span class="sxs-lookup"><span data-stu-id="6451d-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6451d-168"><strong>[電話会議サーバー URI]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-169">電話会議で使用された電話会議サーバーの URI。</span><span class="sxs-lookup"><span data-stu-id="6451d-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6451d-170"><strong>[診断レポート]</strong></span><span class="sxs-lookup"><span data-stu-id="6451d-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6451d-p105">診断およびトラブルシューティングの情報を提供します。失敗したセッションの SIP 応答コード、診断ヘッダー、電話会議参加時間、診断 ID などがあります。</span><span class="sxs-lookup"><span data-stu-id="6451d-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6451d-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6451d-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

