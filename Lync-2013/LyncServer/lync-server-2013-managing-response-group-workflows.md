---
title: 'Lync Server 2013: 応答グループワークフローを管理する'
description: 'Lync Server 2013: 応答グループワークフローを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group workflows
ms:assetid: 42cfccdd-2844-4875-b4e3-813e1df15f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520986(v=OCS.15)
ms:contentKeyID: 48183974
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2223fed2b5b030a2c92e0b958ae8545a7717f848
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437225"
---
# <a name="managing-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="50eb7-103">Lync Server 2013 での応答グループワークフローの管理</span><span class="sxs-lookup"><span data-stu-id="50eb7-103">Managing Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50eb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50eb7-104">

<span> </span></span></span>

<span data-ttu-id="50eb7-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="50eb7-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="50eb7-106">応答グループのワークフローでは、電話が呼び出しに応答する時刻からの呼び出しの動作が定義されます。</span><span class="sxs-lookup"><span data-stu-id="50eb7-106">A Response Group workflow defines the behavior of a call from the time that the phone rings to the time that an agent answers the call.</span></span> <span data-ttu-id="50eb7-107">ワークフローにはキューとルーティング情報が含まれ、ハントグループまたはインタラクティブな音声応答 (IVR) 情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50eb7-107">The workflow includes queue and routing information, and includes either hunt group or interactive voice response (IVR) information.</span></span>

<span data-ttu-id="50eb7-108">このセクションのトピックでは、IVR ワークフローの設計方法、カスタマイズされた業務時間と休日セットの作成方法、ワークフローの作成方法と変更方法、ワークグループの削除方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="50eb7-108">Topics in this section identify best practices for designing IVR workflows, and explain how to create customized business hours and holiday sets, how to create or modify workflows, and how to delete workgroups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="50eb7-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="50eb7-109">In This Section</span></span>

  - [<span data-ttu-id="50eb7-110">Lync Server 2013 での対話型音声応答通話フローの設計</span><span class="sxs-lookup"><span data-stu-id="50eb7-110">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="50eb7-111">省略Lync Server 2013 での応答グループの営業時間の定義</span><span class="sxs-lookup"><span data-stu-id="50eb7-111">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="50eb7-112">省略Lync Server 2013 で回答グループの休日セットを定義する</span><span class="sxs-lookup"><span data-stu-id="50eb7-112">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="50eb7-113">Lync Server 2013 でワークフローを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="50eb7-113">Create or modify a workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-workflow.md)

  - [<span data-ttu-id="50eb7-114">Lync Server 2013 でワークフローを削除する</span><span class="sxs-lookup"><span data-stu-id="50eb7-114">Delete a workflow in Lync Server 2013</span></span>](lync-server-2013-delete-a-workflow.md)

<span data-ttu-id="50eb7-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50eb7-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

