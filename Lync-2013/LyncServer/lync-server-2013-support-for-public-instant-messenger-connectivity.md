---
title: Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート
description: Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for public instant messenger connectivity
ms:assetid: 9c6eb500-647b-4ccd-a00e-2b8dd7c44a76
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn458579(v=OCS.15)
ms:contentKeyID: 59170234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d4a58d71eb23012da960cf4505f1a55fd08df32c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441502"
---
# <a name="support-for-public-instant-messenger-connectivity-in-lync-server-2013"></a><span data-ttu-id="9e064-103">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</span><span class="sxs-lookup"><span data-stu-id="9e064-103">Support for public instant messenger connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e064-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e064-104">

<span> </span></span></span>

<span data-ttu-id="9e064-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="9e064-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<div>

## <a name="support-for-public-instant-messenger-connectivity"></a><span data-ttu-id="9e064-106">パブリックインスタントメッセンジャーの接続のサポート</span><span class="sxs-lookup"><span data-stu-id="9e064-106">Support for Public Instant Messenger Connectivity</span></span>

<span data-ttu-id="9e064-107">この記事では、パブリック IM 接続 (PIC) のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9e064-107">This article provides information about support for Public IM Connectivity (PIC).</span></span> <span data-ttu-id="9e064-108">PIC は、Microsoft Lync の機能で、組織が lync クライアントや id を通じて、特定のパブリックインスタントメッセージング (IM) サービスのユーザーとつながることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="9e064-108">PIC is a feature of Microsoft Lync that allows organizations to enable their Lync users to connect with users of certain public instant messaging (IM) services through their Lync clients and identities.</span></span>

<span data-ttu-id="9e064-109">エンドユーザーは、顧客、パートナー、ベンダーとの間で利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9e064-109">End-users benefit from being able to connect with customers, partners, and vendors on their terms.</span></span> <span data-ttu-id="9e064-110">Lync の制御機能、コンプライアンス機能、アーカイブ機能を維持しながら、単一のリアルタイム通信クライアントをサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="9e064-110">IT benefits from supporting a single real-time communications client while maintaining the control, compliance, and archiving features of Lync.</span></span> <span data-ttu-id="9e064-111">2013年 5 [月に公開](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx)されている Lync-Skype 接続機能は、Lync/Office Communications SERVER (OCS)/live communications SERVER (LCS) が最初に MSN/Windows LIVE、AOL、Yahoo に接続するために確立した、従来の Lync に依存しています。</span><span class="sxs-lookup"><span data-stu-id="9e064-111">Lync-Skype connectivity, [publicly available in May 2013](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx), relies on the legacy that Lync/Office Communications Server (OCS)/Live Communications Server (LCS) first established with PIC in connecting to MSN/Windows Live, AOL, and Yahoo.</span></span>  <span data-ttu-id="9e064-112">Lync-Skype 接続の詳細については、「 [Lync-Skype の接続](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e064-112">For more information on Lync-Skype connectivity, see the [Lync-Skype connectivity](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx).</span></span> <span data-ttu-id="9e064-113">Windows Live、AOL、Yahoo とのフェデレーションはそれぞれ、ライフサイクルの終了までのパスにあります。</span><span class="sxs-lookup"><span data-stu-id="9e064-113">Federation with Windows Live, AOL, and Yahoo are each on a path towards end-of-life.</span></span> <span data-ttu-id="9e064-114">このページでは、各サービスの状態が記載されています。</span><span class="sxs-lookup"><span data-stu-id="9e064-114">This page documents the status of each service.</span></span>

<span data-ttu-id="9e064-115">PIC を使用するには、各パブリック IM サービスプロバイダーのサービスをアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e064-115">To use PIC, customers have been required to activate the service for each public IM service provider.</span></span> <span data-ttu-id="9e064-116">この方法の要件と詳細は、IM サービスプロバイダーと顧客の基になるライセンスプログラムによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9e064-116">The requirements and details for how to do this are dependent upon the IM service provider and the customer's underlying licensing program.</span></span>

<div>

## <a name="windows-live-messenger"></a><span data-ttu-id="9e064-117">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9e064-117">Windows Live Messenger</span></span>

<span data-ttu-id="9e064-118">Microsoft は、Windows Live Messenger と Skype を連携させることができました。</span><span class="sxs-lookup"><span data-stu-id="9e064-118">Microsoft brought Windows Live Messenger and Skype together.</span></span> <span data-ttu-id="9e064-119">2013年4月に、Messenger ユーザーはサインイン時に Skype に移行されました。</span><span class="sxs-lookup"><span data-stu-id="9e064-119">In April 2013, Messenger users were migrated to Skype upon sign-in.</span></span> <span data-ttu-id="9e064-120">Lync とのフェデレーションを利用している Lync のお客様は、Skype に更新した後でも、Messenger の連絡先と通信することができます。</span><span class="sxs-lookup"><span data-stu-id="9e064-120">Lync customers who rely on federation with Messenger will continue to be able to communicate with their Messenger contacts, even after those contacts update to Skype.</span></span> <span data-ttu-id="9e064-121">Lync 管理者または Lync のエンドユーザーがサービスの継続性を維持するために必要な操作はありません。また、Lync 内でのこの機能の管理は、Messenger との通信を行う場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="9e064-121">There is nothing that Lync administrators or Lync end-users need to do to maintain continuity of service, and management of this capability within Lync remains the same as it has been for communications with Messenger.</span></span> 

