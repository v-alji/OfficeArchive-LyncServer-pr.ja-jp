---
title: 'Lync Server 2013: ボイスポリシーに対して電話番号をテストする'
description: 'Lync Server 2013: ボイスポリシーに対して電話番号をテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice policy
ms:assetid: 30c51700-17c6-4c57-891a-8d5ec30b50ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725207(v=OCS.15)
ms:contentKeyID: 63969596
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a6523e7657bd4c30c23909bb02e2569b6067298
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441222"
---
# <a name="test-telephone-number-against-a-voice-policy-in-lync-server-2013"></a><span data-ttu-id="2e239-103">Lync Server 2013 でボイスポリシーに対して電話番号をテストする</span><span class="sxs-lookup"><span data-stu-id="2e239-103">Test telephone number against a voice policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e239-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e239-104">

<span> </span></span></span>

<span data-ttu-id="2e239-105">_**最終更新日:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="2e239-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e239-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="2e239-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="2e239-107">毎月</span><span class="sxs-lookup"><span data-stu-id="2e239-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e239-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="2e239-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="2e239-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e239-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e239-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="2e239-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="2e239-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e239-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="2e239-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsVoicePolicy コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e239-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="2e239-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2e239-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoicePolicy&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="2e239-114">説明</span><span class="sxs-lookup"><span data-stu-id="2e239-114">Description</span></span>

<span data-ttu-id="2e239-115">エンタープライズボイスユーザーが公衆交換電話網 (PSTN) のヒンジを介して発信電話を発信する機能 (大きな部分) は、次の3つの点です。</span><span class="sxs-lookup"><span data-stu-id="2e239-115">The ability of Enterprise Voice users to make outgoing phone calls over the Public Switched Telephone network (PSTN) hinges, in large part, on three things:</span></span>

  - <span data-ttu-id="2e239-116">ユーザーに割り当てられている音声ポリシー。</span><span class="sxs-lookup"><span data-stu-id="2e239-116">The voice policy assigned to the user.</span></span>

  - <span data-ttu-id="2e239-117">Lync Server から PSTN ネットワークへの通話をルーティングするために使用される音声ルート。</span><span class="sxs-lookup"><span data-stu-id="2e239-117">The voice routes used to route calls from Lync Server to the PSTN network.</span></span>

  - <span data-ttu-id="2e239-118">PSTN の使用状況。ボイスポリシーをボイスルートに接続する Lync Server プロパティ。</span><span class="sxs-lookup"><span data-stu-id="2e239-118">The PSTN usage, a Lync Server property that connects a voice policy to a voice route.</span></span>

<span data-ttu-id="2e239-119">PSTN の使用は特に重要です。ボイスポリシーをボイスルートに接続するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="2e239-119">The PSTN usage is especially important: it’s the property that connects a voice policy to a voice route.</span></span> <span data-ttu-id="2e239-120">(音声ポリシーと音声ルートは、少なくとも1つの PSTN が一般的に使用されている場合、接続されていると言われます)。ボイスポリシーは、PSTN の使用を指定せずに構成できます。</span><span class="sxs-lookup"><span data-stu-id="2e239-120">(A voice policy and a voice route are said to be connected if they have at least one PSTN usage in common.) Voice policies can be configured without specifying a PSTN usage.</span></span> <span data-ttu-id="2e239-121">その場合、そのポリシーを割り当てられたユーザーは、PSTN ネットワーク経由での発信通話を行うことができません。</span><span class="sxs-lookup"><span data-stu-id="2e239-121">In that case, users who were assigned that policy won't be able to make outgoing calls over the PSTN network.</span></span> <span data-ttu-id="2e239-122">同様に、少なくとも1つの PSTN 使用量が指定されていないボイスルーティングでは、通話を PSTN ネットワークにルーティングすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2e239-122">Likewise, voice routes that do not have at least one specified PSTN usage will be unable to route calls to the PSTN network.</span></span>

<span data-ttu-id="2e239-123">Test-CsVoicePolicy コマンドレットは、指定された音声ポリシーの使用状況が PSTN であり、少なくとも1つのボイスルートによって使用が共有されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e239-123">The Test-CsVoicePolicy cmdlet verifies that a given voice policy has a PSTN usage and that the usage is shared by at least one voice route.</span></span> <span data-ttu-id="2e239-124">Test-CsVoicePolicy による検証が正常に実行された場合、コマンドレットは、最初に見つかった有効なボイスルートの名前と、そのルートにポリシーを接続する PSTN 使用の名前を報告します。</span><span class="sxs-lookup"><span data-stu-id="2e239-124">If the verification run by Test-CsVoicePolicy succeeds, the cmdlet will report back the name of the first valid voice route it finds, and also the name of the PSTN usage that connects the policy to the route.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="2e239-125">テストの実行</span><span class="sxs-lookup"><span data-stu-id="2e239-125">Running the test</span></span>

