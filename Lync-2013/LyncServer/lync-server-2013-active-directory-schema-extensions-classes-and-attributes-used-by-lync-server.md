---
title: 'Lync Server 2013: Lync Server が使用する Active Directory のスキーマ拡張、クラス、属性'
description: 'Lync Server 2013: Lync Server で使用される Active Directory スキーマの拡張機能、クラス、および属性。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory schema extensions, classes, and attributes used by Lync Server 2013
ms:assetid: 579bfa5a-9443-46dd-9a8e-07d00ba2824d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398379(v=OCS.15)
ms:contentKeyID: 48184188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: beac778d3315573f4d5cc6cb9c827a3a2fce9d0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398013"
---
# <a name="active-directory-schema-extensions-classes-and-attributes-used-by-lync-server-2013"></a><span data-ttu-id="3503a-103">Lync Server 2013 が使用する Active Directory のスキーマ拡張、クラス、属性</span><span class="sxs-lookup"><span data-stu-id="3503a-103">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3503a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3503a-104">

<span> </span></span></span>

<span data-ttu-id="3503a-105">_**最終更新日:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="3503a-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="3503a-106">このリファレンスセクションには、次の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3503a-106">This reference section includes the following information:</span></span>

  - <span data-ttu-id="3503a-107">Lync Server 2013 で新規または変更された Active Directory スキーマの拡張機能</span><span class="sxs-lookup"><span data-stu-id="3503a-107">Active Directory schema extensions that are new or changed for Lync Server 2013</span></span>
    
    <span data-ttu-id="3503a-108">Active Directory のスキーマには、Active Directory フォレストで作成できるすべてのオブジェクトクラスの正式な定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3503a-108">The Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="3503a-109">また、スキーマには、Active Directory オブジェクトに存在できるすべての属性の正式な定義も含まれています。</span><span class="sxs-lookup"><span data-stu-id="3503a-109">The schema also contains formal definitions of every attribute that can exist on an Active Directory object.</span></span> <span data-ttu-id="3503a-110">Active Directory のグローバルカタログには、フォレストのすべてのオブジェクトのレプリカと、各オブジェクトの属性のサブセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3503a-110">The Active Directory global catalog contains replicas of all the objects for the forest, along with a subset of the attributes for each object.</span></span> <span data-ttu-id="3503a-111">このセクションでは、Lync Server 2013 で新規または変更されたクラスと属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="3503a-111">This section describes the classes and attributes that are new or changed in Lync Server 2013.</span></span>

  - <span data-ttu-id="3503a-112">Lync Server で使用されるすべてのクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3503a-112">All the classes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="3503a-113">Lync Server で使用されるすべての属性とそれぞれの説明</span><span class="sxs-lookup"><span data-stu-id="3503a-113">All the attributes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="3503a-114">Lync Server で使用されるクラスの一覧と、それぞれに含まれる可能性のある属性</span><span class="sxs-lookup"><span data-stu-id="3503a-114">A list of the classes used by Lync Server, with the attributes each may contain</span></span>

  - <span data-ttu-id="3503a-115">グローバル設定とオブジェクト、およびフォレストの準備の際に作成されるユニバーサルサービスと管理グループに加えて、</span><span class="sxs-lookup"><span data-stu-id="3503a-115">Global settings and objects, in addition to the universal service and administration groups that are created during forest preparation</span></span>

  - <span data-ttu-id="3503a-116">ドメインの準備中にドメインルートと組み込みのコンテナー上に作成されるアクセス制御エントリ (Ace)</span><span class="sxs-lookup"><span data-stu-id="3503a-116">Access control entries (ACEs) that are created on the domain root and built-in containers during domain preparation</span></span>

  - <span data-ttu-id="3503a-117">Active Directory 組織単位 (OU) で実行される変更は、cssetuppermission の付与コマンドレットによって行われ \_ ます。</span><span class="sxs-lookup"><span data-stu-id="3503a-117">Changes that are made on an Active Directory organizational unit (OU) by the Grant\_CsSetupPermission cmdlet.</span></span>

  - <span data-ttu-id="3503a-118">Active Directory の OU で行われる変更は、 \_ "csoupermission の付与" コマンドレットによって変更されます。</span><span class="sxs-lookup"><span data-stu-id="3503a-118">Changes that are made on an Active Directory OU by the Grant\_CsOUPermission cmdlet.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3503a-119">このセクション中</span><span class="sxs-lookup"><span data-stu-id="3503a-119">In This Section</span></span>

  - [<span data-ttu-id="3503a-120">Lync Server 2013 でのスキーマの変更</span><span class="sxs-lookup"><span data-stu-id="3503a-120">Schema changes in Lync Server 2013</span></span>](lync-server-2013-schema-changes-in-lync-server-2013.md)

  - [<span data-ttu-id="3503a-121">Lync Server 2013 のスキーマクラスと説明</span><span class="sxs-lookup"><span data-stu-id="3503a-121">Schema classes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-classes-and-descriptions.md)

  - [<span data-ttu-id="3503a-122">Lync Server 2013 でのスキーマの属性と説明</span><span class="sxs-lookup"><span data-stu-id="3503a-122">Schema attributes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-and-descriptions.md)

  - [<span data-ttu-id="3503a-123">Lync Server 2013 のクラス別のスキーマ属性</span><span class="sxs-lookup"><span data-stu-id="3503a-123">Schema attributes by class in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-by-class.md)

  - [<span data-ttu-id="3503a-124">Lync Server 2013 でのフォレストの準備によって行われた変更</span><span class="sxs-lookup"><span data-stu-id="3503a-124">Changes made by forest preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-forest-preparation.md)

  - [<span data-ttu-id="3503a-125">Lync Server 2013 でのドメインの準備によって行われた変更</span><span class="sxs-lookup"><span data-stu-id="3503a-125">Changes made by domain preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-domain-preparation.md)

  - [<span data-ttu-id="3503a-126">Lync Server 2013 での Grant-CsSetupPermission による変更</span><span class="sxs-lookup"><span data-stu-id="3503a-126">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission)

  - [<span data-ttu-id="3503a-127">Lync Server 2013 での Grant-CsOUPermission による変更</span><span class="sxs-lookup"><span data-stu-id="3503a-127">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission)

<span data-ttu-id="3503a-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3503a-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

