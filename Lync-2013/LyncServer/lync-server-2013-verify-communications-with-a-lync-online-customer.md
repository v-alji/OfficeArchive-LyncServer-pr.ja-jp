---
title: 'Lync Server 2013: Lync Online の顧客との通信を確認する'
description: 'Lync Server 2013: Lync Online の顧客との通信を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399801"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a>Lync Online の顧客との通信を Lync Server 2013 で確認する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-08_

組織内の Lync ユーザーが Microsoft Lync Online 2010 顧客のユーザーと通信できるようにするには、次の手順を完了する必要があります。

  - すべての前提条件を満たしていること。 これには、内部サーバーとエッジサーバーの展開、組織に対するフェデレーションサポートの有効化、ユーザーアカウントのセットアップなどが含まれます。 詳細については、「 [Lync Online のお客様とのフェデレーションの前提条件 Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md)」を参照してください。

  - 内部展開でドメインアクセスのサポートが構成されている。 これには、ホストプロバイダーエントリの作成、および Lync Online の顧客のドメインからのアクセスを許可するように展開を構成することが含まれます。 詳細については、「 [Lync Server 2013 で Lync Online ドメインのフェデレーションサポートを構成する](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md)」を参照してください。

  - フェデレーションをサポートするようにユーザーアカウントを構成しました。 詳細については、「 [Lync Online のユーザーとのフェデレーションのためのユーザーアクセスを Lync Server 2013 で構成する](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md)」を参照してください。

上記のすべての手順を完了して、Lync Online 2010 顧客の管理者が、組織とのフェデレーションをサポートするオンラインサービスのすべての設定を完了したら、組織内の内部ユーザーと Lync Online 顧客のユーザーの間の通信をテストして、通信を確認します。 通信が失敗した場合は、エッジサーバーのログツールを使用して、ログファイルとトレースファイルをキャプチャし、問題のトラブルシューティングを行います。 ログツールの使用について詳しくは、「 [Lync Server 2013 管理ツール](lync-server-2013-open-lync-server-administrative-tools.md) を使用する」をご覧ください。 ログツールの詳細については、TechNet ライブラリの Lync Server 2010 Logging Tool のマニュアルを参照してください [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) 。

</div>

<span> </span>

</div>

</div>

</div>

