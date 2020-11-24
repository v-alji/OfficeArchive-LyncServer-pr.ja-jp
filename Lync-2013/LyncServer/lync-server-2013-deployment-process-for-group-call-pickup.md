---
title: 'Lync Server 2013: グループ通話のピックアップの展開プロセス'
description: 'Lync Server 2013: グループ通話のピックアップの展開プロセス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Group Call Pickup
ms:assetid: 082daeac-e667-4e2d-b78d-8e0901f9f0e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945615(v=OCS.15)
ms:contentKeyID: 51541444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a01409b257c685ae71dfdb13074f2d8ea590cd9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399603"
---
# <a name="deployment-process-for-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="2f429-103">Lync Server 2013 でのグループ通話のピックアップの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="2f429-103">Deployment process for Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f429-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f429-104">

<span> </span></span></span>

<span data-ttu-id="2f429-105">_**最終更新日:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="2f429-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="2f429-106">このセクションでは、グループ通話のピックアップの展開に関連する手順の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f429-106">This section provides an overview of the steps involved in deploying Group Call Pickup.</span></span> <span data-ttu-id="2f429-107">グループ通話のピックアップを構成する前に、enterprise Edition または Standard Edition をエンタープライズボイスと共に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f429-107">You must deploy Enterprise Edition or Standard Edition with Enterprise Voice before you configure Group Call Pickup.</span></span> <span data-ttu-id="2f429-108">エンタープライズ Voip を展開すると、グループ通話のピックアップに必要なコンポーネントがインストールされて有効になります。</span><span class="sxs-lookup"><span data-stu-id="2f429-108">The components required by Group Call Pickup are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="group-call-pickup-deployment-process"></a><span data-ttu-id="2f429-109">グループ通話ピックアップの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="2f429-109">Group Call Pickup Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f429-110">フェーズ</span><span class="sxs-lookup"><span data-stu-id="2f429-110">Phase</span></span></th>
<th><span data-ttu-id="2f429-111">ステップ</span><span class="sxs-lookup"><span data-stu-id="2f429-111">Steps</span></span></th>
<th><span data-ttu-id="2f429-112">必要なグループおよび役割</span><span class="sxs-lookup"><span data-stu-id="2f429-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="2f429-113">「展開」のドキュメント</span><span class="sxs-lookup"><span data-stu-id="2f429-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f429-114">トポロジで SEFAUtil リソースキットツールを有効にする</span><span class="sxs-lookup"><span data-stu-id="2f429-114">Enable the SEFAUtil resource kit tool in the topology</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="2f429-115"><strong>New-CsTrustedApplicationPool</strong> コマンドレットを使用して、新しい信頼済みアプリケーション プールを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f429-115">Use the <strong>New-CsTrustedApplicationPool</strong> cmdlet to create a new trusted application pool.</span></span></p></li>
<li><p><span data-ttu-id="2f429-116"><strong>New-CsTrustedApplication</strong> コマンドレットを使用して、SEFAUtil ツールを信頼済みアプリケーションとして指定します。</span><span class="sxs-lookup"><span data-stu-id="2f429-116">Use the <strong>New-CsTrustedApplication</strong> cmdlet to specify the SEFAUtil tool as trusted application.</span></span></p></li>
<li><p><span data-ttu-id="2f429-117"><strong>Enable-CsTopology</strong> コマンドレットを実行して、トポロジを有効にします。</span><span class="sxs-lookup"><span data-stu-id="2f429-117">Run the <strong>Enable-CsTopology</strong> cmdlet to enable the topology.</span></span></p></li>
<li><p><span data-ttu-id="2f429-118">手順1で作成した信頼されたアプリケーションプール内のフロントエンドサーバーにリソースキットツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="2f429-118">Install the resource kit tools on a Front End Server that is in the trusted application pool created in step 1.</span></span></p></li>
<li><p><span data-ttu-id="2f429-119">SEFAUtil を実行し、展開内のユーザーの着信の転送設定を表示して、SEFAUtil が適切に実行されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f429-119">Verify that SEFAUtil is running correctly by running it to display the call forwarding settings of a user in the deployment.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="2f429-120">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="2f429-120">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="2f429-121"><a href="lync-server-2013-deploy-the-sefautil-tool.md">Deploy the SEFAUtil tool in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="2f429-121"><a href="lync-server-2013-deploy-the-sefautil-tool.md">Deploy the SEFAUtil tool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f429-122">コール パーク オービット テーブルに通話ピックアップの番号範囲を構成する</span><span class="sxs-lookup"><span data-stu-id="2f429-122">Configure call pickup number ranges in the call park orbit table</span></span></p></td>
<td><p><span data-ttu-id="2f429-123"><strong>CSCallParkOrbit</strong>コマンドレットを使用して、通話パークの番号の範囲を作成し、通話のピックアップの範囲を「grouppickup」として割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2f429-123">Use the <strong>New-CSCallParkOrbit</strong> cmdlet to create call pickup number ranges in the call park orbit table and assign the call pickup ranges the type GroupPickup.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="2f429-124">通話パークの軌道の番号範囲を作成、変更、削除、および表示するには、Lync Server 管理シェルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f429-124">You must use Lync Server Management Shell to create, modify, remove, and view Group Call Pickup number ranges in the call park orbit table.</span></span> <span data-ttu-id="2f429-125">グループ通話の集配番号の範囲は Lync Server コントロールパネルでは利用できません。</span><span class="sxs-lookup"><span data-stu-id="2f429-125">Group Call Pickup number ranges are not available in Lync Server Control Panel.</span></span>


