---
title: 'Lync Server 2013: ボイスルール、ルート、ポリシーをテストする'
description: 'Lync Server 2013: ボイスルール、ルート、ポリシーをテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice rules, routes, and policies
ms:assetid: ebb9c3fa-6950-4311-87ca-e1ecd9280a43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725213(v=OCS.15)
ms:contentKeyID: 63969661
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf205ac2585298dfc5347d93e382e8bbda9f3ff4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398061"
---
# <a name="test-voice-rules-routes-and-policies-in-lync-server-2013"></a><span data-ttu-id="22e6f-103">Lync Server 2013 でのボイスルール、ルート、ポリシーのテスト</span><span class="sxs-lookup"><span data-stu-id="22e6f-103">Test voice rules, routes, and policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22e6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22e6f-104">

<span> </span></span></span>

<span data-ttu-id="22e6f-105">_**最終更新日:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="22e6f-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22e6f-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="22e6f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="22e6f-107">毎月</span><span class="sxs-lookup"><span data-stu-id="22e6f-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22e6f-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="22e6f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="22e6f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="22e6f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22e6f-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="22e6f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="22e6f-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="22e6f-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsVoiceUser コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceUser cmdlet.</span></span> <span data-ttu-id="22e6f-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="22e6f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceUser&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="22e6f-114">説明</span><span class="sxs-lookup"><span data-stu-id="22e6f-114">Description</span></span>

<span data-ttu-id="22e6f-115">ユーザーが電話をかけると、通話の発信先のルートは、そのユーザーに割り当てられているポリシーとダイヤルプランの両方によって異なります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-115">When a user makes a phone call, the route the call takes to reach its destination depends on both the policies and dial plans assigned to that user.</span></span> <span data-ttu-id="22e6f-116">ユーザーの SIP アドレスと電話番号を指定すると、Test-CsVoiceUser コマンドレットによって、該当するユーザーがその番号への通話を完了できるかどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="22e6f-116">Given a user’s SIP address and a phone number, the Test-CsVoiceUser cmdlet verifies whether the user in question can complete a call to that number.</span></span> <span data-ttu-id="22e6f-117">テストが成功した場合、Test-CsVoiceUser は次の値を返します。</span><span class="sxs-lookup"><span data-stu-id="22e6f-117">If the test succeeds, Test-CsVoiceUser returns the following:</span></span>

  - <span data-ttu-id="22e6f-118">番号が164形式に変換されます (ユーザーのダイヤルプランに基づく)</span><span class="sxs-lookup"><span data-stu-id="22e6f-118">The number translated to E.164 format (based on the user’s dial plan)</span></span>

  - <span data-ttu-id="22e6f-119">翻訳を提供した正規化ルール</span><span class="sxs-lookup"><span data-stu-id="22e6f-119">The normalization rule that supplied that translation</span></span>

  - <span data-ttu-id="22e6f-120">使用されているボイスルート (ルートの優先順位に基づく)</span><span class="sxs-lookup"><span data-stu-id="22e6f-120">The voice route used (based on route priority);</span></span>

  - <span data-ttu-id="22e6f-121">ユーザーのボイスポリシーを音声ルートにリンクした電話の使用状況。</span><span class="sxs-lookup"><span data-stu-id="22e6f-121">The phone usage that linked the user’s voice policy to the voice route.</span></span>

<span data-ttu-id="22e6f-122">Test-CsVoiceUser では、特定の電話番号が予期したとおりにルーティングおよび翻訳されるかどうかを決定できます。また、個々のユーザーが経験した通話関連の問題のトラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="22e6f-122">Test-CsVoiceUser enables you to determine whether a specific phone number will route and translate as expected, and can help troubleshoot call-related problems that are experienced by individual users.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="22e6f-123">テストの実行</span><span class="sxs-lookup"><span data-stu-id="22e6f-123">Running the test</span></span>

<span data-ttu-id="22e6f-124">Test-CsVoiceUser コマンドレットを実行するときには、ダイヤルされる番号とテストされるユーザーアカウントの Id の2つの情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-124">When running the Test-CsVoiceUser cmdlet you must supply two pieces of information: the number being dialed (DialedNumber) and the Identity of the user account being tested.</span></span> <span data-ttu-id="22e6f-125">たとえば、次のコマンドは、SIP アドレス sip:kenmyer@litwareinc.com を持っているユーザーが電話番号 + 1206555-1219 への通話を発信できるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="22e6f-125">For example, this command tests the ability of the user who has the SIP address sip:kenmyer@litwareinc.com to make a call to the phone number +1206555-1219:</span></span>

