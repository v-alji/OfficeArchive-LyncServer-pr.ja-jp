---
title: ウォッチャーノードのテストユーザーと構成設定を構成する
description: ウォッチャーノードのテストユーザーと構成設定を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring watcher node test users and configuration settings
ms:assetid: ab00e9cb-f539-4aa6-bcb4-5533fbe7bc44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205152(v=OCS.15)
ms:contentKeyID: 48185048
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e39a35d3db6ed80c715c706f4b5766e4b684e39e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432332"
---
# <a name="configuring-watcher-node-test-users-and-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="e026a-103">Lync Server 2013 で監視ノードのテストユーザーと構成設定を構成する</span><span class="sxs-lookup"><span data-stu-id="e026a-103">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e026a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e026a-104">

<span> </span></span></span>

<span data-ttu-id="e026a-105">_**最終更新日:** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="e026a-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="e026a-106">監視ノードとして動作するコンピューターを構成したら、次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-106">After configuring the computer that will act as a watcher node, you must:</span></span>

1.  <span data-ttu-id="e026a-107">これらのウォッチャーノードで使用するテストアカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="e026a-107">Create the test accounts to be used by these watcher nodes.</span></span> <span data-ttu-id="e026a-108">Negotiate の認証方法を使用している場合は、[Set-CsTestUserCredential](https://technet.microsoft.com/library/JJ205341(v=OCS.15)) コマンドレットを使用し、監視ノードで使用するためにこれらのテスト アカウントを有効にする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="e026a-108">If you are using the Negotiate authentication method, you must also use the [Set-CsTestUserCredential](https://technet.microsoft.com/library/JJ205341(v=OCS.15)) cmdlet to enable these test accounts for use on the watcher node.</span></span>

2.  <span data-ttu-id="e026a-109">監視ノード構成設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="e026a-109">Update the watcher node configuration settings.</span></span>

<span data-ttu-id="e026a-110">このセクションの内容:</span><span class="sxs-lookup"><span data-stu-id="e026a-110">This section covers:</span></span>

  - <span data-ttu-id="e026a-111">テストユーザーアカウントを構成する</span><span class="sxs-lookup"><span data-stu-id="e026a-111">Configuring Test User Accounts</span></span>

  - <span data-ttu-id="e026a-112">既定の代理トランザクションを使った基本的なウォッチャーノードの構成</span><span class="sxs-lookup"><span data-stu-id="e026a-112">Configuring a Basic Watcher Node with the Default Synthetic Transactions</span></span>

  - <span data-ttu-id="e026a-113">拡張テストの構成</span><span class="sxs-lookup"><span data-stu-id="e026a-113">Configuring Extended Tests</span></span>

  - <span data-ttu-id="e026a-114">代理トランザクションの追加と削除</span><span class="sxs-lookup"><span data-stu-id="e026a-114">Adding and Removing Synthetic Transactions</span></span>

  - <span data-ttu-id="e026a-115">監視ノード構成の表示とテスト</span><span class="sxs-lookup"><span data-stu-id="e026a-115">Viewing and Testing the Watcher Node Configuration</span></span>

<div>

## <a name="configuring-test-user-accounts"></a><span data-ttu-id="e026a-116">テストユーザーアカウントを構成する</span><span class="sxs-lookup"><span data-stu-id="e026a-116">Configuring Test User Accounts</span></span>

<span data-ttu-id="e026a-117">テストユーザーは、実際のユーザーを表す必要はありませんが、有効な Active Directory ドメインサービスアカウントである必要があります。さらに、これらのアカウントは Lync Server 2013 で有効にしておく必要があります。また、有効な SIP アドレスがある必要があります。また、エンタープライズ Voip を有効にする必要があります (Test-CsPstnPeerToPeerCall 代理トランザクションを使用する場合)。</span><span class="sxs-lookup"><span data-stu-id="e026a-117">Test users do not need to represent actual people, but they must be valid Active Directory Domain Services accounts; in addition, these accounts must be enabled for Lync Server 2013, they must have valid SIP addresses, and they should be enabled for Enterprise Voice (to use the Test-CsPstnPeerToPeerCall synthetic transaction).</span></span> <span data-ttu-id="e026a-118">TrustedServer 認証方法を使用する場合は、これらのアカウントが存在し、ここで指定したように構成されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-118">If you use the TrustedServer authentication method, then all you need to do is to make sure that these accounts exist and have been configured as specified here.</span></span> <span data-ttu-id="e026a-119">テストしようとする各プールに対して、少なくとも 3 つのテスト ユーザーを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-119">You should assign at least three test users for each pool that you want to test.</span></span>

<span data-ttu-id="e026a-120">Negotiate 認証方法を使用している場合は、 **CsTestUserCredential** コマンドレットと Lync Server Management Shell を使って、これらのテストアカウントで代理トランザクションを操作できるようにする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="e026a-120">If you are using the Negotiate authentication method, you must also use the **Set-CsTestUserCredential** cmdlet and the Lync Server Management Shell to enable these test accounts to work with the synthetic transactions.</span></span> <span data-ttu-id="e026a-121">これを行うには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e026a-121">You can do this by running a command similar to the following.</span></span> <span data-ttu-id="e026a-122">(これらのコマンドは、3つの Active Directory ユーザーアカウントが既に作成されていて、それらのアカウントが Lync Server 2013 用に有効になっていることを前提としています)。</span><span class="sxs-lookup"><span data-stu-id="e026a-122">(These commands assume that the three Active Directory user accounts have already been created and that those accounts have been enabled for Lync Server 2013.):</span></span>

    Set-CsTestUserCredential -SipAddress "sip:watcher1@litwareinc.com" -UserName "litwareinc\watcher1" -Password "P@ssw0rd"
    Set-CsTestUserCredential -SipAddress "sip:watcher2@litwareinc.com" -UserName "litwareinc\watcher2" -Password "P@ssw0rd"
    Set-CsTestUserCredential -SipAddress "sip:watcher3@litwareinc.com" -UserName "litwareinc\watcher3" -Password "P@ssw0rd"

<span data-ttu-id="e026a-123">SIP アドレスだけでなく、ユーザー名とパスワードも含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e026a-123">Note that you must include not only the SIP address but also the user name and password.</span></span> <span data-ttu-id="e026a-124">パスワードが含まれていない場合は Set-CsTestUserCredential 情報を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="e026a-124">If you do not include the password Set-CsTestUserCredential will prompt you to enter that information.</span></span> <span data-ttu-id="e026a-125">ユーザー名は、上記のドメイン名の \\ ユーザー名形式を使用するか、または [ユーザー name@domain 名前の書式設定] を使用して指定できます。たとえば、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="e026a-125">The user name can be specified using the domain name\\user name format shown above, or by using the format user name@domain name; for example:</span></span>

    -UserName "watcher3@litwareinc.com"

<span data-ttu-id="e026a-126">テストユーザーの資格情報が作成されたことを確認するには、Lync Server 管理シェルで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e026a-126">To verify that the test user credentials were created, run these commands from within the Lync Server Management Shell:</span></span>

    Get-CsTestUserCredential -SipAddress "sip:watcher1@litwareinc.com"
    Get-CsTestUserCredential -SipAddress "sip:watcher2@litwareinc.com"
    Get-CsTestUserCredential -SipAddress "sip:watcher3@litwareinc.com"

<span data-ttu-id="e026a-127">このような情報は、ユーザーごとに返されます。</span><span class="sxs-lookup"><span data-stu-id="e026a-127">Information similar to this should be returned for each user:</span></span>

    UserName                        Password
    --------                        --------
    Litwareinc\watcher1              System.Security.SecureString

</div>

<div>

## <a name="configuring-a-basic-watcher-node-with-the-default-synthetic-transactions"></a><span data-ttu-id="e026a-128">既定の代理トランザクションを使った基本的なウォッチャーノードの構成</span><span class="sxs-lookup"><span data-stu-id="e026a-128">Configuring a Basic Watcher Node with the Default Synthetic Transactions</span></span>

<span data-ttu-id="e026a-129">テストユーザーが作成された後、次のようなコマンドを使用してウォッチャーノードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e026a-129">After the test users have been created you can then create a watcher node by using a command similar to this:</span></span>

    New-CsWatcherNodeConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -PortNumber 5061 -TestUsers @{Add= "sip:watcher1@litwareinc.com","sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"}

<span data-ttu-id="e026a-130">このコマンドでは、既定の設定を使用し、既定の代理トランザクションのセットを実行する新しい監視ノードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e026a-130">This command creates a new watcher node that uses the default settings and runs the default set of synthetic transactions.</span></span> <span data-ttu-id="e026a-131">新しい監視ノードでは、watcher1@litwareinc.com、watcher2@litwareinc.com、および watcher3@litwareinc.com のテスト ユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="e026a-131">The new watcher node also uses the test users watcher1@litwareinc.com, watcher2@litwareinc.com, and watcher3@litwareinc.com.</span></span> <span data-ttu-id="e026a-132">ウォッチャーノードが TrustedServer 認証を使用している場合、3つのテストアカウントは Active Directory と Lync Server で有効になっている有効なユーザーアカウントにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e026a-132">If the watcher node is using TrustedServer authentication, the three test accounts can be any valid user accounts enabled for Active Directory and Lync Server.</span></span> <span data-ttu-id="e026a-133">ウォッチャーノードが Negotiate 認証方法を使用している場合は、 **CsTestUserCredential** コマンドレットを使用して、ウォッチャーノードに対してもこれらのユーザーアカウントを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-133">If the watcher node is using the Negotiate authentication method, you must also enable these user accounts for watcher node by using the **Set-CsTestUserCredential** cmdlet.</span></span>

</div>

<div>

## <a name="configuring-extended-tests"></a><span data-ttu-id="e026a-134">拡張テストの構成</span><span class="sxs-lookup"><span data-stu-id="e026a-134">Configuring Extended Tests</span></span>

<span data-ttu-id="e026a-135">公衆交換電話網 (PSTN テスト) を有効にして、公衆交換電話網との接続を確認する場合は、ウォッチャーノードを設定するときに追加の構成を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-135">If you want to enable the public switched telephone network (PSTN test), which verifies connectivity with the public switched telephone network, you will need to do some additional configuration when setting up the watcher node.</span></span> <span data-ttu-id="e026a-136">最初に、テストユーザーに PSTN テストの種類を関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-136">First, you need to associate your test users with the PSTN test type.</span></span> <span data-ttu-id="e026a-137">そのためには、Lync Server 管理シェルで次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e026a-137">To do that, run a command similar to this from within the Lync Server Management Shell:</span></span>

    $pstnTest = New-CsExtendedTest -TestUsers "sip:watcher1@litwareinc.com", "sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"  -Name "Contoso Provider Test" -TestType PSTN

<span data-ttu-id="e026a-138">このコマンドの結果は、変数に格納する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e026a-138">Note that the results of this command must be stored in a variable.</span></span> <span data-ttu-id="e026a-139">この例では、$pstnTest という名前の変数です。</span><span class="sxs-lookup"><span data-stu-id="e026a-139">In this example, that's a variable named $pstnTest.</span></span>

<span data-ttu-id="e026a-140">この時点で、 **CsWatcherNodeConfiguration** コマンドレットを使用して、テストの種類 (可変 $pstnTest) を Lync Server 2013 プールに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e026a-140">At this point, you can use the **New-CsWatcherNodeConfiguration** cmdlet to associate the test type (stored in the variable $pstnTest) to a Lync Server 2013 pool.</span></span> <span data-ttu-id="e026a-141">たとえば、次のコマンドは、プール atl-cs-001.litwareinc.com の新しいウォッチャーノード構成を作成し、前に作成した3つのテストユーザーを追加して、PSTN テストタイプも追加します。</span><span class="sxs-lookup"><span data-stu-id="e026a-141">For example, the following command creates a new watcher node configuration for the pool atl-cs-001.litwareinc.com, adding the three test users that were created previously, and also adding the PSTN test type:</span></span>

    New-CsWatcherNodeConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -PortNumber 5061 -TestUsers @{Add= "sip:watcher1@litwareinc.com","sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"} -ExtendedTests @{Add=$pstnTest}

<span data-ttu-id="e026a-142">Communicator ノードコンピューターに Lync Server core ファイルと RTCLocal データベースをインストールしていない場合は、上記のコマンドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="e026a-142">Note that the preceding command will fail if you have not installed the Lync Server core files and the RTCLocal database on the watcher node computer.</span></span>

<span data-ttu-id="e026a-143">複数のボイスポリシーをテストするには、 **新しい-Csex・ Deddedtest** コマンドレットを使用して、各ポリシーの拡張テストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-143">To test multiple voice policies, you need to create an extended test for each policy by using the **New-CsExtendedTest** cmdlet.</span></span> <span data-ttu-id="e026a-144">このテストに割り当てられているユーザーは、目的の音声ポリシーで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-144">The users assigned to this test should be configured with the desired voice policies.</span></span> <span data-ttu-id="e026a-145">その後、次のようなコマンドを使用して、拡張テストを **新しい-CsWatcherNodeConfiguration** コマンドレットに渡します。</span><span class="sxs-lookup"><span data-stu-id="e026a-145">The extended tests are then passed to the **New-CsWatcherNodeConfiguration** cmdlet by using a command similar to the following:</span></span>

    -ExtendedTests @{Add=$pstnTest1,$pstnTest2,$pstnTest3}

<span data-ttu-id="e026a-146">[テスト] パラメーターを使用せずに New-CsWatcherNodeConfiguration を呼び出すと、新しいウォッチャーノードでは、既定の代理トランザクション (および指定された拡張合成トランザクション) のみが有効になります。</span><span class="sxs-lookup"><span data-stu-id="e026a-146">If New-CsWatcherNodeConfiguration is called without using the Tests parameter, that means that only the Default synthetic transactions (and the specified extended synthetic transaction) will be enabled for the new watcher node.</span></span> <span data-ttu-id="e026a-147">これは、ウォッチャーノードが次のコンポーネントをテストすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e026a-147">This means that the watcher node will test the following components:</span></span>

  - <span data-ttu-id="e026a-148">Registration</span><span class="sxs-lookup"><span data-stu-id="e026a-148">Registration</span></span>

  - <span data-ttu-id="e026a-149">IM</span><span class="sxs-lookup"><span data-stu-id="e026a-149">IM</span></span>

  - <span data-ttu-id="e026a-150">GroupIM</span><span class="sxs-lookup"><span data-stu-id="e026a-150">GroupIM</span></span>

  - <span data-ttu-id="e026a-151">P2PAV (ピアツーピアの音声/ビデオ セッション)</span><span class="sxs-lookup"><span data-stu-id="e026a-151">P2PAV (peer-to-peer audio/video sessions)</span></span>

  - <span data-ttu-id="e026a-152">AvConference (音声/会議)</span><span class="sxs-lookup"><span data-stu-id="e026a-152">AvConference (audio/conferencing)</span></span>

  - <span data-ttu-id="e026a-153">Presence</span><span class="sxs-lookup"><span data-stu-id="e026a-153">Presence</span></span>

  - <span data-ttu-id="e026a-154">ABS (アドレス帳サービス)</span><span class="sxs-lookup"><span data-stu-id="e026a-154">ABS (Address Book service)</span></span>

  - <span data-ttu-id="e026a-155">ABWQ (アドレス帳 Web サービス)</span><span class="sxs-lookup"><span data-stu-id="e026a-155">ABWQ (Address Book web service)</span></span>

  - <span data-ttu-id="e026a-156">PSTN (拡張テストとして指定された pstn ゲートウェイ通話)。</span><span class="sxs-lookup"><span data-stu-id="e026a-156">PSTN (PSTN gateway calls, specified as an extended test.</span></span> <span data-ttu-id="e026a-157">既定では、PSTN は無効になっています。</span><span class="sxs-lookup"><span data-stu-id="e026a-157">By default, PSTN is disabled.</span></span> <span data-ttu-id="e026a-158">この場合、テストは、コマンドによって ExtendedTests パラメーターを使って PSTN が有効になっている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="e026a-158">The test is enabled in this case only because the command enabled PSTN by using the ExtendedTests parameter.)</span></span>

<span data-ttu-id="e026a-159">これは、既定では次のコンポーネントがテストされないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="e026a-159">This also means that the following components will not be tested by default:</span></span>

  - <span data-ttu-id="e026a-160">AVEdgeConnectivity</span><span class="sxs-lookup"><span data-stu-id="e026a-160">AVEdgeConnectivity</span></span>

  - <span data-ttu-id="e026a-161">MCXP2PIM (モバイル デバイス インスタント メッセージング)</span><span class="sxs-lookup"><span data-stu-id="e026a-161">MCXP2PIM (mobile device instant messaging)</span></span>

  - <span data-ttu-id="e026a-162">ExumConnectivity (Exchange ユニファイド メッセージング)</span><span class="sxs-lookup"><span data-stu-id="e026a-162">ExumConnectivity (Exchange Unified Messaging)</span></span>

  - <span data-ttu-id="e026a-163">JoinLauncher</span><span class="sxs-lookup"><span data-stu-id="e026a-163">JoinLauncher</span></span>

  - <span data-ttu-id="e026a-164">PersistentChatMessage</span><span class="sxs-lookup"><span data-stu-id="e026a-164">PersistentChatMessage</span></span>

  - <span data-ttu-id="e026a-165">DataConference</span><span class="sxs-lookup"><span data-stu-id="e026a-165">DataConference</span></span>

  - <span data-ttu-id="e026a-166">XmppIM</span><span class="sxs-lookup"><span data-stu-id="e026a-166">XmppIM</span></span>

  - <span data-ttu-id="e026a-167">UnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="e026a-167">UnifiedContactStore</span></span>

</div>

<div>

## <a name="adding-and-removing-synthetic-transactions"></a><span data-ttu-id="e026a-168">代理トランザクションの追加と削除</span><span class="sxs-lookup"><span data-stu-id="e026a-168">Adding and Removing Synthetic Transactions</span></span>

<span data-ttu-id="e026a-169">ウォッチャーノードが構成されると、 **CsWatcherNodeConfiguration** コマンドレットを使用して、ノードの合成トランザクションを追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="e026a-169">After a watcher node has been configured, you can use the **Set-CsWatcherNodeConfiguration** cmdlet to add or remove synthetic transactions from the node.</span></span> <span data-ttu-id="e026a-170">たとえば、監視ノードに PersistentChatMessage テストを追加するには Add メソッドと次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e026a-170">For example, to add the PersistentChatMessage test to the watcher node, use the Add method and a command similar to this:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Add="PersistentChatMessage"}

<span data-ttu-id="e026a-171">テスト名をコンマで区切ることにより、複数のテストを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e026a-171">Multiple tests can be added by separating the test names by using commas.</span></span> <span data-ttu-id="e026a-172">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e026a-172">For example:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Add="PersistentChatMessage","DataConference","UnifiedContactStore"}

