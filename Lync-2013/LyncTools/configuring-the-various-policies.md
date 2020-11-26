---
title: 各種ポリシーの構成
description: さまざまなポリシーを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440062"
---
# <a name="configuring-the-various-policies"></a><span data-ttu-id="82769-103">各種ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="82769-103">Configuring the Various Policies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82769-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82769-104">

<span> </span></span></span>

<span data-ttu-id="82769-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="82769-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

<span data-ttu-id="82769-106">Lync Server 2013 のストレスとパフォーマンスツールを実行する前に、Lync Server 2013 トポロジで構成できる各種のポリシーを次に示します。</span><span class="sxs-lookup"><span data-stu-id="82769-106">Here are the various policies that you can configure in your Lync Server 2013 topology, prior to running the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="configuring-the-archiving-policy"></a><span data-ttu-id="82769-107">アーカイブポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-107">Configuring the Archiving Policy</span></span>

<span data-ttu-id="82769-108">「スクリプトの例 ArchivingPolicy.ps1 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-108">See the example script ArchivingPolicy.ps1.</span></span> <span data-ttu-id="82769-109">このスクリプトは、アーカイブサーバーがトポロジに展開されている場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82769-109">You need to use this script only if an Archiving Server is deployed in your topology.</span></span> <span data-ttu-id="82769-110">詳細については、「lync Server 2013 のドキュメントとコマンドレットのヘルプ」を参照してください。 [lync server 2013 のコマンドレットのアーカイブと監視](https://technet.microsoft.com/library/gg415629\(v=ocs.15\))を行います。</span><span class="sxs-lookup"><span data-stu-id="82769-110">For details, see the Lync Server 2013 documentation and cmdlet Help for [Archiving and Monitoring cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a><span data-ttu-id="82769-111">会議ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-111">Configuring the Conferencing Policy</span></span>

<span data-ttu-id="82769-112">「スクリプトの例 MeetingPolicy.ps1 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-112">See the example script MeetingPolicy.ps1.</span></span> <span data-ttu-id="82769-113">詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 の Web 会議コマンド](https://technet.microsoft.com/library/gg415675\(v=ocs.15\))レットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-113">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-contacts-policy"></a><span data-ttu-id="82769-114">連絡先ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-114">Configuring the Contacts Policy</span></span>

<span data-ttu-id="82769-115">ContactsPolicy.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-115">See the example ContactsPolicy.ps1.</span></span> <span data-ttu-id="82769-116">詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 の IM とプレゼンスのコマンド](https://technet.microsoft.com/library/gg398611\(v=ocs.15\))レットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-116">For details, see the Lync Server 2013 documentation and the cmdlet Help for [IM and presence cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-federation-policy"></a><span data-ttu-id="82769-117">フェデレーションポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-117">Configuring the Federation Policy</span></span>

<span data-ttu-id="82769-118">FederationPolicy.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-118">See the example FederationPolicy.ps1.</span></span> <span data-ttu-id="82769-119">詳細については、「lync server 2013 ドキュメント」および「lync server 2013 での microsoft Lync Server 2013 および[フェデレーションと外部アクセスコマンド](https://technet.microsoft.com/library/gg415651\(v=ocs.15\))レットの[Edge server コマンド](https://technet.microsoft.com/library/gg415635\(v=ocs.15\))レットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-119">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Edge Server cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) and [Federation and external access cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a><span data-ttu-id="82769-120">通話受付制御ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-120">Configuring the Call Admission Control Policy</span></span>

<span data-ttu-id="82769-121">BandwidthPolicy.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-121">See the example BandwidthPolicy.ps1.</span></span> <span data-ttu-id="82769-122">詳細については、lync server 2013 の「 [通話受付制御](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) 」と「lync server [2013 での通話受付制御コマンド](https://technet.microsoft.com/library/gg415676\(v=ocs.15\))レットのヘルプ」を参照し2013てください。</span><span class="sxs-lookup"><span data-stu-id="82769-122">For details, see the Lync Server 2013 documentation [Overview of call admission control in Lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) and the cmdlet Help for [Call admission control cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a><span data-ttu-id="82769-123">ボイスルーティングルールを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-123">Configuring the Voice Routing Rules</span></span>

<span data-ttu-id="82769-124">RoutingRules.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-124">See the example RoutingRules.ps1.</span></span> <span data-ttu-id="82769-125">ボイスルーティングルールを構成するときは、電話のコンテキスト (¥ Location Profile または/simplename) と内部/外部の市外局番 (特に PSTN-UC および UC-PSTN 用) を指定して、ユーザーを作成するときに指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="82769-125">When you configure the voice routing rules, take note of the Phone Context (that is, /Location Profile or /SimpleName) and Internal/External Area Codes so that you can specify them when creating users and during LyncPerfTool configuration (specifically for PSTN-UC and UC-PSTN).</span></span> <span data-ttu-id="82769-126">たとえば、RoutingRules.ps1 の例の **CsDialPlan** コマンドレットへの呼び出しの simplename パラメーターは、次の UserProfileGenerator.exe の図の locationprofile 値として使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82769-126">For example, the SimpleName parameter in the call to the **New-CsDialPlan** cmdlet in the RoutingRules.ps1 example should be used for the LocationProfile value in the following figure of UserProfileGenerator.exe.</span></span>

<span data-ttu-id="82769-127">![サンプルの音声のルーティング ルール](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "サンプルの音声のルーティング ルール")</span><span class="sxs-lookup"><span data-stu-id="82769-127">![Sample voice routing rule.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Sample voice routing rule.")</span></span>

<span data-ttu-id="82769-128">詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 のエンタープライズボイスコマンド](https://technet.microsoft.com/library/gg415658\(v=ocs.15\))レットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-128">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Enterprise Voice cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a><span data-ttu-id="82769-129">会議アテンダントアプリケーションの構成</span><span class="sxs-lookup"><span data-stu-id="82769-129">Configuring Conferencing Attendant application</span></span>

<span data-ttu-id="82769-130">ConferenceAutoAttendantConfiguration.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-130">See the example ConferenceAutoAttendantConfiguration.ps1.</span></span> <span data-ttu-id="82769-131">ConferencingAutoAttendant 電話番号 (既定では 1121111111) をメモし、それを構成の生成用の LyncPerf ツール構成ツールに入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="82769-131">Take note of the ConferencingAutoAttendant phone number (1121111111, by default), so that you can type it into the LyncPerf Tool Configuration tool for configuration generation.</span></span>

<span data-ttu-id="82769-132">![会議アテンダント アプリケーションを構成する](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "会議アテンダント アプリケーションを構成する")</span><span class="sxs-lookup"><span data-stu-id="82769-132">![Configuring the Conferencing Attendant application](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configuring the Conferencing Attendant application")</span></span>

<span data-ttu-id="82769-133">詳細については、「lync server 2013 ドキュメント」および「lync server 2013 での [Web 会議コマンド](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) レットのヘルプ (lync server 2013 および [ダイヤルイン会議コマンド](https://technet.microsoft.com/library/gg415630\(v=ocs.15\))レットのヘルプ)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-133">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) and [Dial-in conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a><span data-ttu-id="82769-134">Lync Server コールパークサービスの構成</span><span class="sxs-lookup"><span data-stu-id="82769-134">Configuring Lync Server Call Park Service</span></span>

<span data-ttu-id="82769-135">コールパークは既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="82769-135">Call Park is disabled by default.</span></span> <span data-ttu-id="82769-136">CallParkConfiguration.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-136">See the example CallParkConfiguration.ps1.</span></span> <span data-ttu-id="82769-137">詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 のコールパークアプリケーションコマンドレット](https://technet.microsoft.com/library/gg415639\(v=ocs.15\))のヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-137">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Call Park application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-emergency-calls"></a><span data-ttu-id="82769-138">緊急通話の設定</span><span class="sxs-lookup"><span data-stu-id="82769-138">Configuring Emergency Calls</span></span>

<span data-ttu-id="82769-139">緊急通話のストレスとパフォーマンスのテストを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="82769-139">Perform the following steps to configure stress and performance testing for emergency calls.</span></span>

1.  <span data-ttu-id="82769-140">緊急通話のためのボイスルートを設定します。</span><span class="sxs-lookup"><span data-stu-id="82769-140">Set up a voice route for emergency calls.</span></span> <span data-ttu-id="82769-141">このボイスルートを設定する例については、「E911 にルーティングする」の説明を参照し RoutingRules.ps1 てください。</span><span class="sxs-lookup"><span data-stu-id="82769-141">See the RoutingRules.ps1 script under the comment "Route E911 to PSTN" for an example of setting up this voice route.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="82769-142">RoutingRules.ps1 のコマンドの例では、911ではなく数値119を含む数値パターンを使用しています。</span><span class="sxs-lookup"><span data-stu-id="82769-142">The example command in RoutingRules.ps1 has a number pattern that includes the number 119 rather than 911.</span></span> <span data-ttu-id="82769-143">ロードテスト中に、ローカルの緊急電話会社に誤って通話を発信しないようにするには、911 (または実際のローカル緊急電話番号) の使用を避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="82769-143">You should avoid using 911 (or your actual local emergency number) to prevent accidental calls to your local emergency operators during load testing.</span></span> <span data-ttu-id="82769-144">この構成は、シミュレーション目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="82769-144">This configuration is for simulation purposes only.</span></span>

    
    </div>

2.  <span data-ttu-id="82769-145">次の図に示すように、Userプロビジョニングツールの [ **LIS** ] タブの値を入力して、アドレスを構成します。</span><span class="sxs-lookup"><span data-stu-id="82769-145">Configure addresses by filling in the values on the **LIS** tab in the UserProvisioningTool, as shown in the following figure.</span></span>
    
    <span data-ttu-id="82769-146">![場所情報サービスの構成](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "場所情報サービスの構成")</span><span class="sxs-lookup"><span data-stu-id="82769-146">![Configuring the Location Information Service.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configuring the Location Information Service.")</span></span>  

3.  <span data-ttu-id="82769-147">[ **LIS 構成ファイルの生成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82769-147">Click **Generate LIS Config Files**.</span></span>

4.  <span data-ttu-id="82769-148">ポート、サブネット、スイッチ、ワイヤレスアクセスポイント (Wap) の CSV ファイル、および Lync Server 2013 ストレスおよびパフォーマンスツール用の XML ファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="82769-148">CSV files for ports, subnets, switches, and wireless access points (WAPs), and an XML file for the Lync Server 2013 Stress and Performance Tool, are generated.</span></span> <span data-ttu-id="82769-149">CSV ファイルは、LisConfiguration.ps1 スクリプトで場所情報サービス (LIS) を構成するときに、(同じフォルダー内の) 入力として使用されます。</span><span class="sxs-lookup"><span data-stu-id="82769-149">The CSV files are to be used as inputs (in the same folder) when configuring Location Information service (LIS) with the LisConfiguration.ps1 script.</span></span> <span data-ttu-id="82769-150">生成された Locations0.xml ファイルを、Lync Server 2013 のストレスとパフォーマンスツールの実行可能ファイル (LyncPerfTool.exe) と同じフォルダーに移動すると、位置情報プロファイル (ダイヤルプラン) のシナリオが実行されます。</span><span class="sxs-lookup"><span data-stu-id="82769-150">Move the generated Locations0.xml file to the same folder as the Lync Server 2013 Stress and Performance Tool executable (LyncPerfTool.exe), which will run location profile (dial plan) scenarios.</span></span>

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a><span data-ttu-id="82769-151">ユーザーの作成、有効化、構成、無効化</span><span class="sxs-lookup"><span data-stu-id="82769-151">Creating, Enabling, Configuring and Disabling Users</span></span>

<span data-ttu-id="82769-152">次のスクリプトを実行する前に、すべてのユーザーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82769-152">You should create all your users before running the following scripts.</span></span> <span data-ttu-id="82769-153">「ユーザー [と連絡先を作成して](create-users-and-contacts.md) ユーザーを作成する」の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="82769-153">Follow the instructions in [Create Users and Contacts](create-users-and-contacts.md) to create users.</span></span> <span data-ttu-id="82769-154">詳細については、「 [ユーザー](https://technet.microsoft.com/library/gg398125\(v=ocs.15\))用の Lync Server 2013 コマンドレット」を参照してください。また、「ユーザーの [設定](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))」を [参照して](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) ください。</span><span class="sxs-lookup"><span data-stu-id="82769-154">For details, see the Lync Server 2013 cmdlet documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [Set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\)), and [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) cmdlets.</span></span>

</div>

<div>

## <a name="configuring-response-group-application"></a><span data-ttu-id="82769-155">応答グループアプリケーションを構成する</span><span class="sxs-lookup"><span data-stu-id="82769-155">Configuring Response Group application</span></span>

<span data-ttu-id="82769-156">ResponseGroupConfiguration.ps1 の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82769-156">See the example ResponseGroupConfiguration.ps1.</span></span> <span data-ttu-id="82769-157">詳細については、「Lync Server 2013 ドキュメント」および「 [lync server 2013 のグループアプリケーションコマンドレットに応答](https://technet.microsoft.com/library/gg415654\(v=ocs.15\))するためのコマンドレットのヘルプ」を参照してください。応答グループのアプリケーション構成を確認するには、次の図のように「」を参照し `https://<poolfqdn>/RgsConfig/` てください。</span><span class="sxs-lookup"><span data-stu-id="82769-157">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Response Group application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)).To review the Response Group application configuration, see `https://<poolfqdn>/RgsConfig/`, as shown in the following figure.</span></span>

<span data-ttu-id="82769-158">![応答グループ構成ツール](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "応答グループ構成ツール")</span><span class="sxs-lookup"><span data-stu-id="82769-158">![The Response Group Configuration Tool.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "The Response Group Configuration Tool.")</span></span>

<span data-ttu-id="82769-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82769-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

