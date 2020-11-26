---
title: 'Lync Server 2013: ギャラリービューを構成する'
description: 'Lync Server 2013: ギャラリービューを構成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Gallery View
ms:assetid: 4a609178-47d8-4682-ac8d-29f882801924
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204871(v=OCS.15)
ms:contentKeyID: 48184069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2aec2f1e3c7bff9a3736f40584a29880978b9daa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433095"
---
# <a name="configuring-gallery-view-in-lync-server-2013"></a><span data-ttu-id="7d2f6-103">Lync Server 2013 でギャラリービューを構成する</span><span class="sxs-lookup"><span data-stu-id="7d2f6-103">Configuring Gallery View in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d2f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d2f6-104">

<span> </span></span></span>

<span data-ttu-id="7d2f6-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="7d2f6-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="7d2f6-106">Lync Server 2013 では、会議ポリシーの [ビデオ会議] を構成します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-106">In Lync Server 2013, you configure Gallery View video conferencing in conferencing policy.</span></span> <span data-ttu-id="7d2f6-107">ギャラリービューは既定でオンになっています。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-107">Gallery View is turned on by default.</span></span> <span data-ttu-id="7d2f6-108">ギャラリービューを許可しない場合、または一部のユーザーのみに許可する場合は、会議ポリシーのこの機能を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-108">If you do not want to allow Gallery View, or want to allow it for only some users, you need to turn off the feature in conferencing policy.</span></span>

