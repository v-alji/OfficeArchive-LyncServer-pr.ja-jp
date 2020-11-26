---
title: 'Lync Server 2013: モビリティの要件の定義'
description: 'Lync Server 2013: モビリティの要件を定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your mobility requirements
ms:assetid: b7608335-cdeb-4aae-8e4b-d80c55f0d62b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690039(v=OCS.15)
ms:contentKeyID: 48185226
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fbc1a443946f0c879397f41628cfe788b428ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430897"
---
# <a name="defining-your-mobility-requirements-for-lync-server-2013"></a><span data-ttu-id="01f40-103">Lync Server 2013 でのモビリティの要件の定義</span><span class="sxs-lookup"><span data-stu-id="01f40-103">Defining your mobility requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01f40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01f40-104">

<span> </span></span></span>

<span data-ttu-id="01f40-105">_**最終更新日:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="01f40-105">_**Topic Last Modified:** 2013-02-14_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="01f40-106">Lync 2010 Mobile および Lync 2013 モバイルクライアントを使用している場合、Lync Server 2013 のモバイル機能の計画フェーズでは、展開の手順を決定する意思決定を行います。</span><span class="sxs-lookup"><span data-stu-id="01f40-106">During the planning phase for the Lync Server 2013 mobility feature, when you are using Lync 2010 Mobile and Lync 2013 Mobile clients, you make decisions that determine your deployment steps.</span></span>

