---
title: 'Lync Server 2013: 通話の詳細記録 (CDR)'
description: 'Lync Server 2013: 通話の詳細記録 (CDR)。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call detail recording (CDR)
ms:assetid: 67726075-c77c-4191-a64f-a1cf5c7bcbb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688079(v=OCS.15)
ms:contentKeyID: 49733675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 590f99fd0b8649ffb3c4df039488dc54a8f3b7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435776"
---
# <a name="call-detail-recording-cdr-in-lync-server-2013"></a><span data-ttu-id="e9922-103">Lync Server 2013 での通話の詳細記録 (CDR)</span><span class="sxs-lookup"><span data-stu-id="e9922-103">Call detail recording (CDR) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9922-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9922-104">

<span> </span></span></span>

<span data-ttu-id="e9922-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="e9922-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="e9922-106">通話詳細記録 (CDR) は、インスタント メッセージング、ボイス オーバー IP (VoIP) 通話、アプリケーション共有、ファイル送信などの、ピアツーピア アクティビティおよび会議に関する使用状況および診断情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="e9922-106">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities, including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings.</span></span> <span data-ttu-id="e9922-107">使用状況データは投資収益率 (ROI) の計算に、診断データはピアツーピア アクティビティおよび会議のトラブルシューティングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9922-107">The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span> <span data-ttu-id="e9922-108">Lync Server 2013 をインストールすると、CDR 用のグローバル構成設定の定義済みコレクションもインストールされます。</span><span class="sxs-lookup"><span data-stu-id="e9922-108">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for CDR.</span></span> <span data-ttu-id="e9922-109">このセクションのトピックを使用して、CDR を構成します。</span><span class="sxs-lookup"><span data-stu-id="e9922-109">Use the topics in this section to configure CDR.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e9922-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="e9922-110">In This Section</span></span>

  - [<span data-ttu-id="e9922-111">Lync Server 2013 で CDR 構成情報を表示する</span><span class="sxs-lookup"><span data-stu-id="e9922-111">View CDR configuration information in Lync Server 2013</span></span>](lync-server-2013-view-cdr-configuration-information.md)

  - [<span data-ttu-id="e9922-112">Lync Server 2013 での通話の詳細記録を有効にする</span><span class="sxs-lookup"><span data-stu-id="e9922-112">Enable call detail recording in Lync Server 2013</span></span>](lync-server-2013-enable-call-detail-recording.md)

  - [<span data-ttu-id="e9922-113">Lync Server 2013 で CDR 構成設定のコレクションを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="e9922-113">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="e9922-114">Lync Server 2013 で既存の CDR 構成設定のコレクションを削除する</span><span class="sxs-lookup"><span data-stu-id="e9922-114">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="e9922-115">Lync Server 2013 で通話の記録とエクスペリエンスデータベースの記録を手動で削除する</span><span class="sxs-lookup"><span data-stu-id="e9922-115">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e9922-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9922-116">See Also</span></span>


[<span data-ttu-id="e9922-117">Lync Server 2013 での通話の記録と画質設定の設定</span><span class="sxs-lookup"><span data-stu-id="e9922-117">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="e9922-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9922-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

