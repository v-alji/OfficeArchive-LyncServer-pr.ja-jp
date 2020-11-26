---
title: 'Lync Server 2013: ポートの概要 - リバース プロキシ'
description: 'Lync Server 2013: ポートの概要-リバースプロキシ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Reverse proxy
ms:assetid: 59b9ac3c-3e6f-4776-b366-174f0dd1f2eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204932(v=OCS.15)
ms:contentKeyID: 48184251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf07800c91f5a28165eb05e14e2d775758460f50
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442811"
---
# <a name="port-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="8b712-103">ポートの概要 - Lync Server 2013 のリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="8b712-103">Port summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b712-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b712-104">

<span> </span></span></span>

<span data-ttu-id="8b712-105">_**最終更新日:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="8b712-105">_**Topic Last Modified:** 2013-02-15_</span></span>

<span data-ttu-id="8b712-106">リバースプロキシには、ファイアウォールとポート/プロトコルの最小要件があります。</span><span class="sxs-lookup"><span data-stu-id="8b712-106">The reverse proxy has minimal requirements for firewall and port/protocol.</span></span>

  - <span data-ttu-id="8b712-107">外部ファイアウォールの要件として、HTTPS/TCP/443 と、オプションの HTTP/TCP/80 が挙げられます。</span><span class="sxs-lookup"><span data-stu-id="8b712-107">External firewall requirements are the HTTPS/TCP/443 and the optional HTTP/TCP/80.</span></span> <span data-ttu-id="8b712-108">HTTPS は、SSL と TLS のセキュリティ保護された通信に、リバースプロキシ経由で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b712-108">HTTPS is used for SSL and TLS secure communications through the reverse proxy.</span></span> <span data-ttu-id="8b712-109">証明書を変更するときに、自動検出サービスへのアクセスを許可することを選んだ場合、HTTP が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b712-109">HTTP is used if you choose to allow access to the Autodiscover Service when modifying certificates might prove difficult or not cost justified.</span></span>

  - <span data-ttu-id="8b712-110">クライアントは、HTTPS で Office Web Apps サーバーに連絡することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="8b712-110">Clients expect to contact the Office Web Apps Server on HTTPS.</span></span> <span data-ttu-id="8b712-111">Office Web Apps サーバーは、HTTPS/TCP/443 上の内部クライアントからの通信を想定しています。</span><span class="sxs-lookup"><span data-stu-id="8b712-111">The Office Web Apps Server expects communication from internal clients on HTTPS/TCP/443.</span></span> <span data-ttu-id="8b712-112">推奨される構成では、リバースプロキシから Office Web Apps サーバーへの HTTPS/TCP/443 の使用を許可します。</span><span class="sxs-lookup"><span data-stu-id="8b712-112">The recommended configuration is to allow HTTPS/TCP/443 from the reverse proxy to the Office Web Apps Server.</span></span>

  - <span data-ttu-id="8b712-113">ポート8080は、リバースプロキシの内部インターフェイスからフロントエンドサーバー、フロントエンドプール仮想 IP (VIP)、またはオプションのディレクターまたはディレクタープール VIP にトラフィックをルーティングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b712-113">Port 8080 is used to route traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP.</span></span> <span data-ttu-id="8b712-114">ポート TCP 8080 は、Lync を実行しているモバイルデバイスで、自動検出サービスを検索するために必要です (たとえば、多数の SIP ドメインがある場合など)。</span><span class="sxs-lookup"><span data-stu-id="8b712-114">Port TCP 8080 is required for mobile devices running Lync to locate the Autodiscover Service in situations where modifying the external web service publishing rule certificate is undesirable (for example, if you have a large number of SIP domains).</span></span> <span data-ttu-id="8b712-115">必要な SAN エントリを使用して新しい証明書を取得する場合、ポート TCP 8080 は不要であり、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8b712-115">If you choose to acquire new certificates with the necessary SAN entries, the port TCP 8080 is not needed and is optional.</span></span>

  - <span data-ttu-id="8b712-116">ポート4443は、リバースプロキシ内部インターフェイスからフロントエンドサーバー、フロントエンドプール仮想 IP (VIP)、またはオプションのディレクターまたはディレクタープール VIP へのトラフィックに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b712-116">Port 4443 is used for traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP</span></span>
    
    <span data-ttu-id="8b712-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span><span class="sxs-lookup"><span data-stu-id="8b712-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span></span>  
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8b712-118">4443とリバースプロキシの間の TCP トラフィックを、標準エディションサーバーまたは全体管理ストアの役割を管理するフロントエンドプールの内部4443展開に混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="8b712-118">Do not confuse the 4443 over TCP from the reverse proxy to the internal deployment for the port 4443 over TCP traffic from the Standard Edition server or the Front End pool that manages the Central Management store role.</span></span>

    
    </div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="8b712-119">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="8b712-119">Port and Protocol Details</span></span>

