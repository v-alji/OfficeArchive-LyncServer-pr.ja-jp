---
title: 'Lync Server 2013: アーカイブのためのサイトポリシーを設定する'
description: 'Lync Server 2013: アーカイブ用のサイトポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up site policies for Archiving
ms:assetid: dc2ea206-8b9c-44dd-a479-efb217593c89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205325(v=OCS.15)
ms:contentKeyID: 48185613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27e5b80b7f62ddc18d418415307457c7f2c4010d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441691"
---
# <a name="setting-up-site-policies-for-archiving-in-lync-server-2013"></a>Lync Server 2013 でアーカイブ用のサイトポリシーを設定する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-09_

各サイトのアーカイブポリシーを作成して構成することで、特定のサイトのアーカイブを有効または無効にすることができます。 サイト ポリシーはグローバル ポリシーより優先されますが、サイト ポリシーよりもユーザー ポリシーが優先されます。 アーカイブポリシーが適用されるのは、Microsoft Exchange 統合を使用していない場合、または Microsoft Exchange 統合を使用していないが、Exchange 2013 を使っていないユーザーがいて、メールボックスが In-Place 保留になっている場合のみです。

グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。

<div>


> [!NOTE]  
> 展開時に Microsoft Exchange の統合を有効にすると、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかを制御するための Exchange In-Place ホールドポリシーが適用され、メールボックスは In-Place 保留になります。 詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。<BR>アーカイブ ポリシーで内部または外部の通信のアーカイブを有効にする前に、アーカイブ構成のすべてのオプションを適切に指定してください。 詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site"></a>サイトのアーカイブポリシーを作成するには

1.  CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server 2013 コントロールパネルを開きます。

3.  左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。
    
    グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。

4.  [**新規作成**] をクリックし、[**サイト ポリシー**] をクリックします。

5.  [**サイトの選択**] でポリシーを適用するサイトをクリックします。

6.  [**新しいアーカイブ ポリシー**] で、次の操作を実行します。
    
      - [**名前**] で、サイト ポリシーの名前を指定します。
    
      - [**説明**] にサイト ポリシーに関する情報を入力します (「Redmond のサイト ポリシー」など)。
    
      - 指定したサイトの内部通信のアーカイブを制御するには、[**内部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。
    
      - 指定したサイトの外部通信のアーカイブを制御するには、[**外部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。

7.  [**確定**] をクリックします。

</div>

</div>

<span> </span>

</div>

</div>

</div>

