---
title: セキュリティ構成ウィザードで IIS のポートを閉じた後にサーバーを再アクティブ化する
description: セキュリティ構成ウィザードが終了した後にサーバーを再アクティブ化する IIS のポートを閉じます。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436721"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a><span data-ttu-id="b76d2-103">セキュリティ構成ウィザードで IIS のポートを閉じた後にサーバーを再アクティブ化する</span><span class="sxs-lookup"><span data-stu-id="b76d2-103">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b76d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b76d2-104">

<span> </span></span></span>

<span data-ttu-id="b76d2-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b76d2-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b76d2-106">一部の Lync Server 2013 ロールでは、インターネットインフォメーションサービス (IIS) ポート4443で Web サービスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b76d2-106">Some Lync Server 2013 roles run Web Services on Internet Information Services (IIS) port 4443.</span></span> <span data-ttu-id="b76d2-107">Lync Server 展開ウィザードを実行するか、[Bootstrapper.exe] を使うか、または、 **CsComputer** コマンドレットを使用して、ファイアウォールで例外を作成し、ポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b76d2-107">Running the Lync Server Deployment Wizard, Bootstrapper.exe, or using the **Enable-CsComputer** cmdlet creates an exception in the firewall and opens the port.</span></span> <span data-ttu-id="b76d2-108">その後、Windows Server 2008 R2 セキュリティ構成ウィザード (またはその他の強化スクリプト) を実行すると、ポート4443はブロックされ、外部クライアントは Web サービスに接続できなくなります。</span><span class="sxs-lookup"><span data-stu-id="b76d2-108">If you then run the Windows Server 2008 R2 Security Configuration Wizard (or other hardening scripts), port 4443 will be blocked, and external clients will not be able to contact Web Services.</span></span> <span data-ttu-id="b76d2-109">ポートをもう一度開くには、ファイアウォールの例外を直接変更するか、サーバーを再アクティブ化することができます。</span><span class="sxs-lookup"><span data-stu-id="b76d2-109">To reopen the port you can either modify the firewall exception directly or re-activate the server.</span></span>

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a><span data-ttu-id="b76d2-110">展開ウィザードを使用してサーバーを再アクティブ化するには</span><span class="sxs-lookup"><span data-stu-id="b76d2-110">To re-activate the server by using the Deployment Wizard</span></span>

1.  <span data-ttu-id="b76d2-111">Lync Server の展開ウィザードのページで、[**手順 2: Lync サーバーコンポーネントをセットアップまたは削除** する] の横にある [**実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b76d2-111">On the Lync Server Deployment Wizard page, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

2.  <span data-ttu-id="b76d2-112">[ **Lync Server コンポーネントのセットアップ** ] ページで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b76d2-112">On **Setup Lync Server components** page, click **Next**.</span></span>

3.  <span data-ttu-id="b76d2-113">[ **コマンドの実行** ] ページで、タスクの状態が [完了] と表示されたら、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b76d2-113">On the **Executing Commands** page, when the task status is shown as completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="b76d2-114">bootstrapper.exe を使用するか、または <STRONG>CsComputer を有効</STRONG> にしてサーバーを再アクティブ化することもできます。</span><span class="sxs-lookup"><span data-stu-id="b76d2-114">You can also use bootstrapper.exe or <STRONG>Enable-CsComputer</STRONG> to re-activate the server.</span></span>

    
    <span data-ttu-id="b76d2-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b76d2-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

