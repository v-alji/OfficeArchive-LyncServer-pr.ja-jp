---
title: 'Lync Server 2013: 役割ベースのアクセス制御の計画'
description: 'Lync Server 2013: ロールベースのアクセス制御の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for role-based access control (RBAC)
ms:assetid: 41204ba3-ce5b-41a8-a6c3-b444468fa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425917(v=OCS.15)
ms:contentKeyID: 48183962
ms.date: 01/28/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 971b3353694a1cdd53d88452717e6a9a360c6870
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400184"
---
# <a name="planning-for-role-based-access-control-in-lync-server-2013"></a><span data-ttu-id="13dc1-103">Lync Server 2013 での役割ベースのアクセス制御の計画</span><span class="sxs-lookup"><span data-stu-id="13dc1-103">Planning for role-based access control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13dc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13dc1-104">

<span> </span></span></span>

<span data-ttu-id="13dc1-105">_**最終更新日:** 2015-01-27_</span><span class="sxs-lookup"><span data-stu-id="13dc1-105">_**Topic Last Modified:** 2015-01-27_</span></span>

<span data-ttu-id="13dc1-106">セキュリティの高い標準を維持しながら、管理タスクの委任を可能にするために、Lync Server 2013 は役割ベースのアクセス制御 (RBAC) を提供しています。</span><span class="sxs-lookup"><span data-stu-id="13dc1-106">To enable you to delegate administrative tasks while maintaining high standards for security, Lync Server 2013 offers role-based access control (RBAC).</span></span> <span data-ttu-id="13dc1-107">RBAC では、管理者権限が付与され、管理者ロールにユーザーが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-107">With RBAC, administrative privilege is granted by assigning users to administrative roles.</span></span> <span data-ttu-id="13dc1-108">Lync Server 2013 には、豊富な組み込みの管理者ロールが用意されています。また、新しいロールを作成して、新しい役割ごとにコマンドレットのカスタムリストを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-108">Lync Server 2013 includes a rich set of built-in administrative roles, and also enables you to create new roles and specify a custom list of cmdlets for each new role.</span></span> <span data-ttu-id="13dc1-109">また、定義済み RBAC 役割およびカスタム RBAC 役割の許可されたタスクに、コマンドレットのスクリプトを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-109">You can also add scripts of cmdlets to the allowed tasks of both predefined and custom RBAC roles.</span></span>

<div>

## <a name="better-server-security-and-centralization"></a><span data-ttu-id="13dc1-110">サーバーのセキュリティと集中化の向上</span><span class="sxs-lookup"><span data-stu-id="13dc1-110">Better Server Security and Centralization</span></span>

<span data-ttu-id="13dc1-111">RBAC では、アクセスと承認はユーザーの Lync Server の役割に基づいています。</span><span class="sxs-lookup"><span data-stu-id="13dc1-111">With RBAC, access and authorization is based precisely on a user’s Lync Server role.</span></span> <span data-ttu-id="13dc1-112">これにより、"最低限の権限" というセキュリティ慣行を使用できるようになり、管理者とユーザーには、その職務に必要な権利のみが付与されます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-112">This enables use of the security practice of "least privilege," granting administrators and users only the rights that are necessary for their job.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="13dc1-113">RBAC の制限は、Lync Server コントロールパネルまたは Lync Server 管理シェルを使用して、リモートで作業している管理者に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-113">RBAC restrictions work only on administrators working remotely, using either the Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="13dc1-114">Lync Server を実行しているサーバーに座っているユーザーは、RBAC によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="13dc1-114">A user sitting at a server running Lync Server is not restricted by RBAC.</span></span> <span data-ttu-id="13dc1-115">したがって、Lync Server の物理的なセキュリティは、RBAC の制限を維持することが重要です。</span><span class="sxs-lookup"><span data-stu-id="13dc1-115">Therefore, physical security of your Lync Server is important to preserve RBAC restrictions.</span></span>



</div>

</div>

<div>

## <a name="roles-and-scope"></a><span data-ttu-id="13dc1-116">役割と範囲</span><span class="sxs-lookup"><span data-stu-id="13dc1-116">Roles and Scope</span></span>

