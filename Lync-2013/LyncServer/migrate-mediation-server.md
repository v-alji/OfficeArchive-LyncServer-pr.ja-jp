---
title: 仲介サーバーを移行する
description: 仲介サーバーを移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Mediation Server
ms:assetid: b0b77121-2c8f-413e-b276-dbf1038361d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205173(v=OCS.15)
ms:contentKeyID: 48185117
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31cc4c95f0e9c86b48594238218db22f3ec1a387
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446872"
---
# <a name="migrate-mediation-server"></a>仲介サーバーを移行する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-28_

統合ウィザードを実行すると、仲介サーバーが Lync Server 2013 パイロットトポロジに統合されます。 ただし、Office Communications Server 2007 R2 プールは Lync Server 2013 仲介サーバーと通信できないため、すべてのユーザーが移行した後で、Lync Server 2013 仲介サーバーを構成します。 並列での移行中に、Lync Server 2013 プールは、Office Communications Server 2007 R2 仲介サーバーと通信します。

Lync Server 2013 仲介サーバーを構成する場合は、Office Communications Server 2007 R2 ゲートウェイもアップグレードまたは置き換える必要があります。 Office Communications Server 2007 R2 ゲートウェイは、Lync Server 2013 仲介サーバーをサポートしていません。 Lync Server 2013 で認定されているゲートウェイを展開して、Lync Server 2013 仲介サーバーと関連付ける必要があります。 Office Communications Server 2007 R2 の展開を完全に停止するには、この手順を実行する必要があります。

このセクションのトピックでは、Lync Server 2013 仲介サーバーの移行を完了した後に実行する必要がある構成タスクについて説明します。 併置された仲介サーバーをスタンドアロンの仲介サーバーに移行することは、任意のタスクです。

  - [仲介サーバーを構成する](configure-mediation-server.md)

  - [新しい Lync Server 2013 仲介サーバーを使用するようにボイスルートを変更する](change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md)

  - [併置した仲介サーバーをスタンドアロンの仲介サーバーに移行する (オプション)](transition-a-collocated-mediation-server-to-a-stand-alone-mediation-server-optional.md)

</div>

<span> </span>

</div>

</div>

</div>

