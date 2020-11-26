---
title: 'Lync Server 2013: ユーザーのアーカイブポリシーを設定する'
description: 'Lync Server 2013: ユーザーのアーカイブポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Archiving policies for users
ms:assetid: 1bbb45df-0590-4c66-9d65-d25526f57790
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204722(v=OCS.15)
ms:contentKeyID: 48183549
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c18a15c1a0611f49a6fd9a4983f3ce87104332e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444764"
---
# <a name="setting-up-archiving-policies-for-users-in-lync-server-2013"></a>Lync Server 2013 でユーザーのアーカイブポリシーを設定する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-09_

特定のユーザーのアーカイブを有効または無効にするには、ユーザーのアーカイブポリシーを作成して構成し、そのポリシーを特定のユーザーまたはユーザーグループに適用します。 ユーザー ポリシーは、グローバル ポリシーやサイト ポリシーより優先されます。 アーカイブポリシーが適用されるのは、Microsoft Exchange 統合を使用していない場合、または Microsoft Exchange 統合を使用していないが、Exchange 2013 を使っていないユーザーがいて、メールボックスが In-Place 保留になっている場合のみです。

グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。

<div>


> [!NOTE]  
> 展開時に Microsoft Exchange の統合を有効にすると、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかを制御するための Exchange In-Place ホールドポリシーが適用され、メールボックスは In-Place 保留になります。 詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。<BR>アーカイブ ポリシーで内部または外部の通信のアーカイブを有効にする前に、アーカイブ構成のすべてのオプションを適切に指定してください。 詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でアーカイブ用のユーザーポリシーを設定する](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md)

  - [Exchange Server との統合を使用するときに、Lync Server 2013 でアーカイブするためのポリシーを設定する](lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

