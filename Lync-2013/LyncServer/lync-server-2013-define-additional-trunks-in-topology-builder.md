---
title: 'Lync Server 2013: トポロジビルダーで追加の trunks を定義する'
description: 'Lync Server 2013: トポロジビルダーで追加の trunks を定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define additional trunks in Topology Builder
ms:assetid: e68b8377-50a2-452a-bf5c-910929e34236
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721915(v=OCS.15)
ms:contentKeyID: 49733849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57983d3e4d6a47c14f2dcdc153fe6872a33eb6e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431123"
---
# <a name="define-additional-trunks-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="fcda4-103">Lync Server 2013 のトポロジビルダーで追加の trunks を定義する</span><span class="sxs-lookup"><span data-stu-id="fcda4-103">Define additional trunks in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcda4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcda4-104">

<span> </span></span></span>

<span data-ttu-id="fcda4-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="fcda4-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="fcda4-106">次の手順に従って、トポロジビルダーを使用して、 *ピア* を仲介サーバーに関連付けることができる追加のトランクを定義します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-106">Follow these steps to use Topology Builder to define an additional trunk to which you can associate a *peer* with a Mediation Server.</span></span> <span data-ttu-id="fcda4-107">Peer は、公衆交換電話網 (PSTN) に接続して、エンタープライズ Voip を有効にします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-107">A peer provides users enabled for Enterprise Voice with connectivity to the public switched telephone network (PSTN).</span></span> <span data-ttu-id="fcda4-108">ピアとなるのは、PSTN ゲートウェイ、IP-PBX、またはインターネット テレフォニー サービス プロバイダー (ITSP) のセッション ボーダー コントローラー (SBC) などです。</span><span class="sxs-lookup"><span data-stu-id="fcda4-108">A peer can be a PSTN gateway, an IP-PBX, or a Session Border Controller (SBC) for an Internet Telephony Service Provider (ITSP).</span></span> <span data-ttu-id="fcda4-109">トランクは、仲介サーバーとピア間の接続を定義します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-109">The trunk defines this connection between the Mediation Server and peer.</span></span> <span data-ttu-id="fcda4-110">複数の trunks は、仲介サーバーごとに定義できます。</span><span class="sxs-lookup"><span data-stu-id="fcda4-110">Multiple trunks can be defined per Mediation Server.</span></span> <span data-ttu-id="fcda4-111">仲介サーバーは、複数のピアに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="fcda4-111">A Mediation Server can be associated with multiple peers.</span></span>

<span data-ttu-id="fcda4-112">トランクは、仲介サーバーと、組によって一意に識別されたゲートウェイの間の論理的な接続です。</span><span class="sxs-lookup"><span data-stu-id="fcda4-112">A trunk is a logical connection between a Mediation Server and a gateway uniquely identified by the tuple:</span></span>

<span data-ttu-id="fcda4-113">{仲介サーバーの FQDN、仲介サーバーのリッスンポート (TLS または TCP): ゲートウェイ IP と FQDN、ゲートウェイリッスンポート}</span><span class="sxs-lookup"><span data-stu-id="fcda4-113">{Mediation Server FQDN, Mediation Server listening port (TLS or TCP) : gateway IP and FQDN, gateway listening port}</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fcda4-114">このトピックでは、展開ドキュメントの <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Lync server 2013 の [トポロジビルダーでのゲートウェイの定義</A> ] の説明に従って、少なくとも1つの併置またはスタンドアロンの仲介サーバーまたはプールで PSTN ゲートウェイとルートトランクをセットアップしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="fcda4-114">This topic assumes that you have setup a PSTN gateway and root trunk with at least one collocated or stand-alone Mediation Server or pool as described in <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="fcda4-115">このトピックでは、少なくとも1つのセントラルサイトで少なくとも1つのフロントエンドプールまたは Standard Edition サーバーを設定していることを前提<A href="lync-server-2013-publish-the-topology.md">2013</A>としています。詳細については、「 <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">lync Server 2013 でフロントエンドプールまたは standard Edition サーバーを定義して構成</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fcda4-115">This topic assumes that you have set up at least one Front End pool or Standard Edition server in at least one central site, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> and <A href="lync-server-2013-publish-the-topology.md">Publish the topology in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-define-an-additional-trunk-between-a-mediation-server-and-a-gateway-peer"></a><span data-ttu-id="fcda4-116">仲介サーバーとゲートウェイピアの間に追加のトランクを定義するには</span><span class="sxs-lookup"><span data-stu-id="fcda4-116">To Define an additional Trunk between a Mediation Server and a Gateway Peer</span></span>

