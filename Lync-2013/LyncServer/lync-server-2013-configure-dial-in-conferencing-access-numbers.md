---
title: 'Lync Server 2013: ダイヤルイン会議アクセス番号の構成'
description: 'Lync Server 2013: ダイヤルイン会議アクセス番号を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing access numbers
ms:assetid: d8a18030-f318-43dd-834d-70e5014b5e8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398952(v=OCS.15)
ms:contentKeyID: 48185623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0edb3492c243b36b69c4b48df8c22adc4ece7999
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399932"
---
# <a name="configure-dial-in-conferencing-access-numbers-in-lync-server-2013"></a><span data-ttu-id="9e44f-103">Lync Server 2013 でのダイヤルイン会議アクセス番号の構成</span><span class="sxs-lookup"><span data-stu-id="9e44f-103">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e44f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e44f-104">

<span> </span></span></span>

<span data-ttu-id="9e44f-105">_**最終更新日:** 2011-07-17_</span><span class="sxs-lookup"><span data-stu-id="9e44f-105">_**Topic Last Modified:** 2011-07-17_</span></span>

<span data-ttu-id="9e44f-106">ダイヤルイン会議を展開するときには、ユーザーが公衆交換電話網 (PSTN) からダイヤルして電話会議のオーディオ部分に参加するための電話番号を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e44f-106">When you deploy dial-in conferencing, you need to set up phone numbers that users can dial from the public switched telephone network (PSTN) to join the audio portion of conferences.</span></span> <span data-ttu-id="9e44f-107">それらのダイヤルイン アクセス番号は、ミーティングの招待状と [ダイヤルイン会議の設定] Web ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e44f-107">These dial-in access numbers appear in meeting invitations and on the Dial-in Conferencing Settings webpage.</span></span>

<span data-ttu-id="9e44f-108">ダイヤルイン アクセス番号を作成する前に、まずダイヤルイン会議の域を計画し、その地域のダイヤル プランを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e44f-108">Before you can create dial-in access numbers, you must first plan your dial-in conferencing regions and then configure dial plans with the regions.</span></span> <span data-ttu-id="9e44f-109">地域の詳細については、計画ドキュメントの「 [Lync Server 2013 でのダイヤルイン会議の要件](lync-server-2013-dial-in-conferencing-requirements.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e44f-109">For details about regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span> <span data-ttu-id="9e44f-110">ダイヤルイン会議のダイヤルプランの設定の詳細については、「 [Lync Server 2013 でダイヤルイン会議のダイヤルプランを構成する](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e44f-110">For details about configuring dial plans for dial-in conferencing, see [Configure dial plans for dial-in conferencing in Lync Server 2013](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9e44f-111">このアクセス番号の Active Directory ドメインサービス (AD &nbsp; DS) のレプリケーションが完了するまで、新しいダイヤルインアクセス番号を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="9e44f-111">You cannot use a new dial-in access number until Active Directory Domain Services (AD&nbsp;DS) replication of that access number is complete.</span></span> <span data-ttu-id="9e44f-112">レプリケーションが完了するまでに数時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="9e44f-112">Replication can take several hours to complete.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="9e44f-113">ダイヤルイン アクセス番号を作成した後は、Active Directory の連絡先オブジェクトの表示名を変更し、ユーザーが正しいアクセス番号を識別しやすくすることができます。</span><span class="sxs-lookup"><span data-stu-id="9e44f-113">After you create dial-in access numbers, you can modify the display name for the Active Directory contact objects so that users can more easily identify the correct access number.</span></span> <span data-ttu-id="9e44f-114">表示名を変更するには、 <STRONG>CsDialInConferencingAccessNumber</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e44f-114">Use the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet to modify the display name.</span></span> <span data-ttu-id="9e44f-115">Active Directory のオブジェクトは手動で変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="9e44f-115">You should not modify Active Directory objects manually.</span></span> <span data-ttu-id="9e44f-116">アクセス番号の変更について詳しくは、「 <STRONG>CsDialInConferencingAccessNumber</STRONG> コマンドレットの Lync Server 管理シェルドキュメント」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9e44f-116">For details about modifying an access number, see Lync Server Management Shell documentation for the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9e44f-117">このセクション中</span><span class="sxs-lookup"><span data-stu-id="9e44f-117">In This Section</span></span>

[<span data-ttu-id="9e44f-118">Lync Server 2013 でのダイヤルイン会議アクセス番号の作成または変更</span><span class="sxs-lookup"><span data-stu-id="9e44f-118">Create or modify a dial-in conferencing access number in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-dial-in-conferencing-access-number.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9e44f-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e44f-119">See Also</span></span>


[<span data-ttu-id="9e44f-120">Lync Server 2013 でのダイヤルイン会議の要件</span><span class="sxs-lookup"><span data-stu-id="9e44f-120">Dial-in conferencing requirements in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-requirements.md)  


[<span data-ttu-id="9e44f-121">Lync Server 2013 でのダイヤルイン会議のダイヤル プランの構成</span><span class="sxs-lookup"><span data-stu-id="9e44f-121">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)  
  

<span data-ttu-id="9e44f-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e44f-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

