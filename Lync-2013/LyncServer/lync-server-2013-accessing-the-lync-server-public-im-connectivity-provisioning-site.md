---
title: Lync Server パブリック IM 接続プロビジョニング サイトへのアクセス
description: Lync Server パブリック IM 接続プロビジョニングサイトへのアクセス。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing the Lync Server public IM connectivity provisioning site
ms:assetid: 77a08234-6bcf-4f59-b43b-ee5fc1926585
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440174(v=OCS.15)
ms:contentKeyID: 57793364
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e12916b12de1ef3a3f990c6bee54c312ba6c1992
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398049"
---
# <a name="accessing-the-lync-server-public-im-connectivity-provisioning-site-from-lync-server-2013"></a><span data-ttu-id="4cff5-103">Lync Server 2013 から Lync Server パブリック IM 接続プロビジョニング サイトへのアクセス</span><span class="sxs-lookup"><span data-stu-id="4cff5-103">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cff5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cff5-104">

<span> </span></span></span>

<span data-ttu-id="4cff5-105">_**最終更新日:** 2019-03-22_</span><span class="sxs-lookup"><span data-stu-id="4cff5-105">_**Topic Last Modified:** 2019-03-22_</span></span>

<span data-ttu-id="4cff5-106">以前の PIC プロビジョニング方法と比較して、Lync-Skype 接続のプロビジョニング処理が変更されています。</span><span class="sxs-lookup"><span data-stu-id="4cff5-106">The provisioning process for Lync-Skype connectivity has changed, as compared to previous PIC provisioning methods.</span></span> <span data-ttu-id="4cff5-107">このプロビジョニングプロセスは、完了までに最大で30日間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-107">This provisioning process can take up to thirty days to complete.</span></span> <span data-ttu-id="4cff5-108">Microsoft は、このドキュメントの残りの手順を完了する前に、このプロセスを先に開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4cff5-108">We recommend that you start this process first, prior to completing the remaining steps in this document.</span></span> <span data-ttu-id="4cff5-109">アカウントの Lync-Skype プロビジョニングプロセスが完了すると、アカウントがアクティブ化され、有効なユーザーにパブリック IM 接続が有効になります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-109">After the Lync-Skype provisioning process is completed for your account, the account is activated and your eligible users are enabled for public IM connectivity.</span></span>

### <a name="to-provision-lync-skype-connectivity-you-need-the-following-information"></a><span data-ttu-id="4cff5-110">Lync-Skype 接続をプロビジョニングするには、次の情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="4cff5-110">To provision Lync-Skype connectivity, you need the following information:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="4cff5-111">Microsoft 契約番号</span><span class="sxs-lookup"><span data-stu-id="4cff5-111">Microsoft Agreement Number</span></span></p></li>
<li><p><span data-ttu-id="4cff5-112">アクセス エッジ サービスの完全修飾ドメイン名 (FQDN)</span><span class="sxs-lookup"><span data-stu-id="4cff5-112">Access Edge service fully qualified domain name (FQDN)</span></span></p></li>
<li><p><span data-ttu-id="4cff5-113">セッション開始プロトコル (SIP) のドメイン</span><span class="sxs-lookup"><span data-stu-id="4cff5-113">Session Initiation Protocol (SIP) domain(s)</span></span></p></li>
<li><p><span data-ttu-id="4cff5-114">追加のアクセス エッジ サービスの FQDN</span><span class="sxs-lookup"><span data-stu-id="4cff5-114">Any additional Access Edge service FQDNs</span></span></p></li>
<li><p><span data-ttu-id="4cff5-115">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="4cff5-115">Contact information</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4cff5-116">2019年4月以降、pic.lync.com の web サイトから Skype フェデレーションを提供されているお客様の連絡先情報の収集と保持を停止します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-116">Beginning in April 2019, we will stop the collection and retention of contact information for customers who are provisioned for Skype Federation via the pic.lync.com website.</span></span> <span data-ttu-id="4cff5-117">この変更は、pic.lync.com プロビジョニングシステムが Microsoft のプライバシーポリシーに準拠していることを確認するために行われています。</span><span class="sxs-lookup"><span data-stu-id="4cff5-117">This change is being made to ensure that the pic.lync.com provisioning system adheres to Microsoft privacy policies.</span></span> 

