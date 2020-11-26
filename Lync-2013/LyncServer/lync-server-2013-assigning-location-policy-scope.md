---
title: 'Lync Server 2013: 場所ポリシーのスコープを割り当てる'
description: 'Lync Server 2013: 場所ポリシーのスコープを割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning location policy scope
ms:assetid: e4c66517-c593-4253-b900-7b4dd8bddf2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205360(v=OCS.15)
ms:contentKeyID: 48185734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9f6c46150241b0b224e8005556c0f2f594d8bce5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438303"
---
# <a name="assigning-location-policy-scope-in-lync-server-2013"></a>Lync Server 2013 で位置情報ポリシーのスコープを割り当てる

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-06-06_

他の Lync Server ポリシーと同様に、場所ポリシーは、グローバル、サイト、ユーザーという複数のスコープレベルで割り当てることができます。 ただし、ユーザーレベルの位置情報ポリシーの範囲は、他の Lync Server ポリシーとは少し異なります。 ユーザーごとの場所ポリシーをエンドポイントオブジェクト (ユーザー、一般的なエリア電話の連絡先オブジェクトなど) に適用できるだけでなく、それらを Lync Server ネットワークサイトに適用することもできます。 ネットワーク サイトは、地理的場所に関連付けられたクライアント サブネットをグループ化したものです (ただし、必ずしも中央サイトまたはブランチ サイト全体の中のすべてのサブネットである必要はありません)。 ネットワーク サイト内のサブネットに接続されるクライアントはすべて、そのネットワーク サイトに割り当てられた場所ポリシーを自動的に取得します。 ユーザー レベルの場所ポリシーがユーザーとネットワーク サイトの両方に割り当てられる場合、ネットワーク サイト ベースの場所ポリシーがユーザーごとのポリシー設定より優先されます。

各ネットワーク サイトにはそれぞれに割り当てられた場所ポリシーがあり、各ポリシーには異なる PSTN 使用法、通知 URI、および電話会議 URI の値が割り当てられます。

<div>


> [!NOTE]  
> このようにポリシー スコープが特殊な動作をするのは、ある支店のプールに所属するユーザーが別の支店を訪れていて、緊急電話を発信する場合、ユーザーに割り当てられたプールまたはサイトに関係なく、そのネットワーク サイトに適した E9-1-1 通話ルーティング設定が適用されるようにするためです。



</div>

</div>

<span> </span>

</div>

</div>

</div>

