---
title: 'Lync Server 2013: メディア バイパスの計画'
description: 'Lync Server 2013: メディアのバイパスを計画しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for media bypass
ms:assetid: 8ac732b6-8538-4d7b-b1a9-2035e419dac2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398703(v=OCS.15)
ms:contentKeyID: 48184768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92a50d9d838b0f13fd6837cbfadee1c48712f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424487"
---
# <a name="planning-for-media-bypass-in-lync-server-2013"></a>Lync Server 2013 でのメディア バイパスの計画

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-21_

メディアバイパスは、可能な限りメディアパスから仲介サーバーを削除します。これは、シグナルが仲介サーバーを通過する呼び出しに対して可能です。

メディア バイパスにより、遅延、不要な変換、パケット損失の可能性、および潜在的な障害点の数を低減して、音声品質を向上できます。 回避された通話のメディア処理を排除することで、仲介サーバーにかかる負荷が減るため、スケーラビリティが向上します。 この負荷の削減は、複数のゲートウェイを制御する仲介サーバーの機能を補完します。

仲介サーバーのないブランチサイトが1つまたは複数の WAN リンクによって中央サイトに接続されていて、帯域幅が制限されている場合、メディアのバイパスによって帯域幅の要件が低減されます。この場合、最初に WAN リンクを中央サイトの仲介サーバーに移動してから元のサイトに移動します

メディアの処理から仲介サーバーを削減することで、エンタープライズ Voip インフラストラクチャで必要な仲介サーバーの数を減らすこともできます。

次の図は、メディア バイパスを使用した場合と使用しない場合の、トポロジ内のメディアと信号の基本経路を示しています。

**メディア バイパスを使用した場合と使用しない場合の、メディアと信号の経路**

![音声 CAC メディア バイパス接続の適用](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "音声 CAC メディア バイパス接続の適用")

原則として、メディア バイパスを可能な限り有効にします。

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でのメディアのバイパスの概要](lync-server-2013-overview-of-media-bypass.md)

  - [Lync Server 2013 のメディア バイパス モード](lync-server-2013-media-bypass-modes.md)

  - [Lync Server 2013 でのメディア バイパスと通話受付管理](lync-server-2013-media-bypass-and-call-admission-control.md)

  - [Lync Server 2013 メディア バイパスの技術要件](lync-server-2013-technical-requirements-for-media-bypass.md)

</div>

<div>

## <a name="related-sections"></a>関連項目

[Lync Server 2013 での高度なエンタープライズ Voip 機能の展開](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

</div>

<div>

## <a name="see-also"></a>関連項目


[Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[Lync Server 2013 のグローバルメディアバイパスオプション](lync-server-2013-global-media-bypass-options.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

