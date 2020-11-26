---
title: 常設チャット サーバーに対する下位互換性の実行
description: 常設チャットサーバーの下位互換性を実行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run backward compatibility for Persistent Chat Server
ms:assetid: 53f1a706-3104-4a94-8b4e-8badd9a066d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204901(v=OCS.15)
ms:contentKeyID: 48184175
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0486992d44e6385559d3e9df9f9ffc2125120da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423380"
---
# <a name="run-backward-compatibility-for-persistent-chat-server"></a><span data-ttu-id="9bed8-103">常設チャット サーバーに対する下位互換性の実行</span><span class="sxs-lookup"><span data-stu-id="9bed8-103">Run backward compatibility for Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9bed8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9bed8-104">

<span> </span></span></span>

<span data-ttu-id="9bed8-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9bed8-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9bed8-106">Lync Server 2013、常設チャットサーバーのエンドポイントは、常設チャットサーバープールを示す簡単な URL を作成するための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-106">The Lync Server 2013, Persistent Chat Server endpoint provides a way to create a simple URL that points to a Persistent Chat Server pool.</span></span> <span data-ttu-id="9bed8-107">これは、レガシクライアント (Microsoft Office Communications Server 2007 R2 グループチャットサーバーまたは Lync Server 2010、グループチャット) で便利です。ユーザーは、Lync 2013、常設チャットを実行しているコンピューターにレガシクライアントをポイントするときに、手動構成で簡単な URL を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-107">This is useful for legacy clients (Microsoft Office Communications Server 2007 R2 Group Chat Server or Lync Server 2010, Group Chat) because users can enter a simple URL in the manual configuration when trying to point the legacy client to a computer running Lync 2013, Persistent Chat.</span></span> <span data-ttu-id="9bed8-108">このエンドポイントは常設チャットで使用されておらず、レガシクライアントでのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="9bed8-108">This endpoint isn’t used by Persistent Chat, and is required for legacy clients only.</span></span> <span data-ttu-id="9bed8-109">これは、会議室が移行される中間的な期間内に、Lync 2013 クライアントが組織全体に展開されていない場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="9bed8-109">This is useful for the interim period where rooms may be migrated, but the Lync 2013 clients have not been deployed throughout the organization.</span></span> <span data-ttu-id="9bed8-110">Lync 2010 グループチャット (クライアント) を実行しているユーザーは、引き続き常設チャットサーバーバックエンドサーバーに接続できます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-110">Users running Lync 2010 Group Chat (client) can then still connect to the Persistent Chat Server Back End Server.</span></span>

<span data-ttu-id="9bed8-111">複数の常設チャットサーバーのエンドポイントを作成する必要はありません。常設チャットサーバープールごとに1つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="9bed8-111">You don’t need to create multiple Persistent Chat Server endpoints; you just need one for each Persistent Chat Server pool.</span></span> <span data-ttu-id="9bed8-112">管理者は複数のエンドポイントを作成できますが (1 つのプールあたり1つ)、従来のクライアントは一度に1つのプールにしか接続できないように構成できます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-112">Administrators can create multiple endpoints (one per pool), but legacy clients can be configured to connect to only one pool at a time.</span></span> <span data-ttu-id="9bed8-113">通常またはメインストリームのシナリオでは、従来の展開は1つのプールのみになります。</span><span class="sxs-lookup"><span data-stu-id="9bed8-113">In the usual or mainstream scenario, the legacy deployment is one pool only.</span></span> <span data-ttu-id="9bed8-114">新しい展開では、通常、プールは新しい Lync Server 2013 に移行され、追加の常設チャットサーバープールが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="9bed8-114">A new deployment generally migrates that pool to a new Lync Server 2013 and might add some new additional Persistent Chat Server pools.</span></span>

