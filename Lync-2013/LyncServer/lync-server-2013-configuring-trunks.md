---
title: 'Lync Server 2013: トランクの構成'
description: 'Lync Server 2013: trunks を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432465"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="3475c-103">Lync Server 2013 でのトランクの構成</span><span class="sxs-lookup"><span data-stu-id="3475c-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3475c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3475c-104">

<span> </span></span></span>

<span data-ttu-id="3475c-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3475c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3475c-106">エンタープライズ Voip の展開の一部として、仲介サーバーと次のピアの1つ以上にトランクを構成して、組織内のエンタープライズボイスクライアントとデバイスの公衆交換電話網 (PSTN) 接続を提供できます。</span><span class="sxs-lookup"><span data-stu-id="3475c-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="3475c-107">インターネット テレフォニー サービス プロバイダー (ITSP) への SIP トランク接続</span><span class="sxs-lookup"><span data-stu-id="3475c-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="3475c-108">PSTN ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="3475c-108">PSTN gateway</span></span>

  - <span data-ttu-id="3475c-109">構内交換機 (PBX)</span><span class="sxs-lookup"><span data-stu-id="3475c-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="3475c-110">詳細については、計画ドキュメントの「 [Lync Server 2013 での PSTN 接続の計画](lync-server-2013-planning-for-pstn-connectivity.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3475c-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3475c-111">トランクの構成を開始する前に、トポロジが作成され、仲介サーバーとそのピアが構成されて互いに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3475c-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="3475c-112">詳細については、展開ドキュメントの「 <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Lync Server 2013 でのトポロジビルダーでのゲートウェイの定義</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3475c-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="3475c-113">トランク構成の一部として、Lync Server 2013 メディアバイパス機能を有効にして、メディアが仲介サーバーをバイパスすることを可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3475c-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="3475c-114">Trunks は、メディアのバイパスを有効にするかどうかを指定して構成できますが、有効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3475c-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="3475c-115">詳細については、計画ドキュメントの「 <A href="lync-server-2013-planning-for-media-bypass.md">Lync Server 2013 でのメディアのバイパスの計画</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3475c-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3475c-116">このセクション中</span><span class="sxs-lookup"><span data-stu-id="3475c-116">In This Section</span></span>

  - [<span data-ttu-id="3475c-117">Lync Server 2013 での複数のトランクのサポート</span><span class="sxs-lookup"><span data-stu-id="3475c-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="3475c-118">Lync Server 2013 のクロストランクルーティング</span><span class="sxs-lookup"><span data-stu-id="3475c-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="3475c-119">Lync Server 2013 でのトランク構成情報の表示</span><span class="sxs-lookup"><span data-stu-id="3475c-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="3475c-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3475c-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="3475c-121">Lync Server 2013 でメディアをバイパスせずにトランクを構成する</span><span class="sxs-lookup"><span data-stu-id="3475c-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="3475c-122">Lync Server 2013 で、トランク構成設定の新しいコレクションを作成する</span><span class="sxs-lookup"><span data-stu-id="3475c-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="3475c-123">Lync Server 2013 で既存の SIP トランク構成設定のコレクションを削除する</span><span class="sxs-lookup"><span data-stu-id="3475c-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="3475c-124">Lync Server 2013 で SIP トランクの設定を変更する</span><span class="sxs-lookup"><span data-stu-id="3475c-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="3475c-125">Lync Server 2013 で SIP トランクの構成設定をテストする</span><span class="sxs-lookup"><span data-stu-id="3475c-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="3475c-126">Lync Server 2013 で個別の SIP trunks に関する情報を表示する</span><span class="sxs-lookup"><span data-stu-id="3475c-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3475c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3475c-127">See Also</span></span>


[<span data-ttu-id="3475c-128">Lync Server 2013 でのトポロジビルダーでのゲートウェイの定義</span><span class="sxs-lookup"><span data-stu-id="3475c-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="3475c-129">Lync Server 2013 での PSTN 接続の計画</span><span class="sxs-lookup"><span data-stu-id="3475c-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="3475c-130">Lync Server 2013 でのメディア バイパスの計画</span><span class="sxs-lookup"><span data-stu-id="3475c-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="3475c-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3475c-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

