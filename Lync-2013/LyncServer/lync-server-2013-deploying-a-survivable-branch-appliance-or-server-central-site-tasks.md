---
title: 存続可能ブランチ アプライアンスまたはサーバーの展開 - 中央サイトのタスク
description: Survivable Branch Appliance または Server central site のタスクを展開する。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430134"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a><span data-ttu-id="5a1f1-103">Lync Server 2013 による存続可能ブランチ アプライアンスまたはサーバーの展開 - 中央サイトのタスク</span><span class="sxs-lookup"><span data-stu-id="5a1f1-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a1f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a1f1-104">

<span> </span></span></span>

<span data-ttu-id="5a1f1-105">_**最終更新日:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="5a1f1-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="5a1f1-106">セントラルサイトでこのセクションのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-106">Complete the tasks in this section at the central site.</span></span> <span data-ttu-id="5a1f1-107">Survivable Branch Server を展開している場合は、最初のタスクをスキップします。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-107">If you’re deploying a Survivable Branch Server, skip the first task.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="5a1f1-108">このセクションのタスクを実行する前に、次の条件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-108">Before you perform the tasks in this section, the following conditions must be in place:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="5a1f1-109">Lync Server はセントラルサイトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-109">Lync Server must be set up at the central site.</span></span></P>
> <LI>
> <P><span data-ttu-id="5a1f1-110">ブランチサイトのインストール技術者は、RTCUniversalSBATechnicians グループに追加されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-110">An installation technician at the branch site must be added to the RTCUniversalSBATechnicians group.</span></span></P></LI></UL><span data-ttu-id="5a1f1-111">さらに、次の操作を行うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-111">In addition, we recommend that you do the following:</span></span>
> <UL>
> <LI>
> <P><span data-ttu-id="5a1f1-112">各ブランチサイトに DHCP サーバーを展開して、クライアントが IP アドレスを取得できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-112">Deploy a DHCP server at each branch site to enable clients to obtain IP addresses.</span></span></P>
> <LI>
> <P><span data-ttu-id="5a1f1-113">各ブランチサイトに DHCP サーバーを展開する代わりに、Lync Server Management Shell コマンドレットの <STRONG>CsRegistrarConfiguration – EnableDHCPServer $true</STRONG>を使って、Survivable branch Appliance または Survivable branch Server で LYNC server DHCP を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-113">As an alternative to deploying a DHCP server at each branch site, enable Lync Server DHCP on the Survivable Branch Appliance or Survivable Branch Server by using the Lync Server Management Shell cmdlet <STRONG>Set-CsRegistrarConfiguration –EnableDHCPServer $true</STRONG>.</span></span> <span data-ttu-id="5a1f1-114">詳細については、計画ドキュメントの「 <A href="lync-server-2013-branch-site-resiliency-requirements.md">Lync Server 2013 のブランチサイトの回復要件</A> 」の「ハードウェアとソフトウェアの要件」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a1f1-114">For details, see the “Hardware and Software Requirements” section of <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5a1f1-115">このセクション中</span><span class="sxs-lookup"><span data-stu-id="5a1f1-115">In This Section</span></span>

  - [<span data-ttu-id="5a1f1-116">Lync Server 2013 での、Active Directory への存続可能ブランチ アプライアンスの追加</span><span class="sxs-lookup"><span data-stu-id="5a1f1-116">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</span></span>](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [<span data-ttu-id="5a1f1-117">Lync Server 2013 でのトポロジへのブランチ サイトの追加</span><span class="sxs-lookup"><span data-stu-id="5a1f1-117">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="5a1f1-118">Lync Server 2013 での存続可能ブランチ アプライアンスまたは存続可能ブランチ サーバーの定義</span><span class="sxs-lookup"><span data-stu-id="5a1f1-118">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="5a1f1-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a1f1-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

