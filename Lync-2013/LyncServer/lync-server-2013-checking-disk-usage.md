---
title: 'Lync Server 2013: ディスク使用量のチェック'
description: 'Lync Server 2013: ディスク使用量を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking disk usage
ms:assetid: 0f0cb9bf-3f11-43ff-be10-5c8e1b5c4f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720908(v=OCS.15)
ms:contentKeyID: 63969578
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7eddde772d156f0a416dab381efe1ab33ee202f9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434992"
---
# <a name="checking-disk-usage-in-lync-server-2013"></a><span data-ttu-id="61d39-103">Lync Server 2013 でディスク使用量を確認する</span><span class="sxs-lookup"><span data-stu-id="61d39-103">Checking disk usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61d39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61d39-104">

<span> </span></span></span>

<span data-ttu-id="61d39-105">_**最終更新日:** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="61d39-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="61d39-106">ハードディスクドライブは、Lync Server 2013 展開の重要なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="61d39-106">Hard disks drives are an important component of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="61d39-107">十分な空きディスク容量がなくても、オペレーティングシステムと Lync Server 2013 データベースは正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="61d39-107">Without sufficient free disk volume, neither the operating system nor the Lync Server 2013 databases can function correctly.</span></span> <span data-ttu-id="61d39-108">サーバーのディスク領域が不足しないことを確認し、必要に応じてストレージリソースを追加するための準備として、Lync Server 2013 バックエンドデータベースの統計情報を毎日監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61d39-108">You must monitor the Lync Server 2013 back-end database statistics daily to help to make sure that servers do not run out of disk space, and to prepare to add storage resources as required.</span></span>

<span data-ttu-id="61d39-109">オペレーティングシステム、プログラムファイル、データベース、トランザクションログ (Lync Server 2013 Back End) をホストしているディスクの空き領域を確認する以外に、次の重要なデータを含むファイル共有のディスク領域を含むファイルシステムの使用状況を監視する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="61d39-109">Apart from checking space on disks hosting the operating system, program files, database, and transaction logs (Lync Server 2013 Back End), you should also monitor usage of the file system that includes disk space for file shares that contain the following important data:</span></span>

  - <span data-ttu-id="61d39-110">会議コンテンツ</span><span class="sxs-lookup"><span data-stu-id="61d39-110">Meeting content</span></span>

  - <span data-ttu-id="61d39-111">会議コンテンツのメタデータ</span><span class="sxs-lookup"><span data-stu-id="61d39-111">Meeting content metadata</span></span>

  - <span data-ttu-id="61d39-112">会議のコンプライアンスログ</span><span class="sxs-lookup"><span data-stu-id="61d39-112">Meeting compliance logs</span></span>

  - <span data-ttu-id="61d39-113">アプリケーションデータファイル (アプリケーションサーバーコンポーネントによって内部的に使用されます)</span><span class="sxs-lookup"><span data-stu-id="61d39-113">Application data files (used internally by the application server component)</span></span>

  - <span data-ttu-id="61d39-114">グループチャットサーバー web サービスとコンプライアンスフォルダ (グループチャット web サービスにアップロードされたファイルを保存する)</span><span class="sxs-lookup"><span data-stu-id="61d39-114">Group Chat Server web service and compliance folders (to store files uploaded to the Group Chat web service)</span></span>

  - <span data-ttu-id="61d39-115">グループチャットのコンプライアンス XML ファイル (グループチャットのコンプライアンスレコードが含まれています)</span><span class="sxs-lookup"><span data-stu-id="61d39-115">Group Chat compliance XML files (that contain Group Chat compliance records)</span></span>

  - <span data-ttu-id="61d39-116">ファイルを更新する (デバイス更新サービスの場合)</span><span class="sxs-lookup"><span data-stu-id="61d39-116">Update files (for Device Update Service)</span></span>

  - <span data-ttu-id="61d39-117">アドレス帳ファイル</span><span class="sxs-lookup"><span data-stu-id="61d39-117">Address Book files</span></span>