<span data-ttu-id="e026a-173">このようなテスト (たとえば、DataConference) がウォッチャーノードで既に有効になっている場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e026a-173">Note that an error will occur if one or more of these tests (for example, DataConference) has already been enabled on the watcher node.</span></span> <span data-ttu-id="e026a-174">この場合、次のようなエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e026a-174">In this case, you will receive an error message similar to the following:</span></span>

    Set-CsWatcherNodeConfiguration : There is a duplicate key sequence 'DataConference' for the 'urn:schema:Microsoft.Rtc.Management.Settings.WatcherNode.2010:TestName' key or unique identity constraint.

<span data-ttu-id="e026a-175">このエラーが発生した場合、変更は一切適用されません。</span><span class="sxs-lookup"><span data-stu-id="e026a-175">When this error occurs, no changes will be applied.</span></span> <span data-ttu-id="e026a-176">重複したテストを削除してコマンドを再実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-176">The command should be rerun with the duplicate test removed.</span></span>

<span data-ttu-id="e026a-177">ウォッチャーノードから合成トランザクションを削除するには、Add メソッドの代わりに Remove メソッドを使います。</span><span class="sxs-lookup"><span data-stu-id="e026a-177">To remove a synthetic transaction from a watcher node, use the Remove method instead of the Add method.</span></span> <span data-ttu-id="e026a-178">たとえば、次のコマンドでは、監視ノードから ABWQ テストを削除します。</span><span class="sxs-lookup"><span data-stu-id="e026a-178">For example, this command removes the ABWQ test from a watcher node:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Remove="ABWQ"}

