---
title: 'Lync Server 2013: 常設チャット ポリシーを実行、付与、削除、または設定する'
description: 'Lync Server 2013: [実行]、[アクセスの許可]、[取得]、[削除]、または [常設チャット] ポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Run, grant, get, remove, or set Persistent Chat Policy
ms:assetid: 39ccdbe8-fb3d-47bc-96e2-9486b6d317e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204810(v=OCS.15)
ms:contentKeyID: 48183857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45763fa4d521efccd5ada62589e76e893d7a4933
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442272"
---
# <a name="run-grant-get-remove-or-set-persistent-chat-policy-in-lync-server-2013"></a><span data-ttu-id="a34ec-103">Lync Server 2013 で常設チャット ポリシーを実行、付与、削除、または設定する</span><span class="sxs-lookup"><span data-stu-id="a34ec-103">Run, grant, get, remove, or set Persistent Chat Policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a34ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a34ec-104">

<span> </span></span></span>

<span data-ttu-id="a34ec-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a34ec-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a34ec-106">新しい常設チャットポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="a34ec-106">To create a new Persistent Chat policy</span></span>

    New-CsPersistentChatPolicy -Identity <XdsIdentity> [-Enable <Switch Parameter>] [-Confirm <Switch Parameter>] [-Force <Switch Parameter>] [-WhatIf <Switch Parameter>] [-InMemory <Switch Parameter>]

<span data-ttu-id="a34ec-107">常設チャットポリシーを付与するには</span><span class="sxs-lookup"><span data-stu-id="a34ec-107">To grant Persistent Chat policy</span></span>

    Grant-CsPersistentChatPolicy -Identity <UserIdParameter> -PolicyName <String> [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="a34ec-108">常設チャットのポリシーを取得するには</span><span class="sxs-lookup"><span data-stu-id="a34ec-108">To get Persistent Chat policy</span></span>

    Get-CsPersistentChatPolicy [-Identity <XdsIdentity>] [-Filter <String>] [-LocalStore <Switch Parameter>]

<span data-ttu-id="a34ec-109">常設チャットポリシーを削除するには</span><span class="sxs-lookup"><span data-stu-id="a34ec-109">To remove Persistent Chat policy</span></span>

    Remove-CsPersistentChatPolicy -Identity <XdsIdentity> [-Confirm <Switch Parameter>] [-Force <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="a34ec-110">常設チャットポリシーを設定するには</span><span class="sxs-lookup"><span data-stu-id="a34ec-110">To set Persistent Chat policy</span></span>

    Set-CsPersistentChatPolicy [-Identity <XdsIdentity>] [-Instance < PSObject>]

<span data-ttu-id="a34ec-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a34ec-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

