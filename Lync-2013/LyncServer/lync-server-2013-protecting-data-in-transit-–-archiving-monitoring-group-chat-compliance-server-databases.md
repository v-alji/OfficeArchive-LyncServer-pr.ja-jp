---
title: 'Lync Server 2013: 転送中のデータの保護 (アーカイブ データベース、監視データベース、グループ チャット コンプライアンス サーバー データベース)'
description: 'Lync Server 2013: 輸送中のデータの保護–アーカイブ、監視、グループチャットのコンプライアンスサーバーデータベース。'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436847"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a><span data-ttu-id="5cb26-103">Lync Server 2013 での転送中のデータの保護 (アーカイブ データベース、監視データベース、グループ チャット コンプライアンス サーバー データベース)</span><span class="sxs-lookup"><span data-stu-id="5cb26-103">Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cb26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cb26-104">

<span> </span></span></span>

<span data-ttu-id="5cb26-105">_**最終更新日:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="5cb26-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="5cb26-106">Microsoft Lync Server 2013 アーカイブサーバーと監視サーバーはどちらも、メッセージキュー (MSMQ とも呼ばれます) サービスを使って、コレクションポイントからリポジトリサーバーにデータメッセージを収集し、確実に移動します。</span><span class="sxs-lookup"><span data-stu-id="5cb26-106">Microsoft Lync Server 2013 Archiving Server and Monitoring Server both use the Message Queuing (also known as MSMQ) service to collect and reliably move data messages from the collection point to the repository servers.</span></span> <span data-ttu-id="5cb26-107">コンプライアンスサービスは、グループチャットサーバーと連携してデータを収集します。これには、メッセージキューも使用されます。</span><span class="sxs-lookup"><span data-stu-id="5cb26-107">Compliance service collects data in conjunction with the Group Chat Server, which also uses Message Queuing.</span></span>

<span data-ttu-id="5cb26-108">Lync Server 2013 では、ネットワーク上のデータに対する内部保護は行われません。ただし、このトラフィックをセキュリティで保護するための要件がある場合は、メッセージキューサービスは送信メッセージキューのメッセージレベルで暗号化を提供できます。</span><span class="sxs-lookup"><span data-stu-id="5cb26-108">In Lync Server 2013, there is no internal protection for data on the wire; however, if there is a requirement to secure this traffic, the Message Queuing service can provide encryption at a message level on the sending message queue.</span></span> <span data-ttu-id="5cb26-109">これは、Active Directory ドメインサービスによって管理される証明書を使用して実現されます。</span><span class="sxs-lookup"><span data-stu-id="5cb26-109">This is accomplished using certificates that are managed by the Active Directory Domain Services.</span></span> <span data-ttu-id="5cb26-110">詳細については、「付録 D: windows Server 2008 でのメッセージキューとインターネット通信」 [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) または「付録 I: windows server 2008 r2 での Windows server 2008 r2 のメッセージキューとインターネット通信」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) 。</span><span class="sxs-lookup"><span data-stu-id="5cb26-110">For details, see Appendix D: Message Queuing and Internet Communication in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) or Appendix I: Message Queuing and Internet Communication in Windows Server 2008 R2 at [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) for Windows Server 2008 R2.</span></span>

<span data-ttu-id="5cb26-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cb26-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

