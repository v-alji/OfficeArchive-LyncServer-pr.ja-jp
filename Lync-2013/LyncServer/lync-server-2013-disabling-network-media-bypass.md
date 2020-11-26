---
title: 'Lync Server 2013: ネットワークメディアのバイパスを無効にする'
description: 'Lync Server 2013: ネットワークメディアのバイパスを無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429099"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a>Lync Server 2013 でネットワークメディアのバイパスを無効にする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-15_

メディアバイパスの設定は、Microsoft Lync Server 2013 の展開でグローバルに適用されます。 メディアのバイパスでは、仲介サーバーを経由せずに通話を発信できます。 メディアのバイパスを使用する場合の詳細については、「計画」セクションの「 [Lync Server 2013 でのメディアのバイパスの計画](lync-server-2013-planning-for-media-bypass.md) 」を参照してください。Lync Server コントロールパネルからメディアのバイパスを無効にすることができます。 Medial バイパスの有効化と構成の詳細については、「 [Lync Server 2013 でネットワークメディアのバイパスを有効にする](lync-server-2013-enabling-network-media-bypass.md)」を参照してください。

<div>

## <a name="to-disable-media-bypass"></a>メディアのバイパスを無効にするには

1.  RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **グローバル**] をクリックします。

4.  [ **グローバル** ] ページで、[ **グローバル** 構成] をクリックします。 構成は常に1つだけであり、常に Global という名前が付いています。

5.  [ **編集** ] メニューの [ **詳細の表示**] をクリックします。

6.  [ **グローバル設定の編集** ] ページで、[ **メディアバイパスを有効にする** ] チェックボックスをオフにします。

7.  [ **コミット** ] をクリックして変更内容を保存します。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でネットワークメディアのバイパスを有効にする](lync-server-2013-enabling-network-media-bypass.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

