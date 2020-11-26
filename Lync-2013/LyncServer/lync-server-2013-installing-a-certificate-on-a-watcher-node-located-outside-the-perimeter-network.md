---
title: 'Lync Server 2013: 境界ネットワークの外側にあるウォッチャーノードに証明書をインストールする'
description: 'Lync Server 2013: 境界ネットワークの外側にあるウォッチャーノードに証明書をインストールします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing a certificate on a watcher node located outside the perimeter network
ms:assetid: 825c9c02-1951-4d7a-a25e-a313a85333f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688113(v=OCS.15)
ms:contentKeyID: 49733711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66f40886e9784b5bd4182a60b955745b5daf2034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427069"
---
# <a name="installing-a-certificate-on-a-watcher-node-located-outside-the-perimeter-network-of-lync-server-2013"></a>Lync Server 2013 の境界ネットワークの外側にあるウォッチャーノードに証明書をインストールする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-22_

境界ネットワーク (Lync Server Edge Server など) で実行されている System Center Operations Manager エージェント、エンタープライズ (外部の代理トランザクションウォッチャーノードなど)、または Active Directory ドメインサービスの信頼境界を超えている場合、System Center Operations Manager ゲートウェイサーバーの構成が必要になることがあります。 このサーバーの役割により、ルート管理サーバーとの信頼関係を持たないエージェントは、アラートを発生させることができます。 詳細については、System Center Operations Manager の TechNet ライブラリの「Operations Manager 2007 でゲートウェイサーバーを管理する」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703) 。

これらのいずれかの場所でエージェントを展開する場合は、watcher ノードが System Center Operations Manager に通知を送信できるようにする証明書を要求して構成する必要があります。 このプロセスを簡略化するために、Operations Manager チームは、ウォッチャーノードのコンピューターで正しい種類の証明書を要求およびインストールできる一連のユーティリティを作成しました。 詳細を確認し、これらのユーティリティをダウンロードするには、「証明書の生成ウィザードを使って簡単にドメインに参加していないエージェントの証明書を取得する」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421) 。

</div>

<span> </span>

</div>

</div>

</div>

