---
title: 'Lync Server 2013: 障害復旧時のアナウンスの管理'
description: 'Lync Server 2013: 障害回復時にお知らせを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage announcements during disaster recovery
ms:assetid: c33e51ea-421f-42d2-826b-b73968f6bd5b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721874(v=OCS.15)
ms:contentKeyID: 49733807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d85dfcd15c9c3650bafafa6fa7702e19ac9c4f7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426124"
---
# <a name="manage-announcements-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="f1148-103">Lync Server 2013 での障害復旧時のアナウンスの管理</span><span class="sxs-lookup"><span data-stu-id="f1148-103">Manage announcements during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1148-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1148-104">

<span> </span></span></span>

<span data-ttu-id="f1148-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f1148-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f1148-106">Lync Server 2013 は、停止中に、未割り当ての電話番号への通話に対するお知らせをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f1148-106">Lync Server 2013 supports announcements for calls to unassigned numbers during outages.</span></span> <span data-ttu-id="f1148-107">停止中のアナウンスメント機能の復元は任意です。</span><span class="sxs-lookup"><span data-stu-id="f1148-107">Restoring announcement functionality during an outage is optional.</span></span> <span data-ttu-id="f1148-108">停止中にお知らせを復元する場合は、バックアッププールでアナウンスメントの構成を再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1148-108">If you choose to restore announcements during an outage, you need recreate your announcement configuration in the backup pool.</span></span> <span data-ttu-id="f1148-109">このセクションでは、障害回復中にお知らせを復元する場合に必要な操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="f1148-109">This section describes what you need to do if you choose to restore announcements during disaster recovery.</span></span>

<span data-ttu-id="f1148-110">このセクションは、アナウンスメントアプリケーションを使用する未割り当ての番号範囲に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f1148-110">This section applies to unassigned number ranges that use the Announcement application.</span></span> <span data-ttu-id="f1148-111">このセクションは、Exchange ユニファイドメッセージング (UM) 自動応答を使用する未使用の番号範囲には適用されません。</span><span class="sxs-lookup"><span data-stu-id="f1148-111">This section does not apply to unassigned number ranges that use Exchange Unified Messaging (UM) Auto Attendant.</span></span>

<div>

## <a name="before-an-outage"></a><span data-ttu-id="f1148-112">停止前</span><span class="sxs-lookup"><span data-stu-id="f1148-112">Before an Outage</span></span>

<span data-ttu-id="f1148-113">システム停止中にお知らせを使用するかどうかに関係なく、アナウンスメントアプリケーション用に構成したカスタマイズされたオーディオファイルのバックアップを個別に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1148-113">Regardless of whether you choose to use announcements during outages, you should take separate backups of any customized audio files that you configured for the Announcement application.</span></span> <span data-ttu-id="f1148-114">カスタマイズされたお知らせは、Lync Server の障害回復プロセスの一部としてはバックアップされません。</span><span class="sxs-lookup"><span data-stu-id="f1148-114">Customized announcements are not backed up as part of the Lync Server disaster recovery process.</span></span> <span data-ttu-id="f1148-115">ファイルのバックアップを個別に行わず、サーバーやプールにアップロードしたファイルが破損している、破損している、または消去された場合、ファイルは失われます。</span><span class="sxs-lookup"><span data-stu-id="f1148-115">If you do not take separate backups of the files and the files that you uploaded to the server or pool are damaged, corrupted, or erased, the files will be lost.</span></span>

<span data-ttu-id="f1148-116">カスタマイズしたオーディオファイルのバックアップコピーを持っておらず、元のオーディオファイルを使用できない場合は、最初にファイルをインポートしたサーバーまたはプールのファイルストアで、アナウンスメントアプリケーション用に構成したオーディオファイルを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f1148-116">If you do not have backup copies of customized audio files, and the original audio files are no longer available, you can find the audio files that you configured for an Announcement application by looking in the File Store for the server or pool where you originally imported the files.</span></span> <span data-ttu-id="f1148-117">アナウンスメントアプリケーション用に設定したすべてのオーディオファイルを、ファイルストアからコピーできます。</span><span class="sxs-lookup"><span data-stu-id="f1148-117">You can copy all the audio files that you configured for the Announcement application from the File Store.</span></span>

<span data-ttu-id="f1148-118">**ファイルストアからオーディオファイルをコピーするには**</span><span class="sxs-lookup"><span data-stu-id="f1148-118">**To copy audio files from the file store**</span></span>

