---
title: 'Lync Server 2013: グループ通話のピックアップをユーザーに対して有効にし、グループ番号を割り当てる'
description: 'Lync Server 2013: グループ通話のピックアップを有効にして、グループ番号を割り当てることができます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users and assign a group number
ms:assetid: c33bb6c2-d43b-4fb6-a0fa-6d82a7b09abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945650(v=OCS.15)
ms:contentKeyID: 51541517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a03fcb20bfd88842dc8b29100b9ece595bf76254
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428924"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013-and-assign-a-group-number"></a><span data-ttu-id="61d53-103">Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にし、グループ番号を割り当てる</span><span class="sxs-lookup"><span data-stu-id="61d53-103">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61d53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61d53-104">

<span> </span></span></span>

<span data-ttu-id="61d53-105">_**最終更新日:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="61d53-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="61d53-106">コールパークの軌道の表に通話集配グループ番号を追加した後、グループ番号をユーザーに割り当て、グループ通話のピックアップを有効にします。</span><span class="sxs-lookup"><span data-stu-id="61d53-106">After you add call pickup group numbers to the call park orbit table, you assign the group numbers to users and enable Group Call Pickup for them.</span></span> <span data-ttu-id="61d53-107">セカンダリ拡張機能のアクティブ化 (SEFAUtil) リソースキットツールを使用して、グループ番号を割り当て、グループ通話のピックアップを有効にします。</span><span class="sxs-lookup"><span data-stu-id="61d53-107">Use the secondary extension feature activation (SEFAUtil) resource kit tool to assign group numbers and enable Group Call Pickup.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="61d53-108">ハイブリッド展開では、オンラインのユーザーにグループの通話ピックアップグループを割り当てないでください。</span><span class="sxs-lookup"><span data-stu-id="61d53-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="61d53-109">自宅のユーザーはグループ通話のピックアップに参加できません。</span><span class="sxs-lookup"><span data-stu-id="61d53-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="61d53-110">つまり、オンラインに所属するユーザーへの呼び出しを他のユーザーが応答することや、他のユーザーへの呼び出しをオンラインに所属するユーザーが応答することはできません。</span><span class="sxs-lookup"><span data-stu-id="61d53-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-number-and-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="61d53-111">グループ番号を割り当てて、ユーザーに対してグループ通話のピックアップを有効にするには</span><span class="sxs-lookup"><span data-stu-id="61d53-111">To assign a group number and enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="61d53-112">SEFAUtil ツールをインストールしたコンピューターに管理者権限でログオンします。</span><span class="sxs-lookup"><span data-stu-id="61d53-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="61d53-113">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="61d53-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="61d53-114">たとえば、グループ番号 199 をユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="61d53-114">For example, to assign group number 199 to a user:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199 

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="61d53-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="61d53-115">See Also</span></span>


[<span data-ttu-id="61d53-116">Lync Server 2013 のユーザーに対してグループ通話のピックアップを無効にする</span><span class="sxs-lookup"><span data-stu-id="61d53-116">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="61d53-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61d53-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

