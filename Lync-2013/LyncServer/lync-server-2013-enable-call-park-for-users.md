---
title: 'Lync Server 2013: ユーザーのコールパークを有効にする'
description: 'Lync Server 2013: ユーザーに対してコールパークを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Call Park for users
ms:assetid: 9430763f-3394-467c-9c6d-426bf761604e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398753(v=OCS.15)
ms:contentKeyID: 48184814
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7f9ab23b9fa71943efafd588b8c57a2af781b08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428938"
---
# <a name="enable-call-park-for-users-in-lync-server-2013"></a><span data-ttu-id="f2533-103">Lync Server 2013 のユーザーに対してコールパークを有効にする</span><span class="sxs-lookup"><span data-stu-id="f2533-103">Enable Call Park for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2533-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2533-104">

<span> </span></span></span>

<span data-ttu-id="f2533-105">_**最終更新日:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="f2533-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="f2533-106">ユーザーは、音声ポリシーでのコールパークが有効になるまで、通話をパークしたり、保留中の通話を取得したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f2533-106">Users cannot park calls or retrieve parked calls until they are enabled for Call Park in voice policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f2533-107">既定では、すべてのユーザーに対して [コールパーク] が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="f2533-107">By default, Call Park is disabled for all users.</span></span>



</div>

<span data-ttu-id="f2533-108">グローバルスコープまたはサイトのスコープまたはユーザーの範囲で、通話パークを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f2533-108">You can enable Call Park at the global scope, or at the site scope or user scope.</span></span> <span data-ttu-id="f2533-109">ユーザー スコープはサイト スコープより優先され、サイト スコープはグローバル スコープよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="f2533-109">User scope takes precedence over site scope, and site scope takes precedence over global scope.</span></span> <span data-ttu-id="f2533-110">複数のボイスポリシーがある場合は、グローバルポリシーだけでなく、すべてのポリシーを確認してコールパークを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f2533-110">If you have multiple voice policies, review all the policies to enable Call Park, not just the global policy.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-enable-call-park-for-users"></a><span data-ttu-id="f2533-111">Lync Server コントロールパネルを使用してユーザーのコールパークを有効にするには</span><span class="sxs-lookup"><span data-stu-id="f2533-111">To Use Lync Server Control Panel to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="f2533-112">**RTCUniversalServerAdmins** グループのメンバーとしてコンピューターにログオンするか、**CsVoiceAdministrator**、**CsServerAdministrator**、または **CsAdministrator** 管理者役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f2533-112">Log on to the computer as a member of the **RTCUniversalServerAdmins** group, or as a member of the **CsVoiceAdministrator**, **CsServerAdministrator**, or **CsAdministrator** administrative role.</span></span>

2.  <span data-ttu-id="f2533-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2533-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f2533-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f2533-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f2533-115">左側のナビゲーション バーで [**音声ルーティング**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2533-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="f2533-116">[**音声ポリシー**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2533-116">Click the **Voice Policy** tab.</span></span>

5.  <span data-ttu-id="f2533-117">既存の音声ポリシーをダブルクリックして、[**音声ポリシーの編集**] ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2533-117">Double-click an existing voice policy to open the **Edit Voice Policy** dialog box.</span></span>

6.  <span data-ttu-id="f2533-118">[**通話機能**] の [**コール パークを有効にする**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2533-118">Under **Calling features**, select **Enable call park**.</span></span>

7.  <span data-ttu-id="f2533-119">[**OK**] をクリックして音声ポリシーを保存します。</span><span class="sxs-lookup"><span data-stu-id="f2533-119">Click **OK** to save the voice policy</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-enable-call-park-for-users"></a><span data-ttu-id="f2533-120">コマンドレットを使用してユーザーのコールパークを有効にするには</span><span class="sxs-lookup"><span data-stu-id="f2533-120">To Use Cmdlets to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="f2533-121">RTCUniversalServerAdmins グループのメンバーとしてコンピューターにログオンするか、CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator 管理者役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f2533-121">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator administrative role.</span></span>

2.  <span data-ttu-id="f2533-122">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2533-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f2533-123">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="f2533-123">Run:</span></span>
    
        Set-CsVoicePolicy -Identity <VoicePolicy> -EnableCallPark $true
    
    <span data-ttu-id="f2533-124">たとえば、既定のグローバルボイスポリシーのコールパークを有効にするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="f2533-124">For example, to enable Call Park for the default global voice policy:</span></span>
    
        Set-CsVoicePolicy -EnableCallPark $true

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f2533-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2533-125">See Also</span></span>


[<span data-ttu-id="f2533-126">Lync Server 2013 で音声ポリシーを作成し、PSTN 使用状況レコードを構成する</span><span class="sxs-lookup"><span data-stu-id="f2533-126">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
  

<span data-ttu-id="f2533-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2533-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

