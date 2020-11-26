---
title: System Center discovery に参加するように Lync Server コンピューターを構成する
description: System Center discovery に参加するように Lync Server コンピューターを構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computer to participate in System Center discovery
ms:assetid: 2f9c9cb0-3120-4571-9cd2-657c2123fe21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204776(v=OCS.15)
ms:contentKeyID: 48183731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d25ba3de673084b2e64e17790a2776cbe57f07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432563"
---
# <a name="configuring-the-lync-server-2013-computer-to-participate-in-system-center-discovery"></a><span data-ttu-id="20722-103">System Center discovery に参加するように Lync Server 2013 コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="20722-103">Configuring the Lync Server 2013 computer to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20722-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20722-104">

<span> </span></span></span>

<span data-ttu-id="20722-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="20722-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="20722-106">新しい Lync Server エージェントが System Center Operations Manager の検出プロセスに参加するようにするには、System Center Operations Manager コンソールがインストールされている各コンピューターで、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20722-106">To make sure that your new Lync Server agent participates in discovery process for System Center Operations Manager, you must complete the following procedure on each computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="20722-107">[ **管理** ] タブで、[ **エージェントで管理** します] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20722-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="20722-108">コンピューターの名前を右クリックし、[**プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20722-108">Right-click the name of the computer, and then click **Properties**.</span></span> <span data-ttu-id="20722-109">[ **プロパティ** ] ダイアログボックスの [ **セキュリティ** ] タブで、[ **このエージェントがプロキシとして機能することを許可し、他のコンピューター上の管理オブジェクトを検出** します] をクリックし、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20722-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="20722-110">手順2を完了したら、正常性エージェントサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="20722-110">After completing step 2, reboot the Health Agent service.</span></span> <span data-ttu-id="20722-111">(サービスを再起動すると、新しいコンピューターの検出が強制されます。</span><span class="sxs-lookup"><span data-stu-id="20722-111">(Rebooting the service will “force” discovery of the new machine.</span></span> <span data-ttu-id="20722-112">サービスを再起動しない場合は、新しいコンピューターが System Center Operations Manager によって検出されるまでに4時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="20722-112">If you do not reboot the service, it could take as long as 4 hours before the new machine is discovered by System Center Operations Manager.).</span></span> <span data-ttu-id="20722-113">サービスが再起動したら、そのコンピューターの Operations Manager イベントログにエラーイベントが記録されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="20722-113">After the service has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span>

<span data-ttu-id="20722-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20722-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

