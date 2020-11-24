---
title: 'Lync Server 2013: コールパークを作成または変更する範囲'
description: 'Lync Server 2013: コールパークの範囲を作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a Call Park orbit range
ms:assetid: 549ec118-eee5-4333-9416-80929ec057e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398361(v=OCS.15)
ms:contentKeyID: 48184142
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3889f30264593bedcffb54811dd5bd844f48f0cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399357"
---
# <a name="create-or-modify-a-call-park-orbit-range-in-lync-server-2013"></a><span data-ttu-id="96936-103">通話パークの作成または変更 Lync Server 2013 の範囲の軌道</span><span class="sxs-lookup"><span data-stu-id="96936-103">Create or modify a Call Park orbit range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96936-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96936-104">

<span> </span></span></span>

<span data-ttu-id="96936-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="96936-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="96936-106">コール パーク オービットの範囲を作成または変更するには、次のいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="96936-106">Use one of the following procedures to create or modify a call park orbit range.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-create-or-modify-a-range-of-numbers-for-parking-calls"></a><span data-ttu-id="96936-107">Lync Server コントロールパネルを使用して、パーキング通話の番号の範囲を作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="96936-107">To use Lync Server Control Panel to create or modify a range of numbers for parking calls</span></span>

1.  <span data-ttu-id="96936-108">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="96936-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="96936-109">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96936-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="96936-110">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="96936-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="96936-111">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="96936-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="96936-112">左側のナビゲーション バーで [**音声機能**] をクリックし、[**コール パーク**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96936-112">In the left navigation bar, click **Voice Features** and then click **Call Park**.</span></span>

4.  <span data-ttu-id="96936-113">[**コール パーク**] ページで、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="96936-113">On the **Call Park** page, do one of the following:</span></span>
    
      - <span data-ttu-id="96936-p103">新しいオービット範囲を作成するには、[**新規作成**] をクリックします。[**名前**] に、この番号範囲の識別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="96936-p103">To create a new orbit range, click **New**. In **Name**, type an identifying name for this range of numbers.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="96936-116">オービット範囲をデータベースにコミットした後に、この名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="96936-116">After you commit the orbit range to the database, you cannot change this name.</span></span>

        
        </div>
    
      - <span data-ttu-id="96936-p104">既存のオービット範囲を変更するには、検索フィールドにそのオービット範囲の名前または名前の一部を入力します。オービットの検索結果の一覧で、目的のオービットをクリックし、[**編集**] をクリックして、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96936-p104">To modify an existing orbit range, type all or part of the name of the orbit range in the search field. In the resulting list of orbits, click the orbit you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="96936-119">最初の [**番号範囲**] フィールドに、このコール パーク オービットの内線番号の範囲の開始番号を入力し、2 番目の [**番号範囲**] フィールドに、範囲の終了番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="96936-119">In the first **Number range** field, type the beginning number of the range of extensions for this call park orbit, and in the second **Number range** field, type the ending number of the range.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="96936-120">範囲の開始番号が終了番号より大きくならないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="96936-120">The beginning number of the range must be less than or equal to the ending number of the range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="96936-121">範囲の開始番号の値は、範囲の終了番号と同じ長さである必要があります。</span><span class="sxs-lookup"><span data-stu-id="96936-121">The value of the beginning number of the range must be the same length as the ending number of the range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="96936-p105">オービット範囲は一意である必要があります。この範囲が他のどの範囲とも重ならないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="96936-p105">The orbit range must be unique. This range cannot overlap with any other range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="96936-124">オービット範囲が、文字 \* または # で始まる場合、範囲は 100 を超える必要があります。</span><span class="sxs-lookup"><span data-stu-id="96936-124">If the orbit range begins with the character \* or #, the range must be greater than 100.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="96936-125">有効な値: 正規表現の文字列と一致する必要があります ([ \* | #]? [1 ~ 9] \d {0,7} ) |([1-9] \d {0,8} )</span><span class="sxs-lookup"><span data-stu-id="96936-125">Valid values: Must match the regular expression string ([\*|#]?[1-9]\d{0,7})|([1-9]\d{0,8}).</span></span> <span data-ttu-id="96936-126">つまり、値には \* または # の文字あるいは 1 ～ 9 の数字で始まる文字列を指定する必要があります (最初の文字を 0 にすることはできません)。</span><span class="sxs-lookup"><span data-stu-id="96936-126">This means the value must be a string beginning with either the character \* or # or a number 1 through 9 (the first character cannot be a zero).</span></span> <span data-ttu-id="96936-127">最初の文字が \* または # である場合、次の文字には 1 ～ 9 の数字 (0 は不可) を指定します。</span><span class="sxs-lookup"><span data-stu-id="96936-127">If the first character is \* or #, the following character must be a number 1 through 9 (it cannot be a zero).</span></span> <span data-ttu-id="96936-128">後続の文字には、0 ~ 9 までの追加文字を使用できます (たとえば、"#6000"、"*92000"*、"95551212"、"915551212")。</span><span class="sxs-lookup"><span data-stu-id="96936-128">Subsequent characters can be any number 0 through 9 up to seven additional characters (for example, "#6000", "*92000", "* 95551212", and "915551212").</span></span> <span data-ttu-id="96936-129">最初の文字が \* または # ではない場合、最初の文字には 1 ～ 9 の数字 (0 は不可) を指定し、その後に 0 ～ 9 の数字を最大 8 文字まで指定します ("915551212"、"41212"、"300" など)。</span><span class="sxs-lookup"><span data-stu-id="96936-129">If the first character is not \* or #, the first character must be a number 1 through 9 (it cannot be zero), followed by up to eight characters, each a number 0 through 9 (for example, "915551212", "41212", "300").</span></span></P>
    > <LI>
    > <P><span data-ttu-id="96936-p107">プール当たりの合計が 50,000 オービットを超えないようにしてください。各オービット範囲は、通常、100 以下のオービットを含みますが、10,000 オービットを超えなければ、範囲をそれよりも広くすることができます。たとえば、開始番号 "7000000"、終了番号 "8000000" を指定するのではなく、開始番号 "7000000"、終了番号 "7000100" を指定することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="96936-p107">You should not have more than a total of 50,000 orbits per pool. Each orbit range typically encompasses 100 or fewer orbits, but it can be much larger as long as it includes fewer than 10,000 orbits. For example, instead of specifying a starting number of "7000000" and an ending number of "8000000," consider specifying a starting number of "7000000" and an ending number of "7000100."</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="96936-133">[ **宛先サーバーの fqdn**] で、コールパークアプリケーションをホストするアプリケーションサービスの完全修飾ドメイン名 (FQDN) またはサービス ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96936-133">In **FQDN of destination server**, click the fully qualified domain name (FQDN) or service ID of the Application service that hosts the Call Park application.</span></span> <span data-ttu-id="96936-134">オービット範囲の開始番号と終了番号で指定された範囲内の番号にパークされる通話は、すべてこのサーバーまたはプールにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="96936-134">All calls parked to numbers within the range specified by the start number and end number in the orbit range will be routed to this server or pool.</span></span>

