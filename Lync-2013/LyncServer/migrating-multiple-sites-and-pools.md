---
title: 複数のサイトとプールの移行
description: 複数のサイトとプールを移行する。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating multiple sites and pools
ms:assetid: a6d726d2-564d-4b39-a97c-5656a673292a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205165(v=OCS.15)
ms:contentKeyID: 48185079
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7efaa6f038286ff9138e631f23da88bb445e20f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440375"
---
# <a name="migrating-multiple-sites-and-pools"></a>複数のサイトとプールの移行

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-17_

Lync Server 2013 は、複数サイトと複数プールの展開をサポートしています。 複数のプールを Lync Server 2010 から Lync Server 2013 に移行するには、次の点を考慮する必要があります。

1.  Lync Server 2013 パイロットプールを展開した後、Lync Server 2013 プールに移動されるパイロットユーザーのサブセットと、ユーザーの機能を検証するための方法を定義する必要があります。 たとえば、パイロットプールにユーザーを移動した後、ユーザーの会議ポリシーが Lync Server 2013 に移動されたことを確認します。

2.  パイロットプールにエッジサーバーを展開した後、外部ユーザーが Lync Server 2013 プールと通信できることを検証する必要があります。

3.  Lync Server 2010 エッジサーバーからのフェデレーションルートを試験的な Lync Server 2013 エッジサーバーに移行した後、フェデレーションされたユーザーが Lync Server 2013 プールと通信できることを検証する必要があります。

4.  すべてのユーザーと非ユーザーの連絡先オブジェクトを移動した後、Lync Server 2010 プールが空であることを確認する必要があります。

5.  Lync Server 2010 プールが空であることを確認した後、プールを非アクティブ化することができます。
    
    従来の Lync Server 2010 プールとサーバーを非アクティブ化する方法について詳しくは、「 [フェーズ 8: レガシプールの廃止](phase-8-decommission-legacy-pools.md)」をご覧ください。

</div>

<span> </span>

</div>

</div>

</div>

