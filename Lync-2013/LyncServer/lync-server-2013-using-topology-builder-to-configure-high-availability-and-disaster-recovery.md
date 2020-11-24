---
title: トポロジ ビルダーを使用して高可用性と障害回復を構成する
description: トポロジビルダーを使用して、高可用性と障害回復を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400118"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="983f0-103">Lync Server 2013 でトポロジ ビルダーを使用して高可用性と障害回復を構成する</span><span class="sxs-lookup"><span data-stu-id="983f0-103">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="983f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="983f0-104">

<span> </span></span></span>

<span data-ttu-id="983f0-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="983f0-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="983f0-106">[トポロジビルダー] で次の手順を実行して、常設チャットサーバーの高可用性と障害回復を構成します。</span><span class="sxs-lookup"><span data-stu-id="983f0-106">Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.</span></span>

1.  <span data-ttu-id="983f0-107">ミラーデータベースとログ配布のセカンダリデータベース SQL Server ストアを追加します。</span><span class="sxs-lookup"><span data-stu-id="983f0-107">Add the mirror databases and the log shipping secondary database SQL Server stores.</span></span>

2.  <span data-ttu-id="983f0-108">常設チャットサーバーサービスのプロパティを編集するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="983f0-108">Edit the Persistent Chat Server service properties to:</span></span>
    
    1.  <span data-ttu-id="983f0-109">プライマリ データベースのミラーリングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="983f0-109">Enable mirroring for the primary database.</span></span>
    
    2.  <span data-ttu-id="983f0-110">プライマリミラー SQL Server ストアを追加します。</span><span class="sxs-lookup"><span data-stu-id="983f0-110">Add the primary mirror SQL Server store.</span></span>
    
    3.  <span data-ttu-id="983f0-111">SQL Server のログ配布データベースを有効にします。</span><span class="sxs-lookup"><span data-stu-id="983f0-111">Enable the SQL Server Log Shipping database.</span></span>
    
    4.  <span data-ttu-id="983f0-112">SQL Server ログ配布のセカンダリ SQL Server ストアを追加します。</span><span class="sxs-lookup"><span data-stu-id="983f0-112">Add the SQL Server Log Shipping secondary SQL Server store.</span></span>
    
    5.  <span data-ttu-id="983f0-113">セカンダリデータベースの SQL Server ストアミラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="983f0-113">Add the SQL Server store mirror for the secondary database.</span></span>
    
    6.  <span data-ttu-id="983f0-114">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="983f0-114">Publish the topology.</span></span>

<span data-ttu-id="983f0-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="983f0-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