<span data-ttu-id="9bed8-115">このメインストリームシナリオは一般的に、次のパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="9bed8-115">This mainstream scenario generally follows this pattern:</span></span>

  - <span data-ttu-id="9bed8-116">1人の Lync Server 2010、グループチャットプール、Lync 2010 グループチャットクライアントを使って、ユーザーを管理するには、既知のユーザー (既定の sip: ocschat@ \<domainName\> .com など) を使用します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-116">You administer users with one Lync Server 2010, Group Chat pool, and your Lync 2010 Group Chat clients connect to that pool by using some well-known user (either default sip:ocschat@\<domainName\>.com, or a similar one).</span></span> <span data-ttu-id="9bed8-117">ユーザーは SIP 対応の Active Directory ドメインサービスであり、参照サービスは、着信要求を受信するためにそれを登録します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-117">The users are SIP-enabled Active Directory Domain Services, and the Lookup service registers with them to receive incoming requests.</span></span>

  - <span data-ttu-id="9bed8-118">続いて、Lync Server 2013 常設チャットサーバーと常設チャットサーバープールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="9bed8-118">Subsequently, you install a Lync Server 2013 Persistent Chat Server and Persistent Chat Server pool.</span></span>

  - <span data-ttu-id="9bed8-119">通常、ユーザーがオフラインになっている時間 (例: 週末):</span><span class="sxs-lookup"><span data-stu-id="9bed8-119">During a time when users are generally offline (for example, a weekend):</span></span>
    
      - <span data-ttu-id="9bed8-120">Lync Server 2010、グループチャットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="9bed8-120">Turn off Lync Server 2010, Group Chat.</span></span>
    
      - <span data-ttu-id="9bed8-121">Lync Server 2010 からデータを移行するには、グループチャットプールを Lync Server 2013 常設チャットサーバープールに移動します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-121">Migrate data from the Lync Server 2010, Group Chat pool to the Lync Server 2013 Persistent Chat Server pool.</span></span>
    
      - <span data-ttu-id="9bed8-122">Active Directory ドメインサービスから既知のユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-122">Delete the well-known user from the Active Directory Domain Services.</span></span>
    
      - <span data-ttu-id="9bed8-123">以前に削除した既知のユーザーと同じ SIP URI を持つ新しい *従来のエンドポイント* を作成します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-123">Create a new *legacy endpoint* with the same SIP URI as the previously deleted well-known user.</span></span>
    
      - <span data-ttu-id="9bed8-124">Lync Server 2013 の常設チャットサーバーを起動します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-124">Start the Lync Server 2013, Persistent Chat Servers.</span></span>

  - <span data-ttu-id="9bed8-125">ユーザーは、設定を変更せずに、Lync 2010 グループチャット (クライアント) を使ってもう一度ログインし、データに接続します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-125">Users log back on by using their Lync 2010 Group Chat (client) and connect to their data without needing to change any configuration.</span></span>

  - <span data-ttu-id="9bed8-126">後で、Lync Server 2010、グループチャットの使用を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-126">At a later time, you can decommission the Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="9bed8-127">続いて、Lync Server 2013、常設チャットサーバーを展開して、新しい Lync Server 2013 常設チャットサーバープールをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-127">Subsequently, you can deploy Lync Server 2013, Persistent Chat Server, and install new Lync Server 2013 Persistent Chat Server pools.</span></span>

<span data-ttu-id="9bed8-128">Lync Server 2010 からの移行の詳細については、グループチャットから Lync Server 2013、常設チャットサーバーに移行する方法については、「 [Lync server 2010、グループチャット、または Office Communications server 2007 R2 グループチャットから Lync server 2013、常設チャットサーバーへの移行](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9bed8-128">For details about migrating from Lync Server 2010, Group Chat to Lync Server 2013, Persistent Chat Server, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="9bed8-129">下位互換性を実行するには (従来のグループチャットプールクライアントで使用できる常設チャットサーバープールをポイントする常設チャットサーバーのエンドポイントを作成するには) 次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9bed8-129">To run backward compatibility (to create a Persistent Chat Server endpoint that points to a Persistent Chat Server pool, which can be used by legacy Group Chat pool clients):</span></span>

    New-CsPersistentChatEndpoint -SipAddress <CO name, ex. persistentchat@contoso.com> -PersistentChatPoolFqdn <pool FQDN, like pcpool.contoso.com>

<span data-ttu-id="9bed8-130">次に、その SIP アドレスを連絡先オブジェクトとして使用するように常設チャットクライアントを構成します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-130">Next, configure Persistent Chat clients to use that SIP address as their contact object.</span></span> <span data-ttu-id="9bed8-131">SIP アドレスは、特定の常設チャットサーバープール用の **CsPersistentChatEndpoint** コマンドレットを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="9bed8-131">The SIP address is created with the **New-CsPersistentChatEndpoint** cmdlet for a specific Persistent Chat Server pool.</span></span>

<span data-ttu-id="9bed8-132">Windows PowerShell コマンドラインインターフェイスを使用して常設チャットサーバーのエンドポイントを追加するには、次の例を参考にしてください。</span><span class="sxs-lookup"><span data-stu-id="9bed8-132">To add the Persistent Chat Server endpoint by using Windows PowerShell command-line interface, consider the following example.</span></span> <span data-ttu-id="9bed8-133">この場合、プールの完全修飾ドメイン名 (FQDN) が "pcpool.contoso.com" である "contoso.com" トポロジで、"persistentchat" という名前の連絡先オブジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="9bed8-133">In this case, you are configuring the contact object to be named "persistentchat" on the "contoso.com" topology, where the pool fully qualified domain name (FQDN) is "pcpool.contoso.com":</span></span>

    New-CsPersistentChatEndpoint -SipAddress sip:persistentchat@contoso.com -PersistentChatPoolFqdn pcpool.contoso.com

<div>

## <a name="see-also"></a><span data-ttu-id="9bed8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bed8-134">See Also</span></span>


[<span data-ttu-id="9bed8-135">Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行</span><span class="sxs-lookup"><span data-stu-id="9bed8-135">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)  
  

<span data-ttu-id="9bed8-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9bed8-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

