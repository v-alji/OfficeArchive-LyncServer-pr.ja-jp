---
title: 監視サーバー用の SQL Server データベースの削除
description: 監視サーバーの SQL Server データベースを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Monitoring server
ms:assetid: aed5e394-d63e-4ad4-af40-f12d3a044344
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721848(v=OCS.15)
ms:contentKeyID: 49733781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99bf734f0a9978fe14055fb36b01ce37f77e14a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440256"
---
# <a name="remove-the-sql-server-database-for-a-monitoring-server"></a>監視サーバー用の SQL Server データベースの削除

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-04_

Microsoft Lync Server 2010 監視サーバーを削除したら、サーバーデータをホストしている SQL Server データベースを削除できます。 次の手順を使用して、Topology Builder から定義を削除し、データベースサーバーからデータベースとログファイルを削除します。

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a>トポロジビルダーを使用して SQL Server データベースを削除するには

1.  Lync Server 2013 フロントエンドサーバーで、[トポロジビルダー] を開きます。

2.  [トポロジビルダー] で、[ **共有コンポーネント** ] に移動し、[ **sql server ストア**] で、削除または再構成された監視サーバーに関連付けられている sql server インスタンスを右クリックし、[ **削除**] をクリックします。

3.  トポロジを公開し、レプリケーションの状態を確認します。

</div>

<div>

## <a name="to-remove-the-database-files-from-the-sql-server"></a>SQL Server からデータベースファイルを削除するには

1.  SQL Server ベースのサーバー上のデータベースを削除するには、データベースファイルを削除する SQL Server サーバーの SQL Server の [データファイル] グループのメンバーである必要があります。

2.  Lync Server 管理シェルを開きます。

3.  コマンドラインで、次のように入力します。
    
        Uninstall-CsDataBase -DatabaseType Monitoring -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    \<FQDN\>は、データベースサーバーの完全修飾ドメイン名 (FQDN) であり、 \<instance\> オプションの名前付きデータベースインスタンスです。

4.  **CsDataBase** コマンドレットで操作の確認を求めるメッセージが表示されたら、情報を読み、 **Y** キーを押します (または、enter キーを押すか、enter キーを押して続行します)。または、コマンドレットを停止するか (エラーがある場合)、enter キー **を押します**。

</div>

</div>

<span> </span>

</div>

</div>

</div>

