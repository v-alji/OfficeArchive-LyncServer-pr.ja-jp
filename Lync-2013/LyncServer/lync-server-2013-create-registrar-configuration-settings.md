---
title: 'Lync Server 2013: レジストラー構成の設定を作成する'
description: 'Lync Server 2013: レジストラー構成の設定を作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Registrar configuration settings
ms:assetid: eddfbdd2-cfd0-4c03-986e-443d6728db7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182601(v=OCS.15)
ms:contentKeyID: 48185758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ada10302b3c2319e0f713ce2d3bea00b6fed126
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431604"
---
# <a name="create-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d8ef2-103">Lync Server 2013 でレジストラー構成設定を作成する</span><span class="sxs-lookup"><span data-stu-id="d8ef2-103">Create Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8ef2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8ef2-104">

<span> </span></span></span>

<span data-ttu-id="d8ef2-105">_**最終更新日:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="d8ef2-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="d8ef2-p101">レジストラーを使用してプロキシ サーバーの認証方式を構成できます。指定する認証プロトコルにより、プール内のサーバーがクライアントに発行するチャレンジの種類が決まります。使用可能なプロトコルは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-p101">You can use the Registrar to configure proxy server authentication methods. The authentication protocol you specify determines which type of challenges the servers in the pool issue to clients. The available protocols are:</span></span>

  - <span data-ttu-id="d8ef2-109">**Kerberos**   これは、クライアントが利用できる最強のパスワードベースの認証スキームですが、通常はエンタープライズクライアントでのみ利用できます。これは、キー配布センター (Kerberos ドメインコントローラー) へのクライアント接続が必要であるためです。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-109">**Kerberos**   This is the strongest password-based authentication scheme available to clients, but it is normally available only to enterprise clients because it requires client connection to a Key Distribution Center (Kerberos domain controller).</span></span> <span data-ttu-id="d8ef2-110">この設定は、サーバーでエンタープライズのクライアントのみを認証する場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-110">This setting is appropriate if the server authenticates only enterprise clients.</span></span>

  - <span data-ttu-id="d8ef2-111">**NTLM**   これはパスワードベースの認証であり、パスワードに関するチャレンジ応答ハッシュスキームを使用するクライアントで利用できます。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-111">**NTLM**   This is the password-based authentication available to clients that use a challenge-response hashing scheme on the password.</span></span> <span data-ttu-id="d8ef2-112">これは、リモート ユーザーなど、キー配布センター (Kerberos ドメイン コントローラー) に接続できないクライアントの認証で使用できる唯一のクライアント認証方式です。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-112">This is the only form of authentication available to clients without connectivity to a Key Distribution Center (Kerberos domain controller), such as remote users.</span></span> <span data-ttu-id="d8ef2-113">サーバーでリモート ユーザーのみの認証処理を行う場合は、NTLM を選択してください。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-113">If a server authenticates only remote users, you should choose NTLM.</span></span>

  - <span data-ttu-id="d8ef2-114">**証明書の認証**   これは、サーバーが Lync Phone Edition クライアント、共通のエリア電話、Lync 2013、Lync Windows ストアアプリから証明書を取得する必要がある場合の新しい認証方法です。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-114">**Certificate authentication**   This is the new authentication method when the server needs to obtain certificates from Lync Phone Edition clients, common area phones, Lync 2013 and the Lync Windows Store app.</span></span> <span data-ttu-id="d8ef2-115">Lync Phone Edition クライアントでは、ユーザーがサインインして、暗証番号 (PIN) を提供して認証された後、Lync Server 2013 は電話に対して SIP URI をプロビジョニングし、その電話に対して、Lync Server の署名された証明書または Joe (Ex: SN=joe@contoso.com) を識別するユーザー証明書をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-115">On Lync Phone Edition clients, after a user signs in and is successfully authenticated by providing a personal identification number (PIN), Lync Server 2013 then provisions the SIP URI to the phone and provisions a Lync Server signed certificate or a user certificate that identifies Joe (Ex: SN=joe@contoso.com ) to the phone.</span></span> <span data-ttu-id="d8ef2-116">この証明書は、レジストラー サービスと Web サービスでの認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-116">This certificate is used for authenticating with the Registrar and Web Services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d8ef2-p105">サーバーがリモートとエンタープライズ両方のクライアント認証をサポートする場合は、Kerberos と NTLM の両方を有効にすることをお勧めします。エッジ サーバーと内部サーバーは通信して、NTLM 認証のみがリモート クライアントに提供されるようにします。これらのサーバーで Kerberos のみが有効な場合、リモート ユーザーを認証できません。エンタープライズ ユーザーはサーバーに対しても認証を行い、Kerberos が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-p105">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span><BR><span data-ttu-id="d8ef2-121">Lync Windows ストアアプリクライアントを使用する場合は、証明書の認証を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-121">If you will use Lync Windows Store app clients, you must enable certificate authentication.</span></span>



</div>

<span data-ttu-id="d8ef2-122">以下の手順に従って新しいレジストラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-122">Follow these steps to create a new Registrar.</span></span>

<div>

## <a name="to-create-new-registrar-configuration-settings"></a><span data-ttu-id="d8ef2-123">レジストラー構成設定を作成するには</span><span class="sxs-lookup"><span data-stu-id="d8ef2-123">To create new Registrar configuration settings</span></span>

1.  <span data-ttu-id="d8ef2-124">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="d8ef2-125">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d8ef2-126">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d8ef2-127">左側のナビゲーション バーで [**セキュリティ**] をクリックし、[**レジストラー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-127">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="d8ef2-128">[**レジストラー**] ページで [**新規作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-128">On the **Registrar** page, click **New**</span></span>

5.  <span data-ttu-id="d8ef2-129">[**サービスの選択**] で、レジストラーを適用するサービスをクリックし、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-129">In **Select a Service**, click the service to which the Registrar is to be applied and then click **OK**.</span></span>

6.  <span data-ttu-id="d8ef2-130">[**新規レジストラー設定**] で、クライアントの機能および環境のサポート状況に応じて、次の中から 1 つ以上選択します。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-130">In **New Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="d8ef2-131">[**Kerberos 認証を有効にする**]。プール内のサーバーは、Kerberos 認証を使用してチャレンジを発行します。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-131">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="d8ef2-132">[**NTLM 認証を有効にする**]。プール内のサーバーは、NTLM 認証を使用してチャレンジを発行します。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-132">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="d8ef2-133">[**証明書認証を有効にする**]。プール内のサーバーは、クライアントに対して証明書を発行します。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-133">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

7.  <span data-ttu-id="d8ef2-134">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8ef2-134">Click **Commit**.</span></span>

<span data-ttu-id="d8ef2-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8ef2-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