<span data-ttu-id="13dc1-117">RBAC では、特定の種類の管理者または技術者のために役立つように設計されたコマンドレットのリストを使用する *役割* が有効になります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-117">In RBAC, a *role* is enabled to use a list of cmdlets, designed to be useful for a certain type of administrator or technician.</span></span> <span data-ttu-id="13dc1-118">*スコープ* とは、役割で定義されているコマンドレットで操作できる一連のオブジェクトのことです。</span><span class="sxs-lookup"><span data-stu-id="13dc1-118">A *scope* is the set of objects which the cmdlets defined in a role can operate on.</span></span> <span data-ttu-id="13dc1-119">範囲に影響を与えるオブジェクトは、ユーザーアカウント (組織単位でグループ化) または (サイトごとにグループ化された) いずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-119">The objects that scope affects can be either user accounts (grouped by organizational unit) or servers (grouped by site).</span></span>

<span data-ttu-id="13dc1-120">次の表に、Lync Server で定義されている役割と、各タスクの種類の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-120">The following table lists the predefined roles in Lync Server, and gives a general overview of the types of tasks each can do.</span></span> <span data-ttu-id="13dc1-121">4番目の列には、各 Lync Server の役割に類似した Microsoft Exchange Server の役割 (存在する場合) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-121">The fourth column shows the similar Microsoft Exchange Server role for each Lync Server role, if there is one.</span></span>

