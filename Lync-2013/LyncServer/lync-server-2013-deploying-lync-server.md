---
title: 'Lync Server 2013: Lync Server の展開'
description: 'Lync Server 2013: Lync Server を展開しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013
ms:assetid: b76795a4-4e71-4c70-a5c0-d1197fa8028c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412892(v=OCS.15)
ms:contentKeyID: 48185197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 569b1e8b07954f04ee7e4f73de51494ece27157e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429931"
---
# <a name="deploying-lync-server-2013"></a><span data-ttu-id="66d33-103">Lync Server 2013 の展開</span><span class="sxs-lookup"><span data-stu-id="66d33-103">Deploying Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66d33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66d33-104">

<span> </span></span></span>

<span data-ttu-id="66d33-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="66d33-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="66d33-106">Lync Server 2013 の展開プロセスは、インストールする必要がある Lync Server のトポロジとコンポーネントによって決定されます。これには、フロントエンドプールと Standard Edition サーバーのどちらを展開するかなどが含まれます。</span><span class="sxs-lookup"><span data-stu-id="66d33-106">Your deployment process for Lync Server 2013 is determined by the Lync Server topology and components you decide to install, including whether you want to deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="66d33-107">このセクションのトピックでは、展開する環境を決定し、展開プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="66d33-107">The topics in this section help you determine what environment you want to deploy and guide you through the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="66d33-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="66d33-108">In This Section</span></span>

  - [<span data-ttu-id="66d33-109">Lync Server 2013 の展開の概要</span><span class="sxs-lookup"><span data-stu-id="66d33-109">Deployment overview for Lync Server 2013</span></span>](lync-server-2013-deployment-overview.md)

  - [<span data-ttu-id="66d33-110">Lync Server 2013 のシステム要件</span><span class="sxs-lookup"><span data-stu-id="66d33-110">System requirements for Lync Server 2013</span></span>](lync-server-2013-system-requirements.md)

  - [<span data-ttu-id="66d33-111">Lync Server 2013 のインフラストラクチャとシステムの準備</span><span class="sxs-lookup"><span data-stu-id="66d33-111">Preparing the infrastructure and systems for Lync Server 2013</span></span>](lync-server-2013-preparing-the-infrastructure-and-systems.md)

  - [<span data-ttu-id="66d33-112">Lync Server 2013 でのトポロジの定義と構成</span><span class="sxs-lookup"><span data-stu-id="66d33-112">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)

  - [<span data-ttu-id="66d33-113">Lync Server 2013 でのトポロジ設計の完了と実装</span><span class="sxs-lookup"><span data-stu-id="66d33-113">Finalizing and implementing the topology design in Lync Server 2013</span></span>](lync-server-2013-finalizing-and-implementing-the-topology-design.md)

  - [<span data-ttu-id="66d33-114">Lync Server 2013 でのフロント エンド サーバーおよびフロント エンド プールの設定</span><span class="sxs-lookup"><span data-stu-id="66d33-114">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md)

  - [<span data-ttu-id="66d33-115">既存の Lync Server 2013 Enterprise への Lync Server 2013 Standard Edition の展開</span><span class="sxs-lookup"><span data-stu-id="66d33-115">Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise</span></span>](lync-server-2013-deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise.md)

  - [<span data-ttu-id="66d33-116">Lync Server 2013 でのサーバーの役割の追加</span><span class="sxs-lookup"><span data-stu-id="66d33-116">Adding server roles in Lync Server 2013</span></span>](lync-server-2013-adding-server-roles.md)

  - [<span data-ttu-id="66d33-117">Lync Server 2013 での Kerberos 認証の設定</span><span class="sxs-lookup"><span data-stu-id="66d33-117">Setting up Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication.md)

<span data-ttu-id="66d33-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66d33-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

