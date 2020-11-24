---
title: 'Lync Server 2013: 常設チャット サーバーの展開チェックリスト'
description: 'Lync Server 2013: 常設チャットサーバー用の展開チェックリスト'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Persistent Chat Server
ms:assetid: b1108f8f-88a2-4660-8086-d25ba76f7239
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412851(v=OCS.15)
ms:contentKeyID: 48185155
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28d96da5e2961634e6a81450796e5d1ae3426819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399140"
---
# <a name="deployment-checklist-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="0d0b6-103">Lync Server 2013 の常設チャット サーバーの展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="0d0b6-103">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d0b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d0b6-104">

<span> </span></span></span>

<span data-ttu-id="0d0b6-105">_**最終更新日:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="0d0b6-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="0d0b6-106">Lync Server 2013、常設チャットサーバーを展開するには、正しい順序で展開し、必要なすべての展開手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-106">Deployment of Lync Server 2013, Persistent Chat Server requires that you deploy it in the correct sequence and that you complete all required deployment steps.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="0d0b6-107">展開シーケンス</span><span class="sxs-lookup"><span data-stu-id="0d0b6-107">Deployment Sequence</span></span>

<span data-ttu-id="0d0b6-108">少なくとも1つの Lync Server 2013、フロントエンドプール、または1つの Lync Server 2013、Standard Edition server を含む、最初のトポロジを展開した後、常設チャットサーバーを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-108">You can deploy Persistent Chat Server after you deploy your initial topology, including at least one Lync Server 2013, Front End pool or one Lync Server 2013, Standard Edition server.</span></span> <span data-ttu-id="0d0b6-109">このトピックでは、既存の展開に追加して、常設チャットサーバーを展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-109">This topic describes how to deploy Persistent Chat Server by adding it to an existing deployment.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="0d0b6-110">展開プロセス</span><span class="sxs-lookup"><span data-stu-id="0d0b6-110">Deployment Process</span></span>

<span data-ttu-id="0d0b6-111">次の表は、常設チャットサーバーを展開するための基本的な手順と、詳細情報のリンクを示しています。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-111">The following table lists the basic steps to deploy Persistent Chat Server and provides links for more details.</span></span>

