---
title: ロードを実行するトポロジのプロビジョニング
description: ロードを実行するトポロジのプロビジョニング。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446424"
---
# <a name="provisioning-the-topology-to-run-load"></a>ロードを実行するトポロジのプロビジョニング

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-04_

<div>

Lync Server 2013 の既存の設定と構成によっては、お使いの環境で次の変更を行う必要があります。

1.  Windows PowerShell の実行ポリシーを無制限に設定します。 実行ポリシーの設定を確認するには、Lync Server 管理シェルを開き、次のコマンドを実行します。

    ``` powershell
        Get-ExecutionPolicy
    ```        

    このコマンドを実行しても無制限の値が返されない場合は、次のコマンドを実行します。

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  Lync Server 2013 を効果的に構成するには、次のことを行う必要があります。
    
      - Lync Server 2013 トポロジ (コンピューター名、サービスインスタンス、サイト名、ポリシーなど) について理解している必要があります。
    
      - 応答グループのハントグループ (SIP Uri など) など、グループに作成されたユーザーの一部を割り当てます。

3.  コマンドラインからスクリプトを実行するには、次のように使用します。

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  通常、このパッケージのいずれかのスクリプトが実行されると、スクリプトからの結果のトレースは、スクリプトが呼び出されたときと同じパスのファイルに格納され、 \<scriptname\> $h $ m $s.txt という名前が付けられます。 たとえば、ArchivingPolicy.ps1 を午後12:15 時に実行します。 ArchivingPolicy121500.txt などのログファイルが生成されます。

5.  最後に、サーバーを構成するための例を用意しましたが、ロードの実行が完了した後で構成を変更または削除する責任があります。

</div>

</div>

<span> </span>

</div>

</div>

</div>

