---
title: 'Lync Server 2013: クラスごとのスキーマ属性'
description: 'Lync Server 2013: クラスごとのスキーマ属性。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes by class
ms:assetid: 72726b43-f1ea-458c-9304-a26e8a12128c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398544(v=OCS.15)
ms:contentKeyID: 48184468
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd31e42ce825049903310d6021e13086fe07afd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441992"
---
# <a name="schema-attributes-by-class-in-lync-server-2013"></a><span data-ttu-id="b7639-103">Lync Server 2013 のクラス別のスキーマ属性</span><span class="sxs-lookup"><span data-stu-id="b7639-103">Schema attributes by class in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7639-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7639-104">

<span> </span></span></span>

<span data-ttu-id="b7639-105">_**最終更新日:** 2012-08-29_</span><span class="sxs-lookup"><span data-stu-id="b7639-105">_**Topic Last Modified:** 2012-08-29_</span></span>

<span data-ttu-id="b7639-106">このセクションでは、各 Lync Server 2013 クラスに含めることができるスキーマ属性と、他のクラスに含めることができるクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b7639-106">This section lists the schema attributes that can be contained in each Lync Server 2013 class and the classes that can be contained in other classes.</span></span> <span data-ttu-id="b7639-107">すべてのクラスとその説明の一覧については、「 [Lync Server 2013 でのスキーマクラスと説明](lync-server-2013-schema-classes-and-descriptions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7639-107">For a list of all the classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="b7639-108">すべての属性と説明の一覧については、「 [Lync Server 2013 でのスキーマの属性と説明](lync-server-2013-schema-attributes-and-descriptions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7639-108">For a list of all the attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span>

<div>

## <a name="attributes-by-class"></a><span data-ttu-id="b7639-109">クラスごとの属性</span><span class="sxs-lookup"><span data-stu-id="b7639-109">Attributes by Class</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7639-110">クラス</span><span class="sxs-lookup"><span data-stu-id="b7639-110">Class</span></span></th>
<th><span data-ttu-id="b7639-111">以下の属性が含まれている可能性がある</span><span class="sxs-lookup"><span data-stu-id="b7639-111">May contain these attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7639-112">問い合わせ</span><span class="sxs-lookup"><span data-stu-id="b7639-112">Contact</span></span></p></td>
<td><p><span data-ttu-id="b7639-113">SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="b7639-113">msDS-SourceObjectDN</span></span></p>
<p><span data-ttu-id="b7639-114">Msrtcsip-userenabled true-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="b7639-114">msRTCSIP-AcpInfo</span></span></p>
<p><span data-ttu-id="b7639-115">Msrtcsip-userenabled true-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="b7639-115">msRTCSIP-ApplicationDestination</span></span></p>
<p><span data-ttu-id="b7639-116">Msrtcsip-userenabled true-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="b7639-116">msRTCSIP-ApplicationOptions</span></span></p>
<p><span data-ttu-id="b7639-117">Msrtcsip-userenabled true-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="b7639-117">msRTCSIP-ApplicationPrimaryLanguage</span></span></p>
<p><span data-ttu-id="b7639-118">Msrtcsip-userenabled true-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="b7639-118">msRTCSIP-ApplicationSecondaryLanguages</span></span></p>
<p><span data-ttu-id="b7639-119">Msrtcsip-userenabled true-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-119">msRTCSIP-ArchivingEnabled</span></span></p>
<p><span data-ttu-id="b7639-120">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="b7639-120">msRTCSIP-DeploymentLocator</span></span></p>
<p><span data-ttu-id="b7639-121">Msrtcsip-userenabled true-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-121">msRTCSIP-FederationEnabled</span></span></p>
<p><span data-ttu-id="b7639-122">Msrtcsip-userenabled true-GroupingID</span><span class="sxs-lookup"><span data-stu-id="b7639-122">msRTCSIP-GroupingID</span></span></p>
<p><span data-ttu-id="b7639-123">Msrtcsip-userenabled true-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-123">msRTCSIP-InternetAccessEnabled</span></span></p>
<p><span data-ttu-id="b7639-124">Msrtcsip-userenabled true ライン</span><span class="sxs-lookup"><span data-stu-id="b7639-124">msRTCSIP-Line</span></span></p>
<p><span data-ttu-id="b7639-125">Msrtcsip-userenabled true</span><span class="sxs-lookup"><span data-stu-id="b7639-125">msRTCSIP-LineServer</span></span></p>
<p><span data-ttu-id="b7639-126">Msrtcsip-userenabled true-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="b7639-126">msRTCSIP-OptionFlags</span></span></p>
<p><span data-ttu-id="b7639-127">Msrtcsip-userenabled true-Sid</span><span class="sxs-lookup"><span data-stu-id="b7639-127">msRTCSIP-OriginatorSid</span></span></p>
<p><span data-ttu-id="b7639-128">Msrtcsip-userenabled true-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="b7639-128">msRTCSIP-OwnerUrn</span></span></p>
<p><span data-ttu-id="b7639-129">Msrtcsip-userenabled true-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="b7639-129">msRTCSIP-PrimaryHomeServer</span></span></p>
<p><span data-ttu-id="b7639-130">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="b7639-130">msRTCSIP-PrimaryUserAddress</span></span></p>
<p><span data-ttu-id="b7639-131">Msrtcsip-userenabled true-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="b7639-131">msRTCSIP-PrivateLine</span></span></p>
<p><span data-ttu-id="b7639-132">Msrtcsip-userenabled true-ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b7639-132">msRTCSIP-ProxyAddresses</span></span></p>
<p><span data-ttu-id="b7639-133">Msrtcsip-userenabled true-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="b7639-133">msRTCSIP-SourceObjectType</span></span></p>
<p><span data-ttu-id="b7639-134">Msrtcsip-userenabled true-Targethoのメッセージ</span><span class="sxs-lookup"><span data-stu-id="b7639-134">msRTCSIP-TargetHomeServer</span></span></p>
<p><span data-ttu-id="b7639-135">Msrtcsip-userenabled true-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7639-135">msRTCSIP-TargetUserPolicies</span></span></p>
<p><span data-ttu-id="b7639-136">Msrtcsip-userenabled true-TenantId</span><span class="sxs-lookup"><span data-stu-id="b7639-136">msRTCSIP-TenantId</span></span></p>
<p><span data-ttu-id="b7639-137">Msrtcsip-userenabled true-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-137">msRTCSIP-UserEnabled</span></span></p>
<p><span data-ttu-id="b7639-138">Msrtcsip-userenabled true-UserExtension</span><span class="sxs-lookup"><span data-stu-id="b7639-138">msRTCSIP-UserExtension</span></span></p>
<p><span data-ttu-id="b7639-139">Msrtcsip-userenabled true-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="b7639-139">msRTCSIP-UserLocationProfile</span></span></p>
<p><span data-ttu-id="b7639-140">Msrtcsip-userenabled true-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7639-140">msRTCSIP-UserPolicies</span></span></p>
<p><span data-ttu-id="b7639-141">Msrtcsip-userenabled true-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="b7639-141">msRTCSIP-UserPolicy</span></span></p>
<p><span data-ttu-id="b7639-142">Msrtcsip-userenabled true-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b7639-142">msRTCSIP-UserRoutingGroupId</span></span></p>
<p><span data-ttu-id="b7639-143">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b7639-143">ProxyAddresses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-144">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="b7639-144">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="b7639-145">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-145">msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="b7639-146">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="b7639-146">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-147">Msrtcsip-userenabled true-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="b7639-147">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="b7639-148">Msrtcsip-userenabled true-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="b7639-148">msRTCSIP-ApplicationServerBL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-149">Msrtcsip-userenabled true-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-149">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-150">Msrtcsip-userenabled true-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="b7639-150">msRTCSIP-ApplicationList</span></span></p>
<p><span data-ttu-id="b7639-151">Msrtcsip-userenabled true-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="b7639-151">msRTCSIP-ApplicationServerPoolLink</span></span></p>
<p><span data-ttu-id="b7639-152">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-152">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-153">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-153">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-154">Msrtcsip-userenabled true-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="b7639-154">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="b7639-155">Msrtcsip-userenabled true-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="b7639-155">msRTCSIP-ConferenceDirectoryHomePool</span></span></p>
<p><span data-ttu-id="b7639-156">Msrtcsip-userenabled true-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="b7639-156">msRTCSIP-ConferenceDirectoryId</span></span></p>
<p><span data-ttu-id="b7639-157">Msrtcsip-userenabled true-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="b7639-157">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p>
<p><span data-ttu-id="b7639-158">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-158">msRTCSIP-ExtensionData</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-159">Msrtcsip-userenabled true-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="b7639-159">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="b7639-160">Msrtcsip-userenabled true-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="b7639-160">msRTCSIP-DefaultCWAExternalURL</span></span></p>
<p><span data-ttu-id="b7639-161">Msrtcsip-userenabled true-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="b7639-161">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-162">Msrtcsip-userenabled true-ドメイン</span><span class="sxs-lookup"><span data-stu-id="b7639-162">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="b7639-163">Msrtcsip-userenabled true-既定値</span><span class="sxs-lookup"><span data-stu-id="b7639-163">msRTCSIP-Default</span></span></p>
<p><span data-ttu-id="b7639-164">Msrtcsip-userenabled true-DomainData</span><span class="sxs-lookup"><span data-stu-id="b7639-164">msRTCSIP-DomainData</span></span></p>
<p><span data-ttu-id="b7639-165">Msrtcsip-userenabled true-ドメイン名</span><span class="sxs-lookup"><span data-stu-id="b7639-165">msRTCSIP-DomainName</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-166">Msrtcsip-userenabled true-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="b7639-166">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="b7639-167">Msrtcsip-userenabled true-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="b7639-167">msRTCSIP-EdgeProxyData</span></span></p>
<p><span data-ttu-id="b7639-168">Msrtcsip-userenabled true-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-168">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-169">Msrtcsip-userenabled true-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-169">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-170">Msrtcsip-userenabled true-MCUData</span><span class="sxs-lookup"><span data-stu-id="b7639-170">msRTCSIP-MCUData</span></span></p>
<p><span data-ttu-id="b7639-171">Msrtcsip-userenabled true-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="b7639-171">msRTCSIP-MCUFactoryAddress</span></span></p>
<p><span data-ttu-id="b7639-172">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-172">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-173">Msrtcsip-userenabled true-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-173">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-174">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-174">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-175">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-175">msRTCSIP-ServerVersion</span></span></p>
<p><span data-ttu-id="b7639-176">Msrtcsip-userenabled true-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="b7639-176">msRTCSIP-TrustedServiceLinks</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-177">Msrtcsip-userenabled true-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-177">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-178">Msrtcsip-userenabled true-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="b7639-178">msRTCSIP-EnterpriseServices</span></span></p>
<p><span data-ttu-id="b7639-179">Msrtcsip-userenabled true-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="b7639-179">msRTCSIP-PoolAddress</span></span></p>
<p><span data-ttu-id="b7639-180">Msrtcsip-userenabled true-ServerData</span><span class="sxs-lookup"><span data-stu-id="b7639-180">msRTCSIP-ServerData</span></span></p>
<p><span data-ttu-id="b7639-181">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-181">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-182">Msrtcsip-userenabled true-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="b7639-182">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="b7639-183">Msrtcsip-userenabled true-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="b7639-183">msRTCSIP-BackEndServer</span></span></p>
<p><span data-ttu-id="b7639-184">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-184">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-185">Msrtcsip-userenabled true-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="b7639-185">msRTCSIP-MirrorBackEndServer</span></span></p>
<p><span data-ttu-id="b7639-186">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-186">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-187">Msrtcsip-userenabled true-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="b7639-187">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="b7639-188">Msrtcsip-userenabled true-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="b7639-188">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-189">Msrtcsip-userenabled true-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="b7639-189">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="b7639-190">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-190">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-191">Msrtcsip-userenabled true-MappingContact</span><span class="sxs-lookup"><span data-stu-id="b7639-191">msRTCSIP-MappingContact</span></span></p>
<p><span data-ttu-id="b7639-192">Msrtcsip-userenabled true-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="b7639-192">msRTCSIP-MappingLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-193">Msrtcsip-userenabled true-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="b7639-193">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="b7639-194">Msrtcsip-userenabled true-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="b7639-194">msRTCSIP-ExternalAccessCode</span></span></p>
<p><span data-ttu-id="b7639-195">Msrtcsip-userenabled true-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="b7639-195">msRTCSIP-LocationProfileOptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-196">Msrtcsip-userenabled true-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="b7639-196">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="b7639-197">Msrtcsip-userenabled true-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="b7639-197">msRTCSIP-MCUFactoryData</span></span></p>
<p><span data-ttu-id="b7639-198">Msrtcsip-userenabled true-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="b7639-198">msRTCSIP-MCUFactoryProviderID</span></span></p>
<p><span data-ttu-id="b7639-199">msrtcsip-userenabled true-mcuser</span><span class="sxs-lookup"><span data-stu-id="b7639-199">msRTCSIP-MCUServers</span></span></p>
<p><span data-ttu-id="b7639-200">Msrtcsip-userenabled true-MCUType</span><span class="sxs-lookup"><span data-stu-id="b7639-200">msRTCSIP-MCUType</span></span></p>
<p><span data-ttu-id="b7639-201">Msrtcsip-userenabled true-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="b7639-201">msRTCSIP-MCUVendor</span></span></p>
<p><span data-ttu-id="b7639-202">Msrtcsip-userenabled true-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="b7639-202">msRTCSIP-PoolAddresses</span></span></p>
<p><span data-ttu-id="b7639-203">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-203">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-204">Msrtcsip-userenabled true-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="b7639-204">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="b7639-205">Msrtcsip-userenabled true-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="b7639-205">msRTCSIP-MCUFactoryPath</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-206">Msrtcsip-userenabled true</span><span class="sxs-lookup"><span data-stu-id="b7639-206">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="b7639-207">Msrtcsip-userenabled true-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="b7639-207">msRTCSIP-MobilityFlags</span></span></p>
<p><span data-ttu-id="b7639-208">Msrtcsip-userenabled true-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7639-208">msRTCSIP-MobilityPolicy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-209">Msrtcsip-userenabled true-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="b7639-209">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="b7639-210">dnsHostName</span><span class="sxs-lookup"><span data-stu-id="b7639-210">dnsHostName</span></span></p>
<p><span data-ttu-id="b7639-211">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-211">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-212">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-212">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-213">Msrtcsip-userenabled true プール</span><span class="sxs-lookup"><span data-stu-id="b7639-213">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="b7639-214">Msrtcsip-userenabled true-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="b7639-214">msRTCSIP-ApplicationList</span></span></p>
<p><span data-ttu-id="b7639-215">Msrtcsip-userenabled true-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="b7639-215">msRTCSIP-BackEndServer</span></span></p>
<p><span data-ttu-id="b7639-216">Msrtcsip-userenabled true-dnsHostName</span><span class="sxs-lookup"><span data-stu-id="b7639-216">msRTCSIP-dnsHostName</span></span></p>
<p><span data-ttu-id="b7639-217">Msrtcsip-userenabled true-PoolData</span><span class="sxs-lookup"><span data-stu-id="b7639-217">msRTCSIP-PoolData</span></span></p>
<p><span data-ttu-id="b7639-218">Msrtcsip-userenabled true-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="b7639-218">msRTCSIP-PoolDisplayName</span></span></p>
<p><span data-ttu-id="b7639-219">Msrtcsip-userenabled true-Pooldomaqdn</span><span class="sxs-lookup"><span data-stu-id="b7639-219">msRTCSIP-PoolDomainFQDN</span></span></p>
<p><span data-ttu-id="b7639-220">Msrtcsip-userenabled true-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="b7639-220">msRTCSIP-PoolFunctionality</span></span></p>
<p><span data-ttu-id="b7639-221">Msrtcsip-userenabled true-PoolType</span><span class="sxs-lookup"><span data-stu-id="b7639-221">msRTCSIP-PoolType</span></span></p>
<p><span data-ttu-id="b7639-222">Msrtcsip-userenabled true-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-222">msRTCSIP-PoolVersion</span></span></p>
<p><span data-ttu-id="b7639-223">Msrtcsip-userenabled true-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="b7639-223">msRTCSIP-TrustedServiceLinks</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-224">Msrtcsip-userenabled true-PoolService</span><span class="sxs-lookup"><span data-stu-id="b7639-224">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="b7639-225">Msrtcsip-userenabled true-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="b7639-225">msRTCSIP-FrontEndServers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-226">Msrtcsip-userenabled true-プレゼンス</span><span class="sxs-lookup"><span data-stu-id="b7639-226">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="b7639-227">Msrtcsip-userenabled true-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="b7639-227">msRTCSIP-PresenceFlags</span></span></p>
<p><span data-ttu-id="b7639-228">Msrtcsip-userenabled true-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="b7639-228">msRTCSIP-PresencePolicy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-229">Msrtcsip-userenabled true-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="b7639-229">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="b7639-230">Msrtcsip-userenabled true-MCUType</span><span class="sxs-lookup"><span data-stu-id="b7639-230">msRTCSIP-MCUType</span></span></p>
<p><span data-ttu-id="b7639-231">Msrtcsip-userenabled true-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="b7639-231">msRTCSIP-MCUVendor</span></span></p>
<p><span data-ttu-id="b7639-232">Msrtcsip-userenabled true-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="b7639-232">msRTCSIP-RoutingPoolDN</span></span></p>
<p><span data-ttu-id="b7639-233">Msrtcsip-userenabled true-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="b7639-233">msRTCSIP-TrustedMCUData</span></span></p>
<p><span data-ttu-id="b7639-234">Msrtcsip-userenabled true-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-234">msRTCSIP-TrustedMCUFQDN</span></span></p>
<p><span data-ttu-id="b7639-235">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-235">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-236">Msrtcsip-userenabled true-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="b7639-236">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="b7639-237">Msrtcsip-userenabled true-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="b7639-237">msRTCSIP-TrustedProxyData</span></span></p>
<p><span data-ttu-id="b7639-238">Msrtcsip-userenabled true-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-238">msRTCSIP-TrustedProxyFQDN</span></span></p>
<p><span data-ttu-id="b7639-239">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-239">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-240">Msrtcsip-userenabled true-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="b7639-240">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="b7639-241">Msrtcsip-userenabled true-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="b7639-241">msRTCSIP-TrustedServerData</span></span></p>
<p><span data-ttu-id="b7639-242">Msrtcsip-userenabled true-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-242">msRTCSIP-TrustedServerFQDN</span></span></p>
<p><span data-ttu-id="b7639-243">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-243">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-244">Msrtcsip-userenabled true-TrustedService</span><span class="sxs-lookup"><span data-stu-id="b7639-244">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="b7639-245">Msrtcsip-userenabled true-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7639-245">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="b7639-246">Msrtcsip-userenabled true-ルーティング可能</span><span class="sxs-lookup"><span data-stu-id="b7639-246">msRTCSIP-Routable</span></span></p>
<p><span data-ttu-id="b7639-247">Msrtcsip-userenabled true-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="b7639-247">msRTCSIP-RoutingPoolDN</span></span></p>
<p><span data-ttu-id="b7639-248">Msrtcsip-userenabled true-ServerBL</span><span class="sxs-lookup"><span data-stu-id="b7639-248">msRTCSIP-ServerBL</span></span></p>
<p><span data-ttu-id="b7639-249">Msrtcsip-userenabled true-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-249">msRTCSIP-TrustedServerFQDN</span></span></p>
<p><span data-ttu-id="b7639-250">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-250">msRTCSIP-TrustedServerVersion</span></span></p>
<p><span data-ttu-id="b7639-251">Msrtcsip-userenabled true-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="b7639-251">msRTCSIP-TrustedServiceFlags</span></span></p>
<p><span data-ttu-id="b7639-252">Msrtcsip-userenabled true-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="b7639-252">msRTCSIP-TrustedServicePort</span></span></p>
<p><span data-ttu-id="b7639-253">Msrtcsip-userenabled true-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="b7639-253">msRTCSIP-TrustedServiceType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-254">Msrtcsip-userenabled true-Trustedwebのサーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-254">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="b7639-255">Msrtcsip-userenabled true-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="b7639-255">msRTCSIP-TrustedWebComponentsServerData</span></span></p>
<p><span data-ttu-id="b7639-256">Msrtcsip-userenabled true-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b7639-256">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p>
<p><span data-ttu-id="b7639-257">Msrtcsip-userenabled true-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-257">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-258">Msrtcsip-userenabled true-Webmessages サービス</span><span class="sxs-lookup"><span data-stu-id="b7639-258">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="b7639-259">Msrtcsip-userenabled true-Webservers サーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-259">msRTCSIP-WebComponentsServers</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-260">Msrtcsip-userenabled true-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="b7639-260">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-261">Msrtcsip-userenabled true-Webcontacts データ</span><span class="sxs-lookup"><span data-stu-id="b7639-261">msRTCSIP-WebComponentsData</span></span></p>
<p><span data-ttu-id="b7639-262">Msrtcsip-userenabled true-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="b7639-262">msRTCSIP-WebComponentsPoolAddress</span></span></p>
<p><span data-ttu-id="b7639-263">Msrtcsip-userenabled true-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7639-263">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-264">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b7639-264">User</span></span></p></td>
<td><p><span data-ttu-id="b7639-265">Msrtcsip-userenabled true-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="b7639-265">msRTCSIP-AcpInfo</span></span></p>
<p><span data-ttu-id="b7639-266">Msrtcsip-userenabled true-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="b7639-266">msRTCSIP-ApplicationOptions</span></span></p>
<p><span data-ttu-id="b7639-267">Msrtcsip-userenabled true-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-267">msRTCSIP-ArchivingEnabled</span></span></p>
<p><span data-ttu-id="b7639-268">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="b7639-268">msRTCSIP-DeploymentLocator</span></span></p>
<p><span data-ttu-id="b7639-269">Msrtcsip-userenabled true-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-269">msRTCSIP-FederationEnabled</span></span></p>
<p><span data-ttu-id="b7639-270">Msrtcsip-userenabled true-GroupingID</span><span class="sxs-lookup"><span data-stu-id="b7639-270">msRTCSIP-GroupingID</span></span></p>
<p><span data-ttu-id="b7639-271">Msrtcsip-userenabled true-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-271">msRTCSIP-InternetAccessEnabled</span></span></p>
<p><span data-ttu-id="b7639-272">Msrtcsip-userenabled true ライン</span><span class="sxs-lookup"><span data-stu-id="b7639-272">msRTCSIP-Line</span></span></p>
<p><span data-ttu-id="b7639-273">Msrtcsip-userenabled true</span><span class="sxs-lookup"><span data-stu-id="b7639-273">msRTCSIP-LineServer</span></span></p>
<p><span data-ttu-id="b7639-274">Msrtcsip-userenabled true-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="b7639-274">msRTCSIP-OptionFlags</span></span></p>
<p><span data-ttu-id="b7639-275">Msrtcsip-userenabled true-Sid</span><span class="sxs-lookup"><span data-stu-id="b7639-275">msRTCSIP-OriginatorSid</span></span></p>
<p><span data-ttu-id="b7639-276">Msrtcsip-userenabled true-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="b7639-276">msRTCSIP-OwnerUrn</span></span></p>
<p><span data-ttu-id="b7639-277">Msrtcsip-userenabled true-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="b7639-277">msRTCSIP-PrimaryHomeServer</span></span></p>
<p><span data-ttu-id="b7639-278">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="b7639-278">msRTCSIP-PrimaryUserAddress</span></span></p>
<p><span data-ttu-id="b7639-279">Msrtcsip-userenabled true-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="b7639-279">msRTCSIP-PrivateLine</span></span></p>
<p><span data-ttu-id="b7639-280">Msrtcsip-userenabled true-Targethoのメッセージ</span><span class="sxs-lookup"><span data-stu-id="b7639-280">msRTCSIP-TargetHomeServer</span></span></p>
<p><span data-ttu-id="b7639-281">Msrtcsip-userenabled true-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7639-281">msRTCSIP-TargetUserPolicies</span></span></p>
<p><span data-ttu-id="b7639-282">Msrtcsip-userenabled true-TenantId</span><span class="sxs-lookup"><span data-stu-id="b7639-282">msRTCSIP-TenantId</span></span></p>
<p><span data-ttu-id="b7639-283">Msrtcsip-userenabled true-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b7639-283">msRTCSIP-UserEnabled</span></span></p>
<p><span data-ttu-id="b7639-284">Msrtcsip-userenabled true-UserExtension</span><span class="sxs-lookup"><span data-stu-id="b7639-284">msRTCSIP-UserExtension</span></span></p>
<p><span data-ttu-id="b7639-285">Msrtcsip-userenabled true-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="b7639-285">msRTCSIP-UserLocationProfile</span></span></p>
<p><span data-ttu-id="b7639-286">Msrtcsip-userenabled true-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7639-286">msRTCSIP-UserPolicies</span></span></p>
<p><span data-ttu-id="b7639-287">Msrtcsip-userenabled true-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="b7639-287">msRTCSIP-UserPolicy</span></span></p>
<p><span data-ttu-id="b7639-288">Msrtcsip-userenabled true-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b7639-288">msRTCSIP-UserRoutingGroupId</span></span></p>
<p><span data-ttu-id="b7639-289">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b7639-289">ProxyAddresses</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="classes-contained-in-other-classes"></a><span data-ttu-id="b7639-290">他のクラスに含まれるクラス</span><span class="sxs-lookup"><span data-stu-id="b7639-290">Classes Contained in Other Classes</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7639-291">クラス</span><span class="sxs-lookup"><span data-stu-id="b7639-291">Class</span></span></th>
<th><span data-ttu-id="b7639-292">このクラスを含めることができます</span><span class="sxs-lookup"><span data-stu-id="b7639-292">May contain this class</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7639-293">serviceConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="b7639-293">serviceConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="b7639-294">Msrtcsip-userenabled true-サーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-294">msRTCSIP-Server</span></span></p>
<p><span data-ttu-id="b7639-295">Msrtcsip-userenabled true-PoolService</span><span class="sxs-lookup"><span data-stu-id="b7639-295">msRTCSIP-PoolService</span></span></p>
<p><span data-ttu-id="b7639-296">Msrtcsip-userenabled true-MCU</span><span class="sxs-lookup"><span data-stu-id="b7639-296">msRTCSIP-MCU</span></span></p>
<p><span data-ttu-id="b7639-297">Msrtcsip-userenabled true-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="b7639-297">msRTCSIP-MCUFactoryService</span></span></p>
<p><span data-ttu-id="b7639-298">Msrtcsip-userenabled true-Web コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b7639-298">msRTCSIP-WebComponents</span></span></p>
<p><span data-ttu-id="b7639-299">Msrtcsip-userenabled true-Webmessages サービス</span><span class="sxs-lookup"><span data-stu-id="b7639-299">msRTCSIP-WebComponentsService</span></span></p>
<p><span data-ttu-id="b7639-300">Msrtcsip-userenabled true-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="b7639-300">msRTCSIP-ApplicationServerService</span></span></p>
<p><span data-ttu-id="b7639-301">Msrtcsip-userenabled true-サービス</span><span class="sxs-lookup"><span data-stu-id="b7639-301">msRTCSIP-Service</span></span></p>
<p><span data-ttu-id="b7639-302">Msrtcsip-userenabled true-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="b7639-302">msRTCSIP-ConnectionPoint</span></span></p>
<p><span data-ttu-id="b7639-303">Msrtcsip-userenabled true-MediationServer</span><span class="sxs-lookup"><span data-stu-id="b7639-303">msRTCSIP-MediationServer</span></span></p>
<p><span data-ttu-id="b7639-304">Msrtcsip-userenabled true-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="b7639-304">msRTCSIP-ApplicationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-305">Msrtcsip-userenabled true-サービス</span><span class="sxs-lookup"><span data-stu-id="b7639-305">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="b7639-306">Msrtcsip-userenabled true-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="b7639-306">msRTCSIP-GlobalContainer</span></span></p>
<p><span data-ttu-id="b7639-307">Msrtcsip-userenabled true-プール</span><span class="sxs-lookup"><span data-stu-id="b7639-307">msRTCSIP-Pools</span></span></p>
<p><span data-ttu-id="b7639-308">Msrtcsip-userenabled true-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="b7639-308">msRTCSIP-MCUFactories</span></span></p>
<p><span data-ttu-id="b7639-309">Msrtcsip-userenabled true-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="b7639-309">msRTCSIP-TrustedMCUs</span></span></p>
<p><span data-ttu-id="b7639-310">Msrtcsip-userenabled true-Trustedwebservers サーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-310">msRTCSIP-TrustedWebComponentsServers</span></span></p>
<p><span data-ttu-id="b7639-311">Msrtcsip-userenabled true-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="b7639-311">msRTCSIP-TrustedProxies</span></span></p>
<p><span data-ttu-id="b7639-312">Msrtcsip-userenabled true-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="b7639-312">msRTCSIP-TrustedServices</span></span></p>
<p><span data-ttu-id="b7639-313">Msrtcsip-userenabled true-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="b7639-313">msRTCSIP-ApplicationContacts</span></span></p>
<p><span data-ttu-id="b7639-314">Msrtcsip-userenabled true-LocationContactMappings マッピング</span><span class="sxs-lookup"><span data-stu-id="b7639-314">msRTCSIP-LocationContactMappings</span></span></p>
<p><span data-ttu-id="b7639-315">Msrtcsip-userenabled true-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="b7639-315">msRTCSIP-ConferenceDirectories</span></span></p>
<p><span data-ttu-id="b7639-316">Msrtcsip-userenabled true-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="b7639-316">msRTCSIP-GlobalTopologySettings</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-317">Msrtcsip-userenabled true-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="b7639-317">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="b7639-318">Msrtcsip-userenabled true-ドメイン</span><span class="sxs-lookup"><span data-stu-id="b7639-318">msRTCSIP-Domain</span></span></p>
<p><span data-ttu-id="b7639-319">Msrtcsip-userenabled true-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="b7639-319">msRTCSIP-TrustedServer</span></span></p>
<p><span data-ttu-id="b7639-320">Msrtcsip-userenabled true-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="b7639-320">msRTCSIP-EdgeProxy</span></span></p>
<p><span data-ttu-id="b7639-321">Msrtcsip-userenabled true-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="b7639-321">msRTCSIP-MonitoringServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-322">Msrtcsip-userenabled true-プール</span><span class="sxs-lookup"><span data-stu-id="b7639-322">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="b7639-323">Msrtcsip-userenabled true プール</span><span class="sxs-lookup"><span data-stu-id="b7639-323">msRTCSIP-Pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-324">Msrtcsip-userenabled true-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="b7639-324">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="b7639-325">Msrtcsip-userenabled true-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="b7639-325">msRTCSIP-MCUFactory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-326">Msrtcsip-userenabled true-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="b7639-326">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="b7639-327">Msrtcsip-userenabled true-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="b7639-327">msRTCSIP-TrustedMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-328">Msrtcsip-userenabled true-Trustedwebservers サーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-328">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="b7639-329">Msrtcsip-userenabled true-Trustedwebのサーバー</span><span class="sxs-lookup"><span data-stu-id="b7639-329">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-330">Msrtcsip-userenabled true-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="b7639-330">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="b7639-331">Msrtcsip-userenabled true-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="b7639-331">msRTCSIP-TrustedProxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-332">Msrtcsip-userenabled true-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="b7639-332">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="b7639-333">Msrtcsip-userenabled true-TrustedService</span><span class="sxs-lookup"><span data-stu-id="b7639-333">msRTCSIP-TrustedService</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-334">Msrtcsip-userenabled true-LocationContactMappings マッピング</span><span class="sxs-lookup"><span data-stu-id="b7639-334">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="b7639-335">Msrtcsip-userenabled true-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="b7639-335">msRTCSIP-LocationContactMapping</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7639-336">Msrtcsip-userenabled true-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="b7639-336">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="b7639-337">Msrtcsip-userenabled true-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="b7639-337">msRTCSIP-ConferenceDirectory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7639-338">Msrtcsip-userenabled true-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="b7639-338">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="b7639-339">Msrtcsip-userenabled true-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="b7639-339">msRTCSIP-GlobalTopologySetting</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b7639-340">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7639-340">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