<span data-ttu-id="e026a-179">また、Replace メソッドを使用して、現在有効になっているすべてのテストを1つまたは複数の新しいテストに置き換えることもできます。</span><span class="sxs-lookup"><span data-stu-id="e026a-179">You can also use the Replace method to replace all the currently-enabled tests with one or more new tests.</span></span> <span data-ttu-id="e026a-180">たとえば、watcher ノードで IM テストを実行する場合は、次のコマンドを使用してそれを構成できます。</span><span class="sxs-lookup"><span data-stu-id="e026a-180">For example, if you only want a watcher node to run the IM test, you can configure that by using this command:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Replace="IM"}

<span data-ttu-id="e026a-181">上のコマンドを実行すると、指定したウォッチャーノードのすべての代理トランザクションが、IM 以外は無効になります。</span><span class="sxs-lookup"><span data-stu-id="e026a-181">When you run the preceding command, all synthetic transactions on the specified watcher node will be disabled except for IM.</span></span>

</div>

<div>

## <a name="viewing-and-testing-the-watcher-node-configuration"></a><span data-ttu-id="e026a-182">監視ノード構成の表示とテスト</span><span class="sxs-lookup"><span data-stu-id="e026a-182">Viewing and Testing the Watcher Node Configuration</span></span>

<span data-ttu-id="e026a-183">監視ノードに割り当てられているテストを表示する場合は、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e026a-183">If you want to view the tests that have been assigned to a watcher node, use a command similar to this:</span></span>

    Get-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object -ExpandProperty Tests

