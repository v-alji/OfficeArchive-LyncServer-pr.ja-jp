---
title: 'Lync Server 2013: Microsoft Lync 展開方法の決定'
description: 'Lync Server 2013: Microsoft Lync の展開方法を決定する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431233"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a>Lync Server 2013 展開方法の決定

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-03_

Lync を計画する場合、最初の主な決定として、Microsoft Lync: Lync Server 2013 をオンプレミスに展開する方法、またはクラウドで Microsoft 365 または Office 365 を使用して Lync Online を展開する方法が挙げられます。

  - **Lync Server 2013 オンプレミス** : lync のすべての機能セットが提供され、展開の構成、カスタマイズ、および操作に最適な柔軟性が提供されます。 すべてのサーバーがオンサイトにインストールされ、組織によって管理されます。 オンプレミスの展開では、Lync Server のさまざまな機能が提供されます。

  - **クラウドでの Lync Online** Lync Online は、Lync Server のビジネスクラス機能を犠牲にすることなく、クラウドベースのインスタントメッセージング、プレゼンス、会議のコストとアジリティの向上を希望する組織向けに設計されています。 Lync Online を使用すると、Microsoft は必要なサーバーインフラストラクチャを展開して管理し、継続的なメンテナンス、パッチ、アップグレードを処理します。 オンプレミスの展開で利用できる機能の一部は、Lync Online では利用できません。

どのような種類の展開を使用するかは、展開するワークロードと組織の地理的状態とビジネス状態によって異なります。

<div>

## <a name="lync-server"></a>Lync Server

オンプレミスの Lync Server 展開は、次のシナリオに適しています。

  - **完全なエンタープライズ Voip 機能**   PBX の代わりとして、または高度な通話機能を使用する完全なエンタープライズボイスソリューションの展開を計画している場合は、オンプレミスの Lync Server の展開が必要です。 オンプレミスは、PBX システムと trunks との直接接続、および応答グループやコールパークなどの高度な電話機能をサポートします。 現時点では、Lync Online はこれらの機能をサポートしていません。

  - **メディア品質コントロール**   通話受付制御 (CAC) 機能や QoS (Quality of Service) 機能など、さまざまな種類のメディア品質保証機能が必要な場合は、オンプレミスの展開が必要になります。

  - **常設チャット**   組織に常設チャットを展開する必要がある場合は、オンプレミスの展開を選択する必要があります。

  - **サードパーティのサーバーアプリケーション**   オンプレミスの展開のみが、Microsoft ユニファイドコミュニケーションマネージ API (UCMA) を使用する信頼されたサードパーティアプリケーションと連携できます。

  - **地域のサポートが必要な多国籍/地方企業**   複数の国または地域にデータセンターがあり、各地域にサーバーを展開して管理する必要がある場合は、この種類の地域管理機能を提供できるように、オンプレミス展開をお勧めします。

  - **ポリシー、レポート、アップグレードを完全に制御**   する  オンプレミスの Lync Server 展開機能を使用すると、サーバーとクライアントのすべてのポリシー、監視およびその他のレポート、アップグレードのタイミングなどへのアクセスが可能になります。 Lync Online には、ポリシー設定とレポートのサブセットが用意されています。このウィンドウには、アップグレードを承認するための重要なウィンドウが含まれています。

</div>

<div>

## <a name="lync-online"></a>Lync Online

上に挙げた要因が自分にとって重要ではない場合は、[Lync Online] を選んで、展開と管理性をさらに向上させることができます。 Lync Online は、強力な IM、プレゼンス、会議機能のセットを提供します。また、組織内のユーザー間での音声通話とビデオ通話も可能になります。

</div>

</div>

<span> </span>

</div>

</div>

</div>
