---
title: 'Lync Server 2013: UserAgentDef テーブル'
description: 'Lync Server 2013: UserAgentDef テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table
ms:assetid: 96c49239-d999-4045-8b64-9d1940cce8ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205100(v=OCS.15)
ms:contentKeyID: 48184860
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a9b12239d0d6ba6e04a708708a1740dbf02c0e07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439038"
---
# <a name="useragentdef-table-in-lync-server-2013"></a><span data-ttu-id="46bd6-103">Lync Server 2013 の UserAgentDef テーブル</span><span class="sxs-lookup"><span data-stu-id="46bd6-103">UserAgentDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46bd6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46bd6-104">

<span> </span></span></span>

<span data-ttu-id="46bd6-105">_**最終更新日:** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="46bd6-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="46bd6-106">UserAgentDef テーブルは、ユーザーエージェント識別子をエージェントのわかりやすい名前にマップします。</span><span class="sxs-lookup"><span data-stu-id="46bd6-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="46bd6-107">ユーザーエージェントは、Microsoft Lync Server 2013 に接続するために使用されるソフトウェアクライアントです。</span><span class="sxs-lookup"><span data-stu-id="46bd6-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span> <span data-ttu-id="46bd6-108">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="46bd6-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46bd6-109">UAType</span><span class="sxs-lookup"><span data-stu-id="46bd6-109">UAType</span></span></th>
<th><span data-ttu-id="46bd6-110">UAName</span><span class="sxs-lookup"><span data-stu-id="46bd6-110">UAName</span></span></th>
<th><span data-ttu-id="46bd6-111">UACategory</span><span class="sxs-lookup"><span data-stu-id="46bd6-111">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-112">1</span><span class="sxs-lookup"><span data-stu-id="46bd6-112">1</span></span></p></td>
<td><p><span data-ttu-id="46bd6-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="46bd6-113">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="46bd6-114">MediationServer</span><span class="sxs-lookup"><span data-stu-id="46bd6-114">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-115">2</span><span class="sxs-lookup"><span data-stu-id="46bd6-115">2</span></span></p></td>
<td><p><span data-ttu-id="46bd6-116">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="46bd6-116">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="46bd6-117">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="46bd6-117">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-118">4</span><span class="sxs-lookup"><span data-stu-id="46bd6-118">4</span></span></p></td>
<td><p><span data-ttu-id="46bd6-119">OC</span><span class="sxs-lookup"><span data-stu-id="46bd6-119">OC</span></span></p></td>
<td><p><span data-ttu-id="46bd6-120">OC</span><span class="sxs-lookup"><span data-stu-id="46bd6-120">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-121">個</span><span class="sxs-lookup"><span data-stu-id="46bd6-121">8</span></span></p></td>
<td><p><span data-ttu-id="46bd6-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="46bd6-122">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="46bd6-123">OCPhone</span><span class="sxs-lookup"><span data-stu-id="46bd6-123">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-124">16</span><span class="sxs-lookup"><span data-stu-id="46bd6-124">16</span></span></p></td>
<td><p><span data-ttu-id="46bd6-125">LMC</span><span class="sxs-lookup"><span data-stu-id="46bd6-125">LMC</span></span></p></td>
<td><p><span data-ttu-id="46bd6-126">LMC</span><span class="sxs-lookup"><span data-stu-id="46bd6-126">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-127">32</span><span class="sxs-lookup"><span data-stu-id="46bd6-127">32</span></span></p></td>
<td><p><span data-ttu-id="46bd6-128">DVT</span><span class="sxs-lookup"><span data-stu-id="46bd6-128">DVT</span></span></p></td>
<td><p><span data-ttu-id="46bd6-129">DVT</span><span class="sxs-lookup"><span data-stu-id="46bd6-129">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-130">64</span><span class="sxs-lookup"><span data-stu-id="46bd6-130">64</span></span></p></td>
<td><p><span data-ttu-id="46bd6-131">TU</span><span class="sxs-lookup"><span data-stu-id="46bd6-131">MM</span></span></p></td>
<td><p><span data-ttu-id="46bd6-132">TU</span><span class="sxs-lookup"><span data-stu-id="46bd6-132">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-133">64</span><span class="sxs-lookup"><span data-stu-id="46bd6-133">64</span></span></p></td>
<td><p><span data-ttu-id="46bd6-134">MC</span><span class="sxs-lookup"><span data-stu-id="46bd6-134">MC</span></span></p></td>
<td><p><span data-ttu-id="46bd6-135">TU</span><span class="sxs-lookup"><span data-stu-id="46bd6-135">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-136">128</span><span class="sxs-lookup"><span data-stu-id="46bd6-136">128</span></span></p></td>
<td><p><span data-ttu-id="46bd6-137">Attendant</span><span class="sxs-lookup"><span data-stu-id="46bd6-137">Attendant</span></span></p></td>
<td><p><span data-ttu-id="46bd6-138">Attendant</span><span class="sxs-lookup"><span data-stu-id="46bd6-138">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-139">256</span><span class="sxs-lookup"><span data-stu-id="46bd6-139">256</span></span></p></td>
<td><p><span data-ttu-id="46bd6-140">Conferencing_Announcement_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="46bd6-140">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="46bd6-141">CAS</span><span class="sxs-lookup"><span data-stu-id="46bd6-141">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-142">512</span><span class="sxs-lookup"><span data-stu-id="46bd6-142">512</span></span></p></td>
<td><p><span data-ttu-id="46bd6-143">Conferencing_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="46bd6-143">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="46bd6-144">CAA を</span><span class="sxs-lookup"><span data-stu-id="46bd6-144">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-145">512</span><span class="sxs-lookup"><span data-stu-id="46bd6-145">512</span></span></p></td>
<td><p><span data-ttu-id="46bd6-146">Conference_Auto_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="46bd6-146">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="46bd6-147">CAA を</span><span class="sxs-lookup"><span data-stu-id="46bd6-147">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-148">1024</span><span class="sxs-lookup"><span data-stu-id="46bd6-148">1024</span></span></p></td>
<td><p><span data-ttu-id="46bd6-149">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="46bd6-149">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="46bd6-150">RGS</span><span class="sxs-lookup"><span data-stu-id="46bd6-150">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-151">1032</span><span class="sxs-lookup"><span data-stu-id="46bd6-151">1032</span></span></p></td>
<td><p><span data-ttu-id="46bd6-152">Call_Park_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="46bd6-152">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="46bd6-153">RESERVED</span><span class="sxs-lookup"><span data-stu-id="46bd6-153">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-154">1040</span><span class="sxs-lookup"><span data-stu-id="46bd6-154">1040</span></span></p></td>
<td><p><span data-ttu-id="46bd6-155">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="46bd6-155">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="46bd6-156">も</span><span class="sxs-lookup"><span data-stu-id="46bd6-156">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-157">2048</span><span class="sxs-lookup"><span data-stu-id="46bd6-157">2048</span></span></p></td>
<td><p><span data-ttu-id="46bd6-158">Microsoft Rtc. アプリケーションの Ccs</span><span class="sxs-lookup"><span data-stu-id="46bd6-158">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="46bd6-159">CCS</span><span class="sxs-lookup"><span data-stu-id="46bd6-159">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-160">16386</span><span class="sxs-lookup"><span data-stu-id="46bd6-160">16386</span></span></p></td>
<td><p><span data-ttu-id="46bd6-161">CoMo</span><span class="sxs-lookup"><span data-stu-id="46bd6-161">CoMo</span></span></p></td>
<td><p><span data-ttu-id="46bd6-162">CoMo</span><span class="sxs-lookup"><span data-stu-id="46bd6-162">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-163">16387</span><span class="sxs-lookup"><span data-stu-id="46bd6-163">16387</span></span></p></td>
<td><p><span data-ttu-id="46bd6-164">CWA</span><span class="sxs-lookup"><span data-stu-id="46bd6-164">CWA</span></span></p></td>
<td><p><span data-ttu-id="46bd6-165">CWA</span><span class="sxs-lookup"><span data-stu-id="46bd6-165">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-166">16388</span><span class="sxs-lookup"><span data-stu-id="46bd6-166">16388</span></span></p></td>
<td><p><span data-ttu-id="46bd6-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="46bd6-167">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="46bd6-168">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="46bd6-168">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-169">16389</span><span class="sxs-lookup"><span data-stu-id="46bd6-169">16389</span></span></p></td>
<td><p><span data-ttu-id="46bd6-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="46bd6-170">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="46bd6-171">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="46bd6-171">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-172">16393</span><span class="sxs-lookup"><span data-stu-id="46bd6-172">16393</span></span></p></td>
<td><p><span data-ttu-id="46bd6-173">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="46bd6-173">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="46bd6-174">ExUM</span><span class="sxs-lookup"><span data-stu-id="46bd6-174">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-175">16395</span><span class="sxs-lookup"><span data-stu-id="46bd6-175">16395</span></span></p></td>
<td><p><span data-ttu-id="46bd6-176">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="46bd6-176">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="46bd6-177">ARCH AGENT</span><span class="sxs-lookup"><span data-stu-id="46bd6-177">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-178">16396</span><span class="sxs-lookup"><span data-stu-id="46bd6-178">16396</span></span></p></td>
<td><p><span data-ttu-id="46bd6-179">短期</span><span class="sxs-lookup"><span data-stu-id="46bd6-179">ST</span></span></p></td>
<td><p><span data-ttu-id="46bd6-180">短期</span><span class="sxs-lookup"><span data-stu-id="46bd6-180">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-181">16397</span><span class="sxs-lookup"><span data-stu-id="46bd6-181">16397</span></span></p></td>
<td><p><span data-ttu-id="46bd6-182">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="46bd6-182">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="46bd6-183">ASMCU</span><span class="sxs-lookup"><span data-stu-id="46bd6-183">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-184">16398</span><span class="sxs-lookup"><span data-stu-id="46bd6-184">16398</span></span></p></td>
<td><p><span data-ttu-id="46bd6-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-185">WPLync</span></span></p></td>
<td><p><span data-ttu-id="46bd6-186">WPLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-186">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-187">16399</span><span class="sxs-lookup"><span data-stu-id="46bd6-187">16399</span></span></p></td>
<td><p><span data-ttu-id="46bd6-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-188">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="46bd6-189">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-189">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-190">16400</span><span class="sxs-lookup"><span data-stu-id="46bd6-190">16400</span></span></p></td>
<td><p><span data-ttu-id="46bd6-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-191">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="46bd6-192">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-192">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-193">16401</span><span class="sxs-lookup"><span data-stu-id="46bd6-193">16401</span></span></p></td>
<td><p><span data-ttu-id="46bd6-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-194">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="46bd6-195">iPadLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-195">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-196">16402</span><span class="sxs-lookup"><span data-stu-id="46bd6-196">16402</span></span></p></td>
<td><p><span data-ttu-id="46bd6-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-197">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="46bd6-198">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="46bd6-198">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-199">16403</span><span class="sxs-lookup"><span data-stu-id="46bd6-199">16403</span></span></p></td>
<td><p><span data-ttu-id="46bd6-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="46bd6-200">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="46bd6-201">LyncImm</span><span class="sxs-lookup"><span data-stu-id="46bd6-201">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-202">16404</span><span class="sxs-lookup"><span data-stu-id="46bd6-202">16404</span></span></p></td>
<td><p><span data-ttu-id="46bd6-203">SKYDRIVE</span><span class="sxs-lookup"><span data-stu-id="46bd6-203">PCS</span></span></p></td>
<td><p><span data-ttu-id="46bd6-204">SKYDRIVE</span><span class="sxs-lookup"><span data-stu-id="46bd6-204">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-205">16405</span><span class="sxs-lookup"><span data-stu-id="46bd6-205">16405</span></span></p></td>
<td><p><span data-ttu-id="46bd6-206">LWA</span><span class="sxs-lookup"><span data-stu-id="46bd6-206">LWA</span></span></p></td>
<td><p><span data-ttu-id="46bd6-207">LWA</span><span class="sxs-lookup"><span data-stu-id="46bd6-207">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-208">16406</span><span class="sxs-lookup"><span data-stu-id="46bd6-208">16406</span></span></p></td>
<td><p><span data-ttu-id="46bd6-209">OUTLOOK</span><span class="sxs-lookup"><span data-stu-id="46bd6-209">OWA</span></span></p></td>
<td><p><span data-ttu-id="46bd6-210">OUTLOOK</span><span class="sxs-lookup"><span data-stu-id="46bd6-210">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-211">16407</span><span class="sxs-lookup"><span data-stu-id="46bd6-211">16407</span></span></p></td>
<td><p><span data-ttu-id="46bd6-212">AOC</span><span class="sxs-lookup"><span data-stu-id="46bd6-212">AOC</span></span></p></td>
<td><p><span data-ttu-id="46bd6-213">AOC</span><span class="sxs-lookup"><span data-stu-id="46bd6-213">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-214">16408</span><span class="sxs-lookup"><span data-stu-id="46bd6-214">16408</span></span></p></td>
<td><p><span data-ttu-id="46bd6-215">GCC</span><span class="sxs-lookup"><span data-stu-id="46bd6-215">GCC</span></span></p></td>
<td><p><span data-ttu-id="46bd6-216">GCC</span><span class="sxs-lookup"><span data-stu-id="46bd6-216">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-217">16409</span><span class="sxs-lookup"><span data-stu-id="46bd6-217">16409</span></span></p></td>
<td><p><span data-ttu-id="46bd6-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="46bd6-218">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="46bd6-219">IMMCU</span><span class="sxs-lookup"><span data-stu-id="46bd6-219">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-220">16410</span><span class="sxs-lookup"><span data-stu-id="46bd6-220">16410</span></span></p></td>
<td><p><span data-ttu-id="46bd6-221">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="46bd6-221">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="46bd6-222">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="46bd6-222">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bd6-223">32769</span><span class="sxs-lookup"><span data-stu-id="46bd6-223">32769</span></span></p></td>
<td><p><span data-ttu-id="46bd6-224">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="46bd6-224">Gateway</span></span></p></td>
<td><p><span data-ttu-id="46bd6-225">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="46bd6-225">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bd6-226">32770</span><span class="sxs-lookup"><span data-stu-id="46bd6-226">32770</span></span></p></td>
<td><p><span data-ttu-id="46bd6-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="46bd6-227">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="46bd6-228">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="46bd6-228">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="46bd6-229">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46bd6-229">


</div>

<span> </span>

</div>

</div>

</span></span></div>