<span data-ttu-id="e026a-184">上記のコマンドは、ノードに割り当てられている代理トランザクションに応じて、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="e026a-184">The preceding command will return information similar to this, depending on the synthetic transactions that have been assigned to the node:</span></span>

    Registration
    IM
    GroupIM
    P2PAV
    AvConference
    Presence
    PersistentChatMessage
    DataConference

<div>


> [!TIP]
> <span data-ttu-id="e026a-185">代理トランザクションをアルファベット順で表示するには、代わりに次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e026a-185">To view the synthetic transactions in alphabetical order, use this command instead:</span></span><BR><span data-ttu-id="e026a-186">Get-CsWatcherNodeConfiguration – Identity "atl-cs-001.litwareinc.com" |Select-Object – ExpandProperty のテスト |Sort-Object</span><span class="sxs-lookup"><span data-stu-id="e026a-186">Get-CsWatcherNodeConfiguration –Identity "atl-cs-001.litwareinc.com" | Select-Object –ExpandProperty Tests | Sort-Object</span></span>



</div>

<span data-ttu-id="e026a-187">ウォッチャーノードが作成されたことを確認するには、Lync Server 管理シェル内から次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="e026a-187">To verify that a watcher node has been created, type the following command from within the Lync Server Management Shell:</span></span>

    Get-CsWatcherNodeConfiguration

