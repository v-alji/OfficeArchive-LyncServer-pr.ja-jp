---
title: 'Lync Server 2013: 新しい障害復旧および高可用性機能'
description: 'Lync Server 2013: 新しい障害回復と高可用性機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425115"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a><span data-ttu-id="bac76-103">Lync Server 2013 の新しい障害復旧および高可用性機能</span><span class="sxs-lookup"><span data-stu-id="bac76-103">New disaster recovery and high availability features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bac76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bac76-104">

<span> </span></span></span>

<span data-ttu-id="bac76-105">_**最終更新日:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="bac76-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="bac76-106">Lync Server 2010 の場合と同様に、Lync Server 2013 の主な高可用性 (HA) スキームは、プールによるサーバーの冗長性に基づいています。</span><span class="sxs-lookup"><span data-stu-id="bac76-106">As in Lync Server 2010, the main high availability (HA) scheme for Lync Server 2013 is based on server redundancy via pooling.</span></span> <span data-ttu-id="bac76-107">特定のサーバーの役割を実行するサーバーで障害が発生した場合は、プール内の同じ役割を実行する他のサーバーがそのサーバーの負荷を引き受けます。</span><span class="sxs-lookup"><span data-stu-id="bac76-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="bac76-108">同じことが、フロントエンド サーバー、エッジ サーバー、仲介サーバー、およびディレクターでも実行されます。</span><span class="sxs-lookup"><span data-stu-id="bac76-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span>

<span data-ttu-id="bac76-109">Lync Server 2013 は、2つのデータセンターにあるフロントエンドプールを組み合わせることによって、新しい障害回復手段を追加します。</span><span class="sxs-lookup"><span data-stu-id="bac76-109">Lync Server 2013 adds new disaster recovery measures by enabling you to pair Front End pools located in two datacenters.</span></span> <span data-ttu-id="bac76-110">ペアリングされたプールのいずれかがダウンした場合、管理者はそのプールのユーザーをペアの他のプールにフェールオーバーして、サービスの継続を提供できます。</span><span class="sxs-lookup"><span data-stu-id="bac76-110">If one of the paired pools goes down, an administrator can fail over the users from that pool to the other pool in the pair, to provide continuation of service.</span></span> <span data-ttu-id="bac76-111">この機能には、記憶域ネットワークや共有ディスクなどの高価なネットワークやハードウェアソリューションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bac76-111">This functionality does not require expensive network or hardware solutions such as storage networks or shared disks.</span></span>

<span data-ttu-id="bac76-112">また、Lync Server 2013 により、バックエンドサーバーの高可用性が追加されます。</span><span class="sxs-lookup"><span data-stu-id="bac76-112">Lync Server 2013 also adds Back End Server high availability.</span></span> <span data-ttu-id="bac76-113">これは、フロントエンドプール用に2つのバックエンドサーバーを展開し、バックエンドサーバーで実行されているすべての Lync データベースの同期 SQL ミラーリングをセットアップする、オプションのトポロジです。</span><span class="sxs-lookup"><span data-stu-id="bac76-113">This is an optional topology in which you deploy two Back End Servers for a Front End pool, and set up synchronous SQL mirroring for all the Lync databases running on the Back End Servers.</span></span> <span data-ttu-id="bac76-114">ミラーのミラーリングを行うかどうかを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="bac76-114">You may choose whether to deploy a witness for the mirror.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bac76-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="bac76-115">See Also</span></span>


[<span data-ttu-id="bac76-116">Lync Server 2013 での高可用性および障害復旧の計画</span><span class="sxs-lookup"><span data-stu-id="bac76-116">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

<span data-ttu-id="bac76-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bac76-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

