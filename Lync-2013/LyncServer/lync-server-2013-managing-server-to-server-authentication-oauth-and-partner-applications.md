---
title: サーバー間認証 (OAuth) とパートナーアプリケーションの管理
description: サーバー間認証 (OAuth) とパートナーアプリケーションを管理する。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing server-to-server authentication (OAuth) and partner applications
ms:assetid: 38848373-c8c6-4097-bf7f-699fe471348d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204817(v=OCS.15)
ms:contentKeyID: 48183894
ms.date: 05/15/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6efa413ad1809bcff27373a38334d09a8fbfcad9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437197"
---
# <a name="managing-server-to-server-authentication-oauth-and-partner-applications-in-lync-server-2013"></a><span data-ttu-id="8708c-103">Lync Server 2013 でのサーバー間認証 (OAuth) とパートナーアプリケーションの管理</span><span class="sxs-lookup"><span data-stu-id="8708c-103">Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8708c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8708c-104">

<span> </span></span></span>

<span data-ttu-id="8708c-105">_**最終更新日:** 2015-05-14_</span><span class="sxs-lookup"><span data-stu-id="8708c-105">_**Topic Last Modified:** 2015-05-14_</span></span>

<span data-ttu-id="8708c-106">Microsoft Lync Server 2013 は、安全かつシームレスに、他のアプリケーションやサーバー製品と通信できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-106">Microsoft Lync Server 2013 must be able to securely, and seamlessly, communicate with other applications and server products.</span></span> <span data-ttu-id="8708c-107">たとえば、連絡先データやアーカイブデータが Microsoft Exchange Server 2013 に保存されるように Lync Server 2013 を構成することができます。ただし、これを行うことができるのは、Lync Server と Exchange が相互に安全に通信できる場合のみです。</span><span class="sxs-lookup"><span data-stu-id="8708c-107">For example, you can configure Lync Server 2013 so that contact data and/or archiving data is stored in Microsoft Exchange Server 2013; however, this can only be done if Lync Server and Exchange are able to securely communicate with one another.</span></span> <span data-ttu-id="8708c-108">同様に、Lync Server 会議を Microsoft SharePoint Server 内でスケジュールすることもできます。ただし、この操作は、2台のサーバー (SharePoint と Lync Server) が相互に信頼している場合にのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="8708c-108">Likewise, you can schedule a Lync Server conference from within Microsoft SharePoint Server; again, however, this can only be done if the two servers (SharePoint and Lync Server) trust one another.</span></span> <span data-ttu-id="8708c-109">Lync 間の通信には1つの認証メカニズムを使用できますが、Lync 間の通信には個別のメカニズムを使うこともできますが、より効果的かつ効率的な方法は、すべてのサーバー間の認証と承認のために標準化された方法を使用することです。</span><span class="sxs-lookup"><span data-stu-id="8708c-109">Although it's possible to use one authentication mechanism for Lync-to-Exchange communication and a separate mechanism for Lync-to-SharePoint communication, a better and more efficient approach is to use a standardized method for all server-to-server authentication and authorization.</span></span>

<span data-ttu-id="8708c-110">サーバー間認証に単一の標準化された方法を使用することは、Lync Server 2013 によって行われる方法です。</span><span class="sxs-lookup"><span data-stu-id="8708c-110">Using a single, standardized method for server-to-server authentication is the approach taken by Lync Server 2013.</span></span> <span data-ttu-id="8708c-111">2013リリースの Lync Server 2013 (および Exchange 2013 および Microsoft SharePoint Server を含むその他の Microsoft サーバー製品) では、サーバー間の認証と承認のために OAuth (Open Authorization) プロトコルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8708c-111">For the 2013 release, Lync Server 2013 (as well as other Microsoft Server products, including Exchange 2013 and Microsoft SharePoint Server) support the OAuth (Open Authorization) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="8708c-112">多くの主要 web サイトで使用されている標準の認証プロトコルである OAuth を使用している場合、ユーザーの資格情報とパスワードは、あるコンピューターから別のコンピューターに渡されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8708c-112">With OAuth, a standard authorization protocol used by a number of major websites, user credentials and passwords are not passed from one computer to another.</span></span> <span data-ttu-id="8708c-113">代わりに、認証と承認はセキュリティトークンの交換に基づいています。これらのトークンによって、特定の時間に対して特定のリソースのセットへのアクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="8708c-113">Instead, authentication and authorization is based on the exchange of security tokens; these tokens grant access to a specific set of resources for a specific amount of time.</span></span>

