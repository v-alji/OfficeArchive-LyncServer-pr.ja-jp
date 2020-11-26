---
title: 'Lync Server 2013: 未承諾 IM の削減'
description: 'Lync Server 2013: 迷惑な IM を減らします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reducing unsolicited IM for Lync Server 2013
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518335(v=OCS.15)
ms:contentKeyID: 62625493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 294c53a6b82b4dc345fbb9afcf9983d5bd35893a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436672"
---
# <a name="reducing-unsolicited-im-for-lync-server-2013"></a><span data-ttu-id="3ebac-103">Lync Server 2013 での未承諾 IM の削減</span><span class="sxs-lookup"><span data-stu-id="3ebac-103">Reducing unsolicited IM for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ebac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ebac-104">

<span> </span></span></span>

<span data-ttu-id="3ebac-105">_**最終更新日:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="3ebac-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="3ebac-106">インテリジェント IM フィルターアプリケーションは、ユーザーエクスペリエンスの低下を最小限に抑えて、Microsoft Lync Server 2013 の展開を最も一般的なウイルスと保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3ebac-106">The Intelligent IM Filter application helps protect your Microsoft Lync Server 2013 deployment against the most common viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="3ebac-107">インテリジェント IM フィルターでは、次の機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="3ebac-107">The Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="3ebac-108">強化された URL フィルター</span><span class="sxs-lookup"><span data-stu-id="3ebac-108">Enhanced URL filtering</span></span>

  - <span data-ttu-id="3ebac-109">拡張されたファイル転送フィルター機能</span><span class="sxs-lookup"><span data-stu-id="3ebac-109">Enhanced file transfer filtering</span></span>

<span data-ttu-id="3ebac-110">インテリジェント IM フィルターを使用して、組織外のエンドポイントからの不要または有害なインスタントメッセージをブロックするようにフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="3ebac-110">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="3ebac-111">フィルターを設定するには、ハイパーリンクを含むインスタントメッセージや特定の拡張子のファイルなど、ブロックする必要があるものを決定するために使用する条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ebac-111">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks and files with specific extensions.</span></span>

<span data-ttu-id="3ebac-112">インテリジェント IM メッセージフィルターアプリケーションを展開する前に、メッセージが Lync Server 2013 サーバー間でルーティングされるときのフィルターオプションの適用方法を理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebac-112">Before you deploy the Intelligent IM Message Filter application, you should understand how filtering options are applied when messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="3ebac-113">これらのフィルターオプションの適用方法は、サーバーが1つの組織内に配置されているか、組織の境界を超えているかに関係なく一貫しています。</span><span class="sxs-lookup"><span data-stu-id="3ebac-113">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="3ebac-114">この一貫性は、カスタマイズされた通知や警告テキストがメッセージに挿入され、サーバー間で送信される方法に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3ebac-114">This consistency applies to the way that the customized notice, and warning texts are inserted into messages and sent across servers.</span></span>

<span data-ttu-id="3ebac-115">推奨されるフィルターオプションは、ハイパーリンクを使用してインスタントメッセージを許可することですが、インテリジェント IM フィルターを使用して、リンクを無効にするには、その前にアンダースコアを挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebac-115">The recommended filtering option is to allow instant messages with hyperlinks but require the Intelligent IM Filter to disable the link by inserting an underscore before it.</span></span> <span data-ttu-id="3ebac-116">このオプションを選ぶと、ハイパーリンクが設定されている各インスタントメッセージの先頭に表示されるユーザーへの通知を作成するオプションが追加されます。</span><span class="sxs-lookup"><span data-stu-id="3ebac-116">If you choose this option, you have the additional option of composing a notice to users that appears at the beginning of each instant message that contains a hyperlink.</span></span>

<span data-ttu-id="3ebac-117">2番目のフィルターオプションは、ハイパーリンクを変更せずにインスタントメッセージを送信できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="3ebac-117">A second filtering option is to allow instant messages with unmodified hyperlinks.</span></span> <span data-ttu-id="3ebac-118">このオプションを選択すると、各メッセージに挿入されたユーザーに警告を作成するための追加オプション (推奨) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ebac-118">If you choose this option, you have the additional option (recommended) of composing a warning to users that is inserted in each message.</span></span>

<span data-ttu-id="3ebac-119">3番目のオプションは、ハイパーリンクを含むすべてのインスタントメッセージをブロックすることです。</span><span class="sxs-lookup"><span data-stu-id="3ebac-119">A third option is to block all instant messages that contain hyperlinks.</span></span> <span data-ttu-id="3ebac-120">このオプションを選択すると、サーバーはユーザーに警告を送信します。</span><span class="sxs-lookup"><span data-stu-id="3ebac-120">If you choose this option, the server sends a warning to the user.</span></span> <span data-ttu-id="3ebac-121">この警告は、作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebac-121">You must write this warning.</span></span>

<span data-ttu-id="3ebac-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ebac-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

