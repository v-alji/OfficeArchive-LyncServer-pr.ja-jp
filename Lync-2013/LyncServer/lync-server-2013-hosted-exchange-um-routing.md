---
title: 'Lync Server 2013: Hosted Exchange UM のルーティング'
description: 'Lync Server 2013: ホストされている Exchange UM ルーティング。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM routing
ms:assetid: 6c90dc8b-6aef-4ce8-b483-37c7b5a553c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398512(v=OCS.15)
ms:contentKeyID: 48184422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72fbdee5550ae53d5ff5e7513ea384cedad62c5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427595"
---
# <a name="hosted-exchange-um-routing-in-lync-server-2013"></a><span data-ttu-id="3dfae-103">Lync Server 2013 Hosted Exchange UM のルーティング</span><span class="sxs-lookup"><span data-stu-id="3dfae-103">Hosted Exchange UM routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3dfae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3dfae-104">

<span> </span></span></span>

<span data-ttu-id="3dfae-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="3dfae-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="3dfae-106">Exchange UM ルーティングアプリケーションは、オンプレミスの Microsoft Exchange Server ユニファイドメッセージング (UM) 展開またはホストされた Exchange UM サービスのいずれかに、通話をルーティングするために、フロントエンドサーバー上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-106">The Exchange UM Routing application runs on the Front End Server to route calls, either to an on-premises Microsoft Exchange Server Unified Messaging (UM) deployment or to hosted Exchange UM service.</span></span>

<div>

## <a name="the-exum-routing-application"></a><span data-ttu-id="3dfae-107">ExUM ルーティングアプリケーション</span><span class="sxs-lookup"><span data-stu-id="3dfae-107">The ExUM Routing Application</span></span>

<span data-ttu-id="3dfae-108">Lync Server 2013 Exchange UM ルーティングアプリケーションでは、次の図に示すように、ユーザーアカウントの設定とホストされたボイスメールポリシーのパラメーターから情報を使って、ホストされている音声メッセージの着信をルーティングする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="3dfae-108">The Lync Server 2013 Exchange UM Routing application uses information from user account settings and from hosted voice mail policy parameters to determine how to route calls for hosted voice messaging, as shown in the following diagram.</span></span>

<span data-ttu-id="3dfae-109">**混在展開の Exchange UM ルーティングの例**</span><span class="sxs-lookup"><span data-stu-id="3dfae-109">**Example of mixed deployment Exchange UM routing**</span></span>

<span data-ttu-id="3dfae-110">![オンプレミスの Lync Server Exchange UM の展開](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "オンプレミスの Lync Server Exchange UM の展開")</span><span class="sxs-lookup"><span data-stu-id="3dfae-110">![On-premises Lync Server Exchange UM deployment](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "On-premises Lync Server Exchange UM deployment")</span></span>

<span data-ttu-id="3dfae-111">Exchange UM ルーティングは、オンプレミスの Exchange UM を有効にしているユーザー、またはホストされている Exchange UM を有効にしているユーザー、またはこの2つの組み合わせに対して、着信をルーティングするように構成できます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-111">Exchange UM routing can be configured to route calls to users who are enabled for on-premises Exchange UM, to users who are enabled for hosted Exchange UM, or to a combination of the two.</span></span>

<span data-ttu-id="3dfae-112">たとえば、Roy のメールボックスと Exchange UM サービスがオンプレミスの Exchange 展開のホームにあるとします。</span><span class="sxs-lookup"><span data-stu-id="3dfae-112">For example, suppose that Roy’s mailbox and Exchange UM service are homed in an on-premises Exchange deployment.</span></span>

  - <span data-ttu-id="3dfae-113">Roy のユーザーアカウントからのプロキシアドレス情報は、ExUM ルーティングアプリケーションがオンプレミスの Exchange UM サーバーへの呼び出しをルーティングするために使用する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3dfae-113">The proxy address information from Roy’s user account provides the information that the ExUM Routing application uses to route his calls to an on-premises Exchange UM server.</span></span>

