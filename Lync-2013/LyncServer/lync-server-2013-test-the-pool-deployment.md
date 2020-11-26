---
title: 'Lync Server 2013: プール展開のテスト'
description: 'Lync Server 2013: プールの展開をテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the pool deployment
ms:assetid: ffd80617-155a-4041-bbeb-74503e7938dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413092(v=OCS.15)
ms:contentKeyID: 48185976
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28101a252eda5048ded9f1eaf76c092c5cb7f986
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444232"
---
# <a name="test-the-pool-deployment-in-lync-server-2013"></a><span data-ttu-id="577ca-103">Lync Server 2013 でのプール展開のテスト</span><span class="sxs-lookup"><span data-stu-id="577ca-103">Test the pool deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="577ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="577ca-104">

<span> </span></span></span>

<span data-ttu-id="577ca-105">_**最終更新日:** 2013-09-25_</span><span class="sxs-lookup"><span data-stu-id="577ca-105">_**Topic Last Modified:** 2013-09-25_</span></span>

<span data-ttu-id="577ca-106">次の手順では、フロントエンドプールの展開をテストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="577ca-106">The following procedure describes how to test the deployment of the Front End pool.</span></span>

<div>

## <a name="to-test-the-pool-deployment"></a><span data-ttu-id="577ca-107">プールの展開をテストするには</span><span class="sxs-lookup"><span data-stu-id="577ca-107">To test the pool deployment</span></span>

1.  <span data-ttu-id="577ca-108">Active Directory コンピューターとユーザーを使用して、Lync Server 2013 の展開 (Lync Server 2013 コントロールパネルがインストールされている場合) の管理者ロールの Active Directory ユーザーオブジェクトを **csadministrator** グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="577ca-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server 2013 Control Panel is installed) to the **CSAdministrator** group.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="577ca-109">適切なユーザーとグループを CsAdministors グループに追加していない場合は、Lync Server コントロールパネルを開くとエラーが発生します。これは、"権限がありません。ロールベースのアクセス制御 (RBAC) 承認エラーによりアクセスが拒否されました。" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="577ca-109">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

2.  <span data-ttu-id="577ca-110">ユーザーオブジェクトが現在ログオンしている場合は、ログオフしてから再びログオンして、新しいグループの割り当てを登録します。</span><span class="sxs-lookup"><span data-stu-id="577ca-110">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="577ca-111">ユーザーアカウントを、Lync Server 2013 を実行しているサーバーのローカル管理者にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="577ca-111">The user account cannot be the local administrator of any server running Lync Server 2013.</span></span>

    
    </div>

3.  <span data-ttu-id="577ca-112">管理者アカウントを使用して、Lync Server コントロールパネルがインストールされているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="577ca-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="577ca-113">Lync Server コントロールパネルを起動し、メッセージが表示されたら、資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="577ca-113">Start Lync Server Control Panel, and then provide credentials, if prompted.</span></span> <span data-ttu-id="577ca-114">Lync Server コントロールパネルに展開情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="577ca-114">Lync Server Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="577ca-115">左側のナビゲーションバーで、[ **トポロジ**] をクリックし、[サービスの状態] に緑色の矢印が表示されていることを確認し、[レプリケーションの状態] に緑色のチェックマークが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="577ca-115">In the left navigation bar, click **Topology**, and then confirm that the service status shows a computer with a green arrow and that a green check mark for replication status is next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="577ca-116">左側のナビゲーションバーで [ **ユーザー**] をクリックし、[ **ユーザーの有効化**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="577ca-116">In the left navigation bar, click **Users**, and then click **Enable users**.</span></span>

7.  <span data-ttu-id="577ca-117">[ **新しい Lync Server ユーザー** ] ページで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="577ca-117">On the **New Lync Server User** page, click **Add**.</span></span>

