---
title: 'Lync Server 2013: 証明書の概要 - 単一ディレクター'
description: 'Lync Server 2013: 証明書の概要-単一のディレクター。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cf930a73d9989ec44f52f1d70ee9e0f900e4d6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435195"
---
# <a name="certificate-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="74e27-103">証明書の概要 - Lync Server 2013 の単一ディレクター</span><span class="sxs-lookup"><span data-stu-id="74e27-103">Certificate summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74e27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74e27-104">

<span> </span></span></span>

<span data-ttu-id="74e27-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="74e27-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="74e27-106">1つのディレクターの証明書要件は、監督が受信できるサービスのサブジェクト名とサブジェクトの代替名を持つ既定の証明書で構成されます。</span><span class="sxs-lookup"><span data-stu-id="74e27-106">Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="74e27-107">さらに、サーバー間認証のための OAuth トークン証明書も用意されています。</span><span class="sxs-lookup"><span data-stu-id="74e27-107">Additionally, there is an OAuth Token certificate for server to server authentication purposes.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="74e27-108">ディレクター用の証明書</span><span class="sxs-lookup"><span data-stu-id="74e27-108">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74e27-109">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="74e27-109">Component</span></span></th>
<th><span data-ttu-id="74e27-110">サブジェクト名 (SN)</span><span class="sxs-lookup"><span data-stu-id="74e27-110">Subject name (SN)</span></span></th>
<th><span data-ttu-id="74e27-111">サブジェクトの代替名 (SAN)</span><span class="sxs-lookup"><span data-stu-id="74e27-111">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="74e27-112">コメント</span><span class="sxs-lookup"><span data-stu-id="74e27-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74e27-113">Default</span><span class="sxs-lookup"><span data-stu-id="74e27-113">Default</span></span></p></td>
<td><p><span data-ttu-id="74e27-114">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="74e27-114">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="74e27-115">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="74e27-115">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="74e27-116">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="74e27-116">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="74e27-117">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="74e27-117">meet.contoso.com</span></span></p>
<p><span data-ttu-id="74e27-118">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="74e27-118">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="74e27-119">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="74e27-119">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="74e27-120">(必要に応じて) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="74e27-120">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="74e27-121">ディレクター証明書は、内部管理の証明機関 (CA) またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="74e27-121">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="74e27-122">ディレクターは、境界サーバーまたはエッジサーバーのリバースプロキシからの要求に応答します。</span><span class="sxs-lookup"><span data-stu-id="74e27-122">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="74e27-123">内部クライアントでは、監督は使用されません。</span><span class="sxs-lookup"><span data-stu-id="74e27-123">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="74e27-124">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="74e27-124">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74e27-125">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="74e27-125">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="74e27-126">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="74e27-126">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="74e27-127">エントリがありません</span><span class="sxs-lookup"><span data-stu-id="74e27-127">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="74e27-128">最小のキー長は1024ですが、最小の推奨されるキーの長さは2048ビットであるという警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="74e27-128">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="74e27-129">OAuthTokenIssuer 証明書は、大規模な環境でサーバーを認証することを目的とした単一目的の証明書であり、内部 CA またはパブリック CA から要求することができます。</span><span class="sxs-lookup"><span data-stu-id="74e27-129">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="74e27-130">証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="74e27-130">The certificate is required.</span></span></p><span data-ttu-id="74e27-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74e27-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

