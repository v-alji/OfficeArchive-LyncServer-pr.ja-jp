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
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a>Lync Server 2013 での転送中のデータの保護 (アーカイブ データベース、監視データベース、グループ チャット コンプライアンス サーバー データベース)

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-12-05_

Microsoft Lync Server 2013 アーカイブサーバーと監視サーバーはどちらも、メッセージキュー (MSMQ とも呼ばれます) サービスを使って、コレクションポイントからリポジトリサーバーにデータメッセージを収集し、確実に移動します。 コンプライアンスサービスは、グループチャットサーバーと連携してデータを収集します。これには、メッセージキューも使用されます。

Lync Server 2013 では、ネットワーク上のデータに対する内部保護は行われません。ただし、このトラフィックをセキュリティで保護するための要件がある場合は、メッセージキューサービスは送信メッセージキューのメッセージレベルで暗号化を提供できます。 これは、Active Directory ドメインサービスによって管理される証明書を使用して実現されます。 詳細については、「付録 D: windows Server 2008 でのメッセージキューとインターネット通信」 [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) または「付録 I: windows server 2008 r2 での Windows server 2008 r2 のメッセージキューとインターネット通信」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) 。

</div>

<span> </span>

</div>

</div>

</div>

