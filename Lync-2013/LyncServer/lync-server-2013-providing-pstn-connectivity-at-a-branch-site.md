---
title: 'Lync Server 2013: ブランチ サイトでの PSTN 接続の提供'
description: 'Lync Server 2013: ブランチサイトでの PSTN 接続を提供します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Providing PSTN connectivity at a branch site
ms:assetid: d78d76fb-2dd1-42cb-b25a-bfaff9650a70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398945(v=OCS.15)
ms:contentKeyID: 48185633
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63cbc03f78a27bda14c2906e31cc68bed5870878
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436735"
---
# <a name="providing-pstn-connectivity-at-a-branch-site-in-lync-server-2013"></a><span data-ttu-id="0ad36-103">Lync Server 2013 におけるブランチ サイトでの PSTN 接続の提供</span><span class="sxs-lookup"><span data-stu-id="0ad36-103">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ad36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ad36-104">

<span> </span></span></span>

<span data-ttu-id="0ad36-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="0ad36-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="0ad36-106">Microsoft Lync Server 2013、計画ツールを使用してトポロジにブランチサイトを追加し、ブランチサイトで音声インフラストラクチャを設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0ad36-106">We recommend using the Microsoft Lync Server 2013, Planning Tool to add branch sites to your topology and to set up your voice infrastructure in branch sites.</span></span>

<span data-ttu-id="0ad36-107">計画ツールを使用していない場合は、まずこのセクションのトピックに記載されている手順を実行します。最初に、ブランチサイトを追加するには、IP/公衆交換電話網 (PSTN) ゲートウェイを定義するか、SIP トランク (メディアのバイパスありまたはなし) を構成して、音声インフラストラクチャをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="0ad36-107">If you are not using the Planning Tool, use the procedures in the topics in this section—first, to add the branch sites, and then, to set up your voice infrastructure by defining the IP/public switched telephone network (PSTN) gateway and/or by configuring the SIP trunk (with or without media bypass).</span></span> <span data-ttu-id="0ad36-108">プライベートブランチ exchange (PBX) からブランチサイトへの接続は、別のオプションです。</span><span class="sxs-lookup"><span data-stu-id="0ad36-108">Connecting a private branch exchange (PBX) to the branch site is another option.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0ad36-109">ブランチサイトの回復性を提供する場合は、ブランチサイトに Survivable Branch Appliance、Survivable Branch Server、Standard Edition サーバーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ad36-109">If you want to provide branch-site resiliency, you must deploy a Survivable Branch Appliance, a Survivable Branch Server, or Standard Edition server at the branch site.</span></span> <span data-ttu-id="0ad36-110">詳細については、展開ドキュメントに「 <A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">Lync server 2013 を使って Survivable Branch Appliance または server を展開する</A> 」または「 <A href="lync-server-2013-deploying-lync-server.md">lync server 2013</A>を展開する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ad36-110">For details, see <A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</A> or <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A>, as appropriate, in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0ad36-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0ad36-111">In This Section</span></span>

  - [<span data-ttu-id="0ad36-112">Lync Server 2013 でのトポロジへのブランチ サイトの追加</span><span class="sxs-lookup"><span data-stu-id="0ad36-112">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="0ad36-113">Lync Server 2013 でのブランチ サイト用の PSTN ゲートウェイの定義</span><span class="sxs-lookup"><span data-stu-id="0ad36-113">Define a PSTN gateway for a branch site in Lync Server 2013</span></span>](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)

  - [<span data-ttu-id="0ad36-114">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ad36-114">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="0ad36-115">Lync Server 2013 でメディアをバイパスせずにトランクを構成する</span><span class="sxs-lookup"><span data-stu-id="0ad36-115">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ad36-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ad36-116">See Also</span></span>


[<span data-ttu-id="0ad36-117">Lync Server 2013 でのメディア バイパスの計画</span><span class="sxs-lookup"><span data-stu-id="0ad36-117">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
[<span data-ttu-id="0ad36-118">Lync Server 2013 での PSTN 接続の計画</span><span class="sxs-lookup"><span data-stu-id="0ad36-118">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
  

<span data-ttu-id="0ad36-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ad36-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

