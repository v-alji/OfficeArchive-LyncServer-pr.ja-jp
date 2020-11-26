---
title: 'Lync Server 2013: ウォッチャーノードの管理'
description: 'Lync Server 2013: ウォッチャーノードを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing watcher nodes
ms:assetid: 66deaf49-a71f-4a6e-ada0-ea8b688ee921
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688078(v=OCS.15)
ms:contentKeyID: 49733674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1795b09bbca73d8157cf796ceeaaeafb9cc2ebc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425830"
---
# <a name="managing-watcher-nodes-in-lync-server-2013"></a><span data-ttu-id="a22a1-103">Lync Server 2013 でのウォッチャーノードの管理</span><span class="sxs-lookup"><span data-stu-id="a22a1-103">Managing watcher nodes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a22a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a22a1-104">

<span> </span></span></span>

<span data-ttu-id="a22a1-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="a22a1-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="a22a1-106">ウォッチャーノードで実行される代理トランザクションの変更に加えて、管理者は、 **CsWatcherNodeConfiguration** コマンドレットを使用して、他の2つの重要なタスク (ウォッチャーノードの有効化と無効化、テストの実行時に内部 url または外部 url のいずれかを使用するようにウォッチャーノードを構成するなど) を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="a22a1-106">In addition to modifying the synthetic transactions that are executed on a watcher node, administrators can also use the **Set-CsWatcherNodeConfiguration** cmdlet to carry out two other important tasks: enabling and disabling the watcher node, and configuring the watcher node to use either internal URLs or external URLs when running its tests.</span></span>

<span data-ttu-id="a22a1-107">既定では、監視ノードは、すべての有効な代理トランザクションを定期的に実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="a22a1-107">By default, watcher nodes are designed to periodically run all their enabled synthetic transactions.</span></span> <span data-ttu-id="a22a1-108">ただし、場合によっては、それらのトランザクションを中断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a22a1-108">Sometimes, however, you may need to suspend those transactions.</span></span> <span data-ttu-id="a22a1-109">たとえば、監視ノードを一時的にネットワークから切り離す場合は、代理トランザクションを実行する理由がありません。</span><span class="sxs-lookup"><span data-stu-id="a22a1-109">For example, if the watcher node is temporarily disconnected from the network, then there is no reason to run the synthetic transactions.</span></span> <span data-ttu-id="a22a1-110">ネットワーク接続されていない場合、これらのトランザクションは確実に失敗します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-110">Without network connectivity, those transactions are guaranteed to fail.</span></span> <span data-ttu-id="a22a1-111">ウォッチャーノードを一時的に無効にする場合は、次のようなコマンドを Lync Server 管理シェルから実行します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-111">If you want to temporarily disable a watcher node, run a command similar to this from the Lync Server Management Shell:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $False

<span data-ttu-id="a22a1-112">このコマンドは、watcher ノードの001.litwareinc.com での代理トランザクションの実行を無効にします。</span><span class="sxs-lookup"><span data-stu-id="a22a1-112">This command will disable the execution of synthetic transactions on the watcher node atl-watcher- 001.litwareinc.com.</span></span> <span data-ttu-id="a22a1-113">代理トランザクションの実行を再開するには、Enabled プロパティを True ($True) に戻します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-113">To resume execution of the synthetic transactions, set the Enabled property back to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $True

<div>


> [!NOTE]  
> <span data-ttu-id="a22a1-p103">Enabled プロパティを使用して監視ノードをオンまたはオフにできます。監視ノードを完全に削除する場合は、<STRONG>Remove-CsWatcherNodeConfiguration</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-p103">The Enabled property can be used to turn watcher nodes on or off. If you want to permanently delete a watcher node, use the <STRONG>Remove-CsWatcherNodeConfiguration</STRONG> cmdlet:</span></span><BR><span data-ttu-id="a22a1-116">Remove-CsWatcherNodeConfiguration – Identity "atl-watcher-001.litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="a22a1-116">Remove-CsWatcherNodeConfiguration –Identity "atl-watcher-001.litwareinc.com"</span></span><BR><span data-ttu-id="a22a1-117">このコマンドは、指定されたコンピューターからすべてのウォッチャーノードの構成設定を削除します。これにより、コンピューターで代理トランザクションが自動的に実行されることはなくなります。</span><span class="sxs-lookup"><span data-stu-id="a22a1-117">That command removes all the watcher node configuration settings from the specified computer, which prevents the computer from automatically running synthetic transactions.</span></span> <span data-ttu-id="a22a1-118">ただし、このコマンドを実行しても、System Center agent ファイルまたは Lync Server 2013 のシステムファイルはアンインストールされません。</span><span class="sxs-lookup"><span data-stu-id="a22a1-118">However, the command does not uninstall the System Center agent files or the Lync Server 2013 system files.</span></span>



</div>

<span data-ttu-id="a22a1-119">既定では、ウォッチャーノードでは、テストを実施するときに、組織の外部 Url が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a22a1-119">By default, watcher nodes use an organization's external URLs when conducting their tests.</span></span> <span data-ttu-id="a22a1-120">ただし、組織の内部 Url を使用するようにウォッチャーノードを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a22a1-120">However, watcher nodes can also be configured to use the organization's internal URLs.</span></span> <span data-ttu-id="a22a1-121">これにより、管理者は、境界ネットワーク内に配置されたユーザーの URL アクセスを検証できます。</span><span class="sxs-lookup"><span data-stu-id="a22a1-121">This enables administrators to verify URL access for users located inside the perimeter network.</span></span> <span data-ttu-id="a22a1-122">外部 Url の代わりに内部 Url を使用するようにウォッチャーノードを構成するには、UseInternalWebUrls プロパティを True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-122">To configure a watcher node to use internal URLs instead of external URLs, set the UseInternalWebUrls property to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $True

<span data-ttu-id="a22a1-123">このプロパティを既定値の False ($False) にリセットすると、ウォッチャーは外部 Url を使用します。</span><span class="sxs-lookup"><span data-stu-id="a22a1-123">If you reset this property to the default value of False ($False), the watcher will then use the external URLs:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $False

<span data-ttu-id="a22a1-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a22a1-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

