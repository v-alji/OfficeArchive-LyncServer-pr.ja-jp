---
title: 'Lync Server 2013: コアデータと設定のバックアップ'
description: 'Lync Server 2013: コアデータと設定をバックアップします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up core data and settings
ms:assetid: 278bc95a-7b8d-4e01-a872-a844830459de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202170(v=OCS.15)
ms:contentKeyID: 51541452
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 637eeb950a3b8380f6e756f46a5083f51b5d7e1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438100"
---
# <a name="backing-up-core-data-and-settings-in-lync-server-2013"></a>Lync Server 2013 でのコアデータと設定のバックアップ

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-04-23_

次の手順では、Lync Server Management Shell コマンドレットを使用して、コアサービスの設定とデータのバックアップファイルを作成します。 このセクションで使用されるツールの詳細については、「 [Lync Server 2013 のバックアップと復元の要件](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md)」を参照してください。ツールと権限。 アーカイブと監視データのバックアップの詳細については、「 [Lync Server 2013 でのアーカイブと監視データベースのバックアップ](lync-server-2013-backing-up-archiving-and-monitoring-databases.md)」を参照してください。

<div>


> [!NOTE]  
> このセクションの中央管理ストアをバックアップする手順には、アーカイブと監視の設定と構成が含まれます。



</div>

このセクションで説明されているコマンドレットは、ローカルまたはリモートで実行できます。

<div>

## <a name="to-back-up-core-data-and-settings"></a>コアデータと設定をバックアップするには

1.  RTCUniversalServerAdmins グループのメンバーであるユーザーアカウントから、社内展開の任意のコンピューターにログオンします。

2.  次の手順で作成したバックアップを保存するには、新しい共有フォルダーを作成し、 **$Backup** によって参照されるパスを新しい共有フォルダーに更新します。

3.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

4.  一元管理ストア構成ファイルをバックアップします。 コマンドラインで、次のように入力します。
    
        Export-CsConfiguration -FileName <path and file name for backup>
    
    次に例を示します。
    
        Export-CsConfiguration -FileName "C:\Config.zip"
    
    <div>
    

    > [!NOTE]  
    > この手順では、Lync サーバーのトポロジ、ポリシー、構成の設定をファイルにエクスポートします。 トポロジデータをバックアップするために、他の手順は必要ありません。

    
    </div>

5.  バックアップされた全体管理ストア構成ファイルを $Backup にコピーし \\ ます。

6.  位置情報サービスのデータをバックアップします。 コマンドラインで、次のように入力します。
    
        Export-CsLisConfiguration -FileName <path and file name for backup>
    
    次に例を示します。
    
        Export-CsLisConfiguration -FileName "C:\E911Config.zip"

7.  バックアップされた場所情報サービス構成ファイルを $Backup にコピーし \\ ます。

8.  フロントエンドプールおよびすべての Standard Edition サーバーの各バックエンドデータベースで、ユーザーデータをバックアップします。 コマンドラインで、次のように入力します。
    
        Export-CsUserData -PoolFQDN <Fqdn> -FileName <String>
    
    次に例を示します。
    
        Export-CsUserData -PoolFQDN "atl-cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserData.zip"

9.  バックアップされたユーザーファイルを $Backup にコピーし \\ ます。

10. 応答グループアプリケーションを実行するすべてのプールで、応答グループの構成をバックアップします。 以下の操作を行います。
    
    1.  コマンドラインで、次のように入力します。
        
            Export-CsRgsConfiguration -Source "service:ApplicationServer:<pool FQDN>" -FileName <path and file name for backup>
        
        例:
        
            Export-CsRgsConfiguration -Source ApplicationServer:pool01.contoso.com -FileName C:\RgsConfiguration.zip

11. バックアップされた応答グループ構成ファイルを $Backup にコピーし \\ ます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

