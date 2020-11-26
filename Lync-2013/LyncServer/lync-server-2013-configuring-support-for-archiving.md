---
title: 'Lync Server 2013: アーカイブのサポートを構成する'
description: 'Lync Server 2013: アーカイブのサポートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Archiving
ms:assetid: 579283fe-909c-46f2-a0c9-52ca1e7d63d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204905(v=OCS.15)
ms:contentKeyID: 48184187
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4209614ed1248ab0caf3cf438a922d569ba79630
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432633"
---
# <a name="configuring-support-for-archiving-in-lync-server-2013"></a><span data-ttu-id="5c324-103">Lync Server 2013 でアーカイブのサポートを構成する</span><span class="sxs-lookup"><span data-stu-id="5c324-103">Configuring support for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c324-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c324-104">

<span> </span></span></span>

<span data-ttu-id="5c324-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5c324-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5c324-106">トポロジにアーカイブを追加し、新しいトポロジを公開した後、展開でのアーカイブの最初の実装方法のオプションを構成し、展開用のアーカイブを有効にするために、1つ以上のアーカイブポリシーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c324-106">After adding Archiving to your topology and publishing the new topology, you need to configure options for how Archiving is initially implemented in your deployment, and then configure one or more Archiving policies to enable Archiving for your deployment and, optionally, for specific sites and users.</span></span> <span data-ttu-id="5c324-107">Lync Server 2013 コントロールパネルを使用して、この操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5c324-107">You can use Lync Server 2013 Control Panel to do this.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5c324-108">展開後、アーカイブ設定を変更してアーカイブを無効にするか、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c324-108">After deployment, you can change Archiving settings to disable or enable Archiving.</span></span> <span data-ttu-id="5c324-109">日常的な管理のためのアーカイブサポートを実装する方法、または展開後に組織内の新しい要件を満たす方法について詳しくは、「運用ドキュメントの <A href="lync-server-2013-managing-archiving.md">Lync Server 2013 アーカイブを管理</A> する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5c324-109">For details about how to implement archiving support for day-to-day management or to meet new requirements in your organization after deployment, see <A href="lync-server-2013-managing-archiving.md">Managing Lync Server 2013 Archiving</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5c324-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="5c324-110">In This Section</span></span>

  - [<span data-ttu-id="5c324-111">Lync Server 2013 でアーカイブオプションを構成する</span><span class="sxs-lookup"><span data-stu-id="5c324-111">Configuring Archiving options in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options.md)

  - [<span data-ttu-id="5c324-112">Lync Server 2013 でアーカイブポリシーを構成して割り当てる</span><span class="sxs-lookup"><span data-stu-id="5c324-112">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)

  - [<span data-ttu-id="5c324-113">Lync Server 2013 でのフェデレーション パートナーに対するアーカイブ免責事項の送信の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="5c324-113">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

<span data-ttu-id="5c324-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c324-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

