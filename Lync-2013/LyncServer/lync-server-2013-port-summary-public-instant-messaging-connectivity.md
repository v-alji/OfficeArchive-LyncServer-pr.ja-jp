---
title: 'Lync Server 2013: ポートの概要-パブリックインスタントメッセージング接続'
description: 'Lync Server 2013: ポートの概要-パブリックインスタントメッセージング接続。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424276"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="39ac0-103">ポートの概要-Lync Server 2013 でのパブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="39ac0-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39ac0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39ac0-104">

<span> </span></span></span>

<span data-ttu-id="39ac0-105">_**最終更新日:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="39ac0-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="39ac0-106">パブリックインスタントメッセージング接続をサポートするために必要なポートとプロトコル用にファイアウォールを構成するには、まず、SIP/MTLS/TCP 5061 は、パブリック IM プロバイダーの連絡先が Lync クライアントに連絡するか、Lync がパブリック IM の連絡先に連絡できるかどうかを考慮するための双方向です。</span><span class="sxs-lookup"><span data-stu-id="39ac0-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="39ac0-107">Windows Live Messenger は、Lync クライアントとの音声/ビデオ通信に参加できます。</span><span class="sxs-lookup"><span data-stu-id="39ac0-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="39ac0-108">通常、ファイアウォールを使用して、外部ユーザーとして Lync クライアントをサポートする、非常に類似したファイアウォールポートおよびプロトコル構成については、このアカウントをご利用ください。</span><span class="sxs-lookup"><span data-stu-id="39ac0-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="39ac0-109">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="39ac0-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="39ac0-110">Windows Live Messenger とのフェデレーションには、Lync Standard クライアントアクセスライセンス (CAL) を超える追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="39ac0-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="39ac0-111">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="39ac0-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="39ac0-112">Messenger クライアント連絡先とのフェデレーションは、2013年3月15日に正式に終了します。中国とは異なります。</span><span class="sxs-lookup"><span data-stu-id="39ac0-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="39ac0-113">Skype は、以前に Messenger を使用したフェデレーションユーザーのフェデレーションクライアントになります。</span><span class="sxs-lookup"><span data-stu-id="39ac0-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="39ac0-114">ファイアウォールの概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="39ac0-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39ac0-115">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="39ac0-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="39ac0-116">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="39ac0-116">Source IP address</span></span></th>
<th><span data-ttu-id="39ac0-117">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="39ac0-117">Destination IP address</span></span></th>
<th><span data-ttu-id="39ac0-118">メモ</span><span class="sxs-lookup"><span data-stu-id="39ac0-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39ac0-119">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="39ac0-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="39ac0-120">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="39ac0-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="39ac0-121">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-122">SIP を使うフェデレーションおよびパブリック IM 接続の場合。</span><span class="sxs-lookup"><span data-stu-id="39ac0-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39ac0-123">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="39ac0-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="39ac0-124">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-125">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="39ac0-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="39ac0-126">SIP を使うフェデレーションおよびパブリック IM 接続の場合。</span><span class="sxs-lookup"><span data-stu-id="39ac0-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39ac0-127">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="39ac0-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="39ac0-128">クライアント</span><span class="sxs-lookup"><span data-stu-id="39ac0-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="39ac0-129">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-130">外部ユーザー アクセス用のクライアントからサーバーへの SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="39ac0-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39ac0-131">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="39ac0-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="39ac0-132">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-133">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="39ac0-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="39ac0-134">パブリック IM 接続が構成されている場合、Windows Live Messenger でのセッションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="39ac0-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39ac0-135">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="39ac0-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="39ac0-136">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-137">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="39ac0-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="39ac0-138">Windows Live Messenger とのパブリック IM 接続に必要。</span><span class="sxs-lookup"><span data-stu-id="39ac0-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39ac0-139">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="39ac0-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="39ac0-140">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="39ac0-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="39ac0-141">エッジサーバーアクセスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="39ac0-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="39ac0-142">Windows Live Messenger とのパブリック IM 接続に必要。</span><span class="sxs-lookup"><span data-stu-id="39ac0-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39ac0-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="39ac0-143">See Also</span></span>


[<span data-ttu-id="39ac0-144">Lync Server 2013 の外部ユーザー アクセスのシナリオ</span><span class="sxs-lookup"><span data-stu-id="39ac0-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="39ac0-145">Lync Server 2013 の外部の音声ビデオ ファイアウォールおよびポートの要件を決定する</span><span class="sxs-lookup"><span data-stu-id="39ac0-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="39ac0-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39ac0-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