<span data-ttu-id="7d2f6-109">会議参加者のビデオが利用できない場合は、Lync Server 2013 の新機能である高解像度の写真を展開すると、ユーザーのギャラリービューエクスペリエンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-109">When a conference participant's video is not available, the users' Gallery View experience can be enhanced if you deploy high-resolution photos, a new feature in Lync Server 2013.</span></span> <span data-ttu-id="7d2f6-110">高解像度の写真は、Active Directory ドメインサービスに保存されている小型の限定された解像度の連絡先写真の代わりとなるものです。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-110">High-resolution photos provide an alternative to the smaller, limited resolution contact photos stored in Active Directory Domain Services.</span></span> <span data-ttu-id="7d2f6-111">高解像度の写真はユーザーの Exchange 2013 メールボックスに保存されるため、Lync Server 2013 を Exchange 2013 と統合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-111">High-resolution photos are stored in a user's Exchange 2013 mailbox, and, therefore, require you to integrate Lync Server 2013 with Exchange 2013.</span></span> <span data-ttu-id="7d2f6-112">詳細については、「NextHop のブログ記事、「Exchange 2013 と Lync Server 2013 の統合」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987) 。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-112">For details, see the NextHop blog article, "Integrating Exchange 2013 and Lync Server 2013," at [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7d2f6-113">各ブログの内容と URL は、将来予告なしに変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-113">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

<span data-ttu-id="7d2f6-114">ギャラリーの表示パラメーターを表示または変更するには、Lync Server 2013 コントロールパネルを使用するか、次のいずれかのコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-114">You can view or modify the Gallery View parameters by using Lync Server 2013 Control Panel or by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="7d2f6-115">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="7d2f6-115">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="7d2f6-116">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="7d2f6-116">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="7d2f6-117">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="7d2f6-117">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="7d2f6-118">以下の会議ポリシー設定を使用して、ギャラリービューを構成します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-118">Configure Gallery View with the following conferencing policy settings:</span></span>

  - <span data-ttu-id="7d2f6-119">**AllowMultiview**   このパラメーターは、ユーザーがギャラリービューのビデオ会議を整理することを許可されているかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-119">**AllowMultiview**   This parameter controls whether a user is allowed to organize Gallery View video conferences.</span></span> <span data-ttu-id="7d2f6-120">このパラメーターは、ユーザーが作成したスケジュールされた会議と臨時の会議に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-120">This parameter applies to scheduled and ad-hoc meetings created by the user.</span></span>
    
    <span data-ttu-id="7d2f6-121">たとえば</span><span class="sxs-lookup"><span data-stu-id="7d2f6-121">Examples:</span></span>
    
      - <span data-ttu-id="7d2f6-122">ユーザー A が Lync Server 2013 プールをホームにしている場合は、このパラメーターを True に設定します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-122">This parameter is set to True for User A, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="7d2f6-123">ユーザーによって開催された会議複数のビデオストリームの参加と受信を可能にします。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-123">Meetings organized by User A enable users to join and receive multiple video streams.</span></span>
    
      - <span data-ttu-id="7d2f6-124">ユーザー B が Lync Server 2013 プールをホームにしている場合は、このパラメーターを False に設定します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-124">This parameter is set to False for User B, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="7d2f6-125">ユーザー B によって開催された会議には、Lync Server 2010 によって提供されるビデオ会議エクスペリエンスに似た1つのビデオストリームがあります。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-125">Meetings organized by User B have a single video stream that is similar to the video conference experience provided by Lync Server 2010.</span></span>
    
    <span data-ttu-id="7d2f6-126">このパラメーターは、複数のビデオストリームを許可する会議を開催できるユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-126">This parameter determines who can organize meetings that allow multiple video streams.</span></span> <span data-ttu-id="7d2f6-127">複数のビデオストリームを許可する会議の参加者は、個別のアクセス許可に基づいて複数のビデオストリームを受信することは許可されない場合があります (EnableMultiviewJoin パラメーターの説明を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-127">Participants in meetings that allow multiple video streams may or may not be allowed to receive multiple video streams, based on their individual permissions (see the description for the EnableMultiviewJoin parameter).</span></span>

  - <span data-ttu-id="7d2f6-128">**EnableMultiviewJoin**   このパラメーターは、会議の参加者が、会議で許可されているギャラリーの表示ビデオエクスペリエンスを受け取るかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-128">**EnableMultiviewJoin**   This parameter controls whether a participant in a meeting receives the Gallery View video experience in meetings that allow it.</span></span> <span data-ttu-id="7d2f6-129">このパラメーターは、ユーザーが参加している会議でのユーザーエクスペリエンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-129">This parameter controls the user's experience in any meeting in which he or she participates.</span></span>
    
    <span data-ttu-id="7d2f6-130">たとえば</span><span class="sxs-lookup"><span data-stu-id="7d2f6-130">Examples:</span></span>
    
      - <span data-ttu-id="7d2f6-131">ユーザー c の場合、このパラメーターは True に設定されます。ユーザー A が開催した会議に参加しているか、ユーザー A によって開始された場合、ユーザー c は複数のビデオストリームを受信できます。ユーザー C は、会議に参加している、またはユーザー B が開始したときに、Lync Server 2010 によって</span><span class="sxs-lookup"><span data-stu-id="7d2f6-131">This parameter is set to True for User C. User C can receive multiple video streams when participating in a meeting organized or started by User A. User C receives a single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in a meeting organized or started by User B.</span></span>
    
      - <span data-ttu-id="7d2f6-132">ユーザー D の場合、このパラメーターは False に設定されます。ユーザー D は、ユーザー A またはユーザー B によって開催された会議に参加しているときに、Lync Server 2010 によって提供されるビデオ会議エクスペリエンスと同様の単一のビデオストリームを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-132">This parameter is set to False for User D. User D receives single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in any meeting organized by User A or User B.</span></span>

<span data-ttu-id="7d2f6-133">次の手順では、Lync Server 管理シェルを使って、ギャラリービューのビデオ会議を有効にする例を示します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-133">The following procedure is an example of using Lync Server Management Shell to enable Gallery View video conferencing.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-gallery-view-video-conferencing"></a><span data-ttu-id="7d2f6-134">ギャラリービューのビデオ会議用の会議ポリシーを変更するには</span><span class="sxs-lookup"><span data-stu-id="7d2f6-134">To modify conferencing policy for Gallery View video conferencing</span></span>

1.  <span data-ttu-id="7d2f6-135">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="7d2f6-136">コマンドラインで、次のコマンドレットを実行して会議ポリシーを編集します。</span><span class="sxs-lookup"><span data-stu-id="7d2f6-136">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -AllowMultiview $true -EnableMultiviewJoin $true 

<span data-ttu-id="7d2f6-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d2f6-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

