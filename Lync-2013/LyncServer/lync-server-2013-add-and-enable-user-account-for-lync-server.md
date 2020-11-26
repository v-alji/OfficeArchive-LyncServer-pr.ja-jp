---
title: 'Lync Server 2013: Lync Server のユーザーアカウントを追加して有効にする'
description: 'Lync Server 2013: Lync Server のユーザーアカウントを追加して有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439374"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="949a9-103">Lync Server 2013 のユーザーアカウントを追加して有効にする</span><span class="sxs-lookup"><span data-stu-id="949a9-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="949a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="949a9-104">

<span> </span></span></span>

<span data-ttu-id="949a9-105">_**最終更新日:** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="949a9-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="949a9-106">Active Directory ユーザーとコンピューターでユーザーアカウントを有効にした後、Lync Server コントロールパネルを使用して、Active Directory ユーザーを Lync Server に追加することで、新しい Lync Server 2013 ユーザーアカウントを作成して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="949a9-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="949a9-107">新しい Lync Server ユーザーを追加して有効にするには</span><span class="sxs-lookup"><span data-stu-id="949a9-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="949a9-108">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="949a9-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="949a9-109">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="949a9-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="949a9-110">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="949a9-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="949a9-111">左側のナビゲーション バーで [**ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="949a9-112">[ **ユーザーを有効にする] を** クリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="949a9-113">[ **新しい Lync Server ユーザー** ] ダイアログボックスで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="949a9-114">[ **ユーザーの検索** ] ボックスで、名前、表示名、姓、名、姓、セキュリティアカウントマネージャー (SAM) アカウント名、メールアドレス、ユーザープリンシパル名 (UPN)、または必要な Active Directory ユーザーアカウントの電話番号のすべてまたは最初の部分を入力し、[ **検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="949a9-115">表で、Lync Server に追加するアカウントを選び、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="949a9-116">プールにユーザーを割り当て、追加の詳細を指定して、ポリシーを目的のユーザーに割り当て、[ **有効に** する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="949a9-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="949a9-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="949a9-117">See Also</span></span>


[<span data-ttu-id="949a9-118">Lync Server 2013 のユーザーアカウントを無効にするか、再び有効にする</span><span class="sxs-lookup"><span data-stu-id="949a9-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="949a9-119">Lync Server 2013 からユーザーアカウントを削除する</span><span class="sxs-lookup"><span data-stu-id="949a9-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="949a9-120">Lync Server 2013 のユーザーを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="949a9-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="949a9-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="949a9-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

