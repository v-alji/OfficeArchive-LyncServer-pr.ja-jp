---
title: LyncPerfTool の実行
description: LyncPerfTool を実行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run LyncPerfTool
ms:assetid: f2fd1940-d744-47b5-b299-04a914039182
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945612(v=OCS.15)
ms:contentKeyID: 51541437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3278754c9154f47602c5c4f1fa95cdc4b465b228
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446407"
---
# <a name="run-lyncperftool"></a>LyncPerfTool の実行

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-24_

Lync Server 2013 応力とパフォーマンスツール (LyncPerfTool.exe) を実行する前に、ユーザー、連絡先、シナリオを作成する必要があります。 これらの操作を実行するためのツールの使用について詳しくは、「 [ユーザーと連絡先を作成](create-users-and-contacts.md) して、 [ユーザープロファイルを構成](configure-user-profile.md)する」をご覧ください。 これらのツールを実行すると、必要なパラメーターが含まれるバッチファイルの一部として LyncPerfTool.exe 実行されるファイルも生成されます。

<div>

## <a name="running-the-lync-server-2013-stress-and-performance-tool"></a>Lync Server 2013 のストレスとパフォーマンスのツールを実行する

UserProfileGenerator.exe ツールは、LyncPerfTool のパフォーマンスカウンターを登録し、XML 構成ファイルを読み込むことによって LyncPerfTool.exe を実行できるバッチファイルを作成します。 このバッチ ファイルでは、構成ファイルごとに LyncPerfTool.exe の 1 つのインスタンスを実行します。 バッチファイルを実行するには、次の操作を行います。

1.  構成フォルダーとファイルを含むフォルダーを、各クライアントコンピューター上の LyncStressTool.exe が含まれているディレクトリにコピーします。 (たとえば、1.28 13.16.16 という名前のフォルダーで構成ファイルを生成した場合は、 \_ 各クライアントの LyncPerfTool.exe が含まれているフォルダーにそのフォルダーをコピーします)。

2.  適切に番号付けされたクライアントフォルダーに移動し、RunClient バッチスクリプトを実行します。 Windows エクスプローラーでバッチファイルをダブルクリックするだけで、そのクライアント番号のすべての構成ファイルが実行されます。 次の構文を使用して、適切なクライアントフォルダーからスクリプトを実行することもできます。

    ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
    ```
LyncPerfTool.exe を直接実行するには、コマンドプロンプトを開き、コマンドラインで次のコマンドを入力します (初めて実行する場合は、この :LyncPerfTool.exe トピックの後半のメモに示すように、パフォーマンスカウンター regsvr32/i/n/s LyncPerfToolPerf.dll を登録してください。\<configXML\>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml
```
このツールで構成ファイルの値を表示するには、次のように、前のコマンドに「/displayfile」パラメーターを含めます。
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml /displayfile
```
プロセスを終了するには、Ctrl キーを押しながら C キーを押します。

<div>


> [!NOTE]  
> LyncPerfTool を直接実行する前に、パフォーマンスカウンターを登録する必要があります。 パフォーマンスカウンターを登録するには、次のコマンドを入力します。



</div>

```Powershell
    regsvr32 /i /n /s LyncPerfToolPerf.dll
```
<div>


> [!NOTE]  
> 開始する LyncPerfTool.exe のすべてのインスタンスは、通常、ユーザーが1秒あたり1人のユーザーとの間に、すぐにユーザーのサインインを開始します。 プールに対するユーザー サインインの最大レートは、毎秒約 12 ユーザーになります。 これは、ユーザーがまだサインインしている間に、12個を超える LyncPerfTool インスタンスを同時に開始しないことを意味します。 1000ユーザーは、1秒あたり最大20分でサインインすることになります。



</div>

</div>

<div>

## <a name="see-also"></a>関連項目


[ユーザーと連絡先の作成](create-users-and-contacts.md)  
[ユーザー プロファイルの構成](configure-user-profile.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

