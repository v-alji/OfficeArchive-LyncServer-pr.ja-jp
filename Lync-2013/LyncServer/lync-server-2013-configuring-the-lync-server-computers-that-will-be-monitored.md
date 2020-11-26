---
title: 'Lync Server 2013: 監視対象の Lync Server コンピューターを構成する'
description: 'Lync Server 2013: 監視される Lync Server コンピューターを構成する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 742bd8a67eb42472e598c45619514e9407cb29cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432556"
---
# <a name="configuring-the-lync-server-computers-that-will-be-monitored-in-lync-server-2013"></a>Lync Server 2013 で監視される Lync Server コンピューターを構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-20_

Lync Server 2013 は、Microsoft Lync Server 2010 で使用されるセントラル検出プロセスを使用していないため、監視する各 Lync Server 2013 コンピューターは、管理サーバーにその存在を自己報告できる必要があります。 これを可能にするには、監視する各コンピューターに Operations Manager エージェントファイルをインストールする必要があります。 エージェントファイルをインストールしたら、System Center プロキシとして動作するようにコンピューターを構成する必要があります。 これらの手順は、これらのコンピューターに Lync Server をインストールして構成した後に実行する必要があることに注意してください。

</div>

<span> </span>

</div>

</div>

</div>

