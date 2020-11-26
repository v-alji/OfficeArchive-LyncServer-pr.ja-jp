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
# <a name="exporting-archived-data-from-lync-server-2013"></a><span data-ttu-id="44ce2-103">Lync Server 2013 からアーカイブデータをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="44ce2-103">Exporting archived data from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44ce2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44ce2-104">

<span> </span></span></span>

<span data-ttu-id="44ce2-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="44ce2-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="44ce2-106">アーカイブ データベースにアーカイブされているデータは、読み取り可能な形式ではなく、検索もできませんが、Export-CsArchivingData コマンドレットを使用すると、アーカイブ データベースからレコードを抽出して Outlook Electronic Mail (EML) ファイルとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="44ce2-106">Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file.</span></span> <span data-ttu-id="44ce2-107">アーカイブデータのエクスポートの詳細については、操作のドキュメントの「 [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44ce2-107">For details about exporting archived data, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in the Operations documentation.</span></span>

<span data-ttu-id="44ce2-108">Microsoft Exchange の統合を有効にすると、データは Exchange 2013 ストアにアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="44ce2-108">If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores.</span></span> <span data-ttu-id="44ce2-109">Exchange 2013 でアーカイブされたデータは、検索可能で見つけやすくなります。</span><span class="sxs-lookup"><span data-stu-id="44ce2-109">Data archived in Exchange 2013 is searchable and discoverable.</span></span> <span data-ttu-id="44ce2-110">Exchange 2013 および Lync Server 2013 の統合通信のサポートの詳細については、サポートドキュメントの「 [Exchange server および Lync server 2013 の SharePoint 統合のサポート](lync-server-2013-exchange-and-sharepoint-integration-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44ce2-110">For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="44ce2-111">Exchange でアーカイブされたデータへのアクセスについて詳しくは、「Exchange 2013 のドキュメント」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="44ce2-111">For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.</span></span>

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="44ce2-112">Windows PowerShell コマンドレットを使用してアーカイブデータをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="44ce2-112">Exporting Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="44ce2-113">アーカイブデータは、Export-CSArchivingData コマンドレットを使用してエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="44ce2-113">Archiving data can be exported by using the Export-CSArchivingData cmdlet.</span></span> <span data-ttu-id="44ce2-114">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="44ce2-114">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="44ce2-115">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="44ce2-115">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="44ce2-116">**アーカイブデータをエクスポートするには**</span><span class="sxs-lookup"><span data-stu-id="44ce2-116">**To export archiving data**</span></span>

  - <span data-ttu-id="44ce2-117">このコマンドは、2012年6月1日以降にアーカイブデータベース atl-sql-001.litwareinc.com に書き込まれたすべてのアーカイブデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="44ce2-117">This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012.</span></span> <span data-ttu-id="44ce2-118">生成される出力ファイルは、フォルダー C: ArchivingExports に格納され \\ ます。</span><span class="sxs-lookup"><span data-stu-id="44ce2-118">The resulting output file will be stored in the folder C:\\ArchivingExports.</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

<span data-ttu-id="44ce2-119">**1人のユーザーのアーカイブデータをエクスポートするには**</span><span class="sxs-lookup"><span data-stu-id="44ce2-119">**To export archiving data for a single user**</span></span>

  - <span data-ttu-id="44ce2-120">次のコマンドは、1人のユーザーのアーカイブデータをエクスポートします。 kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="44ce2-120">The following command exports archiving data for a single user: kenmyer@litwareinc.com.</span></span> <span data-ttu-id="44ce2-121">こうした処理を行うには、UserUri パラメーターの後にユーザーの SIP アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="44ce2-121">This is done by including the UserUri parameter followed by the user’s SIP address.</span></span> <span data-ttu-id="44ce2-122">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="44ce2-122">For example:</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="44ce2-123">詳細については、 [CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="44ce2-123">For more information, see the help topic for the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="44ce2-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="44ce2-124">See Also</span></span>


[<span data-ttu-id="44ce2-125">Lync Server 2013 の Exchange Server および SharePoint の統合のサポート</span><span class="sxs-lookup"><span data-stu-id="44ce2-125">Exchange Server and SharePoint integration support in Lync Server 2013</span></span>](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[<span data-ttu-id="44ce2-126">エクスポート-CsArchivingData</span><span class="sxs-lookup"><span data-stu-id="44ce2-126">Export-CsArchivingData</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[<span data-ttu-id="44ce2-127">Lync Server 2013 アーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="44ce2-127">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="44ce2-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44ce2-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

