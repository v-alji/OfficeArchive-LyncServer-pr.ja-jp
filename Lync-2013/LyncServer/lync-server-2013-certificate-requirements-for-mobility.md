---
title: 'Lync Server 2013: モビリティの証明書の要件'
description: 'Lync Server 2013: モビリティの証明書の要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435363"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="4d775-103">Lync Server 2013 のモビリティの証明書の要件</span><span class="sxs-lookup"><span data-stu-id="4d775-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d775-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d775-104">

<span> </span></span></span>

<span data-ttu-id="4d775-105">_**最終更新日:** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="4d775-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="4d775-106">モバイルクライアントの自動検出をサポートし、モバイルクライアントの自動検出をサポートしている場合は、モバイルクライアントからのセキュリティで保護された接続をサポートするために、証明書に特定のサブジェクト代替名エントリを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d775-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="4d775-107">次の証明書に対して自動検出を行うには、サブジェクトの代替名エントリを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d775-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="4d775-108">ディレクター プール</span><span class="sxs-lookup"><span data-stu-id="4d775-108">Director pool</span></span>

  - <span data-ttu-id="4d775-109">フロントエンド プール</span><span class="sxs-lookup"><span data-stu-id="4d775-109">Front End pool</span></span>

  - <span data-ttu-id="4d775-110">リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="4d775-110">Reverse proxy</span></span>

<span data-ttu-id="4d775-111">このセクションでは、自動検出用に証明書に必要なサブジェクトの代替名エントリについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4d775-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4d775-112">内部証明機関を使った証明書の再発行は、通常は単純なプロセスですが、複数のサブジェクト代替名エントリをリバースプロキシによって使用されるパブリック証明書に追加するのはコストがかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="4d775-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="4d775-113">多数の SIP ドメインがあり、サブジェクトの代替名を追加した場合は、HTTPS (既定の構成) を使う代わりに、最初の自動検出サービス要求に対して HTTP を使うようにリバースプロキシを構成できます。</span><span class="sxs-lookup"><span data-stu-id="4d775-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="4d775-114">詳細については、「 <A href="lync-server-2013-technical-requirements-for-mobility.md">Lync Server 2013 でのモビリティの技術要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d775-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="4d775-115">ディレクタープール証明書の要件</span><span class="sxs-lookup"><span data-stu-id="4d775-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d775-116">説明</span><span class="sxs-lookup"><span data-stu-id="4d775-116">Description</span></span></th>
<th><span data-ttu-id="4d775-117">サブジェクトの代替名エントリ</span><span class="sxs-lookup"><span data-stu-id="4d775-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d775-118">内部自動検出サービス URL</span><span class="sxs-lookup"><span data-stu-id="4d775-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="4d775-119">SAN = lyncdiscoverinternal。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d775-120">外部自動検出サービスの URL</span><span class="sxs-lookup"><span data-stu-id="4d775-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="4d775-121">SAN = lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="4d775-122">または、SAN = \* を使用することもできます。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="4d775-123">フロントエンドプール証明書の要件</span><span class="sxs-lookup"><span data-stu-id="4d775-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d775-124">説明</span><span class="sxs-lookup"><span data-stu-id="4d775-124">Description</span></span></th>
<th><span data-ttu-id="4d775-125">サブジェクトの代替名エントリ</span><span class="sxs-lookup"><span data-stu-id="4d775-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d775-126">内部自動検出サービス URL</span><span class="sxs-lookup"><span data-stu-id="4d775-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="4d775-127">SAN = lyncdiscoverinternal。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d775-128">外部自動検出サービスの URL</span><span class="sxs-lookup"><span data-stu-id="4d775-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="4d775-129">SAN = lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="4d775-130">または、SAN = \* を使用することもできます。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="4d775-131">リバースプロキシ (パブリック CA) 証明書の要件</span><span class="sxs-lookup"><span data-stu-id="4d775-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d775-132">説明</span><span class="sxs-lookup"><span data-stu-id="4d775-132">Description</span></span></th>
<th><span data-ttu-id="4d775-133">サブジェクトの代替名エントリ</span><span class="sxs-lookup"><span data-stu-id="4d775-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d775-134">外部自動検出サービスの URL</span><span class="sxs-lookup"><span data-stu-id="4d775-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="4d775-135">SAN = lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="4d775-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="4d775-136">この SAN を、リバースプロキシの SSL リスナーに割り当てられている証明書に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4d775-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="4d775-137">リバースプロキシリスナーには、外部 Web サービスの URL (たとえば、オプションのディレクターを展開した場合は、SAN = lyncwebextpool01、dirwebexternal.contoso.com など) のサブジェクト代替名があります。</span><span class="sxs-lookup"><span data-stu-id="4d775-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="4d775-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d775-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

