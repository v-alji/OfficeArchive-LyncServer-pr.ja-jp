---
title: 'Lync Server 2013: Lync Server で有効になっているユーザーアカウント'
description: 'Lync Server 2013: Lync Server で有効になっているユーザーアカウント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User accounts enabled for Lync Server 2013
ms:assetid: 8021087e-5084-4a39-9fef-ab9376c6d371
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182543(v=OCS.15)
ms:contentKeyID: 48184651
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf87177c378ffe61715d5332d2fd23b1d8e6fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399434"
---
# <a name="user-accounts-enabled-for-lync-server-2013"></a><span data-ttu-id="d1fff-103">Lync Server 2013 で有効になっているユーザーアカウント</span><span class="sxs-lookup"><span data-stu-id="d1fff-103">User accounts enabled for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1fff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1fff-104">

<span> </span></span></span>

<span data-ttu-id="d1fff-105">_**最終更新日:** 2014-04-18_</span><span class="sxs-lookup"><span data-stu-id="d1fff-105">_**Topic Last Modified:** 2014-04-18_</span></span>

<span data-ttu-id="d1fff-106">このセクションのトピックでは、Lync Server 2013 コントロールパネルを使用して実行できるユーザー設定を構成するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1fff-106">Topics in this section provide step-by-step procedures for configuring user settings that you can perform using the Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d1fff-107">Lync Server コントロールパネルを使用して、Active Directory Domain Admins グループのメンバーであるユーザーを管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="d1fff-107">You cannot use Lync Server Control Panel to manage users who are members of the Active Directory Domain Admins group.</span></span> <span data-ttu-id="d1fff-108">ドメイン管理者のユーザーの場合は、Lync Server コントロールパネルのみを使って読み取り専用の検索操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="d1fff-108">For Domain Admins users, you can use Lync Server Control Panel only to perform read-only search operations.</span></span> <span data-ttu-id="d1fff-109">ドメイン管理者のユーザーに対して書き込み操作を実行するには (たとえば、Lync Server コントロールパネルの有効化または無効化、プールまたはポリシーの割り当ての変更、テレフォニーの設定、SIP アドレス)、ドメイン管理者ユーザーとしてログオンしている場合は、Windows PowerShell コマンドレットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fff-109">To perform write operations on Domain Admins users (for example, enable or disable for Lync Server Control Panel, change pool or policy assignments, telephony settings, SIP address), you must use Windows PowerShell cmdlets while logged on as a Domain Admins user.</span></span> <span data-ttu-id="d1fff-110">Windows PowerShell コマンドレットを使用してユーザーを管理する方法の詳細については、「 <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 管理シェル</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1fff-110">For details about using Windows PowerShell cmdlets to manage users, see <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A>.</span></span>



</div>

<span data-ttu-id="d1fff-111">ユーザーを検索したり、ユーザーの検索結果をフィルター処理したりする Lync Server 2013 の管理タスクを実行すると、一部のユーザープロパティが Active Directory ドメインサービスの属性として存在しますが、Microsoft Exchange Server が展開されるまでグローバルカタログには複製されません。</span><span class="sxs-lookup"><span data-stu-id="d1fff-111">When you perform any Lync Server 2013 administrative task that involves searching for a user or filtering user search results, there are some user properties that exist as attributes in Active Directory Domain Services but are not replicated to the global catalog until Microsoft Exchange Server is deployed.</span></span> <span data-ttu-id="d1fff-112">Microsoft Exchange は、Lync Server ではなく、インストール時にグローバルカタログへの次の属性をマークします。</span><span class="sxs-lookup"><span data-stu-id="d1fff-112">Microsoft Exchange, not Lync Server, marks the following attributes for replication to the global catalog when it is installed:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1fff-113">ユーザー情報</span><span class="sxs-lookup"><span data-stu-id="d1fff-113">User Information</span></span></th>
<th><span data-ttu-id="d1fff-114">住所と電話番号</span><span class="sxs-lookup"><span data-stu-id="d1fff-114">Address and Phone</span></span></th>
<th><span data-ttu-id="d1fff-115">組織</span><span class="sxs-lookup"><span data-stu-id="d1fff-115">Organization</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1fff-116">ネーム</span><span class="sxs-lookup"><span data-stu-id="d1fff-116">Initials</span></span></p></td>
<td><p><span data-ttu-id="d1fff-117">住所</span><span class="sxs-lookup"><span data-stu-id="d1fff-117">Street address</span></span></p>
<p><span data-ttu-id="d1fff-118">国または地域</span><span class="sxs-lookup"><span data-stu-id="d1fff-118">Country/region</span></span></p>
<p><span data-ttu-id="d1fff-119">ページャー</span><span class="sxs-lookup"><span data-stu-id="d1fff-119">Pager</span></span></p>
<p><span data-ttu-id="d1fff-120">/Fax</span><span class="sxs-lookup"><span data-stu-id="d1fff-120">Fax</span></span></p>
<p><span data-ttu-id="d1fff-121">モバイル</span><span class="sxs-lookup"><span data-stu-id="d1fff-121">Mobile</span></span></p></td>
<td><p><span data-ttu-id="d1fff-122">タイトル</span><span class="sxs-lookup"><span data-stu-id="d1fff-122">Title</span></span></p>
<p><span data-ttu-id="d1fff-123">貴社</span><span class="sxs-lookup"><span data-stu-id="d1fff-123">Company</span></span></p>
<p><span data-ttu-id="d1fff-124">各部</span><span class="sxs-lookup"><span data-stu-id="d1fff-124">Department</span></span></p>
<p><span data-ttu-id="d1fff-125">Office</span><span class="sxs-lookup"><span data-stu-id="d1fff-125">Office</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="d1fff-126">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d1fff-126">In This Section</span></span>

  - [<span data-ttu-id="d1fff-127">Lync Server 2013 で有効になっているユーザーアカウントに関する情報の表示</span><span class="sxs-lookup"><span data-stu-id="d1fff-127">Viewing information about user accounts enabled for Lync Server 2013</span></span>](lync-server-2013-viewing-information-about-user-accounts-enabled-for-lync-server.md)

  - [<span data-ttu-id="d1fff-128">Lync Server 2013 のユーザーを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="d1fff-128">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)

  - [<span data-ttu-id="d1fff-129">Lync Server 2013 でのユーザーのエンタープライズボイスの管理</span><span class="sxs-lookup"><span data-stu-id="d1fff-129">Managing Enterprise Voice for users in Lync Server 2013</span></span>](lync-server-2013-managing-enterprise-voice-for-users.md)

  - [<span data-ttu-id="d1fff-130">Lync Server 2013 でユーザーアカウントのプロパティを変更する</span><span class="sxs-lookup"><span data-stu-id="d1fff-130">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)

  - [<span data-ttu-id="d1fff-131">Lync Server 2013 での組織の外部アクセス ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="d1fff-131">Manage external access policy in Lync Server 2013</span></span>](lync-server-2013-manage-external-access-policy-for-your-organization.md)

  - [<span data-ttu-id="d1fff-132">Lync Server 2013 でのユーザーごとのポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="d1fff-132">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1fff-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1fff-133">See Also</span></span>


[<span data-ttu-id="d1fff-134">Lync Server 2013 のユーザー管理コマンドレット</span><span class="sxs-lookup"><span data-stu-id="d1fff-134">User management cmdlets in Lync Server 2013</span></span>](lync-server-2013-user-management-cmdlets.md)  


[<span data-ttu-id="d1fff-135">Lync Server 2013 のユーザー管理</span><span class="sxs-lookup"><span data-stu-id="d1fff-135">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="d1fff-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1fff-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