<span data-ttu-id="8708c-114">OAuth 認証には、通常、単一の承認サーバーと、互いに通信する必要がある2つの領域の3つの当事者が関係します。</span><span class="sxs-lookup"><span data-stu-id="8708c-114">OAuth authentication typically involves three parties: a single authorization server and the two realms that need to communicate with one another.</span></span> <span data-ttu-id="8708c-115">(このドキュメントの後半で説明するプロセスである承認サーバーを使用せずに、サーバー間認証を実行することもできます)。セキュリティトークンは、通信する必要がある2つの領域に対して、承認サーバー (セキュリティトークンサーバーとも呼ばれます) によって発行されます。これらのトークンは、あるレルムから発信された通信が他のレルムによって信頼される必要があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8708c-115">(You can also do server-to-server authentication without using an authorization server, a process that will be discussed later in this document.) Security tokens are issued by the authorization server (also known as a security token server) to the two realms that need to communicate; these tokens verify that communications originating from one realm should be trusted by the other realm.</span></span> <span data-ttu-id="8708c-116">たとえば、承認サーバーは、特定の Lync Server 2013 領域のユーザーに対して、指定された Exchange 2013 領域へのアクセスを許可するかどうかを確認するトークンを発行する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-116">For example, the authorization server might issue tokens that verify that users from a specific Lync Server 2013 realm are able to access a specified Exchange 2013 realm, and vice-versa.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="8708c-117">領域とは、セキュリティ コンテナーのことです。</span><span class="sxs-lookup"><span data-stu-id="8708c-117">A realm is simply a security container.</span></span> <span data-ttu-id="8708c-118">既定では、Lync Server 2013 は、既定の SIP ドメインを OAuth レルムとして使用します。</span><span class="sxs-lookup"><span data-stu-id="8708c-118">By default, Lync Server 2013 uses your default SIP domain as its OAuth realm.</span></span> <span data-ttu-id="8708c-119">追加の SIP 名前空間が OAuth 証明書のサブジェクト代替名に追加されます。</span><span class="sxs-lookup"><span data-stu-id="8708c-119">Additional SIP namespaces are added to the Subject Alternate Name list in the OAuth certificate.</span></span>



</div>

<span data-ttu-id="8708c-120">Lync Server 2013 は、サーバー間認証の3つのシナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8708c-120">Lync Server 2013 supports three server-to-server authentication scenarios.</span></span> <span data-ttu-id="8708c-121">Lync Server 2013 では、次のことができます。</span><span class="sxs-lookup"><span data-stu-id="8708c-121">With Lync Server 2013 you can:</span></span>

  - <span data-ttu-id="8708c-122">オンプレミスでの Lync Server 2013 とオンプレミスインストールとの間で、サーバー間認証を構成します。 Exchange 2013 および Microsoft SharePoint Server のオンプレミスインストール。</span><span class="sxs-lookup"><span data-stu-id="8708c-122">Configure server-to-server authentication between an on-premise installation of Lync Server 2013 and an on-premises installation of Exchange 2013 and/or Microsoft SharePoint Server.</span></span>

  - <span data-ttu-id="8708c-123">Microsoft 365 の2つのコンポーネント (たとえば、Microsoft Exchange と Microsoft Lync Server、または Microsoft Lync Server と Microsoft SharePoint の間) との間でサーバー間認証を構成します。</span><span class="sxs-lookup"><span data-stu-id="8708c-123">Configure server-to-server authentication between a pair of Microsoft 365 components (for example, between Microsoft Exchange and Microsoft Lync Server, or between Microsoft Lync Server and Microsoft SharePoint).</span></span>

  - <span data-ttu-id="8708c-124">クロスプレミス環境 (つまり、オンプレミスサーバーと Microsoft 365 コンポーネントの間のサーバー間認証) でサーバー間認証を構成します。</span><span class="sxs-lookup"><span data-stu-id="8708c-124">Configure server-to-server authentication in a cross-premises environment (that is, server-to-server authentication between an on-premises server and an Microsoft 365 component).</span></span>

