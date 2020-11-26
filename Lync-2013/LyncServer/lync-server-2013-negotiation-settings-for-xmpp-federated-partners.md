---
title: 'Lync Server 2013: XMPP フェデレーション パートナーのネゴシエーション設定'
description: 'Lync Server 2013: XMPP フェデレーションパートナーのネゴシエーション設定。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445588"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="c35a1-103">Lync Server 2013 の XMPP フェデレーション パートナーのネゴシエーション設定</span><span class="sxs-lookup"><span data-stu-id="c35a1-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c35a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c35a1-104">

<span> </span></span></span>

<span data-ttu-id="c35a1-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="c35a1-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="c35a1-106">XMPP パートナーの構成でのネゴシエーションの種類の設定には、さまざまな組み合わせが用意されています。</span><span class="sxs-lookup"><span data-stu-id="c35a1-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="c35a1-107">これらの組み合わせの一部は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="c35a1-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="c35a1-108">このトピックで詳しく説明する表では、有効な設定と無効な設定を定義しています。</span><span class="sxs-lookup"><span data-stu-id="c35a1-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="c35a1-109">一般的な構成は、最初の表の2番目の表で、可能なすべての組み合わせの詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="c35a1-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="c35a1-110">*トランスポート層セキュリティ*(TLS) も使用できる **場合を除き**、*単純な認証とセキュリティレイヤー* (SASL) を持つことはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c35a1-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="c35a1-111">SASL は、暗号化されていない (読み取り可能な) 形式で送信され、TLS などの別の手段で保護されている場合を除き、送信しないでください。</span><span class="sxs-lookup"><span data-stu-id="c35a1-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="c35a1-112">一般的な XMPP のフェデレーションネゴシエーションの方法</span><span class="sxs-lookup"><span data-stu-id="c35a1-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c35a1-113">トランスポート層セキュリティ (TLS)</span><span class="sxs-lookup"><span data-stu-id="c35a1-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="c35a1-114">簡易認証とセキュリティレイヤー (SASL)</span><span class="sxs-lookup"><span data-stu-id="c35a1-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="c35a1-115">ダイヤルバックの認証</span><span class="sxs-lookup"><span data-stu-id="c35a1-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="c35a1-116">予期される認証方法</span><span class="sxs-lookup"><span data-stu-id="c35a1-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="c35a1-117">メモ</span><span class="sxs-lookup"><span data-stu-id="c35a1-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-118">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-118">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-119">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-119">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-120">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-120">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-121">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="c35a1-122">TLS と SASL は、SASL メッセージストリームがセキュリティで保護されていることを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c35a1-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="c35a1-123">コールバックは使用できません。 XMPP フェデレーションパートナーが TLS を必須またはオプションに設定していない場合は、フォールバックメソッドに使用できません。</span><span class="sxs-lookup"><span data-stu-id="c35a1-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-124">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-124">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-126">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-126">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-127">TLS 経由の SASL、TLS コールバック、TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-128">XMPP フェデレーションパートナーが、オプションまたは必須の SASL に SASL を設定している場合は、TLS を要求することによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="c35a1-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="c35a1-129">SASL が利用できない場合は、TLS 経由のダイヤルバックが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c35a1-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-131">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-132">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-132">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-133">TLS 経由の SASL、TLS コールバック、TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-134">提供されているネゴシエーションの方法は非常に柔軟ですが、これらの設定は XMPP フェデレーションパートナーの設定に依存します。</span><span class="sxs-lookup"><span data-stu-id="c35a1-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="c35a1-135">パートナーに TLS がオプションまたは必須であるが、SASL はサポートされていない場合は、TLS のコールバックが利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="c35a1-136">パートナーの TLS と SASL がオプションまたは必須に設定されている場合は、SASL を介した TLS の最適な選択が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c35a1-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-137">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-138">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-139">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-139">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-140">TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-141">多くの場合、TCP コールバックは唯一の解決策です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="c35a1-142">他のオプションよりも望ましいのは、何らかの信頼レベルを提供することです。</span><span class="sxs-lookup"><span data-stu-id="c35a1-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="c35a1-143">XMPP フェデレーションネゴシエーションメソッドマトリックス-完了</span><span class="sxs-lookup"><span data-stu-id="c35a1-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c35a1-144">トランスポート層セキュリティ (TLS)</span><span class="sxs-lookup"><span data-stu-id="c35a1-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="c35a1-145">簡易認証とセキュリティレイヤー (SASL)</span><span class="sxs-lookup"><span data-stu-id="c35a1-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="c35a1-146">ダイヤルバックの認証</span><span class="sxs-lookup"><span data-stu-id="c35a1-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="c35a1-147">予期される認証方法</span><span class="sxs-lookup"><span data-stu-id="c35a1-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="c35a1-148">無効な構成のメモ、警告、またはエラー</span><span class="sxs-lookup"><span data-stu-id="c35a1-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-149">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-149">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-150">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-150">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-151">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-151">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-152">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-153">SASL と TLS の両方が必要な場合、コールバックは動作しません。</span><span class="sxs-lookup"><span data-stu-id="c35a1-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-154">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-154">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-155">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-155">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-156">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-156">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-157">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-159">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-159">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-160">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-160">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-161">TLS 経由の SASL、TLS コールバック、TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-162">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-162">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-163">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-165">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-165">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-166">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-166">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-167">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-168">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-168">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-169">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-170">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-171">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-171">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-172">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-172">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-173">TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-174">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-174">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-175">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-176">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-177">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-177">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-178">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-179">有効な構成ではありません</span><span class="sxs-lookup"><span data-stu-id="c35a1-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-180">SASL には TLS が必要であるため、TLS は利用できません。 SASL/TLS は成功しません。</span><span class="sxs-lookup"><span data-stu-id="c35a1-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="c35a1-181">TCP コールバックは false に設定されているため、使用できません。</span><span class="sxs-lookup"><span data-stu-id="c35a1-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-182">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-182">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-183">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-184">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-184">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-185">Tls による SASL、TLS のコールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-186">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-186">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-187">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-188">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-188">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-189">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-191">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-192">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-192">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-193">TLS 経由の SASL、TLS コールバック、TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-194">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-194">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-195">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-196">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-197">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-198">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-198">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-199">TLS 経由の SASL</span><span class="sxs-lookup"><span data-stu-id="c35a1-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-200">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-200">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-201">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-202">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-203">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-204">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-204">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-205">TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-206">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-206">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-207">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-208">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-209">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-210">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-211">有効な構成ではありません</span><span class="sxs-lookup"><span data-stu-id="c35a1-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-212">SASL には TLS が必要です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-212">SASL requires TLS.</span></span> <span data-ttu-id="c35a1-213">TLS をオプションとして許可すると、セッションのネゴシエーションが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-214">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-214">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-215">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-216">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-216">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-217">TLS のコールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-218">構成により、TLS のコールバックが可能になります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-219">必須</span><span class="sxs-lookup"><span data-stu-id="c35a1-219">Required</span></span></p></td>
<td><p><span data-ttu-id="c35a1-220">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-221">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-221">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-222">有効な構成ではありません</span><span class="sxs-lookup"><span data-stu-id="c35a1-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-223">SASL またはダイヤルバックを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-224">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-225">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-226">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-226">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-227">TLS のダイヤルバック, TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-228">他のエンドポイントのネゴシエーションの選択肢に基づいて、TCP または TLS のコールバックが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="c35a1-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-229">省略可能</span><span class="sxs-lookup"><span data-stu-id="c35a1-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="c35a1-230">非サポート</span><span class="sxs-lookup"><span data-stu-id="c35a1-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-231">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-231">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-232">有効な構成ではありません</span><span class="sxs-lookup"><span data-stu-id="c35a1-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-233">SASL またはダイヤルバックを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c35a1-234">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-235">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-236">True</span><span class="sxs-lookup"><span data-stu-id="c35a1-236">True</span></span></p></td>
<td><p><span data-ttu-id="c35a1-237">TCP コールバック</span><span class="sxs-lookup"><span data-stu-id="c35a1-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="c35a1-238">TCP コールバックは、唯一利用可能なネゴシエーションの方法です。</span><span class="sxs-lookup"><span data-stu-id="c35a1-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c35a1-239">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-240">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="c35a1-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="c35a1-241">False</span><span class="sxs-lookup"><span data-stu-id="c35a1-241">False</span></span></p></td>
<td><p><span data-ttu-id="c35a1-242">有効な構成ではありません</span><span class="sxs-lookup"><span data-stu-id="c35a1-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="c35a1-243">SASL またはダイヤルバックを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c35a1-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="c35a1-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c35a1-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

