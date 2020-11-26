---
title: 'Lync Server 2013: スキーマの属性と説明'
description: 'Lync Server 2013: スキーマの属性と説明。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444960"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="9d487-103">Lync Server 2013 でのスキーマの属性と説明</span><span class="sxs-lookup"><span data-stu-id="9d487-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d487-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d487-104">

<span> </span></span></span>

<span data-ttu-id="9d487-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="9d487-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="9d487-106">このセクションでは、Lync Server 2013 で使用されるすべてのスキーマ属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="9d487-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="9d487-107">属性に関連付けられているクラスについては、「 [Lync Server 2013 のクラス別のスキーマ属性](lync-server-2013-schema-attributes-by-class.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9d487-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="9d487-108">Lync Server 2013 で新しく追加されたクラスと属性の一覧については、「 [Lync server 2013 でのスキーマの変更](lync-server-2013-schema-changes-in-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d487-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="9d487-109">リンクペアの属性は、転送リンクまたは戻るリンクとして指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="9d487-110">別のオブジェクトを参照する属性は、転送リンクです。最初のオブジェクトを参照する他のオブジェクトの属性は、[戻る] リンクです。</span><span class="sxs-lookup"><span data-stu-id="9d487-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="9d487-111">前方リンクは更新可能で、戻るリンクは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="9d487-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="9d487-112">一部の属性にはビットマスク値があります。</span><span class="sxs-lookup"><span data-stu-id="9d487-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="9d487-113">これらの属性の場合、各設定は1ビットで表され、表示される10進値はビット位置を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="9d487-114">ビット位置はビット0から始まります。</span><span class="sxs-lookup"><span data-stu-id="9d487-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="9d487-115">たとえば、1 (binary) はビット0に設定され、1万 (binary) はビット4で設定されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="9d487-116">各ビットはプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-116">Each bit represents a property.</span></span> <span data-ttu-id="9d487-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9d487-117">The following are some examples:</span></span>

  - <span data-ttu-id="9d487-118">1万 (binary) の10進数は16です (つまり、ビット4が設定されています)。</span><span class="sxs-lookup"><span data-stu-id="9d487-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="9d487-119">1億 (binary) の小数点以下の値は 256 (ビット8が設定されている) です。</span><span class="sxs-lookup"><span data-stu-id="9d487-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="9d487-120">1100 (binary) の10進数の値は12です (つまり、ビット2と3は設定され、両方のビットで表されるプロパティは有効です)。</span><span class="sxs-lookup"><span data-stu-id="9d487-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="9d487-121">1111000001 (binary) には、10進数の 961 (ビット0、6、7、8、および9の値が設定されています。これらの各ビットのプロパティは有効です)。</span><span class="sxs-lookup"><span data-stu-id="9d487-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="9d487-122">Lync Server 2013 のスキーマ属性</span><span class="sxs-lookup"><span data-stu-id="9d487-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d487-123">属性</span><span class="sxs-lookup"><span data-stu-id="9d487-123">Attribute</span></span></th>
