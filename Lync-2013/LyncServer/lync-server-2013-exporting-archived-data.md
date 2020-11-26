---
title: 'Lync Server 2013: アーカイブデータのエクスポート'
description: 'Lync Server 2013: アーカイブデータをエクスポートしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 656751f1a2d03b50f0c938a8501ba3e95e304cff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428336"
---
# <a name="exporting-archived-data-from-lync-server-2013"></a>Lync Server 2013 からアーカイブデータをエクスポートする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-23_

アーカイブ データベースにアーカイブされているデータは、読み取り可能な形式ではなく、検索もできませんが、Export-CsArchivingData コマンドレットを使用すると、アーカイブ データベースからレコードを抽出して Outlook Electronic Mail (EML) ファイルとして保存できます。 アーカイブデータのエクスポートの詳細については、操作のドキュメントの「 [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) 」を参照してください。

Microsoft Exchange の統合を有効にすると、データは Exchange 2013 ストアにアーカイブされます。 Exchange 2013 でアーカイブされたデータは、検索可能で見つけやすくなります。 Exchange 2013 および Lync Server 2013 の統合通信のサポートの詳細については、サポートドキュメントの「 [Exchange server および Lync server 2013 の SharePoint 統合のサポート](lync-server-2013-exchange-and-sharepoint-integration-support.md) 」を参照してください。 Exchange でアーカイブされたデータへのアクセスについて詳しくは、「Exchange 2013 のドキュメント」をご覧ください。

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a>Windows PowerShell コマンドレットを使用してアーカイブデータをエクスポートする

アーカイブデータは、Export-CSArchivingData コマンドレットを使用してエクスポートできます。 このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。 リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。

**アーカイブデータをエクスポートするには**

  - このコマンドは、2012年6月1日以降にアーカイブデータベース atl-sql-001.litwareinc.com に書き込まれたすべてのアーカイブデータをエクスポートします。 生成される出力ファイルは、フォルダー C: ArchivingExports に格納され \\ ます。
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

**1人のユーザーのアーカイブデータをエクスポートするには**

  - 次のコマンドは、1人のユーザーのアーカイブデータをエクスポートします。 kenmyer@litwareinc.com こうした処理を行うには、UserUri パラメーターの後にユーザーの SIP アドレスを指定します。 次に例を示します。
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

詳細については、 [CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) コマンドレットのヘルプトピックを参照してください。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の Exchange Server および SharePoint の統合のサポート](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[エクスポート-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[Lync Server 2013 アーカイブの管理](lync-server-2013-managing-archiving.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

