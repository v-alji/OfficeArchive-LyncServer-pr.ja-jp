---
title: 'Lync Server 2013: セットアップ アクセス許可の付与'
description: 'Lync Server 2013: セットアップのアクセス許可を付与します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427901"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="815cf-103">Lync Server 2013 でのセットアップ アクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="815cf-103">Granting setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="815cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="815cf-104">

<span> </span></span></span>

<span data-ttu-id="815cf-105">_**最終更新日:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="815cf-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="815cf-106">WriteSPN アクセス許可コマンドレットを使用 **して、** 指定した Active Directory 組織単位 (OU) の RTCUniversalServerAdmins グループに読み取り、書き込み、readspn、およびのアクセス許可を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="815cf-106">You can use the **Grant-CsSetupPermission** cmdlet to add Read, Write, ReadSPN, and WriteSPN permissions to the RTCUniversalServerAdmins group for a specified Active Directory organizational unit (OU).</span></span> <span data-ttu-id="815cf-107">その後、その OU の RTCUniversalServerAdmins グループのメンバーは、ドメイン管理者グループのメンバーにならずに、指定したドメインで Lync Server 2013 を実行しているサーバーをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="815cf-107">Then members of the RTCUniversalServerAdmins group in that OU can install servers running Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="815cf-108">**Cssetuppermission** コマンドレットを使用して、設定したアクセス許可を確認します。これには、**グラント setuppermission** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="815cf-108">Use the **Test-CsSetupPermission** cmdlet to verify the permissions you set up by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<span data-ttu-id="815cf-109">無効にした場合は、 **Revoke setuppermissions** コマンドレットを使用して、 **付与** したアクセス許可を削除できます。</span><span class="sxs-lookup"><span data-stu-id="815cf-109">You can use the **Revoke-CsSetupPermission** cmdlet to remove permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-setup-permissions"></a><span data-ttu-id="815cf-110">セットアップのアクセス許可を付与するには</span><span class="sxs-lookup"><span data-stu-id="815cf-110">To grant setup permissions</span></span>

1.  <span data-ttu-id="815cf-111">セットアップのアクセス許可を付与するドメインの、Lync Server 2013 を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="815cf-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant setup permissions.</span></span> <span data-ttu-id="815cf-112">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="815cf-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="815cf-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="815cf-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="815cf-114">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="815cf-114">Run:</span></span>
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="815cf-115">指定したドメインの既定の名前付けコンテキスト (たとえば、CN = computers) を基準として、ComputerOu パラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="815cf-115">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="815cf-116">または、このパラメーターを完全な OU 識別名 (DN) として指定することもできます (たとえば、"CN = computers, DC = Contoso, DC = com")。</span><span class="sxs-lookup"><span data-stu-id="815cf-116">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="815cf-117">後者の場合、指定したドメインと一貫性のある OU DN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="815cf-117">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="815cf-118">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="815cf-118">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-setup-permissions"></a><span data-ttu-id="815cf-119">セットアップのアクセス許可を確認するには</span><span class="sxs-lookup"><span data-stu-id="815cf-119">To verify setup permissions</span></span>

1.  <span data-ttu-id="815cf-120">アクセス許可を **付与** したドメイン内の Lync Server 2013 を実行しているコンピューターにログオンします。このコマンドレットを使用して、付与したセットアップのアクセス許可を確認します。</span><span class="sxs-lookup"><span data-stu-id="815cf-120">Log on to a computer running Lync Server 2013 in the domain where you want to verify setup permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="815cf-121">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="815cf-121">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="815cf-122">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="815cf-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="815cf-123">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="815cf-123">Run:</span></span>
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="815cf-124">指定したドメインの既定の名前付けコンテキスト (たとえば、CN = computers) を基準として、ComputerOu パラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="815cf-124">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="815cf-125">または、このパラメーターを完全な OU 識別名 (DN) として指定することもできます (たとえば、"CN = computers, DC = Contoso, DC = com")。</span><span class="sxs-lookup"><span data-stu-id="815cf-125">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="815cf-126">後者の場合、指定したドメインと一貫性のある OU DN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="815cf-126">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="815cf-127">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="815cf-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-setup-permissions"></a><span data-ttu-id="815cf-128">セットアップのアクセス許可を取り消すには</span><span class="sxs-lookup"><span data-stu-id="815cf-128">To revoke setup permissions</span></span>

1.  <span data-ttu-id="815cf-129">**グラント Setuppermission** コマンドレットによって付与されたセットアップのアクセス許可を取り消すドメインで、Lync Server 2013 を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="815cf-129">Log on to a computer running Lync Server 2013 in the domain where you want to revoke setup permissions that were granted by the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="815cf-130">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="815cf-130">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="815cf-131">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="815cf-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="815cf-132">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="815cf-132">Run:</span></span>
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="815cf-133">指定したドメインの既定の名前付けコンテキスト (たとえば、CN = computers) を基準として、ComputerOu パラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="815cf-133">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="815cf-134">または、このパラメーターを完全な OU 識別名 (DN) として指定することもできます (たとえば、"CN = computers, DC = Contoso, DC = com")。</span><span class="sxs-lookup"><span data-stu-id="815cf-134">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="815cf-135">後者の場合、指定したドメインと一貫性のある OU DN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="815cf-135">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="815cf-136">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="815cf-136">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="815cf-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="815cf-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

