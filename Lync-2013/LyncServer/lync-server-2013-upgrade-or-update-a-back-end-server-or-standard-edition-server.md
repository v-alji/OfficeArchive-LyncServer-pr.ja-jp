---
title: バックエンドサーバーまたは Standard Edition server をアップグレードまたは更新する
description: バックエンドサーバーまたは Standard Edition サーバーをアップグレードまたは更新します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update a Back End Server or Standard Edition server
ms:assetid: f95f8d3a-e039-484e-97bd-d727db21a12b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721942(v=OCS.15)
ms:contentKeyID: 49733879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c529546bdcf88ada6fd82399d3b65b46b4312db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440823"
---
# <a name="upgrade-or-update-a-back-end-server-or-standard-edition-server-in-lync-server-2013"></a>Lync Server 2013 でバックエンドサーバーまたは Standard Edition サーバーをアップグレードまたは更新する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

このトピックでは、Enterprise Edition バックエンドサーバーまたは Standard Edition サーバーに更新プログラムをインストールする方法について説明します。

アップグレード中に少なくとも30分間バックエンドサーバーが停止している場合、ユーザーは回復性モードに移行することがあります。 アップグレードが完了し、バックエンドサーバーがプール内のフロントエンドサーバーに再度接続されると、ユーザーは完全な機能に戻ります。 アップグレードが 30 分未満の場合、ユーザーには影響ありません。

<div>

## <a name="to-update-a-back-end-server-or-standard-edition-server"></a>バックエンド サーバーまたは Standard Edition サーバーを更新するには

1.  アップグレードするサーバーに CsAdministrator の役割のメンバーとしてログオンします。

2.  更新をダウンロードして、ローカル ハードディスクに抽出します。

3.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

4.  Lync Server サービスを停止します。 コマンド ラインで次を入力します。
    
        Stop-CsWindowsService

5.  World Wide Web サービスを停止します。 コマンド ラインで次を入力します。
    
        net stop w3svc

6.  すべての Lync Server 管理シェルウィンドウを閉じます。

7.  更新をインストールします。

8.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

9.  もう一度 Lync Server サービスを停止して、グローバルアセンブリキャッシュ (GAC) – d アセンブリをキャッチします。 コマンド ラインで次を入力します。
    
        Stop-CsWindowsService

10. World Wide Web サービスを再起動します。 コマンド ラインで次を入力します。
    
        net start w3svc

11. 次のいずれかの方法で、LyncServerUpdateInstaller.exe によって行われた変更を SQL Server データベースに適用します。
    
      - Enterprise Edition バックエンドサーバーで、データベースのアーカイブや監視など、このサーバー上に併置されたデータベースがない場合は、コマンドラインで次のように入力します。
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>
    
      - Enterprise Edition バックエンドサーバーで、このサーバーに併置されたデータベースがある場合は、コマンドラインで次のように入力します。
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>  -ExcludeCollocatedStores
    
      - Standard Edition サーバーの場合は、コマンドラインで次のように入力します。
        
            Install-CsDatabase -Update -LocalDatabases

</div>

</div>

<span> </span>

</div>

</div>

</div>

