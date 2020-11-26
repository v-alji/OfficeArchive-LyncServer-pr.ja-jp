---
title: 'Lync Server 2013: デバイスに関連付けられていないデバイス更新ファイルを削除する'
description: 'Lync Server 2013: デバイスに関連付けられていないデバイス更新ファイルを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Device Update files not associated with a device
ms:assetid: ecebbf73-b456-4990-a91d-308b84d39404
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994084(v=OCS.15)
ms:contentKeyID: 51803996
ms.date: 12/12/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8338f7274d1d27e2290d822324986238f4856fe4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436406"
---
# <a name="remove-device-update-files-not-associated-with-a-device-in-lync-server-2013"></a>Lync Server 2013 でデバイスに関連付けられていないデバイス更新ファイルを削除する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-20_

新しいデバイス更新プログラムがシステムにアップロードされるたびに、対応するデバイス更新ルールが作成されます。 既定では、これらの新しいデバイス更新ルールは保留状態に割り当てられます。 つまり、テストデバイスにはルールをダウンロードしてインストールすることができますが、ユーザーが更新プログラムを使用できるようになる前にテストをテストすることができます。 テストに基づいて、更新プログラムを承諾して展開するか、または元に戻して削除します。 更新プログラムを拒否すると、デバイス更新プログラムのデバイス更新ルールとの関連付けが解除されます。

<div>


デバイスに関連付けられていないデバイス更新ファイルは、Windows PowerShell と **空の Deviceupdatefile** コマンドレットを使用して削除できます。 このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。

<div>


> [!NOTE]  
> リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。



</div>

<div>


  - たとえば、次のコマンドを実行すると、デバイスに関連付けられていない Web サーバー atl-cs-001.litwareinc.com 上のデバイス更新ルールがすべて削除されます。
    
        Clear-CsDeviceUpdateFile -Identity "service:WebServer:atl-cs-001.litwareinc.com"

</div>

詳細については、「 [CsDeviceUpdateFile](https://docs.microsoft.com/powershell/module/skype/Clear-CsDeviceUpdateFile) コマンドレット」のヘルプトピックを参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