<span data-ttu-id="8708c-125">この時点では、Exchange 2013、SharePoint Server、Lync Server 2013 のみがサーバー間認証をサポートしていることに注意してください。これらのサーバーのいずれかを実行していない場合は、OAuth 認証を完全に実装することはできません。</span><span class="sxs-lookup"><span data-stu-id="8708c-125">Note that, at this point in time, only Exchange 2013, SharePoint Server, and Lync Server 2013 support server-to-server authentication; if you are not running one of these servers then you will not be able to fully implement OAuth authentication.</span></span>

<span data-ttu-id="8708c-126">また、サーバー間認証を使用する必要がないことも指摘されます。 Lync Server 2013 を展開するためにサーバー間認証は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8708c-126">It should also be pointed out that you do not need to use server-to-server authentication: server-to-server authentication is not required in order to deploy Lync Server 2013.</span></span> <span data-ttu-id="8708c-127">Lync Server 2013 が他のサーバー (Exchange 2013 など) と通信する必要がない場合は、サーバー間認証は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8708c-127">If Lync Server 2013 does not need to communicate with other servers (such as Exchange 2013) then server-to-server authentication is not needed.</span></span>

<span data-ttu-id="8708c-128">ただし、Lync Server の新機能の一部 ("統合連絡先ストア" など) を使用する場合は、サーバー間認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="8708c-128">However, server-to-server authentication is required if you want to use some of Lync Server's new features, such as the "unified contact store."</span></span> <span data-ttu-id="8708c-129">統合連絡先ストアでは、Lync Server 2013 の連絡先情報は、Lync Server の代わりに Exchange 2013 に保存されます。これにより、ユーザーは Lync、Microsoft Outlook、または Microsoft Outlook Web Access の中から、簡単にアクセスできる単一の連絡先セットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8708c-129">With unified contact store, Lync Server 2013 contact information is stored in Exchange 2013 instead of in Lync Server; this enables users to have a single set of contacts that is readily accessible from within Lync, Microsoft Outlook, or Microsoft Outlook Web Access.</span></span> <span data-ttu-id="8708c-130">ユニファイド連絡先ストアでは、Lync Server 2013 で Exchange 2013 と情報を共有する必要があるため、機能を展開するには、サーバー間認証を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-130">Because the unified contact store requires Lync Server 2013 to share information with Exchange 2013, you must use server-to-server authentication in order to deploy the feature.</span></span> <span data-ttu-id="8708c-131">インスタントメッセージングセッションのトランスクリプトは、個別のデータベースレコードとしてではなく Exchange 2013 のメールとして保存されるため、Exchange アーカイブの使用を選択する場合も、サーバー間認証が必要になります。</span><span class="sxs-lookup"><span data-stu-id="8708c-131">Server-to-server authentication is also required if you choose to use Exchange archiving, in which the transcripts of instant messaging sessions are saved as Exchange 2013 emails rather than as individual database records.</span></span>

<span data-ttu-id="8708c-132">Microsoft 365 バージョンの Lync Server が Exchange に対応した製品と通信するためには、まず2013、承認サーバーからセキュリティトークンを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-132">For the Microsoft 365 version of Lync Server to communicate with its Exchange counterpart, Lync Server 2013 must first obtain a security token from the authorization server.</span></span> <span data-ttu-id="8708c-133">次に、Lync Server がそのセキュリティトークンを使用して Exchange に対して身元を確認します。</span><span class="sxs-lookup"><span data-stu-id="8708c-133">Lync Server then uses that security token to identify itself to Exchange.</span></span> <span data-ttu-id="8708c-134">Microsoft 365 バージョンの Exchange は、Lync Server 2013 と通信するために、同じ手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-134">The Microsoft 365 version of Exchange must go through the same process in order to communicate with Lync Server 2013.</span></span>

