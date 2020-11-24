---
title: 'Lync Server 2013: Standard Edition サーバーの DNS 要件'
description: 'Lync Server 2013: Standard Edition サーバーの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398186"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="bd232-103">Lync Server 2013 での Standard Edition サーバーの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="bd232-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd232-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd232-104">

<span> </span></span></span>

<span data-ttu-id="bd232-105">_**最終更新日:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="bd232-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="bd232-106">このセクションでは、Standard Edition サーバーの展開に必要なドメインネームシステム (DNS) レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bd232-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="bd232-107">Standard Edition サーバーの DNS レコード</span><span class="sxs-lookup"><span data-stu-id="bd232-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="bd232-108">次の表では、Lync Server 2013 Standard Edition server の展開の DNS 要件を示します。</span><span class="sxs-lookup"><span data-stu-id="bd232-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="bd232-109">Standard Edition Server の DNS 要件</span><span class="sxs-lookup"><span data-stu-id="bd232-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd232-110">展開シナリオ</span><span class="sxs-lookup"><span data-stu-id="bd232-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="bd232-111">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="bd232-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd232-112">Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="bd232-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="bd232-113">内部の A レコード。サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決します。</span><span class="sxs-lookup"><span data-stu-id="bd232-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd232-114">自動クライアントサインイン</span><span class="sxs-lookup"><span data-stu-id="bd232-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="bd232-115">サポートされている各 SIP ドメインについて、_sipinternaltls _tcp の SRV レコード&gt;サインインのためのクライアント要求を認証してリダイレクトする標準エディションサーバーの FQDN にマップされる、ポート5061経由のドメイン。</span><span class="sxs-lookup"><span data-stu-id="bd232-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="bd232-116">詳細については、「 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013 での自動クライアントサインインの DNS 要件</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd232-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd232-117">ユニファイドコミュニケーション (UC) デバイスによるデバイス更新 Web サービスの検出</span><span class="sxs-lookup"><span data-stu-id="bd232-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="bd232-118">"Ucupdates-r2" という名前の内部 A レコード。 &lt;&gt;デバイス更新 Web サービスをホストしている Standard Edition サーバーの IP アドレスに解決される SIP ドメイン。</span><span class="sxs-lookup"><span data-stu-id="bd232-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="bd232-119">UC デバイスが有効になっている状態で、ユーザーがデバイスにログインしたことがない場合、A レコードによってデバイス更新 Web サービスをホストするサーバーがデバイスで検出され、更新プログラムが取得されます。</span><span class="sxs-lookup"><span data-stu-id="bd232-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="bd232-120">そうしないと、デバイスは、ユーザーが初めてログインしたときに、インバンドプロビジョニングでサーバー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="bd232-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd232-121">HTTP トラフィックをサポートする逆プロキシ</span><span class="sxs-lookup"><span data-stu-id="bd232-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="bd232-122">外部の web ファーム FQDN をリバースプロキシの外部 IP アドレスに解決する外部の A レコード。</span><span class="sxs-lookup"><span data-stu-id="bd232-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="bd232-123">クライアントと UC デバイスこのレコードを使ってリバースプロキシに接続します。</span><span class="sxs-lookup"><span data-stu-id="bd232-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="bd232-124">詳細については、「計画ドキュメントの「 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013 の DNS 要件を決定</a> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd232-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bd232-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd232-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

