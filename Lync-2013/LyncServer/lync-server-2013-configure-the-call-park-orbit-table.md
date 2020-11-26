---
title: 'Lync Server 2013: コール パーク オービット テーブルの構成'
description: 'Lync Server 2013: コールパークの軌道テーブルを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433634"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a>Lync Server 2013 でのコール パーク オービット テーブルの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-10_

コールパークでは、orbits を使用してパーキング通話を行います。 ユーザーが通話をパークして取得するには、その前に、コールパークの軌道テーブルを構成する必要があります。 組織がパーキング通話のために予約する内線番号 (orbits) の範囲を指定し、各範囲に対してどのコールパークプールを処理するかを指定する必要があります。 軌道の範囲を定義する場合は、1つの軌道がすぐに再利用されることがないように、1つの orbits を使用することをお勧めします。ただし、ユーザーまたは他のサービスで使用可能な拡張機能の数を制限する orbits はあまり多くありません。 コールパークアプリケーションが展開されている Lync サーバープールごとに、複数のコールパークの範囲を作成できます。 各 Call パーク範囲には、グローバルに一意の名前と一連の固有の拡張子を指定する必要があります。

<div>


> [!IMPORTANT]  
> 一般的にオービット範囲には 100 未満のオービットが含まれます。1 つの範囲の上限は 10,000 オービットです。1 つのプールに含まれるオービットの数は 50,000 未満です。範囲が小さすぎると、オービットが再び使用されるまでの時間が短くなります。



</div>

オービット範囲には、仮想内線番号ブロック (ユーザーまたは電話機が割り当てられていない内線番号) を使用します。

<div>


> [!NOTE]  
> コールパークの軌道テーブルでは、内側の市内ダイヤル (DID) 番号を軌道番号として割り当てることはできません。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

[通話パークの作成または変更 Lync Server 2013 の範囲の軌道](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

