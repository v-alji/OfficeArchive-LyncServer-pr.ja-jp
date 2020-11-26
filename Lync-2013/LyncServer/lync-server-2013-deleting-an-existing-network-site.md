---
title: 'Lync Server 2013: 既存のネットワークサイトを削除する'
description: 'Lync Server 2013: 既存のネットワークサイトを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an existing network site
ms:assetid: 2762149b-3572-4513-b838-beda7fa9e81e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688001(v=OCS.15)
ms:contentKeyID: 49733589
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7cef4774ee71aaf6851757d5b88d30138fc34997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430358"
---
# <a name="deleting-an-existing-network-site-in-lync-server-2013"></a>Lync Server 2013 で既存のネットワークサイトを削除する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

[ネットワークサイト] は、通話受付制御 (CAC) または拡張9-1-1 展開の各領域内に構成されているオフィスまたは場所です。 Lync Server 2013 コントロールパネルを使用して、サイトを構成し、それらを地域と関連付けることができます。 たとえば、北米向けのネットワーク領域は、シカゴ、Redmond、バンクーバーなどのネットワークサイトに関連付けられている場合があります。 サイト内のすべてのサイトに対して、CAC ネットワークサイトを作成する必要があります。このサイトには帯域幅の制限がありません。 Lync Server コントロールパネルからネットワークサイトの作成、変更、削除を行うことができます。 既存のネットワークサイトを削除するには、次の手順を使用します。 ネットワークサイトの作成または変更の詳細については、「 [Lync Server 2013 でネットワークサイトを作成または変更する](lync-server-2013-creating-or-modifying-network-sites.md)」を参照してください。

<div>

## <a name="to-delete-a-network-site"></a>ネットワークサイトを削除するには

1.  RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **サイト**] をクリックします。

4.  [ **サイト** ] ページで、削除するサイトをクリックします。
    
    <div>
    

    > [!NOTE]  
    > 一度に複数のサイトを削除できます。 この操作を行うには、ctrl キーを押しながら複数のサイトを選び、CTRL キーを押しながら選択します。 または、すべてのサイトを選択するには、[<STRONG>編集</STRONG>] メニューの [<STRONG>すべて選択</STRONG>] をクリックします。

    
    </div>

5.  [ **編集** ] メニューの [ **削除**] をクリックします。

6.  **[OK]** をクリックします。
    
    <div>
    

    > [!WARNING]  
    > ネットワークサイトがネットワークサブネットに関連付けられている場合は、そのサイトを削除することはできません。 サブネットに関連付けられているサイトを削除しようとすると、エラーメッセージが表示されます。 サイトがいずれかのサブネットに関連付けられているかどうかを確認するには、サイトをクリックし、[<STRONG>編集</STRONG>] メニューの [<STRONG>詳細の表示</STRONG>] をクリックします。

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

