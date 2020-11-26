---
title: 'Lync Server 2013: クライアントポリシーと設定'
description: 'Lync Server 2013: クライアントポリシーと設定。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client policies and settings
ms:assetid: c3ee47c0-7e20-47ec-809a-f4502d939586
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412966(v=OCS.15)
ms:contentKeyID: 48185330
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 608eefe293942c978270a7841fdd3a8f88876d1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434866"
---
# <a name="client-policies-and-settings-in-lync-server-2013"></a><span data-ttu-id="f995d-103">Lync Server 2013 のクライアントポリシーと設定</span><span class="sxs-lookup"><span data-stu-id="f995d-103">Client policies and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f995d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f995d-104">

<span> </span></span></span>

<span data-ttu-id="f995d-105">_**最終更新日:** 2012-06-18_</span><span class="sxs-lookup"><span data-stu-id="f995d-105">_**Topic Last Modified:** 2012-06-18_</span></span>

<span data-ttu-id="f995d-106">このトピックでは、Lync Server 2013 で構成できるクライアント関連の設定とポリシーの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="f995d-106">This topic provides an overview of the client-related settings and policies that you can configure in Lync Server 2013.</span></span> <span data-ttu-id="f995d-107">Lync Server 2013 には、クライアントを管理および構成するための次のツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f995d-107">Lync Server 2013 includes the following tools for managing and configuring clients:</span></span>

  - <span data-ttu-id="f995d-108">**Lync Server 2013 コントロールパネル**   サーバー、ユーザー、クライアント、デバイスを管理および構成するための web ベースのグラフィカルユーザーインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="f995d-108">**Lync Server 2013 Control Panel**   A web-based graphical user interface for managing and configuring servers, users, clients, and devices.</span></span>

  - <span data-ttu-id="f995d-109">**Lync Server 管理シェル**   豊富な Windows PowerShell コマンドラインインターフェイスコマンドレットと事前に定義されたスクリプトを含む、管理インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="f995d-109">**Lync Server Management Shell**   A management interface with a rich set of Windows PowerShell command-line interface cmdlets and a number of pre-defined scripts.</span></span>

  - <span data-ttu-id="f995d-110">**Lync 2013 グループポリシー**    Office グループポリシー管理用テンプレートを使用して、クライアントに対して構成できる一連のポリシー。</span><span class="sxs-lookup"><span data-stu-id="f995d-110">**Lync 2013 Group Policy**    A set of policies that you can configure for clients by using the Office Group Policy Administrative Template.</span></span> <span data-ttu-id="f995d-111">Lync 2013 クライアントを展開する前に、特定のクライアントブートストラップポリシーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f995d-111">Certain client bootstrapping policies must be configured before you deploy Lync 2013 clients.</span></span> <span data-ttu-id="f995d-112">Lync 2010 のその他のオプションの設定は、引き続き Lync 2013 で受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="f995d-112">Other optional settings from Lync 2010 continue to be honored in Lync 2013.</span></span>

<span data-ttu-id="f995d-113">このセクションでは、Lync Server 2013 でのクライアント関連の設定の変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="f995d-113">This section describes changes to client-related settings in Lync Server 2013.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f995d-114">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f995d-114">In this Section</span></span>

  - <span></span>  
    [<span data-ttu-id="f995d-115">Lync 2013 の新しい設定と変更された設定</span><span class="sxs-lookup"><span data-stu-id="f995d-115">New and changed settings for Lync 2013</span></span>](lync-server-2013-new-and-changed-settings-for-lync-2013.md)

  - <span></span>  
    [<span data-ttu-id="f995d-116">Lync 2013 のグループポリシー設定</span><span class="sxs-lookup"><span data-stu-id="f995d-116">Group Policy settings for Lync 2013</span></span>](lync-server-2013-group-policy-settings-for-lync-2013.md)

<span data-ttu-id="f995d-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f995d-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

