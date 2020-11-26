---
title: 'Lync Server 2013: エッジ サーバーの設定'
description: 'Lync Server 2013: エッジサーバーのセットアップ'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Edge Servers
ms:assetid: 09a22919-e36f-4122-8f0d-8d041198912d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398147(v=OCS.15)
ms:contentKeyID: 48183354
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e25c40e8d642d38b38afbab35225b2c7dda4d68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423982"
---
# <a name="setting-up-edge-servers-in-lync-server-2013"></a><span data-ttu-id="6ce06-103">Lync Server 2013 でのエッジ サーバーの設定</span><span class="sxs-lookup"><span data-stu-id="6ce06-103">Setting up Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ce06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ce06-104">

<span> </span></span></span>

<span data-ttu-id="6ce06-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="6ce06-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="6ce06-106">エッジサーバーのセットアップに必要な主なタスクは、1つのエッジサーバーまたはエッジサーバーの負荷分散プールをインストールする場合と同じですが、ハードウェア負荷分散エッジサーバーのプールにはロードバランサーの配置と、複数のエッジサーバーで設定を複製するための追加の手順が必要である点が異なります。</span><span class="sxs-lookup"><span data-stu-id="6ce06-106">The primary tasks required to set up Edge Servers are the same for installing a single Edge Server or a load-balanced pool of Edge Servers, except that a pool of hardware load balanced Edge Servers requires deployment of the load balancers and additional steps for replicating the set up on multiple Edge Servers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6ce06-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="6ce06-107">In This Section</span></span>

  - [<span data-ttu-id="6ce06-108">Lync Server 2013 でのエッジ サーバーのネットワーク インターフェイスの設定</span><span class="sxs-lookup"><span data-stu-id="6ce06-108">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>](lync-server-2013-set-up-network-interfaces-for-edge-servers.md)

  - [<span data-ttu-id="6ce06-109">Lync Server 2013 のエッジ サーバーへの必要なソフトウェアのインストール</span><span class="sxs-lookup"><span data-stu-id="6ce06-109">Install prerequisite software on Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-prerequisite-software-on-edge-servers.md)

  - [<span data-ttu-id="6ce06-110">エッジ インストール用の Lync Server 2013 のトポロジをエクスポートして外部メディアにコピーする</span><span class="sxs-lookup"><span data-stu-id="6ce06-110">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

  - [<span data-ttu-id="6ce06-111">Lync Server 2013 のエッジ サーバーのインストール</span><span class="sxs-lookup"><span data-stu-id="6ce06-111">Install Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-edge-servers.md)

  - [<span data-ttu-id="6ce06-112">Lync Server 2013 用のエッジ証明書のセットアップ</span><span class="sxs-lookup"><span data-stu-id="6ce06-112">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)

  - [<span data-ttu-id="6ce06-113">Lync Server 2013 でのエッジ サーバーの起動</span><span class="sxs-lookup"><span data-stu-id="6ce06-113">Start Edge Servers in Lync Server 2013</span></span>](lync-server-2013-start-edge-servers.md)

  - [<span data-ttu-id="6ce06-114">Lync Server 2013 のリバース プロキシ サーバーの設定</span><span class="sxs-lookup"><span data-stu-id="6ce06-114">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

<span data-ttu-id="6ce06-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ce06-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

