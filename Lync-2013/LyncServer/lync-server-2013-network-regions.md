---
title: 'Lync Server 2013: ネットワーク領域'
description: 'Lync Server 2013: ネットワーク領域。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425160"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="7534b-103">Lync Server 2013 のネットワーク領域</span><span class="sxs-lookup"><span data-stu-id="7534b-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7534b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7534b-104">

<span> </span></span></span>

<span data-ttu-id="7534b-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="7534b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="7534b-106">*ネットワーク領域* とは、通話受付制御、E9-1、メディアバイパスの構成で使用されるネットワークハブまたはバックボーンのことです。</span><span class="sxs-lookup"><span data-stu-id="7534b-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="7534b-107">ネットワーク領域を表示、作成、または変更するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="7534b-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="7534b-108">たとえば、1つの音声機能のネットワーク領域を既に作成している場合は、新しいネットワークの領域を作成する必要はありません。その他の高度なエンタープライズ Voip 機能でも、同じネットワーク領域が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7534b-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="7534b-109">ただし、機能固有の設定を適用するために、ネットワーク地域に関する既存の定義に変更を加える必要が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="7534b-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="7534b-110">たとえば、E9-1-1 用のネットワーク地域を作成し (この場合は関連付けられた中央サイトは必要ありません)、次に通話受付管理を展開する場合は、中央サイトを指定するためにネットワーク地域の定義を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7534b-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="7534b-111">詳細については、「 [Lync Server 2013 で CAC のネットワーク領域を構成する](lync-server-2013-configure-network-regions-for-cac.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7534b-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7534b-112">ネットワーク領域定義の機能固有の要件については、この機能の展開に関するトピックで説明されています。</span><span class="sxs-lookup"><span data-stu-id="7534b-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7534b-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="7534b-113">In This Section</span></span>

  - [<span data-ttu-id="7534b-114">Lync Server 2013 でのネットワークの地域情報の表示</span><span class="sxs-lookup"><span data-stu-id="7534b-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="7534b-115">Lync Server 2013 でのネットワーク領域の作成または変更</span><span class="sxs-lookup"><span data-stu-id="7534b-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="7534b-116">Lync Server 2013 で既存のネットワーク領域を削除する</span><span class="sxs-lookup"><span data-stu-id="7534b-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="7534b-117">Reference</span><span class="sxs-lookup"><span data-stu-id="7534b-117">Reference</span></span>

[<span data-ttu-id="7534b-118">Lync Server 2013 での高度なエンタープライズ Voip 機能の展開</span><span class="sxs-lookup"><span data-stu-id="7534b-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="7534b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7534b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