8.  <span data-ttu-id="577ca-118">検索するオブジェクトの検索パラメーターを定義するには、[ **Active Directory から選択** ] ページで [ **検索**] を選択し、必要に応じて [ **フィルターの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="577ca-118">To define search parameters for the objects you want to find, on the **Select from Active Directory** page, you can select **Search**, and then optionally click **Add Filter**.</span></span> <span data-ttu-id="577ca-119">**Ldap 検索** を選択し、返されるオブジェクトをフィルター処理または制限するための ldap 式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="577ca-119">You can also select **LDAP search** and enter an LDAP expression to filter or limit the objects that will be returned.</span></span> <span data-ttu-id="577ca-120">検索オプションを決定したら、clink **検索**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="577ca-120">After you have decided on your Search options, clink **Find**.</span></span>

9.  <span data-ttu-id="577ca-121">[検索結果] ウィンドウで、この検索セッションのオブジェクトをすべて選択し、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="577ca-121">In the Search results pane, select all the objects for this search session, and then click **OK**.</span></span>

10. <span data-ttu-id="577ca-122">[ **新しい Lync Server ユーザー** ] ページで、選択したオブジェクトが **ユーザー** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="577ca-122">On the **New Lync Server User** page, the object or objects you selected are in the **Users** display.</span></span> <span data-ttu-id="577ca-123">[ **プールへのユーザーの割り当て** ] ボックスの一覧で、オブジェクトのホームにするサーバーを選びます。</span><span class="sxs-lookup"><span data-stu-id="577ca-123">In the **Assign users to a pool** list, select the server where the objects should be homed.</span></span>
    
    <span data-ttu-id="577ca-124">次に、オブジェクトを構成するためのいくつかのオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="577ca-124">Following are a number of options for configuring the objects.</span></span>
    
      - <span data-ttu-id="577ca-125">**ユーザーの SIP URI を生成する**</span><span class="sxs-lookup"><span data-stu-id="577ca-125">**Generate user’s SIP URI**</span></span>
    
      - <span data-ttu-id="577ca-126">**テレフォニー**</span><span class="sxs-lookup"><span data-stu-id="577ca-126">**Telephony**</span></span>
    
      - <span data-ttu-id="577ca-127">**行の URI**</span><span class="sxs-lookup"><span data-stu-id="577ca-127">**Line URI**</span></span>
    
      - <span data-ttu-id="577ca-128">**会議ポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-128">**Conferencing policy**</span></span>
    
      - <span data-ttu-id="577ca-129">**クライアントのバージョンポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-129">**Client version policy**</span></span>
    
      - <span data-ttu-id="577ca-130">**PIN ポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-130">**PIN policy**</span></span>
    
      - <span data-ttu-id="577ca-131">**外部アクセスポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-131">**External access policy**</span></span>
    
      - <span data-ttu-id="577ca-132">**アーカイブポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-132">**Archiving policy**</span></span>
    
      - <span data-ttu-id="577ca-133">**場所のポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-133">**Location policy**</span></span>
    
      - <span data-ttu-id="577ca-134">**クライアントポリシー**</span><span class="sxs-lookup"><span data-stu-id="577ca-134">**Client policy**</span></span>
    
    <span data-ttu-id="577ca-135">基本的な機能をテストするために、[ **ユーザーの SIP URI の生成** に使用するオプションを選択してください (構成のその他のオプションでは既定の設定が使用されます)] を選び、[ **有効に** する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="577ca-135">For the purposes of testing the basic functionality, select the option you prefer for the **Generate user’s SIP URI** setting (the other options in the configuration will use default settings), and then click **Enable**.</span></span>

11. <span data-ttu-id="577ca-136">概要ページが表示され、[ **有効** ] 列にチェックマークが表示され、オブジェクトが使用できるようになったことを示します。</span><span class="sxs-lookup"><span data-stu-id="577ca-136">A summary page is displayed that shows a check mark in the **Enabled** column to indicate that the objects are now ready for use.</span></span> <span data-ttu-id="577ca-137">**SIP アドレス** 列には、ユーザーのサインイン構成に必要なアドレスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="577ca-137">The **SIP address** column displays the address you need for the user sign-in configuration.</span></span>

12. <span data-ttu-id="577ca-138">1人のユーザーをドメインに参加しているコンピューターにログオンし、別のユーザーをドメイン内の別のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="577ca-138">Log one user on to a computer that is joined to the domain, and another user on to another computer in the domain.</span></span>

13. <span data-ttu-id="577ca-139">2台の各クライアントコンピューターに Lync 2013 をインストールし、両方のユーザーが Lync Server 2013 にサインインして、互いにインスタントメッセージを送信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="577ca-139">Install Lync 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="577ca-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="577ca-140">See Also</span></span>


[<span data-ttu-id="577ca-141">Lync Server 2013 でのクライアントとデバイスの展開</span><span class="sxs-lookup"><span data-stu-id="577ca-141">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="577ca-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="577ca-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

