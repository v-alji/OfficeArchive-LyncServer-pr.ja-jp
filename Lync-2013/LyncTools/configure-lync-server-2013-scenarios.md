---
title: Lync Server 2013 のシナリオを構成する
description: Lync Server 2013 のシナリオを構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 Scenarios
ms:assetid: 6705346b-1512-4af3-85e4-64dfa6ee6f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945596(v=OCS.15)
ms:contentKeyID: 51541420
ms.date: 12/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4a5b7bd271191067779ac358807cc54918b16bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440074"
---
# <a name="configure-lync-server-2013-scenarios"></a><span data-ttu-id="8044d-103">Lync Server 2013 のシナリオを構成する</span><span class="sxs-lookup"><span data-stu-id="8044d-103">Configure Lync Server 2013 Scenarios</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8044d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8044d-104">

<span> </span></span></span>

<span data-ttu-id="8044d-105">_**最終更新日:** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="8044d-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="8044d-106">Lync Server 2013 応力とパフォーマンスツール (LyncPerfTool) を実行するには、最初に Lync Server 2013 トポロジを実行するシナリオに対して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8044d-106">To run the Lync Server 2013 Stress and Performance Tool (LyncPerfTool), the Lync Server 2013 topology must first be configured for the scenarios that will be executed.</span></span> <span data-ttu-id="8044d-107">Lync Server 2013 が構成されていないか、正しく構成されていない場合、ほとんどの場合、読み込みシミュレーションは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8044d-107">If Lync Server 2013 is not configured or is configured incorrectly, load simulation will fail in most cases.</span></span> <span data-ttu-id="8044d-108">Lync server 2013 のストレスとパフォーマンスツールを使って、lync server の管理シェルスクリプトと基本的なリソースファイルの例を提供して、Lync Server 2013 の構成の出発点として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8044d-108">With the Lync Server 2013 Stress and Performance Tool, we have provided example Lync Server Management Shell scripts and basic resource files that can be used as a starting point for configuring Lync Server 2013.</span></span> <span data-ttu-id="8044d-109">このトピックでは、提供されている Windows PowerShell の例について説明します。</span><span class="sxs-lookup"><span data-stu-id="8044d-109">This topic describes the Windows PowerShell examples provided.</span></span> <span data-ttu-id="8044d-110">Lync Server 2013 全般を構成する方法については、このトピックの目標ではありません。</span><span class="sxs-lookup"><span data-stu-id="8044d-110">Note that it is not the goal of this topic to describe how to configure Lync Server 2013 in general.</span></span> <span data-ttu-id="8044d-111">Lync Server 2013 での Windows PowerShell の使用の詳細については、「Lync Server 管理シェルに関するドキュメント」を参照してください <https://technet.microsoft.com/library/gg398474.aspx> 。</span><span class="sxs-lookup"><span data-stu-id="8044d-111">For details about working with Windows PowerShell in Lync Server 2013, see the Lync Server Management Shell documentation at <https://technet.microsoft.com/library/gg398474.aspx>.</span></span>

<div>

## <a name="about-running-lync-server-management-shell-scripts"></a><span data-ttu-id="8044d-112">Lync Server 管理シェルスクリプトの実行について</span><span class="sxs-lookup"><span data-stu-id="8044d-112">About Running Lync Server Management Shell Scripts</span></span>

