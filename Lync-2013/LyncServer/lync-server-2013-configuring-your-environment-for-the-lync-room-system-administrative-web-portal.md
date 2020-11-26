---
title: 'Lync Server 2013: Lync Room System 管理 Web ポータルの環境の構成'
description: 'Lync Server 2013: Lync Room System 管理 Web ポータルの環境を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring your environment for the Lync Room System Administrative Web Portal
ms:assetid: 1bf3cc55-cfa8-46ee-a8bc-6dab3bff76b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436325(v=OCS.15)
ms:contentKeyID: 56737623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c942e1db799a7336a3eafb5571e82584694ddbf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432306"
---
# <a name="configuring-your-lync-server-2013-environment-for-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="26f06-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="26f06-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26f06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26f06-104">

<span> </span></span></span>

<span data-ttu-id="26f06-105">_**最終更新日:** 2014-05-22_</span><span class="sxs-lookup"><span data-stu-id="26f06-105">_**Topic Last Modified:** 2014-05-22_</span></span>

<span data-ttu-id="26f06-106">Lync Room System (LRS) 管理 Web ポータルを使用するには、次の前提条件をインストールまたは構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26f06-106">To use the Lync Room System (LRS) Administrative Web Portal, you will need to install or configure the following prerequisites.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="26f06-107">サーバーが Kerberos 認証と NTLM 認証の両方で構成されていて、ドメインに参加していないコンピューターで LRS が実行されている場合、Kerberos 認証は失敗し、管理ポータルで LRS の状態は表示されません。</span><span class="sxs-lookup"><span data-stu-id="26f06-107">If the server is configured with both Kerberos and NTLM authentication, and LRS is running on a computer that is not joined to the domain, Kerberos authentication will fail and the user will not see the status of LRS in the administrative portal.</span></span> <span data-ttu-id="26f06-108">この問題を解決するには、NTLM 認証を使用してサーバーを構成するか、NTLM と DSK 認証の両方 (Kerberos を使用しない)、または LRS コンピューターをドメインに参加させます。</span><span class="sxs-lookup"><span data-stu-id="26f06-108">To resolve this issue, configure the server with NTLM authentication or both NTLM and TLS-DSK authentication (without Kerberos), or join the LRS computer to the domain.</span></span>



</div>

1.  <span data-ttu-id="26f06-109">Lync Server 2013 累積更新プログラムをインストールする: Lync Server トポロジの2013年7月。</span><span class="sxs-lookup"><span data-stu-id="26f06-109">Install Lync Server 2013 Cumulative Updates: July 2013 in the Lync Server topology.</span></span>
    
    <span data-ttu-id="26f06-110">更新プログラムを入手したり、アプリに含まれている内容を確認したりするには、「 [Lync Server 2013 の更新プログラム](https://go.microsoft.com/fwlink/p/?linkid=323959)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="26f06-110">To get the update or see what’s included with it, see [Updates for Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).</span></span>

2.  <span data-ttu-id="26f06-111">SIP 対応の Active Directory ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="26f06-111">Create a SIP-enabled Active Directory user.</span></span>
    
    <span data-ttu-id="26f06-112">LRS 管理 Web ポータルでは、これらの資格情報を使用して Lync Server から情報を照会します。</span><span class="sxs-lookup"><span data-stu-id="26f06-112">The LRS Administrative Web Portal uses these credentials to query information from Lync Server.</span></span> <span data-ttu-id="26f06-113">推奨されるユーザ名は LRSApp です。</span><span class="sxs-lookup"><span data-stu-id="26f06-113">The recommended username is LRSApp.</span></span>

3.  <span data-ttu-id="26f06-114">LRSSupportAdminGroup という名前の Active Directory セキュリティ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="26f06-114">Create an Active Directory security group with name LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="26f06-p103">[グループのスコープ] が [グローバル]、[グループの種類] が [セキュリティ] のグループを作成します。このグループに追加される SIP 対応ユーザーは、部屋の一覧を参照したり、ログの収集などの特定のコマンドを実行したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="26f06-p103">Create the group with Group Scope as Global and Group Type as Security. SIP enabled users who are added to this group will be authorized to see the list of rooms and execute certain commands, such as collecting logs.</span></span>

4.  <span data-ttu-id="26f06-117">LRSFullAccessAdminGroup という名前の Active Directory セキュリティ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="26f06-117">Create an Active Directory security group with name LRSFullAccessAdminGroup.</span></span>
    
    <span data-ttu-id="26f06-118">グループのスコープを持つグループを [グローバル] と [グループ] のセキュリティとして作成します。このグループに追加された SIP 対応ユーザーは、すべての管理ポータル機能を使用することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="26f06-118">Create the group with Group Scope as Global and Group Type as Security.SIP enabled users who are added to this group are authorized to use all admin portal functionality.</span></span>
    
     
    
    <span data-ttu-id="26f06-119">![セキュリティ グループの役割を持つ Admin グループの一覧](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "セキュリティ グループの役割を持つ Admin グループの一覧")</span><span class="sxs-lookup"><span data-stu-id="26f06-119">![List of Admin Groups with security group role](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "List of Admin Groups with security group role")</span></span>  
    
     

5.  <span data-ttu-id="26f06-120">LRSFullAccessAdminGroup を LRSSupportAdminGroup のメンバーとして追加します。</span><span class="sxs-lookup"><span data-stu-id="26f06-120">Add LRSFullAccessAdminGroup as a member of LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="26f06-121">![LRSSupportAdminGroup プロパティ メンバー ページ](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "LRSSupportAdminGroup プロパティ メンバー ページ")</span><span class="sxs-lookup"><span data-stu-id="26f06-121">![LRSSupportAdminGroup Properties Members page](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

6.  <span data-ttu-id="26f06-122">LRSSupport という名前の SIP 対応の Active Directory ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="26f06-122">Create a SIP enabled Active Directory user with name LRSSupport.</span></span> <span data-ttu-id="26f06-123">このユーザーを LRSSupportAdminGroup に追加します。</span><span class="sxs-lookup"><span data-stu-id="26f06-123">Add this user to LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="26f06-124">![LRSSupportAdminGroup プロパティ メンバー ページ](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "LRSSupportAdminGroup プロパティ メンバー ページ")</span><span class="sxs-lookup"><span data-stu-id="26f06-124">![LRSSupportAdminGroup Properties Members page](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

7.  <span data-ttu-id="26f06-125">Microsoft ダウンロードセンターで入手可能な Visual Studio 2010 SP1 および Visual Web Developer 2010 SP1 の ASP.NET MVC 4 をインストール [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967) します。</span><span class="sxs-lookup"><span data-stu-id="26f06-125">Install ASP.NET MVC 4 for Visual Studio 2010 SP1 and Visual Web Developer 2010 SP1, available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967).</span></span>

<span data-ttu-id="26f06-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26f06-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

