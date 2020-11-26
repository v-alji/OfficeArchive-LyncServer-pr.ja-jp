---
title: 概要
description: 発表.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438744"
---
# <a name="introduction"></a><span data-ttu-id="06f5b-103">概要</span><span class="sxs-lookup"><span data-stu-id="06f5b-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06f5b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06f5b-104">

<span> </span></span></span>

<span data-ttu-id="06f5b-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="06f5b-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="06f5b-106">Lync Server 2013 のストレスとパフォーマンスツール (LyncPerfTool とも呼ばれます) では、次の種類のユーザーロードをシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="06f5b-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-107">インスタントメッセージング (IM) とプレゼンス</span><span class="sxs-lookup"><span data-stu-id="06f5b-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="06f5b-108">電話会議</span><span class="sxs-lookup"><span data-stu-id="06f5b-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f5b-109">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="06f5b-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="06f5b-110">VoIP (公衆交換電話網 (PSTN) シミュレーションを含む) ボイスオーバー IP (VoIP)</span><span class="sxs-lookup"><span data-stu-id="06f5b-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-111">Web Access クライアント会議</span><span class="sxs-lookup"><span data-stu-id="06f5b-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="06f5b-112">Microsoft Lync 2013 アテンダント</span><span class="sxs-lookup"><span data-stu-id="06f5b-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f5b-113">応答グループ</span><span class="sxs-lookup"><span data-stu-id="06f5b-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="06f5b-114">配布リストの展開</span><span class="sxs-lookup"><span data-stu-id="06f5b-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-115">アドレス帳のダウンロードとアドレス帳のクエリ</span><span class="sxs-lookup"><span data-stu-id="06f5b-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="06f5b-116">拡張 9-1-1 (E9) 通話と位置情報プロファイル (ダイヤルプラン)</span><span class="sxs-lookup"><span data-stu-id="06f5b-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f5b-117">MultiView</span><span class="sxs-lookup"><span data-stu-id="06f5b-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="06f5b-118">会議から複数のストリームを表示する</span><span class="sxs-lookup"><span data-stu-id="06f5b-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06f5b-119">Lync Server 2013 のストレスとパフォーマンスツールは、高度な構成のみを通じて、クロスプールの負荷生成とフェデレーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="06f5b-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="06f5b-120">このツールでは、次のクライアントのユーザーロードもシミュレートされません。</span><span class="sxs-lookup"><span data-stu-id="06f5b-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="06f5b-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="06f5b-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="06f5b-122">Lync 2013 常設チャット</span><span class="sxs-lookup"><span data-stu-id="06f5b-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="06f5b-123">このため、Lync Server 2013 のストレスとパフォーマンスツールは、次のコンポーネントのテストをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="06f5b-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="06f5b-124">Lync 2013 常設チャット</span><span class="sxs-lookup"><span data-stu-id="06f5b-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="06f5b-125">Exchange の統合シナリオ</span><span class="sxs-lookup"><span data-stu-id="06f5b-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="06f5b-126">Lync Server 2013 のストレスとパフォーマンスツールに含まれているアプリケーションとファイル</span><span class="sxs-lookup"><span data-stu-id="06f5b-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="06f5b-127">Lync Server 2013 のストレスとパフォーマンスツールには、次のアプリケーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="06f5b-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06f5b-128">ツール</span><span class="sxs-lookup"><span data-stu-id="06f5b-128">Tool</span></span></th>
<th><span data-ttu-id="06f5b-129">説明</span><span class="sxs-lookup"><span data-stu-id="06f5b-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="06f5b-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="06f5b-131">Lync Server 2013 ユーザープロビジョニングツール。</span><span class="sxs-lookup"><span data-stu-id="06f5b-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="06f5b-132">このツールは、ユーザーと連絡先を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="06f5b-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f5b-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="06f5b-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="06f5b-134">Lync Server 2013 のロード構成ツール。</span><span class="sxs-lookup"><span data-stu-id="06f5b-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="06f5b-135">このツールは、シミュレートするためのユーザーロードの特性を構成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="06f5b-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="06f5b-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="06f5b-137">Lync Server 2013 ストレスおよびパフォーマンスツール。</span><span class="sxs-lookup"><span data-stu-id="06f5b-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="06f5b-138">LyncPerfTool は、ユーザーロードをシミュレートするツールです。</span><span class="sxs-lookup"><span data-stu-id="06f5b-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f5b-139">Tmx</span><span class="sxs-lookup"><span data-stu-id="06f5b-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="06f5b-140">Lync Server 2013 ログツールを使用するには、tmx が必要です。</span><span class="sxs-lookup"><span data-stu-id="06f5b-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f5b-141">プロビジョニングスクリプトの例</span><span class="sxs-lookup"><span data-stu-id="06f5b-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="06f5b-142">次の例は、特定のシナリオに基づいて、ロードテストを実行するためのトポロジを構成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="06f5b-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="06f5b-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06f5b-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

