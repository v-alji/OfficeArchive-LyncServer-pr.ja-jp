---
title: 'Lync Server 2013: ダイヤル プランに地域が割り当てられていることの確認'
description: 'Lync Server 2013: ダイヤルプランに地域が割り当てられていることを確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426152"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="cd0fd-103">「ダイヤルプラン Lync Server 2013 に地域が割り当てられていることを確認する」</span><span class="sxs-lookup"><span data-stu-id="cd0fd-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd0fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd0fd-104">

<span> </span></span></span>

<span data-ttu-id="cd0fd-105">_**最終更新日:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="cd0fd-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="cd0fd-106">ダイヤルイン会議に使用するダイヤルプランには、ダイヤルイン会議アクセス番号と適切なダイヤルプランを関連付けるために、 **ダイヤルイン会議領域** が指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="cd0fd-107">ダイヤル プランをセットアップするときに、そのダイヤル プランに適用されるダイヤルイン会議の地域を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="cd0fd-108">次に、ダイヤルインアクセス番号を作成するときに、アクセス番号を適切なダイヤルプランに関連付ける地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="cd0fd-109">すべてのダイヤルプランの地域を指定することが重要であるため、この手順を使用して、すべてのダイヤルプランに地域が設定されていることを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="cd0fd-110">この手順は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-110">This step is optional.</span></span>

<span data-ttu-id="cd0fd-111">**Get-CsDialPlan** コマンドレットを使用して、地域がすべてのダイヤルイン会議ダイヤルプランに設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="cd0fd-112">ダイヤル プランに地域がない場合は、**Set-CsDialPlan** コマンドレットを使用して地域を設定できます。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="cd0fd-113">Lync Server コントロールパネルを使用して、既存のダイヤルプランの領域を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="cd0fd-114">Lync Server コントロールパネルの使用について詳しくは、「 [Lync server 2013 でダイヤルプランを変更](lync-server-2013-modify-a-dial-plan.md)する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="cd0fd-115">ダイヤル プランで地域プロパティが設定されているかどうかを確認するには</span><span class="sxs-lookup"><span data-stu-id="cd0fd-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="cd0fd-116">RTCUniversalServerAdmins グループのメンバーか、**Cs-VoiceAdministrator**、**Cs-ServerAdministrator**、または **CsAdministrator** の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="cd0fd-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="cd0fd-118">コマンド プロンプトで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="cd0fd-119">例:</span><span class="sxs-lookup"><span data-stu-id="cd0fd-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="cd0fd-120">この例では、組織で構成されているすべてのダイヤル プランが戻されます。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="cd0fd-121">戻されたダイヤル プランを確認して、ダイヤルイン会議の地域が含まれていないものを識別します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="cd0fd-122">詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="cd0fd-123">ダイヤル プランの地域プロパティを設定するには</span><span class="sxs-lookup"><span data-stu-id="cd0fd-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="cd0fd-124">RTCUniversalServerAdmins グループのメンバーか、**Cs-VoiceAdministrator**、**Cs-ServerAdministrator**、または **CsAdministrator** の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="cd0fd-125">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="cd0fd-126">ダイヤルイン会議の地域が含まれていないダイヤル プランで、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="cd0fd-127">例:</span><span class="sxs-lookup"><span data-stu-id="cd0fd-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="cd0fd-128">この例では、Redmond という Identity を持つダイヤル プランを変更して、DialinConferencingRegion プロパティを "US West Coast" に設定します。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="cd0fd-129">詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd0fd-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="cd0fd-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd0fd-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

