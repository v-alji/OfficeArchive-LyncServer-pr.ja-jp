---
title: Lync Server 2013 for A/V 会議用の展開チェックリスト
description: Lync Server 2013 for A/V 会議の展開チェックリスト
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for A/V conferencing
ms:assetid: 6d47426f-6559-407b-9ac1-2453f0b7a2a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619183(v=OCS.15)
ms:contentKeyID: 49733684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9a4584172ed4c01eb163ea51aa4f62c2ce75185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429756"
---
# <a name="deployment-checklist-for-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="2f998-103">Lync Server 2013 での A/V 会議の展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="2f998-103">Deployment checklist for A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f998-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f998-104">

<span> </span></span></span>

<span data-ttu-id="2f998-105">_**最終更新日:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="2f998-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="2f998-106">他の Lync Server 2013 コンポーネントの展開と同じように、A/V 会議の展開では、会議を組み込んだトポロジを作成して公開するために、トポロジビルダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f998-106">As with deployment of your other Lync Server 2013 components, deployment of A/V conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="2f998-107">展開シーケンス</span><span class="sxs-lookup"><span data-stu-id="2f998-107">Deployment Sequence</span></span>

<span data-ttu-id="2f998-108">最初のトポロジを展開するとき、または少なくとも1つのフロントエンドプールまたは Standard Edition サーバーを展開した後で、会議を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="2f998-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="2f998-109">会議展開プロセス</span><span class="sxs-lookup"><span data-stu-id="2f998-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="2f998-110">次の表は、既存のトポロジに会議を展開するために必要な手順の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f998-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f998-111">段階</span><span class="sxs-lookup"><span data-stu-id="2f998-111">Phase</span></span></th>
<th><span data-ttu-id="2f998-112">手順</span><span class="sxs-lookup"><span data-stu-id="2f998-112">Steps</span></span></th>
<th><span data-ttu-id="2f998-113">役割とグループ メンバーシップ</span><span class="sxs-lookup"><span data-stu-id="2f998-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="2f998-114">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="2f998-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f998-115"><strong>必要なハードウェアとソフトウェアのインストール</strong></span><span class="sxs-lookup"><span data-stu-id="2f998-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="2f998-116">会議は、フロントエンドプールと Standard Edition サーバーのフロントエンドサーバー上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="2f998-116">Conferencing runs on Front End Servers of a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="2f998-117">これらのサーバーのインストールに必要なもの以外には、追加のハードウェア要件やソフトウェア要件はありません。</span><span class="sxs-lookup"><span data-stu-id="2f998-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="2f998-118">Lync Server 2013 は、PowerPoint プレゼンテーションの共有とレンダリングを処理するために、Office Web Apps と Office Web Apps サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="2f998-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="2f998-119">Office Web Apps サーバーのインストールと構成の詳細については、「 <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Office Web Apps サーバーおよび Lync server 2013 との統合を構成する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f998-119">For details about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="2f998-120">ローカル Administrators グループのメンバーであるドメイン ユーザー</span><span class="sxs-lookup"><span data-stu-id="2f998-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="2f998-121"><a href="lync-server-2013-supported-hardware.md">サポートされているドキュメントの Lync Server 2013 でサポートされているハードウェア</a></span><span class="sxs-lookup"><span data-stu-id="2f998-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="2f998-122">サポートドキュメントの<a href="lync-server-2013-server-software-and-infrastructure-support.md">Lync server 2013 でのサーバーソフトウェアとインフラストラクチャのサポート</a></span><span class="sxs-lookup"><span data-stu-id="2f998-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="2f998-123">計画ドキュメントの<a href="lync-server-2013-determining-your-system-requirements.md">Lync Server 2013 のシステム要件を決定</a>する。</span><span class="sxs-lookup"><span data-stu-id="2f998-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="2f998-124">計画ドキュメントの<a href="lync-server-2013-technical-requirements-for-archiving.md">Lync Server 2013 でのアーカイブの技術要件</a>。</span><span class="sxs-lookup"><span data-stu-id="2f998-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f998-125"><strong>会議をサポートするために適切な内部トポロジの作成</strong></span><span class="sxs-lookup"><span data-stu-id="2f998-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="2f998-126">トポロジに会議を追加するには、トポロジビルダーを実行して、トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="2f998-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="2f998-127">トポロジを定義するには、ローカル Users グループのメンバーであるアカウント</span><span class="sxs-lookup"><span data-stu-id="2f998-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="2f998-128">トポロジを公開するには、ドメイン管理者グループと RTCUniversalServerAdmins グループのメンバーであり、Lync Server 2013 ファイルストアで使用するフルコントロールのアクセス許可 (読み取り/書き込み/変更) を持つアカウント (トポロジビルダーが必要な Dacl を構成できるようにする)</span><span class="sxs-lookup"><span data-stu-id="2f998-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="2f998-129">展開ドキュメントで、「<a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">トポロジビルダーでの Lync Server 2013 のトポロジを定義して構成する」</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f998-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f998-130"><strong>会議のポリシーとサポートを構成する</strong></span><span class="sxs-lookup"><span data-stu-id="2f998-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="2f998-131">Lync Server 2013 コントロールパネルまたは Lync Server 管理シェルを使用して、会議の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="2f998-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="2f998-132">RTCUniversalServerAdmins group (Windows PowerShell のみ) またはユーザーを [] または [CSAdministrator] の役割に割り当てる</span><span class="sxs-lookup"><span data-stu-id="2f998-132">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="2f998-133">運用ドキュメントの<a href="lync-server-2013-conferencing-policies.md">Lync Server 2013 での会議ポリシー</a> 。</span><span class="sxs-lookup"><span data-stu-id="2f998-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2f998-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f998-134">See Also</span></span>


[<span data-ttu-id="2f998-135">Lync Server 2013 での会議の概要</span><span class="sxs-lookup"><span data-stu-id="2f998-135">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)  
[<span data-ttu-id="2f998-136">Lync Server 2013 での会議の要件の定義</span><span class="sxs-lookup"><span data-stu-id="2f998-136">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)  
  

<span data-ttu-id="2f998-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f998-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