`Test-CsVoiceUser -DialedNumber "12065551219" -SipUri "sip:kenmyer@litwareinc.com"`

<span data-ttu-id="22e6f-126">電話番号は、ダイヤルする場合と同じように書式設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-126">The phone number should be formatted in the way that you expect it to be dialed.</span></span> <span data-ttu-id="22e6f-127">たとえば、通常、長距離通話を発信する前に1がダイヤルされない場合は、次の形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-127">For example, if users typically do not dial the 1 before placing a long distance call then you should use this format:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="22e6f-128">ただし、この場合、番号2065551219を正しく変換できる正規化ルールを持っていない場合、テストは失敗します。これは、Lync Server で使用されている電子電話形式の E.i になります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-128">Of course, in that case, the test will fail if you do not have a normalization rule that can correctly translate the number 2065551219 into the E.164 telephone format that is used by Lync Server.</span></span> <span data-ttu-id="22e6f-129">詳細については、「ヘルプトピック New-CsVoiceNormalizationRule コマンドレット」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22e6f-129">For more information, see the help topic New-CsVoiceNormalizationRule cmdlet.</span></span>

<span data-ttu-id="22e6f-130">各ユーザーアカウントに対して同じテストを実行する場合は、次のようなコマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="22e6f-130">If you want to run this same test against each of your user accounts, you can use a command similar to the following:</span></span>

`Get-CsUser | ForEach-Object {$_.DisplayName; Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri $_.SipAddress} | Format-List`

<span data-ttu-id="22e6f-131">詳細については、Test-CsVoiceUser コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="22e6f-131">For more information, see the Help documentation for the Test-CsVoiceUser cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="22e6f-132">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="22e6f-132">Determining success or failure</span></span>

<span data-ttu-id="22e6f-133">テストが正常に完了した場合 (つまり、ユーザーが指定した番号に電話をかけることができる場合)、出力には、翻訳された電話番号や、一致する正規化ルールとボイスルートなどの情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="22e6f-133">If the test is completed successfully (that is, if the user can make a phone call to the specified number), the output will show information like the translated phone number and the matching normalization rule and voice route:</span></span>

<span data-ttu-id="22e6f-134">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="22e6f-134">TranslatedNumber    MatchingRule    FirstMatchingRoute    MatchingUsage</span></span>

<span data-ttu-id="22e6f-135">\----------------    ------------    ------------------    -------------</span><span class="sxs-lookup"><span data-stu-id="22e6f-135">\----------------    ------------    ------------------    -------------</span></span>

<span data-ttu-id="22e6f-136">\+12065551219 Descripti   LocalRoute ローカル</span><span class="sxs-lookup"><span data-stu-id="22e6f-136">\+12065551219        Descripti...    LocalRoute            Local</span></span>