<span data-ttu-id="9e064-122">Messenger ユーザーが Microsoft アカウント (つまり、Messenger に使用されるのと同じ資格情報) を使って Skype にサインインしたときに、Lync のフェデレーションを含むすべての Messenger の連絡先が表示されます。 Skype に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="9e064-122">When Messenger users sign into Skype using their Microsoft accounts (i.e., the same credentials used for Messenger) all of their Messenger contacts - including federated Lync contacts - follow them into Skype.</span></span> <span data-ttu-id="9e064-123">この連絡先の Skype と Lync 間のプレゼンス共有とインスタントメッセージ (im) は、ご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="9e064-123">Presence sharing and instant messaging between Skype and Lync for these contacts is available.</span></span> 

<span data-ttu-id="9e064-124">Lync-Skype 接続-連絡先の追加、プレゼンスの共有、インスタントメッセージング、および Lync と Skype ユーザー間の音声通話は、すべての Lync ユーザーが利用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9e064-124">Lync-Skype connectivity - contact adding, presence sharing, instant messaging, and audio calling between Lync and Skype users - is also now available to all Lync customers.</span></span>

</div>

<div>

## <a name="yahoo-and-aol-instant-messenger"></a><span data-ttu-id="9e064-125">!\!</span><span class="sxs-lookup"><span data-stu-id="9e064-125">Yahoo\!</span></span> <span data-ttu-id="9e064-126">AOL のインスタントメッセンジャー</span><span class="sxs-lookup"><span data-stu-id="9e064-126">and AOL Instant Messenger</span></span>