1.  <span data-ttu-id="fcda4-117">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-117">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="fcda4-118">[Lync Server 2013、サイト名、 **共有コンポーネント**] で、[ **Trunks** ] ノードを右クリックし、[ **新しいトランク**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-118">Under Lync Server 2013, your site name, **Shared Components**, right-click the **Trunks** node, and then click **New Trunk**.</span></span>
    
    <span data-ttu-id="fcda4-119">![Lync Server トポロジビルダーのファイル構造画面](images/JJ721915.90d5b349-aa1e-407a-87ed-fa112f478560(OCS.15).png "Lync Server トポロジビルダーのファイル構造画面")</span><span class="sxs-lookup"><span data-stu-id="fcda4-119">![Lync Server Topology Builder file structure screen](images/JJ721915.90d5b349-aa1e-407a-87ed-fa112f478560(OCS.15).png "Lync Server Topology Builder file structure screen")</span></span>

3.  <span data-ttu-id="fcda4-120">[**新しいトランクの定義**] で、トランクを一意に識別するためのフレンドリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-120">In **Define New Trunk**, specify a friendly name to uniquely identify the trunk.</span></span> <span data-ttu-id="fcda4-121">2 つのトランクに同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="fcda4-121">You cannot have two trunks with the same name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fcda4-122">トランスポートの種類としてトランスポート層セキュリティ (TLS) を指定した場合は、仲介サーバーのピアの IP アドレスではなく、FQDN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcda4-122">If you specify Transport Layer Security (TLS) as the transport type, you must specify the FQDN instead of the IP address of the peer of the Mediation Server.</span></span>

    
    </div>

4.  <span data-ttu-id="fcda4-123">[**PSTN ゲートウェイの関連付け**] で、PSTN ゲートウェイ ピアを選択してこのトランクと関連付けます。</span><span class="sxs-lookup"><span data-stu-id="fcda4-123">Under **Associated PSTN gateway**, select the PSTN gateway peer to associate with this trunk.</span></span>
    
    <span data-ttu-id="fcda4-124">![トランク用 PSTN ゲートウェイピアのプロパティ設定](images/JJ721915.7c3fe8ee-8f4c-4413-8462-8347228e61bb(OCS.15).png "トランク用 PSTN ゲートウェイピアのプロパティ設定")</span><span class="sxs-lookup"><span data-stu-id="fcda4-124">![Property settings for PSTN gateway peer for trunk](images/JJ721915.7c3fe8ee-8f4c-4413-8462-8347228e61bb(OCS.15).png "Property settings for PSTN gateway peer for trunk")</span></span>

5.  <span data-ttu-id="fcda4-125">[ **Pstn ゲートウェイのリスニングポート**] で、ピア (pstn ゲートウェイ、IP PBX、または SBC) がこのトランクに関連付けられている仲介サーバーから SIP メッセージを受信するリッスンポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-125">Under **Listening Port for PSTN gateway**, type the listening port that the peer (PSTN gateway, IP-PBX, or SBC) will receive SIP messages from the Mediation Server that is to be associated with this trunk.</span></span> <span data-ttu-id="fcda4-126">既定のピア ポートは、伝送制御プロトコル (TCP) 用が 5066 で、トランスポート層セキュリティ (TLS) 用が 5067 です。</span><span class="sxs-lookup"><span data-stu-id="fcda4-126">The default peer ports are 5066 for Transmission Control Protocol (TCP) and 5067 for Transport Layer Security (TLS).</span></span> <span data-ttu-id="fcda4-127">既定の Survivable Branch Appliance ポートは、TCP と5082の TLS 用の5081です。</span><span class="sxs-lookup"><span data-stu-id="fcda4-127">The default Survivable Branch Appliance ports are 5081 for TCP and 5082 for TLS.</span></span>

