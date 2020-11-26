---
title: 'Lync Server 2013: ネットワークサイト情報の表示'
description: 'Lync Server 2013: ネットワークサイトの情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440403"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a>Lync Server 2013 でのネットワークサイト情報の表示

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-23_

[ネットワークサイト] は、通話受付制御 (CAC) または拡張9-1-1 展開の各領域内に構成されているオフィスまたは場所です。 ネットワークサイトの情報は、Lync Server 2013 コントロールパネルまたは Lync Server 管理シェルで確認できます。 ネットワークサイトの作成または変更の詳細については、「 [Lync Server 2013 でネットワークサイトを作成または変更する](lync-server-2013-creating-or-modifying-network-sites.md)」を参照してください。

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a>Lync Server コントロールパネルでネットワークサイト情報を表示するには

1.  RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **サイト**] をクリックします。

4.  [ **サイト** ] ページで、表示するサイトをクリックします。
    
    <div>
    

    > [!NOTE]  
    > 一度に1つのサイトの情報のみを表示できます。

    
    </div>

5.  [**編集**] メニューの [**詳細の表示**] をクリックします。

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a>Windows PowerShell コマンドレットを使用したネットワークサイト情報の表示

Windows PowerShell と Get-CsNetworkSite コマンドレットを使用して、ネットワークサイトの情報を表示できます。 このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。 リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。

<div>

## <a name="to-view-network-site-information"></a>ネットワークサイトの情報を表示するには

  - すべてのネットワークサイトに関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。
    
        Get-CsNetworkSite
    
    次のような情報が表示されます。
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

詳細については、「 [CsNetworkSite site](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) 」コマンドレットのヘルプトピックを参照してください。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でのネットワークサイトの作成または変更](lync-server-2013-creating-or-modifying-network-sites.md)  
[Lync Server 2013 で既存のネットワークサイトを削除する](lync-server-2013-deleting-an-existing-network-site.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