<span data-ttu-id="9e064-127">Yahoo とのフェデレーション\!</span><span class="sxs-lookup"><span data-stu-id="9e064-127">Federation with Yahoo\!</span></span> <span data-ttu-id="9e064-128">また、AOL は、Lync (および Office Communications Server) のお客様にとって、エンドツーエンドのパスにあります。</span><span class="sxs-lookup"><span data-stu-id="9e064-128">and AOL are both on a path toward end-of-life for customers of Lync (and Office Communications Server).</span></span> <span data-ttu-id="9e064-129">これらの各サービスを提供するための Microsoft の機能は、Yahoo のサポートによって異なります。\!</span><span class="sxs-lookup"><span data-stu-id="9e064-129">Microsoft’s ability to provide each of these services has been contingent upon support from Yahoo\!</span></span> <span data-ttu-id="9e064-130">および AOL では、これらの契約の基になっています。</span><span class="sxs-lookup"><span data-stu-id="9e064-130">and AOL, and the underlying agreements of these are winding down.</span></span> <span data-ttu-id="9e064-131">両方の Yahoo の場合\!</span><span class="sxs-lookup"><span data-stu-id="9e064-131">For both Yahoo\!</span></span> <span data-ttu-id="9e064-132">また AOL は、2014年6月に引き続きご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="9e064-132">and AOL, service will continue through June 2014.</span></span>

  - <span data-ttu-id="9e064-133">**Yahoo** -サービスは2014年6月に継続され、お客様は引き続き Microsoft LYNC パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") でライセンスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e064-133">**Yahoo** - Service will continue through June 2014, and customers continue to need to be licensed with the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”).</span></span>  <span data-ttu-id="9e064-134">2012年9月1日時点で、PIC USL は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="9e064-134">As of September 1st, 2012, the PIC USL, is no longer available for purchase for new or renewing agreements.</span></span>  <span data-ttu-id="9e064-135">この日付より前に購入したライセンスをお持ちのお客様は、引き続き Yahoo とのフェデレーションを行うことができます。\!</span><span class="sxs-lookup"><span data-stu-id="9e064-135">Customers with licenses purchased prior to this date will be able to continue to federate with Yahoo\!</span></span> <span data-ttu-id="9e064-136">サービス終了日またはライセンスの有効期限が切れるまでの間。</span><span class="sxs-lookup"><span data-stu-id="9e064-136">until the earlier of the service shut down date or their license expiration.</span></span> <span data-ttu-id="9e064-137">Lync チームブログの [お知らせ](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e064-137">Read [the announcement](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) on the Lync Team Blog.</span></span> <span data-ttu-id="9e064-138">2014年6月30日以降の契約について、お客様は、2014年6月30日以降の期間における支払い金額に応じてクレジットを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="9e064-138">Customers who have PIC licenses on agreements that extend past June 30, 2014 will receive a credit in proportion to the amount of the payments covering the time period following June 30, 2014.</span></span>

  - <span data-ttu-id="9e064-139">**AOL** -2014 年6月30日に、LYNC の IM 接続 ("PIC") サービスは利用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="9e064-139">**AOL** - On June 30, 2014, Lync's IM connectivity ("PIC") service will no longer be available.</span></span> <span data-ttu-id="9e064-140">サービス終了時に顧客の中断を抑えるため、お客様の追加のドメインのプロビジョニングは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="9e064-140">In order to limit customer disruption when the service ends, we have discontinued the provisioning of additional customer domains.</span></span> <span data-ttu-id="9e064-141">2014年6月30日まで、お客様はターゲットとのフェデレーションコミュニケーションを引き続きサポートするために何もする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9e064-141">Until June 30, 2014, customers do not need to do anything to continue to support federated communications with AIM.</span></span> <span data-ttu-id="9e064-142">この日付 (またはその間に追加のドメインをプロビジョニングしたいお客様向け) には、AOL から直接代替サービスを利用できます。</span><span class="sxs-lookup"><span data-stu-id="9e064-142">Beyond this date (or for customers that would like to provision additional domains in the meantime), a substitute service is available directly from AOL.</span></span> <span data-ttu-id="9e064-143">AOL の新しいサービスの詳細については、「 [AIM と直接フェデレーションを確立](http://aimenterprise.aol.com/pic.php)  する (AOL.com で新しいページを開く)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e064-143">For more information on AOL's new service, see [Establishing Direct Federation with AIM](http://aimenterprise.aol.com/pic.php)  (opens new page on AOL.com).</span></span>  

</div>

<div>

## <a name="public-im-provider-summary"></a><span data-ttu-id="9e064-144">パブリック IM プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="9e064-144">Public IM Provider Summary</span></span>

<span data-ttu-id="9e064-145">次の表では、パブリック IM サービスプロバイダーの概要、Lync とのフェデレーション機能、およびライセンスの要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e064-145">The following table provides a summary of the Public IM service providers, federation capabilities with Lync, and licensing requirements.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e064-146">パブリック IM サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="9e064-146">Public IM Service Provider</span></span></th>
<th><span data-ttu-id="9e064-147">フェデレーション機能</span><span class="sxs-lookup"><span data-stu-id="9e064-147">Federated Capabilities</span></span></th>
<th><span data-ttu-id="9e064-148">ライセンス要件</span><span class="sxs-lookup"><span data-stu-id="9e064-148">Licensing Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e064-149">Skype</span><span class="sxs-lookup"><span data-stu-id="9e064-149">Skype</span></span></p></td>
<td><p><span data-ttu-id="9e064-150">IM、プレゼンス、音声</span><span class="sxs-lookup"><span data-stu-id="9e064-150">IM, Presence, Audio</span></span></p></td>
<td><p><span data-ttu-id="9e064-151">Lync Server クライアントアクセスライセンス、Lync Online Plan 1/2/3</span><span class="sxs-lookup"><span data-stu-id="9e064-151">Lync Server Client Access Licenses, Lync Online Plan 1/2/3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e064-152">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9e064-152">Windows Live Messenger</span></span></p></td>
<td><p><span data-ttu-id="9e064-153">IM、プレゼンス、音声/ビデオ</span><span class="sxs-lookup"><span data-stu-id="9e064-153">IM, Presence, Audio/Video</span></span></p></td>
<td><p><span data-ttu-id="9e064-154">Lync Server クライアントアクセスライセンス (WLM が市場にある限りサポートされます)</span><span class="sxs-lookup"><span data-stu-id="9e064-154">Lync Server Client Access Licenses (supported as long as WLM is in market)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e064-155">AOL</span><span class="sxs-lookup"><span data-stu-id="9e064-155">AOL</span></span></p></td>
<td><p><span data-ttu-id="9e064-156">IM、プレゼンス</span><span class="sxs-lookup"><span data-stu-id="9e064-156">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="9e064-157">Lync Server クライアントアクセスライセンス既存のお客様は、2014年6月にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9e064-157">Lync Server Client Access Licenses; supported through June 2014 for existing customers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e064-158">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9e064-158">Yahoo!</span></span></p></td>
<td><p><span data-ttu-id="9e064-159">IM、プレゼンス</span><span class="sxs-lookup"><span data-stu-id="9e064-159">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="9e064-160">Lync Server クライアントアクセスライセンスに加えて、追加の Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") が必要です。</span><span class="sxs-lookup"><span data-stu-id="9e064-160">Requires additional Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) in addition to Lync Server Client Access Licences.</span></span> <span data-ttu-id="9e064-161">2012年9月の価格表の時点では、PIC USL は購入できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="9e064-161">As of the September 2012 Price List, the PIC USL is no longer available for purchase.</span></span> <span data-ttu-id="9e064-162">アクティブなライセンスを持つユーザーは Yahoo! とのフェデレーションを続行できる</span><span class="sxs-lookup"><span data-stu-id="9e064-162">Customers with active licenses are able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9e064-163">2014年6月30日にサービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="9e064-163">Messenger until the service shut down date on June 30, 2014.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9e064-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e064-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

