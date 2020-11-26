---
title: 'Lync Server 2013: スキーマのクラスと説明'
description: 'Lync Server 2013: スキーマのクラスと説明。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441971"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="f1b97-103">Lync Server 2013 のスキーマクラスと説明</span><span class="sxs-lookup"><span data-stu-id="f1b97-103">Schema classes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1b97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1b97-104">

<span> </span></span></span>

<span data-ttu-id="f1b97-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="f1b97-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="f1b97-106">このセクションでは、Lync Server 2013 で使用されるすべてのスキーマクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-106">This section describes all the schema classes used by Lync Server 2013.</span></span>

<div>

## <a name="schema-classes-and-descriptions"></a><span data-ttu-id="f1b97-107">スキーマのクラスと説明</span><span class="sxs-lookup"><span data-stu-id="f1b97-107">Schema Classes and Descriptions</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1b97-108">クラス</span><span class="sxs-lookup"><span data-stu-id="f1b97-108">Class</span></span></th>
<th><span data-ttu-id="f1b97-109">説明</span><span class="sxs-lookup"><span data-stu-id="f1b97-109">Description</span></span></th>
<th><span data-ttu-id="f1b97-110">注釈</span><span class="sxs-lookup"><span data-stu-id="f1b97-110">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-111">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="f1b97-111">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="f1b97-112">Exchange ユニファイドメッセージング (UM) メール受信者。</span><span class="sxs-lookup"><span data-stu-id="f1b97-112">Exchange Unified Messaging (UM) email recipient.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-113">この補助クラスは Exchange UM と共有されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-113">This auxiliary class is shared with Exchange UM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-114">Msrtcsip-userenabled true-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="f1b97-114">msRTCSIP-ApplicationContacts</span></span></p></td>
<td><p><span data-ttu-id="f1b97-115">このクラスは、複数のアプリケーションの連絡先のコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-115">This class is a container for multiple application contacts and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-116">Microsoft Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="f1b97-116">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-117">Msrtcsip-userenabled true-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="f1b97-117">msRTCSIP-ApplicationServer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-118">このクラスは、ユニファイドコミュニケーションアプリケーションサービス (UCAS) のインスタンスのサービスコントロールポイントのエントリを保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-118">This class holds the entry for the service control point for an instance of Unified Communications Application Services (UCAS).</span></span></p></td>
<td><p><span data-ttu-id="f1b97-119">Office Communications Server 2007 R2 の新製品。</span><span class="sxs-lookup"><span data-stu-id="f1b97-119">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-120">Msrtcsip-userenabled true-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="f1b97-120">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="f1b97-121">このクラスは、特定のプールからそのアプリケーションサービスへの関連付けを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-121">This class provides an association from a specific pool to its Application service.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-122">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-122">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-123">Msrtcsip-userenabled true-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-123">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-124">この補助クラスと Msrtcsip-userenabled true-ApplicationServer は、アプリケーションサービスのインスタンスの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-124">This auxiliary class to msRTCSIP-ApplicationServer holds attributes representing settings for instances of the Application service.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-125">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-125">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-126">Msrtcsip-userenabled true-アーカイブ (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-126">msRTCSIP-Archive (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-127">この補助クラス to Msrtcsip-userenabled true-GlobalContainer は、アーカイブに関連するすべての設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-127">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to archiving.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-128">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-128">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-129">Msrtcsip-userenabled true-ArchivingServer (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-129">msRTCSIP-ArchivingServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-130">このクラスは、単一のインスタントメッセージングアーカイブサーバーを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-130">This class represents a single instant messaging Archiving Server.</span></span> <span data-ttu-id="f1b97-131">このクラスのインスタンスは、インスタントメッセージアーカイブサービスがインストールされているコンピューターなど、コンピューターがインスタントメッセージングアーカイブサーバーとしてアクティブ化されたときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-131">An instance of this class is created when a computer is activated as an instant messaging Archiving Server, such as a computer with the Instant Messaging Archiving service installed.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-132">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-132">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-133">Msrtcsip-userenabled true-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="f1b97-133">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="f1b97-134">このクラスは、会議ディレクトリの複数のインスタンスのコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-134">This class is a container for multiple instances of conference directories and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-135">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-135">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-136">Msrtcsip-userenabled true-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="f1b97-136">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="f1b97-137">このクラスには、特定の会議ディレクトリの設定を表す属性が保持しています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-137">This class holds attributes representing settings for a specific conference directory.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-138">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-138">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-139">Msrtcsip-userenabled true-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="f1b97-139">msRTCSIP-ConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="f1b97-140">[汎用サービス制御ポイント (SCP)] は、Lync Server を実行しているサーバーとしてコンピューターを指定します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-140">Generic service control point (SCP) to specify the computer as a server running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-141">Lync 2010 の新方法。</span><span class="sxs-lookup"><span data-stu-id="f1b97-141">New in Lync 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-142">Msrtcsip-userenabled true-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="f1b97-142">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="f1b97-143">この補助クラスは、Microsoft Lync Web App bank の設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-143">This auxiliary class holds the settings for a Microsoft Lync Web App bank.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-144">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-144">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-145">Msrtcsip-userenabled true-ドメイン</span><span class="sxs-lookup"><span data-stu-id="f1b97-145">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="f1b97-146">このクラスは、SIP レジストラーの構成済みドメインを定義する属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-146">This class holds attributes that define the configured domains of the SIP Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-147">Msrtcsip-userenabled true-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="f1b97-147">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="f1b97-148">このクラスコンテナーは、単一のアクセスエッジサービスを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-148">This class container represents a single Access Edge service.</span></span> <span data-ttu-id="f1b97-149">アクセスエッジサービスは境界ネットワークに展開されているため、ユーザーは通常、境界ネットワークからの Active Directory ドメインサービスへのアクセスを許可しません。アクセスエッジサービスのインスタンスは、イントラネットの Active Directory ネットワークには参加していません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-149">Because an Access Edge service is deployed in the perimeter network and customers usually do not allow Active Directory Domain Services access from the perimeter network, instances of Access Edge service are not joined to the intranet’s Active Directory network.</span></span> <span data-ttu-id="f1b97-150">そのため、アクセスプロキシは AD DS に自動的に登録されません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-150">Therefore, Access Proxies are not automatically registered in AD DS.</span></span> <span data-ttu-id="f1b97-151">管理者は、AD DS のアクセスエッジサービスの各インスタンスの存在を手動で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1b97-151">The administrator must manually configure the existence of each instance of Access Edge service in AD DS.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-152">Msrtcsip-userenabled true-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-152">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-153">この補助クラスから Msrtcsip-userenabled true への属性は、会議サーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-153">This auxiliary class to msRTCSIP-MCU holds attributes representing settings for Conferencing servers.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-154">Microsoft Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="f1b97-154">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-155">Msrtcsip-userenabled true-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-155">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-156">この補助クラスの Msrtcsip-userenabled true-MediationServer は、仲介サーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-156">This auxiliary class to msRTCSIP-MediationServer holds attributes representing settings for Mediation Servers.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-157">Office Communications Server 2007 の新製品。</span><span class="sxs-lookup"><span data-stu-id="f1b97-157">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-158">Msrtcsip-userenabled true-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-158">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-159">Msrtcsip-userenabled true への補助クラスは、SIP サーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-159">This auxiliary class to msRTCSIP-Server holds attributes representing settings for SIP servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-160">Msrtcsip-userenabled true-フェデレーション</span><span class="sxs-lookup"><span data-stu-id="f1b97-160">msRTCSIP-Federation</span></span></p></td>
<td><p><span data-ttu-id="f1b97-161">この補助クラス to Msrtcsip-userenabled true-GlobalContainer は、フェデレーションに関連するすべての設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-161">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to federation.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-162">Msrtcsip-userenabled true-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="f1b97-162">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-163">このクラスは、Lync Server の展開全体で適用されるすべての設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-163">This class holds all settings that apply throughout a Lync Server deployment.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-164">Msrtcsip-userenabled true-GlobalUserPolicy (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-164">msRTCSIP-GlobalUserPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-165">このクラスは、1つの Office Communications Server 会議ポリシーを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-165">This class represents a single Office Communications Server meeting policy.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-166">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-166">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-167">Msrtcsip-userenabled true-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="f1b97-167">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="f1b97-168">ローカルグローバルトポロジ設定オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f1b97-168">The local global topology setting object.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-169">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-169">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-170">Msrtcsip-userenabled true-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-170">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-171">グローバルトポロジ設定オブジェクトを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="f1b97-171">Container to hold global topology setting objects.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-172">Lync Server 2010 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-172">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-173">Msrtcsip-userenabled true-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="f1b97-173">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="f1b97-174">このクラスは、位置正規化規則のインスタンスを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-174">This class is a container that represents an instance of a location normalization rule.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-175">Msrtcsip-userenabled true-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="f1b97-175">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="f1b97-176">このクラスは、会議アテンダントアプリケーションによって作成され、地域ごとの会議電話番号の分類に使われる属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-176">This class is created by the Conferencing Attendant application and holds attributes used to categorize conference telephone numbers by region.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-177">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-177">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-178">Msrtcsip-userenabled true-LocationContactMappings マッピング</span><span class="sxs-lookup"><span data-stu-id="f1b97-178">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-179">このクラスは、場所の連絡先マッピングの複数のインスタンスのコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-179">This class is a container for multiple instances of location contact mappings and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-180">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-180">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-181">Msrtcsip-userenabled true-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="f1b97-181">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="f1b97-182">このクラスは、特定の位置情報プロファイルを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-182">This class is a container that represents a specific location profile.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-183">Msrtcsip-userenabled true-LocationProfiles (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-183">msRTCSIP-LocationProfiles (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-184">このクラスは、複数の場所プロファイルのコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-184">This class is a container for multiple location profiles and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-185">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-185">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-186">Msrtcsip-userenabled true-LocalNormalizations 廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-186">msRTCSIP-LocalNormalizations (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-187">このクラスは、複数のローカル正規化規則のコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-187">This class is a container for multiple local normalization rules and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-188">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-188">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-189">Msrtcsip-userenabled true-MCU</span><span class="sxs-lookup"><span data-stu-id="f1b97-189">msRTCSIP-MCU</span></span></p></td>
<td><p><span data-ttu-id="f1b97-190">このクラスは、単一の会議サーバーを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-190">This class represents a single Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-191">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-191">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-192">Msrtcsip-userenabled true-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="f1b97-192">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="f1b97-193">このクラスは、複数の Msrtcsip-userenabled true を保持し、属性自体は持ちません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-193">This class holds multiple msRTCSIP-MCUFactory classes and does not have attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-194">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-194">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-195">Msrtcsip-userenabled true-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="f1b97-195">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="f1b97-196">このクラスは、単一のメディアの種類の会議サーバーファクトリを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-196">This class is a container representing a Conferencing Server Factory for a single medium type.</span></span> <span data-ttu-id="f1b97-197">このクラスのインスタンスは、この特定の種類とベンダーの最初の会議サーバーがアクティブ化されたときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-197">An instance of this class is created when the first Conferencing server for this particular type and vendor is activated.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-198">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-198">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-199">Msrtcsip-userenabled true-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="f1b97-199">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="f1b97-200">このクラスは、特定のプールから会議サーバーファクトリへの関連付けを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-200">This class provides an association from a specific pool to its Conferencing Server Factory.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-201">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-201">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-202">Msrtcsip-userenabled true-MediationServer</span><span class="sxs-lookup"><span data-stu-id="f1b97-202">msRTCSIP-MediationServer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-203">このクラスは、仲介サーバーのサービス制御ポイントのエントリを保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-203">This class holds the entry for the service control point for a Mediation Server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-204">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-204">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-205">Msrtcsip-userenabled true-会議 (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-205">msRTCSIP-Meeting (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-206">この補助クラスの Msrtcsip-userenabled true-GlobalContainer は、構成可能な会議の設定を示す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-206">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing configurable meeting settings.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-207">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-207">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-208">Msrtcsip-userenabled true</span><span class="sxs-lookup"><span data-stu-id="f1b97-208">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="f1b97-209">グローバルモバイル設定を格納するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="f1b97-209">Container that stores the global mobility settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-210">Msrtcsip-userenabled true-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="f1b97-210">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-211">このクラスは、単一の監視サーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-211">This class holds attributes that represent settings for a single Monitoring Server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-212">Communications Server 2007 R2 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-212">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-213">Msrtcsip-userenabled true-PhoneRoute (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-213">msRTCSIP-PhoneRoute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-214">このクラスは、ゲートウェイまたはゲートウェイのセットへの最小料金のルートのインスタンスを示すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-214">This class is a container representing an instance of a least cost route to a gateway or set of gateways.</span></span> <span data-ttu-id="f1b97-215">この情報は、標準エディションを実行しているすべてのエンタープライズプールまたはサーバーが、発信した通話を、最もお得な方法で公衆交換電話網 (PSTN) にルーティングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-215">This information is used by all Enterprise pools or servers running Standard Edition to route outgoing calls to the public switched telephone network (PSTN) in the most cost effective way.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-216">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-216">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-217">Msrtcsip-userenabled true-PhoneRoutes (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-217">msRTCSIP-PhoneRoutes (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-218">このクラスは、コストが最小の複数のルートのコンテナーであり、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-218">This class is a container for multiple, least cost routes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-219">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-219">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-220">Msrtcsip-userenabled true-ポリシー (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-220">msRTCSIP-Policies (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-221">このクラスには、複数の Lync Server ポリシークラスが含まれており、属性自体は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-221">This class holds multiple Lync Server policy classes and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-222">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-222">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-223">Msrtcsip-userenabled true プール</span><span class="sxs-lookup"><span data-stu-id="f1b97-223">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="f1b97-224">このクラスは、単一の Lync サーバープールを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-224">This class represents a single Lync Server pool.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-225">Msrtcsip-userenabled true-プール</span><span class="sxs-lookup"><span data-stu-id="f1b97-225">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="f1b97-226">このクラスは、複数の Lync Server プールを保持しており、属性自体を持ちません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-226">This class holds multiple Lync Server pools and does not have any attributes itself.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-227">Msrtcsip-userenabled true-PoolService</span><span class="sxs-lookup"><span data-stu-id="f1b97-227">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="f1b97-228">このクラスは、プールのサービス制御ポイントサービス制御ポイントを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-228">This class represents the service control pointservice control point of a pool.</span></span> <span data-ttu-id="f1b97-229">プールでホストされているユーザーの Msrtcsip-userenabled true 属性ポイントは、このクラスのインスタンスになります。</span><span class="sxs-lookup"><span data-stu-id="f1b97-229">Users hosted on a pool have their msRTCSIP-PrimaryHomeServer attribute point to an instance of this class.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-230">Msrtcsip-userenabled true-プレゼンス</span><span class="sxs-lookup"><span data-stu-id="f1b97-230">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="f1b97-231">グローバルプレゼンス設定を格納するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="f1b97-231">Container that stores the global presence settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-232">Msrtcsip-userenabled true-レジストラー</span><span class="sxs-lookup"><span data-stu-id="f1b97-232">msRTCSIP-Registrar</span></span></p></td>
<td><p><span data-ttu-id="f1b97-233">この補助クラス to Msrtcsip-userenabled true-GlobalContainer は、SIP レジストラーサーバーによって管理されるユーザー設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-233">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing user settings maintained by the SIP Registrar servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-234">Msrtcsip-userenabled true-RouteUsage (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-234">msRTCSIP-RouteUsage (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-235">このクラスは、電話ルートの使用状況のインスタンスを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-235">This class is a container representing an instance of a phone route usage.</span></span> <span data-ttu-id="f1b97-236">電話ルートの利用状況クラスは、属性フィールドと説明フィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-236">A phone route usage class consists of an attribute field and a description field.</span></span> <span data-ttu-id="f1b97-237">属性フィールドには、使用の種類が定義されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-237">The attribute field defines a usage type.</span></span> <span data-ttu-id="f1b97-238">[説明] フィールドでは、管理者が電話ルートでこの属性の使用を説明できます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-238">The description field allows administrators to describe the usage for this attribute in the phone route.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-239">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-239">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-240">Msrtcsip-userenabled true-RouteUsages (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-240">msRTCSIP-RouteUsages (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-241">このクラスは、Msrtcsip-userenabled true-RouteUsage クラスの複数のインスタンスを保持します。属性自体はありません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-241">This class holds multiple instances of the msRTCSIP-RouteUsage class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-242">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-243">Msrtcsip-userenabled true-検索</span><span class="sxs-lookup"><span data-stu-id="f1b97-243">msRTCSIP-Search</span></span></p></td>
<td><p><span data-ttu-id="f1b97-244">この補助クラス to Msrtcsip-userenabled true-GlobalContainer は、検索結果の範囲を制限および制御する属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-244">This auxiliary class to msRTCSIP-GlobalContainer holds attributes that limit and control the scope of search results.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-245">Msrtcsip-userenabled true-サーバー</span><span class="sxs-lookup"><span data-stu-id="f1b97-245">msRTCSIP-Server</span></span></p></td>
<td><p><span data-ttu-id="f1b97-246">このクラスは、Lync Server を実行している1台のサーバーを表します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-246">This class represents a single server running Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-247">Msrtcsip-userenabled true-サービス</span><span class="sxs-lookup"><span data-stu-id="f1b97-247">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="f1b97-248">このクラスは、グローバル設定コンテナーと Msrtcsip-userenabled true オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-248">This class holds the global settings container and msRTCSIP-Domain objects.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-249">Msrtcsip-userenabled true-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="f1b97-249">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="f1b97-250">このクラスは、信頼できる会議サーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-250">This class holds attributes that represent settings for a trusted Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-251">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-251">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-252">Msrtcsip-userenabled true-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="f1b97-252">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="f1b97-253">このクラスには、Msrtcsip-userenabled true の複数のインスタンスが含まれており、属性自体はありません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-253">This class holds multiple instances of the msRTCSIP-TrustedMCU class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-254">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-254">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-255">Msrtcsip-userenabled true-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="f1b97-255">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="f1b97-256">このクラスは、複数の Msrtcsip-userenabled true プロキシクラスを保持し、属性自体は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-256">This class holds multiple msRTCSIP-TrustedProxy classes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-257">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-257">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-258">Msrtcsip-userenabled true-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="f1b97-258">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="f1b97-259">このクラスは、プロキシサーバーを実行しているサーバーを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-259">This class is a container representing a server running Proxy Server.</span></span> <span data-ttu-id="f1b97-260">このクラスのインスタンスは、AD DS に参加しているコンピューターで新しいプロキシサーバーをアクティブ化するときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-260">An instance of this class is created when activating a new Proxy Server on a computer joined to AD DS.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-261">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-261">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-262">Msrtcsip-userenabled true-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="f1b97-262">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-263">このクラスは、信頼されたサーバーの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-263">This class holds attributes that represent settings for a trusted server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-264">Msrtcsip-userenabled true-TrustedService</span><span class="sxs-lookup"><span data-stu-id="f1b97-264">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="f1b97-265">このクラスは、グローバルルーティング可能なユーザーエージェント URI (GRUU) アドレスを使ってルーティング可能な、信頼されたサービスを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-265">This class is a container representing a trusted service that is routable using a Globally Routable User Agent URI (GRUU) address.</span></span> <span data-ttu-id="f1b97-266">このクラスのインスタンスは、Lync Server によって信頼されている新しいサーバーがアクティブ化されたときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1b97-266">An instance of this class is created when a new server that is trusted by Lync Server is activated.</span></span> <span data-ttu-id="f1b97-267">この信頼できるサーバーは Active Directory ドメインに参加している必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1b97-267">This trusted server must be joined to an Active Directory domain.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-268">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-268">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-269">Msrtcsip-userenabled true-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="f1b97-269">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="f1b97-270">このクラスは、複数の GRUU サーバーのコンテナーであり、属性自体は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-270">This class is a container for multiple GRUU servers and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-271">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-271">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-272">Msrtcsip-userenabled true-Trustedwebのサーバー</span><span class="sxs-lookup"><span data-stu-id="f1b97-272">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="f1b97-273">このクラスは、信頼された web コンポーネントの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-273">This class holds attributes that represent the settings for a trusted web component.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-274">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-274">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-275">Msrtcsip-userenabled true-Trustedwebservers サーバー</span><span class="sxs-lookup"><span data-stu-id="f1b97-275">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="f1b97-276">このクラスは、Msrtcsip-userenabled true Webcomponentserver クラスの複数のインスタンスを保持します。属性自体はありません。</span><span class="sxs-lookup"><span data-stu-id="f1b97-276">This class holds multiple instances of the msRTCSIP-TrustedWebComponentServer class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-277">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-277">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-278">Msrtcsip-userenabled true-UnifiedCommunications (廃止)</span><span class="sxs-lookup"><span data-stu-id="f1b97-278">msRTCSIP-UnifiedCommunications (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="f1b97-279">この補助クラスの Msrtcsip-userenabled true-GlobalContainer は、統合された通信に関連する属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-279">This auxiliary class to msRTCSIP-GlobalContainer holds attributes related to unified communications.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-280">Lync Server 2010 では廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f1b97-280">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-281">Msrtcsip-userenabled true-Web コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f1b97-281">msRTCSIP-WebComponents</span></span></p></td>
<td><p><span data-ttu-id="f1b97-282">このクラスは、インターネットインフォメーションサーバー (IIS) のサービスコントロールポイントサービス制御ポイントを保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-282">This class holds the service control pointservice control point for Internet Information Server (IIS).</span></span> <span data-ttu-id="f1b97-283">Web コンポーネントサーバーとしてサーバーを識別します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-283">It identifies a server as a web components server.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-284">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-284">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b97-285">Msrtcsip-userenabled true-Webmessages サービス</span><span class="sxs-lookup"><span data-stu-id="f1b97-285">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="f1b97-286">このクラスは、プールで使用される web コンポーネントと特定のプールとの関連付けを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-286">This class provides an association from a specific pool to the web components that the pool will use.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-287">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-287">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b97-288">Msrtcsip-userenabled true-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="f1b97-288">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="f1b97-289">この補助クラスの Msrtcsip-userenabled true コンポーネントは、web コンポーネントの設定を表す属性を保持します。</span><span class="sxs-lookup"><span data-stu-id="f1b97-289">This auxiliary class to msRTCSIP-WebComponents holds attributes representing settings for web components.</span></span></p></td>
<td><p><span data-ttu-id="f1b97-290">Communications Server 2007 の新サービスです。</span><span class="sxs-lookup"><span data-stu-id="f1b97-290">New in Communications Server 2007.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f1b97-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1b97-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