6.  <span data-ttu-id="fcda4-128">[**SIP トランスポート プロトコル**] で、ピアが使用するトランスポートの種類をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-128">Under **SIP Transport Protocol**, click the transport type that the peer uses.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fcda4-129">セキュリティ上の理由から、TLS を使用できる仲介サーバーにピアを展開することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-129">For security reasons, we strongly recommend that you deploy a peer to the Mediation Server that can use TLS.</span></span>

    
    </div>

7.  <span data-ttu-id="fcda4-130">[ **関連付けられた仲介サーバー**] で、このピアのルートトランクに関連付ける仲介サーバープールを選択します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-130">Under **Associated Mediation Server**, select the Mediation Server pool to associate with the root trunk of this peer</span></span>

8.  <span data-ttu-id="fcda4-131">[ **関連付けられた仲介サーバーのポート**] で、仲介サーバーがピアから SIP メッセージを受信するリスニングポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-131">Under **Associated Mediation Server port**, type the listening port that the Mediation Server will receive SIP messages from the peer.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fcda4-132">Lync Server 2013 で複数のトランクがサポートされている場合、同じ<STRONG>関連の仲介サーバーポート</STRONG>と<STRONG>IP/PSTN ゲートウェイ用のリスニングポート</STRONG>を使用して、異なるトランク名を持つ2つの trunks を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="fcda4-132">With multiple trunk support in Lync Server 2013, two trunks with different trunk names cannot be configured with the same <STRONG>Associated Mediation Server port</STRONG> and <STRONG>Listening Port for IP/PSTN gateway</STRONG></span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fcda4-133">Lync Server 2013 で複数のトランクがサポートされているため、複数のピアと通信するために、複数の SIP シグナリングポートを仲介サーバーで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="fcda4-133">With multiple trunk support in Lync Server 2013, multiple SIP signaling ports can be defined on the Mediation Server for communication with multiple peers.</span></span> <span data-ttu-id="fcda4-134">トランクを定義する場合、 <STRONG>関連する仲介サーバーのポート</STRONG> 番号は、仲介サーバーで許可されている各プロトコルのリッスンポートの範囲内である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcda4-134">When defining a trunk, the <STRONG>Associated Mediation Server port</STRONG> number must be within the range of the listening ports for the respective protocol allowed by the Mediation Server.</span></span> <span data-ttu-id="fcda4-135">このポート範囲は、「Lync Server 2013 および仲介サーバープール」に定義されています。</span><span class="sxs-lookup"><span data-stu-id="fcda4-135">This port range is defined under Lync Server 2013 and Mediation Server pools.</span></span> <span data-ttu-id="fcda4-136">関連する仲介サーバープールを右クリックし、[ <STRONG>プロパティの編集</STRONG>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fcda4-136">Right-click the relevant Mediation Server pool, and select <STRONG>Edit Properties</STRONG>.</span></span> <span data-ttu-id="fcda4-137">Specify the port range in the <STRONG>Listening ports</STRONG> field.</span><span class="sxs-lookup"><span data-stu-id="fcda4-137">Specify the port range in the <STRONG>Listening ports</STRONG> field.</span></span>

    
    </div>

9.  <span data-ttu-id="fcda4-138">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fcda4-138">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fcda4-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcda4-139">See Also</span></span>


[<span data-ttu-id="fcda4-140">Lync Server 2013 でのトポロジビルダーでのトランクの変更</span><span class="sxs-lookup"><span data-stu-id="fcda4-140">Modify a trunk in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-modify-a-trunk-in-topology-builder.md)  
  

<span data-ttu-id="fcda4-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcda4-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

