---
title: 'Lync Server 2013: Standard Edition サーバーの復元'
description: 'Lync Server 2013: Standard Edition サーバーを復元します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Standard Edition server
ms:assetid: d1845663-3138-4fd6-b3e7-337e294d40d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202190(v=OCS.15)
ms:contentKeyID: 51541519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2cd6976324492e0539c47999f78434e1a82706
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436224"
---
# <a name="restoring-a-standard-edition-server-in-lync-server-2013"></a>Lync Server 2013 での Standard Edition サーバーの復元

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

中央管理ストアをホストしていない Standard Edition サーバーで問題が発生した場合は、このセクションの手順に従ってください。 サーバーの全体管理ストアでエラーが発生した場合は、「 [Lync server 2013 で中央管理ストアをホストしているサーバーの復元](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)」を参照してください。

<div>


> [!TIP]  
> 復元を開始する前に、システムのイメージコピーを取得することをお勧めします。 復元中に問題が発生した場合に備えて、この画像をロールバックポイントとして使うことができます。 オペレーティングシステムと SQL Server をインストールした後に画像のコピーを取得し、証明書を復元または再登録することができます。



</div>

<div>

## <a name="to-restore-a-standard-edition-server"></a>Standard Edition サーバーを復元するには

1.  障害のあるコンピューターと同じ完全修飾ドメイン名 (FQDN) を持つクリーンで、または新しいサーバーから始め、オペレーティングシステムをインストールして、証明書を復元または reenroll します。
    
    <div>
    

    > [!NOTE]  
    > 組織のサーバー展開手順に従って、この手順を実行します。

    
    </div>

2.  RTCUniversalServerAdmins グループとローカルの管理者グループのメンバーであるユーザーアカウントから、復元しているサーバーにログオンします。

3.  適切なファイルストアを $Backup からサーバー上のファイルストアの場所にコピーして、ファイルストアを復元し、フォルダーを共有します。
    
    <div>
    

    > [!IMPORTANT]  
    > 復元されたファイルストアのパスとファイル名は、ファイルを使用するコンポーネントがアクセスできるように、バックアップされたファイルストアとまったく同じである必要があります。

    
    </div>

4.  トポロジビルダーを実行します。
    
    1.  トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。
    
    2.  [ **既存の展開からトポロジをダウンロード**] をクリックし、[ **OK**] をクリックします。
    
    3.  トポロジを選択し、[ **保存**] をクリックします。 選択内容を確認するには、[ **はい]** をクリックします。

5.  Lync Server のインストールフォルダーまたはメディアを参照して、setup amd64Setup.exe にある Lync Server 展開ウィザードを起動し \\ \\ \\ ます。 Lync Server 展開ウィザードを使用して、次の操作を行います。
    
    1.  **手順 1: ローカル構成ストアをインストール** して、ローカル構成ファイルをインストールします。
    
    2.  **手順 2: lync server のコンポーネントをセットアップまたは削除** して lync server サーバーの役割をインストールする
    
    3.  手順 3: 証明書を割り当てるために **証明書を要求、インストール、または割り当て** ます。
    
    4.  **手順 4: サービスを開始** して、サーバー上のサービスを開始します。
    
    展開ウィザードの実行の詳細については、復元するサーバーの役割の展開ドキュメントを参照してください。

6.  ユーザーデータを復元するには、次の操作を行います。
    
    1.  $Backup から \\ ローカルディレクトリに ExportedUserData.zip をコピーします。
    
    2.  ユーザーデータを復元する前に、Lync サービスを停止する必要があります。 そのためには、次のように入力します。
        
            Stop-CsWindowsService
    
    3.  ユーザーデータを復元するには、コマンドラインで次のように入力します。
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        次に例を示します。
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  次のように入力して Lync サービスを再起動します。
        
            Start-CsWindowsService

7.  この Standard Edition サーバーで応答グループを展開した場合は、応答グループの構成データを復元します。 詳細については、「 [Lync Server 2013 での応答グループの設定の復元](lync-server-2013-restoring-response-group-settings.md)」を参照してください。

8.  この Standard Edition サーバーに常設チャットを展開した場合は、常設チャットデータベース (行う) を復元します。
    
    SQL Server バックアップを使って常設チャットデータベースをバックアップした場合は、SQL Server の復元手順を使用して復元します。
    
    Export-CsPersistentChatData コマンドレットを使用してバックアップを作成した場合は、Import-CsPersistentChatData を使って復元します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

