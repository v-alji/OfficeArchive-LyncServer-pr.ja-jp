---
title: 'Lync Server 2013: Exchange 記憶域との統合を有効または無効にする'
description: 'Lync Server 2013: Exchange ストレージとの統合を有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling integration with Exchange storage
ms:assetid: c08b9ba5-04f6-452a-b44c-c130f1564a34
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205228(v=OCS.15)
ms:contentKeyID: 48185295
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42d140bd99bdc4aa86bea2f6ad310c4e06f06faf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428777"
---
# <a name="enabling-or-disabling-integration-of-lync-server-2013-with-exchange-storage"></a><span data-ttu-id="f94fa-103">Lync Server 2013 と Exchange ストレージの統合を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="f94fa-103">Enabling or disabling integration of Lync Server 2013 with Exchange storage</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f94fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f94fa-104">

<span> </span></span></span>

<span data-ttu-id="f94fa-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="f94fa-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="f94fa-106">Lync Server 2013 コントロールパネルで、[アーカイブ構成] を使って、Exchange ストレージとの統合を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-106">In Lync Server 2013 Control Panel, you use Archiving configurations to enable and disable integration with Exchange storage.</span></span> <span data-ttu-id="f94fa-107">これには、次のアーカイブ構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f94fa-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="f94fa-108">Lync Server 2013 を展開するときに既定で作成されるグローバル構成。</span><span class="sxs-lookup"><span data-stu-id="f94fa-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="f94fa-109">作成および使用して、特定のサイトまたはプールに対するアーカイブの実装方法を指定することができる、オプションのサイトレベルとプールレベルの構成。</span><span class="sxs-lookup"><span data-stu-id="f94fa-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="f94fa-110">アーカイブ構成の実装方法について詳しくは、「指定できるオプションやアーカイブ構成の階層」をご覧ください。「計画ドキュメント、展開ドキュメント、または操作のドキュメントでの [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f94fa-110">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>

## <a name="to-enable-or-disable-integration-with-microsoft-exchange-storage"></a><span data-ttu-id="f94fa-111">Microsoft Exchange 記憶域との統合を有効または無効にするには</span><span class="sxs-lookup"><span data-stu-id="f94fa-111">To enable or disable integration with Microsoft Exchange storage</span></span>

1.  <span data-ttu-id="f94fa-112">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f94fa-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f94fa-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f94fa-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f94fa-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f94fa-115">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="f94fa-116">アーカイブ構成の一覧から、適切なグローバル構成、サイト構成、またはプール構成の名前をクリックし、[**編集**]、[**詳細の表示**] の順にクリックし、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f94fa-116">Click the name of the appropriate global, site, or pool configuration in the list of archiving configurations, click **Edit**, click **Show details**, and then do the following:</span></span>
    
      - <span data-ttu-id="f94fa-117">Exchange 2013 ストレージとの統合を有効にするには、[ **Microsoft Exchange 統合** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-117">To enable integration with Exchange 2013 storage, select the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="f94fa-118">Exchange 2013 ストレージとの統合を無効にするには、[ **Microsoft Exchange 統合** ] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-118">To disable integration with Exchange 2013 storage, clear the **Microsoft Exchange integration** check box.</span></span>

5.  <span data-ttu-id="f94fa-119">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f94fa-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f94fa-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="f94fa-120">See Also</span></span>


[<span data-ttu-id="f94fa-121">Lync Server 2013 でのアーカイブのしくみ</span><span class="sxs-lookup"><span data-stu-id="f94fa-121">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="f94fa-122">組織、サイト、およびプールの Lync Server 2013 でアーカイブ構成オプションを管理する</span><span class="sxs-lookup"><span data-stu-id="f94fa-122">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="f94fa-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f94fa-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

