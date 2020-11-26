---
title: 'Lync Server 2013: UCWA イベント'
description: 'Lync Server 2013: UCWA イベント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440466"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="c5037-103">Lync Server での UCWA 2013</span><span class="sxs-lookup"><span data-stu-id="c5037-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5037-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5037-104">

<span> </span></span></span>

<span data-ttu-id="c5037-105">_**最終更新日:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="c5037-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="c5037-106">Lync Server 2013 は、Microsoft Exchange に連絡して、モバイルクライアントのプレゼンスを更新するなど、さまざまな目的で、ユニファイドコミュニケーション Web API (UCWA) を使用します。</span><span class="sxs-lookup"><span data-stu-id="c5037-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="c5037-p101">UCWA は、実行動作の記録を、"情報"、"警告"、および "エラー" のイベントの種類として書き込みます。次の表に、UCWA コンポーネントによって書き込まれる可能性があるイベントを示します。</span><span class="sxs-lookup"><span data-stu-id="c5037-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5037-109">イベント ID</span><span class="sxs-lookup"><span data-stu-id="c5037-109">Event ID</span></span></th>
<th><span data-ttu-id="c5037-110">イベントの種類</span><span class="sxs-lookup"><span data-stu-id="c5037-110">Event Type</span></span></th>
<th><span data-ttu-id="c5037-111">概要</span><span class="sxs-lookup"><span data-stu-id="c5037-111">Summary</span></span></th>
<th><span data-ttu-id="c5037-112">原因と解決策</span><span class="sxs-lookup"><span data-stu-id="c5037-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5037-113">20001</span><span class="sxs-lookup"><span data-stu-id="c5037-113">20001</span></span></p></td>
<td><p><span data-ttu-id="c5037-114">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-115">UCWA が初期化されました</span><span class="sxs-lookup"><span data-stu-id="c5037-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="c5037-116">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-116">N/A</span></span></p>
<p><span data-ttu-id="c5037-117">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-118">20002</span><span class="sxs-lookup"><span data-stu-id="c5037-118">20002</span></span></p></td>
<td><p><span data-ttu-id="c5037-119">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-119">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-120">初期化中に UCWA で予期しない例外が発生しました</span><span class="sxs-lookup"><span data-stu-id="c5037-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="c5037-121">初期化中に予期しないエラーが発生しました</span><span class="sxs-lookup"><span data-stu-id="c5037-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="c5037-122">関連付けられたイベント ログ エントリで例外の詳細を調査し、可能性のある原因を特定します</span><span class="sxs-lookup"><span data-stu-id="c5037-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-123">20003</span><span class="sxs-lookup"><span data-stu-id="c5037-123">20003</span></span></p></td>
<td><p><span data-ttu-id="c5037-124">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-124">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-125">UCWA で処理不能な例外が発生しました</span><span class="sxs-lookup"><span data-stu-id="c5037-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="c5037-126">処理不能な例外が発生しました</span><span class="sxs-lookup"><span data-stu-id="c5037-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="c5037-p102">サーバーを再起動します。問題が解決しない場合は、製品サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c5037-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-129">20004</span><span class="sxs-lookup"><span data-stu-id="c5037-129">20004</span></span></p></td>
<td><p><span data-ttu-id="c5037-130">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-130">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-131">Exchange の HD 写真にアクセスできません</span><span class="sxs-lookup"><span data-stu-id="c5037-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="c5037-132">Exchange への接続を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="c5037-133">Exchange への接続が利用できることを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-134">20005</span><span class="sxs-lookup"><span data-stu-id="c5037-134">20005</span></span></p></td>
<td><p><span data-ttu-id="c5037-135">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-136">Exchange の HD 写真にアクセスできないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="c5037-137">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-138">20006</span><span class="sxs-lookup"><span data-stu-id="c5037-138">20006</span></span></p></td>
<td><p><span data-ttu-id="c5037-139">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-139">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-140">Exchange の連絡先検索にアクセスできません</span><span class="sxs-lookup"><span data-stu-id="c5037-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="c5037-141">Exchange への接続を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="c5037-142">Exchange への接続が利用できることを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-143">20007</span><span class="sxs-lookup"><span data-stu-id="c5037-143">20007</span></span></p></td>
<td><p><span data-ttu-id="c5037-144">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-145">Exchange の連絡先を検索できないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="c5037-146">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-147">20008</span><span class="sxs-lookup"><span data-stu-id="c5037-147">20008</span></span></p></td>
<td><p><span data-ttu-id="c5037-148">警告</span><span class="sxs-lookup"><span data-stu-id="c5037-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="c5037-149">アプリケーションごとの許容数を超えるプレゼンス サブスクリプションの登録が試行されました</span><span class="sxs-lookup"><span data-stu-id="c5037-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="c5037-150">アプリケーションごとの許容数を超えるプレゼンス サブスクリプションの登録が試行されました</span><span class="sxs-lookup"><span data-stu-id="c5037-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="c5037-151">クライアントに不要なサブスクリプションがないかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-152">20009</span><span class="sxs-lookup"><span data-stu-id="c5037-152">20009</span></span></p></td>
<td><p><span data-ttu-id="c5037-153">警告</span><span class="sxs-lookup"><span data-stu-id="c5037-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="c5037-154">バッチごとの許容数を超えるプレゼンス サブスクリプションの登録が試行されました</span><span class="sxs-lookup"><span data-stu-id="c5037-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="c5037-155">バッチごとの許容数を超えるプレゼンス サブスクリプションの登録が試行されました</span><span class="sxs-lookup"><span data-stu-id="c5037-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="c5037-156">クライアントに不要なサブスクリプションがないかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-157">20010</span><span class="sxs-lookup"><span data-stu-id="c5037-157">20010</span></span></p></td>
<td><p><span data-ttu-id="c5037-158">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-158">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-159">インバンド データを取得できません</span><span class="sxs-lookup"><span data-stu-id="c5037-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="c5037-160">インバンド データを取得できません</span><span class="sxs-lookup"><span data-stu-id="c5037-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="c5037-161">問題が解決しない場合は、製品サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c5037-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-162">20011</span><span class="sxs-lookup"><span data-stu-id="c5037-162">20011</span></span></p></td>
<td><p><span data-ttu-id="c5037-163">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-163">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-164">プレゼンスを登録できません</span><span class="sxs-lookup"><span data-stu-id="c5037-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="c5037-165">プレゼンスを登録できません</span><span class="sxs-lookup"><span data-stu-id="c5037-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="c5037-166">問題が解決しない場合は、製品サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c5037-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-167">20012</span><span class="sxs-lookup"><span data-stu-id="c5037-167">20012</span></span></p></td>
<td><p><span data-ttu-id="c5037-168">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-168">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-169">エンドポイントの登録に失敗しました</span><span class="sxs-lookup"><span data-stu-id="c5037-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="c5037-170">エンドポイントの登録に失敗しました</span><span class="sxs-lookup"><span data-stu-id="c5037-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="c5037-171">問題が解決しない場合は、製品サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c5037-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-172">20013</span><span class="sxs-lookup"><span data-stu-id="c5037-172">20013</span></span></p></td>
<td><p><span data-ttu-id="c5037-173">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-173">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-174">IM MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="c5037-175">IM MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="c5037-176">IM MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-177">20014</span><span class="sxs-lookup"><span data-stu-id="c5037-177">20014</span></span></p></td>
<td><p><span data-ttu-id="c5037-178">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-179">IM MCU に接続できないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-180">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-181">20015</span><span class="sxs-lookup"><span data-stu-id="c5037-181">20015</span></span></p></td>
<td><p><span data-ttu-id="c5037-182">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-182">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-183">AV MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="c5037-184">AV MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="c5037-185">AV MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-186">20016</span><span class="sxs-lookup"><span data-stu-id="c5037-186">20016</span></span></p></td>
<td><p><span data-ttu-id="c5037-187">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-188">AV MCU に接続できないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-189">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-190">20017</span><span class="sxs-lookup"><span data-stu-id="c5037-190">20017</span></span></p></td>
<td><p><span data-ttu-id="c5037-191">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-191">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-192">AS MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="c5037-193">AS MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="c5037-194">AS MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-195">20018</span><span class="sxs-lookup"><span data-stu-id="c5037-195">20018</span></span></p></td>
<td><p><span data-ttu-id="c5037-196">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-197">AS MCU に接続できないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-198">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-199">20019</span><span class="sxs-lookup"><span data-stu-id="c5037-199">20019</span></span></p></td>
<td><p><span data-ttu-id="c5037-200">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-200">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-201">データ MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="c5037-202">データ MCU を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="c5037-203">データ MCU が実行されていることを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-204">20020</span><span class="sxs-lookup"><span data-stu-id="c5037-204">20020</span></span></p></td>
<td><p><span data-ttu-id="c5037-205">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-206">データ MCU に接続できないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-207">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-208">20021</span><span class="sxs-lookup"><span data-stu-id="c5037-208">20021</span></span></p></td>
<td><p><span data-ttu-id="c5037-209">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-209">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-210">IM MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-211">IM MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="c5037-212">IM MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-213">20022</span><span class="sxs-lookup"><span data-stu-id="c5037-213">20022</span></span></p></td>
<td><p><span data-ttu-id="c5037-214">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-214">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-215">AV MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-216">AV MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="c5037-217">AV MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-218">20023</span><span class="sxs-lookup"><span data-stu-id="c5037-218">20023</span></span></p></td>
<td><p><span data-ttu-id="c5037-219">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-219">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-220">AS MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-221">AS MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="c5037-222">AS MCU が実行されているかどうかを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-223">20024</span><span class="sxs-lookup"><span data-stu-id="c5037-223">20024</span></span></p></td>
<td><p><span data-ttu-id="c5037-224">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-224">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-225">データ MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="c5037-226">データ MCU に参加できません</span><span class="sxs-lookup"><span data-stu-id="c5037-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="c5037-227">データ MCU が実行されていることを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-228">20025</span><span class="sxs-lookup"><span data-stu-id="c5037-228">20025</span></span></p></td>
<td><p><span data-ttu-id="c5037-229">エラー</span><span class="sxs-lookup"><span data-stu-id="c5037-229">Error</span></span></p></td>
<td><p><span data-ttu-id="c5037-230">Active Directory の写真にアクセスできません</span><span class="sxs-lookup"><span data-stu-id="c5037-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="c5037-231">Active Directory への接続を利用できません</span><span class="sxs-lookup"><span data-stu-id="c5037-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="c5037-232">Active Directory への接続が利用できることを確認します</span><span class="sxs-lookup"><span data-stu-id="c5037-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5037-233">20026</span><span class="sxs-lookup"><span data-stu-id="c5037-233">20026</span></span></p></td>
<td><p><span data-ttu-id="c5037-234">情報</span><span class="sxs-lookup"><span data-stu-id="c5037-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="c5037-235">Active Directory の写真にアクセスできないエラーから復旧しました</span><span class="sxs-lookup"><span data-stu-id="c5037-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="c5037-236">該当なし</span><span class="sxs-lookup"><span data-stu-id="c5037-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5037-237">20027</span><span class="sxs-lookup"><span data-stu-id="c5037-237">20027</span></span></p></td>
<td><p><span data-ttu-id="c5037-238">警告</span><span class="sxs-lookup"><span data-stu-id="c5037-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="c5037-239">逆シリアル化できません</span><span class="sxs-lookup"><span data-stu-id="c5037-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="c5037-240">逆シリアル化できません</span><span class="sxs-lookup"><span data-stu-id="c5037-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="c5037-241">問題が解決しない場合は、製品サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c5037-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c5037-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5037-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