<span data-ttu-id="61d39-118">Lync Server 2013 には、以前に一覧表示されているファイル共有のファイルに加えて、データベースとトランザクションログを保存するためのハードディスク領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="61d39-118">Lync Server 2013 needs hard disk space to store its databases and transaction logs in addition to files on file shares previously listed.</span></span>

<span data-ttu-id="61d39-119">記憶域リソースが不足しているため、Lync Server 2013 の展開に悪影響がないことを確認するために、ディスク領域を定期的に監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61d39-119">You should monitor the disk space regularly to help to make sure that the Lync Server 2013 deployment is not adversely affected because of insufficient storage resources.</span></span>

<span data-ttu-id="61d39-120">Lync Server 2013 の各ボリュームで利用可能なディスク領域に関する統計情報を比較して維持し、データベースおよびトランザクションログファイルの増加量を求めます。</span><span class="sxs-lookup"><span data-stu-id="61d39-120">Compare and maintain statistical information about available disk space on each Lync Server 2013 volume and expected growth of the databases and transaction log files.</span></span> <span data-ttu-id="61d39-121">これは、記憶域リソースが必要なときに容量の計画や記憶域の追加を行うのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="61d39-121">This helps with capacity planning and adding storage when the storage resources are required.</span></span>

<span data-ttu-id="61d39-122">トラブルシューティングと障害回復の状況に対応するために、使用可能な空きボリューム領域は、データベースのサイズの110% 以上にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="61d39-122">To accommodate troubleshooting and disaster recovery situations, we recommend that available free volume space be equal or greater than 110 percent of the size of database.</span></span>

<span data-ttu-id="61d39-123">次の方法を使用して、空きディスク領域を確認できます。</span><span class="sxs-lookup"><span data-stu-id="61d39-123">You can check free disk space by using the following methods:</span></span>

1.  <span data-ttu-id="61d39-124">**System Center Operations Manager**   System Center Operations Manager を使用すると、ボリュームスペースに制約がある場合に管理者に警告を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="61d39-124">**System Center Operations Manager**   System Center Operations Manager can be used to warn administrators when volume space is constrained.</span></span>

2.  <span data-ttu-id="61d39-125">**スクリプトを実行する**   使用可能なハードディスク領域が20% を下回った場合にメッセージを送信するスクリプトを実行して、ディスク領域を監視します。</span><span class="sxs-lookup"><span data-stu-id="61d39-125">**Running a script**   Monitor disk space by running a script that sends you a message if the available hard disk space falls below 20 percent.</span></span> <span data-ttu-id="61d39-126">TechNet の Microsoft Script Center でサンプルスクリプトを参照してください。次の点を確認してください。 [https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard%20disk%20alert\&f%5B0%5D.Value=hard%20disk%20alert\&f%5B0%5D.Type=SearchText\&ac=5](https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard+disk+alert%26f%5b0%5d.value=hard+disk+alert%26f%5b0%5d.type=searchtext%26ac=5)</span><span class="sxs-lookup"><span data-stu-id="61d39-126">You can find a sample script on Microsoft Script Center on TechNet, examine: [https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard%20disk%20alert\&f%5B0%5D.Value=hard%20disk%20alert\&f%5B0%5D.Type=SearchText\&ac=5](https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard+disk+alert%26f%5b0%5d.value=hard+disk+alert%26f%5b0%5d.type=searchtext%26ac=5)</span></span>

3.  <span data-ttu-id="61d39-127">**Windows エクスプローラー**   Windows エクスプローラーを使用して、Lync Server 2013 ログとデータベースが保存されているボリュームのディスク領域を確認します。</span><span class="sxs-lookup"><span data-stu-id="61d39-127">**Windows Explorer**   Use Windows Explorer to check for disk space on volumes that store Lync Server 2013 logs and databases.</span></span>

<span data-ttu-id="61d39-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61d39-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

