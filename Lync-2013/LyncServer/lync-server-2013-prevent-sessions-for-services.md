---
title: 'Lync Server 2013: サービスのセッションを禁止する'
description: 'Lync Server 2013: サービスのセッションを禁止する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436903"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a>Lync Server 2013 でサービスのセッションを禁止する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

Lync Server コントロールパネルを使用すると、特定のコンピューターで実行されているすべての Lync Server 2013 サービスの新しいセッションを禁止したり、特定の Lync Server 2013 サービスの新しいセッションを禁止したりすることができます。

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a>コンピューター上のすべての Lync Server サービスの新しいセッションを禁止するには

1.  RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。

4.  [ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、新しいセッションを禁止するサービスを実行しているコンピューターを検索して、それをクリックします。

5.  [ **アクション**] をクリックします。

6.  [ **すべてのサービスに対して新規セッションを** 許可しない] をクリックします。

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a>特定のサービスの新しいセッションを禁止するには

1.  RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。

4.  [ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。

5.  [ **プロパティ**] をクリックします。

6.  必要に応じてサービスの一覧を並べ替えて、新しいセッションを禁止するサービスをクリックします。

7.  [ **アクション**] をクリックします。

8.  [ **サービスの新規セッションを** 許可しない] をクリックします。

9.  [**閉じる**] をクリックします。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 トポロジの管理](lync-server-2013-managing-the-lync-server-topology.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

