---
title: 'Lync Server 2013: 監視の展開チェックリスト'
description: 'Lync Server 2013: 監視用の展開チェックリスト。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for monitoring
ms:assetid: 4e798370-277c-4391-84b4-13a972b45ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204874(v=OCS.15)
ms:contentKeyID: 48184080
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe3d3293accf6e25c20ae8391f9107ae75fef338
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399141"
---
# <a name="deployment-checklist-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="d0bc1-103">Lync Server 2013 の監視の展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="d0bc1-103">Deployment checklist for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0bc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0bc1-104">

<span> </span></span></span>

<span data-ttu-id="d0bc1-105">_**最終更新日:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="d0bc1-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="d0bc1-106">監視は既に各フロントエンドサーバーにインストールされてライセンス認証されていますが、Microsoft Lync Server 2013 の監視データを実際に収集する前に、いくつかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-106">Although monitoring is already installed and activated on each Front End server, there are still several steps that you must undertake before you can actually being to collect monitoring data for Microsoft Lync Server 2013.</span></span> <span data-ttu-id="d0bc1-107">これらの手順については、次のチェックリストで説明します。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-107">These steps are outlined in the following checklist:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0bc1-108">段階</span><span class="sxs-lookup"><span data-stu-id="d0bc1-108">Phase</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-109">手順</span><span class="sxs-lookup"><span data-stu-id="d0bc1-109">Steps</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-110">役割とグループのメンバーシップ</span><span class="sxs-lookup"><span data-stu-id="d0bc1-110">Role and group membership</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-111">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="d0bc1-111">Documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bc1-112"><strong>必要なハードウェアとソフトウェアのインストール</strong></span><span class="sxs-lookup"><span data-stu-id="d0bc1-112"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bc1-113">監視用のバックエンドデータストアとして機能する、サポートされているバージョンの Microsoft SQL Server をコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-113">Install a supported version of Microsoft SQL Server on the computer that will act as the backend data store for monitoring.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-114">ローカル管理者グループのメンバーでもあるドメインユーザー。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-114">Domain user who is also a member of the local administrators group.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-115"><a href="lync-server-2013-supported-hardware.md">サポートガイドの Lync Server 2013 でサポートされているハードウェア</a></span><span class="sxs-lookup"><span data-stu-id="d0bc1-115"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability guide</span></span></p>
<p><span data-ttu-id="d0bc1-116">サポートガイドの<a href="lync-server-2013-server-software-and-infrastructure-support.md">Lync server 2013 でのサーバーソフトウェアとインフラストラクチャのサポート</a></span><span class="sxs-lookup"><span data-stu-id="d0bc1-116"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability Guide</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bc1-117"><strong>監視をサポートする適切な内部トポロジを作成する</strong></span><span class="sxs-lookup"><span data-stu-id="d0bc1-117"><strong>Create the appropriate internal topology to support monitoring</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bc1-118">Lync Server 2013 トポロジビルダーを使用して、監視データベースをトポロジに追加した後、更新されたトポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-118">Use Lync Server 2013 Topology Builder to add monitoring databases to the topology, then published the updated topology.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-119">トポロジ (ローカルユーザーグループのメンバーであるユーザー) を定義するには、[] を選びます。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-119">To define a topology, a user who is a member of the local users group.</span></span></p>
<p><span data-ttu-id="d0bc1-120">トポロジを公開するには、ドメイン管理者グループと RTCUniversalServerAdmins グループのメンバーであるユーザー。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-120">To publish the topology, a user who is a member if the domain administrators group and the RTCUniversalServerAdmins group.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-121">展開ガイドの<a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Lync Server 2013 でのフロントエンドプールへの監視ストアの関連付け</a></span><span class="sxs-lookup"><span data-stu-id="d0bc1-121"><a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Associating a monitoring store with a Front End pool in Lync Server 2013</a> in the Deployment guide</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bc1-122"><strong>適切な監視設定を有効にする</strong></span><span class="sxs-lookup"><span data-stu-id="d0bc1-122"><strong>Enable the appropriate monitoring settings</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bc1-123">グローバルまたはサイトのスコープで、通話の詳細記録 (CDR) と Quality of Experience (QoE) 監視を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-123">Enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global and/or the site scopes.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-124">RTCUniversalServerAdmins グループのメンバーであるか、CsCdrConfiguration と CsQoEConfiguration コマンドレットへのアクセスを提供する RBAC の役割が割り当てられているユーザー。</span><span class="sxs-lookup"><span data-stu-id="d0bc1-124">A user who is a member of the RTCUniversalServerAdmins group or who has been assigned an RBAC role that provides access to the CsCdrConfiguration and CsQoEConfiguration cmdlets.</span></span></p></td>
<td><p><span data-ttu-id="d0bc1-125">運用ガイドの<a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Lync Server 2013 での通話の記録と音質の設定を構成する</a></span><span class="sxs-lookup"><span data-stu-id="d0bc1-125"><a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</a> in the Operations guide</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d0bc1-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0bc1-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