<span data-ttu-id="01f40-107">考慮する必要がある決定事項は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="01f40-107">Here are the decisions that you must consider:</span></span>

  - <span data-ttu-id="01f40-108">**Lync モバイルクライアントの自動検出を使用しますか?**</span><span class="sxs-lookup"><span data-stu-id="01f40-108">**Do you want to use automatic discovery for Lync mobile clients?**</span></span>
    
    <span data-ttu-id="01f40-109">自動検出をサポートするには、新しい内部および外部ドメインネームシステム (DNS) レコードを作成し、フロントエンドサーバー、ディレクター、リバースプロキシの証明書にサブジェクトの代替名を追加して、リバースプロキシで既存の公開ルールを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-109">If you want to support automatic discovery, you need to create new internal and external Domain Name System (DNS) records, add subject alternative names to certificates on the Front End Servers, Directors, and reverse proxy, and modify the existing publishing rules on the reverse proxy.</span></span> <span data-ttu-id="01f40-110">詳細については、「 [Lync Server 2013 でのモビリティの技術要件](lync-server-2013-technical-requirements-for-mobility.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f40-110">For details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="01f40-111">自動検出を使用すると、ユーザーは、モバイルデバイスの設定で Url を入力しなくても、企業ネットワークの内外の任意の場所から Lync Server 2013 Web サービスを自動的に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="01f40-111">With automatic discovery, users can automatically locate Lync Server 2013 Web Services from anywhere inside or outside the corporate network, without entering URLs in their mobile device settings.</span></span>
    
    <span data-ttu-id="01f40-112">自動検出の代わりに手動の設定を使用する場合、モバイルユーザーは、モバイルデバイスに次の Url を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-112">If you use manual settings instead of automatic discovery, mobile users need to manually enter the following URLs in their mobile devices:</span></span>
    
      - <span data-ttu-id="01f40-113">\<ExtPoolFQDN\>外部アクセス用の Https:///Autodiscover/autodiscoverservice.svc/Root</span><span class="sxs-lookup"><span data-stu-id="01f40-113">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>
    
      - <span data-ttu-id="01f40-114">\<IntPoolFQDN\>内部アクセス用の Https:///AutoDiscover/autodiscoverservice/ルート</span><span class="sxs-lookup"><span data-stu-id="01f40-114">https://\<IntPoolFQDN\>/AutoDiscover/ autodiscoverservice.svc/Root for internal access</span></span>
    
    <span data-ttu-id="01f40-115">自動検出を使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="01f40-115">We strongly recommend using automatic discovery.</span></span> <span data-ttu-id="01f40-116">手動設定の主な用途は、トラブルシューティングです。</span><span class="sxs-lookup"><span data-stu-id="01f40-116">The primary use of manual settings is for troubleshooting.</span></span>

  - <span data-ttu-id="01f40-117">**自動検出をサポートすることにした場合、リバースプロキシの証明書を各 SIP ドメインのサブジェクト別の名前を使用して更新する必要がありますか?**</span><span class="sxs-lookup"><span data-stu-id="01f40-117">**If you decide to support automatic discovery, are you willing to update certificates on the reverse proxy with subject alternative names for each SIP domain?**</span></span>
    
    <span data-ttu-id="01f40-118">SIP ドメインが多い場合は、リバースプロキシのパブリック証明書を更新すると非常にコストがかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="01f40-118">If you have many SIP domains, updating public certificates on the reverse proxy can become very expensive.</span></span> <span data-ttu-id="01f40-119">この場合は、自動検出を実装して、HTTPS をポート443で使う代わりに、最初の自動検出サービス要求でポート80に対して HTTP を使うようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="01f40-119">If this is the case, you can choose to implement automatic discovery so that the initial Autodiscover Service request uses HTTP on port 80, instead of using HTTPS on port 443.</span></span> <span data-ttu-id="01f40-120">ただし、この方法はお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="01f40-120">However, this is not the recommended approach.</span></span> <span data-ttu-id="01f40-121">この代替を選択する場合は、リバースプロキシで証明書を更新する必要はありませんが、HTTP 用の web 公開ルールは、ポート80で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-121">If you decide to choose this alternative, you do not need to update the certificates on the reverse proxy, but you need to create a web publishing rule for HTTP on port 80.</span></span> <span data-ttu-id="01f40-122">詳細については、「 [Lync Server 2013 でのモビリティの技術要件](lync-server-2013-technical-requirements-for-mobility.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f40-122">For more details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="01f40-123">**企業ネットワークの内部と外部の両方の Lync モバイルクライアントをサポートしますか。または企業ネットワーク内でのみサポートされているクライアントをサポートしますか?**</span><span class="sxs-lookup"><span data-stu-id="01f40-123">**Do you want to support Lync mobile clients both internal and external to the corporate network, or support clients only inside the corporate network?**</span></span>
    
    <span data-ttu-id="01f40-124">ネットワークの内部と外部のモバイルクライアントをサポートしたい場合、モバイルデバイスはどこからでもモビリティ機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="01f40-124">If you want to support mobile clients internal and external to your network, mobile devices can access mobility features from any location.</span></span> <span data-ttu-id="01f40-125">既定の構成では、社内ネットワークと社外のクライアントの両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="01f40-125">The default configuration is to support clients both internal and external to the corporate network.</span></span>
    
    <span data-ttu-id="01f40-126">既定の構成では、モバイルクライアントトラフィックが外部サイトを通過できるようになりますが、モバイルクライアントトラフィックを内部の企業ネットワークに制限することができます。</span><span class="sxs-lookup"><span data-stu-id="01f40-126">Although the default configuration enables mobile client traffic to go through the external site, you can restrict mobile client traffic to the internal corporate network.</span></span> <span data-ttu-id="01f40-127">内部ネットワークへのトラフィックを制限すると、ユーザーは、ネットワーク内にいるときにのみ、モバイルデバイスで Lync モバイルアプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="01f40-127">When you restrict the traffic to the internal network, users can use Lync mobile applications on their mobile devices only when they are inside the network.</span></span>
    
    <span data-ttu-id="01f40-128">Mcx mobility service と Lync 2010 Mobile を使ったモビリティをサポートする展開の場合は、 **Set-CsMcxConfiguration** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="01f40-128">For deployments that support mobility using the Mcx mobility service and Lync 2010 Mobile, you run the **Set-CsMcxConfiguration** cmdlet.</span></span> <span data-ttu-id="01f40-129">内部使用のためだけにモバイル機能を設定するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f40-129">To set mobility for internal use only, you would use a command similar to the following:</span></span>
    
        Set-CsMcxConfiguration -Identity site:Redmond -ExposedWebURL Internal
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="01f40-130">UCWA には、その他の構成は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="01f40-130">There are no additional configurations required for UCWA.</span></span> <span data-ttu-id="01f40-131">UCWA には、相当する内部専用構成がありません。</span><span class="sxs-lookup"><span data-stu-id="01f40-131">UCWA does not have an equivalent internal-only configuration.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="01f40-132">Lync Server 2013 フロントエンドサーバーまたはフロントエンドプールを使用していて、 &nbsp; Lync server 2010 フロントエンドサーバーまたはフロントエンドプールを使って <STRONG>い</STRONG> ない場合は &nbsp; 、 <STRONG>cookie ベースの常設は必要ありませ</STRONG>ん。</span><span class="sxs-lookup"><span data-stu-id="01f40-132">If you are using a Lync Server 2013&nbsp;Front End Server or Front End pools and <STRONG>you do not have</STRONG> any Lync Server 2010&nbsp;Front End Servers or Front End pools, <STRONG>there is no requirement for cookie-based persistence</STRONG>.</span></span> <span data-ttu-id="01f40-133">Lync Server 2010 &nbsp; フロントエンドサーバーまたはフロントエンドプールを保持する必要がある場合は、依然として、cookie ベースの常設用に Lync server 2010 の場合と同じ規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="01f40-133">If you need to retain any Lync Server 2010&nbsp;Front End Servers or Front End pools, the same rules still apply as in Lync Server 2010 for cookie-based persistence.</span></span>

    
    </div>

  - <span data-ttu-id="01f40-134">**Apple iOS デバイスと Windows Phone のプッシュ通知をサポートしますか?**</span><span class="sxs-lookup"><span data-stu-id="01f40-134">**Do you want to support push notifications for Apple iOS devices and Windows Phones?**</span></span>
    
    <span data-ttu-id="01f40-135">プッシュ通知をサポートしている場合、サポートされている Apple iOS デバイスと Windows Phone は、モバイルアプリケーションが非アクティブなときに発生するイベントの通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="01f40-135">If you support push notifications, supported Apple iOS devices and Windows Phones receive a notification of events that occur when the mobile application is inactive.</span></span> <span data-ttu-id="01f40-136">エッジサーバーは、Lync Online データセンターにあるクラウドベースの Lync Server プッシュ通知サービスとのフェデレーション関係を持ち、プッシュ通知を有効にするコマンドレットを実行するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-136">You must configure your Edge Server to have a federation relationship with the cloud-based Lync Server Push Notification Service, which is located in the Lync Online datacenter, and run a cmdlet to enable push notifications.</span></span>
    
    <span data-ttu-id="01f40-137">Wi-Fi ネットワーク経由でプッシュ通知をサポートする必要がある場合は、モバイルデバイスプロバイダーの3G またはデータネットワーク経由でプッシュ通知をサポートするだけでなく、エンタープライズ Wi-Fi ネットワークでポート5223送信を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-137">If you want to support push notifications over your Wi-Fi network, in addition to supporting push notifications over the mobile device providers' 3G or data networks, you must open port 5223 outbound on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="01f40-138">Wi-Fi ネットワーク経由でのプッシュ通知のサポートには、Wi-Fi と、室内受信の低いモバイルデバイスのみを使用するモバイルデバイスがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="01f40-138">Supporting push notifications over the Wi-Fi network supports mobile devices that use only Wi-Fi and mobile devices that have poor indoor reception.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="01f40-139">Lync 2010 モバイルクライアントを実行している Apple デバイスをサポートしている場合にのみ、ポート TCP 5223 を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-139">Opening port TCP 5223 is required only when supporting Apple devices running the Lync 2010 Mobile client.</span></span>

    
    </div>
    
    <span data-ttu-id="01f40-140">プッシュ通知がサポートされていない場合は、Apple モバイルデバイスおよび Windows Phone のユーザーは、モバイルアプリケーションが非アクティブなときに発生する、インスタントメッセージの招待状や不在着信メッセージなどのイベントについては検出されません。</span><span class="sxs-lookup"><span data-stu-id="01f40-140">If you do not support push notifications, users of Apple mobile devices and Windows Phones will not find out about events—such as instant message invitations or missed messages—that occur when the mobile application is inactive.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="01f40-141">Apple デバイス上の Lync 2013 モバイルクライアントでは、プッシュ通知は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="01f40-141">Lync 2013 Mobile clients on Apple devices do not require push notification.</span></span> <span data-ttu-id="01f40-142">Windows Phone の Lync 2013 モバイルクライアントでは、プッシュ通知が使われます。</span><span class="sxs-lookup"><span data-stu-id="01f40-142">The Lync 2013 Mobile clients on Windows Phone use push notification.</span></span> <span data-ttu-id="01f40-143">プッシュ通知の計画とプッシュ通知のクリアリングハウスは、Lync 2013 モバイルクライアントを実行できない Windows Phone および Apple デバイス上の Lync Mobile でも同じです。</span><span class="sxs-lookup"><span data-stu-id="01f40-143">Planning for push notification and the push notification clearinghouse remain the same for Lync Mobile on Windows Phone and Apple devices that are not able to run the Lync 2013 Mobile client.</span></span>

    
    </div>

  - <span data-ttu-id="01f40-144">**すべてのユーザーがモビリティ機能にアクセスできるようにするか、これらの機能にアクセスできるユーザーを指定できるようにする必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="01f40-144">**Do you want all users to have access to mobility features, or do you want to be able to specify which users have access to these features?**</span></span>
    
    <span data-ttu-id="01f40-145">この表では、Lync Server 2013 でユーザーが使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="01f40-145">The table describes features available to users in Lync Server 2013.</span></span> <span data-ttu-id="01f40-146">既定では、勤務先での通話が許可され、ボイスオーバー IP (VoIP) が許可され、モビリティが有効になります。</span><span class="sxs-lookup"><span data-stu-id="01f40-146">The defaults allow Call via Work, allow Voice over IP (VoIP), and enable Mobility.</span></span> <span data-ttu-id="01f40-147">使用可能なオプションの全セットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="01f40-147">Here is the full set of available options:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="01f40-148">Feature/Parameter Name/Scope (ポリシーパラメーター名は同じではない可能性があります)</span><span class="sxs-lookup"><span data-stu-id="01f40-148">Feature/Parameter Name/Scope (Policy parameter names may not be the same)</span></span></th>
    <th><span data-ttu-id="01f40-149">説明</span><span class="sxs-lookup"><span data-stu-id="01f40-149">Description</span></span></th>
    <th><span data-ttu-id="01f40-150">導か</span><span class="sxs-lookup"><span data-stu-id="01f40-150">Introduced</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="01f40-151">モビリティを有効にする</span><span class="sxs-lookup"><span data-stu-id="01f40-151">Enable Mobility</span></span></p>
    <p><span data-ttu-id="01f40-152">パラメーター名: <code>EnableMobility</code></span><span class="sxs-lookup"><span data-stu-id="01f40-152">Parameter Name : <code>EnableMobility</code></span></span></p>
    <p><span data-ttu-id="01f40-153">スコープ: グローバル/サイト/ユーザー</span><span class="sxs-lookup"><span data-stu-id="01f40-153">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="01f40-154">管理者設定 Lync Mobile がインストールされている特定のスコープでユーザーを制御するには、ポリシーを False に設定すると、ユーザーはクライアントにサインインできなくなります。</span><span class="sxs-lookup"><span data-stu-id="01f40-154">Administrative setting to control users in a given scope that have the Lync Mobile installed, If the policy is set to False, the user would not be able to sign into the client.</span></span></p>
    <p><span data-ttu-id="01f40-155">既定の設定は True です。</span><span class="sxs-lookup"><span data-stu-id="01f40-155">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="01f40-156">Lync Server 2010 の累積更新プログラム: 2011 年11月</span><span class="sxs-lookup"><span data-stu-id="01f40-156">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="01f40-157">外部音声を有効にする</span><span class="sxs-lookup"><span data-stu-id="01f40-157">Enable Outside Voice</span></span></p>
    <p><span data-ttu-id="01f40-158">パラメーター名: <code>EnableOutsideVoice</code></span><span class="sxs-lookup"><span data-stu-id="01f40-158">Parameter Name : <code>EnableOutsideVoice</code></span></span></p>
    <p><span data-ttu-id="01f40-159">スコープ: グローバル/サイト/ユーザー</span><span class="sxs-lookup"><span data-stu-id="01f40-159">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="01f40-160">勤務先のユーザーが通話を使用する機能を制御します。この機能は、ユーザーが携帯電話番号の代わりに勤務先の電話番号を使って通話を発信および受信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="01f40-160">Controls a user’s ability to use Call Via Work, a feature that enables users to make and receive calls by using their work number instead of their mobile number.</span></span> <span data-ttu-id="01f40-161">False に設定した場合、ユーザーはモバイルデバイスから勤務先の電話番号を使用して通話を発信または受信することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="01f40-161">If set to False, the user will not be able to make or receive calls by using their work number from their mobile device.</span></span></p>
    <p><span data-ttu-id="01f40-162">既定の設定は True です。</span><span class="sxs-lookup"><span data-stu-id="01f40-162">The default setting is True</span></span></p></td>
    <td><p><span data-ttu-id="01f40-163">Lync Server 2010 の累積更新プログラム: 2011 年11月</span><span class="sxs-lookup"><span data-stu-id="01f40-163">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="01f40-164">IP オーディオと IP ビデオを有効にする</span><span class="sxs-lookup"><span data-stu-id="01f40-164">Enable IP Audio and Video</span></span></p>
    <p><span data-ttu-id="01f40-165">パラメーター名: <code>EnableIPAudioVideo</code></span><span class="sxs-lookup"><span data-stu-id="01f40-165">Parameter Name : <code>EnableIPAudioVideo</code></span></span></p>
    <p><span data-ttu-id="01f40-166">スコープ: グローバル/サイト/ユーザー</span><span class="sxs-lookup"><span data-stu-id="01f40-166">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="01f40-167">ユーザーがモバイルデバイスで VoIP を使用して音声通話またはビデオ通話を受信できるようにするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="01f40-167">Controls whether a user can use VoIP to make or receive voice or video calls on their mobile device.</span></span> <span data-ttu-id="01f40-168">False に設定すると、ユーザーはデバイスで VoIP またはビデオ通話を発信または受信できなくなります。</span><span class="sxs-lookup"><span data-stu-id="01f40-168">If set to False, the user will not be able to make or receive VoIP or video calls on their device.</span></span></p>
    <p><span data-ttu-id="01f40-169">既定の設定は True です。</span><span class="sxs-lookup"><span data-stu-id="01f40-169">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="01f40-170">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01f40-170">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="01f40-171">IP オーディオ用の WiFi が必要</span><span class="sxs-lookup"><span data-stu-id="01f40-171">Require WiFi for IP Audio</span></span></p>
    <p><span data-ttu-id="01f40-172">パラメーター名: <code>RequireWiFiForIPAudio</code></span><span class="sxs-lookup"><span data-stu-id="01f40-172">Parameter Name : <code>RequireWiFiForIPAudio</code></span></span></p>
    <p><span data-ttu-id="01f40-173">スコープ: グローバル/サイト/ユーザー</span><span class="sxs-lookup"><span data-stu-id="01f40-173">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="01f40-174">この設定は、携帯電話のデータネットワークではなく、WiFi 上の VoIP 経由での通話の発信と受信をクライアントが必要とするかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="01f40-174">This setting defines whether the client will be required to make and receive calls over VoIP on WiFi instead of the cellular data network.</span></span> <span data-ttu-id="01f40-175">True に設定すると、ユーザーは WiFi ネットワークに接続している場合にのみ VoIP 通話を発信および受信できます。</span><span class="sxs-lookup"><span data-stu-id="01f40-175">If set to True, the user can make and receive VoIP calls only when connected to a WiFi network.</span></span></p>
    <p><span data-ttu-id="01f40-176">既定の設定は False です。</span><span class="sxs-lookup"><span data-stu-id="01f40-176">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="01f40-177">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01f40-177">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="01f40-178">IP ビデオ用の WiFi が必要</span><span class="sxs-lookup"><span data-stu-id="01f40-178">Require WiFi for IP Video</span></span></p>
    <p><span data-ttu-id="01f40-179">パラメーター名: <code>RequireWiFiForIPVideo</code></span><span class="sxs-lookup"><span data-stu-id="01f40-179">Parameter Name : <code>RequireWiFiForIPVideo</code></span></span></p>
    <p><span data-ttu-id="01f40-180">スコープ: グローバル/サイト/ユーザー</span><span class="sxs-lookup"><span data-stu-id="01f40-180">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="01f40-181">この設定では、携帯電話のデータネットワークではなく、Wi-Fi でのビデオ通話の発信と受信をクライアントが必要とするかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="01f40-181">This setting defines whether the client will be required to make and receive video calls on Wi-Fi instead of on the cellular data network.</span></span> <span data-ttu-id="01f40-182">True に設定すると、Wi-Fi ネットワークに接続しているときにのみビデオ通話を発信および受信できます。</span><span class="sxs-lookup"><span data-stu-id="01f40-182">If set to True, the user can make and receive video calls only when connected to a Wi-Fi network.</span></span></p>
    <p><span data-ttu-id="01f40-183">既定の設定は False です。</span><span class="sxs-lookup"><span data-stu-id="01f40-183">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="01f40-184">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01f40-184">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="01f40-185">構成可能なポリシー設定とポリシーの管理方法の説明については、「 [New-set-csmobilitypolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy)、 [Set-set-csmobilitypolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy)、 [Get-set-csmobilitypolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy)、 [Grant-set-csmobilitypolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) 、 [Remove-set-csmobilitypolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f40-185">For a description of the policy settings that you can configure, and how to manage the policies, see [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) and [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span></span>

  - <span data-ttu-id="01f40-186">**エンタープライズ Voip が有効になっていないユーザーが、クリックして会議に参加できるようにしますか?**</span><span class="sxs-lookup"><span data-stu-id="01f40-186">**Do you want users who are not enabled for Enterprise Voice to be able to use Click to Join to join conferences?**</span></span>
    
    <span data-ttu-id="01f40-187">ユーザーがモバイル機能にアクセスし、勤務先から通話を発信できるようにするには、エンタープライズ Voip を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-187">For users to have access to mobility features and Call via Work, they must be enabled for Enterprise Voice.</span></span> <span data-ttu-id="01f40-188">ただし、エンタープライズ Voip を有効にしていないユーザーは、モバイルデバイス上のリンクをクリックすると、適切な音声ポリシーが割り当てられている場合に、会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="01f40-188">However, users who are not enabled for Enterprise Voice can join conferences by clicking the link on their mobile device, if they have an appropriate voice policy assigned to them.</span></span> <span data-ttu-id="01f40-189">特定のボイスポリシーをこれらのユーザーに割り当てるか、グローバルポリシーまたはサイトレベルのポリシーが存在していることを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="01f40-189">You can either assign a specific voice policy to these users or make sure that a global policy or site-level policy exists that applies to them.</span></span> <span data-ttu-id="01f40-190">割り当てるボイスポリシーには、公衆交換電話網 (PSTN) 利用状況レコードと、ユーザーが電話会議にダイヤルアウトできる領域を定義するルートが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f40-190">The voice policy that you assign must have public switched telephone network (PSTN) usage records and routes that define the areas to which users can dial out to join a conference.</span></span> <span data-ttu-id="01f40-191">ボイスポリシー、PSTN 使用状況レコード、およびルートの設定の詳細については、「 [Lync Server 2013 で音声ポリシー、pstn 使用状況レコード、および音声ルートを構成する](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f40-191">For details about setting voice policy, PSTN usage records, and routes, see [Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="01f40-192">クリックして参加したいモバイルユーザーは、モバイルデバイスでリンクをクリックすると、Lync Server 2013 からの発信通話が発生するため、音声ポリシーと関連する PSTN 使用状況レコードと音声ルートが必要になります。</span><span class="sxs-lookup"><span data-stu-id="01f40-192">Mobile users who want to use Click to Join require a voice policy, along with the related PSTN usage records and voice routes, because clicking the link on the mobile device results in an outbound call from Lync Server 2013.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="01f40-193">関連項目</span><span class="sxs-lookup"><span data-stu-id="01f40-193">See Also</span></span>


[<span data-ttu-id="01f40-194">Lync Server 2013 でのモビリティの技術要件</span><span class="sxs-lookup"><span data-stu-id="01f40-194">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  


[<span data-ttu-id="01f40-195">Lync Server 2013 での音声ポリシー、PSTN 使用状況レコード、および音声ルートの構成</span><span class="sxs-lookup"><span data-stu-id="01f40-195">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="01f40-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01f40-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