### <a name="predefined-administrative-roles"></a><span data-ttu-id="13dc1-122">定義済みの管理者ロール</span><span class="sxs-lookup"><span data-stu-id="13dc1-122">Predefined Administrative Roles</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13dc1-123">ロール</span><span class="sxs-lookup"><span data-stu-id="13dc1-123">Role</span></span></th>
<th><span data-ttu-id="13dc1-124">許可されたタスク</span><span class="sxs-lookup"><span data-stu-id="13dc1-124">Tasks allowed</span></span></th>
<th><span data-ttu-id="13dc1-125">基になる Active Directory グループ</span><span class="sxs-lookup"><span data-stu-id="13dc1-125">Underlying Active Directory group</span></span></th>
<th><span data-ttu-id="13dc1-126">同等の交換</span><span class="sxs-lookup"><span data-stu-id="13dc1-126">Exchange equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-127">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-127">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-128">すべての管理タスクを実行し、ロールの作成やロールへのユーザーの割り当てなどのすべての設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-128">Can perform all administrative tasks and modify all settings, including creating roles and assigning users to roles.</span></span> <span data-ttu-id="13dc1-129">新しいサイト、プール、およびサービスを追加して展開を展開できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-129">Can expand a deployment by adding new sites, pools, and services.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-130">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-130">CSAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-131">組織管理</span><span class="sxs-lookup"><span data-stu-id="13dc1-131">Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13dc1-132">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-132">CsUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-133">Lync Server のユーザーを有効または無効にしたり、ユーザーを移動したり、既存のポリシーをユーザーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-133">Can enable and disable users for Lync Server, move users and assign existing policies to users.</span></span> <span data-ttu-id="13dc1-134">ポリシーを変更できません。</span><span class="sxs-lookup"><span data-stu-id="13dc1-134">Cannot modify policies.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-135">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-135">CSUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-136">メールの宛先</span><span class="sxs-lookup"><span data-stu-id="13dc1-136">Mail Recipients</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-137">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-137">CsVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-138">音声関連の設定とポリシーの作成、構成、管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-138">Can create, configure, and manage voice-related settings and policies.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-139">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-139">CSVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-140">該当なし</span><span class="sxs-lookup"><span data-stu-id="13dc1-140">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13dc1-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-141">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-142">サーバーとサービスの管理、監視、トラブルシューティングを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-142">Can manage, monitor, and troubleshoot servers and services.</span></span> <span data-ttu-id="13dc1-143">サーバーへの新しい接続の禁止、サービスの停止と開始、ソフトウェアの更新プログラムの適用を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-143">Can prevent new connections to servers, stop and start services, and apply software updates.</span></span> <span data-ttu-id="13dc1-144">グローバル構成の影響を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="13dc1-144">Cannot make changes with global configuration impact.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-145">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-145">CSServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-146">サーバー管理</span><span class="sxs-lookup"><span data-stu-id="13dc1-146">Server Management</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-147">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-147">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-148">展開の正常性を監視するために、ユーザーやサーバーの情報などの展開を表示できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-148">Can view the deployment, including user and server information, in order to monitor deployment health.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-149">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-149">CSViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-150">組織管理の View-Only</span><span class="sxs-lookup"><span data-stu-id="13dc1-150">View-Only Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13dc1-151">CsHelpDesk</span><span class="sxs-lookup"><span data-stu-id="13dc1-151">CsHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="13dc1-152">ユーザーのプロパティやポリシーなどの展開を表示できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-152">Can view the deployment, including user's properties and policies.</span></span> <span data-ttu-id="13dc1-153">特定のトラブルシューティングタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-153">Can run specific troubleshooting tasks.</span></span> <span data-ttu-id="13dc1-154">ユーザーのプロパティやポリシー、サーバーの構成、またはサービスを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="13dc1-154">Cannot change user properties or policies, server configuration, or services.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-155">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="13dc1-155">CSHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="13dc1-156">ヘルプデスク</span><span class="sxs-lookup"><span data-stu-id="13dc1-156">HelpDesk</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-157">CsArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-157">CsArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-158">アーカイブの構成とポリシーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-158">Can modify archiving configuration and policies.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-159">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-159">CSArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-160">保持管理、法的保持</span><span class="sxs-lookup"><span data-stu-id="13dc1-160">Retention Management, Legal Hold</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13dc1-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-161">CsResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-162">サイト内の応答グループアプリケーションの構成を管理できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-162">Can manage the configuration of the Response Group application within a site.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-163">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-163">CSResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-164">該当なし</span><span class="sxs-lookup"><span data-stu-id="13dc1-164">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-165">CsLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-165">CsLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-166">9-1-1 (E9) の管理を強化するための最小レベルの権限 (E9 の場所とネットワーク識別子の作成、および相互の関連付けを含む)。</span><span class="sxs-lookup"><span data-stu-id="13dc1-166">Lowest level of rights for Enhanced 9-1-1 (E9-1-1) management, including creating E9-1-1 locations and network identifiers, and associating these with each other.</span></span> <span data-ttu-id="13dc1-167">この役割は、常にグローバルスコープに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-167">This role is always assigned with a global scope.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-168">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-168">CSLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-169">該当なし</span><span class="sxs-lookup"><span data-stu-id="13dc1-169">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13dc1-170">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="13dc1-170">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="13dc1-171">特定の応答グループを管理できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-171">Can manage specific response groups.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-172">CSResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="13dc1-172">CSResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="13dc1-173">該当なし</span><span class="sxs-lookup"><span data-stu-id="13dc1-173">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13dc1-174">CsPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-174">CsPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-175">常設チャット機能と特定の常設チャットルームを管理できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-175">Can manage the Persistent Chat feature and specific Persistent Chat rooms.</span></span></p></td>
<td><p><span data-ttu-id="13dc1-176">CSPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="13dc1-176">CSPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="13dc1-177">該当なし</span><span class="sxs-lookup"><span data-stu-id="13dc1-177">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13dc1-178">Lync Server に組み込まれているすべての定義済みロールにはグローバルスコープがあります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-178">All predefined roles shipped in Lync Server have a global scope.</span></span> <span data-ttu-id="13dc1-179">最低限の権限適用方法を実行するには、限定されたサーバーまたはユーザーのセットのみを管理する場合は、グローバル範囲の役割にユーザーを割り当てないでください。</span><span class="sxs-lookup"><span data-stu-id="13dc1-179">To follow least privilege practices, you should not assign users to roles with global scope if they are going to administer only a limited set of servers or users.</span></span> <span data-ttu-id="13dc1-180">これを実現するために、既存のロールに基づいているが、スコープが制限されているロールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-180">To accomplish this, you can create roles which are based on an existing role, but with a more limited scope.</span></span>

<div>

## <a name="creating-a-scoped-role"></a><span data-ttu-id="13dc1-181">スコープ指定された役割の作成</span><span class="sxs-lookup"><span data-stu-id="13dc1-181">Creating a Scoped Role</span></span>