<span data-ttu-id="4cff5-118">この変更が有効になった後は、保留中のプロビジョニングの変更でメールの更新を提供することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-118">Once this change goes live, we will no longer be able to provide email updates on pending provisioning changes.</span></span> <span data-ttu-id="4cff5-119">PIC プロビジョニングの変更は、通常、入力後の24-48 時間以内に完了します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-119">PIC provisioning changes typically complete within 24-48 hours after being entered.</span></span> <span data-ttu-id="4cff5-120">引き続き Skype フェデレーションの問題が発生した場合は、プロビジョニングリクエストの送信後に48時間がかかる場合は、Microsoft テクニカルサポートに協力して、さらに詳しく調査してください。</span><span class="sxs-lookup"><span data-stu-id="4cff5-120">If you are still experiencing Skype Federation issues 48 hours after submitting a provisioning request, please engage Microsoft Technical Support to investigate further.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cff5-121">この変更の一環として、以前に入力したすべての連絡先情報は、2019年4月のによってシステムから削除されます。</span><span class="sxs-lookup"><span data-stu-id="4cff5-121">As part of this change, all previously entered contact information will be purged from our system by the end of April, 2019.</span></span>

### <a name="to-initiate-the-provisioning-process-for-lync-skype-connectivity"></a><span data-ttu-id="4cff5-122">Lync-Skype 接続のプロビジョニングプロセスを開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-122">To initiate the provisioning process for Lync-Skype connectivity:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="4cff5-123"><strong>https://pic.lync.com</strong>Microsoft Windows LIVE ID を使用して、web サイトにサインインします。</span><span class="sxs-lookup"><span data-stu-id="4cff5-123">Sign in to the website, <strong>https://pic.lync.com</strong>, using your Microsoft Windows Live ID.</span></span></p></li>
<li><p><span data-ttu-id="4cff5-124">Microsoft ライセンスの契約の種類を選びます。</span><span class="sxs-lookup"><span data-stu-id="4cff5-124">Select the Microsoft licensing agreement type.</span></span></p></li>
<li><p><span data-ttu-id="4cff5-125">このチェックボックスをオンにして、Lync Server の製品使用権限を読み、同意していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-125">Select the check box, verifying that you have read and accept the Product Use Rights for Lync Server.</span></span></p></li>
<li><p><span data-ttu-id="4cff5-126">[ <strong>プロビジョニング要求の開始</strong> ] ページで、適切なリンクをクリックしてプロビジョニング要求を開始します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-126">On the <strong>Initiate a Provisioning Request</strong> page, click the appropriate link to initiate a provisioning request:</span></span></p></li>
<li><p><span data-ttu-id="4cff5-127">[ <strong>プロビジョニング情報の指定</strong> ] ページで、 <strong>アクセスエッジサービスの FQDN</strong>を入力します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-127">On the <strong>Specify Provisioning Information</strong> page, enter the <strong>Access Edge service FQDN</strong>.</span></span> <span data-ttu-id="4cff5-128">たとえば、 <strong>sip.contoso.com</strong>のようになります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-128">For example, <strong>sip.contoso.com</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="4cff5-129">2017年7月1日以降、お客様には、引き続き機能するために、Microsoft がパブリック IM 接続用に展開されたフェデレーション DNS SRV レコードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-129">After July 1st, 2017 Microsoft will additionally require customers have the Federation DNS SRV record deployed for Public IM connectivity to continue to work.</span></span>

</li>
<li><p><span data-ttu-id="4cff5-130">少なくとも1つ以上の SIP ドメイン名を入力して、「 <strong>追加</strong>」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4cff5-130">Enter at least one or more SIP domain names, and then click <strong>Add</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="4cff5-131">プロビジョニング処理を完了するには、少なくとも1つのアクセスエッジサーバーと1つの SIP ドメインが必要です。</span><span class="sxs-lookup"><span data-stu-id="4cff5-131">At least one Access Edge server and one SIP domain are required to complete the provisioning process.</span></span> <span data-ttu-id="4cff5-132">SIP ドメインとアクセス エッジ サーバーは、アクティブで、正常に機能し、ネットワーク上で到達可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-132">The SIP domain and the Access Edge server must be active, functioning, and reachable on the network.</span></span>