<span data-ttu-id="8044d-113">ここでは、ロードシミュレーションを実行するための準備として使用される可能性のある Lync Server Management Shell スクリプトの例を提供しています。</span><span class="sxs-lookup"><span data-stu-id="8044d-113">We have provided example Lync Server Management Shell scripts that may be used in preparation for running load simulation.</span></span> <span data-ttu-id="8044d-114">このスクリプトは、読み込みシミュレーションを目的としているため、単純で寛容なものであるため、運用には適していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8044d-114">Because the scripts are intended for load simulation, they are simple and permissive, and therefore may not be appropriate for production.</span></span> <span data-ttu-id="8044d-115">すべてのスクリプトは例であり、確認する必要があります。また、場合によっては、トポロジを反映するように変更されます。</span><span class="sxs-lookup"><span data-stu-id="8044d-115">All scripts are examples and must be reviewed, and, in some cases, modified to reflect your topology.</span></span> <span data-ttu-id="8044d-116">少なくとも、応答グループサービス (RGS) シナリオは、エージェントグループに割り当てられているエージェントを指定するように変更する必要があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="8044d-116">At a minimum, we expect that the Response Group Service (RGS) scenario would need to be modified to specify the agents that are assigned to the agent groups.</span></span> <span data-ttu-id="8044d-117">ただし、このロードをシミュレートするオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="8044d-117">However, you have the option to not simulate this load.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="8044d-118">提供されている例を確認して理解してください。</span><span class="sxs-lookup"><span data-stu-id="8044d-118">Take care in reviewing and understanding the examples provided.</span></span> <span data-ttu-id="8044d-119">スクリプトはトポロジ内の既存の設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="8044d-119">Scripts will overwrite any existing settings in the topology.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="8044d-120">Windows PowerShell と Lync Server 管理シェルの使用の詳細については、「Lync Server 2013 Windows PowerShell のブログ」を参照してください <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A> 。</span><span class="sxs-lookup"><span data-stu-id="8044d-120">For details about using Windows PowerShell and the Lync Server Management Shell, see the Lync Server 2013 Windows PowerShell Blog at <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A>.</span></span>



</div>

</div>

<div>

## <a name="stress-and-performance-tool-client-version-monikers"></a><span data-ttu-id="8044d-121">ストレスとパフォーマンスのツールクライアントバージョンのモニカー</span><span class="sxs-lookup"><span data-stu-id="8044d-121">Stress and Performance Tool Client Version Monikers</span></span>

<span data-ttu-id="8044d-122">既定値の設定を変更した場合は、クライアントのバージョンチェックポリシーの構成が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="8044d-122">You may need to configure the Client Version Check policy if you have changed the settings from the default values.</span></span> <span data-ttu-id="8044d-123">詳細については、「サポートされているクライアントバージョンを構成する」を参照してください <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx> 。</span><span class="sxs-lookup"><span data-stu-id="8044d-123">For details, see “Configuring supported client versions” at <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx>.</span></span> <span data-ttu-id="8044d-124">Lync Server 2013 のストレスとパフォーマンスツールでは、Lync Server 2013 と通信するときに、次のユーザーエージェントバージョンが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8044d-124">The Lync Server 2013 Stress and Performance Tool uses the following User Agent Versions by default when communicating with Lync Server 2013:</span></span>

  - <span data-ttu-id="8044d-125">LSPT/15.0.0.0 (Lync Server 2013 応力とパフォーマンスツール)</span><span class="sxs-lookup"><span data-stu-id="8044d-125">LSPT/15.0.0.0 (Lync Server 2013 Stress and Performance Tool)</span></span>

  - <span data-ttu-id="8044d-126">OCPHONE 電話/0.522</span><span class="sxs-lookup"><span data-stu-id="8044d-126">OCPHONE/.0.522</span></span>

<span data-ttu-id="8044d-127">LyncPerfTool のモビリティ (UCWA) クライアントの場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="8044d-127">These are for the Mobility (UCWA) client in LyncPerfTool:</span></span>

  - <span data-ttu-id="8044d-128">Ucwa Perf ツール/Web 会議</span><span class="sxs-lookup"><span data-stu-id="8044d-128">Ucwa Perf Tool/Web Conference</span></span>

  - <span data-ttu-id="8044d-129">Ucwa Perf ツール/モバイル</span><span class="sxs-lookup"><span data-stu-id="8044d-129">Ucwa Perf Tool/Mobile</span></span>

<span data-ttu-id="8044d-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8044d-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

