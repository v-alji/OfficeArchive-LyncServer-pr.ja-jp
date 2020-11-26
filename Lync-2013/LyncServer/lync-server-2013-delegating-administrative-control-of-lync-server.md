---
title: 'Lync Server 2013: Lync Server の管理機能の委任'
description: 'Lync Server 2013: Lync Server の管理制御を委任します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegating administrative control of Lync Server 2013
ms:assetid: 0f378eff-8ef4-4c60-9fd2-67d7ee259ef8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520951(v=OCS.15)
ms:contentKeyID: 48183418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8d3710af2d194a5aa4ebdd7291be2ee58176507
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430764"
---
# <a name="delegating-administrative-control-of-lync-server-2013"></a><span data-ttu-id="09030-103">Lync Server 2013 の管理機能の委任</span><span class="sxs-lookup"><span data-stu-id="09030-103">Delegating administrative control of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09030-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09030-104">

<span> </span></span></span>

<span data-ttu-id="09030-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="09030-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="09030-106">Lync Server 2013 では、新しいロールベースのアクセス制御 (RBAC) 機能を使用して、管理タスクがユーザーに委任されます。</span><span class="sxs-lookup"><span data-stu-id="09030-106">In Lync Server 2013, administrative tasks are delegated to users by using the new role-based access control (RBAC) feature.</span></span> <span data-ttu-id="09030-107">Lync Server をインストールすると、複数の RBAC の役割が作成されます。</span><span class="sxs-lookup"><span data-stu-id="09030-107">When you install Lync Server, a number of RBAC roles are created for you.</span></span> <span data-ttu-id="09030-108">これらの役割は、Active Directory ドメイン サービスのユニバーサル セキュリティ グループに対応します。</span><span class="sxs-lookup"><span data-stu-id="09030-108">These roles correspond to universal security groups in Active Directory Domain Services.</span></span> <span data-ttu-id="09030-109">たとえば、RBAC の役割 CsHelpDesk は、Active Directory ドメインサービスの Users コンテナーに含まれる CsHelpDesk グループに対応しています。</span><span class="sxs-lookup"><span data-stu-id="09030-109">For example, the RBAC role CsHelpDesk corresponds to the CsHelpDesk group found in the Users container in Active Directory Domain Services.</span></span> <span data-ttu-id="09030-110">さらに、各 RBAC の役割は、Lync Server Windows PowerShell コマンドレットのセットと関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="09030-110">In addition, each RBAC role is associated with a set of Lync Server Windows PowerShell cmdlets.</span></span> <span data-ttu-id="09030-111">これらのコマンドレットは、特定の RBAC の役割が割り当てられたユーザーが実行できるタスクを表します。</span><span class="sxs-lookup"><span data-stu-id="09030-111">These cmdlets represent the tasks that can be carried out by users who have been assigned the given RBAC role.</span></span> <span data-ttu-id="09030-112">たとえば、CsHelpDesk の役割には Lock-CsClientPin と UnlockCsClientPin コマンドレットが割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="09030-112">For example, the CsHelpDesk role has been assigned the Lock-CsClientPin and UnlockCsClientPin cmdlets.</span></span> <span data-ttu-id="09030-113">つまり、CsHelpDesk の役割が割り当てられているユーザーは、ユーザーの PIN 番号のロックとロック解除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="09030-113">That means users who have been assigned the CsHelpDesk role can lock and unlock user PIN numbers.</span></span> <span data-ttu-id="09030-114">ただし、CsHelpDesk の役割には New-CsVoicePolicy コマンドレットが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="09030-114">However, the CsHelpDesk role has not been assigned the New-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="09030-115">つまり、CsHelpDesk role を割り当てられているユーザーは、新しいボイスポリシーを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="09030-115">That means that users who have been assigned the CsHelpDesk role cannot create new voice policies.</span></span>

<div>

## <a name="viewing-information-about-rbac-roles"></a><span data-ttu-id="09030-116">RBAC ロールに関する情報を表示する</span><span class="sxs-lookup"><span data-stu-id="09030-116">Viewing Information about RBAC Roles</span></span>

<span data-ttu-id="09030-117">次のコマンドを Lync Server 管理シェルから実行して、RBAC の役割に関する基本的な情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="09030-117">You can retrieve basic information about your RBAC roles by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRole

