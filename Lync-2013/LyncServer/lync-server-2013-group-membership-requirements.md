---
title: 'Lync Server 2013: グループ メンバーシップの要件'
description: 'Lync Server 2013: グループメンバーシップの要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427839"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a><span data-ttu-id="85c60-103">Lync Server 2013 のグループ メンバーシップの要件</span><span class="sxs-lookup"><span data-stu-id="85c60-103">Group membership requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85c60-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85c60-104">

<span> </span></span></span>

<span data-ttu-id="85c60-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="85c60-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="85c60-106">次の表は、Lync Server 2013 を正常にインストール、管理、トラブルシューティングするために、ユーザーが所属する必要があるグループをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="85c60-106">The following table summarizes the group or groups that a person should belong to in order to successfully install, manage, and troubleshoot Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85c60-107">Lync Server 2013 実行可能ファイル</span><span class="sxs-lookup"><span data-stu-id="85c60-107">Lync Server 2013 Executable</span></span></th>
<th><span data-ttu-id="85c60-108">グループメンバーシップが必要です</span><span class="sxs-lookup"><span data-stu-id="85c60-108">Group Membership Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85c60-109"><strong>Setup.exe</strong> – Lync Server 2013 管理ツールのインストールを開始する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="85c60-109"><strong>Setup.exe</strong> – Executable that starts the installation of the Lync Server 2013 administrative tools.</span></span></p></td>
<td><p><span data-ttu-id="85c60-110">実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-110">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="85c60-111">Active Directory ドメインサービスの情報を読み取るためのドメインユーザーグループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-111">Member of Domain Users group to read information in Active Directory Domain Services.</span></span> <span data-ttu-id="85c60-112">ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="85c60-112">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="85c60-113">また、ドメイン管理者グループのメンバーシップを付与しないユーザーまたはグループに、セットアップのアクセス許可を委任することもできます。</span><span class="sxs-lookup"><span data-stu-id="85c60-113">You can also delegate setup permissions to users or groups to whom you do not want to grant membership in the Domain Admins group.</span></span> <span data-ttu-id="85c60-114">詳細については、展開ドキュメントの「 <A href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 でのセットアップ権限の付与</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85c60-114">For details, see <A href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</A> in the Deployment documentation.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c60-115"><strong>Deploy.exe</strong> – setup.exe によって呼び出される deploy.exe は、サーバーの役割のソフトウェアコンポーネントの展開を担当します。</span><span class="sxs-lookup"><span data-stu-id="85c60-115"><strong>Deploy.exe</strong> – Called by setup.exe, deploy.exe is responsible for the deployment of the software components for the server roles.</span></span></p></td>
<td><p><span data-ttu-id="85c60-116">実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-116">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="85c60-117">ドメインユーザーグループのメンバーで、AD DS の情報を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="85c60-117">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="85c60-118">ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="85c60-118">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span> <span data-ttu-id="85c60-119">中央管理ストアを読むには、RtcUniversalReadOnlyAdmins group のメンバーシップが必要です。</span><span class="sxs-lookup"><span data-stu-id="85c60-119">Membership in RtcUniversalReadOnlyAdmins group is necessary to read the Central Management store.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="85c60-120">Windows Vista オペレーティングシステムまたは Windows 7 オペレーティングシステムを実行している場合は、ユーザーアカウント制御 (UAC) によってインストールを続行するかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85c60-120">If you are running the Windows Vista operating system or Windows 7 operating system, you will be prompted by User Account Control (UAC) to proceed with installation.</span></span> <span data-ttu-id="85c60-121">標準ユーザーアカウントでログオンしている場合は、ソフトウェアをインストールする権限を持つアカウントの入力を求められたときに、資格情報を提供するために、ローカル管理者グループのメンバーであるユーザーが必要になります。</span><span class="sxs-lookup"><span data-stu-id="85c60-121">If you are logged on with a standard user account, you will need someone who is a member of the Local Administrators group to provide credentials when prompted for an account with permissions to install the software.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c60-122"><strong>Bootstrapper.exe</strong> – setup.exe によって呼び出される bootstrapper.exe は、サーバーの役割の展開と構成を担当します。</span><span class="sxs-lookup"><span data-stu-id="85c60-122"><strong>Bootstrapper.exe</strong> – Called by setup.exe, bootstrapper.exe is responsible for deployment and configuration of server roles.</span></span></p></td>
<td><p><span data-ttu-id="85c60-123">実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-123">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="85c60-124">Bootstrapper.exe を実行する RTCUniversalServerAdmins グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-124">Member of the RTCUniversalServerAdmins group to run Bootstrapper.exe.</span></span> <span data-ttu-id="85c60-125">ドメインユーザーグループのメンバーで、AD DS の情報を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="85c60-125">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="85c60-126">ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="85c60-126">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c60-127"><strong>TopologyBuilder</strong> – Lync Server 2013 トポロジの作成、表示、調整、検証を行うためのウィザードベースのユーザーインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="85c60-127"><strong>TopologyBuilder</strong> – Wizard-driven user interface to create, view, adjust, and validate Lync Server 2013 topologies.</span></span></p></td>
<td><p><span data-ttu-id="85c60-128">トポロジを表示するために、実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-128">Member of the Local Administrators group on the computer from which the executable is run to view the topology.</span></span> <span data-ttu-id="85c60-129">構成の設定を変更する RTCUniversalServerAdmins グループのメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-129">Member of the RTCUniversalServerAdmins group to change configuration settings.</span></span> <span data-ttu-id="85c60-130">トポロジを公開するには、RTCUniversalServerAdmins group と Domain Admins グループのメンバー、または RTCUniversalServerAdmins グループのメンバー (グループに委任の設定権限が付与されている場合のみ)。</span><span class="sxs-lookup"><span data-stu-id="85c60-130">Member of the RTCUniversalServerAdmins group and Domain Admins group, or member of the RTCUniversalServerAdmins group (only if the group has been granted delegate setup permissions), to publish the topology.</span></span> <span data-ttu-id="85c60-131">RTCUniversalServerAdmins グループのメンバーが、ドメイン管理者グループのメンバーにならずにトポロジを公開できるようにするための委任セットアップのアクセス許可の詳細については、「展開ドキュメントの「 <a href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 でのセットアップアクセス許可の付与</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85c60-131">For details about delegating setup permissions to allow members of the RTCUniversalServerAdmins group to publish the topology without being members of the Domain Admins group, see <a href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c60-132"><strong>AdminUIHost</strong> – Lync Server 2013 を管理するための Web ベースのグラフィカルユーザーインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="85c60-132"><strong>AdminUIHost</strong> – Web-based graphical user interface for managing Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="85c60-133">特定の管理タスクが割り当てられている、他の役割ベースのアクセス制御 (RBAC) 役割のメンバー。 CsAdministrator グループまたはメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-133">Member of CsAdministrator group or member of another role-based access control (RBAC) role to which the specific administrative task is assigned.</span></span> <span data-ttu-id="85c60-134">Lync Server 2013 コントロールパネルでは、Lync Server 2013 Management Shell コマンドレットを実行することで、構成の変更を実装します。</span><span class="sxs-lookup"><span data-stu-id="85c60-134">Lync Server 2013 Control Panel implements configuration changes by running Lync Server 2013 Management Shell cmdlets.</span></span> <span data-ttu-id="85c60-135">定義済みの役割と、コマンドレットのメンバーの実行を許可する方法については、計画ドキュメントの「 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 でのロールベースのアクセス制御の計画</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85c60-135">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c60-136">Lync server <strong>2013 モジュールを読み込み</strong>ました。 lync server 2013 の管理に固有のコマンドレットを使用して、コマンドライン管理ツールをPowerShell.exe します。</span><span class="sxs-lookup"><span data-stu-id="85c60-136"><strong>PowerShell.exe with the Lync Server 2013 module loaded</strong> – Command-line administrative tool with cmdlets specific to management of Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="85c60-137">特定のコマンドレットが割り当てられている CsAdministrator グループまたは別の RBAC 役割のメンバー。</span><span class="sxs-lookup"><span data-stu-id="85c60-137">Member of CsAdministrator group or member of another RBAC role to which the specific cmdlet has been assigned.</span></span> <span data-ttu-id="85c60-138">定義済みの役割と、コマンドレットのメンバーの実行を許可する方法については、計画ドキュメントの「 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 でのロールベースのアクセス制御の計画</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85c60-138">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="85c60-139">または、コマンドレットに応じて、次の1つまたは複数のグループのメンバーになります。</span><span class="sxs-lookup"><span data-stu-id="85c60-139">Or, member of one or more of the following groups, depending on the cmdlet:</span></span></p>
<ul>
<li><p><span data-ttu-id="85c60-140">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="85c60-140">RTCUniversalServerAdmins</span></span></p></li>
<li><p><span data-ttu-id="85c60-141">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="85c60-141">RTCUniversalUserAdmins</span></span></p></li>
<li><p><span data-ttu-id="85c60-142">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="85c60-142">RTCUniversalReadOnlyAdmins</span></span></p></li>
</ul></td>
</tr><span data-ttu-id="85c60-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85c60-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