<span data-ttu-id="8708c-135">ただし、2つの Microsoft サーバー間でのオンプレミスのサーバー間認証の場合、サードパーティのトークンサーバーを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8708c-135">However, for on-premises server-to-server authentication between two Microsoft servers there is no need to use a third-party token server.</span></span> <span data-ttu-id="8708c-136">Lync Server 2013 や Exchange 2013 などのサーバー製品には、サーバー間認証をサポートする他の Microsoft サーバー (SharePoint Server など) との認証目的で使用できる組み込みのトークンサーバーがあります。</span><span class="sxs-lookup"><span data-stu-id="8708c-136">Server products such as Lync Server 2013 and Exchange 2013 have a built-in token server that can be used for authentication purposes with other Microsoft servers (such as SharePoint server) that support server-to-server authentication.</span></span> <span data-ttu-id="8708c-137">たとえば、Lync Server 2013 は、セキュリティトークンを単独で発行して署名し、そのトークンを使って Exchange 2013 と通信することができます。</span><span class="sxs-lookup"><span data-stu-id="8708c-137">For example, Lync Server 2013 can issue and sign a security token by itself, then use that token to communicate with Exchange 2013.</span></span> <span data-ttu-id="8708c-138">このような場合は、サードパーティのトークンサーバーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8708c-138">In a case like this, there is no need for a third-party token server.</span></span>

<span data-ttu-id="8708c-139">Lync Server 2013 のオンプレミス実装用にサーバー間認証を構成するには、次の2つの操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-139">In order to configure server-to-server authentication for an on-premises implementation of Lync Server 2013 you must do two things:</span></span>

  - <span data-ttu-id="8708c-140">Lync Server の組み込みトークン発行者に証明書を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8708c-140">Assign a certificate to Lync Server's built-in token issuer.</span></span>

  - <span data-ttu-id="8708c-141">Lync Server 2013 で通信するサーバーを "パートナーアプリケーション" として構成します。</span><span class="sxs-lookup"><span data-stu-id="8708c-141">Configure the server that Lync Server 2013 will communicate with to be a "partner application."</span></span> <span data-ttu-id="8708c-142">たとえば、Lync Server 2013 が Exchange 2013 と通信する必要がある場合、Exchange をパートナーアプリケーションとして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8708c-142">For example, if Lync Server 2013 needs to communicate with Exchange 2013 then you will need to configure Exchange to be a partner application.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="8708c-143">"パートナーアプリケーション" は、サードパーティのセキュリティトークンサーバーを経由せずに、Lync Server 2013 がセキュリティトークンを直接交換できるアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="8708c-143">A "partner application" is any application that Lync Server 2013 can directly exchange security tokens with, without having to go through a third-party security token server.</span></span>



</div>

<span data-ttu-id="8708c-144">OAuth は製品の中核部分なので、無効化したり削除したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8708c-144">Note that OAuth is a core part of the product and cannot be disabled or removed.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="8708c-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="8708c-145">See Also</span></span>


[<span data-ttu-id="8708c-146">サーバー間認証証明書を Microsoft Lync Server 2013 に割り当てる</span><span class="sxs-lookup"><span data-stu-id="8708c-146">Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013</span></span>](lync-server-2013-assigning-a-server-to-server-authentication-certificate-to-lync-server-2013.md)  
[<span data-ttu-id="8708c-147">クロスプレミス環境で Microsoft Lync Server 2013 を構成する</span><span class="sxs-lookup"><span data-stu-id="8708c-147">Configuring Microsoft Lync Server 2013 in a cross-premises environment</span></span>](lync-server-2013-configuring-lync-server-in-a-cross-premises-environment.md)  
  

<span data-ttu-id="8708c-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8708c-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