<th><span data-ttu-id="9d487-124">説明</span><span class="sxs-lookup"><span data-stu-id="9d487-124">Description</span></span></th>
<th><span data-ttu-id="9d487-125">注釈</span><span class="sxs-lookup"><span data-stu-id="9d487-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d487-126">dnsHostName</span><span class="sxs-lookup"><span data-stu-id="9d487-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="9d487-127"><strong>Msrtcsip-userenabled true</strong>と<strong>msrtcsip-userenabled true の</strong>両方のサーバークラスに関連付けられている、Active Directory ドメインサービス内の既存の属性。</span><span class="sxs-lookup"><span data-stu-id="9d487-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="9d487-128">この属性は、プールまたは監視サーバーの完全修飾ドメイン名 (FQDN) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="9d487-129">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-130">Microsoft Office Live Communications Server 2005 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-131">SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="9d487-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-132">この属性には、このオブジェクトに対応する別のフォレストのオブジェクトの識別名 (DN) の文字列表現が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="9d487-133">この属性は、配布グループの展開と自動参加に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="9d487-134">この属性は、Windows Server 2003 R2 の既定の Active Directory スキーマで定義されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="9d487-135">AD DS から Windows Server 2003 R2 へのアップグレードを必要としないように、Active Directory スキーマの準備では、Windows Server 2003 スキーマがこの属性定義で拡張されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="9d487-136">Microsoft Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="9d487-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="9d487-138">この複数値属性はボイスメールの設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="9d487-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="9d487-139">この属性は、Exchange ユニファイドメッセージング (UM) と共有されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="9d487-140">Microsoft Lync Server 2010 の新製品です。</span><span class="sxs-lookup"><span data-stu-id="9d487-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="9d487-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="9d487-142">このマルチバリュー属性は、ユーザーに適用される保留ポリシーの識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="9d487-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="9d487-143">保留ポリシーは、保留中のユーザーのメールボックスアイテムを保持します。</span><span class="sxs-lookup"><span data-stu-id="9d487-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="9d487-144">この属性は Exchange 2013 と共有されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="9d487-145">Lync Server 2013 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-146">Msrtcsip-userenabled true-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="9d487-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="9d487-147">この属性は、ユーザーに対して電話会議プロバイダーの情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="9d487-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="9d487-148">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-149">Msrtcsip-userenabled true-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="9d487-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="9d487-150">この属性は、アプリケーションの連絡先に対して信頼されているサービスエントリを指します。</span><span class="sxs-lookup"><span data-stu-id="9d487-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="9d487-151">Microsoft Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-152">Msrtcsip-userenabled true-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="9d487-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="9d487-153">この属性には、アプリケーションサーバー上でホストされているアプリケーションの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="9d487-154">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-155">Msrtcsip-userenabled true-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="9d487-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="9d487-156">この属性は、アプリケーションの連絡先のオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="9d487-157">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-158">Msrtcsip-userenabled true-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="9d487-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="9d487-159">この属性には、アプリケーションの連絡先の第一言語が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="9d487-160">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-161">Msrtcsip-userenabled true-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="9d487-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="9d487-162">この複数の値の属性には、アプリケーションの連絡先のセカンダリ言語が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="9d487-163">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-164">Msrtcsip-userenabled true-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="9d487-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="9d487-165">この属性には、このプールに属しているアプリケーションサーバーの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="9d487-166">このバックリンク属性への対応する前方リンクは <strong>Msrtcsip-userenabled true Serverpoollink</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-167">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-168">Msrtcsip-userenabled true-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="9d487-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="9d487-169">この属性は、このアプリケーションサーバーが属しているプールを指します。</span><span class="sxs-lookup"><span data-stu-id="9d487-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="9d487-170">これは、転送リンクです。</span><span class="sxs-lookup"><span data-stu-id="9d487-170">This is the forward link.</span></span> <span data-ttu-id="9d487-171">対応する後方リンクは、 <strong>Msrtcsip-userenabled true Serverbl</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-172">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-173">Msrtcsip-userenabled true-アーカイブの既定値 (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-174">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-175">Office Communications Server 2007 で廃止されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-176">Msrtcsip-userenabled true-アーカイブ Defaultflags (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-177">この属性は、すべてのユーザーの通信をアーカイブするために、フォレストの境界内でグローバルな既定値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="9d487-178">これは、アーカイブエージェントレイヤーによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="9d487-179">この属性の値の範囲は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-180"><strong>TRUE</strong>: すべてのユーザーをアーカイブする</span><span class="sxs-lookup"><span data-stu-id="9d487-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="9d487-181"><strong>FALSE</strong>: すべてのユーザーをアーカイブしない</span><span class="sxs-lookup"><span data-stu-id="9d487-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="9d487-182">この属性は、フォレストの境界内でのグローバルコントロールであり、内部ネットワーク内でのユーザーの通信はどのようにアーカイブされますか。</span><span class="sxs-lookup"><span data-stu-id="9d487-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="9d487-183"><strong>Live Communications Server 2005 の動作 (現在は廃止)</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="9d487-184">この属性の値の範囲は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-185">0: メッセージ本文をアーカイブする [ビット 0]</span><span class="sxs-lookup"><span data-stu-id="9d487-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="9d487-186">1: メッセージ本文をアーカイブしない [ビット 0]</span><span class="sxs-lookup"><span data-stu-id="9d487-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="9d487-187"><strong>Office Communications Server 2007 の動作</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="9d487-188">この属性の値の範囲は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-189">0: ArchiveFederationDefaultWithoutBody (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="9d487-190">1-2: アーカイブ内部通信</span><span class="sxs-lookup"><span data-stu-id="9d487-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="9d487-191">3-4: ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="9d487-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="9d487-192">5: RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="9d487-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="9d487-193">6: RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-194">7: RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-195">8: RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="9d487-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="9d487-196">9: RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-197">10: RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-198">11: RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-199">12: RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="9d487-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="9d487-200">13: Record会議のインスタンス化</span><span class="sxs-lookup"><span data-stu-id="9d487-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="9d487-201">14: Record会議の結合</span><span class="sxs-lookup"><span data-stu-id="9d487-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="9d487-202">15: RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="9d487-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="9d487-203">16: RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="9d487-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-204">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-205">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-206">Msrtcsip-userenabled true-ArchiveFederationDefault (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-207">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-208">Office Communications Server 2007 で廃止されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-209">Msrtcsip-userenabled true-ArchiveFederationDefaultFlags (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-210">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-211">Office Communications Server 2007 で廃止されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-212">Msrtcsip-userenabled true-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="9d487-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="9d487-213">この属性は、1人のユーザーの通信がアーカイブされるかどうかを制御するためのビットフィールドとして使用される整数です。</span><span class="sxs-lookup"><span data-stu-id="9d487-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="9d487-214">このコントロールは、アーカイブエージェントレイヤーによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="9d487-215">グローバルカタログのレプリケーション用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="9d487-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-216">この属性の範囲は、1人のユーザーまたは連絡先によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9d487-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="9d487-217">Lync Server の有効な値 (および関連するビット位置) は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-218">0: アーカイブしない (ビットセットなし)</span><span class="sxs-lookup"><span data-stu-id="9d487-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="9d487-219">1: 廃止 (ビット位置 0)</span><span class="sxs-lookup"><span data-stu-id="9d487-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="9d487-220">2: 廃止 (ビット位置 1)</span><span class="sxs-lookup"><span data-stu-id="9d487-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="9d487-221">4: 内部通信をアーカイブする (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-222">8: フェデレーション通信をアーカイブする (ビット位置 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="9d487-223">Live Communications Server 2005 で以前に有効になっていた値は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-224">0: Msrtcsip-userenabled true によって定義された既定値を使用します。これは、次の優先順位で、 <strong>アーカイブの既定</strong> と <strong>msrtcsip-userenabled true フェデレーション</strong> によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-225">1: アーカイブ</span><span class="sxs-lookup"><span data-stu-id="9d487-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="9d487-226">2: アーカイブしない</span><span class="sxs-lookup"><span data-stu-id="9d487-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="9d487-227">3: メッセージ本文を含まないアーカイブ</span><span class="sxs-lookup"><span data-stu-id="9d487-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="9d487-228">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-229">Msrtcsip-userenabled true-ArchivingServerData (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-230">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-231">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-232">Msrtcsip-userenabled true-ArchivingServerVersion (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-233">この属性は、アーカイブサービスのバージョンを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="9d487-234">この属性は、各公式の製品リリースによってインクリメントされる monotonously の増加整数型です。</span><span class="sxs-lookup"><span data-stu-id="9d487-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="9d487-235">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-236">未定義: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d487-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="9d487-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="9d487-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="9d487-238">Live Communications Server 2005 SP1</span><span class="sxs-lookup"><span data-stu-id="9d487-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="9d487-239">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9d487-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="9d487-240">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9d487-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-241">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-242">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-243">Msrtcsip-userenabled true-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="9d487-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="9d487-244">この属性は、プールのバックエンドサーバーの FQDN を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="9d487-245">バックエンドサーバーは1つのプールにつき1つしか存在できないため、これは単一値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="9d487-246">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-247">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-248">Msrtcsip-userenabled true-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="9d487-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="9d487-249">この属性には、会議ディレクトリをホストするプールの識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="9d487-250">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-251">Msrtcsip-userenabled true-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="9d487-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="9d487-252">この属性には、会議ディレクトリの識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="9d487-253">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-254">Msrtcsip-userenabled true-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="9d487-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="9d487-255">この属性には、会議ディレクトリの移動先のプールの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="9d487-256">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-257">Msrtcsip-userenabled true-既定値</span><span class="sxs-lookup"><span data-stu-id="9d487-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="9d487-258">このブール値の属性は、電話の使用状況が既定で使用されているかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="9d487-259">この属性が <strong>TRUE</strong>に設定されている場合、電話の使用状況は既定で使用されているため、管理者は削除できません。</span><span class="sxs-lookup"><span data-stu-id="9d487-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="9d487-260">この属性が <strong>FALSE</strong>に設定されている場合、使用法は削除できます。</span><span class="sxs-lookup"><span data-stu-id="9d487-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="9d487-261">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-262">Msrtcsip-userenabled true-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="9d487-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="9d487-263">この属性は、組織外のユーザーの Communicator Web Access URL を識別します。</span><span class="sxs-lookup"><span data-stu-id="9d487-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="9d487-264">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-265">Msrtcsip-userenabled true-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="9d487-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="9d487-266">この属性は、組織内のユーザーの Communicator Web Access URL を識別します。</span><span class="sxs-lookup"><span data-stu-id="9d487-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="9d487-267">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-268">Msrtcsip-userenabled true-DefaultLocationProfileLink (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-269">この単一値の属性には、割り当てられた位置情報プロファイルクラスオブジェクトの識別名 (DN) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="9d487-270">転送リンク: <strong>リンク ID 11036</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="9d487-271">対応する後方リンクは、 <strong>msrtcsip-userenabled true-ServerReferenceBL</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-272">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-273">Msrtcsip-userenabled true-DefaultPolicy (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-274">このブール属性は、ポリシーが既定のポリシーであるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="9d487-275">ポリシーは、 <strong>TRUE</strong>に設定されている場合の既定のポリシーです。</span><span class="sxs-lookup"><span data-stu-id="9d487-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-276">Office Communications Server 2007 の新製品</span><span class="sxs-lookup"><span data-stu-id="9d487-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="9d487-277">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-278">Msrtcsip-userenabled true-DefaultRouteToEdgeProxy (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-279">この属性は、アクセスエッジサービスを実行しているエッジサーバーの FQDN (access edge サービスを実行しているサーバーのプールに直接アクセスできるか、またはハードウェアロードバランサー) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="9d487-280">アクセスエッジサービスを実行しているサーバーが1つ以上のディレクターを介してのみアクセスできる場合、この属性は、ディレクタープールを提供するディレクターまたはハードウェアロードバランサーのポート番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="9d487-281">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-282">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-283">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-284">Msrtcsip-userenabled true-DefaultRouteToEdgeProxyPort (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-285">この属性は、アクセスエッジサービスを実行しているサーバーへの接続に使用するポート番号を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="9d487-286">有効な値は、使用するポートを指定する整数値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="9d487-287">既定値は5061です。</span><span class="sxs-lookup"><span data-stu-id="9d487-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="9d487-288">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-289">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-290">Msrtcsip-userenabled true-DefPresenceSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-291">この属性は、既定のプレゼンスサブスクリプションのタイムアウト期間を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="9d487-292">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-293">Msrtcsip-userenabled true-DefRegistrationTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-294">この属性は、既定の登録タイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-295">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-296">Msrtcsip-userenabled true-DefRoamingDataSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-297">この属性は、既定のローミングデータサブスクリプションのタイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-298">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="9d487-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="9d487-300">この属性は、分割ドメイントポロジで使用され、完全修飾ドメイン名 (FQDN) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="9d487-301">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-302">Msrtcsip-userenabled true-Description (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-303">この単一値の UNICODE 文字列属性には、この電話ルートまたは正規化ルールのわかりやすい説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="9d487-304">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-305">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-306">Msrtcsip-userenabled true-DomainData</span><span class="sxs-lookup"><span data-stu-id="9d487-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="9d487-307">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-308">Msrtcsip-userenabled true-ドメイン名</span><span class="sxs-lookup"><span data-stu-id="9d487-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="9d487-309">この属性は、レジストラー用に構成されているドメインを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-310">Msrtcsip-userenabled true-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="9d487-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="9d487-311">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-312">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-313">Msrtcsip-userenabled true-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="9d487-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-314">この属性は、Access Edge サービスを実行しているサーバーの FQDN を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="9d487-315">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-316">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-317">Msrtcsip-userenabled true-EnableBestEffortNotify (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-318">この属性は、クライアントからの SUBSCRIBE 要求に応じて、サーバーが NOTIFY 要求ではなく、ベストエフォート通知 (BENOTIFY) 要求を生成するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="9d487-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="9d487-319">BENOTIFY は、通常の通知要求の代わりにサーバーが BENOTIFY 要求を生成する、サブスクライブ通知ハンドシェイクのパフォーマンス強化された拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="9d487-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="9d487-320">パフォーマンスの利点は、通知要求によって、BENOTIFY 要求でクライアントから 200 OK 応答が要求されないことです。</span><span class="sxs-lookup"><span data-stu-id="9d487-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="9d487-321">有効な値は、 <strong>TRUE</strong> または <strong>FALSE</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9d487-322">Live Communications Server 2003 は BENOTIFY 要求をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9d487-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="9d487-323">Live communications server の2005とサードパーティのサーバーで実行されている Live Communications Server 2003 server API で記述されたサーバーアプリケーションと相互運用するには、BENOTIFY 要求の値を <STRONG>FALSE</STRONG>に設定して無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9d487-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="9d487-324">現在、BENOTIFY は IETF (インターネットエンジニアリングタスクフォース) SIP 標準化プロセスの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="9d487-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="9d487-325">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-326">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-327">Msrtcsip-userenabled true-EnableFederation (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-328">この属性は、IT 管理者が他の組織のユーザーとの通信を許可するかどうかを構成するために使用するグローバルスイッチです。</span><span class="sxs-lookup"><span data-stu-id="9d487-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="9d487-329">管理者が個々のユーザーの <strong>FederationEnabled</strong> 属性を上書きできるようにします。</span><span class="sxs-lookup"><span data-stu-id="9d487-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="9d487-330">この属性は、ワーム、ウイルス、または企業の標的となる攻撃によって発生する可能性があるインターネット攻撃から内部ネットワークを保護するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9d487-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="9d487-331">有効な値 (および関連するビット位置) は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-332">1: パブリック IM 接続を有効にする (ビット位置 0)</span><span class="sxs-lookup"><span data-stu-id="9d487-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="9d487-333">2: 予約済み (ビット位置 1)</span><span class="sxs-lookup"><span data-stu-id="9d487-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="9d487-334">4: 予約済み (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-335">8: 予約済み (ビット位置 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="9d487-336">16: リモート通話コントロールが有効になっている [Telephony] (ビット位置 4)</span><span class="sxs-lookup"><span data-stu-id="9d487-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="9d487-337">64: AllowOrganizeMeetingWithAnonymousParticipants (ユーザーが会議に匿名ユーザーを招待することを許可する (ビット位置 6)</span><span class="sxs-lookup"><span data-stu-id="9d487-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="9d487-338">128: UCEnabled (ユニファイドコミュニケーションのためのユーザーの有効化) (ビット位置 7)</span><span class="sxs-lookup"><span data-stu-id="9d487-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="9d487-339">256: EnabledForEnhancedPresence (ユーザーにパブリック IM 接続を有効にする) (ビット位置 8)</span><span class="sxs-lookup"><span data-stu-id="9d487-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="9d487-340">512: RemoteCallControlDualMode (ビット位置 9)</span><span class="sxs-lookup"><span data-stu-id="9d487-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-341">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-342">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-343">Msrtcsip-userenabled true-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="9d487-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="9d487-344">この属性は、エンタープライズサービスが指定されたサーバーに読み込まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9d487-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-345">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="9d487-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="9d487-346">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-347">Msrtcsip-userenabled true-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="9d487-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="9d487-348">この属性には、外部アクセスのダイヤルコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="9d487-349">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-350">Msrtcsip-userenabled true-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="9d487-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="9d487-351">この属性は、1人のユーザーがフェデレーションを有効にしているかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="9d487-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="9d487-352">エンタープライズサービスレイヤーによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="9d487-353">グローバルカタログのレプリケーション用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="9d487-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-354">有効な値は、 <strong>TRUE</strong> または <strong>FALSE</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-355">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-356">Msrtcsip-userenabled true-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="9d487-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="9d487-357">この属性は、プールに関連付けられたすべての Enterprise Edition サーバーのドメイン名の複数値を持つ一覧です。</span><span class="sxs-lookup"><span data-stu-id="9d487-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="9d487-358">戻るリンク: <strong>リンク ID 11023</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="9d487-359">この戻るリンクへの対応する前方リンクは <strong>msrtcsip-userenabled true の住所</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-360">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-361">Msrtcsip-userenabled true-ゲートウェイ (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-362">この複数値文字列属性には、ゲートウェイとポート (ゲートウェイごと) の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="9d487-363">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-364">Msrtcsip-userenabled true-GlobalSettingsData (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-365">この属性には、名前と値のペアが格納されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="9d487-366">既に定義された名前: 値のペアは、プレゼンス設定の [ <strong>ポーリングを許可</strong> する] に対応しています。</span><span class="sxs-lookup"><span data-stu-id="9d487-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="9d487-367">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-368">Msrtcsip-userenabled true-GroupingID</span><span class="sxs-lookup"><span data-stu-id="9d487-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="9d487-369">この属性は、アドレス帳のエントリをグループ化するために使用されるグループの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="9d487-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="9d487-370">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-371">Msrtcsip-userenabled true-HomeServer (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-372">最新のライブ通信サーバー 2003 (使用されていません)。</span><span class="sxs-lookup"><span data-stu-id="9d487-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="9d487-373">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-374">Msrtcsip-userenabled true-HomeServerString (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-375">Live Communications Server 2003 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="9d487-376">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-377">Msrtcsip-userenabled true-ホームユーザー (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-378">最新のライブ通信サーバー 2003 (使用されていません)。</span><span class="sxs-lookup"><span data-stu-id="9d487-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="9d487-379">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-380">Msrtcsip-userenabled true-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="9d487-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="9d487-381">この属性は、1人のユーザーが外部ユーザーアクセスを有効にしているかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="9d487-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="9d487-382">エンタープライズサービスレイヤーによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="9d487-383">グローバルカタログのレプリケーション用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="9d487-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-384">有効な値は、 <strong>TRUE</strong> または <strong>FALSE</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-385">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-386">Msrtcsip-userenabled true-IsMaster (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-387">最新のライブコミュニケーションサーバー2003</span><span class="sxs-lookup"><span data-stu-id="9d487-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="9d487-388">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-389">Msrtcsip-userenabled true ライン</span><span class="sxs-lookup"><span data-stu-id="9d487-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="9d487-390">この単一値の属性には、Lync for telephony によって使用されるデバイス ID (SIP URI またはユーザーが制御する電話の TEL URI のいずれか) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="9d487-391">この属性はグローバルカタログのレプリケーション用にマークされ、インデックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="9d487-392">ユーザーがエンタープライズ Voip を有効にしている場合、この属性には、ユーザーの電話番号の E.i 正規化されたバージョンが格納されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="9d487-393">Microsoft Office Live Communications Server 2005 SP1 の新製品</span><span class="sxs-lookup"><span data-stu-id="9d487-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-394">Msrtcsip-userenabled true</span><span class="sxs-lookup"><span data-stu-id="9d487-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="9d487-395">この単一値属性には、CSTA-SIP ゲートウェイサーバーの SIP URI が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="9d487-396">この属性はグローバルカタログのレプリケーション用にマークされていますが、インデックスは作成されません。</span><span class="sxs-lookup"><span data-stu-id="9d487-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="9d487-397">Microsoft Office Live Communications Server 2005 SP1 の新製品</span><span class="sxs-lookup"><span data-stu-id="9d487-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-398">Msrtcsip-userenabled true-LocalNormalizationData (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-399">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-400">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-401">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-402">Msrtcsip-userenabled true-Localnormallinks (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-403">この複数値属性には、この場所プロファイルに関連付けられたローカル正規化識別名 (DN) の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="9d487-404">この属性の型は、DN バイナリです。</span><span class="sxs-lookup"><span data-stu-id="9d487-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="9d487-405">位置情報プロファイルとローカル正規化ルールの間には一対多のリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="9d487-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="9d487-406">ローカル正規化 DNs の一覧の順序は、管理者が指定した順序で維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d487-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="9d487-407">順序の保持は、DN バイナリのバイナリ部分によって管理されます。これにより、注文インデックスが指定されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="9d487-408">転送リンク: <strong>リンク ID 11034</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="9d487-409">この転送リンク属性への対応する "戻る" リンクは、 <strong>msrtcsip-userenabled true (プロファイル Ebl)</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-410">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-411">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-412">Msrtcsip-userenabled true-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="9d487-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="9d487-413">この属性には、正規化ルールのオプションの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="9d487-414">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-415">Msrtcsip-userenabled true-LocationName (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-416">この単一値の属性には、このプロファイルが表す場所を示す場所プロファイルのフレンドリ名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="9d487-417">複数の場所プロファイルが存在する可能性があるため、管理者はさまざまなプロファイルを区別するための方法が必要です。</span><span class="sxs-lookup"><span data-stu-id="9d487-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="9d487-418">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-419">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-420">Msrtcsip-userenabled true-locationProfileBL (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-421">この複数値属性には、場所プロファイルの識別名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="9d487-422">この属性は、1つ以上の位置情報プロファイルへの戻るリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="9d487-423">戻るリンク: <strong>リンク ID 11035</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="9d487-424">この属性は、forward link <strong>msrtcsip-userenabled true-Localnormalのリンク</strong>に対応します。</span><span class="sxs-lookup"><span data-stu-id="9d487-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-425">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-426">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-427">Msrtcsip-userenabled true-LocationProfileData (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-428">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-429">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-430">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-431">Msrtcsip-userenabled true-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="9d487-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="9d487-432">この属性には、位置情報プロファイルのオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="9d487-433">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-434">Msrtcsip-userenabled true-MappingContact</span><span class="sxs-lookup"><span data-stu-id="9d487-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="9d487-435">この複数値属性は、アプリケーションの連絡先の一覧を保持します。</span><span class="sxs-lookup"><span data-stu-id="9d487-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="9d487-436">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-437">Msrtcsip-userenabled true-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="9d487-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="9d487-438">この複数値属性は、位置情報プロファイルの一覧を保持します。</span><span class="sxs-lookup"><span data-stu-id="9d487-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="9d487-439">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-440">Msrtcsip-userenabled true-Maxnumoutスタンド Ingsearchperserver (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-441">この属性は、サーバーあたりの未処理の検索要求の最大数を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="9d487-442">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-443">Msrtcsip-userenabled true-MaxNumSubscriptionsPerUser (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-444">この属性は、ユーザーごとのサブスクリプションの最大数を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="9d487-445">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-446">Msrtcsip-userenabled true-MaxPresenceSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-447">この属性は、サブスクリプションの最大タイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-448">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-449">Msrtcsip-userenabled true-MaxRegistrationsTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-450">この属性は、登録の最大タイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-451">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-452">Msrtcsip-userenabled true-MaxRoamingDataSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-453">この属性は、最大ローミングデータサブスクリプションのタイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-454">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-455">Msrtcsip-userenabled true-MCUData</span><span class="sxs-lookup"><span data-stu-id="9d487-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="9d487-456">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-457">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-458">Msrtcsip-userenabled true-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="9d487-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="9d487-459">この属性は、属している multipoint control unit (MCU) ファクトリへのリンクを指定するコンピュータークラスの下のサービス制御ポイント属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="9d487-460">このサービス制御ポイントと属性は、Microsoft MCU ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="9d487-461">各 Microsoft MCU は、プールレベルの設定を取得するために、所属するプールのバックエンドサーバーを見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d487-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="9d487-462">この属性の値は、MCU ファクトリの識別名 (DN) です。</span><span class="sxs-lookup"><span data-stu-id="9d487-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="9d487-463">これは単一値の属性であり、グローバルカタログのレプリケーション用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="9d487-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-464">転送リンク: <strong>リンク ID 11026</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="9d487-465">この転送リンク属性への対応する "戻る" リンクは、 <strong>Msrtcsip-userenabled true MCUServers</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-466">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-467">Msrtcsip-userenabled true-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="9d487-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="9d487-468">これは、複数の文字列で予約された属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="9d487-469">この属性に格納される設定は、name = value のペアとして表されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="9d487-470">現在定義されている name = value のペア:</span><span class="sxs-lookup"><span data-stu-id="9d487-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="9d487-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-472">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-473">Msrtcsip-userenabled true-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="9d487-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="9d487-474">これは、プールに関連付けられた単一の MCU ファクトリの識別名 (DN) を含む単一値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="9d487-475">転送リンク: <strong>リンク ID 11024</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="9d487-476">この転送リンク属性への対応する "戻る" リンクは <strong>msrtcsip-userenabled true の住所</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-477">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-478">Msrtcsip-userenabled true-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="9d487-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="9d487-479">この属性は、MCU ファクトリプロバイダーの GUID を指定する単一値の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="9d487-480">MCU ファクトリプロセスは、GUID 値に基づいて、この MCU 型をサービスするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="9d487-481">GUID 値が <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>の場合は、MCU ファクトリプロセス (既定では Lync Server で利用可能) によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="9d487-482">他の GUID 値の場合、MCU ファクトリプロセスは MCU の種類を処理しません。</span><span class="sxs-lookup"><span data-stu-id="9d487-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="9d487-483">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-484">msrtcsip-userenabled true-mcuser</span><span class="sxs-lookup"><span data-stu-id="9d487-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="9d487-485">この属性は、複数値を持つ識別名 (DN) の一覧です。</span><span class="sxs-lookup"><span data-stu-id="9d487-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="9d487-486">この属性には、この MCU ファクトリに関連付けられている同じ種類とベンダーのすべての MCU サーバーの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="9d487-487">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="9d487-488">戻るリンク: リンク ID 11027</span><span class="sxs-lookup"><span data-stu-id="9d487-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="9d487-489">この戻るリンクへの対応する前方リンクは <strong>Msrtcsip-userenabled true MCUFactoryAddress</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-490">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-491">Msrtcsip-userenabled true-MCUType</span><span class="sxs-lookup"><span data-stu-id="9d487-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="9d487-492">この属性は、MCU が処理できる媒体を指定する単一値の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="9d487-493">サポートされている有効な形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-494">会議</span><span class="sxs-lookup"><span data-stu-id="9d487-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="9d487-495">オーディオ-ビデオ</span><span class="sxs-lookup"><span data-stu-id="9d487-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="9d487-496">チャット</span><span class="sxs-lookup"><span data-stu-id="9d487-496">chat</span></span></p></li>
<li><p><span data-ttu-id="9d487-497">電話-conf</span><span class="sxs-lookup"><span data-stu-id="9d487-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-498">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-499">Msrtcsip-userenabled true-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="9d487-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="9d487-500">この属性は、MCU ベンダーの名前を指定する単一値の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="9d487-501">Microsoft のすべての Mcu は、この属性を <strong>Microsoft Corporation</strong>に指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-502">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-503">Msrtcsip-userenabled true-会議フラグ (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-504">この属性は、すべてのユーザーまたは連絡先オブジェクトでグローバルに有効になるさまざまな会議オプションを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="9d487-505">この属性は、整数型のビットマスク値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="9d487-506">有効な値 (および関連するビット位置) は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-507">0: AllowOrganizeMeetingWithAnonymousParticipants が None (ユーザーが会議に匿名ユーザーを招待することを許可しない) (bits は設定されません)</span><span class="sxs-lookup"><span data-stu-id="9d487-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="9d487-508">4: AllowOrganizeMeetingWithAnonymousParticipants はすべてのユーザー (すべてのユーザーが会議に匿名ユーザーを招待することを許可します) (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-509">8: AllowOrganizeMeetingWithAnonymousParticipants は UsePerUserSetting (ユーザーごとの設定に基づいてユーザーが会議に匿名ユーザーを招待できるようにします) (ビット位置 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="9d487-510">16: Userperuser会議ポリシー (会議ポリシーはユーザーごとに定義されます) (ビット位置 4)</span><span class="sxs-lookup"><span data-stu-id="9d487-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-511">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-512">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-513">Msrtcsip-userenabled true-会議ポリシー (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-514">この属性は、管理者がこのユーザーに割り当てたポリシーの識別名 (DN) を単一値の属性として指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="9d487-515">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-516">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-517">Msrtcsip-userenabled true-MinPresenceSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-518">この属性は、最小プレゼンスサブスクリプションのタイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-519">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-520">Msrtcsip-userenabled true-MinRegistrationTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-521">この属性は、最小登録タイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-522">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-523">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-524">Msrtcsip-userenabled true-MinRoamingDataSubscriptionTimeout (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-525">この属性は、最小のローミングデータサブスクリプションのタイムアウトウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="9d487-526">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-527">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-528">Msrtcsip-userenabled true-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="9d487-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="9d487-529">この属性は、フロントエンドプールによって使用されるミラー化された SQL Server バックエンドを格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="9d487-530">Lync Server 2013 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-531">Msrtcsip-userenabled true-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="9d487-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="9d487-532">この属性には、モビリティー設定を定義するオプションとフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="9d487-533">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-534">Msrtcsip-userenabled true-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9d487-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="9d487-535">この属性には、モビリティーポリシーオブジェクトの DN が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="9d487-536">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-537">Msrtcsip-userenabled true-NumDevicesPerUser (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-538">この属性は、ユーザーが SIP コミュニケーションに登録してプレゼンスをサブスクライブできるデバイスの許可された数を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="9d487-539">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-540">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-541">Msrtcsip-userenabled true-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="9d487-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="9d487-542">この属性は、ユーザーまたは連絡先オブジェクトに対して有効になるオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="9d487-543">この属性は、integer 型のビットマスク値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="9d487-544">各オプションは1ビットで表されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-544">Each option is represented by a bit.</span></span> <span data-ttu-id="9d487-545">この属性は、グローバルカタログのレプリケーション用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="9d487-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-546">有効な値 (および関連するビット位置) は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-547">1: パブリックインスタントメッセージング (IM) 接続を有効にします (ビット位置 0)。</span><span class="sxs-lookup"><span data-stu-id="9d487-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="9d487-548">2: 予約済み (ビット位置 1)</span><span class="sxs-lookup"><span data-stu-id="9d487-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="9d487-549">4: 予約済み (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-550">8: 予約済み (ビット位置 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="9d487-551">16: リモート通話コントロールが有効になっている [Telephony] (ビット位置 4)</span><span class="sxs-lookup"><span data-stu-id="9d487-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="9d487-552">64: AllowOrganizeMeetingWithAnonymousParticipants (ユーザーが会議に匿名ユーザーを招待することを許可する (ビット位置 6)</span><span class="sxs-lookup"><span data-stu-id="9d487-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="9d487-553">128: UCEnabled (UC でのユーザーの有効化) (ビット位置 7)</span><span class="sxs-lookup"><span data-stu-id="9d487-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="9d487-554">256: EnabledForEnhancedPresence (ユーザーにパブリック IM 接続を有効にする) (ビット位置 8)</span><span class="sxs-lookup"><span data-stu-id="9d487-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="9d487-555">512: RemoteCallControlDualMode (ビット位置 9)</span><span class="sxs-lookup"><span data-stu-id="9d487-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-556">SP1 での最新のライブ通信サーバー2005。</span><span class="sxs-lookup"><span data-stu-id="9d487-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="9d487-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="9d487-558">この属性は、リソースおよび中央フォレストトポロジで使用され、Windows NT Server プリンシパルアカウントからのユーザーの ObjectSID が、リソースまたは中央フォレストの対応するユーザーまたは連絡先オブジェクトのこの属性にコピーされた場合に、シングルサインオンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9d487-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="9d487-559">Communicator Web Access は、この属性またはユーザーの ObjectSID を使用して、AD DS 内のユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="9d487-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="9d487-560">この属性は、グローバルカタログのレプリケーション用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="9d487-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-561">Msrtcsip-userenabled true-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="9d487-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="9d487-562">この属性は、アプリケーションの連絡先の所有者の Uniform Resource Name (URN) です。</span><span class="sxs-lookup"><span data-stu-id="9d487-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="9d487-563">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-564">Msrtcsip-userenabled true-Pattern (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-565">この単一値文字列属性には、ダイヤル番号を E.i 形式に一致させるために使われるパターンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="9d487-566">ダイヤル番号がこのパターンと一致する場合、翻訳はダイヤルされた番号に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="9d487-567">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-568">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-569">Msrtcsip-userenabled true-PhoneRouteBL (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-570">この複数値属性には、電話ルートの識別名 (DN) の一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="9d487-571">この属性は、1つ以上の電話ルートへの戻るリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="9d487-572">戻るリンク: <strong>リンク ID 11033</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="9d487-573">この属性は、 <strong>msrtcsip-userenabled true-RouteUsageLinks</strong>の前方リンクに対応しています。</span><span class="sxs-lookup"><span data-stu-id="9d487-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-574">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-575">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-576">Msrtcsip-userenabled true-PhoneRouteData (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-577">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-578">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-579">Msrtcsip-userenabled true-PhoneRouteName (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-580">この単一の値の UNICODE 文字列属性は、電話ルートのフレンドリ名を指定するため、管理者が簡単に参照できます。</span><span class="sxs-lookup"><span data-stu-id="9d487-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="9d487-581">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-582">Msrtcsip-userenabled true-電話の使用データ (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-583">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-584">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-585">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-586">Msrtcsip-userenabled true-ポリシーのコンテンツ (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-587">この属性は、単一の値を持つ Unicode 文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="9d487-588">この文字列属性には、XML 形式のポリシー定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="9d487-589">XML スキーマ定義は、ポリシーの種類によって共通していますが、ポリシーの種類によって設定は異なります。</span><span class="sxs-lookup"><span data-stu-id="9d487-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="9d487-590">XML スキーマ定義 (XSD) は、次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="9d487-591">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-592">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-593">Msrtcsip-userenabled true-ポリシーデータ (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-594">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-595">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-596">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-597">Msrtcsip-userenabled true-PolicyType (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-598">この単一値の Unicode 文字列属性には、ポリシー型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="9d487-599">有効なポリシーの種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-600">会議</span><span class="sxs-lookup"><span data-stu-id="9d487-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="9d487-601">電話</span><span class="sxs-lookup"><span data-stu-id="9d487-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-602">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-603">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-604">Msrtcsip-userenabled true-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="9d487-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="9d487-605">この属性は、コンピューターが属しているプールへのリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="9d487-606">この属性は、コンピューターで実行されているのが標準エディションであるか、エンタープライズ版の Lync Server であるかに関係なく設定されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="9d487-607">この属性は、グローバルカタログのレプリケーション用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="9d487-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="9d487-608">有効な値は、プールのドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="9d487-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="9d487-609">転送リンク: <strong>リンク ID 11022</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="9d487-610">この転送リンク属性への対応する "戻る" リンクは、 <strong>msrtcsip-userenabled true-FrontEndServers</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-611">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-612">Msrtcsip-userenabled true-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="9d487-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="9d487-613">これは、MCU ファクトリが関連付けられているプールの識別名 (DN) の一覧を含む複数値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="9d487-614">戻るリンク: <strong>リンク ID 11025</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="9d487-615">この戻るリンクへの対応する前方リンクは <strong>Msrtcsip-userenabled true MCUFactoryPath</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-616">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-617">Msrtcsip-userenabled true-PoolData</span><span class="sxs-lookup"><span data-stu-id="9d487-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="9d487-618">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-619">SP1 での最新のライブ通信サーバー2005。</span><span class="sxs-lookup"><span data-stu-id="9d487-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-620">Msrtcsip-userenabled true-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="9d487-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="9d487-621">この属性は、管理コンソールによって表示されるプールの任意の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="9d487-622">この名前は管理者が変更できます。</span><span class="sxs-lookup"><span data-stu-id="9d487-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="9d487-623">有効な値は、プールの名前を表す文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="9d487-624">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-625">Msrtcsip-userenabled true-Pooldomaqdn</span><span class="sxs-lookup"><span data-stu-id="9d487-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-626">この属性は単一値文字列値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="9d487-627">この属性の値が指定されている場合、管理者が、フロントエンドプールを作成する Active Directory ドメイン構造に準拠していない (たとえば、Domain Name System (DNS) 名前空間から分離した SIP 名前空間) というプールのドメイン FQDN を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="9d487-628">プールが存在する Active Directory ドメインとして、フロントエンドプールドメイン FQDN をドメイン名部分にマッピングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9d487-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="9d487-629">そのため、この属性に値が含まれていない場合、フロントエンドプールの FQDN は、 <strong>dnsHostName</strong> 属性で示される Active Directory ドメイン名の構造体に既定値として設定されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="9d487-630">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-631">Msrtcsip-userenabled true-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="9d487-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="9d487-632">プールに関連付けられたすべての Lync Server Enterprise Edition サーバーのドメイン名の複数値を持つリスト。</span><span class="sxs-lookup"><span data-stu-id="9d487-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="9d487-633">Integer 型の属性は、プールがインスタントメッセージング (IM) とプレゼンス、会議に対応しているかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="9d487-634">有効な値の型は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-635">未定義: IM とプレゼンスサービス (Live Communications Server 2005 および 2003)</span><span class="sxs-lookup"><span data-stu-id="9d487-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="9d487-636">1: IM とプレゼンスサービス (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="9d487-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="9d487-637">2: IM、プレゼンス、会議サービス (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="9d487-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-638">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-639">Msrtcsip-userenabled true-PoolType</span><span class="sxs-lookup"><span data-stu-id="9d487-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="9d487-640">この属性は、サーバープールで Standard Edition server または Enterprise Edition server が実行されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="9d487-641">この属性は、integer 型のビットマスク値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="9d487-642">各オプションは1ビットで表されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="9d487-643">有効な値 (および関連するビット位置) は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-644">1: Standard Edition server、ホストユーザー (ビット位置 0)</span><span class="sxs-lookup"><span data-stu-id="9d487-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="9d487-645">2: Enterprise Edition server、hosts ユーザー (ビット位置 1)</span><span class="sxs-lookup"><span data-stu-id="9d487-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="9d487-646">4: 標準エディションサーバー、ホストアプリケーション (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-647">8: Enterprise Edition server、ホストアプリケーション (ビット位置 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="9d487-648">Lync Server はアプリケーションのみをホストするプールをサポートしていないため、有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-649">5: 標準エディションサーバー、ホストユーザーとアプリケーション (ビット位置0、2)</span><span class="sxs-lookup"><span data-stu-id="9d487-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="9d487-650">10: Enterprise Edition server、ホストユーザーとアプリケーション (ビット位置1と 3)</span><span class="sxs-lookup"><span data-stu-id="9d487-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-651">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-652">Msrtcsip-userenabled true-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="9d487-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="9d487-653">この属性はプールのバージョンを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-653">This attribute defines the pool version.</span></span> <span data-ttu-id="9d487-654">これは、主要製品のリリースごとにインクリメントされる整数型です。</span><span class="sxs-lookup"><span data-stu-id="9d487-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="9d487-655">有効な値の型は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-656">0: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d487-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="9d487-657">1: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="9d487-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="9d487-658">2: SP1 での Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="9d487-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="9d487-659">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9d487-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="9d487-660">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9d487-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="9d487-661">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9d487-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-662">Live Communications Server 2005 SP1</span><span class="sxs-lookup"><span data-stu-id="9d487-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-663">Msrtcsip-userenabled true-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="9d487-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="9d487-664">この属性には、プレゼンス設定を定義するオプションとフラグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="9d487-665">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-666">Msrtcsip-userenabled true-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="9d487-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="9d487-667">この属性には、プレゼンスポリシーオブジェクトの DN が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="9d487-668">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-669">Msrtcsip-userenabled true-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="9d487-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="9d487-670">この属性によって、SIP メッセージングのユーザーまたは連絡先が有効になります。</span><span class="sxs-lookup"><span data-stu-id="9d487-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="9d487-671">この機能は、中央フォレストのトポロジでは、ユーザーオブジェクトではなく SIP 対応の連絡先オブジェクトであるため、連絡先クラスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="9d487-672">有効な値は、ユーザーが所属する Standard Edition server または Enterprise Edition のフロントエンドプールの DN です。</span><span class="sxs-lookup"><span data-stu-id="9d487-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="9d487-673">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="9d487-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="9d487-675">この属性には、特定のユーザーの SIP アドレスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-676">Msrtcsip-userenabled true-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="9d487-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="9d487-677">この属性には、プライベート回線デバイスのデバイス ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="9d487-678">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-679">Msrtcsip-userenabled true-ルーティング可能</span><span class="sxs-lookup"><span data-stu-id="9d487-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="9d487-680">この属性は、Lync Server がその GRUU アドレスを使ってこのサービスにルーティングすることを許可するかどうかを決定するために使用されるブール型の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="9d487-681">この値が <strong>TRUE</strong>に設定されている場合、Lync Server はこのサービスにルーティングすることを許可されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="9d487-682">この値が <strong>FALSE</strong>に設定されている場合、Lync Server はこのサービスにルーティングする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="9d487-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="9d487-683">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-684">Msrtcsip-userenabled true-RouteUsageAttribute (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-685">この単一値の UNICODE 文字列属性は、電話ルートの使用を限定する属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="9d487-686">電話ルートの選択は、電話ルートに割り当てられる利用属性と、発信者に許可されているポリシー使用属性の2つの要素に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="9d487-687">呼び出し元の使用が許可されている使用法属性を持つ最初の電話ルートが選択されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="9d487-688">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-689">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-690">Msrtcsip-userenabled true-RouteUsageLinks (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-691">この複数値識別名 (DN) 属性には、ルートの使用の識別名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="9d487-692">転送リンク: <strong>リンク ID 11032</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="9d487-693">この属性は、対応する back link <strong>msrtcsip-userenabled true-PhoneRouteBL</strong>への転送リンクです。</span><span class="sxs-lookup"><span data-stu-id="9d487-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-694">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-695">Msrtcsip-userenabled true-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="9d487-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-696">この属性には、この MCU または信頼されたサービスに宛てたすべての SIP トラフィックが通過する必要があるプールを指す DN が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="9d487-697">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-698">Msrtcsip-userenabled true-RuleName (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-699">この単一値の UNICODE 文字列属性は、正規化ルールのフレンドリ名を指定するため、管理者が簡単に参照できます。</span><span class="sxs-lookup"><span data-stu-id="9d487-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="9d487-700">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-701">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-702">Msrtcsip-userenabled true-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="9d487-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="9d487-703">この属性は、組織に現在展開されているスキーマバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-704">Msrtcsip-userenabled true-SearchMaxRequests (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-705">この属性は、ユーザーが Communicator を使って連絡先を検索するときに、ディレクトリ検索から返される検索結果の数を制限します。</span><span class="sxs-lookup"><span data-stu-id="9d487-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="9d487-706">この属性は、クライアントによって指定された値を上書きします。</span><span class="sxs-lookup"><span data-stu-id="9d487-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="9d487-707">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-708">Msrtcsip-userenabled true-SearchMaxResults (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-709">この属性は、返される検索要求の数を制限します。</span><span class="sxs-lookup"><span data-stu-id="9d487-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="9d487-710">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-711">Msrtcsip-userenabled true-ServerBL</span><span class="sxs-lookup"><span data-stu-id="9d487-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="9d487-712">この複数値属性は、識別名 (DN) の一覧を含む戻るリンクです。</span><span class="sxs-lookup"><span data-stu-id="9d487-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="9d487-713">これらの DNs はプールまたは <strong>Trustedservice</strong> オブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="9d487-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="9d487-714">この属性は、 <strong>msrtcsip-userenabled true-TrustedServiceLinks</strong>の前方リンクに対応しています。</span><span class="sxs-lookup"><span data-stu-id="9d487-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-715">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-716">Msrtcsip-userenabled true-ServerData</span><span class="sxs-lookup"><span data-stu-id="9d487-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="9d487-717">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-718">Msrtcsip-userenabled true-ServerReferenceBL (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-719">この複数値属性には、識別名のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="9d487-720">これらの識別名は、既定の場所プロファイルを割り当てることができる他のサーバーオブジェクトを参照する戻るリンクです。</span><span class="sxs-lookup"><span data-stu-id="9d487-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="9d487-721">戻るリンク: <strong>リンク ID 11037</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="9d487-722">この戻るリンクへの対応する前方リンクは <strong>msrtcsip-userenabled true-DefaultLocationProfileLink</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="9d487-723">この back link 属性は、プールおよび仲介サーバーのみを参照します。</span><span class="sxs-lookup"><span data-stu-id="9d487-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="9d487-724">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-725">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-726">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9d487-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="9d487-727">この属性は、サーバーのバージョン情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="9d487-728">このバージョン番号は、すべてのサーバーの役割に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-728">This version number applies to all server roles.</span></span> <span data-ttu-id="9d487-729">これは、各公式の製品リリースによって増加する monotonously 整数です。</span><span class="sxs-lookup"><span data-stu-id="9d487-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="9d487-730">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-731">未定義: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d487-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="9d487-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="9d487-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="9d487-733">Live Communications Server 2005 SP1</span><span class="sxs-lookup"><span data-stu-id="9d487-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="9d487-734">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9d487-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="9d487-735">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9d487-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="9d487-736">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9d487-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="9d487-737">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d487-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-738">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-739">Msrtcsip-userenabled true-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="9d487-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="9d487-740">Integer 型の単一値属性は、次のように、 <strong>SourceObjectDN</strong> が指すオブジェクトの型を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-741">null |0x00000001: 別のフォレストから Windows NT Server プリンシパルユーザーオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="9d487-742">次の属性は、配布グループの展開用に別のフォレストからのグループの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="9d487-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="9d487-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="9d487-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="9d487-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="9d487-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="9d487-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="9d487-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="9d487-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="9d487-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="9d487-748">0x90000000: 同じフォレストまたは別のフォレストからの自動応答またはサブスクライバーのアクセスオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="9d487-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="9d487-749">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-750">Msrtcsip-userenabled true-SubscriptionAuthRequired (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-751">Live Communications Server 2003 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="9d487-752">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-753">Msrtcsip-userenabled true-Targethoのメッセージ</span><span class="sxs-lookup"><span data-stu-id="9d487-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="9d487-754">この属性によって、ユーザーまたは連絡先オブジェクトを、Lync Server プール間で移動することができます。</span><span class="sxs-lookup"><span data-stu-id="9d487-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="9d487-755">この属性は、中央フォレストのトポロジでは、ユーザーオブジェクトではなく、SIP が有効になるため、contact クラスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="9d487-756">有効な値は、ユーザーが移動するターゲットの Standard Edition サーバーまたはフロントエンドプールの DN です。</span><span class="sxs-lookup"><span data-stu-id="9d487-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="9d487-757">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-758">Msrtcsip-userenabled true-TargetPhoneNumber (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-759">この単一値文字列属性には、 <strong>msrtcsip-userenabled true</strong>で定義されたゲートウェイにルーティングするための電話番号のパターンまたは範囲が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-760">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-761">Msrtcsip-userenabled true-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="9d487-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="9d487-762">この属性は、Lync Server ユーザーのターゲットポリシーの名前と値のペアを格納します。</span><span class="sxs-lookup"><span data-stu-id="9d487-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="9d487-763">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-764">Msrtcsip-userenabled true-TenantId</span><span class="sxs-lookup"><span data-stu-id="9d487-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="9d487-765">この属性には、テナントの一意の識別子が格納されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="9d487-766">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-767">Msrtcsip-userenabled true-翻訳 (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-768">この属性は、Lync Server の音声機能によって使用され、一致が見つかった場合は、ダイヤルした番号に適用する翻訳文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="9d487-769">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="9d487-770">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-771">Msrtcsip-userenabled true-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="9d487-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="9d487-772">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-773">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-774">Msrtcsip-userenabled true-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="9d487-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-775">この属性は、MCU の FQDN を含む文字列値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="9d487-776">これは単一値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-776">This is a single-valued attribute.</span></span> <span data-ttu-id="9d487-777">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-778">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-779">Msrtcsip-userenabled true-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="9d487-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="9d487-780">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-781">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-782">Msrtcsip-userenabled true-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="9d487-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-783">この属性は、プロキシサーバーを実行しているサーバーの FQDN を含む文字列値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="9d487-784">この属性は単一値になります。</span><span class="sxs-lookup"><span data-stu-id="9d487-784">This attribute is single-valued.</span></span> <span data-ttu-id="9d487-785">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-786">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-787">Msrtcsip-userenabled true-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="9d487-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="9d487-788">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-789">Msrtcsip-userenabled true-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="9d487-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-790">この属性は、信頼されたサーバーの FQDN を表す単一値属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="9d487-791">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-792">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="9d487-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="9d487-793">この属性は、信頼されたサーバーの一覧にあるサーバーのバージョン番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="9d487-794">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-795">NULL: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d487-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="9d487-796">2: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="9d487-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="9d487-797">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9d487-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="9d487-798">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9d487-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="9d487-799">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9d487-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="9d487-800">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d487-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-801">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-802">Msrtcsip-userenabled true-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="9d487-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="9d487-803">この属性は、信頼されたサービスに対して有効になるオプションを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="9d487-804">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-805">Msrtcsip-userenabled true-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="9d487-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="9d487-806">この複数値属性には、メディアリレー認証サービスなどの信頼されたサービスオブジェクトを参照する識別名 (DN) の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="9d487-807">リモートユーザー向けのオーディオシナリオをサポートするには、メディアリレー認証サービス (A/V 会議サービスを実行しているエッジサーバーに物理的に併置されているサービス) がプールに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d487-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="9d487-808">この転送リンク属性への対応する [戻る] リンクは、 <strong>msrtcsip-userenabled true-ServerBL</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-809">コミュニケーション</span><span class="sxs-lookup"><span data-stu-id="9d487-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-810">Msrtcsip-userenabled true-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="9d487-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="9d487-811">この属性は、この GRUU サービスへの接続に使用するポート番号を定義する整数です。</span><span class="sxs-lookup"><span data-stu-id="9d487-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="9d487-812">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-813">Msrtcsip-userenabled true-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="9d487-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="9d487-814">この属性は、GRUU サービスの型を定義する文字列値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="9d487-815">有効な GRUU サービスの種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-816">MediationServer</span><span class="sxs-lookup"><span data-stu-id="9d487-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="9d487-817">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="9d487-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="9d487-818">メディアリレー認証サービス (MRAS)</span><span class="sxs-lookup"><span data-stu-id="9d487-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="9d487-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="9d487-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="9d487-820">Msrtcsip-userenabled true-UserExtension CWA</span><span class="sxs-lookup"><span data-stu-id="9d487-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-821">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-822">Msrtcsip-userenabled true-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="9d487-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="9d487-823">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-824">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-825">Msrtcsip-userenabled true-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="9d487-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="9d487-826">この属性は、Lync Server Web サービスが実行されている IIS の FQDN を含む文字列値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="9d487-827">これは単一値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-827">This is a single-valued attribute.</span></span> <span data-ttu-id="9d487-828">各セグメントの有効な値は、63文字です。FQDN 全体の有効な値は、255文字です。</span><span class="sxs-lookup"><span data-stu-id="9d487-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="9d487-829">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-830">Msrtcsip-userenabled true-UCFlags (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-831">この属性は、すべてのユーザーオブジェクトまたは連絡先オブジェクトでグローバルに有効になるさまざまな UC オプションを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d487-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="9d487-832">この属性は、整数型のビットマスク値です。</span><span class="sxs-lookup"><span data-stu-id="9d487-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="9d487-833">各オプションはビットが存在することで表されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="9d487-834">有効な値 (および関連するビット位置) は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9d487-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-835">4: Peruserucpolicy (ビット位置 2)</span><span class="sxs-lookup"><span data-stu-id="9d487-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="9d487-836">このビットが設定されると、ユーザーごとに UC ポリシーが定義されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="9d487-837">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-838">Msrtcsip-userenabled true-UCPolicy (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-839">この単一値属性には、管理者がこのユーザーに割り当てた UC ポリシーの識別名 (DN) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="9d487-840">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-841">Msrtcsip-userenabled true-UserDomainList (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="9d487-842">この属性は、SIP 対応ユーザーをホストしているフォレスト内のすべてのドメインの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d487-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="9d487-843">既定値は空の一覧で、フォレスト内のすべてのドメインが SIP 対応であることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d487-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="9d487-844">有効な値は、個々のドメインのドメイン名を表す複数の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9d487-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="9d487-845">Live Communications Server 2005 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="9d487-846">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-847">Msrtcsip-userenabled true-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="9d487-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="9d487-848">この属性は、ユーザーが Lync Server で現在有効になっているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9d487-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-849">Msrtcsip-userenabled true-UserExtension</span><span class="sxs-lookup"><span data-stu-id="9d487-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="9d487-850">この複数値を持つ属性には、name = value の形式の名前と値のペアの一覧が含まれてい &quot; ます。 &quot; この属性は、グローバルカタログのレプリケーション用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="9d487-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="9d487-851">SP1 での最新のライブ通信サーバー2005。</span><span class="sxs-lookup"><span data-stu-id="9d487-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-852">Msrtcsip-userenabled true-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="9d487-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="9d487-853">この属性には、場所プロファイルオブジェクトを参照する識別名 (DN) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="9d487-854">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-855">Msrtcsip-userenabled true-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="9d487-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="9d487-856">この属性は、ユーザーポリシーの名前と値のペアを格納します。</span><span class="sxs-lookup"><span data-stu-id="9d487-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="9d487-857">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-858">Msrtcsip-userenabled true-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="9d487-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="9d487-859">これは、さまざまな種類のグローバルユーザーポリシーを指定するバイナリ (DN_WITH_BINARY) の識別名の一覧を含む複数値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="9d487-860">バイナリ部分は、DN の部分が指しているポリシーの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="9d487-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="9d487-861">有効なバイナリ値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d487-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-862">0x00000001: 会議のポリシー</span><span class="sxs-lookup"><span data-stu-id="9d487-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="9d487-863">0x00000002: UC ポリシー</span><span class="sxs-lookup"><span data-stu-id="9d487-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="9d487-864">0x00000005: プレゼンスポリシー</span><span class="sxs-lookup"><span data-stu-id="9d487-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-865">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-866">Msrtcsip-userenabled true-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="9d487-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="9d487-867">これは、SIP ルーティンググループの ID です。</span><span class="sxs-lookup"><span data-stu-id="9d487-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="9d487-868">同じグループ内のユーザーは、同じフロントエンドサーバーに登録されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="9d487-869">Lync Server 2013 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-870">Msrtcsip-userenabled true-Webcontacts データ</span><span class="sxs-lookup"><span data-stu-id="9d487-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="9d487-871">これは複数値の属性です。</span><span class="sxs-lookup"><span data-stu-id="9d487-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="9d487-872">この属性は将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="9d487-873">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-874">Msrtcsip-userenabled true-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="9d487-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="9d487-875">この単一値の属性は、web コンポーネントが属しているプールまたは Standard Edition サーバーを指します。</span><span class="sxs-lookup"><span data-stu-id="9d487-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="9d487-876">転送リンク: <strong>リンク ID 11028</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="9d487-877">この転送リンク属性への対応する "戻る" リンクは、 <strong>Msrtcsip-userenabled true Webservers サーバー</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-878">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-879">Msrtcsip-userenabled true-Webservers サーバー</span><span class="sxs-lookup"><span data-stu-id="9d487-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="9d487-880">この属性は、複数値を持つ識別名の一覧です。</span><span class="sxs-lookup"><span data-stu-id="9d487-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="9d487-881">この属性には、このプールに関連付けられているすべての Web サーバーの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d487-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="9d487-882">戻るリンク: <strong>リンク ID 11029</strong></span><span class="sxs-lookup"><span data-stu-id="9d487-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="9d487-883">この戻るリンクへの対応する前方リンクは <strong>Msrtcsip-userenabled true WebComponentsPoolAddress</strong>です。</span><span class="sxs-lookup"><span data-stu-id="9d487-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="9d487-884">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="9d487-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-885">Msrtcsip-userenabled true の形式の Instanceid (廃止)</span><span class="sxs-lookup"><span data-stu-id="9d487-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="9d487-886">Live Communications Server 2003 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="9d487-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="9d487-887">現在、ライブ通信サーバー2005で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-888">他の Ip電話</span><span class="sxs-lookup"><span data-stu-id="9d487-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="9d487-889">この既存の Active Directory 属性は、電話の代替 TCP/IP アドレスの一覧を指定するためにテレフォニーで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="9d487-890">Windows Server 2008 オペレーティングシステムの新機能。</span><span class="sxs-lookup"><span data-stu-id="9d487-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-891">他の電話帳</span><span class="sxs-lookup"><span data-stu-id="9d487-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="9d487-892">この既存の Active Directory 属性は、ユニファイドメッセージングの自動応答とサブスクライバーアクセス番号の呼び出しをルーティングすることを目的として、Lync Server のボイスコンポーネントに対してのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="9d487-893">無条件着信転送アドレスがこの複数値属性に保存されています。</span><span class="sxs-lookup"><span data-stu-id="9d487-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="9d487-894">このアカウントは、自動応答とサブスクライバーアクセスの特定の目的で作成されます。</span><span class="sxs-lookup"><span data-stu-id="9d487-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="9d487-895">このアカウントの属性は、管理者が変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d487-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="9d487-896">Windows 2000 オペレーティングシステムの新機能。</span><span class="sxs-lookup"><span data-stu-id="9d487-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d487-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="9d487-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="9d487-898">この既存の Active Directory マルチバリュー属性は、Windows 2000 で導入されたベース Active Directory スキーマの一部です。</span><span class="sxs-lookup"><span data-stu-id="9d487-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="9d487-899">この属性には、ユーザーのメールのさまざまな X400、X500、および SMTP アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="9d487-900">Live Communications Server 2003 以降では、sip: タグを使用して、ユーザーの SIP URI がこのリストに追加されます &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="9d487-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="9d487-901">次のアプリケーションは、この属性によってユーザーの SIP URI を検索します。</span><span class="sxs-lookup"><span data-stu-id="9d487-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d487-902">Microsoft Office Outlook 2003 メッセージングおよびコラボレーションクライアント</span><span class="sxs-lookup"><span data-stu-id="9d487-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="9d487-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="9d487-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d487-904">Windows 2000 オペレーティングシステムの新機能。</span><span class="sxs-lookup"><span data-stu-id="9d487-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d487-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="9d487-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="9d487-906">この既存の Active Directory の属性には、ユーザーの電話番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d487-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="9d487-907">Windows 2000 オペレーティングシステムの新機能。</span><span class="sxs-lookup"><span data-stu-id="9d487-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="9d487-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d487-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

