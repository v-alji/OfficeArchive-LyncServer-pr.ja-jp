---
title: 'Lync Server 2013: プライマリ管理サーバーを構成する'
description: 'Lync Server 2013: プライマリ管理サーバーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the primary management server
ms:assetid: 44e2e9a8-c130-4c66-9871-80b1ff11b27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204844(v=OCS.15)
ms:contentKeyID: 48183986
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43f986f4f03e96cafa27dfdd302bb98a00d8b2ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400035"
---
# <a name="configuring-the-primary-management-server-in-lync-server-2013"></a>Lync Server 2013 でのプライマリ管理サーバーの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-03-19_

Microsoft Lync Server 2013 に含まれている新しい正常性監視機能を最大限に活用するためには、まず、プライマリ管理サーバーとして動作するようにコンピューターを指定する必要があります。そのコンピューターで、System Center Operations Manager 2007 R2 または System Center Operations Manager 2012 をインストールする必要があります。 さらに、サポートされているバージョンの SQL Server を、Operations Manager バックエンドデータベースとして機能するようにインストールする必要があります。 System Center Operations Manager 2012 を使用している場合は、次のいずれかのバージョンの SQL Server をバックエンドデータベースとして使用できます。

  - SQL Server 2008 R2 Service Pack 1

  - SQL Server 2008 R2 Service Pack 2

System Center Operations Manager 2007 R2 を使用している場合は、SQL Server 2005 Service Pack 4 または SQL Server 2008 Service Pack 3 をインストールすることをお勧めします。 また、System Center Operations Manager 2007 R2 のバックエンドデータベースとして SQL Server 2008 R2 を使用することもできます。 SQL Server 2008 R2 を System Center Operations Manager 2007 R2 と連携するように構成する方法については、このドキュメントの「付録1」を参照してください。

System Center Operations Manager 2012 または System Center Operations Manager 2007 R2 をインストールするには、次のような製品のすべてのコンポーネントをインストールする必要があります。

  - オペレーション データベース

  - サーバー

  - コンソール

  - Windows PowerShell コマンドレット

  - Web コンソール

  - レポート

  - データ ウェアハウス

このドキュメントでは、これらのコンポーネントとそのインストールについて詳しくは説明しません。 System Center Operations Manager 2007 R2 の詳細については、「Operations Manager 2007 R2 のドキュメント」 <https://go.microsoft.com/fwlink/p/?linkid=257526> および System Center Operations manager 2012 のドキュメントを参照してください <https://go.microsoft.com/fwlink/p/?linkid=257527> 。 SQL Server 2005 または SQL Server 2008 Service Pack 1 をバックエンドデータベースとして使用する場合は、これらの手順に従う必要があります。

System Center Operations Manager 2012 を使用している場合は、バックエンドデータベースとして SQL Server 2012 を使用できます。 SQL Server 2012 の詳細については、「SQL Server 2012 のオンラインブック」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528) 。

Lync Server の展開ごとに1つのプライマリ管理サーバーしか設定できないことに注意してください。 また、System Center Operations Manager 2012 または System Center Operations Manager 2007 R2 のいずれかを使用できますが、2つのアプリケーションを同時に実行することはできません。どちらか一方を選ぶ必要があります。 たとえば、System Center Operations Manager 2012 を実行している場合、System Center エージェントも System Center Operations Manager 2012 を実行している必要があります。 System Center Operations Manager 2012 と System Center Operations Manager 2007 R2 を実行しているエージェントの一部を実行することはできません。

</div>

<span> </span>

</div>

</div>

</div>

