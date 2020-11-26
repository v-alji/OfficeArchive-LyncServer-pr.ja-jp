---
title: 'Lync Server 2013: UserAgentDef テーブル (QoE)'
description: 'Lync Server 2013: UserAgentDef テーブル (QoE)。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table (QoE)
ms:assetid: cfd8e3e0-4076-4162-9381-5276da8316d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205259(v=OCS.15)
ms:contentKeyID: 48185394
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8546a33e607524b23755e9abf3edb2d5e2e417d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439045"
---
# <a name="useragentdef-table-qoe-in-lync-server-2013"></a><span data-ttu-id="89455-103">Lync Server 2013 の UserAgentDef テーブル (QoE)</span><span class="sxs-lookup"><span data-stu-id="89455-103">UserAgentDef table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89455-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89455-104">

<span> </span></span></span>

<span data-ttu-id="89455-105">_**最終更新日:** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="89455-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="89455-106">UserAgentDef テーブルは、ユーザーエージェント識別子をエージェントのわかりやすい名前にマップします。</span><span class="sxs-lookup"><span data-stu-id="89455-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="89455-107">ユーザーエージェントは、Microsoft Lync Server 2013 に接続するために使用されるソフトウェアクライアントです。</span><span class="sxs-lookup"><span data-stu-id="89455-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89455-108">UAType</span><span class="sxs-lookup"><span data-stu-id="89455-108">UAType</span></span></th>
<th><span data-ttu-id="89455-109">UAName</span><span class="sxs-lookup"><span data-stu-id="89455-109">UAName</span></span></th>
<th><span data-ttu-id="89455-110">UACategory</span><span class="sxs-lookup"><span data-stu-id="89455-110">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89455-111">1</span><span class="sxs-lookup"><span data-stu-id="89455-111">1</span></span></p></td>
<td><p><span data-ttu-id="89455-112">MediationServer</span><span class="sxs-lookup"><span data-stu-id="89455-112">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="89455-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="89455-113">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-114">2</span><span class="sxs-lookup"><span data-stu-id="89455-114">2</span></span></p></td>
<td><p><span data-ttu-id="89455-115">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="89455-115">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="89455-116">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="89455-116">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-117">4</span><span class="sxs-lookup"><span data-stu-id="89455-117">4</span></span></p></td>
<td><p><span data-ttu-id="89455-118">OC</span><span class="sxs-lookup"><span data-stu-id="89455-118">OC</span></span></p></td>
<td><p><span data-ttu-id="89455-119">OC</span><span class="sxs-lookup"><span data-stu-id="89455-119">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-120">個</span><span class="sxs-lookup"><span data-stu-id="89455-120">8</span></span></p></td>
<td><p><span data-ttu-id="89455-121">OCPhone</span><span class="sxs-lookup"><span data-stu-id="89455-121">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="89455-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="89455-122">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-123">16</span><span class="sxs-lookup"><span data-stu-id="89455-123">16</span></span></p></td>
<td><p><span data-ttu-id="89455-124">LMC</span><span class="sxs-lookup"><span data-stu-id="89455-124">LMC</span></span></p></td>
<td><p><span data-ttu-id="89455-125">LMC</span><span class="sxs-lookup"><span data-stu-id="89455-125">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-126">32</span><span class="sxs-lookup"><span data-stu-id="89455-126">32</span></span></p></td>
<td><p><span data-ttu-id="89455-127">DVT</span><span class="sxs-lookup"><span data-stu-id="89455-127">DVT</span></span></p></td>
<td><p><span data-ttu-id="89455-128">DVT</span><span class="sxs-lookup"><span data-stu-id="89455-128">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-129">64</span><span class="sxs-lookup"><span data-stu-id="89455-129">64</span></span></p></td>
<td><p><span data-ttu-id="89455-130">TU</span><span class="sxs-lookup"><span data-stu-id="89455-130">MM</span></span></p></td>
<td><p><span data-ttu-id="89455-131">TU</span><span class="sxs-lookup"><span data-stu-id="89455-131">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-132">64</span><span class="sxs-lookup"><span data-stu-id="89455-132">64</span></span></p></td>
<td><p><span data-ttu-id="89455-133">MC</span><span class="sxs-lookup"><span data-stu-id="89455-133">MC</span></span></p></td>
<td><p><span data-ttu-id="89455-134">TU</span><span class="sxs-lookup"><span data-stu-id="89455-134">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-135">128</span><span class="sxs-lookup"><span data-stu-id="89455-135">128</span></span></p></td>
<td><p><span data-ttu-id="89455-136">Attendant</span><span class="sxs-lookup"><span data-stu-id="89455-136">Attendant</span></span></p></td>
<td><p><span data-ttu-id="89455-137">Attendant</span><span class="sxs-lookup"><span data-stu-id="89455-137">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-138">256</span><span class="sxs-lookup"><span data-stu-id="89455-138">256</span></span></p></td>
<td><p><span data-ttu-id="89455-139">Conferencing_Announcement_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="89455-139">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="89455-140">CAS</span><span class="sxs-lookup"><span data-stu-id="89455-140">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-141">512</span><span class="sxs-lookup"><span data-stu-id="89455-141">512</span></span></p></td>
<td><p><span data-ttu-id="89455-142">Conferencing_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="89455-142">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="89455-143">CAA を</span><span class="sxs-lookup"><span data-stu-id="89455-143">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-144">512</span><span class="sxs-lookup"><span data-stu-id="89455-144">512</span></span></p></td>
<td><p><span data-ttu-id="89455-145">Conference_Auto_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="89455-145">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="89455-146">CAA を</span><span class="sxs-lookup"><span data-stu-id="89455-146">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-147">1024</span><span class="sxs-lookup"><span data-stu-id="89455-147">1024</span></span></p></td>
<td><p><span data-ttu-id="89455-148">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="89455-148">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="89455-149">RGS</span><span class="sxs-lookup"><span data-stu-id="89455-149">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-150">1032</span><span class="sxs-lookup"><span data-stu-id="89455-150">1032</span></span></p></td>
<td><p><span data-ttu-id="89455-151">Call_Park_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="89455-151">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="89455-152">RESERVED</span><span class="sxs-lookup"><span data-stu-id="89455-152">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-153">1040</span><span class="sxs-lookup"><span data-stu-id="89455-153">1040</span></span></p></td>
<td><p><span data-ttu-id="89455-154">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="89455-154">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="89455-155">も</span><span class="sxs-lookup"><span data-stu-id="89455-155">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-156">2048</span><span class="sxs-lookup"><span data-stu-id="89455-156">2048</span></span></p></td>
<td><p><span data-ttu-id="89455-157">Microsoft Rtc. アプリケーションの Ccs</span><span class="sxs-lookup"><span data-stu-id="89455-157">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="89455-158">CCS</span><span class="sxs-lookup"><span data-stu-id="89455-158">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-159">16386</span><span class="sxs-lookup"><span data-stu-id="89455-159">16386</span></span></p></td>
<td><p><span data-ttu-id="89455-160">CoMo</span><span class="sxs-lookup"><span data-stu-id="89455-160">CoMo</span></span></p></td>
<td><p><span data-ttu-id="89455-161">CoMo</span><span class="sxs-lookup"><span data-stu-id="89455-161">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-162">16387</span><span class="sxs-lookup"><span data-stu-id="89455-162">16387</span></span></p></td>
<td><p><span data-ttu-id="89455-163">CWA</span><span class="sxs-lookup"><span data-stu-id="89455-163">CWA</span></span></p></td>
<td><p><span data-ttu-id="89455-164">CWA</span><span class="sxs-lookup"><span data-stu-id="89455-164">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-165">16388</span><span class="sxs-lookup"><span data-stu-id="89455-165">16388</span></span></p></td>
<td><p><span data-ttu-id="89455-166">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="89455-166">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="89455-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="89455-167">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-168">16389</span><span class="sxs-lookup"><span data-stu-id="89455-168">16389</span></span></p></td>
<td><p><span data-ttu-id="89455-169">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="89455-169">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="89455-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="89455-170">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-171">16393</span><span class="sxs-lookup"><span data-stu-id="89455-171">16393</span></span></p></td>
<td><p><span data-ttu-id="89455-172">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="89455-172">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="89455-173">ExUM</span><span class="sxs-lookup"><span data-stu-id="89455-173">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-174">16395</span><span class="sxs-lookup"><span data-stu-id="89455-174">16395</span></span></p></td>
<td><p><span data-ttu-id="89455-175">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="89455-175">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="89455-176">ARCH AGENT</span><span class="sxs-lookup"><span data-stu-id="89455-176">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-177">16396</span><span class="sxs-lookup"><span data-stu-id="89455-177">16396</span></span></p></td>
<td><p><span data-ttu-id="89455-178">短期</span><span class="sxs-lookup"><span data-stu-id="89455-178">ST</span></span></p></td>
<td><p><span data-ttu-id="89455-179">短期</span><span class="sxs-lookup"><span data-stu-id="89455-179">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-180">16397</span><span class="sxs-lookup"><span data-stu-id="89455-180">16397</span></span></p></td>
<td><p><span data-ttu-id="89455-181">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="89455-181">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="89455-182">ASMCU</span><span class="sxs-lookup"><span data-stu-id="89455-182">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-183">16398</span><span class="sxs-lookup"><span data-stu-id="89455-183">16398</span></span></p></td>
<td><p><span data-ttu-id="89455-184">WPLync</span><span class="sxs-lookup"><span data-stu-id="89455-184">WPLync</span></span></p></td>
<td><p><span data-ttu-id="89455-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="89455-185">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-186">16399</span><span class="sxs-lookup"><span data-stu-id="89455-186">16399</span></span></p></td>
<td><p><span data-ttu-id="89455-187">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="89455-187">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="89455-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="89455-188">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-189">16400</span><span class="sxs-lookup"><span data-stu-id="89455-189">16400</span></span></p></td>
<td><p><span data-ttu-id="89455-190">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="89455-190">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="89455-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="89455-191">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-192">16401</span><span class="sxs-lookup"><span data-stu-id="89455-192">16401</span></span></p></td>
<td><p><span data-ttu-id="89455-193">iPadLync</span><span class="sxs-lookup"><span data-stu-id="89455-193">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="89455-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="89455-194">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-195">16402</span><span class="sxs-lookup"><span data-stu-id="89455-195">16402</span></span></p></td>
<td><p><span data-ttu-id="89455-196">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="89455-196">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="89455-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="89455-197">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-198">16403</span><span class="sxs-lookup"><span data-stu-id="89455-198">16403</span></span></p></td>
<td><p><span data-ttu-id="89455-199">LyncImm</span><span class="sxs-lookup"><span data-stu-id="89455-199">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="89455-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="89455-200">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-201">16404</span><span class="sxs-lookup"><span data-stu-id="89455-201">16404</span></span></p></td>
<td><p><span data-ttu-id="89455-202">SKYDRIVE</span><span class="sxs-lookup"><span data-stu-id="89455-202">PCS</span></span></p></td>
<td><p><span data-ttu-id="89455-203">SKYDRIVE</span><span class="sxs-lookup"><span data-stu-id="89455-203">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-204">16405</span><span class="sxs-lookup"><span data-stu-id="89455-204">16405</span></span></p></td>
<td><p><span data-ttu-id="89455-205">LWA</span><span class="sxs-lookup"><span data-stu-id="89455-205">LWA</span></span></p></td>
<td><p><span data-ttu-id="89455-206">LWA</span><span class="sxs-lookup"><span data-stu-id="89455-206">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-207">16406</span><span class="sxs-lookup"><span data-stu-id="89455-207">16406</span></span></p></td>
<td><p><span data-ttu-id="89455-208">OUTLOOK</span><span class="sxs-lookup"><span data-stu-id="89455-208">OWA</span></span></p></td>
<td><p><span data-ttu-id="89455-209">OUTLOOK</span><span class="sxs-lookup"><span data-stu-id="89455-209">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-210">16407</span><span class="sxs-lookup"><span data-stu-id="89455-210">16407</span></span></p></td>
<td><p><span data-ttu-id="89455-211">AOC</span><span class="sxs-lookup"><span data-stu-id="89455-211">AOC</span></span></p></td>
<td><p><span data-ttu-id="89455-212">AOC</span><span class="sxs-lookup"><span data-stu-id="89455-212">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-213">16408</span><span class="sxs-lookup"><span data-stu-id="89455-213">16408</span></span></p></td>
<td><p><span data-ttu-id="89455-214">GCC</span><span class="sxs-lookup"><span data-stu-id="89455-214">GCC</span></span></p></td>
<td><p><span data-ttu-id="89455-215">GCC</span><span class="sxs-lookup"><span data-stu-id="89455-215">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-216">16409</span><span class="sxs-lookup"><span data-stu-id="89455-216">16409</span></span></p></td>
<td><p><span data-ttu-id="89455-217">IMMCU</span><span class="sxs-lookup"><span data-stu-id="89455-217">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="89455-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="89455-218">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-219">16410</span><span class="sxs-lookup"><span data-stu-id="89455-219">16410</span></span></p></td>
<td><p><span data-ttu-id="89455-220">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="89455-220">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="89455-221">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="89455-221">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89455-222">32769</span><span class="sxs-lookup"><span data-stu-id="89455-222">32769</span></span></p></td>
<td><p><span data-ttu-id="89455-223">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="89455-223">Gateway</span></span></p></td>
<td><p><span data-ttu-id="89455-224">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="89455-224">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89455-225">32770</span><span class="sxs-lookup"><span data-stu-id="89455-225">32770</span></span></p></td>
<td><p><span data-ttu-id="89455-226">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="89455-226">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="89455-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="89455-227">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="89455-228">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89455-228">


</div>

<span> </span>

</div>

</div>

</span></span></div>