<span data-ttu-id="13dc1-182">制限されたスコープ (スコープ指定された役割) を持つ役割を作成する場合は、スコープを指定し、基になる既存の役割と、役割を割り当てられる Active Directory グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-182">When you create a role with limited scope (a scoped role), you specify the scope, along with the existing role it is based on and the Active Directory group to be assigned the role.</span></span> <span data-ttu-id="13dc1-183">指定した Active Directory グループは、既に作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-183">The Active Directory group you specify must already be created.</span></span> <span data-ttu-id="13dc1-184">次のコマンドレットは、事前に定義されている管理者ロールの1つであるという権限を持ち、スコープが制限されている役割を作成する例です。</span><span class="sxs-lookup"><span data-stu-id="13dc1-184">The following cmdlet is an example of a creating a role which has the privileges of one of the pre-defined administrative roles, but with limited scope.</span></span> <span data-ttu-id="13dc1-185">という新しい役割が作成され `Site01 Server Administrators` ます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-185">It creates a new role called `Site01 Server Administrators`.</span></span> <span data-ttu-id="13dc1-186">この役割には、定義済みの CsServerAdministrator ロールの権限がありますが、Site01 サイトにあるサーバーに対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-186">The role has the abilities of the predefined CsServerAdministrator role, but only for the servers located in the Site01 site.</span></span> <span data-ttu-id="13dc1-187">このコマンドレットが動作するためには、Site01 サイトが既に定義されており、という名前のユニバーサルセキュリティグループが既に存在している必要があり `Site01 Server Administrators` ます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-187">For this cmdlet to work, the Site01 site must already be defined, and a universal security group named `Site01 Server Administrators` must already exist.</span></span>

    New-CsAdminRole -Identity "Site01 Server Administrators" -Template CsServerAdministrator -ConfigScopes "site:Site01"

<span data-ttu-id="13dc1-188">このコマンドレットを実行すると、グループのメンバーになっているすべてのユーザーに、 `Site01 Server Administrators` Site01 のサーバーのサーバー管理者権限が与えられます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-188">After this cmdlet runs, all users who are members of the `Site01 Server Administrators` group will have server administrator privileges for the servers in Site01.</span></span> <span data-ttu-id="13dc1-189">さらに、このユニバーサルセキュリティグループに後で追加されたすべてのユーザーも、この役割の権限を取得します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-189">Additionally, any users who are later added to this universal security group also gain the privileges of this role.</span></span> <span data-ttu-id="13dc1-190">役割自体と、それに割り当てられているユニバーサルセキュリティグループの両方が呼び出され `Site01 Server Administrators` ます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-190">Note that both the role itself, and the universal security group it is assigned to are called `Site01 Server Administrators`.</span></span>

<span data-ttu-id="13dc1-191">次の例では、サーバースコープの代わりにユーザーのスコープを制限しています。</span><span class="sxs-lookup"><span data-stu-id="13dc1-191">The following example limits user scope instead of server scope.</span></span> <span data-ttu-id="13dc1-192">`Sales Users Administrator`営業組織単位のユーザーアカウントを管理するための役割を作成します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-192">It creates a `Sales Users Administrator` role to administer the user accounts in the Sales organizational unit.</span></span> <span data-ttu-id="13dc1-193">このコマンドレットが機能するためには、Salesて管理者のユニバーサルセキュリティグループが既に作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-193">The SalesUsersAdministrator universal security group must already be created for this cmdlet to work.</span></span>

    New-CsAdminRole -Identity "Sales Users Administrator " -Template CsUserAdministrator -UserScopes "OU:OU=Sales, OU=Lync Tenants, DC=Domain, DC=com"

</div>

<div>

## <a name="creating-a-new-role"></a><span data-ttu-id="13dc1-194">新しい役割の作成</span><span class="sxs-lookup"><span data-stu-id="13dc1-194">Creating a New Role</span></span>

