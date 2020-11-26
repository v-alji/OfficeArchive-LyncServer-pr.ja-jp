---
title: 'Lync Server 2013: CDR テーブルの詳細'
description: 'Lync Server 2013: CDR テーブルの詳細。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435482"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="80d8c-103">Lync Server 2013 の CDR テーブルの詳細</span><span class="sxs-lookup"><span data-stu-id="80d8c-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80d8c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80d8c-104">

<span> </span></span></span>

<span data-ttu-id="80d8c-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="80d8c-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="80d8c-106">次のトピックでは、各通話詳細レコード (CDR) データベーススキーマテーブルの列について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="80d8c-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="80d8c-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="80d8c-107">In This Section</span></span>

  - [<span data-ttu-id="80d8c-108">Lync Server 2013 の Application テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="80d8c-109">Lync Server 2013 の CallPriorities テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="80d8c-110">Lync Server 2013 の CallType テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="80d8c-111">Lync Server 2013 の ClientVersions テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="80d8c-112">Lync Server 2013 の ConferenceJoinTimeThresholds テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="80d8c-113">Lync Server 2013 の ConferenceMessageCount テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="80d8c-114">Lync Server 2013 の Conferences テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="80d8c-115">Lync Server 2013 の ConferenceSessionDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="80d8c-116">Lync Server 2013 の ConferenceUris テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="80d8c-117">Lync Server 2013 の ContentTypes テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="80d8c-118">Lync Server 2013 の DeRegisterType テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="80d8c-119">Lync Server 2013 の Devices テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="80d8c-120">Lync Server 2013 の Dialogs テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="80d8c-121">Lync Server 2013 の EdgeServers テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="80d8c-122">Lync Server 2013 の ErrorCategory テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="80d8c-123">Lync Server 2013 ErrorDef テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="80d8c-124">Lync Server 2013 の ErrorReport テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="80d8c-125">Lync Server 2013 の FileTransfers テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="80d8c-126">Lync Server 2013 の FocusJoinsAndLeaves テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="80d8c-127">Lync Server 2013 のフロントエンドテーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="80d8c-128">Lync Server 2013 のゲートウェイ テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="80d8c-129">Lync Server 2013 の HardwareVersions テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="80d8c-130">Lync Server 2013 の IMReportSummary テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="80d8c-131">Lync Server 2013 の Locations テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="80d8c-132">Lync Server 2013 の Manufacturers テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="80d8c-133">Lync Server 2013 の McuJoinsAndLeaves テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="80d8c-134">Lync Server 2013 の Mcus テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="80d8c-135">Lync Server 2013 の Media テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="80d8c-136">Lync Server 2013 の MediaList テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="80d8c-137">Lync Server 2013 の MediationServers テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="80d8c-138">Lync Server 2013 の MSMQProcessing テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="80d8c-139">Lync Server 2013 の Phones テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="80d8c-140">Lync Server 2013 の Pools テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="80d8c-141">Lync Server 2013 の ProgressReport テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="80d8c-142">Lync Server 2013 の PurgeSettings テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="80d8c-143">Lync Server 2013 の Registration テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="80d8c-144">Lync Server 2013 の Roles テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="80d8c-145">Lync Server 2013 の Servers テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="80d8c-146">Lync Server 2013 の SessionDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="80d8c-147">Lync Server 2013 の SIPResponseMetaData テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="80d8c-148">Lync Server 2013 の Syndicators テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="80d8c-149">Lync Server 2013 の SyndicatorsTenantMap テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="80d8c-150">Lync Server 2013 のタスクテーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="80d8c-151">Lync Server 2013 の Tenants テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="80d8c-152">Lync Server 2013 の UriTypes テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="80d8c-153">Lync Server 2013 のユーザー テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="80d8c-154">Lync Server 2013 の UserAgentDef テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="80d8c-155">Lync Server 2013 の UserStatistics テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="80d8c-156">Lync Server 2013 の VoipDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="80d8c-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="80d8c-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80d8c-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

