---
title: 'Lync Server 2013: DNS の概要 - リバース プロキシ'
description: 'Lync Server 2013: DNS 概要-リバースプロキシ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Reverse proxy
ms:assetid: 3073affa-4d92-4453-9974-3a82ca0c6445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204781(v=OCS.15)
ms:contentKeyID: 48183755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc2d806893786a11317be1eff9bfdc08c9230bf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437722"
---
# <a name="dns-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="4b77f-103">DNS の概要 - Lync Server 2013 でのリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="4b77f-103">DNS summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b77f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b77f-104">

<span> </span></span></span>

<span data-ttu-id="4b77f-105">_**最終更新日:** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="4b77f-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="4b77f-106">リバースプロキシでは、次のように2つのネットワークアダプターを構成します。</span><span class="sxs-lookup"><span data-stu-id="4b77f-106">You configure two network adapters in your reverse proxy as follows:</span></span>

<div>

## <a name="reverse-proxy-network-adapter-requirements"></a><span data-ttu-id="4b77f-107">リバースプロキシネットワークアダプターの要件</span><span class="sxs-lookup"><span data-stu-id="4b77f-107">Reverse Proxy Network Adapter Requirements</span></span>

  - <span data-ttu-id="4b77f-108">**ネットワークアダプター 1 (内部インターフェイス)** の例</span><span class="sxs-lookup"><span data-stu-id="4b77f-108">**Network adapter 1 (Internal Interface)** example</span></span>
    
    <span data-ttu-id="4b77f-109">172.25.33.40 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="4b77f-109">Internal interface with 172.25.33.40 assigned.</span></span>
    
    <span data-ttu-id="4b77f-110">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="4b77f-110">No default gateway is defined.</span></span>
    
    <span data-ttu-id="4b77f-111">Lync Server フロントエンドプールサーバーが含まれているネットワーク (172.25.33.0 から192.168.10.0 など) に、リバースプロキシの内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4b77f-111">Ensure there is a route from the network containing the reverse proxy internal interface to any networks that contain Lync Server Front End pool servers (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="4b77f-112">**ネットワークアダプター 2 (外部インターフェイス)** の例</span><span class="sxs-lookup"><span data-stu-id="4b77f-112">**Network adapter 2 (External Interface)** example</span></span>
    
    <span data-ttu-id="4b77f-113">このネットワークアダプターには、少なくとも1つのパブリック IP アドレスが割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="4b77f-113">A minimum of one public IP address is assigned to this network adapter.</span></span>
    
    <span data-ttu-id="4b77f-114">ゲートウェイは、外部境界のルーターまたは統合ファイアウォールを指すように定義されています。</span><span class="sxs-lookup"><span data-stu-id="4b77f-114">Gateway is defined to point to the router or integrated firewall in your outer perimeter.</span></span> <span data-ttu-id="4b77f-115">(シナリオの例の 10.45.16.1)</span><span class="sxs-lookup"><span data-stu-id="4b77f-115">(10.45.16.1 in the scenario examples)</span></span>

### <a name="dns-records-required-for-reverse-proxy"></a><span data-ttu-id="4b77f-116">リバースプロキシに必要な DNS レコード</span><span class="sxs-lookup"><span data-stu-id="4b77f-116">DNS Records Required for Reverse Proxy</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b77f-117">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="4b77f-117">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="4b77f-118">FQDN</span><span class="sxs-lookup"><span data-stu-id="4b77f-118">FQDN</span></span></th>
<th><span data-ttu-id="4b77f-119">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="4b77f-119">IP address</span></span></th>
<th><span data-ttu-id="4b77f-120">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="4b77f-120">Maps to/comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b77f-121">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-121">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-122">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-122">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-123">外部公開リソースの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-123">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="4b77f-124">内部展開からの外部 web サービス。</span><span class="sxs-lookup"><span data-stu-id="4b77f-124">External web services from the internal deployment.</span></span> <span data-ttu-id="4b77f-125">このリバースプロキシを使用し、外部 web サービスが定義されているすべての SIP ドメイン用のすべてのプールおよび単一サーバー用に、追加のレコードを定義して作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4b77f-125">Additional records can be defined and created for all pools and single servers for any SIP domain that will use this reverse proxy, and has defined external web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b77f-126">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-126">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-127">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-127">webdirext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-128">外部公開リソースの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-128">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="4b77f-129">展開内のディレクターまたはディレクタープール用の外部 web サービス。</span><span class="sxs-lookup"><span data-stu-id="4b77f-129">External web services for the Directors or Director pools in your deployment.</span></span> <span data-ttu-id="4b77f-130">複数のダイレクタを定義できます。これらは、他の SIP ドメインと関連付けられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4b77f-130">You can define as many Directors as there are distinct Directors, of which may be associated with other SIP domains.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="4b77f-131">ディレクターの DNS レコードの定義と、フロントエンドプールまたはディレクターの決定にはなりません。</span><span class="sxs-lookup"><span data-stu-id="4b77f-131">Defining the DNS records for and publishing the Directors is not an either the Front End pool or the Director decision.</span></span> <span data-ttu-id="4b77f-132">ディレクターを使用している場合は、監督とフロントエンドプールの両方の外部 web サービスを定義して公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b77f-132">You must define and publish both the Director and the Front End pool external web services if you are using Directors.</span></span> <span data-ttu-id="4b77f-133">トポロジで定義されている場合、まず、特定のトラフィックの種類 (認証やその他の使用用) がディレクターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="4b77f-133">Specific traffic types (for authentication and other uses) will be sent to the Director first, if it is defined in the topology.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b77f-134">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-134">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-135">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-135">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-136">外部公開リソースの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-136">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="4b77f-137">外部で公開されたダイヤルイン会議</span><span class="sxs-lookup"><span data-stu-id="4b77f-137">Dial-in conferencing published externally</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b77f-138">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-139">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-139">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-140">外部公開リソースの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-140">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="4b77f-141">外部で公開された会議</span><span class="sxs-lookup"><span data-stu-id="4b77f-141">Conferences published externally</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b77f-142">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-143">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-143">officewebapps01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-144">Office Web Apps サーバーの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-144">Assigned listener for Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="4b77f-145">Office Web Apps サーバーが内部または境界内に展開され、外部クライアントアクセス用に公開されている</span><span class="sxs-lookup"><span data-stu-id="4b77f-145">Office Web Apps Server deployed internally or in the perimeter, and published for external client access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b77f-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="4b77f-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="4b77f-147">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4b77f-147">lyncdiscover.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4b77f-148">外部公開リソースの割り当て済みのリスナー</span><span class="sxs-lookup"><span data-stu-id="4b77f-148">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="4b77f-149">Lync で外部公開の自動検出の外部レコードが検出されました。モビリティ、Microsoft Lync Web App、scheduler Web アプリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b77f-149">Lync Discover External record for externally published AutoDiscover, and includes Mobility, Microsoft Lync Web App, and scheduler Web app</span></span></p></td>
</tr><span data-ttu-id="4b77f-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b77f-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