1.  <span data-ttu-id="f1148-119">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1148-119">At the command line, run:</span></span>
    
        Xcopy <Source: Pool Announcement Service File Store path> <Destination>
    
    <span data-ttu-id="f1148-120">例:</span><span class="sxs-lookup"><span data-stu-id="f1148-120">For example:</span></span>
    
        Xcopy "<Pool File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS" "<Destination: Backup location>"
    
    <span data-ttu-id="f1148-121">ここで、ApplicationServer-X はプールのアプリケーションサーバーのサービス ID を示します (たとえば、1-ApplicationServer-1)。</span><span class="sxs-lookup"><span data-stu-id="f1148-121">Where X-ApplicationServer-X refers to the service ID of the Application Server of the pool (for example, 1-ApplicationServer-1")</span></span>


</div>

<div>

## <a name="during-an-outage"></a><span data-ttu-id="f1148-122">停止中</span><span class="sxs-lookup"><span data-stu-id="f1148-122">During an Outage</span></span>

<span data-ttu-id="f1148-123">このセクションで説明されているタスクを実行することにより、アプリの停止中にお知らせの設定を再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1148-123">To use the Announcement application during an outage, you need to recreate the announcement configuration in the backup pool by performing the tasks described in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f1148-124">バックアッププールにフェールオーバーした後、これらのタスクを実行することをお勧めします。これは、手順2を実行するとすぐに、割り当てられていない番号範囲の所有権を取得するためです。</span><span class="sxs-lookup"><span data-stu-id="f1148-124">We recommend that you perform these tasks after you fail over to the backup pool, because as soon as you perform step 2, the backup pool takes ownership of the unassigned number ranges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="f1148-125">Exchange UM 自動応答の電話番号を使用する番号の範囲については、以下の手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f1148-125">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="f1148-126">**バックアッププールでお知らせの構成を再作成するには**</span><span class="sxs-lookup"><span data-stu-id="f1148-126">**To recreate the announcement configuration in the backup pool**</span></span>

1.  <span data-ttu-id="f1148-127">バックアッププールのプライマリプールに展開したお知らせを再作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1148-127">Recreate the announcements that you deployed in the primary pool in the backup pool by doing the following:</span></span>
    
    1.  <span data-ttu-id="f1148-128">**インポート-CsAnnouncementFile** コマンドレットを使用して、プライマリプールで使用されているすべてのオーディオファイルをバックアッププールにインポートし、親パラメーターのバックアッププールを指定します。</span><span class="sxs-lookup"><span data-stu-id="f1148-128">Import any audio files used in the primary pool to the backup pool by using the **Import-CsAnnouncementFile** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    2.  <span data-ttu-id="f1148-129">**新しい-csannouncement** コマンドレットを使用し、親パラメーターのバックアッププールを指定して、各アナウンスを再作成します。</span><span class="sxs-lookup"><span data-stu-id="f1148-129">Recreate each announcement by using the **New-CsAnnouncement** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1148-130">これらのパラメーターを使用してバックアッププールでお知らせを作成する方法の詳細については、「 <A href="lync-server-2013-create-an-announcement.md">Lync Server 2013 でお知らせを作成</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1148-130">For details about using these parameters to create announcements in the backup pool, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="f1148-131">すべてのアナウンスをバックアッププールに再作成したら、プライマリプールのお知らせを使用する、割り当てられていないすべての番号範囲をバックアッププール内の再作成したアナウンスにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="f1148-131">After all announcements are recreated in the backup pool, redirect all the unassigned number ranges that use announcements in the primary pool to the recreated announcements in the backup pool.</span></span>
    
    <span data-ttu-id="f1148-132">割り当てられていない番号の範囲ごとに、プライマリプールでお知らせを使用するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1148-132">For each unassigned number range that uses an announcement in the primary pool, run the following:</span></span>
    
        Set-CsUnassignedNumber -Identity "<name of number range>" -AnnouncementService "<FQDN of backup pool>" -AnnouncementName "<announcement name in backup pool>"

</div>

<div>

## <a name="after-the-outage"></a><span data-ttu-id="f1148-133">停止後</span><span class="sxs-lookup"><span data-stu-id="f1148-133">After the Outage</span></span>

<span data-ttu-id="f1148-134">プライマリプールが利用可能になったら、停止するために変更した未使用の番号範囲をプライマリプールに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1148-134">When the primary pool becomes available, you need to redirect the unassigned number ranges that you changed for the outage back to the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f1148-135">Exchange UM 自動応答の電話番号を使用する番号の範囲については、以下の手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f1148-135">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="f1148-136">**プライマリプールのアナウンスを復元するには**</span><span class="sxs-lookup"><span data-stu-id="f1148-136">**To restore announcements in the primary pool**</span></span>

1.  <span data-ttu-id="f1148-137">回復中にプライマリプールを再構築する必要がある場合は、親パラメーターのプライマリプールを指定することを除き、オーディオファイルをインポートして、バックアッププールの場合と同様に、お知らせを作成して、プライマリプールでアナウンスを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1148-137">If you had to rebuild the primary pool during the recovery, you need to recreate the announcements in the primary pool by importing the audio files and creating announcements, just as you did in the backup pool, except that you specify the primary pool for the Parent parameter.</span></span> <span data-ttu-id="f1148-138">詳細については、このトピックの前の「停止中」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1148-138">For details, see "During an Outage" earlier in this topic.</span></span>

2.  <span data-ttu-id="f1148-139">停止のために変更した未使用の番号の範囲ごとに、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1148-139">For each unassigned number range that you changed for the outage, run the following:</span></span>
    
        Set-CsUnassignedNumber [-Identity "<name of number range>"] -AnnouncementService "<FQDN of primary pool>" -AnnouncementName "<announcement name in primary pool>"

3.  <span data-ttu-id="f1148-140">必要に応じて、バックアッププールで再作成したお知らせを削除します。</span><span class="sxs-lookup"><span data-stu-id="f1148-140">Optionally, remove the announcements that you recreated in the backup pool.</span></span> <span data-ttu-id="f1148-141">バックアッププールのアナウンスメントアプリケーションのお知らせリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f1148-141">Get a list of announcements for the backup pool Announcement application.</span></span> <span data-ttu-id="f1148-142">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1148-142">At the command line, run:</span></span>
    
        Get-CsAnnouncement -Identity "<Service:service ID>"
    
    <span data-ttu-id="f1148-143">例:</span><span class="sxs-lookup"><span data-stu-id="f1148-143">For example:</span></span>
    
        Get-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com
    
    <span data-ttu-id="f1148-144">結果の一覧で、削除するお知らせを見つけて、Guid をコピーします。</span><span class="sxs-lookup"><span data-stu-id="f1148-144">In the resulting list, locate the announcements you want to remove and copy the GUIDs.</span></span> <span data-ttu-id="f1148-145">削除するお知らせごとに、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1148-145">For each announcement you want to remove, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>"
    
    <span data-ttu-id="f1148-146">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f1148-146">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"


<span data-ttu-id="f1148-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1148-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