<span data-ttu-id="22e6f-137">Windows PowerShell 画面の制限により、少なくともいくつかの情報 (一致する正規化ルールの詳細な説明) が画面に表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-137">Because of the limitations of the Windows PowerShell screen, at least some returned information (most notably the full description of the matching normalization rule) might not appear on-screen.</span></span> <span data-ttu-id="22e6f-138">テストの成功または失敗のみを目的としている場合は、これは問題ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-138">If you are only interested in the success or failure of the test, then this might not matter.</span></span> <span data-ttu-id="22e6f-139">返されるデータの完全な詳細情報を表示したい場合は、テストの実行時に Format-List コマンドレットに出力をパイプします。</span><span class="sxs-lookup"><span data-stu-id="22e6f-139">If you would prefer to see the full details of the returned data then pipe the output to the Format-List cmdlet when running the test:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose | Format-List`

<span data-ttu-id="22e6f-140">これにより、次のような出力がわかりやすい形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="22e6f-140">That will display the output in a more reader-friendly format:</span></span>

<span data-ttu-id="22e6f-141">TranslatedNumber: + 12065551219</span><span class="sxs-lookup"><span data-stu-id="22e6f-141">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="22e6f-142">MatchingRule: Description =;Pattern = ^ ( \\ d {11} ) $;翻訳 = + $ 1;</span><span class="sxs-lookup"><span data-stu-id="22e6f-142">MatchingRule : Description=;Pattern=^(\\d{11})$;Translation=+$1;</span></span>

<span data-ttu-id="22e6f-143">Name = Prefix All; IsInternalExtension = False</span><span class="sxs-lookup"><span data-stu-id="22e6f-143">Name=Prefix All;IsInternalExtension=False</span></span>

<span data-ttu-id="22e6f-144">FirsMatchingRoute: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="22e6f-144">FirsMatchingRoute : LocalRoute</span></span>

<span data-ttu-id="22e6f-145">MatchingUsage: Local</span><span class="sxs-lookup"><span data-stu-id="22e6f-145">MatchingUsage : Local</span></span>

<span data-ttu-id="22e6f-146">テストに失敗した場合、Test-CsVoiceUser は、空のプロパティ値のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="22e6f-146">If the test fails, Test-CsVoiceUser will return an empty set of property values:</span></span>

<span data-ttu-id="22e6f-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="22e6f-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="22e6f-148">\---------------- ------------ ------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="22e6f-148">\---------------- ------------ ------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="22e6f-149">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="22e6f-149">Reasons why the test might have failed</span></span>

<span data-ttu-id="22e6f-150">Test-CsVoiceUser コマンドレットが失敗する可能性がある理由はいくつかあります。指定した電話番号を変換できる正規化ルールがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-150">There are any number of reasons why the Test-CsVoiceUser cmdlet might fail: there might not be a normalization rule that can translate the provided phone number.</span></span> <span data-ttu-id="22e6f-151">ボイスルーティングで問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-151">There could be problems with the voice route.</span></span> <span data-ttu-id="22e6f-152">問題のユーザーに割り当てられているダイヤルプランの構成で問題が発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-152">There could be a configuration issue with the dial plan assigned to the user in question.</span></span> <span data-ttu-id="22e6f-153">このため、Test-CsVoiceUser コマンドレットを実行する場合は、Verbose パラメーターを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-153">Because of that, you might want to include the Verbose parameter when you are running the Test-CsVoiceUser cmdlet:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose`

<span data-ttu-id="22e6f-154">Verbose コマンドレットが含まれている場合、Test-CsVoiceUser は、実行中のすべての手順について、詳細なアカウントを確認します。</span><span class="sxs-lookup"><span data-stu-id="22e6f-154">When the Verbose cmdlet is included, Test-CsVoiceUser will issue a detailed account of all the steps in takes when conducting its checks.</span></span> <span data-ttu-id="22e6f-155">たとえば、次のような手順が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-155">For example, you might see steps similar to these:</span></span> 

<span data-ttu-id="22e6f-156">VERBOSE: id が "sip:kenmyer@litwareinc.com" のユーザーを検索しています</span><span class="sxs-lookup"><span data-stu-id="22e6f-156">VERBOSE: Locating user with identity "sip:kenmyer@litwareinc.com"</span></span>

<span data-ttu-id="22e6f-157">詳細: ダイヤルプランを読み込み中: "RedmondDialPlan"</span><span class="sxs-lookup"><span data-stu-id="22e6f-157">VERBOSE: Loading dial plan: "RedmondDialPlan"</span></span>

<span data-ttu-id="22e6f-158">この追加情報は、エラーの原因を特定するために実行できる手順についてのヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="22e6f-158">This additional information can provide hints as to the steps that you can take to pinpoint the cause of the failure.</span></span> <span data-ttu-id="22e6f-159">たとえば、ここに表示される verbose の出力では、テスト対象のユーザーにダイヤルプランの RedmondDialPlan が割り当てられたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-159">For example, the verbose output shown here tells us that the user being tested was assigned the dial plan RedmondDialPlan.</span></span> <span data-ttu-id="22e6f-160">テストが失敗した場合は、RedmondDialPlan が指定した電話番号を翻訳できるかどうかを確認するための論理的な次の手順があります。</span><span class="sxs-lookup"><span data-stu-id="22e6f-160">If the test has failed, one logical next step would be to verify that RedmondDialPlan can translate the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="22e6f-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="22e6f-161">See Also</span></span>


[<span data-ttu-id="22e6f-162">テスト-Get-csvoiceuser</span><span class="sxs-lookup"><span data-stu-id="22e6f-162">Test-CsVoiceUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceUser)  
  

<span data-ttu-id="22e6f-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22e6f-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