</li>
<li><p><span data-ttu-id="4cff5-133"><strong>パブリック IM サービスプロバイダ</strong>のリストで、「 <strong>Skype</strong> 」を選択し、「<strong>次</strong>へ」をクリックして連絡先情報を追加し、プロビジョニングリクエストを送信します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-133">In the list of <strong>Public IM Service providers</strong>, select <strong>Skype,</strong> and click <strong>Next</strong> to add contact information, and submit the provisioning request.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4cff5-134">プロビジョニング要求が送信されると、アカウントがアクティブ化され、ユーザーがパブリック IM 接続を有効にするまでに最長で30日間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-134">After the provisioning request has been submitted, it can take up to 30 days for the account to activate and for users to be enabled for public IM connectivity.</span></span>

<div>

## <a name="enabling-federation-and-public-im-connectivity-pic"></a><span data-ttu-id="4cff5-135">フェデレーションとパブリック IM 接続 (PIC) の有効化</span><span class="sxs-lookup"><span data-stu-id="4cff5-135">Enabling Federation and Public IM Connectivity (PIC)</span></span>

<span data-ttu-id="4cff5-136">プロビジョニング要求を送信した後は、Lync Server 環境と、Lync-Skype 接続を構成するために必要な管理タスクに集中することができます。</span><span class="sxs-lookup"><span data-stu-id="4cff5-136">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="4cff5-137">このセクションでは、Lync Server の管理者が Lync Server を展開し、外部アクセスを構成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="4cff5-137">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="4cff5-138">Lync Server の外部アクセスの構成の詳細については、「」および「外部ユーザーアクセスの計画」を参照してください [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378) 。</span><span class="sxs-lookup"><span data-stu-id="4cff5-138">For additional information on configuring external access for Lync Server, see "Planning for External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) and "Deploying External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378).</span></span>

<span data-ttu-id="4cff5-139">Lync server の環境を Lync-Skype 接続用に準備するには、Lync Server の管理者が次の3つのタスクを実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-139">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="4cff5-140">1 \.</span><span class="sxs-lookup"><span data-stu-id="4cff5-140">1\.</span></span> <span data-ttu-id="4cff5-141">フェデレーションと PIC を構成する</span><span class="sxs-lookup"><span data-stu-id="4cff5-141">Configure Federation and PIC</span></span>

<span data-ttu-id="4cff5-142">組織内の Lync ユーザーと Skype ユーザーとの通信を可能にするには、フェデレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="4cff5-142">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="4cff5-143">パブリックインスタントメッセージング接続 (PIC) はフェデレーションのクラスであり、Lync ユーザーが Skype ユーザーと通信できるように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-143">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="4cff5-144">フェデレーションと PIC は、次に示す Lync Server コントロールパネルを使用して構成されています。</span><span class="sxs-lookup"><span data-stu-id="4cff5-144">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="4cff5-145">PIC フェデレーションは、Live Communication Server 2005 SP1 または Office Communications Server 2007 ではサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4cff5-145">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="4cff5-146">PIC フェデレーションでサポートされているプラットフォームには、Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2 があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-146">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="4cff5-147">2 \.</span><span class="sxs-lookup"><span data-stu-id="4cff5-147">2\.</span></span> <span data-ttu-id="4cff5-148">フェデレーション ユーザーのアクセスをサポートするように、少なくとも 1 つのポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="4cff5-148">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="4cff5-149">Lync Server コントロールパネルを使用して、管理者は、1つ以上の外部ユーザーアクセスポリシーを構成して、Skype ユーザーが社内の Lync Server ユーザーと共同作業できるかどうかを制御する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-149">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="4cff5-150">3 \.</span><span class="sxs-lookup"><span data-stu-id="4cff5-150">3\.</span></span> <span data-ttu-id="4cff5-151">Lync の Skype PIC プロバイダー設定を構成する</span><span class="sxs-lookup"><span data-stu-id="4cff5-151">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="4cff5-152">Lync Server 管理シェルを使用する場合、管理者は Lync クライアントポリシーを構成して、Skype を追加の PIC プロバイダーとして表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-152">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4cff5-153">また、管理者が少なくとも 1 つのポリシー (この手続きの手順 2.) を構成してパブリック IM 接続をサポートするまでは、パブリック インスタント メッセージング接続 (PIC) サービス プロバイダーのユーザーは組織の IM や会議に参加できません。</span><span class="sxs-lookup"><span data-stu-id="4cff5-153">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span><BR><span data-ttu-id="4cff5-154">フェデレーションと PIC を構成するには、で「フェデレーションとパブリック IM 接続を有効または無効にする」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A> 。</span><span class="sxs-lookup"><span data-stu-id="4cff5-154">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A>.</span></span><BR><span data-ttu-id="4cff5-155">フェデレーションされたユーザーアクセスをサポートするために、少なくとも1つのポリシーを構成するには、「パブリックユーザーアクセスを制御するためのポリシーの構成」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A> 。</span><span class="sxs-lookup"><span data-stu-id="4cff5-155">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A>.</span></span>



