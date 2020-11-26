---
title: 'Lync Server 2013: 組織単位アクセス許可の付与'
description: 'Lync Server 2013: 組織単位のアクセス許可を付与します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427897"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a><span data-ttu-id="7f9fb-103">Lync Server 2013 での組織単位アクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="7f9fb-103">Granting organizational unit permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f9fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f9fb-104">

<span> </span></span></span>

<span data-ttu-id="7f9fb-105">_**最終更新日:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="7f9fb-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="7f9fb-106">**Grant-CsOuPermission** コマンドレットを使用して、指定した組織単位 (ou) 内のオブジェクトにアクセス許可を付与することができます。これにより、フォレストの準備によって作成された RTC ユニバーサルグループのメンバーは、domain Admins グループのメンバーにならずにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-106">You can use the **Grant-CsOuPermission** cmdlet to grant permissions to objects in specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access them without being members of the Domain Admins group.</span></span> <span data-ttu-id="7f9fb-107">指定した OU に追加されたアクセス許可は、 **ドメインの準備** 中に [コンピューターとユーザー] コンテナーに追加される [権限の付与] のアクセス許可と同じです。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-107">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users containers during domain preparation.</span></span>

<span data-ttu-id="7f9fb-108">ユーザー権限の **付与** コマンドレットを使用して、設定したアクセス許可を確認するには、 **csoupermission** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-108">Use the **Test-CsOuPermission** cmdlet to verify the permissions you set up by using the **Grant-CsOuPermission** cmdlet.</span></span>

<span data-ttu-id="7f9fb-109">**Revoke-csoupermission** コマンドレットを使用して、**グラント-csoupermission** コマンドレットを使用して付与したアクセス許可を削除できます。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-109">You can use the **Revoke-CsOuPermission** cmdlet to remove permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-ou-permissions"></a><span data-ttu-id="7f9fb-110">OU 権限を付与するには</span><span class="sxs-lookup"><span data-stu-id="7f9fb-110">To grant OU permissions</span></span>

1.  <span data-ttu-id="7f9fb-111">OU 権限を付与するドメインの、Lync Server 2013 を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant OU permissions.</span></span> <span data-ttu-id="7f9fb-112">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f9fb-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f9fb-114">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-114">Run:</span></span>
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f9fb-115">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-115">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-ou-permissions"></a><span data-ttu-id="7f9fb-116">OU 権限を確認するには</span><span class="sxs-lookup"><span data-stu-id="7f9fb-116">To verify OU permissions</span></span>

1.  <span data-ttu-id="7f9fb-117">**Grant-CsOuPermission** コマンドレットを使用して付与した OU 権限を確認するドメインの、Lync Server 2013 を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-117">Log on to a computer running Lync Server 2013 in the domain where you want to verify OU permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="7f9fb-118">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-118">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f9fb-119">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f9fb-120">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-120">Run:</span></span>
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f9fb-121">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-121">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-ou-permissions"></a><span data-ttu-id="7f9fb-122">OU 権限を取り消すには</span><span class="sxs-lookup"><span data-stu-id="7f9fb-122">To revoke OU permissions</span></span>

1.  <span data-ttu-id="7f9fb-123">**Grant-CsOuPermission** コマンドレットによって付与された OU 権限を取り消すドメインで、Lync Server 2013 を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-123">Log on to a computer running Lync Server 2013 in the domain where you want to revoke OU permissions that were granted by the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="7f9fb-124">OU が別の子ドメインにある場合は、Domain Admins グループまたは Enterprise Admins グループのメンバーであるアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-124">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f9fb-125">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f9fb-126">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-126">Run:</span></span>
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f9fb-127">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="7f9fb-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="7f9fb-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f9fb-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

