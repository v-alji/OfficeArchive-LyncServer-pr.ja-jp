---
title: 'Lync Server 2013: 応答グループキューを削除する'
description: 'Lync Server 2013: 応答グループキューを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Response Group queue
ms:assetid: 67c7a489-8c5f-4c6b-9387-9d4c11d43695
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521008(v=OCS.15)
ms:contentKeyID: 48184356
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76b00257a12b872615ebc124abff595268b120e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430687"
---
# <a name="delete-a-response-group-queue-in-lync-server-2013"></a>Lync Server 2013 で応答グループキューを削除する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

キューを削除するには、次のいずれかの手順を使用します。

<div>

## <a name="to-use-lync-server-control-panel-to-delete-a-queue"></a>Lync Server コントロールパネルを使用してキューを削除するには

1.  RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーション バーで [**応答グループ**] をクリックし、[**キュー**] をクリックします。

4.  検索フィールドに、削除するキューの名前の一部またはすべてを入力します。

5.  キューの一覧で、目的のキューをクリックし、[ **編集**] をクリックして、[ **削除**] をクリックします。

6.  **[OK]** をクリックします。

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-queue"></a>Windows PowerShell を使用してキューを削除するには

1.  RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。

2.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

3.  コマンド ラインで、次のコマンドを実行します。
    
        Get-CsRgsQueue -Identity <Application Server service> -Name "<name of queue>" | Remove-CsRgsQueue
    
    例:
    
        Get-CsRgsQueue -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsQueue

</div>

</div>

<span> </span>

</div>

</div>

</div>

