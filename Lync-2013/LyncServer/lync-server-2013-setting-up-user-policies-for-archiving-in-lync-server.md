---
title: 'Lync Server 2013: Lync Server でアーカイブ用のユーザーポリシーを設定する'
description: 'Lync Server 2013: Lync Server でアーカイブ用のユーザーポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up user policies for Archiving in Lync Server
ms:assetid: 22d6cc76-6b5c-4a8c-bb8a-7996450ec085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204742(v=OCS.15)
ms:contentKeyID: 48183626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e33abf6cf16c9c1367162aa8beee91874f4c725
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441628"
---
# <a name="setting-up-user-policies-for-archiving-in-lync-server-2013"></a>Lync Server 2013 でアーカイブ用のユーザーポリシーを設定する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-10_

Lync Server 2013 上にある特定のユーザーに対してアーカイブを有効または無効にするには、1つ以上のユーザーポリシーを作成して構成し、適切なポリシーを特定のユーザーまたはユーザーグループに適用する必要があります。 ユーザーポリシーは、サイトとグローバルポリシーを上書きします。ただし、Lync Server 2013 に所属しているユーザーのみです。

ユーザーは常に Lync Server に置かれています。 Microsoft Exchange の統合が有効になっている場合、メールボックスが Microsoft Exchange Server 2013 にあるユーザーは、Lync Server で管理されているアーカイブポリシーを持っている必要はありません。 アーカイブを使用するユーザーは、Exchange In-Place ホールドによって管理されます。

グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「計画ドキュメント、展開ドキュメント、または操作のドキュメント」の「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」をご覧ください。

<div>


> [!NOTE]  
> 展開に対して Microsoft Exchange の統合を有効にしている場合、exchange 2013 を使っているユーザーに対してアーカイブが有効になっているかどうかが Exchange In-Place ホールドポリシーによって制御されます。 これらのユーザーのアーカイブを使用するには、メールボックスを In-Place 保持する必要があります。 詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。<BR>アーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。 詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でアーカイブ用のユーザーポリシーを作成および構成する](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md)

  - [Lync server 2013 でユーザーに Lync Server のアーカイブポリシーを適用する](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

