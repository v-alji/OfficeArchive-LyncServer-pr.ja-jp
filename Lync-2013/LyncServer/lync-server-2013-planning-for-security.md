---
title: 'Lync Server 2013: セキュリティの計画'
description: 'Lync Server 2013: セキュリティの計画'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for security
ms:assetid: 17eeba87-cafa-4e9b-852d-c017a7d10d59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342827(v=OCS.15)
ms:contentKeyID: 56107267
ms.date: 06/22/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1abc02aa3f42a6b12c66c621b071e0b3ddb545c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424444"
---
# <a name="planning-for-security-in-lync-server-2013"></a><span data-ttu-id="67c2a-103">Lync Server 2013 のセキュリティの計画</span><span class="sxs-lookup"><span data-stu-id="67c2a-103">Planning for security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67c2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67c2a-104">

<span> </span></span></span>

<span data-ttu-id="67c2a-105">_**最終更新日:** 2016-06-22_</span><span class="sxs-lookup"><span data-stu-id="67c2a-105">_**Topic Last Modified:** 2016-06-22_</span></span>

<span data-ttu-id="67c2a-106">このセキュリティセクションを使用して、Lync Server 2013 の展開に関するセキュリティリスクを評価して管理します。</span><span class="sxs-lookup"><span data-stu-id="67c2a-106">Use this security section to assess and manage security risks to your deployment of Lync Server 2013.</span></span>

<span data-ttu-id="67c2a-107">Lync Server 2013 の展開が妥当である場合でも、ネットワークには、独自のセキュリティドキュメントが含まれているコンポーネントが含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67c2a-107">Even if your Lync Server 2013 deployment is modest, you probably have components in your network that have their own security documentation.</span></span> <span data-ttu-id="67c2a-108">そのため、このセクションでは、展開に関連するすべてのコンポーネントと領域のセキュリティに関するすべての側面について説明しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="67c2a-108">Therefore, it is unlikely that this section covers all aspects of security for all components and areas that are pertinent to your deployment.</span></span>

<span data-ttu-id="67c2a-109">このセクションは、Lync Server 2013 の展開のセキュリティに対応するための出発点として使用してください。</span><span class="sxs-lookup"><span data-stu-id="67c2a-109">Use this section as a starting point to address the security of your Lync Server 2013 deployment.</span></span> <span data-ttu-id="67c2a-110">一般的なガイドラインと、最も一般的なセキュリティリスクを評価および管理するためのベストプラクティスを紹介します。</span><span class="sxs-lookup"><span data-stu-id="67c2a-110">It provides general guidelines and best practices for assessing and managing the most common security risks.</span></span> <span data-ttu-id="67c2a-111">各トピックの最後には、追加の製品とセキュリティのリソースが記載されています。</span><span class="sxs-lookup"><span data-stu-id="67c2a-111">Additional product and security resources are listed at the end of each topic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="67c2a-112">セキュリティは、絶えず進化するトピックです。</span><span class="sxs-lookup"><span data-stu-id="67c2a-112">Security is a constantly evolving topic.</span></span> <span data-ttu-id="67c2a-113">新しい脅威や解決策が発生したため、古いドキュメント、ソリューション、方法、および手順は最新の資料に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="67c2a-113">As new threats and solutions arise, outdated documents, solutions, methods, and procedures should be replaced with up-to-date material.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67c2a-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="67c2a-114">In This Section</span></span>

  - [<span data-ttu-id="67c2a-115">Lync Server 2013 の主要なセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="67c2a-115">Key security features in Lync Server 2013</span></span>](lync-server-2013-key-security-features.md)

  - [<span data-ttu-id="67c2a-116">モダンなコンピューティングでの一般的なセキュリティの脅威</span><span class="sxs-lookup"><span data-stu-id="67c2a-116">Common security threats in modern day computing</span></span>](lync-server-2013-common-security-threats-in-modern-day-computing.md)

  - [<span data-ttu-id="67c2a-117">Lync Server 2013 用のウイルス スキャン除外範囲</span><span class="sxs-lookup"><span data-stu-id="67c2a-117">Antivirus scanning exclusions for Lync Server 2013</span></span>](lync-server-2013-antivirus-scanning-exclusions.md)

  - [<span data-ttu-id="67c2a-118">Lync Server 2013 のセキュリティフレームワーク</span><span class="sxs-lookup"><span data-stu-id="67c2a-118">Security framework for Lync Server 2013</span></span>](lync-server-2013-security-framework-for-lync-server.md)

  - [<span data-ttu-id="67c2a-119">Lync Server 2013 向けのコアインフラストラクチャへの脅威への対応</span><span class="sxs-lookup"><span data-stu-id="67c2a-119">Addressing threats to your core infrastructure for Lync Server 2013</span></span>](lync-server-2013-addressing-threats-to-your-core-infrastructure.md)

  - [<span data-ttu-id="67c2a-120">Lync Server 2013 で SQL Server の非標準ポートおよびエイリアスを展開する</span><span class="sxs-lookup"><span data-stu-id="67c2a-120">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>](deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013.md)

<span data-ttu-id="67c2a-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67c2a-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