<span data-ttu-id="13dc1-195">定義済みのロールのいずれにも含まれていない一連のコマンドレット、または一連のスクリプトまたはモジュールにアクセスできる役割を作成するには、あらかじめ定義されたいずれかのロールをテンプレートとして使用します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-195">To create a role that has access to a set of cmdlets not in one of the predefined roles, or to a set of scripts or modules, you again start by using one of the predefined roles as a template.</span></span> <span data-ttu-id="13dc1-196">ロールを実行できるスクリプトとモジュールは、次の場所に格納されている必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="13dc1-196">Note that scripts and modules that roles are to be able to run must be stored in the following locations:</span></span>

  - <span data-ttu-id="13dc1-197">Lync モジュールのパス (既定では C: \\ Program files の \\ 共通ファイル \\ Microsoft lync Server 2013 \\ モジュール \\ Lync)</span><span class="sxs-lookup"><span data-stu-id="13dc1-197">The Lync module path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Modules\\Lync</span></span>

  - <span data-ttu-id="13dc1-198">ユーザースクリプトパス (既定では C: \\ Program Files \\ Common Files \\ Microsoft Lync Server 2013 \\ adminscripts)</span><span class="sxs-lookup"><span data-stu-id="13dc1-198">The user script path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\AdminScripts</span></span>

<span data-ttu-id="13dc1-199">新しい役割を作成するには、 **新しい-CsAdminRole** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-199">To make a new role, you use the **New-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="13dc1-200">**新しい CsAdminRole** を実行する前に、この役割に関連付けられる、基になるユニバーサルセキュリティグループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-200">Before running **New-CsAdminRole**, you must first create the underlying universal security group that will be associated with this role.</span></span>

<span data-ttu-id="13dc1-201">次のコマンドレットは、新しい役割の作成例として機能します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-201">The following cmdlets serve as an example of a creating a new role.</span></span> <span data-ttu-id="13dc1-202">これにより、という新しい役割の種類が作成され `MyHelpDeskScriptRole` ます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-202">They create a new role type called `MyHelpDeskScriptRole`.</span></span> <span data-ttu-id="13dc1-203">新しい役割には、定義済みの CsHelpDesk ロールの機能があり、"testscript" という名前のスクリプトでさらに関数を実行できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-203">The new role has the abilities of the predefined CsHelpDesk role, and can additionally run the functions in a script named “testscript”.</span></span>

    New-CsAdminRole -Identity "MyHelpDeskScriptRole" -Template CsHelpDesk -ScriptModules @{Add="testScript.ps1"}

<span data-ttu-id="13dc1-204">このコマンドレットが動作するためには、まずユニバーサルセキュリティグループ Myhelpデスク Scriptrole を作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-204">For this cmdlet to work, you must have first created the universal security group MyHelpDeskScriptRole.</span></span>

<span data-ttu-id="13dc1-205">このコマンドレットを実行した後、このロールにユーザーを直接割り当てる (その場合はグローバルスコープを持つ) か、このドキュメントの「スコープロールの作成」で説明したように、このロールに基づいてスコープ指定された役割を作成できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-205">After this cmdlet runs, you can assign users directly to this role (in which case they have global scope), or create a scoped role based on this role, as explained in Creating a Scoped Role, previously in this document.</span></span>

</div>

<div>

## <a name="assigning-roles-to-users"></a><span data-ttu-id="13dc1-206">ロールをユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="13dc1-206">Assigning Roles to Users</span></span>

<span data-ttu-id="13dc1-207">各 Lync Server の役割は、基になる Active Directory ユニバーサルセキュリティグループに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="13dc1-207">Each Lync Server role is associated with an underlying Active Directory universal security group.</span></span> <span data-ttu-id="13dc1-208">基になるグループに追加したユーザーは、その役割の能力を獲得できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-208">Any users who you add to the underlying group gain the abilities of that role.</span></span>

<span data-ttu-id="13dc1-209">前のセクションの例では、新しい役割を作成し、既存のユニバーサルセキュリティグループを新しい役割に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="13dc1-209">The examples in the preceding sections both created a new role and assigned an existing universal security group to the new role.</span></span> <span data-ttu-id="13dc1-210">既存の役割を1人または複数のユーザーに割り当てるには、その役割に関連付けられたグループにそれらのユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-210">To assign an existing role to one or more users, add those users to the group associated with the role.</span></span> <span data-ttu-id="13dc1-211">これらのグループには、個々のユーザーとユニバーサルセキュリティグループの両方を追加できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-211">You can add both individual users and universal security groups to these groups.</span></span>

