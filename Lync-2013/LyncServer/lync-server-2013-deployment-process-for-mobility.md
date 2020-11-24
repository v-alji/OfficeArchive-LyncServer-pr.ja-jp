---
title: 'Lync Server 2013: モビリティの展開プロセス'
description: 'Lync Server 2013: モビリティの展開プロセス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for mobility
ms:assetid: 5a1cebda-c14b-4ff4-9c36-f7caa868160f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690023(v=OCS.15)
ms:contentKeyID: 48184220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b49d69af899f6d9f2ac1db5040d017a9d62ce9eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399561"
---
# <a name="deployment-process-for-mobility-in-lync-server-2013"></a><span data-ttu-id="b0eb4-103">Lync Server 2013 のモビリティの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="b0eb4-103">Deployment process for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0eb4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0eb4-104">

<span> </span></span></span>

<span data-ttu-id="b0eb4-105">_**最終更新日:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="b0eb4-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013. It is noted accordingly.

<span data-ttu-id="b0eb4-106">このセクションでは、Lync Server 2013 モビリティ機能の展開に必要な一連の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-106">This section describes the sequence of steps required to deploy the Lync Server 2013 mobility feature.</span></span>

### <a name="mobility-deployment-process"></a><span data-ttu-id="b0eb4-107">モバイル展開プロセス</span><span class="sxs-lookup"><span data-stu-id="b0eb4-107">Mobility Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0eb4-108">段階</span><span class="sxs-lookup"><span data-stu-id="b0eb4-108">Phase</span></span></th>
<th><span data-ttu-id="b0eb4-109">ステップ</span><span class="sxs-lookup"><span data-stu-id="b0eb4-109">Steps</span></span></th>
<th><span data-ttu-id="b0eb4-110">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="b0eb4-110">Permissions</span></span></th>
<th><span data-ttu-id="b0eb4-111">「展開」のドキュメント</span><span class="sxs-lookup"><span data-stu-id="b0eb4-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0eb4-112">ドメインネームシステム (DNS) レコードを作成する</span><span class="sxs-lookup"><span data-stu-id="b0eb4-112">Create Domain Name System (DNS) records</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b0eb4-113">内部の自動検出サービス URL を解決する内部 DNS CNAME または A (IPv6、AAAA) レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-113">Create an internal DNS CNAME or A (host, if IPv6, AAAA) record to resolve the internal Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-114">外部の自動検出サービス URL を解決するには、外部 DNS CNAME または A (IPv6、AAAA) レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-114">Create an external DNS CNAME or A (host, if IPv6, AAAA) record to resolve the external Autodiscover Service URL.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b0eb4-115">Domain Admins</span><span class="sxs-lookup"><span data-stu-id="b0eb4-115">Domain Admins</span></span></p>
<p><span data-ttu-id="b0eb4-116">DnsAdmins</span><span class="sxs-lookup"><span data-stu-id="b0eb4-116">DnsAdmins</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Lync Server 2013 での自動検出サービスの DNS レコードの作成</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Creating DNS records for the Autodiscover Service in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0eb4-118">証明書を変更する</span><span class="sxs-lookup"><span data-stu-id="b0eb4-118">Modify certificates</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-119">モバイルユーザーへのセキュリティで保護された接続をサポートするために、次の証明書にサブジェクト代替名のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-119">Add subject alternative name entries to the following certificates to support secure connections for mobile users:</span></span></p>
<ul>
<li><p><span data-ttu-id="b0eb4-120">ディレクター証明書</span><span class="sxs-lookup"><span data-stu-id="b0eb4-120">Director certificate</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-121">フロントエンドプールの証明書</span><span class="sxs-lookup"><span data-stu-id="b0eb4-121">Front End pool certificate</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-122">リバースプロキシ証明書</span><span class="sxs-lookup"><span data-stu-id="b0eb4-122">Reverse proxy certificate</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b0eb4-123">ローカル管理者</span><span class="sxs-lookup"><span data-stu-id="b0eb4-123">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Lync Server 2013 でのモビリティに合わせた証明書の変更</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modifying certificates for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0eb4-125">リバース プロキシを構成する</span><span class="sxs-lookup"><span data-stu-id="b0eb4-125">Configure the reverse proxy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b0eb4-126">サブジェクトの代替名を使用して、セキュリティで保護されたソケットレイヤー (SSL) リスナーに証明書を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-126">Assign certificates updated with subject alternative names to the Secure Sockets Layer (SSL) Listener.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-127">外部自動検出サービス URL の web 公開ルールを再構成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-127">Reconfigure the web publishing rule for the external Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-128">フロントエンドプールの外部の Lync Server 2013 Web サービスの URL に web 発行ルールが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-128">Be sure that a web publishing rule exists for the external Lync Server 2013 Web Services URL on your Front End pool.</span></span></p></li>
</ul>
<p><span data-ttu-id="b0eb4-129">または</span><span class="sxs-lookup"><span data-stu-id="b0eb4-129">Or</span></span></p>
<ul>
<li><p><span data-ttu-id="b0eb4-130">最初の自動検出要求に HTTP を使用し、証明書のサブジェクト代替名の一覧を更新しない場合は、新しい web 公開ルールを構成するか、ポート 80 HTTP の既存の公開ルールを再設定します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-130">If you choose to use HTTP for the initial Autodiscover request and do not update subject alternative name lists on the certificates, configure a new web publishing rule or reconfigure an existing publishing rule for port 80 HTTP.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b0eb4-131">ローカル管理者</span><span class="sxs-lookup"><span data-stu-id="b0eb4-131">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Lync Server 2013 での、モビリティに合わせたリバース プロキシの構成</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0eb4-133">Mcx Mobility Service を使用して Lync 2010 Mobile のモバイル展開をテストする</span><span class="sxs-lookup"><span data-stu-id="b0eb4-133">Test your mobility deployment for Lync 2010 Mobile using the Mcx Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-134"><strong>CsMcxP2PIM</strong>を実行して、1人のユーザーから別のユーザーへのインスタントメッセージの送信をテストします。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-134">Run <strong>Test-CsMcxP2PIM</strong> to test sending an instant message from one person to another.</span></span></p>
<p><span data-ttu-id="b0eb4-135">オプションの完全な一覧については、「 <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">CsMcxP2PIM</a> の Lync Server 管理シェルコマンドレット」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-135">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">Test-CsMcxP2PIM</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-136">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="b0eb4-136">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Lync Server 2013 でのモビリティ展開の確認</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0eb4-138">UCWA Web コンポーネントを使用して Lync 2013 モバイルクライアント用のモバイル展開をテストする</span><span class="sxs-lookup"><span data-stu-id="b0eb4-138">Test your mobility deployment for Lync 2013 Mobile clients using the UCWA Web components</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-139"><strong>CsUcwaConference</strong>コマンドレットを使用して、事前に定義されたテストユーザーまたは実際のユーザーが ucwa を使用して会議を作成し、参加できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-139">Use the <strong>Test-CsUcwaConference</strong> cmdlet to test and verify that pre-defined test users or a pair of actual users can use UCWA to create and participate in a conference.</span></span></p>
<p><span data-ttu-id="b0eb4-140">オプションの完全な一覧については、「 <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">CsUcwaConference</a> の Lync Server 管理シェルコマンドレット」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-140">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">Test-CsUcwaConference</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-141">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="b0eb4-141">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Lync Server 2013 でのモビリティ展開の確認</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0eb4-143">プッシュ通知を構成する</span><span class="sxs-lookup"><span data-stu-id="b0eb4-143">Configure for push notifications</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b0eb4-144">Lync Server 2013 Edge サーバーの場合は、Lync Server online ホスティングプロバイダーを追加して、ホスティングプロバイダーフェデレーションを構成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-144">For Lync Server 2013 Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-145">Lync Server 2010 Edge サーバーの場合は、Lync Server online ホスティングプロバイダーを追加して、ホスティングプロバイダーフェデレーションを構成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-145">For Lync Server 2010  Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-146">Office Communications Server 2007 R2 Edge サーバーの場合は、フェデレーションパートナーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-146">For Office Communications Server 2007 R2 Edge Servers, add a federated partner.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-147">Wi-Fi ネットワーク経由でプッシュ通知をサポートするには、TCP ポート5223用のファイアウォール規則を構成します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-147">If you want to support push notifications over a Wi-Fi network, configure a firewall rule outbound for TCP port 5223.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-148"><strong>Set-cspの設定</strong>コマンドレットを使用して、Apple Push notification SERVICE (APNS) と Microsoft プッシュ通知サービス (MPNS) へのプッシュ通知を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-148">Use the <strong>Set-CsPushNotificationConfiguration</strong> cmdlet to enable push notifications to the Apple Push Notification Service (APNS) and Microsoft Push Notification Service (MPNS).</span></span> <span data-ttu-id="b0eb4-149">この機能は既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-149">This feature is disabled by default.</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-150"><strong>CsFederatedPartner</strong>コマンドレットを使用して、フェデレーション構成とテスト用<strong>CsMCXPushNotification</strong>コマンドレットをテストして、プッシュ通知をテストします。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-150">Use the <strong>Test-CsFederatedPartner</strong> cmdlet to test the federation configuration and the <strong>Test-CsMCXPushNotification</strong> cmdlet to test push notifications.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="b0eb4-151">Apple デバイスと Windows Phone での Lync 2010 モバイルクライアントでは、プッシュ通知が使われます。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-151">Push notifications are used for Lync 2010 Mobile clients on Apple devices and Windows Phone</span></span><BR><span data-ttu-id="b0eb4-152">Windows Phone のみの Lync 2013 モバイルクライアントでプッシュ通知が必要</span><span class="sxs-lookup"><span data-stu-id="b0eb4-152">Push notification is required for Lync 2013 Mobile clients on Windows Phone only</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="b0eb4-153">RtcUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b0eb4-153">RtcUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Lync Server 2013 でプッシュ通知を構成する</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configuring for push notifications in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0eb4-155">モビリティポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="b0eb4-155">Configure mobility policy</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-156"><strong>Set-csmobilitypolicy</strong>コマンドレットを使用して、次の操作を許可または禁止します。</span><span class="sxs-lookup"><span data-stu-id="b0eb4-156">Use the <strong>Set-CsMobilityPolicy</strong> cmdlet to allow or disallow:</span></span></p>
<ul>
<li><p><span data-ttu-id="b0eb4-157">勤務先から通話</span><span class="sxs-lookup"><span data-stu-id="b0eb4-157">Call via Work</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-158">IP オーディオと IP ビデオを有効にする</span><span class="sxs-lookup"><span data-stu-id="b0eb4-158">Enable IP Audio and IP Video</span></span></p></li>
<li><p><span data-ttu-id="b0eb4-159">[IP オーディオまたは IP ビデオに WiFi を使用する]</span><span class="sxs-lookup"><span data-stu-id="b0eb4-159">Require WiFi for IP Audio and/or IP Video</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b0eb4-160">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="b0eb4-160">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="b0eb4-161"><a href="lync-server-2013-configuring-mobility-policy.md">Lync Server 2013 でのモビリティ ポリシーの構成</a></span><span class="sxs-lookup"><span data-stu-id="b0eb4-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configuring mobility policy in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="b0eb4-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0eb4-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

