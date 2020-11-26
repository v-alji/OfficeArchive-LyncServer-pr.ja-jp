---
title: 'Lync Server 2013: 統合連絡先ストアでユーザーを有効にする'
description: 'Lync Server 2013: 統合連絡先ストアのユーザーを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for unified contact store
ms:assetid: 7b46a01f-beb5-4a33-adb0-35f0502b168d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205024(v=OCS.15)
ms:contentKeyID: 48184599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2249249d314e13d840b276e46f1fe38ad271664a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428819"
---
# <a name="enable-users-for-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="3063e-103">Lync Server 2013 の統合連絡先ストアでユーザーを有効にする</span><span class="sxs-lookup"><span data-stu-id="3063e-103">Enable users for unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3063e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3063e-104">

<span> </span></span></span>

<span data-ttu-id="3063e-105">_**最終更新日:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="3063e-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="3063e-106">Lync Server 2013 を展開してトポロジを公開すると、既定では、統合連絡先ストアがすべてのユーザーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="3063e-106">When you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="3063e-107">Lync Server 2013 を展開した後、ユニファイド連絡先ストアを有効にするために、追加の操作を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3063e-107">You do not need to take any additional action to enable unified contact store after you deploy Lync Server 2013.</span></span> <span data-ttu-id="3063e-108">ただし、**Set-CsUserServicesPolicy** コマンドレットを使用すると、どのユーザーが統合連絡先ストアを使用できるのかをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="3063e-108">However, you can use the **Set-CsUserServicesPolicy** cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="3063e-109">この機能の有効化は、グローバルに行うことも、サイトごと、テナントごと、または個人やそのグループごとに行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="3063e-109">You can enable this feature globally, by site, by tenant, or by individuals or groups of individuals.</span></span>

<div>

## <a name="to-enable-users-for-unified-contact-store"></a><span data-ttu-id="3063e-110">統合連絡先ストアでユーザーを有効にするには</span><span class="sxs-lookup"><span data-stu-id="3063e-110">To enable users for unified contact store</span></span>

1.  <span data-ttu-id="3063e-111">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3063e-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3063e-112">次のいずれかの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="3063e-112">Do any of the following:</span></span>
    
      - <span data-ttu-id="3063e-113">すべての Lync Server ユーザーに対して、統合された連絡先ストアをグローバルに有効にするには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-113">To enable unified contact store globally for all Lync Server users, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Identity global -UcsAllowed $True
    
      - <span data-ttu-id="3063e-114">特定のサイトのユーザーに対してユニファイド連絡先ストアを有効にするには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-114">To enable unified contact store for the users at a specific site, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity site:<site name> -UcsAllowed $True
        
        <span data-ttu-id="3063e-115">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3063e-115">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity site:Redmond -UcsAllowed $True
    
      - <span data-ttu-id="3063e-116">テナントを使用してユニファイド連絡先ストアを有効にするには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-116">To enable unified contact store by tenant, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Tenant <tenantId> -UcsAllowed $True
        
        <span data-ttu-id="3063e-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3063e-117">For example:</span></span>
        
            Set-CsUserServicesPolicy -Tenant "38aad667-af54-4397-aaa7-e94c79ec2308" -UcsAllowed $True
    
      - <span data-ttu-id="3063e-118">特定のユーザーに対してユニファイド連絡先ストアを有効にするには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-118">To enable unified contact store for specific users, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "<user display name>" -PolicyName <"policy name">
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3063e-119">ユーザーの表示名の代わりに、ユーザー エイリアスや SIP URI を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="3063e-119">You can also use user alias or SIP URI instead of the user display name.</span></span>

        
        </div>
        
        <span data-ttu-id="3063e-120">例:</span><span class="sxs-lookup"><span data-stu-id="3063e-120">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "UCS Enabled Users"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3063e-p102">前記の例の最初のコマンドでは、UcsAllowed フラグを True に設定することで、新しいユーザーごとのポリシーを <EM>UCS Enabled Users</EM> という名前で作成しています。2 番目のコマンドでは、Ken Myer という表示名のユーザーにこのポリシーを割り当てています。これは、Ken Myer が統合連絡先ストアで有効になったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="3063e-p102">In the preceding example, the first command creates a new per-user policy named <EM>UCS Enabled Users</EM> with the UcsAllowed flag set to True. The second command assigns the policy to the user with the display name Ken Myer, which means that Ken Myer is now enabled for unified contact store.</span></span>

        
        <span data-ttu-id="3063e-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3063e-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

