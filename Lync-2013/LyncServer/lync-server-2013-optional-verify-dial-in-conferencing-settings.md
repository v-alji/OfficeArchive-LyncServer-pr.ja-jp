---
title: 'Lync Server 2013: (オプション) ダイヤルイン会議の設定の検証'
description: 'Lync Server 2013: (オプション) ダイヤルイン会議の設定を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify dial-in conferencing settings
ms:assetid: a85efdda-97b0-4f3b-bd26-04416bee8ef5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412789(v=OCS.15)
ms:contentKeyID: 48185027
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec002cfbd7cdd67498768a360143f88ab4f8e1b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445205"
---
# <a name="optional-verify-dial-in-conferencing-settings-in-lync-server-2013"></a><span data-ttu-id="ce3b1-103">(オプション) Lync Server 2013 でのダイヤルイン会議の設定の検証</span><span class="sxs-lookup"><span data-stu-id="ce3b1-103">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce3b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce3b1-104">

<span> </span></span></span>

<span data-ttu-id="ce3b1-105">_**最終更新日:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="ce3b1-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="ce3b1-106">ダイヤルイン会議構成の最後の確認作業として、どのアクセス番号も使用しないダイヤルイン会議の地域があるダイヤル プランやダイヤルイン会議の地域が指定されていないアクセス番号を検索します。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-106">As final verification of your dial-in conferencing configuration, you can search for dial plans that have a dial-in conferencing region that is not used by any access number and for access numbers that have not specified a dial-in conferencing region.</span></span> <span data-ttu-id="ce3b1-107">この手順は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-107">This step is optional.</span></span>

<div>

## <a name="to-find-dial-plans-with-a-dial-in-conferencing-region-that-is-not-used-by-an-access-number"></a><span data-ttu-id="ce3b1-108">アクセス番号で使用されていないダイヤルイン会議領域でダイヤルプランを検索するには</span><span class="sxs-lookup"><span data-stu-id="ce3b1-108">To find dial plans with a dial-in conferencing region that is not used by an access number</span></span>

1.  <span data-ttu-id="ce3b1-109">RTCUniversalServerAdmins グループのメンバーとして、または **Cs-serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="ce3b1-110">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ce3b1-111">コマンド プロンプトで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-111">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingAccessNumber -EmptyRegion
    
    <span data-ttu-id="ce3b1-112">このコマンドレットは、どのアクセス番号も使用していないダイヤルイン会議の地域がある、すべてのダイヤル プランを返します。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-112">This cmdlet returns all of the dial plans that have a dial-in conferencing region that is not used by an access number.</span></span>

</div>

<div>

## <a name="to-find-access-numbers-without-assigned-regions"></a><span data-ttu-id="ce3b1-113">割り当てられている地域のないアクセス番号を検索するには</span><span class="sxs-lookup"><span data-stu-id="ce3b1-113">To find access numbers without assigned regions</span></span>

1.  <span data-ttu-id="ce3b1-114">RTCUniversalServerAdmins グループのメンバーとして、または **Cs-serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-114">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="ce3b1-115">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ce3b1-116">コマンド プロンプトで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-116">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingAccessNumber -Region NULL
    
    <span data-ttu-id="ce3b1-117">このコマンドレットは、地域に関連付けられていないダイヤルイン会議アクセス番号をすべて返します。</span><span class="sxs-lookup"><span data-stu-id="ce3b1-117">This cmdlet returns all the dial-in conferencing access numbers that are not associated with a region.</span></span>

<span data-ttu-id="ce3b1-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce3b1-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