<span data-ttu-id="2e239-126">Test-CsVoicePolicy コマンドレットを実行するには、最初に Get-CsVoicePolicy コマンドレットを使用して、テストする音声ポリシーのインスタンスを取得する必要があります。その後、そのインスタンスを CsVoicePolicy にパイプする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e239-126">To run the Test-CsVoicePolicy cmdlet you must first use the Get-CsVoicePolicy cmdlet retrieve an instance of the voice policy to be tested; that instance must then be piped to Test-CsVoicePolicy.</span></span> <span data-ttu-id="2e239-127">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2e239-127">For example:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="2e239-128">このコマンドは、音声ポリシーのインスタンスを取得するために Get-CsVoicePolicy を使用しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e239-128">Note that this command, which does not use Get-CsVoicePolicy to retrieve a voice policy instance, will fail:</span></span>

`Test-CsVoicePolicy -TargetNumber "+12065551219" -VoicePolicy "Global"`

<span data-ttu-id="2e239-129">すべての音声ポリシーを指定の電話番号に対して確認する場合は、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e239-129">If you want to check all the voice policies against a specified phone number then use a command similar to this:</span></span>

`Get-CsVoicePolicy | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="2e239-130">TargetNumber は、E.i 形式で指定する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e239-130">Note that the TargetNumber must be specified by using the E.164 format.</span></span> <span data-ttu-id="2e239-131">Test-CsVoicePolicy は、電話番号を E-164 形式で正規化または翻訳しようとしません。</span><span class="sxs-lookup"><span data-stu-id="2e239-131">Test-CsVoicePolicy won't attempt to normalize or translate phone numbers into the E.164 format.</span></span>

<span data-ttu-id="2e239-132">詳細については、Test-CsVoicePolicy コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e239-132">For more information, see the Help documentation for the Test-CsVoicePolicy cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="2e239-133">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="2e239-133">Determining success or failure</span></span>

<span data-ttu-id="2e239-134">ボイスポリシーが一致する音声ルートと、一致する PSTN 使用の両方を見つけることができる場合は、ルートと利用状況の両方が画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e239-134">If the voice policy can find both a matching voice route and a matching PSTN usage, then both the route and the usage will be displayed on-screen:</span></span>

<span data-ttu-id="2e239-135">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="2e239-135">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="2e239-136">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="2e239-136">\------------------ -------------</span></span>

<span data-ttu-id="2e239-137">RedmondVoiceRoute RedmondPstnUsage</span><span class="sxs-lookup"><span data-stu-id="2e239-137">RedmondVoiceRoute RedmondPstnUsage</span></span>

<span data-ttu-id="2e239-138">適切な音声ルートまたは適切な PSTN 使用が見つからない場合は、空白のプロパティ値が画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e239-138">If either an appropriate voice route or an appropriate PSTN usage cannot be found then blank property values will be displayed on-screen:</span></span>

<span data-ttu-id="2e239-139">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="2e239-139">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="2e239-140">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="2e239-140">\------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="2e239-141">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="2e239-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="2e239-142">ボイスポリシーがボイスルートで PSTN 使用状況を共有していない可能性があるという意味で Test-CsVoicePolicy が返されない場合。</span><span class="sxs-lookup"><span data-stu-id="2e239-142">If Test-CsVoicePolicy does not return a match that could mean that the voice policy does not share a PSTN usage with a voice route.</span></span> <span data-ttu-id="2e239-143">これを確認するには、次のようなコマンドレットを使用して、ボイスポリシーに割り当てられている PSTN の使用状況を確認します。</span><span class="sxs-lookup"><span data-stu-id="2e239-143">To verify that, use a cmdlet similar to the following to verify that PSTN usages assigned to the voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Select-Object PstnUsages | Format-List`

<span data-ttu-id="2e239-144">次に、このコマンドを実行して、PSTN 使用状況が各ボイスルートに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e239-144">Next, run this command to determine the PSTN usages assign to each of your voice routes:</span></span>

`Get-CsVoiceRoute | Select-Object Identity, PstnUsages`

<span data-ttu-id="2e239-145">一致するものが見つかった場合 (つまり、音声ポリシーで1つ以上の PSTN 使用状況を共有する1つ以上の音声ルートが表示されている場合) は、Test-CsVoiceRoute コマンドレットを実行して、ボイスルートが指定された電話番号をダイヤルできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e239-145">If you see any matches (that is, if you see one or more voice routes that share at least one PSTN usage with your voice policy), you should then run the Test-CsVoiceRoute cmdlet to verify that the voice route can dial the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2e239-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e239-146">See Also</span></span>


[<span data-ttu-id="2e239-147">テスト-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="2e239-147">Test-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoicePolicy)  
  

<span data-ttu-id="2e239-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e239-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

