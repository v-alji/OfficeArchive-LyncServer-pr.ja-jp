---
title: 'Lync Server 2013: グループ通話の集配番号の範囲を削除する'
description: 'Lync Server 2013: グループ通話の集配番号の範囲を削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Group Call Pickup number range
ms:assetid: 521891f3-7a5d-45de-92dc-d57025453159
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945629(v=OCS.15)
ms:contentKeyID: 51541475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b40d423b64d29300741c55433864128897c3ac8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430708"
---
# <a name="delete-a-group-call-pickup-number-range-in-lync-server-2013"></a>Lync Server 2013 でグループ通話の集配番号の範囲を削除する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-01-30_

グループ通話の集配番号の範囲を削除するには、次の手順を使用します。

<div>

## <a name="to-delete-a-call-pickup-group-number-range"></a>通話ピックアップグループの番号範囲を削除するには

1.  Lync Server 管理シェルが RTCUniversalServerAdmins グループのメンバーとして、または「 [Lync server 2013 の委任セットアップの権限](lync-server-2013-delegate-setup-permissions.md)」で説明されているように、必要なユーザー権限を持つコンピューターにログオンします。

2.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

3.  コマンドラインで、次のように入力します。
    
        Remove-CsCallParkOrbit -Identity "<group number range name>" 
    
    例:
    
        Remove-CsCallParkOrbit -Identity "Redmond call pickup"
    
    <div>
    

    > [!NOTE]  
    > その他のオプションの詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>」を参照してください。

    
    </div>

</div>

<div>

## <a name="see-also"></a>関連項目


[通話パークの作成または変更 Lync Server 2013 の範囲の軌道](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[Remove-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[Get-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

