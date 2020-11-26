---
title: 'Lync Server 2013: 証明書の概要-拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション'
description: 'Lync Server 2013: 証明書の概要-拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: b059a34e-99df-40af-91fe-fe2aa52841f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618374(v=OCS.15)
ms:contentKeyID: 49105661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e2bb593d909c2eec6032dc89c07cc5f5b1a72db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435300"
---
# <a name="certificate-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="8400b-103">証明書の概要-Lync Server 2013 での拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション</span><span class="sxs-lookup"><span data-stu-id="8400b-103">Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8400b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8400b-104">

<span> </span></span></span>

<span data-ttu-id="8400b-105">_**最終更新日:** 2012-12-23_</span><span class="sxs-lookup"><span data-stu-id="8400b-105">_**Topic Last Modified:** 2012-12-23_</span></span>

<span data-ttu-id="8400b-106">拡張メッセージングとプレゼンスプロトコル (XMPP) パートナーとの通信を有効にして確立するための証明書要件には、XMPP ドメインの追加レコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="8400b-106">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require the additional record of your XMPP domains.</span></span> <span data-ttu-id="8400b-107">サブジェクトの代替名 (SAN) として証明書に含まれているレコードは、XMPP 通信に参加できるドメインです。</span><span class="sxs-lookup"><span data-stu-id="8400b-107">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="8400b-108">ドメイン全体で XMPP を有効にする場合や、ユーザーのサブセットに対して XMPP を有効にしている場合は、ドメインのルートレベルのドメイン (たとえば、contoso.com) にすることができます (例: corp.contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="8400b-108">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="8400b-109">拡張メッセージングとプレゼンスプロトコルの証明書の概要</span><span class="sxs-lookup"><span data-stu-id="8400b-109">Certificate Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8400b-110">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8400b-110">Component</span></span></th>
<th><span data-ttu-id="8400b-111">サブジェクト名</span><span class="sxs-lookup"><span data-stu-id="8400b-111">Subject name</span></span></th>
<th><span data-ttu-id="8400b-112">サブジェクト代替名 (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="8400b-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="8400b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="8400b-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8400b-114">エッジサーバーまたはエッジプールのアクセスエッジサービスに割り当てる</span><span class="sxs-lookup"><span data-stu-id="8400b-114">Assign to Access Edge service of Edge Server or Edge pool</span></span></p></td>
<td><p><span data-ttu-id="8400b-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8400b-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="8400b-116">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8400b-116">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="8400b-117">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8400b-117">sip.contoso.com</span></span></p>
<p><span data-ttu-id="8400b-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="8400b-118">sip.fabrikam.com</span></span></p>
<p><span data-ttu-id="8400b-119">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8400b-119">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="8400b-120">最初の3つの SAN エントリは、フルエッジサーバーの通常の SAN エントリです。</span><span class="sxs-lookup"><span data-stu-id="8400b-120">The first three SAN entries are the normal SAN entries for a full Edge Server.</span></span> <span data-ttu-id="8400b-121">Contoso.com は、ルートドメインレベルで XMPP パートナーとのフェデレーションを行うために必要なエントリです。</span><span class="sxs-lookup"><span data-stu-id="8400b-121">The contoso.com is the entry required for federation with the XMPP partner at the root domain level.</span></span> <span data-ttu-id="8400b-122">このエントリは、サフィックス contoso.com を持つすべてのドメインで XMPP を許可します。</span><span class="sxs-lookup"><span data-stu-id="8400b-122">This entry will allow XMPP for all domains with the suffix contoso.com.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8400b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8400b-123">See Also</span></span>


[<span data-ttu-id="8400b-124">Lync Server 2013 での XMPP 構成の例  - Google Talk との XMPP フェデレーション</span><span class="sxs-lookup"><span data-stu-id="8400b-124">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="8400b-125">Lync Server 2013 でエッジ サーバー証明書を計画する</span><span class="sxs-lookup"><span data-stu-id="8400b-125">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  


[<span data-ttu-id="8400b-126">Lync Server 2013 用のエッジ証明書のセットアップ</span><span class="sxs-lookup"><span data-stu-id="8400b-126">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)  
[<span data-ttu-id="8400b-127">要求-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="8400b-127">Request-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate)  
[<span data-ttu-id="8400b-128">設定-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="8400b-128">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="8400b-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8400b-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

