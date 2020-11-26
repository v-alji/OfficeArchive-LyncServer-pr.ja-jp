---
title: 'Lync Server 2013: グループ通話のピックアップをユーザーに対して有効にする'
description: 'Lync Server 2013: グループ通話のピックアップをユーザーに対して有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users
ms:assetid: 20ec5f41-6ba2-4156-82ed-b91d05b62a6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945620(v=OCS.15)
ms:contentKeyID: 51541457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27951e9000fd17aac90339cf2a507757ae96a397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437596"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013"></a><span data-ttu-id="47458-103">Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にする</span><span class="sxs-lookup"><span data-stu-id="47458-103">Enable Group Call Pickup for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47458-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47458-104">

<span> </span></span></span>

<span data-ttu-id="47458-105">_**最終更新日:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="47458-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="47458-106">SEFAUtil リソースキットツールを使用して、ユーザーのグループ通話のピックアップを有効にします。</span><span class="sxs-lookup"><span data-stu-id="47458-106">Use the SEFAUtil resource kit tool to enable Group Call Pickup for users.</span></span> <span data-ttu-id="47458-107">グループ通話のピックアップを有効にするには、コールパークの軌道の種類が GroupPickup のグループ番号がユーザーに割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="47458-107">Users must be assigned a group number with type GroupPickup in the call park orbit table to have Group Call Pickup enabled.</span></span> <span data-ttu-id="47458-108">通話集配グループ番号を割り当て、グループ通話のピックアップを同時に有効にするには、SEFAUtil.exe を実行するときに、/enablegrouppickup パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47458-108">You assign a call pickup group number and enable Group Call Pickup at the same time by using the /enablegrouppickup parameter when you run SEFAUtil.exe.</span></span>

<div>

## <a name="to-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="47458-109">ユーザーに対してグループ通話のピックアップを有効にするには</span><span class="sxs-lookup"><span data-stu-id="47458-109">To enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="47458-110">SEFAUtil ツールをインストールしたコンピューターに管理者権限でログオンします。</span><span class="sxs-lookup"><span data-stu-id="47458-110">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="47458-111">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="47458-111">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="47458-112">例:</span><span class="sxs-lookup"><span data-stu-id="47458-112">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="47458-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="47458-113">See Also</span></span>


[<span data-ttu-id="47458-114">グループ通話の集配番号を Lync Server 2013 のユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="47458-114">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[<span data-ttu-id="47458-115">Lync Server 2013 のユーザーに対してグループ通話のピックアップを無効にする</span><span class="sxs-lookup"><span data-stu-id="47458-115">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="47458-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47458-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

