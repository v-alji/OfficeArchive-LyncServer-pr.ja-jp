---
title: 'Lync Server 2013: ディレクターを使った自動クライアント サインインの構成'
description: 'Lync Server 2013: ディレクターを使用するように自動クライアント Sign-In を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399620"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a>Lync Server 2013 でのディレクターを使った自動クライアント サインインの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-08_

Lync Server 2013、ディレクター、またはディレクタープールを展開する場合は、ベストプラクティスとして、自動クライアント Sign-In を使用することをお勧めします。 自動クライアントサインイン用に DNS サーバーを構成する方法について詳しくは、「計画ドキュメントの「 [Lync Server 2013 での自動クライアントサインインの dns 要件](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) 」をご覧ください。

既に自動クライアントサインインを展開している場合は、次のセクションを参照してディレクターで構成してください。

<div>

## <a name="single-director-instance"></a>単一のディレクターインスタンス

既に自動クライアント Sign-In 展開されていて、フロントエンドサーバーまたはフロントエンドプールをポイントしている場合は、そのディレクターをポイントするように DNS SRV レコードを変更する必要があります。

</div>

<div>

## <a name="director-pool"></a>ディレクタープール

既に自動クライアント Sign-In 展開されていて、フロントエンドサーバーまたはフロントエンドプールを指している場合は、そのディレクタープールをポイントするように DNS SRV レコードを変更する必要があります。

</div>

</div>

<span> </span>

</div>

</div>

</div>

