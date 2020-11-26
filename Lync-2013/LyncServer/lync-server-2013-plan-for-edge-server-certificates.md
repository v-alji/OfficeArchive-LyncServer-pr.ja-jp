---
title: 'Lync Server 2013: エッジ サーバー証明書を計画する'
description: 'Lync Server 2013: エッジサーバー証明書の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Plan for Edge Server certificates
ms:assetid: f1dfe220-2398-4ac8-ba4c-206c8c0cbc50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413010(v=OCS.15)
ms:contentKeyID: 48185798
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22ec3743256fe3e4c55dba0f6357a85b1ad81cd0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437135"
---
# <a name="plan-for-edge-server-certificates-in-lync-server-2013"></a><span data-ttu-id="63919-103">Lync Server 2013 でエッジ サーバー証明書を計画する</span><span class="sxs-lookup"><span data-stu-id="63919-103">Plan for Edge Server certificates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63919-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63919-104">

<span> </span></span></span>

<span data-ttu-id="63919-105">_**最終更新日:** 2012-11-05_</span><span class="sxs-lookup"><span data-stu-id="63919-105">_**Topic Last Modified:** 2012-11-05_</span></span>

<span data-ttu-id="63919-106">Lync Server 2013 で、Edge 用の証明書の作成が簡略化されています。</span><span class="sxs-lookup"><span data-stu-id="63919-106">Certificate creation for Edge is simplified in Lync Server 2013.</span></span>

<span data-ttu-id="63919-107">**エッジ サーバー用の証明書のフロー チャート**</span><span class="sxs-lookup"><span data-stu-id="63919-107">**Certificates Flow Chart for Edge Server**</span></span>

<span data-ttu-id="63919-108">![4364 a5fc20db-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "4364 a5fc20db-b577-6a709a8367cd")</span><span class="sxs-lookup"><span data-stu-id="63919-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span></span>

<span data-ttu-id="63919-109">1つの公開証明書を作成して、証明書に対して定義されたエクスポート可能な秘密キーがあることを確認し、証明書ウィザードを使用して、次のエッジサーバーの外部インターフェイスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63919-109">Create a single public certificate, ensure that you have an exportable private key defined for the certificate, and assign it to the following Edge Server external interfaces using the certificate wizard:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="63919-110">Lync Server では、ワイルドカード証明書はサポートされていません。リバースプロキシを介して単純な Url を要約するために使用された場所を除きます。</span><span class="sxs-lookup"><span data-stu-id="63919-110">Wildcard certificates are not supported in Lync Server, except where used to summarize the Simple URLs through the reverse proxy.</span></span> <span data-ttu-id="63919-111">各 SIP ドメイン名、Web 会議エッジサービス、A/V Edge サービス、および展開によって提供される XMPP ドメインに対して、個別のサブジェクト代替名 (San) を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63919-111">You must define distinct subject alternate names (SANs) for each SIP domain name, Web Conferencing Edge service, A/V Edge service and XMPP domain offered by your deployment.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="63919-112">Lync Server 2013 で導入されました。現在の証明書の有効期限が切れる前に、オーディオ/ビデオ認証の証明書をステージングするには、追加の計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="63919-112">Introduced in Lync Server 2013, staging Audio/Video Authentication certificates in advance of the expiration time of the current certificate requires some additional planning.</span></span> <span data-ttu-id="63919-113">外部 Edge インターフェイスの複数の目的を持つ1つの証明書の代わりに、アクセスエッジサービスと Web 会議エッジサービスに割り当てられている証明書と、A/V Edge サービス用の証明書の2つが必要です。</span><span class="sxs-lookup"><span data-stu-id="63919-113">Instead of one certificate with multiple purposes for the external Edge interface, you will require two certificates, one assigned to the Access Edge service and Web Conferencing Edge service, and one certificate for the A/V Edge service.</span></span> <span data-ttu-id="63919-114">詳細については、「 <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Lync Server 2013 での、AV および OAuth 証明書の使用</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63919-114">For additional details, see <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</A></span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="63919-115">エッジサーバーのプールがある場合は、各エッジサーバーに秘密キーを持つ証明書をエクスポートし、各エッジサーバーサービスに証明書を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63919-115">In the event of a pool of Edge Servers, you export the certificate with the private key to each Edge Server and assign the certificate to each Edge Server service.</span></span> <span data-ttu-id="63919-116">内部エッジサーバー証明書についても同じ操作を行い、秘密キーを使って証明書をエクスポートし、各内部エッジインターフェイスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63919-116">Do the same for the internal Edge Server certificate, exporting the certificate with the private key and assigning to each internal Edge interface.</span></span>