### <a name="firewall-details-for-reverse-proxy-server-external-interface"></a><span data-ttu-id="8b712-120">リバースプロキシサーバーのファイアウォールの詳細: 外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8b712-120">Firewall Details for Reverse Proxy Server: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b712-121">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="8b712-121">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8b712-122">ソース IP アドレス</span><span class="sxs-lookup"><span data-stu-id="8b712-122">Source IP Address</span></span></th>
<th><span data-ttu-id="8b712-123">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="8b712-123">Destination IP Address</span></span></th>
<th><span data-ttu-id="8b712-124">メモ</span><span class="sxs-lookup"><span data-stu-id="8b712-124">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b712-125">HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="8b712-125">HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="8b712-126">任意</span><span class="sxs-lookup"><span data-stu-id="8b712-126">Any</span></span></p></td>
<td><p><span data-ttu-id="8b712-127">リバースプロキシリスナー</span><span class="sxs-lookup"><span data-stu-id="8b712-127">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="8b712-128">省略ユーザーが http://publishedsitefqdn を入力した場合に HTTPS にリダイレクト &lt; &gt; します。</span><span class="sxs-lookup"><span data-stu-id="8b712-128">(Optional) Redirection to HTTPS if user enters http://&lt;publishedSiteFQDN&gt;.</span></span></p>
<p><span data-ttu-id="8b712-129">また、会議用の Office Web Apps および Lync を実行しているモバイルデバイスで、組織が外部 Web サービス公開ルールの証明書を変更しない場合には、自動検出サービスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b712-129">Also required if using Office Web Apps for conferencing and the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b712-130">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="8b712-130">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8b712-131">任意</span><span class="sxs-lookup"><span data-stu-id="8b712-131">Any</span></span></p></td>
<td><p><span data-ttu-id="8b712-132">リバースプロキシリスナー</span><span class="sxs-lookup"><span data-stu-id="8b712-132">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="8b712-133">アドレス帳のダウンロード、アドレス帳 Web クエリサービス、自動検出、クライアント更新、会議コンテンツ、デバイス更新プログラム、グループ拡張、会議用の Office Web アプリ、ダイヤルイン会議、会議。</span><span class="sxs-lookup"><span data-stu-id="8b712-133">Address book downloads, Address Book Web Query service, Autodiscover, client updates, meeting content, device updates, group expansion, Office Web Apps for conferencing, dial-in conferencing, and meetings.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-details-for-reverse-proxy-server-internal-interface"></a><span data-ttu-id="8b712-134">リバースプロキシサーバーのファイアウォールの詳細: 内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8b712-134">Firewall Details for Reverse Proxy Server: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b712-135">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="8b712-135">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8b712-136">ソース IP アドレス</span><span class="sxs-lookup"><span data-stu-id="8b712-136">Source IP Address</span></span></th>
<th><span data-ttu-id="8b712-137">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="8b712-137">Destination IP Address</span></span></th>
<th><span data-ttu-id="8b712-138">メモ</span><span class="sxs-lookup"><span data-stu-id="8b712-138">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b712-139">HTTP/TCP/8080</span><span class="sxs-lookup"><span data-stu-id="8b712-139">HTTP/TCP/8080</span></span></p></td>
<td><p><span data-ttu-id="8b712-140">内部のリバースプロキシインターフェイス</span><span class="sxs-lookup"><span data-stu-id="8b712-140">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="8b712-141">フロントエンドサーバー、フロントエンドプール、ディレクター、ディレクタープール</span><span class="sxs-lookup"><span data-stu-id="8b712-141">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="8b712-142">組織で外部 web サービス公開ルールの証明書を変更しない場合に、Lync を実行しているモバイルデバイスで自動検出サービスを使用する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="8b712-142">Required if using the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p>
<p><span data-ttu-id="8b712-143">リバースプロキシの外部インターフェイスでポート80に送信されるトラフィックは、プール Web サービスが内部の web トラフィックと区別できるように、リバースプロキシの内部インターフェイスからポート8080上のプールにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="8b712-143">Traffic sent to port 80 on the reverse proxy external interface is redirected to a pool on port 8080 from the reverse proxy internal interface so that the pool Web Services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b712-144">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="8b712-144">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="8b712-145">内部のリバースプロキシインターフェイス</span><span class="sxs-lookup"><span data-stu-id="8b712-145">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="8b712-146">フロントエンドサーバー、フロントエンドプール、ディレクター、ディレクタープール</span><span class="sxs-lookup"><span data-stu-id="8b712-146">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="8b712-147">リバースプロキシの外部インターフェイスでポート443に送信されるトラフィックは、プール web サービスが内部の web トラフィックと区別できるように、リバースプロキシの内部インターフェイスからポート4443上のプールにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="8b712-147">Traffic sent to port 443 on the reverse proxy external interface is redirected to a pool on port 4443 from the reverse proxy internal interface so that the pool web services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b712-148">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="8b712-148">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8b712-149">内部のリバースプロキシインターフェイス</span><span class="sxs-lookup"><span data-stu-id="8b712-149">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="8b712-150">会議用の Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="8b712-150">Office Web Apps for conferencing</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="8b712-151">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b712-151">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