### <a name="persistent-chat-server-deployment-process"></a><span data-ttu-id="0d0b6-112">常設チャットサーバーの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="0d0b6-112">Persistent Chat Server Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0d0b6-113">タスク</span><span class="sxs-lookup"><span data-stu-id="0d0b6-113">Task</span></span></th>
<th><span data-ttu-id="0d0b6-114">ステップ</span><span class="sxs-lookup"><span data-stu-id="0d0b6-114">Steps</span></span></th>
<th><span data-ttu-id="0d0b6-115">必要な役割とグループ メンバーシップ</span><span class="sxs-lookup"><span data-stu-id="0d0b6-115">Required roles and group memberships</span></span></th>
<th><span data-ttu-id="0d0b6-116">関連トピック</span><span class="sxs-lookup"><span data-stu-id="0d0b6-116">Related topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d0b6-117"><strong>必要なハードウェアとソフトウェアのインストール</strong></span><span class="sxs-lookup"><span data-stu-id="0d0b6-117"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0b6-118">システム要件を満たすハードウェアに、次をインストールします。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-118">On hardware that meets system requirements, install the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-119">常設チャットサーバーのフロントエンドサーバーで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-119">On the Persistent Chat Server Front End Servers:</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="0d0b6-120">システム要件を満たすオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="0d0b6-120">An operating system that meets system requirements</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-121">Lync Server 2013 を実行しているコンピューターのソフトウェアの前提条件</span><span class="sxs-lookup"><span data-stu-id="0d0b6-121">Software prerequisites for computers running Lync Server 2013</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-122">常設チャットサーバーデータベースをホストするサーバー上の SQL Server</span><span class="sxs-lookup"><span data-stu-id="0d0b6-122">SQL Server on the server that will host Persistent Chat Server database</span></span></p></li>
</ul>
<p><span data-ttu-id="0d0b6-123">常設チャットサーバーのコンプライアンスが必要な場合:</span><span class="sxs-lookup"><span data-stu-id="0d0b6-123">If Persistent Chat Server compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-124">常設チャットサーバーのコンプライアンスデータベースをホストするサーバー上の SQL Server</span><span class="sxs-lookup"><span data-stu-id="0d0b6-124">SQL Server on the server that will host Persistent Chat Server compliance database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="0d0b6-125">ローカルの Administrators グループのメンバーであるユーザー。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-125">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-126"><a href="lync-server-2013-supported-hardware.md">サポートされているドキュメントの Lync Server 2013 でサポートされているハードウェア</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-126"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="0d0b6-127">サポートドキュメントの<a href="lync-server-2013-server-software-and-infrastructure-support.md">Lync server 2013 でのサーバーソフトウェアとインフラストラクチャのサポート</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="0d0b6-128"><a href="lync-server-2013-determining-your-system-requirements.md">Lync Server 2013 システム要件の決定</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="0d0b6-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Lync Server 2013 の常設チャットサーバーの技術要件</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Technical requirements for Persistent Chat Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d0b6-130"><strong>常設チャットサーバーをサポートするための適切な内部トポロジを作成します (また、必要に応じて常設チャットのコンプライアンスも可能)。</strong></span><span class="sxs-lookup"><span data-stu-id="0d0b6-130"><strong>Create the appropriate internal topology to support Persistent Chat Server (and optionally, Persistent Chat compliance)</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0b6-131">トポロジビルダーを実行して、常設チャットサーバープールをトポロジに追加します。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-131">Run Topology Builder to add a Persistent Chat Server pool to your topology:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-132">常設チャットサーバーコンポーネントをトポロジに追加する</span><span class="sxs-lookup"><span data-stu-id="0d0b6-132">Add Persistent Chat Server components to the topology</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-133">常設チャットサーバーストア用の SQL Server データベースを作成します (および障害回復用のバックアップ SQL Server)。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-133">Create a SQL Server database for the Persistent Chat Server store (and a backup SQL Server for disaster recovery)</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-134">新しい Lync ファイルストアを定義するか、既存の Lync ファイルストアで常設チャットサーバーファイルを使用する</span><span class="sxs-lookup"><span data-stu-id="0d0b6-134">Define a new Lync File Store or use an existing Lync File Store for Persistent Chat Server files</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-135">要求をこの常設チャットサーバープールにルーティングできる Lync Server 2013 プールを関連付ける</span><span class="sxs-lookup"><span data-stu-id="0d0b6-135">Associate the Lync Server 2013 pool that can route requests to this Persistent Chat Server pool</span></span></p></li>
</ul>
<p><span data-ttu-id="0d0b6-136">常設チャット コンプライアンスが必要な場合</span><span class="sxs-lookup"><span data-stu-id="0d0b6-136">If Persistent Chat compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-137">常設チャットのコンプライアンスストアを追加する</span><span class="sxs-lookup"><span data-stu-id="0d0b6-137">Add Persistent Chat Compliance Store</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-138">コンプライアンスを有効にするには、[常設チャットサーバープールの定義] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-138">Click the Persistent Chat Server pool definition check box for enabling compliance</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-139">トポロジを公開する</span><span class="sxs-lookup"><span data-stu-id="0d0b6-139">Publish the topology</span></span></p></li>
</ul>
<p><span data-ttu-id="0d0b6-140">Standard Edition に常設チャットサーバーをインストールする場合は、常設チャットサーバープールの完全修飾ドメイン名 (FQDN) が Standard Edition サーバーと一致する必要があります。 SQL Server データベースは、Standard Edition サーバー上の SQL Server Express インスタンスに併置されています。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-140">If you install Persistent Chat Server on Standard Edition, the fully qualified domain name (FQDN) of the Persistent Chat Server pool must match the Standard Edition server, and the SQL Server databases are collocated on the SQL Server Express instance on the Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-141">トポロジを定義するには、ローカルの Users グループのメンバーであるアカウント。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-141">To define a topology, an account that is a member of the local Users group.</span></span></p>
<p><span data-ttu-id="0d0b6-142">トポロジを公開するには、ドメイン管理者グループと RTCUniversalServerAdmins グループのメンバーであるアカウントであり、ユーザーは、常設チャットサーバーファイル用の Lync ファイルストアに対するフルコントロールのアクセス許可 (読み取り/書き込み/変更) を持っている必要があります (これにより、トポロジビルダーは必要な Dacl を構成できるようになります)。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-142">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and the user should also have full control permissions (read/write/modify) on the Lync File Store for Persistent Chat Server files (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-143">展開ドキュメントの<a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Lync server 2013 での展開への常設チャットサーバーの追加</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d0b6-144"><strong>常設チャット サーバーの展開</strong></span><span class="sxs-lookup"><span data-stu-id="0d0b6-144"><strong>Deploy Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0b6-145">常設チャットサーバーを実行しているすべてのコンピューターで Lync Server のセットアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-145">Run the Lync Server setup on all the computers running Persistent Chat Server.</span></span> <span data-ttu-id="0d0b6-146">常設チャットサーバーのセットアップは Lync Server 2013 展開ウィザードに統合されているため、次の手順で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-146">The Persistent Chat Server setup is integrated into the Lync Server 2013 Deployment wizard that provides the following instructions:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-147">ローカル管理ストアを展開する。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-147">Deploy local management store</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-148">常設チャットサーバーサービスをインストールする</span><span class="sxs-lookup"><span data-stu-id="0d0b6-148">Install Persistent Chat Server services</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-149">証明書を要求および割り当てる。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-149">Request and assign certificates</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-150">サービスを実行および開始する。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-150">Run and start the services</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="0d0b6-151">ローカルの Administrators グループのメンバーであるユーザー。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-151">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-152">展開ドキュメントの<a href="lync-server-2013-deploying-persistent-chat-server.md">Lync server 2013 での常設チャットサーバーの展開</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d0b6-153"><strong>常設チャット管理者の作成</strong></span><span class="sxs-lookup"><span data-stu-id="0d0b6-153"><strong>Create a Persistent Chat administrator</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0b6-154">ユーザーを CsPersistentChatAdministrator セキュリティ グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-154">Add users to the CsPersistentChatAdministrator security group.</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-155">ドメイン管理者のメンバーであるユーザー。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-155">Any user who is a member of domain administrators.</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-156">展開ドキュメントの<a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Lync Server 2013 での常設チャット管理者の追加</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Adding a Persistent Chat administrator in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d0b6-157"><strong>常設チャット サーバーの構成</strong></span><span class="sxs-lookup"><span data-stu-id="0d0b6-157"><strong>Configure Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0b6-158">次のようにユーザーを構成します。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-158">Configure users:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d0b6-159">ユーザは、常設チャットサーバにアクセスするためにポリシーによって有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-159">User has to be enabled by policy to access Persistent Chat Server.</span></span> <span data-ttu-id="0d0b6-160">既定では、ポリシーはすべてのユーザーに対してオフになっており、グローバル/サイト/プール/ユーザー スコープで定義できます。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-160">By default, the policy is turned off for all users and can be defined at global/site/pool/user scopes.</span></span></p></li>
<li><p><span data-ttu-id="0d0b6-161">設定の構成</span><span class="sxs-lookup"><span data-stu-id="0d0b6-161">Configure settings</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="0d0b6-p104">ユーザーは CsPersistentChatAdministrator のメンバーであることが必要です。ポリシーを変更するには、ユーザーは最低でも CsUserAdministrator であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-p104">User must be a member of CsPersistentChatAdministrator. To change policy, user must be in CsUserAdministrator, at a minimum.</span></span></p></td>
<td><p><span data-ttu-id="0d0b6-164">展開ドキュメントの<a href="lync-server-2013-configuring-persistent-chat-server.md">Lync server 2013 での常設チャットサーバーの構成</a></span><span class="sxs-lookup"><span data-stu-id="0d0b6-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configuring Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="0d0b6-165">1つ以上の常設チャットサーバープールを展開できます。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-165">You can deploy one or more Persistent Chat Server pools.</span></span> <span data-ttu-id="0d0b6-166">複数の常設チャットサーバープールをサポートしており、特定の地域で生成されたデータをその地域内に維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-166">We support multiple Persistent Chat Server pools for regulatory reasons whereby data generated in a given region is required to stay in that region.</span></span> <span data-ttu-id="0d0b6-167">たとえば、Zurich で常設チャットサーバープールを展開し、スイスのデータに関する規制に準拠するために、ユーザーは、アクセス権を持っている常設チャットサーバープールの会議室に接続できます。</span><span class="sxs-lookup"><span data-stu-id="0d0b6-167">For example, if you deploy a Persistent Chat Server pool in Chicago, and another in Zurich to comply with regulations for data in Switzerland, users can connect to rooms in both the Persistent Chat Server pools, provided they have access.</span></span>



<span data-ttu-id="0d0b6-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d0b6-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

