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
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="e202e-103">Lync Server 2013 の Standard Edition サーバーの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="e202e-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e202e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e202e-104">

<span> </span></span></span>

<span data-ttu-id="e202e-105">_**トピック最終更新日:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="e202e-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="e202e-106">ここでは、Standard Edition サーバーの展開に必要なドメイン ネーム システム (DNS) レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e202e-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="e202e-107">Standard Edition Servers の DNS レコード</span><span class="sxs-lookup"><span data-stu-id="e202e-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="e202e-108">次の表は、Lync Server 2013 Standard Edition サーバー展開の DNS 要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="e202e-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="e202e-109">Standard Edition Server の DNS 要件</span><span class="sxs-lookup"><span data-stu-id="e202e-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e202e-110">展開シナリオ</span><span class="sxs-lookup"><span data-stu-id="e202e-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="e202e-111">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="e202e-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e202e-112">Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="e202e-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="e202e-113">サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決する内部 A レコード。</span><span class="sxs-lookup"><span data-stu-id="e202e-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e202e-114">クライアントの自動サインイン</span><span class="sxs-lookup"><span data-stu-id="e202e-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="e202e-115">サポートされている SIP ドメインごとに、_sipinternaltls._tcp の SRV レコード。 &lt;サインインのクライアント要求を認証およびリダイレクトする Standard Edition サーバーの FQDN にマップされるポート &gt; 5061 を超えるドメイン。</span><span class="sxs-lookup"><span data-stu-id="e202e-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="e202e-116">詳細については <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">、Lync Server 2013</a>での自動クライアント サインインの DNS 要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e202e-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e202e-117">ユニファイド コミュニケーション (UC) デバイスによるデバイス更新 Web サービス検出</span><span class="sxs-lookup"><span data-stu-id="e202e-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="e202e-118">ucupdates-r2 という名前の内部 A レコード。 &lt;Device &gt; Update Web サービスをホストする Standard Edition サーバーの IP アドレスに解決される SIP ドメイン。</span><span class="sxs-lookup"><span data-stu-id="e202e-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="e202e-119">UC デバイスがオンになっているが、ユーザーがデバイスにログインしたことがない場合、A レコードにより、デバイスは Device Update Web サービスをホストしているサーバーを検出して更新プログラムを取得できます。</span><span class="sxs-lookup"><span data-stu-id="e202e-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="e202e-120">それ以外の場合、ユーザーが初めてログインすると、デバイスはインバンド プロビジョニングを行ってサーバー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e202e-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e202e-121">HTTP トラフィックをサポートするリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="e202e-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="e202e-122">外部 Web ファームの FQDN をリバース プロキシの外部 IP アドレスに解決する外部 A レコード。</span><span class="sxs-lookup"><span data-stu-id="e202e-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="e202e-123">クライアントと UC デバイスは、このレコードを使用してリバース プロキシに接続します。</span><span class="sxs-lookup"><span data-stu-id="e202e-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="e202e-124">詳細については、計画に <a href="lync-server-2013-determine-dns-requirements.md">関するドキュメントの「Lync Server 2013</a> の DNS 要件を決定する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e202e-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e202e-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e202e-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

