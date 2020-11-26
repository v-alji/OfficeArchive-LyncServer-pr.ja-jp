---
title: 'Lync Server 2013: 証明書の概要 - リバース プロキシ'
description: 'Lync Server 2013: 証明書の概要-リバースプロキシ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Reverse proxy
ms:assetid: f2b9a53f-aead-413d-81e9-4a294a010fbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205381(v=OCS.15)
ms:contentKeyID: 48185820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cc250d6de2eb1a0b6c3ad3495c8df62942f9a81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435280"
---
# <a name="certificate-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="86cd0-103">証明書の概要 - Lync Server 2013 リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="86cd0-103">Certificate summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86cd0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86cd0-104">

<span> </span></span></span>

<span data-ttu-id="86cd0-105">_**最終更新日:** 2012-11-14_</span><span class="sxs-lookup"><span data-stu-id="86cd0-105">_**Topic Last Modified:** 2012-11-14_</span></span>

<span data-ttu-id="86cd0-106">リバースプロキシの証明書の要件は、エッジサーバーよりもずっと簡単です。</span><span class="sxs-lookup"><span data-stu-id="86cd0-106">Certificate requirements for the reverse proxy are much simpler than that for the Edge Servers.</span></span> <span data-ttu-id="86cd0-107">提供されたフローチャートは、必要な要件を示します。</span><span class="sxs-lookup"><span data-stu-id="86cd0-107">The provided flowchart presents the requirements necessary.</span></span> <span data-ttu-id="86cd0-108">この表に示すのは、microsoft が Edge Server のディスカッションでレビューしたシナリオに関連する、一般的な証明書のサブジェクト名とサブジェクトの別名を示しています。</span><span class="sxs-lookup"><span data-stu-id="86cd0-108">The accompanying table presents typical certificate subject name and subject alternative names in relation to the scenarios that we have been reviewed in the Edge Server discussions.</span></span> <span data-ttu-id="86cd0-109">エッジサーバーのシナリオについて詳しくは、「 [Lync server 2013 での外部ユーザーアクセスのシナリオ](lync-server-2013-scenarios-for-external-user-access.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="86cd0-109">For more details on the Edge Server scenarios, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="86cd0-110">**リバースプロキシ用の証明書フローチャート**</span><span class="sxs-lookup"><span data-stu-id="86cd0-110">**Certificates Flow Chart for Reverse Proxy**</span></span>

<span data-ttu-id="86cd0-111">![エッジ サーバー用の証明書のフロー チャート](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "エッジ サーバー用の証明書のフロー チャート")</span><span class="sxs-lookup"><span data-stu-id="86cd0-111">![Certificates Flow Chart for Edge Server](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Certificates Flow Chart for Edge Server")</span></span>

### <a name="reverse-proxy-external-interface"></a><span data-ttu-id="86cd0-112">リバースプロキシ: 外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="86cd0-112">Reverse Proxy: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86cd0-113">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86cd0-113">Component</span></span></th>
<th><span data-ttu-id="86cd0-114">サブジェクト名</span><span class="sxs-lookup"><span data-stu-id="86cd0-114">Subject name</span></span></th>
<th><span data-ttu-id="86cd0-115">サブジェクト代替名 (SAN) の/Order</span><span class="sxs-lookup"><span data-stu-id="86cd0-115">Subject alternative name (SAN)/Order</span></span></th>
<th><span data-ttu-id="86cd0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="86cd0-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86cd0-117">リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="86cd0-117">Reverse Proxy</span></span></p></td>
<td><p><span data-ttu-id="86cd0-118">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-118">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="86cd0-119">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-119">webext.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-120">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-120">webdirext.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-121">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-121">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-122">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-122">meet.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-123">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-123">officewebapps01.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-124">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-124">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="86cd0-125">(省略可能):\* contoso.com</span><span class="sxs-lookup"><span data-stu-id="86cd0-125">(Optional):\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="86cd0-126">証明書は、公開 CA とサーバー EKU によって発行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cd0-126">Certificate must be issued by a public CA and with the server EKU.</span></span> <span data-ttu-id="86cd0-127">サービスには、アドレス帳サービス、配布グループ展開会議用 Office Web Apps、Lync IP デバイス発行ルールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="86cd0-127">Services include Address Book Service, distribution group expansion Office Web Apps for conferencing, and Lync IP Device publishing rules.</span></span> <span data-ttu-id="86cd0-128">サブジェクトの代替名には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="86cd0-128">Subject alternative name includes:</span></span></p>
<ul>
<li><p><span data-ttu-id="86cd0-129">フロントエンドサーバーまたはフロントエンドプール用の外部 Web サービス FQDN</span><span class="sxs-lookup"><span data-stu-id="86cd0-129">External Web Services FQDN for Front End Server or Front End pool</span></span></p></li>
<li><p><span data-ttu-id="86cd0-130">ディレクターまたはディレクタープール用の外部 Web サービス FQDN</span><span class="sxs-lookup"><span data-stu-id="86cd0-130">External Web Services FQDN for Director or Director pool</span></span></p></li>
<li><p><span data-ttu-id="86cd0-131">ダイヤルイン会議</span><span class="sxs-lookup"><span data-stu-id="86cd0-131">Dial-in conferencing</span></span></p></li>
<li><p><span data-ttu-id="86cd0-132">オンライン会議の公開ルール</span><span class="sxs-lookup"><span data-stu-id="86cd0-132">Online meeting publishing rule</span></span></p></li>
<li><p><span data-ttu-id="86cd0-133">会議用の Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="86cd0-133">Office Web Apps for conferencing</span></span></p></li>
<li><p><span data-ttu-id="86cd0-134">Lyncdiscover (自動検出)</span><span class="sxs-lookup"><span data-stu-id="86cd0-134">Lyncdiscover (Autodiscover)</span></span></p></li>
</ul>
<p><span data-ttu-id="86cd0-135">会議の開始とダイヤルインの両方のオプションワイルドカード</span><span class="sxs-lookup"><span data-stu-id="86cd0-135">The optional wildcard replaces both meet and dialin SAN</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="86cd0-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86cd0-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

