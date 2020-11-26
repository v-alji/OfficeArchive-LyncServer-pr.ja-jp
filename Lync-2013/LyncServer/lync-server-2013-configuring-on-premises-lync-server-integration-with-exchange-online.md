---
title: Exchange Online とのオンプレミス Lync Server との統合を構成する
description: Exchange Online とのオンプレミス Lync Server との統合を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432836"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="3c3b1-103">オンプレミスの Lync Server 2013 と Exchange Online の統合を構成する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c3b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c3b1-104">

<span> </span></span></span>

<span data-ttu-id="3c3b1-105">_**最終更新日:** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="3c3b1-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="3c3b1-106">オンプレミスの Lync Server 2013 の展開を使用しているユーザーは、ハイブリッド展開モードで Microsoft Exchange Online の Microsoft Outlook Web App との相互運用性を構成できます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="3c3b1-107">相互運用性機能には、シングル サインオンが含まれるほか、Outlook Web App インターフェイスとのインスタント メッセージングおよびプレゼンスの統合が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="3c3b1-108">この統合を有効にするには、次のタスクを実行して、オンプレミスの Lync Server 展開でエッジサーバーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="3c3b1-109">共有 SIP アドレス スペースを構成する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="3c3b1-110">エッジサーバーでホスティングプロバイダーを構成する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="3c3b1-111">更新された中央管理ストアのレプリケーションを確認する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="3c3b1-112">Lync Server 2013 が Exchange Online と統合されている場合、OWA から IM にサインインしようとしているユーザーは、リモートユーザーまたは外部ユーザーと見なされます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="3c3b1-113">このシナリオでは、このユーザーは、次のオプションが選択されている外部アクセスポリシーが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="3c3b1-114">**リモートユーザーとの通信を有効にする**</span><span class="sxs-lookup"><span data-stu-id="3c3b1-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="3c3b1-115">出張中の在宅勤務者やユーザーなど、組織内のユーザーがインターネット経由で Lync Server に接続できるようにする場合は、このオプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="3c3b1-116">詳細については、「 [Lync Server 2013 で外部アクセスポリシーを管理](lync-server-2013-manage-external-access-policy-for-your-organization.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="3c3b1-117">共有 SIP アドレス スペースを構成する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="3c3b1-118">オンプレミスの Lync Server 2013 を Exchange Online と統合するには、共有 SIP アドレス空間を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="3c3b1-119">同じ SIP ドメインアドレス空間は、Lync Server と Exchange Online サービスの両方でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="3c3b1-120">Lync Server 管理シェルを使用して、次の例に示すパラメーターを使用して、 **CSAccessEdgeConfiguration** コマンドレットを実行して、フェデレーション用にエッジサーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="3c3b1-121">**AllowFederatedUsers** は、内部ユーザーとフェデレーション ドメインからのユーザーとの通信を許可するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="3c3b1-122">このプロパティは、内部ユーザーが Lync Server および Exchange Online を使用して、共有 SIP アドレス空間のシナリオでユーザーと通信できるかどうかも決定します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="3c3b1-123">Lync Server 管理シェルの使い方の詳細については、「 [Lync server 2013 管理シェル](lync-server-2013-lync-server-management-shell.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="3c3b1-124">エッジ サーバーにホスティング プロバイダーを構成する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="3c3b1-125">Lync Server 管理シェルを使用して、エッジサーバーでホスティングプロバイダーを構成します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="3c3b1-126">これを行うには、次の例のパラメーターを使用して、 **新しい-CsHostingProvider** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="3c3b1-127">中国の 21Vianet により運営されている Office 365 を使用している場合は、この例の <STRONG>ProxyFqdn</STRONG> パラメーターの値 ("exap.um.outlook.com") を、21Vianet により運営されているサービスの FQDN である "exap.um.partner.outlook.cn" に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="3c3b1-128">**Identity** は、作成するホスティング プロバイダーの、一意の文字列値から成る識別子を指定します (例: "Exchange Online")。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="3c3b1-129">スペースを含む値は二重引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="3c3b1-130">**Enabled** は、ドメインとホスティング プロバイダー間のネットワーク接続が有効になっているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="3c3b1-131">これは **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="3c3b1-132">**EnabledSharedAddressSpace** は、ホスティング プロバイダーが共有 SIP アドレス スペース シナリオで使用されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="3c3b1-133">これは **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="3c3b1-134">**Hostているユーザー** は、ホスティングプロバイダーが Office Communications server または Lync Server をホストするために使用されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="3c3b1-135">この値は **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="3c3b1-136">**ProxyFQDN** は、ホスティング プロバイダーによって使用されるプロキシ サーバーの完全修飾ドメイン名 (FQDN) を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="3c3b1-137">Exchange Online の FQDN は exap.um.outlook.com です。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="3c3b1-138">**Islocal** は、ホスティングプロバイダーによって使用されたプロキシサーバーが Lync server トポロジ内に含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="3c3b1-139">この値は **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="3c3b1-140">**VerificationLevel** は、ホストされているプロバイダーとの間で送受信されるメッセージに対して許可される確認レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="3c3b1-141">Sns の **確認** を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="3c3b1-142">このオプションは、ホスティングプロバイダーから送信されるメッセージに含まれている確認レベルに依存します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="3c3b1-143">このレベルが指定されていない場合、メッセージは、確認不能として拒否されます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="3c3b1-144">更新された中央管理ストアのレプリケーションを確認する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="3c3b1-145">前のセクションのコマンドレットを使用して行った変更は、自動的にエッジサーバーに適用され、複製には1分未満かかります。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="3c3b1-146">次のコマンドレットを使用して、レプリケーションの状態を確認し、変更がエッジサーバーに適用されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="3c3b1-147">Lync Server の展開でサーバー上のレプリケーションの更新を確認するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="3c3b1-148">変更が適用されたことを確認するには、エッジサーバーで次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="3c3b1-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3c3b1-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c3b1-149">See Also</span></span>


[<span data-ttu-id="3c3b1-150">Lync Server 2013 ユーザーに Hosted Exchange UM のボイス メールを提供する</span><span class="sxs-lookup"><span data-stu-id="3c3b1-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="3c3b1-151">Lync Server 2013 の Hosted Exchange ユニファイド メッセージング統合</span><span class="sxs-lookup"><span data-stu-id="3c3b1-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="3c3b1-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c3b1-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
