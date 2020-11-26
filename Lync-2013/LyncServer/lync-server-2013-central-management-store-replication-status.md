---
title: 'Lync Server 2013: 中央管理ストアのレプリケーションの状態'
description: 'Lync Server 2013: サーバーの全体管理ストアのレプリケーションの状態。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435461"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a><span data-ttu-id="30fac-103">Lync Server 2013 での中央管理ストアのレプリケーションの状態</span><span class="sxs-lookup"><span data-stu-id="30fac-103">Central management store replication status in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30fac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30fac-104">

<span> </span></span></span>

<span data-ttu-id="30fac-105">_**最終更新日:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="30fac-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="30fac-106">管理者が Lync Server に何らかの変更を加えた場合 (たとえば、管理者が新しい音声ポリシーを作成した場合や、アドレス帳サーバー構成設定を変更した場合など)、その変更は中央管理ストアに記録されます。</span><span class="sxs-lookup"><span data-stu-id="30fac-106">When an administrator makes a change of some kind to Lync Server (for example, when an administrator creates a new voice policy or changes the Address Book Server configuration settings) that change is recorded in the Central Management store.</span></span> <span data-ttu-id="30fac-107">次に、Lync Server サービスまたはサーバーの役割を実行しているすべてのコンピューターに変更を複製する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30fac-107">In turn, the change must then be replicated to all the computers that are running Lync Server services or server roles.</span></span>

<span data-ttu-id="30fac-108">データをレプリケートするために、(中央管理サーバー上で動作している) マスター レプリケーターは、変更後の構成データのスナップショットを作成します。</span><span class="sxs-lookup"><span data-stu-id="30fac-108">To replicate data, the Master Replicator (running on the Central Management Server) creates a snapshot of the changed configuration data.</span></span> <span data-ttu-id="30fac-109">次に、このスナップショットのコピーが、Lync Server サービスまたはサーバーの役割を実行している各コンピューターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="30fac-109">A copy of this snapshot is then sent to each computer that is running Lync Server services or server roles.</span></span> <span data-ttu-id="30fac-110">それらのコンピューター上では、レプリケーション エージェントがスナップショットを受信し、変更後のデータをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="30fac-110">On those computers, a replication agent receives the snapshot and uploads the changed data.</span></span> <span data-ttu-id="30fac-111">次に、エージェントは、マスター レプリケーターに、レプリケーションの最新の状態を報告するメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="30fac-111">The agent then sends the Master Replicator a message reporting the latest replication status.</span></span>

<span data-ttu-id="30fac-112">Get-CsManagementStoreReplicationStatus コマンドレットを使用すると、組織内のすべての Lync Server コンピューターのレプリケーションの状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="30fac-112">The Get-CsManagementStoreReplicationStatus cmdlet enables you to verify the replication status for any (or all) of the Lync Server computers in your organization.</span></span>

<span data-ttu-id="30fac-113">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーが、Get-CsManagementStoreReplicationStatus  コマンドレットのローカル実行を承認されています。</span><span class="sxs-lookup"><span data-stu-id="30fac-113">Who can run this cmdlet?</span></span> <span data-ttu-id="30fac-114">RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="30fac-114">By default, members of the following groups are authorized to run the Get-CsManagementStoreReplicationStatus cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span>

<span data-ttu-id="30fac-115">このコマンドレットが割り当てられたすべての RBAC ロール (自分自身で作成したカスタム RBAC ロールを含む) の一覧を返すには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="30fac-115">To return a list of all RBAC roles this cmdlet was assigned to (including any custom RBAC roles that you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a><span data-ttu-id="30fac-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="30fac-116">See Also</span></span>


[<span data-ttu-id="30fac-117">Get-CsManagementStoreReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="30fac-117">Get-CsManagementStoreReplicationStatus</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

<span data-ttu-id="30fac-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30fac-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

