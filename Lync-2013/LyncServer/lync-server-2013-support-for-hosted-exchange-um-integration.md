---
title: 'Lync Server 2013: ホスト型 Exchange UM 統合のサポート'
description: Lync Server 2013 では、ホストされた Exchange UM との統合がサポートされています。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398120"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a>Lync Server 2013 でのホスト型 Exchange UM 統合のサポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-21_

Lync server 2013 ExUM ルーティングアプリケーションでは、次の図に示すように、オンプレミス環境での Exchange ユニファイドメッセージング (UM) との統合をサポートしています。この場合、Lync Server 2013 と Exchange UM は両方とも企業内でローカルにインストールされているか、またはサービスプロバイダーによってホストされている Exchange UM

![オンプレミスの Lync Server Exchange UM の展開](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "オンプレミスの Lync Server Exchange UM の展開")

次のモードがサポートされています。

  - **オンプレミスモード**   Lync Server 2013 と Exchange UM は両方とも、エンタープライズ内のローカルサーバーに展開されます。

  - **クロスプレミスモード**   Lync Server 2013 は企業内のローカルサーバーに展開され、Exchange UM は Microsoft Exchange Online のデータセンターなどのオンラインサービスプロバイダーの機能でホストされます。

  - **混在モード**   Lync Server 2013 の展開では、組織内の Microsoft Exchange Server を実行しているローカルサーバー上の一部のユーザーメールボックス、およびホストされている Exchange service データセンターにある一部のメールボックスを使用しています。
    
    <div>
    

    > [!NOTE]  
    > 混在モードは、評価中にユーザーをホストされた Exchange UM に移行するときに、移行ソリューションとして使用することができます。また、他のユーザーを移行した後で、一部のユーザーの Exchange UM サービスをオンプレミスのままにしておくと、永続的な解決策として使用できます。

    
    </div>

Lync Server 2013 をホストされた Exchange UM と統合するには、 *共有 SIP アドレス空間* ( *分割ドメイン* とも呼ばれます) を構成する必要があります。 この構成では、Lync Server 2013 とサードパーティがホストする Exchange UM サービスプロバイダーは両方とも、同じ SIP ドメインアドレス空間にアクセスできます。 詳細については、計画ドキュメントの「 [Lync Server 2013 の Hosted EXCHANGE UM 統合アーキテクチャ](lync-server-2013-hosted-exchange-um-integration-architecture.md) 」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

