---
title: 'Lync Server 2013: グループ通話の集配番号をユーザーに割り当てる'
description: 'Lync Server 2013: グループ通話の集配番号をユーザーに割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438345"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a><span data-ttu-id="63454-103">グループ通話の集配番号を Lync Server 2013 のユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="63454-103">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63454-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63454-104">

<span> </span></span></span>

<span data-ttu-id="63454-105">_**最終更新日:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="63454-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="63454-106">グループ通話のピックアップグループ番号をコールパークの軌道テーブルに追加したら、グループをユーザーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="63454-106">After you add Group Call Pickup group numbers to the call park orbit table, you can assign the groups to users.</span></span> <span data-ttu-id="63454-107">セカンダリ拡張機能のアクティブ化 (SEFAUtil) リソースキットツールを使用して、ユーザーに通話ピックアップグループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63454-107">Use the secondary extension feature activation (SEFAUtil ) resource kit tool to assign call pickup groups to users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="63454-108">ハイブリッド展開では、オンラインのユーザーにグループの通話ピックアップグループを割り当てないでください。</span><span class="sxs-lookup"><span data-stu-id="63454-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="63454-109">自宅のユーザーはグループ通話のピックアップに参加できません。</span><span class="sxs-lookup"><span data-stu-id="63454-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="63454-110">つまり、オンラインに所属するユーザーへの呼び出しを他のユーザーが応答することや、他のユーザーへの呼び出しをオンラインに所属するユーザーが応答することはできません。</span><span class="sxs-lookup"><span data-stu-id="63454-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a><span data-ttu-id="63454-111">グループ通話のピックアップグループをユーザーに割り当てるには</span><span class="sxs-lookup"><span data-stu-id="63454-111">To assign a Group Call Pickup group to a user</span></span>

1.  <span data-ttu-id="63454-112">SEFAUtil ツールをインストールしたコンピューターに管理者権限でログオンします。</span><span class="sxs-lookup"><span data-stu-id="63454-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="63454-113">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="63454-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="63454-114">例:</span><span class="sxs-lookup"><span data-stu-id="63454-114">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="63454-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="63454-115">See Also</span></span>


[<span data-ttu-id="63454-116">Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にする</span><span class="sxs-lookup"><span data-stu-id="63454-116">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
[<span data-ttu-id="63454-117">Lync Server 2013 のユーザーに対してグループ通話のピックアップを無効にする</span><span class="sxs-lookup"><span data-stu-id="63454-117">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="63454-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63454-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

