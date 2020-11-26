---
title: マスター番地の住所ガイドに照らして都市の住所をテストする
description: マスター番地の住所ガイドに照らして、都市の住所をテストします。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439829"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a><span data-ttu-id="eda89-103">Lync Server 2013 の主要住所ガイドに照らして、都市の住所をテストする</span><span class="sxs-lookup"><span data-stu-id="eda89-103">Testing civic addresses against the master street address guide in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eda89-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eda89-104">

<span> </span></span></span>

<span data-ttu-id="eda89-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="eda89-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eda89-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="eda89-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="eda89-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="eda89-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda89-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="eda89-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="eda89-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="eda89-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda89-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="eda89-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="eda89-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="eda89-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="eda89-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsRegistration コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eda89-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="eda89-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="eda89-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="eda89-114">説明</span><span class="sxs-lookup"><span data-stu-id="eda89-114">Description</span></span>

<span data-ttu-id="eda89-115">Test-CsLisCivicAddress コマンドレットを使用して、位置情報サービス (LIS) データベースに追加された場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="eda89-115">The Test-CsLisCivicAddress cmdlet is used to verify locations that were added to your Location Information service (LIS) database.</span></span> <span data-ttu-id="eda89-116">このコマンドレットを実行するには、E9 のネットワークルーティングプロバイダーに属している主要な住所ガイド (MSAG) で見つかった場所を比較します。</span><span class="sxs-lookup"><span data-stu-id="eda89-116">The cmdlet works by comparing locations against the locations found in the Master Street Address Guide (MSAG) that belongs to your E9-1-1 Network Routing Provider.</span></span> <span data-ttu-id="eda89-117">ネットワークルーティングプロバイダーを持っていない場合、またはプロバイダーに接続できない場合、テストは失敗します。</span><span class="sxs-lookup"><span data-stu-id="eda89-117">If you do not have a network routing provider or if the provider cannot be reached, then your tests will fail.</span></span>

<span data-ttu-id="eda89-118">コマンドにオプションのスイッチパラメーター UpdateValidationStatus を追加した場合、テストを渡す各アドレスについて、対応する MSAGValid な database プロパティが True に設定されます。</span><span class="sxs-lookup"><span data-stu-id="eda89-118">If you add the optional switch parameter UpdateValidationStatus to your command, then the corresponding MSAGValid database property will be set to True for each address passing the test.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="eda89-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="eda89-119">Running the test</span></span>

<span data-ttu-id="eda89-120">Test-CsLisCivicAddress コマンドレットを使用して、個々のアドレスのテストや複数のアドレスのテストを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="eda89-120">The Test-CsLisCivicAddress cmdlet can be used to test individual addresses or to test multiple addresses.</span></span> <span data-ttu-id="eda89-121">たとえば、このコマンドは、Redmond、WA にある1つのアドレスをテストします。</span><span class="sxs-lookup"><span data-stu-id="eda89-121">For example, this command tests a single address located in Redmond, WA:</span></span>

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

<span data-ttu-id="eda89-122">このコマンドでは、現在の LIS データベースにあるすべてのアドレスがテストされます。</span><span class="sxs-lookup"><span data-stu-id="eda89-122">By comparison, this command tests all the addresses currently in your LIS database:</span></span>

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

<span data-ttu-id="eda89-123">詳細については、「 [CsRegistration のテスト](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) 」コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eda89-123">For more information, see the Help documentation for the [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="eda89-124">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="eda89-124">Determining success or failure</span></span>

<span data-ttu-id="eda89-125">Test-CsLisCivicAddress は、指定されたアドレスのバックが成功したか失敗したかを報告します。</span><span class="sxs-lookup"><span data-stu-id="eda89-125">Test-CsLisCivicAddress will report back Success or Failure for the supplied addresses.</span></span> <span data-ttu-id="eda89-126">アドレスが見つからない場合、またはサービスプロバイダに接続できない場合、住所テストは失敗します。</span><span class="sxs-lookup"><span data-stu-id="eda89-126">An address test will fail if the address cannot be found or if the service provider cannot be contacted.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="eda89-127">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="eda89-127">Reasons why the test might have failed</span></span>

<span data-ttu-id="eda89-128">Test-CsLisCivicAddress が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="eda89-128">Here are some common reasons why Test-CsLisCivicAddress might fail:</span></span>

  - <span data-ttu-id="eda89-129">LIS サービスプロバイダーが利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eda89-129">The LIS service provider might not be available.</span></span> <span data-ttu-id="eda89-130">Get-CsLisConfiguration コマンドレットを実行して、LIS サービスプロバイダーの URL を取得できます。</span><span class="sxs-lookup"><span data-stu-id="eda89-130">You can retrieve the URL of your LIS service provider by running the Get-CsLisConfiguration cmdlet:</span></span>
    
        Get-CsLisConfiguration 
    
    <span data-ttu-id="eda89-131">その URL に ping して、サービスプロバイダが利用可能であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="eda89-131">You can then ping that URL to verify that the service provider is available.</span></span>

<span data-ttu-id="eda89-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eda89-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

