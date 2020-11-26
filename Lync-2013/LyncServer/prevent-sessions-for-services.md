---
title: サービスのセッションの禁止
description: サービスのセッションを禁止する。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438464"
---
# <a name="prevent-sessions-for-services"></a>サービスのセッションの禁止

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-04_

Microsoft Lync Server 2010 コントロールパネルを使用すると、特定のコンピューターで実行されているすべての Lync Server 2010 サービスの新しいセッションを禁止したり、特定の Lync Server 2010 サービスの新しいセッションを禁止したりすることができます。

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a>コンピューター上のすべての Lync Server サービスの新しいセッションを禁止するには

1.  RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。

2.  [Lync Server コントロール パネル] を開きます。

3.  左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。

4.  [ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、新しいセッションを禁止するサービスを実行しているコンピューターを検索して、それをクリックします。

5.  [ **アクション**] をクリックします。

6.  [ **すべてのサービスに対して新規セッションを** 許可しない] をクリックします。

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a>特定のサービスの新しいセッションを禁止するには

1.  RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。

2.  [Lync Server コントロール パネル] を開きます。

3.  左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。

4.  [ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。

5.  [ **プロパティ**] をクリックします。

6.  必要に応じてサービスの一覧を並べ替えて、新しいセッションを禁止するサービスをクリックします。

7.  [ **アクション**] をクリックします。

8.  [ **サービスの新規セッションを** 許可しない] をクリックします。

9.  [**閉じる**] をクリックします。

</div>

</div>

<span> </span>

</div>

</div>

</div>