<span data-ttu-id="e026a-188">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e026a-188">You will receive information similar to this:</span></span>

    Identity      : atl-cs-001.litwareinc.com
    TestUsers     : {sip:watcher1@litwareinc.com, sip:watcher2@litwareinc.com ...}
    ExtendedTests : {TestUsers=IList<System.String>;Name=PSTN Test; Te...}
    TargetFqdn    : atl-cs-001.litwareinc.com
    PortNumber    : 5061

<span data-ttu-id="e026a-189">ウォッチャーノードが正しく構成されていることを確認するには、Lync Server 管理シェルで次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="e026a-189">To verify that the watcher node has been configured correctly, type the following command from within the Lync Server Management Shell:</span></span>

    Test-CsWatcherNodeConfiguration

<span data-ttu-id="e026a-190">上のコマンドを実行すると、展開の各ウォッチャーノードがテストされ、次のような情報がわかります。</span><span class="sxs-lookup"><span data-stu-id="e026a-190">The preceding command will test each watcher node in your deployment and tell you information, such as whether:</span></span>

  - <span data-ttu-id="e026a-191">必要なレジストラー役割がインストールされました。</span><span class="sxs-lookup"><span data-stu-id="e026a-191">The required Registrar role been installed.</span></span>

  - <span data-ttu-id="e026a-192">CsWatcherNodeConfiguration を実行したときに必要なレジストリキーが作成されました。</span><span class="sxs-lookup"><span data-stu-id="e026a-192">The required registry key was created for you when you ran Set-CsWatcherNodeConfiguration.</span></span>

  - <span data-ttu-id="e026a-193">サーバーで、正しいバージョンの Lync Server が実行されている。</span><span class="sxs-lookup"><span data-stu-id="e026a-193">Your servers are running the correct version of Lync Server.</span></span>

  - <span data-ttu-id="e026a-194">ポートが正しく構成されています。</span><span class="sxs-lookup"><span data-stu-id="e026a-194">Your ports been configured correctly.</span></span>

  - <span data-ttu-id="e026a-195">割り当てられたテストユーザーには、必要な資格情報があります。</span><span class="sxs-lookup"><span data-stu-id="e026a-195">Your assigned test users have the required credentials.</span></span>

<span data-ttu-id="e026a-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e026a-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

