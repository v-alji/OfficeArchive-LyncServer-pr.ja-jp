---
title: 'Lync Server 2013: 常設チャットサーバーの DNS 要件'
description: 'Lync Server 2013: 常設チャットサーバーの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Persistent Chat Servers
ms:assetid: f7531374-d7ed-4b63-ae81-02294cb4496a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205391(v=OCS.15)
ms:contentKeyID: 48185857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01bfc126ab588542ef5160a0eabe0c839dcf0e44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429057"
---
# <a name="dns-requirements-for-persistent-chat-servers-in-lync-server-2013"></a><span data-ttu-id="a2efb-103">Lync Server 2013 の常設チャットサーバーの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="a2efb-103">DNS requirements for Persistent Chat Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2efb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2efb-104">

<span> </span></span></span>

<span data-ttu-id="a2efb-105">_**最終更新日:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="a2efb-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="a2efb-106">このセクションでは、常設チャットサーバーの展開に必要なドメインネームシステム (DNS) レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a2efb-106">This section describes the Domain Name System (DNS) records that are required for deployment of Persistent Chat Servers.</span></span>

<div>

## <a name="dns-records-for-persistent-chat-servers"></a><span data-ttu-id="a2efb-107">常設チャットサーバーの DNS レコード</span><span class="sxs-lookup"><span data-stu-id="a2efb-107">DNS Records for Persistent Chat Servers</span></span>

<span data-ttu-id="a2efb-108">次の表は、常設チャットサーバーの展開の DNS 要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="a2efb-108">The following table specifies DNS requirements for Persistent Chat Server deployment.</span></span>

### <a name="dns-requirements-for-a-persistent-chat-server"></a><span data-ttu-id="a2efb-109">常設チャットサーバーの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="a2efb-109">DNS Requirements for a Persistent Chat Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2efb-110">展開シナリオ</span><span class="sxs-lookup"><span data-stu-id="a2efb-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="a2efb-111">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="a2efb-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2efb-112">1つの常設チャットサーバー</span><span class="sxs-lookup"><span data-stu-id="a2efb-112">One Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="a2efb-113">内部の A レコード。サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決します。</span><span class="sxs-lookup"><span data-stu-id="a2efb-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2efb-114">常設チャットプール</span><span class="sxs-lookup"><span data-stu-id="a2efb-114">Persistent Chat pool</span></span></p></td>
<td><p><span data-ttu-id="a2efb-115">内部の A レコード。サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決します。</span><span class="sxs-lookup"><span data-stu-id="a2efb-115">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="a2efb-116"><strong>例</strong></span><span class="sxs-lookup"><span data-stu-id="a2efb-116"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="a2efb-117">PersistentChatServer01.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="a2efb-117">PersistentChatServer01.contoso.com     10.10.10.1</span></span></p>
<p><span data-ttu-id="a2efb-118">PersistentChatServer02.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="a2efb-118">PersistentChatServer02.contoso.com     10.10.10.2</span></span></p>
<p><span data-ttu-id="a2efb-119">内部の A レコード。サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決します。</span><span class="sxs-lookup"><span data-stu-id="a2efb-119">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="a2efb-120"><strong>例</strong></span><span class="sxs-lookup"><span data-stu-id="a2efb-120"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="a2efb-121">PersistentChatPool.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="a2efb-121">PersistentChatPool.contoso.com    10.10.10.1</span></span></p>
<p><span data-ttu-id="a2efb-122">PersistentChatPool.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="a2efb-122">PersistentChatPool.contoso.com    10.10.10.2</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a2efb-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2efb-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