<span data-ttu-id="13dc1-212">たとえば、 **Csadministrator** の役割は、Active Directory の **CS 管理者** のユニバーサルセキュリティグループに自動的に付与されます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-212">For example, the **CsAdministrator** role is automatically granted to the **CS Administrators** universal security group in Active Directory.</span></span> <span data-ttu-id="13dc1-213">このユニバーサルセキュリティグループは、Lync Server を展開するときに Active Directory で作成されます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-213">This universal security group is created in Active Directory when you deploy Lync Server.</span></span> <span data-ttu-id="13dc1-214">ユーザーまたはグループにこの権限を付与するには、 **CS 管理者** グループに追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="13dc1-214">To grant a user or group this privilege, you can simply add them to the **CS Administrators** group.</span></span>

<span data-ttu-id="13dc1-215">ユーザーには、各役割に対応する、基になる Active Directory グループに追加することで、複数の RBAC ロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-215">A user can be given multiple RBAC roles by being added to the underlying Active Directory groups that correspond to each role.</span></span>

<span data-ttu-id="13dc1-216">ロールを作成すると、基になる Active Directory グループに後で追加されたユーザーにその役割の機能が与えられることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="13dc1-216">Note that when you create a role, users who are later added to the underlying Active Directory group gain the abilities of that role.</span></span>

</div>

<div>

## <a name="modifying-the-abilities-of-a-role"></a><span data-ttu-id="13dc1-217">役割の権限を変更する</span><span class="sxs-lookup"><span data-stu-id="13dc1-217">Modifying the Abilities of a Role</span></span>

<span data-ttu-id="13dc1-218">役割が実行できるコマンドレットとスクリプトの一覧は変更できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-218">You can modify the list of cmdlets and scripts that a role can run.</span></span> <span data-ttu-id="13dc1-219">カスタムロールで実行できるコマンドレットとスクリプトの両方を変更することはできますが、定義済みのロールのスクリプトのみを変更できます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-219">You can modify both the cmdlets and scripts that custom roles can run, but you can modify only the scripts for predefined roles.</span></span> <span data-ttu-id="13dc1-220">入力する各コマンドレットでは、コマンドレットまたはスクリプトの追加、削除、置換を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-220">Each cmdlet you type can add, remove, or replace cmdlets or scripts.</span></span>

<span data-ttu-id="13dc1-221">役割を変更するには、 **Set-CsAdminRole** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-221">To modify a role, use the **Set-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="13dc1-222">次のコマンドレットは、役割から1つのスクリプトを削除します。</span><span class="sxs-lookup"><span data-stu-id="13dc1-222">The following cmdlet removes one script from the role.</span></span>

    Set-CsAdminRole -Identity "MyHelpDeskScriptRole" -ScriptModules @{Remove="testScript.ps1"}

</div>

</div>

<div>

## <a name="planning-for-rbac"></a><span data-ttu-id="13dc1-223">RBAC の計画</span><span class="sxs-lookup"><span data-stu-id="13dc1-223">Planning for RBAC</span></span>

<span data-ttu-id="13dc1-224">Lync Server の展開にどのような管理権限を付与するかについては、どのようなタスクを実行する必要があるかを正確に考慮し、その職務に必要な最低限の権限と範囲の役割を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="13dc1-224">For each person who is to be given any kind of administrative rights for your Lync Server deployment, consider exactly which tasks they need to perform, then assign them to roles with the least privilege and scope necessary for their job.</span></span> <span data-ttu-id="13dc1-225">必要に応じて、[ **Set-CsAdminRole** ] コマンドレットを使用して、このユーザーのタスクに必要なコマンドレットのみを含む新しい役割を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-225">If necessary, you can use the **Set-CsAdminRole** cmdlet to create a new role with only the cmdlets necessary for this person’s tasks.</span></span>

<span data-ttu-id="13dc1-226">CsAdministrator ロールを持っているユーザーは、CsAdministrator に基づくロールを含むすべての種類の役割を作成し、ユーザーを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="13dc1-226">Users who have the CsAdministrator role can create all types of roles, including roles based on CsAdministrator, and assign users to them.</span></span> <span data-ttu-id="13dc1-227">ベストプラクティスとして、CsAdministrator の役割を、非常に少数の信頼できるユーザーに割り当てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="13dc1-227">The best practice is to assign the CsAdministrator role to a very small set of trusted users.</span></span>

<span data-ttu-id="13dc1-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13dc1-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

