---
title: 'Lync Server 2013: 常設チャット サーバー テーブルの詳細'
description: 'Lync Server 2013: 常設チャットサーバーの表の詳細。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443084"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="117fd-103">Lync Server 2013 の常設チャット サーバー テーブルの詳細</span><span class="sxs-lookup"><span data-stu-id="117fd-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="117fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="117fd-104">

<span> </span></span></span>

<span data-ttu-id="117fd-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="117fd-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="117fd-106">次のトピックでは、常設チャットデータベースの各スキーマテーブルの列について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="117fd-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="117fd-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="117fd-107">In This Section</span></span>

  - [<span data-ttu-id="117fd-108">Lync Server 2013 の tblADCookie</span><span class="sxs-lookup"><span data-stu-id="117fd-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="117fd-109">Lync Server 2013 の tblPrincipalMemberDifference</span><span class="sxs-lookup"><span data-stu-id="117fd-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="117fd-110">Lync Server 2013 の tblADUpdates</span><span class="sxs-lookup"><span data-stu-id="117fd-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="117fd-111">Lync Server 2013 の tblPrincipalMembers</span><span class="sxs-lookup"><span data-stu-id="117fd-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="117fd-112">Lync Server 2013 の tblPrincipalMeta</span><span class="sxs-lookup"><span data-stu-id="117fd-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="117fd-113">Lync Server 2013 の tblSkippedAffiliations</span><span class="sxs-lookup"><span data-stu-id="117fd-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="117fd-114">Lync Server 2013 の tblPrincipalType</span><span class="sxs-lookup"><span data-stu-id="117fd-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="117fd-115">Lync Server 2013 の tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="117fd-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="117fd-116">Lync Server 2013 の tblPrincipalAffiliations</span><span class="sxs-lookup"><span data-stu-id="117fd-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="117fd-117">Lync Server 2013 の tblNode</span><span class="sxs-lookup"><span data-stu-id="117fd-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="117fd-118">Lync Server 2013 の tblRoleType</span><span class="sxs-lookup"><span data-stu-id="117fd-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="117fd-119">Lync Server 2013 の tblScopePrincipal</span><span class="sxs-lookup"><span data-stu-id="117fd-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="117fd-120">Lync Server 2013 の tblPrincipalRole</span><span class="sxs-lookup"><span data-stu-id="117fd-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="117fd-121">Lync Server 2013 の tblSiopWhiteList</span><span class="sxs-lookup"><span data-stu-id="117fd-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="117fd-122">Lync Server 2013 の tblEnumAttribute</span><span class="sxs-lookup"><span data-stu-id="117fd-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="117fd-123">Lync Server 2013 の tblEnumValue</span><span class="sxs-lookup"><span data-stu-id="117fd-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="117fd-124">Lync Server 2013 の tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="117fd-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="117fd-125">Lync Server 2013 の tblChat</span><span class="sxs-lookup"><span data-stu-id="117fd-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="117fd-126">Lync Server 2013 の tblLastInviteId</span><span class="sxs-lookup"><span data-stu-id="117fd-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="117fd-127">Lync Server 2013 の tblLastChatId</span><span class="sxs-lookup"><span data-stu-id="117fd-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="117fd-128">Lync Server 2013 の tblPreference</span><span class="sxs-lookup"><span data-stu-id="117fd-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="117fd-129">Lync Server 2013 の tblFileToken</span><span class="sxs-lookup"><span data-stu-id="117fd-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="117fd-130">Lync Server 2013 の tblServerIdentity</span><span class="sxs-lookup"><span data-stu-id="117fd-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="117fd-131">Lync Server 2013 の tblAdminLock</span><span class="sxs-lookup"><span data-stu-id="117fd-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="117fd-132">Lync Server 2013 の tblSystemRevision</span><span class="sxs-lookup"><span data-stu-id="117fd-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="117fd-133">Lync Server 2013 の tblActivePeers</span><span class="sxs-lookup"><span data-stu-id="117fd-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="117fd-134">Lync Server 2013 の tblConfig</span><span class="sxs-lookup"><span data-stu-id="117fd-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="117fd-135">Lync Server 2013 の tblComplianceData</span><span class="sxs-lookup"><span data-stu-id="117fd-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="117fd-136">Lync Server 2013 内の tblComplianceFanout</span><span class="sxs-lookup"><span data-stu-id="117fd-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="117fd-137">Lync Server 2013 内の tblComplianceParticipant</span><span class="sxs-lookup"><span data-stu-id="117fd-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="117fd-138">Lync Server 2013 の tblComplianceState</span><span class="sxs-lookup"><span data-stu-id="117fd-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="117fd-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="117fd-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

