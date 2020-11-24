---
title: 内部サーバーとエッジ サーバーの間の接続の検証
description: 内部サーバーとエッジサーバー間の接続性を確認します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399800"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a><span data-ttu-id="b8b49-103">Lync Server 2013 での内部サーバーとエッジ サーバーの間の接続の検証</span><span class="sxs-lookup"><span data-stu-id="b8b49-103">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8b49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8b49-104">

<span> </span></span></span>

<span data-ttu-id="b8b49-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="b8b49-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="b8b49-106">Lync Server 2013 では、エッジサーバーと内部サーバーの間の接続を検証するために、個別の検証ウィザードを利用できました。</span><span class="sxs-lookup"><span data-stu-id="b8b49-106">In Lync Server 2013, a separate validation wizard was available to help validate connectivity between Edge Servers and internal servers.</span></span> <span data-ttu-id="b8b49-107">Lync Server 2013 では、エッジサーバーをインストールすると、接続の検証が自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="b8b49-107">In Lync Server 2013 validation of connectivity is done automatically when you install your Edge Servers.</span></span>

<span data-ttu-id="b8b49-108">中央管理ストアが配置されている内部コンピューター (または Lync Server 2013 コアコンポーネント (OcsCore.msi) がインストールされている任意のドメインに参加しているコンピューターで Windows PowerShell **CsManagementStoreReplicationStatus** コマンドレットを実行することで、構成情報のレプリケーションを検証できます。</span><span class="sxs-lookup"><span data-stu-id="b8b49-108">You can validate the replication of configuration information to the edge by running the Windows PowerShell **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located (or any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span> <span data-ttu-id="b8b49-109">初期結果では、レプリケーションに "True" ではなく "False" と表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="b8b49-109">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="b8b49-110">その場合は、 **CsManagementStoreReplication** コマンドレットを実行して、 **CsManagementStoreReplicationStatus** をもう一度実行する前に複製処理が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="b8b49-110">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="b8b49-111">Office Communications Server リモート接続アナライザーを使用してリモートユーザー接続を確認するなど、外部ユーザー接続を個別に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b8b49-111">You can verify external user connectivity separately, including using the Office Communications Server Remote Connectivity Analyzer to verify remote user connectivity.</span></span> <span data-ttu-id="b8b49-112">詳細については、「 [Lync Server 2013 で外部ユーザーへの接続を確認](lync-server-2013-verify-connectivity-for-external-users.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8b49-112">For details, see [Verify connectivity for external users in Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span></span>

<span data-ttu-id="b8b49-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8b49-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