<span data-ttu-id="09030-118">RBAC の役割 (CsVoiceAdministrator など) の Id は、Active Directory ドメインサービスの Users コンテナーにあるセキュリティグループに直接マッピングされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="09030-118">Keep in mind that the Identity of the RBAC role (for example, CsVoiceAdministrator) has a direct mapping to a security group found in the Users container in Active Directory Domain Services.</span></span>

<span data-ttu-id="09030-119">ロールに割り当てられているコマンドレットの一覧を表示するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="09030-119">To view a list of the cmdlets that have been assigned to a role, use a command similar to this:</span></span>

    Get-CsAdminRole -Identity "CsHelpDesk" | Select-Object -ExpandProperty Cmdlets

</div>

<div>

## <a name="assigning-an-rbac-role-to-a-user"></a><span data-ttu-id="09030-120">RBAC の役割をユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="09030-120">Assigning an RBAC Role to a User</span></span>

<span data-ttu-id="09030-121">RBAC の役割をユーザーに割り当てるには、適切な Active Directory セキュリティグループにそのユーザーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09030-121">To assign an RBAC role to a user, you must add that user to the appropriate Active Directory security group.</span></span> <span data-ttu-id="09030-122">たとえば、CsLocationAdministrator の役割をユーザーに割り当てるには、そのユーザーを CsLocationAdministrator グループに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09030-122">For example, to assign the CsLocationAdministrator role to a user, you must add that user to the CsLocationAdministrator group.</span></span> <span data-ttu-id="09030-123">そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="09030-123">That can be done by carrying out the following procedure:</span></span>

<span data-ttu-id="09030-124">**セキュリティグループにユーザーを割り当てるには**</span><span class="sxs-lookup"><span data-stu-id="09030-124">**To assign a user to a security group**</span></span>

1.  <span data-ttu-id="09030-125">Active Directory グループのメンバーシップを変更する権限を持つアカウントを使用して、Active Directory ユーザーとコンピューターがインストールされているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="09030-125">Using an account that has permission to modify the membership of an Active Directory group, log on to a computer where Active Directory Users and Computers has been installed.</span></span>

2.  <span data-ttu-id="09030-126">[ **スタート**] をクリックし、[ **すべてのプログラム**] をクリックし、[ **管理ツール**] をクリックして、[ **Active Directory ユーザーとコンピューター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-126">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

3.  <span data-ttu-id="09030-127">Active Directory ユーザーとコンピューターで、ドメインの名前を展開し、[ **ユーザー** ] コンテナーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-127">In Active Directory Users and Computers, expand the name of your domain and click the **Users** container.</span></span>

4.  <span data-ttu-id="09030-128">セキュリティグループ **Cslocationadministrator 者** を右クリックし、[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-128">Right-click the security group **CsLocationAdministrator**, and then click **Properties**.</span></span>

5.  <span data-ttu-id="09030-129">[ **プロパティ** ] ダイアログボックスの [ **メンバー** ] タブで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-129">In the **Properties** dialog box, on the **Members** tab, click **Add**.</span></span>

6.  <span data-ttu-id="09030-130">**[ユーザー、コンピューター、連絡先、またはグループの選択**] ダイアログボックスで、 **[選択するオブジェクト名を入力** してください] ボックスに、グループに追加するユーザー名またはユーザー名 ( **Ken Myer** など) を入力し、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-130">In the **Select Users, Computers, Contacts, or Groups** dialog box, type the user name or display name of the user to be added to the group (for example, **Ken Myer**) in the **Enter the object names to select** box and then click **OK**.</span></span>

7.  <span data-ttu-id="09030-131">[ **プロパティ** ] ダイアログボックスで、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09030-131">In the **Properties** dialog box, click **OK**.</span></span>

<span data-ttu-id="09030-132">RBAC の役割が割り当てられていることを確認するには、ユーザーの "SamAccountName (Active Directory のログオン名)" というコマンドレットを渡して、 [Csadminadminroleassignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) コマンドレットを使います。</span><span class="sxs-lookup"><span data-stu-id="09030-132">To verify that the RBAC role has been assigned, use the [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) cmdlet, passing the cmdlet the SamAccountName (Active Directory logon name) of the user.</span></span> <span data-ttu-id="09030-133">たとえば、Lync Server 管理シェルで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="09030-133">For example, run this command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRoleAssignment  -Identity "kenmyer"

<span data-ttu-id="09030-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09030-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