7.  <span data-ttu-id="96936-135">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96936-135">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-range-of-numbers-for-parking-calls"></a><span data-ttu-id="96936-136">Windows PowerShell を使用してパーキング通話の数値の範囲を作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="96936-136">To use Windows PowerShell to create or modify a range of numbers for parking calls</span></span>

1.  <span data-ttu-id="96936-137">Lync Server 管理シェルが RTCUniversalServerAdmins グループのメンバーとして、または「 [Lync server 2013 の委任セットアップの権限](lync-server-2013-delegate-setup-permissions.md)」で説明されているように、必要なユーザー権限を持つコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="96936-137">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="96936-138">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="96936-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="96936-139">オービット番号の新しい範囲を作成するには、**New-CsCallParkOrbit** を使用します。</span><span class="sxs-lookup"><span data-stu-id="96936-139">Use **New-CsCallParkOrbit** to create a new range of orbit numbers.</span></span> <span data-ttu-id="96936-140">オービット番号の既存の範囲を変更するには、**Set-CsCallParkOrbit** を使用します。</span><span class="sxs-lookup"><span data-stu-id="96936-140">Use **Set-CsCallParkOrbit** to modify an existing range of orbit numbers.</span></span>
    
    <span data-ttu-id="96936-141">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="96936-141">At the command line, run:</span></span>
    
        New-CsCallParkOrbit -Identity <name of orbit range> -NumberRangeStart <first number in orbit range> -NumberRangeEnd <last number in orbit range> -CallParkService <FQDN or service ID of the Application service that hosts the Call Park application>
    
    <span data-ttu-id="96936-142">例:</span><span class="sxs-lookup"><span data-stu-id="96936-142">For example:</span></span>
    
        New-CsCallParkOrbit -Identity "Redmond orbit 1" -NumberRangeStart 100 -NumberRangeEnd 199 -CallParkService redmond-applicationserver-1
    
    <span data-ttu-id="96936-143">次の例は、既存のオービット範囲内の番号を変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="96936-143">The following example shows how to modify the numbers in an existing orbit range,</span></span>
    
        Set-CsCallParkOrbit -Identity "Redmond orbit 1" -NumberRangeStart 500 -NumberRangeEnd 699

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="96936-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="96936-144">See Also</span></span>


[<span data-ttu-id="96936-145">Lync Server 2013 でのコールパークの範囲の削除</span><span class="sxs-lookup"><span data-stu-id="96936-145">Delete a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-delete-a-call-park-orbit-range.md)  


[<span data-ttu-id="96936-146">新規-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="96936-146">New-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsCallParkOrbit)  
[<span data-ttu-id="96936-147">Set-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="96936-147">Set-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit)  
  

<span data-ttu-id="96936-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96936-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

