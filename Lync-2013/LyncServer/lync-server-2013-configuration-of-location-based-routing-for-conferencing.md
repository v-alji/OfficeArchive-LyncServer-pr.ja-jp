---
title: 'Lync Server 2013: 会議のための場所に基づくルーティングの構成'
description: 'Lync Server 2013: 会議の Location-Based ルーティングの構成。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399950"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Lync Server 2013 での会議のための場所に基づくルーティングの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-09-11_

Location-Based ルーティング会議アプリケーションは、Lync Server 2013 Location-Based ルーティングの構成に依存しています。 主な構成は次のとおりです。

  - 会議の参加者の場所は、ネットワーク サイトに基づいて決定されます。 Location-Based ルーティングを適用するには、ネットワークサイトとそれに関連付けられたネットワークサブネットが Lync Server で定義されている必要があります。

  - 会議の Location-Based ルーティングを適用するには、Location-Based ルーティング用に Lync 参加者を有効にする必要があります。

  - 会議に参加する PSTN エンドポイントの Location-Based ルーティングを適用するには、PSTN エンドポイントを接続するために使用される SIP トランクを Location-Based ルーティング用に構成する必要があります。

Lync Server 2013 Location-Based ルーティングの展開と構成の詳細については、「 [場所ベースのルーティング](lync-server-2013-configuring-location-based-routing.md)を構成する」を参照してください。

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Location-Based ルーティング会議アプリケーションを有効にする

Location-Based ルーティング会議アプリケーションは、既定では無効になっています。 このアプリケーションを有効にする前に、このアプリケーションに割り当てるのに適した優先順位を決める必要があります。 この優先度を決定するには、Lync Server 管理シェルで次のコマンドレットを実行します。

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

このコマンドレットで \<Pool FQDN\> は、Location-Based ルーティング会議アプリケーションを有効にするプールを指定します。

このコマンドレットは、Lync Server によってホストされているアプリケーションの一覧とそれぞれの priority の値を返します。 Location-Based ルーティング会議アプリケーションには、"UdcAgent" アプリケーションよりも大きく、"DefaultRouting"、"ExumRouting"、"OutboundRouting" アプリケーションよりも小さい優先度の値を割り当てる必要があります。 Location-Based ルーティング会議アプリケーションには、"UdcAgent" アプリケーションの優先度値より1ポイント高い優先度の値を割り当てることをお勧めします。

たとえば、"UdcAgent" アプリケーションの優先度値が "2" の場合 "DefaultRouting" アプリケーションの優先度値は "8" で、"ExumRouting" アプリケーションの優先度値は "9" で、"OutboundRouting" アプリケーションには "10" という優先度の値が設定されています。その場合は、Location-Based ルーティング会議アプリケーションに優先度値 "3" を割り当てる必要があります。 こうすると、アプリケーションの優先度が次の順序で設定されます。その他のアプリケーション (優先度: 0 から 1)、"UdcAgent" (優先度: 2)、Location-Based ルーティング会議アプリケーション (優先度: 3)、その他のアプリケーション (優先度: 4)、その他のアプリケーション (優先度:10)、"ExumRouting" (priority:10)、"OutboundRouting" (Priority:11)。

Location-Based ルーティング会議アプリケーションの正しい優先度の値を見つけたら、次のコマンドレットを使用して、ユーザーが Location-Based ルーティング用に有効になっている各 Front-End プールまたは Standard Edition Server に対して、次のコマンドレットを入力します。

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

次に例を示します。

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

このコマンドレットを使用した後、Location-Based ルーティング会議アプリケーションが有効になっているプールまたは Standard Edition サーバーで、すべてのフロントエンドサーバーを再起動します。

<div>


> [!IMPORTANT]  
> Enforcements での会議または提案転送へのルーティングは、該当するプールまたは Standard Edition サーバーのすべてのフロントエンドサーバーが再起動されるまでは適用されません。 Location-Based



</div>

Location-Based ルーティング会議アプリケーションが正常に有効になり、適用可能なすべての Lync サーバーが再起動されると、Location-Based ルーティングが有効になっている Lync ユーザーによって開催されたすべての会議が監視され、PSTN の有料電話のバイパスを防ぐことができます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