</div>
<div>

> [!NOTE]  
> <span data-ttu-id="2f429-p103">既存のダイヤル プランとシームレスに統合するため、番号範囲は、通常、仮想の内線番号のブロックとして構成されます。コール パーク オービット テーブルで Direct Inward Dialing (DID) 番号を範囲番号として指定することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2f429-p103">For seamless integration with existing dial plans, number ranges are typically configured as a block of virtual extensions. Assigning Direct Inward Dialing (DID) numbers as range numbers in the call park orbit table is not supported.</span></span>


</div></td>
<td><p><span data-ttu-id="2f429-128">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="2f429-128">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="2f429-129">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="2f429-129">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="2f429-130">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="2f429-130">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="2f429-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="2f429-131">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2f429-132"><a href="lync-server-2013-configure-call-pickup-group-numbers.md">Lync Server 2013 での通話ピックアップグループ番号の設定</a></span><span class="sxs-lookup"><span data-stu-id="2f429-132"><a href="lync-server-2013-configure-call-pickup-group-numbers.md">Configure call pickup group numbers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f429-133">通話集配番号をユーザーに割り当てて、ユーザーに対してグループ通話のピックアップを有効にする</span><span class="sxs-lookup"><span data-stu-id="2f429-133">Assign a call pickup number to users, and enable Group Call Pickup for the users</span></span></p></td>
<td><p><span data-ttu-id="2f429-134">SEFAUtil リソースキットツールの/enablegrouppickup パラメーターを使用して、グループ通話のピックアップを有効にし、ユーザーに通話の集配番号を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2f429-134">Use the /enablegrouppickup parameter in the SEFAUtil resource kit tool to enable Group Call Pickup and assign a call pickup number for users.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="2f429-135"><a href="lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md">Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にし、グループ番号を割り当てる</a></span><span class="sxs-lookup"><span data-stu-id="2f429-135"><a href="lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f429-136">割り当てられた通話ピックアップ番号をユーザーに通知し、必要な他の番号があるかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="2f429-136">Notify users of their assigned call pickup number and any other number of interest</span></span></p></td>
<td><p><span data-ttu-id="2f429-137">グループ通話のピックアップユーザーに発信された通話は、ユーザーが取得することができるため、ユーザーは複数のグループを監視する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f429-137">Because any user can retrieve a call made to a Group Call Pickup user, users may want to monitor more than one group.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="2f429-138"><a href="lync-server-2013-communicate-group-call-pickup-assignment-to-users.md">グループ通話の集配の課題を Lync Server 2013 のユーザーに伝える</a></span><span class="sxs-lookup"><span data-stu-id="2f429-138"><a href="lync-server-2013-communicate-group-call-pickup-assignment-to-users.md">Communicate Group Call Pickup assignments to users in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f429-139">グループ通話の集配の展開を確認する</span><span class="sxs-lookup"><span data-stu-id="2f429-139">Verify your Group Call Pickup deployment</span></span></p></td>
<td><p><span data-ttu-id="2f429-140">通話の発信と取得をテストし、構成が予想どおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f429-140">Test placing and retrieving calls to make sure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="2f429-141"><a href="lync-server-2013-optional-verify-the-group-call-pickup-deployment.md">省略Lync Server 2013 でグループ通話のピックアップの展開を確認する</a></span><span class="sxs-lookup"><span data-stu-id="2f429-141"><a href="lync-server-2013-optional-verify-the-group-call-pickup-deployment.md">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="2f429-142">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f429-142">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

