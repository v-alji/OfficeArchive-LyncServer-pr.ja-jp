---
title: 'Lync Server 2013: PSTN 電話の通話ルーティングのテスト'
description: 'Lync Server 2013: PSTN 電話による通話のルーティングをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440991"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a><span data-ttu-id="6f621-103">Lync Server 2013 での PSTN 電話による通話ルーティングのテスト</span><span class="sxs-lookup"><span data-stu-id="6f621-103">Testing PSTN phone call routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f621-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f621-104">

<span> </span></span></span>

<span data-ttu-id="6f621-105">_**最終更新日:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="6f621-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f621-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="6f621-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="6f621-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="6f621-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f621-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="6f621-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="6f621-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f621-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f621-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="6f621-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="6f621-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f621-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="6f621-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、 <strong>CsInterTrunkRouting</strong> コマンドレットを実行するためのアクセス許可が与えられている RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f621-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsInterTrunkRouting</strong> cmdlet.</span></span> <span data-ttu-id="6f621-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6f621-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="6f621-114">説明</span><span class="sxs-lookup"><span data-stu-id="6f621-114">Description</span></span>

<span data-ttu-id="6f621-115">**CsInterTrunkRouting** コマンドレットは、通話がある SIP から別の SIP にルーティングできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f621-115">The **Test-CsInterTrunkRouting** cmdlet verifies that calls can be routed from one SIP to another.</span></span> <span data-ttu-id="6f621-116">これを行うには、コマンドレットに電話番号とトランク構成を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f621-116">To do this, the cmdlet is given a phone number and a trunk configuration.</span></span> <span data-ttu-id="6f621-117">**CsInterTrunkRouting** は、指定された番号について、一致するルートと一致する PSTN の使用状況を報告します。</span><span class="sxs-lookup"><span data-stu-id="6f621-117">**Test-CsInterTrunkRouting** will then report back matching routes and matching PSTN usages for the specified number.</span></span> <span data-ttu-id="6f621-118">Trunks には、指定した電話番号と一致する番号パターンがあり、trunks が少なくとも1つの PSTN 使用を共有している場合のみ、trunks 間で通話をルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="6f621-118">Note that calls can be routed between trunks only if the trunks have a number pattern that matches the specified phone number and only if the trunks share at least one PSTN usage.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="6f621-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="6f621-119">Running the test</span></span>

<span data-ttu-id="6f621-120">次に示すコマンドは、ユーザーが Redmond サイトのトランク構成設定を使用して電話番号1-206-555-1219 に発信できるように、一致するルートと一致する電話の使用状況を返します。</span><span class="sxs-lookup"><span data-stu-id="6f621-120">The commands shown below return the matching routes and matching phone usages that enable users to call the phone number 1-206-555-1219 using the trunk configuration settings for the Redmond site.</span></span>

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="6f621-121">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="6f621-121">Determining success or failure</span></span>

<span data-ttu-id="6f621-122">通話を別の SIP にルーティングできる場合は、次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f621-122">If calls can be routed from one SIP to another, you'll receive output similar to this:</span></span>

<span data-ttu-id="6f621-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span><span class="sxs-lookup"><span data-stu-id="6f621-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span></span>

<span data-ttu-id="6f621-124">\------------------ ------------- --------------</span><span class="sxs-lookup"><span data-stu-id="6f621-124">\------------------ ------------- --------------</span></span>

<span data-ttu-id="6f621-125">RedmondRoute LocalUsage {RedmondRoute}</span><span class="sxs-lookup"><span data-stu-id="6f621-125">RedmondRoute LocalUsage {RedmondRoute}</span></span>

<span data-ttu-id="6f621-126">テストが成功しなかった場合は、次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f621-126">If the test did not succeed, you'll receive output similar to this:</span></span>

<span data-ttu-id="6f621-127">Test-CsInterTrunkRouting: パラメーターで引数の変換を処理できない</span><span class="sxs-lookup"><span data-stu-id="6f621-127">Test-CsInterTrunkRouting : Cannot process argument transformation on parameter</span></span>

<span data-ttu-id="6f621-128">'TrunkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="6f621-128">'TrunkConfiguration'.</span></span> <span data-ttu-id="6f621-129">TrunkConfigurationsetting (パラメーター) が無効です。</span><span class="sxs-lookup"><span data-stu-id="6f621-129">Invalid TrunkConfigurationsetting (parameter).</span></span> <span data-ttu-id="6f621-130">を指定する</span><span class="sxs-lookup"><span data-stu-id="6f621-130">Specify a</span></span>

<span data-ttu-id="6f621-131">有効な設定 (パラメーター) を入力してからやり直してください。</span><span class="sxs-lookup"><span data-stu-id="6f621-131">valid setting (parameter) and then try again.</span></span>

<span data-ttu-id="6f621-132">行: 1 char:79</span><span class="sxs-lookup"><span data-stu-id="6f621-132">At line:1 char:79</span></span>

<span data-ttu-id="6f621-133">\+ Test-CsInterTrunkRouting-TargetNumber "tel: + 12065551219"</span><span class="sxs-lookup"><span data-stu-id="6f621-133">\+ Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219"</span></span>

<span data-ttu-id="6f621-134">\-TrunkConfiguration $t...</span><span class="sxs-lookup"><span data-stu-id="6f621-134">\-TrunkConfiguration $t ...</span></span>

\+

~~

<span data-ttu-id="6f621-135">\+ カテゴリ情報: InvalidData: (:) \[CsInterTrunkRouting \] 、Par</span><span class="sxs-lookup"><span data-stu-id="6f621-135">\+ CategoryInfo : InvalidData: (:) \[Test-CsInterTrunkRouting\], Par</span></span>

<span data-ttu-id="6f621-136">Ameterbindingargumentの例外</span><span class="sxs-lookup"><span data-stu-id="6f621-136">ameterBindingArgumentTransformationException</span></span>

<span data-ttu-id="6f621-137">\+ FullyQualifiedErrorId: Parameterargumentトランスエラー、Microsoft R</span><span class="sxs-lookup"><span data-stu-id="6f621-137">\+ FullyQualifiedErrorId : ParameterArgumentTransformationError,Microsoft.R</span></span>

<span data-ttu-id="6f621-138">tc.TestOcsInterTrunkRoutingCmdlet を管理します。</span><span class="sxs-lookup"><span data-stu-id="6f621-138">tc.Management.Voice.Cmdlets.TestOcsInterTrunkRoutingCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="6f621-139">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="6f621-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="6f621-140">次に **、テスト-CsInterTrunkRouting** が失敗する可能性がある一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="6f621-140">Here are some common reasons why **Test-CsInterTrunkRouting** might fail:</span></span>

  - <span data-ttu-id="6f621-141">無効なパラメーターが指定されました。</span><span class="sxs-lookup"><span data-stu-id="6f621-141">You specified invalid parameters.</span></span> <span data-ttu-id="6f621-142">トランクがまだ正しく構成されておらず、指定されたターゲット番号が間違っているか、無効である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6f621-142">The trunk might not yet be correctly configured and the specified target number might be incorrect or invalid.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f621-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f621-143">See Also</span></span>


[<span data-ttu-id="6f621-144">Get-CsTrunk</span><span class="sxs-lookup"><span data-stu-id="6f621-144">Get-CsTrunk</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[<span data-ttu-id="6f621-145">Get-Set-cstrunkconfiguration</span><span class="sxs-lookup"><span data-stu-id="6f621-145">Get-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

<span data-ttu-id="6f621-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f621-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

