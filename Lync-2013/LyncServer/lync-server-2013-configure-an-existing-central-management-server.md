---
title: 'Lync Server 2013: 既存の中央管理サーバーの構成'
description: 'Lync Server 2013: 既存のサーバーの全体管理サーバーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an existing Central Management Server
ms:assetid: d715b24a-1256-4a7c-a5ef-1cee41d6b733
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205315(v=OCS.15)
ms:contentKeyID: 48185584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef93281be2537ca5e4a5892a8617500ce54f3c45
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434125"
---
# <a name="configure-an-existing-central-management-server-in-lync-server-2013"></a><span data-ttu-id="c1809-103">Lync Server 2013 での既存の中央管理サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="c1809-103">Configure an existing Central Management Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c1809-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c1809-104">

<span> </span></span></span>

<span data-ttu-id="c1809-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="c1809-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="c1809-106">既存の Lync Server 2013 の展開から中央管理サーバーを再利用する場合は、次に説明する手順を実行して、Lync Server コントロールパネルと Windows PowerShell が正しく機能することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1809-106">If you reuse a Central Management Server from an existing Lync Server 2013 deployment, you must run the procedure described below to make sure that Lync Server Control Panel and Windows PowerShell function correctly.</span></span>

<div>

## <a name="to-configure-an-existing-central-management-server"></a><span data-ttu-id="c1809-107">既存のサーバーの全体管理サーバーを構成するには</span><span class="sxs-lookup"><span data-stu-id="c1809-107">To configure an existing Central Management Server</span></span>

1.  <span data-ttu-id="c1809-108">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1809-108">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="c1809-109">[ **更新プログラム** ]、[管理者] の役割コマンドレットを使用して、サーバーの全体管理サーバーに保存されている役割ベースのアクセス制御 (RBAC) ロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="c1809-109">Use the **Update-CsAdminRole** cmdlet to update the role-based access control (RBAC) roles stored in the Central Management Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c1809-110">エラーがない限り、出力は予期されません。</span><span class="sxs-lookup"><span data-stu-id="c1809-110">No output is expected unless there is an error.</span></span>

    
    <span data-ttu-id="c1809-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c1809-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

