---
title: 'Lync Server 2013: メディア バイパスと仲介サーバー'
description: 'Lync Server 2013: メディアバイパスと仲介サーバー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425704"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a>Lync Server 2013 のメディア バイパスと仲介サーバー

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-21_

メディアのバイパスは、管理者がユーザーのエンドポイントと公衆交換電話網 (PSTN) ゲートウェイの間で直接流れるようにするための Lync Server の機能です。 メディアのバイパスでは、待ち時間の削減、不必要な翻訳、パケット損失の可能性、および潜在的な障害ポイントの数によって通話品質が向上します。 仲介サーバーのないリモートサイトが1つまたは複数の WAN リンクによって中央サイトに接続されていて、帯域幅が制限されている場合、メディアのバイパスでは、リモートサイトのクライアントから中央サイトの仲介サーバーへの直接フローを行うことなく、そのローカルゲートウェイに直接流れるメディアを有効にすることによって、帯域このメディア処理の削減は、複数のゲートウェイを制御するための仲介サーバーの機能にも補います。

メディア バイパスと通話受付管理 (CAC) を同時に使用することはできません。 通話にメディア バイパスを使用している場合、その通話に対して CAC は実行されません。 通話に関連するリンクについて、帯域幅に制約のあるリンクがないことを前提としています。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の通話受付管理と仲介サーバー](lync-server-2013-call-admission-control-and-mediation-server.md)  


[Lync Server 2013 でのメディア バイパスの計画](lync-server-2013-planning-for-media-bypass.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