</div>

1.  <span data-ttu-id="4cff5-156">Lync Server フロントエンドサーバーから、Lync Server 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4cff5-156">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="4cff5-157">次の 2 つのコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-157">Run the following two commands:</span></span>
    
      - `Remove-CsPublicProvider -Identity <identity-name>`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="4cff5-158">環境に PIC プロバイダーがなく、新しい PIC プロバイダーを作成している場合は、 <STRONG>CsPublicProvider</STRONG> コマンドレットを実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4cff5-158">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

        
        </div>
    
      - `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="4cff5-159">Lync Server 2013 CU5 以降 &amp; lync デスクトップクライアントに Office 2013 SP1 で追加されました。 lync ユーザーが skype の連絡先を追加するには、Microsoft 以外のドメインを "装飾" して、skype (ユーザー (contoso) @msn の形式であることを確認し、ルーティングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-159">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="4cff5-160">こうした新しい設定により、ユーザーが [Skype 連絡先の追加] ダイアログ ボックスに入力したアドレスに NameDecorationExcludedDomainList のドメイン (現在は msn.com、live.com、Hotmail.com、outlook.com に対応できます) が含まれない場合は、このアドレスの NameDecorationRoutingDomain による自動書式設定 (msn.com に設定する必要があります) が可能になります。</span><span class="sxs-lookup"><span data-stu-id="4cff5-160">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

        
        </div>

3.  <span data-ttu-id="4cff5-161">Lync クライアントから、PIC プロバイダとして Skype を選択できるようになりました。 Skype クライアントを追加するには、お客様の Microsoft アカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-161">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="4cff5-162">さらに、Microsoft アカウントで統合してログインした Skype ユーザーは、連絡先要求を Lync ユーザーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="4cff5-162">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="4cff5-163">Microsoft アカウントの詳細については、「 [microsoft アカウントとは](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cff5-163">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="4cff5-164">Lync にクライアントを追加する方法の詳細については、「 [Lync Server 2013 でのエンドユーザーとしての Lync-Skype 接続の使用](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cff5-164">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>

4.  <span data-ttu-id="4cff5-165">ホストされているプロバイダーの変更の詳細については、の「ホステッド SIP フェデレーションプロバイダーを作成または編集する」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) 。</span><span class="sxs-lookup"><span data-stu-id="4cff5-165">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="4cff5-166">これで、サーバー上で実行する必要がある管理タスクが完了します。</span><span class="sxs-lookup"><span data-stu-id="4cff5-166">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="4cff5-167">これで Lync-Skype 接続が設定されました。</span><span class="sxs-lookup"><span data-stu-id="4cff5-167">You are now set up for Lync-Skype connectivity.</span></span>

</div>

</div>

<div>

## <a name="additional-resources"></a><span data-ttu-id="4cff5-168">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4cff5-168">Additional Resources</span></span>

[<span data-ttu-id="4cff5-169">エンド ユーザーとしての Lync Server 2013 での Lync と Skype の接続の使用</span><span class="sxs-lookup"><span data-stu-id="4cff5-169">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

[<span data-ttu-id="4cff5-170">Lync Server 2013 での Lync と Skype の接続のプロビジョニング ガイド</span><span class="sxs-lookup"><span data-stu-id="4cff5-170">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

<span data-ttu-id="4cff5-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cff5-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

