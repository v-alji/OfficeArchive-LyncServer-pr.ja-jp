---
title: Lync Online と内部設置型のハイブリッド展開の構成
description: Lync Online とハイブリッド用のオンプレミス展開を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring an on-premises deployment for hybrid with Lync Online
ms:assetid: c26addb0-2936-4eea-9071-3ab95825154b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205237(v=OCS.15)
ms:contentKeyID: 48185321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 717900389db98fc14513a7d54bd37813757f98ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433389"
---
# <a name="configuring-an-on-premises-deployment-for-hybrid-with-lync-online"></a><span data-ttu-id="8499d-103">Lync Online と内部設置型のハイブリッド展開の構成</span><span class="sxs-lookup"><span data-stu-id="8499d-103">Configuring an on-premises deployment for hybrid with Lync Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8499d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8499d-104">

<span> </span></span></span>

<span data-ttu-id="8499d-105">_**最終更新日:** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="8499d-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="8499d-106">ハイブリッド展開とは、一部のユーザーがオンプレミスであり、一部のユーザーがオンラインであるものの、すべてのユーザーが user@contoso.com などの同じドメインを共有する展開です。</span><span class="sxs-lookup"><span data-stu-id="8499d-106">A hybrid deployment is a deployment in which some users are homed on-premises and some users are homed online, but all users share the same domain, such as user@contoso.com.</span></span> <span data-ttu-id="8499d-107">このセクションでは、ハイブリッド展開に必要なアプリケーションを展開して、それを有効にするように展開を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8499d-107">This section guides you through deploying the applications required for a hybrid deployment, and then configuring your deployment to enable it.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8499d-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="8499d-108">In This Section</span></span>

  - [<span data-ttu-id="8499d-109">Lync Server 2013 ハイブリッド環境の概要</span><span class="sxs-lookup"><span data-stu-id="8499d-109">Overview of the Lync Server 2013 hybrid environment</span></span>](lync-server-2013-overview-of-the-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="8499d-110">Lync Server 2013 ハイブリッド環境を準備および展開する手順</span><span class="sxs-lookup"><span data-stu-id="8499d-110">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>](lync-server-2013-steps-to-prepare-and-deploy-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="8499d-111">Lync Server 2013 と Lync Online のフェデレーションを構成する</span><span class="sxs-lookup"><span data-stu-id="8499d-111">Configure federation of Lync Server 2013 with Lync Online</span></span>](lync-server-2013-configure-federation-with-lync-online.md)

  - [<span data-ttu-id="8499d-112">Lync Server 2013 で電話会議プロバイダーのフェデレーションを構成する</span><span class="sxs-lookup"><span data-stu-id="8499d-112">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>](lync-server-2013-configure-federation-for-an-audio-conferencing-provider.md)

  - [<span data-ttu-id="8499d-113">Lync Server 2013 でユーザーを Lync Online に移動する</span><span class="sxs-lookup"><span data-stu-id="8499d-113">Move users to Lync Online in Lync Server 2013</span></span>](lync-server-2013-move-users-to-lync-online.md)

  - [<span data-ttu-id="8499d-114">ハイブリッド Lync Server 2013 展開でユーザーを管理する</span><span class="sxs-lookup"><span data-stu-id="8499d-114">Administering users in a hybrid Lync Server 2013 deployment</span></span>](lync-server-2013-administering-users-in-a-hybrid-deployment.md)

<span data-ttu-id="8499d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8499d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