</div>

  - <span data-ttu-id="63919-117">証明書に対して、エクスポート可能な秘密キーが割り当てられていることを確認する</span><span class="sxs-lookup"><span data-stu-id="63919-117">Ensure that you have an exportable private key assigned for the certificate</span></span>

  - <span data-ttu-id="63919-118">Access Edge サービス (証明書ウィザードの [ **外部 SIP アクセスエッジ** ] とも呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="63919-118">Access Edge service (referred to as **SIP Access Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="63919-119">Web 会議エッジサービス (証明書ウィザードの [ **外部] Web 会議エッジ** とも呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="63919-119">Web Conferencing Edge service (referred to as **Web Conferencing Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="63919-120">A/V 認証サービス (証明書ウィザードの「 **外部** 」とも呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="63919-120">A/V Authentication service (referred to as **A/V Edge External** in the certificate wizard)</span></span>

<span data-ttu-id="63919-121">エクスポート可能な秘密キーを使用して、1つの内部証明書を作成し、エッジサーバーの内部インターフェイスごとにコピーして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63919-121">Create a single internal certificate with exportable private key, copy and assign it to each of the Edge Server internal interfaces:</span></span>

  - <span data-ttu-id="63919-122">エッジサーバー (証明書ウィザードでは、" **edge** " と呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="63919-122">Edge Server (referred to as **Edge Internal** in the certificate wizard)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="63919-123">エッジサーバーサービスごとに個別の証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="63919-123">It is possible to use separate and distinct certificates for each Edge Server service.</span></span> <span data-ttu-id="63919-124">個別の証明書を選択することをお勧めするのは、A/V Edge サービス証明書の新しいローリング証明書機能を使用する場合です。</span><span class="sxs-lookup"><span data-stu-id="63919-124">A good reason to choose separate certificates is if you want to use the new rolling certificate feature for the A/V Edge service certificate.</span></span> <span data-ttu-id="63919-125">この機能を使用する場合は、アクセスエッジサービスおよび Web 会議エッジサービスから A/V Edge サービス証明書を分離することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="63919-125">In the case of this feature, decoupling the A/V Edge service certificate from the Access Edge service and Web Conferencing Edge service is recommended.</span></span> <span data-ttu-id="63919-126">各サービスに対して個別の証明書を取得して割り当てる場合は、秘密キーが A/v Edge サービス用にエクスポート可能であることを要求する必要があります (これは、A/v 認証サービスの場合もあります)。また、同じ証明書を各エッジサーバーの A/V Edge 外部インターフェイスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63919-126">If you choose to request, acquire and assign separate certificates for each service, you must request that the private key be exportable for the A/V Edge service (again, this is in actuality the A/V Authentication service) and assign the same certificate to the A/V Edge External interface on each Edge Server.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="63919-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="63919-127">See Also</span></span>


[<span data-ttu-id="63919-128">Lync Server 2013 での、AV および OAuth 証明書の使用-セットアップ-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="63919-128">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  


[<span data-ttu-id="63919-129">エッジ サーバーの計画に影響する Lync Server 2013 での変更点</span><span class="sxs-lookup"><span data-stu-id="63919-129">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)  
  

<span data-ttu-id="63919-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63919-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