<span data-ttu-id="3dfae-114">アリスのメールボックスと Exchange UM サービスは、ホスティングされている Exchange サービスプロバイダーのデータセンターにあります。</span><span class="sxs-lookup"><span data-stu-id="3dfae-114">Alice’s mailbox and Exchange UM service are located at a hosted Exchange service provider’s data center.</span></span> <span data-ttu-id="3dfae-115">Exchange UM の呼び出しに対するルーティングは、次のように構成されます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-115">Routing for her Exchange UM calls is configured as follows:</span></span>

  - <span data-ttu-id="3dfae-116">Alice のユーザーアカウントの msExchUCVoiceMailSettings 属性で設定された値は、ExUM ルーティングアプリケーションに対して、ホストされたボイスメールポリシーでルーティングの詳細を確認するように指示します。</span><span class="sxs-lookup"><span data-stu-id="3dfae-116">The values set in the msExchUCVoiceMailSettings attribute of Alice’s user account tell the ExUM Routing application to check for routing details in a hosted voice mail policy.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3dfae-117">MsExchUCVoiceMailSettings 属性の値は、Exchange サービスプロバイダーまたは Lync Server 2013 管理者のいずれかで設定できます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-117">The value of the msExchUCVoiceMailSettings attribute can be set by either the Exchange service provider or the Lync Server 2013 administrator.</span></span> <span data-ttu-id="3dfae-118">上の図の例では、Lync Server 2013 管理者によって、ホストされたボイスメールを有効にするように値 (CsHostedVoiceMail = 1) が設定されていました。</span><span class="sxs-lookup"><span data-stu-id="3dfae-118">In the example shown in the preceding diagram, the value (CsHostedVoiceMail=1) was set by the Lync Server 2013 administrator to enable hosted voice mail for Alice.</span></span> <span data-ttu-id="3dfae-119">この属性の詳細については、「 <A href="lync-server-2013-hosted-exchange-user-management.md">Lync Server 2013 でのホスト型 Exchange ユーザーの管理</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dfae-119">For details about this attribute, see <A href="lync-server-2013-hosted-exchange-user-management.md">Hosted Exchange user management in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="3dfae-120">Alice のユーザーアカウントに割り当てられているホスト型ボイスメールのポリシーによって、ルーティングの詳細が提供されます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-120">The hosted voice mail policy that is assigned to Alice’s user account provides routing details:</span></span>
    
      - <span data-ttu-id="3dfae-121">[Destination] は、ホストされている Exchange UM サービスプロバイダーです (ls)。ExUm. \<hostedExchangeServer\> ..この例では com を使用します)。</span><span class="sxs-lookup"><span data-stu-id="3dfae-121">Destination is the hosted Exchange UM service provider (ls.ExUm.\<hostedExchangeServer\>.com in this example).</span></span>
    
      - <span data-ttu-id="3dfae-122">組織は、ls に配置されている Exchange Server テナントの SIP メッセージのルーティング Fqdn であるテナント Id によって識別されます。ExUm. \<hostedExchangeServer\> ..com (この例では corp.contoso.com と corp.litwareinc.com)。</span><span class="sxs-lookup"><span data-stu-id="3dfae-122">Organizations are identified by the tenant IDs, which are the routing FQDNs for SIP messages for Exchange Server tenants that are located on ls.ExUm.\<hostedExchangeServer\>.com (corp.contoso.com and corp.litwareinc.com in this example).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3dfae-123">Exchange Online の FQDN は exap.um.outlook.com です。</span><span class="sxs-lookup"><span data-stu-id="3dfae-123">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

        
        </div>
        
        <span data-ttu-id="3dfae-124">詳細については、「 [Lync Server 2013 のホスト型ボイスメールポリシー](lync-server-2013-hosted-voice-mail-policies.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dfae-124">For details, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3dfae-125">ユーザーアカウントに msExchUCVoiceMailSettings 属性と UM プロキシアドレスの両方の設定が含まれている場合は、msExchUCVoiceMailSettings 属性が優先されます。</span><span class="sxs-lookup"><span data-stu-id="3dfae-125">If both the msExchUCVoiceMailSettings attribute and the UM proxy address settings are present in a user account, the msExchUCVoiceMailSettings attribute takes precedence.</span></span>



<span data-ttu-id="3dfae-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3dfae-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

