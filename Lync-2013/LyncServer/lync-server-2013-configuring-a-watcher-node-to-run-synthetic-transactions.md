---
title: 'Lync Server 2013: 代理トランザクションを実行するためのウォッチャーノードの構成'
description: 'Lync Server 2013: 代理トランザクションを実行するためのウォッチャーノードの構成。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to run synthetic transactions
ms:assetid: cedda508-8881-4079-88d5-49798f342ddf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205314(v=OCS.15)
ms:contentKeyID: 48185578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd5fdb3d1a1499a6ef79e962a41d9eb3ee174c33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433470"
---
# <a name="configuring-a-watcher-node-to-run-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="97df3-103">Lync Server 2013 で代理トランザクションを実行するためのウォッチャーノードの構成</span><span class="sxs-lookup"><span data-stu-id="97df3-103">Configuring a watcher node to run synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97df3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97df3-104">

<span> </span></span></span>

<span data-ttu-id="97df3-105">_**最終更新日:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="97df3-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="97df3-106">System Center agent ファイルをインストールしたら、次にウォッチャーノード自体を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97df3-106">After the System Center agent files have been installed, you must next configure the watcher node itself.</span></span> <span data-ttu-id="97df3-107">ウォッチャーノードを構成するための手順は、ウォッチャーノードのコンピューターが境界ネットワーク内にあるか境界ネットワークの外側にあるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="97df3-107">The steps you take to configure a watcher node will vary depending on whether your watcher node computer lies inside your perimeter network or outside your perimeter network.</span></span>

<span data-ttu-id="97df3-108">監視ノードの構成時には、そのノードが使用する認証方法の種類も選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97df3-108">When you configure a watcher node, you must also choose the type of authentication method to be employed by that node.</span></span> <span data-ttu-id="97df3-109">Lync Server 2013 では、次の2つの認証方法のいずれかを選択できます。信頼されたサーバーまたは資格情報認証。</span><span class="sxs-lookup"><span data-stu-id="97df3-109">Lync Server 2013 enables you to choose one of two authentication methods: Trusted Server or Credential Authentication.</span></span> <span data-ttu-id="97df3-110">この2つの方法の違いについては、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="97df3-110">The differences between these two methods are outlined in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97df3-111">構成</span><span class="sxs-lookup"><span data-stu-id="97df3-111">Configuration</span></span></th>
<th><span data-ttu-id="97df3-112">説明</span><span class="sxs-lookup"><span data-stu-id="97df3-112">Description</span></span></th>
<th><span data-ttu-id="97df3-113">サポートされている場所</span><span class="sxs-lookup"><span data-stu-id="97df3-113">Locations Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97df3-114">信頼できるサーバー</span><span class="sxs-lookup"><span data-stu-id="97df3-114">Trusted Server</span></span></p></td>
<td><p><span data-ttu-id="97df3-115">内部サーバーを偽装する証明書を使用し、認証チャレンジをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="97df3-115">Uses a certificate to impersonate an internal server and bypass authentication challenges.</span></span></p>
<p><span data-ttu-id="97df3-116">これは、各ウォッチャーノードで多くのユーザーパスワードの代わりに1つの証明書を管理することを希望している管理者にとって便利です。</span><span class="sxs-lookup"><span data-stu-id="97df3-116">This is useful for administrators who would prefer to manage a single certificate instead of many user passwords on each watcher node.</span></span></p></td>
<td><p><span data-ttu-id="97df3-117">エンタープライズの内側。</span><span class="sxs-lookup"><span data-stu-id="97df3-117">Inside the enterprise.</span></span></p>
<p><span data-ttu-id="97df3-118">この方法では、監視ノードが監視対象のプールと同じドメインに存在する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="97df3-118">Note that, with this method, the watcher node must be in the same domain as the pools being monitored.</span></span> <span data-ttu-id="97df3-119">ウォッチャーノードと監視対象のプールが異なるドメインにある場合は、代わりに資格情報認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="97df3-119">If the watcher node and the monitored pools are in different domains, use Credential Authentication instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97df3-120">資格情報認証</span><span class="sxs-lookup"><span data-stu-id="97df3-120">Credential Authentication</span></span></p></td>
<td><p><span data-ttu-id="97df3-121">ユーザー名とパスワードを各監視ノードの Windows 資格情報マネージャーに保管します。</span><span class="sxs-lookup"><span data-stu-id="97df3-121">Stores user names and passwords securely in Windows Credential Manager on each watcher node.</span></span></p>
<p><span data-ttu-id="97df3-122">このモードでは、より多くのパスワードを管理する必要がありますが、エンタープライズの外部にあるウォッチャーノードには唯一の選択肢です。</span><span class="sxs-lookup"><span data-stu-id="97df3-122">This mode requires more password management, but is the only option for watcher nodes located outside of the enterprise.</span></span> <span data-ttu-id="97df3-123">このような外側に位置する監視ノードを認証の際に信頼済みのエンドポイントとして扱うことはできません。</span><span class="sxs-lookup"><span data-stu-id="97df3-123">These watcher nodes cannot be treated as an endpoint trusted for authentication.</span></span></p></td>
<td><p><span data-ttu-id="97df3-124">エンタープライズの外側。</span><span class="sxs-lookup"><span data-stu-id="97df3-124">Outside the enterprise.</span></span></p>
<p><span data-ttu-id="97df3-125">エンタープライズの内側。</span><span class="sxs-lookup"><span data-stu-id="97df3-125">Inside the enterprise.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97df3-126">また、ファイアウォールで MonitoringHost.exe と PowerShell.exe の両方の受信規則が適用されていることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97df3-126">You should also verify that your firewall has inbound rules for both MonitoringHost.exe and PowerShell.exe.</span></span> <span data-ttu-id="97df3-127">これらのプロセスがファイアウォールによってブロックされた場合、代理トランザクションは 504 (サーバータイムアウト) エラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="97df3-127">If these processes are blocked by the firewall then your synthetic transactions will fail with a 504 (server timeout) error.</span></span>

<span data-ttu-id="97df3-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97df3-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

