---
title: 'Lync Server 2013: 既定の URL フィルターを変更する'
description: 'Lync Server 2013: 既定の URL フィルターを変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default URL filter
ms:assetid: 80a472b3-054e-45a6-80fc-9ee2bda28ee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182544(v=OCS.15)
ms:contentKeyID: 48184653
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 079fcc83cd9041f99f1d14663ad51e86f6c23619
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445709"
---
# <a name="modify-the-default-url-filter-in-lync-server-2013"></a><span data-ttu-id="d7c17-103">Lync Server 2013 で既定の URL フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="d7c17-103">Modify the default URL filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7c17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7c17-104">

<span> </span></span></span>

<span data-ttu-id="d7c17-105">_**トピックの最終更新日:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="d7c17-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="d7c17-106">インスタントメッセージング (IM) フィルターを使用すると、lync server 2013 には、Lync Server 2013 の展開全体でユーザー間の IM 会話に含まれる特定の Url をブロックするグローバル URL フィルターが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d7c17-106">By using the instant messaging (IM) filter, Lync Server 2013 provides a global URL filter that blocks specific URLs contained in IM conversations among users throughout your Lync Server 2013 deployment.</span></span> <span data-ttu-id="d7c17-107">Lync Server コントロールパネルを使用すると、次のことができます。</span><span class="sxs-lookup"><span data-stu-id="d7c17-107">By using Lync Server Control Panel, you can do the following:</span></span>

  - <span data-ttu-id="d7c17-108">インスタントメッセージの会話で、Url の一部またはすべてをブロックします。</span><span class="sxs-lookup"><span data-stu-id="d7c17-108">Block all or a subset of URLs in instant message conversations.</span></span>

  - <span data-ttu-id="d7c17-109">すべての Url を許可します。</span><span class="sxs-lookup"><span data-stu-id="d7c17-109">Allow all URLs.</span></span> <span data-ttu-id="d7c17-110">オプションとして、URL を含む各インスタントメッセージの先頭に挿入された通知を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d7c17-110">As an option, you can create a notice that is inserted at the beginning of each instant message that contains a URL.</span></span>

  - <span data-ttu-id="d7c17-111">特定の Url を許可し、URL を含む各インスタントメッセージに対して警告を追加します。</span><span class="sxs-lookup"><span data-stu-id="d7c17-111">Allow specific URLs and include a warning with each instant message that contains a URL.</span></span>

<span data-ttu-id="d7c17-112">さらに、特定の種類のファイルを含む Url をブロックしたり、インターネット Url をブロックしたりすることもできます。これにより、サーバーのローカルイントラネットゾーン内の Url (イントラネット Url) がサーバーを通過できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d7c17-112">In addition, you can choose to block URLs that contain specific file types, or block only Internet URLs by allowing URLs that are within the server’s local intranet zone — intranet URLs — to pass through the server.</span></span> <span data-ttu-id="d7c17-113">URL フィルタリングの詳細については、「 [Lync Server 2013 でインスタントメッセージング (IM) のファイル転送と URL フィルタリングを構成する](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7c17-113">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="d7c17-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7c17-114">See Also</span></span>


[<span data-ttu-id="d7c17-115">Lync Server 2013 でのインスタントメッセージング (IM) のファイル転送と URL フィルタリングの構成</span><span class="sxs-lookup"><span data-stu-id="d7c17-115">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="d7c17-116">Lync Server 2013 で特定のサイト用の新しいファイル転送フィルターを作成する</span><span class="sxs-lookup"><span data-stu-id="d7c17-116">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="d7c17-117">Lync Server 2013 で新しい URL フィルターを作成して、IM 会話のハイパーリンクを処理する</span><span class="sxs-lookup"><span data-stu-id="d7c17-117">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="d7c17-118">Lync Server 2013 で既定のファイル転送フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="d7c17-118">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  
  

<span data-ttu-id="d7c17-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7c17-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

