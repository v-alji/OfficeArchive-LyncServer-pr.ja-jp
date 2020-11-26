---
title: 'Lync Server 2013: 未割り当ての番号範囲を作成または変更する'
description: 'Lync Server 2013: 割り当てられていない番号の範囲を作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify an unassigned number range
ms:assetid: a102b226-0460-4d5c-82f9-79b8444fa958
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412748(v=OCS.15)
ms:contentKeyID: 48185013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2998616b931e94c9c38fc44d569b84b3af37709d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431660"
---
# <a name="create-or-modify-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="de162-103">Lync Server 2013 で、割り当てられていない番号範囲を作成または変更する</span><span class="sxs-lookup"><span data-stu-id="de162-103">Create or modify an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de162-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de162-104">

<span> </span></span></span>

<span data-ttu-id="de162-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="de162-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="de162-106">次のいずれかの手順を使用して、アナウンスメントアプリケーションの未割り当ての番号範囲を構成します。</span><span class="sxs-lookup"><span data-stu-id="de162-106">Use one of the following procedures to configure unassigned number ranges for the Announcement application.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="de162-107">[割り当てられていない番号] テーブルを構成する前に、1つ以上のアナウンスを既に定義しているか、Exchange ユニファイドメッセージング (UM) 自動応答をセットアップしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de162-107">Before you configure the unassigned number table, you must have already defined one or more announcements or set up an Exchange Unified Messaging (UM) Auto Attendant.</span></span>



</div>

<div>

## <a name="to-use-lync-server-control-panel-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="de162-108">Lync Server コントロールパネルを使用して、割り当てられていない電話番号を設定するには</span><span class="sxs-lookup"><span data-stu-id="de162-108">To use Lync Server Control Panel to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="de162-109">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="de162-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="de162-110">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de162-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="de162-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="de162-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="de162-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="de162-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="de162-113">左側のナビゲーション バーで [**音声機能**] をクリックし、[**割り当てられていない番号**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-113">In the left navigation bar, click **Voice Features**, and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="de162-114">[**割り当てられていない番号**] ページで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="de162-114">On the **Unassigned Number** page, do one of the following:</span></span>
    
      - <span data-ttu-id="de162-p103">新しい番号範囲を作成するには、[**新規**] をクリックします。[**名前**] にこの番号範囲の識別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="de162-p103">To create a new number range, click **New**. In **Name**, type an identifying name for this range of numbers.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="de162-117">割り当てられていない番号の新しい範囲をデータベースに送信した後は、この名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="de162-117">After you commit the new unassigned number range to the database, you cannot change this name.</span></span>

        
        </div>
    
      - <span data-ttu-id="de162-p104">既存の番号範囲を変更するには、番号範囲の名前または名前の一部を検索フィールドに入力します。結果の番号範囲の一覧で、対象の名前をクリックして、[**編集**] をクリックし、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-p104">To modify an existing number range, type all or part of the name of the number range in the search field. In the resulting list of number ranges, click the name you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="de162-120">最初の [**数値の範囲**] フィールドに範囲の開始番号を入力し、2 番目の [**数値の範囲**] フィールドに範囲の終了番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="de162-120">In the first **Number range** field, type the beginning number of the range, and in the second **Number range** field, type the ending number of the range.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="de162-121">範囲の開始番号が終了番号より大きくならないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="de162-121">The beginning number of the range must be less than or equal to the ending number of the range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="de162-122">範囲の開始番号または終了番号に内線番号が含まれる場合は、両方の番号が内線番号を含む必要があり、その内線番号は両方の番号で一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de162-122">If the beginning number of the range or the ending number of the range includes an extension number, both the beginning number and the ending number of the range must include an extension, and the extension number must be the same for both the beginning number and the ending number.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="de162-123">数値は正規表現 (tel:)? () と一致する必要があり \+ ますか?[1-9] \d {0,17} (; ext = [1-9] \d {0,9} )?</span><span class="sxs-lookup"><span data-stu-id="de162-123">The number must match the regular expression (tel:)?(\+)?[1-9]\d{0,17}(;ext=[1-9]\d{0,9})?.</span></span> <span data-ttu-id="de162-124">これは、数値が文字列 "tel" で始まる可能性があることを意味します (文字列を指定しない場合は自動的に追加されます)、プラス記号 (+)、1 ~ 9 桁の数字です。</span><span class="sxs-lookup"><span data-stu-id="de162-124">This means the number may begin with the string tel: (if you don’t specify that string, it will be automatically added for you), a plus sign (+), and a digit 1 through 9.</span></span> <span data-ttu-id="de162-125">電話番号は最大17桁で、その後に形式の内線番号、内線番号、内線番号が続く場合があります。</span><span class="sxs-lookup"><span data-stu-id="de162-125">The phone number can be up to 17 digits and may be followed by an extension in the format ;ext= followed by the extension number.</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="de162-126">[**アナウンス サービス**] で、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de162-126">In **Announcement service**, do one of the following:</span></span>
    
      - <span data-ttu-id="de162-127">[**アナウンス**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-127">Click **Announcement**.</span></span>
    
      - <span data-ttu-id="de162-128">[**Exchange UM**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-128">Click **Exchange UM**.</span></span>

7.  <span data-ttu-id="de162-129">前の手順で [**アナウンス**] をクリックした場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de162-129">If, in the previous step, you clicked **Announcement**, do the following:</span></span>
    
    1.  <span data-ttu-id="de162-130">[ **宛先サーバーの FQDN**] で [ **選択**] をクリックし、この範囲の未割り当て番号への着信通話を処理するアナウンスメントアプリケーションを実行するアプリケーションサービスのサービス ID をクリックして、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-130">Under **FQDN of destination server**, click **Select**, click the service ID of the Application service that runs the Announcement application that will handle incoming calls to this range of unassigned numbers, and then click **OK**.</span></span>
    
    2.  <span data-ttu-id="de162-131">[**アナウンス**] で、この割り当てられていない番号範囲に対して再生されるアナウンスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-131">In **Announcement**, click the announcement to be played for this range of unassigned numbers.</span></span>

8.  <span data-ttu-id="de162-132">前の手順で [**Exchange UM**] をクリックした場合は、[**自動応答の電話番号**] で、[**選択**] をクリックし、この割り当てられていない番号範囲に対して使用される電話番号をクリックし、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-132">If, in the previous step, you clicked **Exchange UM**, under **Auto Attendant phone number**, click **Select**, click the phone number to be used for this range of unassigned numbers, and then click **OK**.</span></span>

9.  <span data-ttu-id="de162-133">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-133">Click **OK**.</span></span>

10. <span data-ttu-id="de162-p106">[**割り当てられていない番号**] ページで、割り当てられていない番号範囲が希望どおりの順序で並んでいることを確認します。表で範囲の位置を変更するには、範囲の一覧で 1 つ以上の連続する名前をクリックして、上矢印または下矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-p106">On the **Unassigned Number** page, be sure that the unassigned number ranges are arranged in the order that you want. To change a range's position in the table, click one or more consecutive names in the list of ranges, and then click the up arrow or the down arrow.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="de162-136">Lync Server は、割り当てられていない番号テーブルを上から下に検索し、割り当てられていない番号に一致する最初の範囲を使用します。</span><span class="sxs-lookup"><span data-stu-id="de162-136">Lync Server searches the unassigned number table from top to bottom and uses the first range that matches the unassigned number.</span></span> <span data-ttu-id="de162-137">重複する範囲があり、そのうちの 1 つが最後のアクションを指定している場合は、その範囲が一覧の一番下にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="de162-137">If you have overlapping ranges and one range specifies a last resort action, make sure that range is at the bottom of the list.</span></span>

    
    </div>

11. <span data-ttu-id="de162-138">割り当てられていない番号範囲が希望どおりの順序で並んでいることを確認したら、[**すべて確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-138">When you have the unassigned number ranges in the order that you want, click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="de162-139">Windows PowerShell を使用して、割り当てられていない電話番号を構成するには</span><span class="sxs-lookup"><span data-stu-id="de162-139">To use Windows PowerShell to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="de162-140">Lync Server 管理シェルが RTCUniversalServerAdmins グループのメンバーとして、または「 [Lync server 2013 の委任セットアップの権限](lync-server-2013-delegate-setup-permissions.md)」で説明されているように、必要なユーザー権限を持つコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="de162-140">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="de162-141">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="de162-141">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="de162-142">新しい割り当てられていない番号範囲を作成するには、**New-CsUnassignedNumber** を使用します。</span><span class="sxs-lookup"><span data-stu-id="de162-142">Use **New-CsUnassignedNumber** to create a new unassigned number range.</span></span> <span data-ttu-id="de162-143">既存の割り当てられていない番号範囲を変更するには、**Set-CsUnassignedNumber** を使用します。</span><span class="sxs-lookup"><span data-stu-id="de162-143">Use **Set-CsUnassignedNumber** to modify an existing unassigned number range.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="de162-p109">重複する範囲があり、それらを特定の順序で適用する場合は、Priority パラメーターを含めます。最も優先度の高い範囲が通話に適用されます。</span><span class="sxs-lookup"><span data-stu-id="de162-p109">If you have overlapping ranges and want the ranges to be applied in a specific order, include the Priority parameter. The range with the highest priority will be applied to the call.</span></span>

    
    </div>
    
    <span data-ttu-id="de162-146">コマンド ラインで、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="de162-146">At the command line, do one of the following:</span></span>
    
      - <span data-ttu-id="de162-147">アナウンス サービスの番号範囲を作成するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="de162-147">To create a number range for an Announcement service, run:</span></span>
        
            New-CsUnassignedNumber -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range> -AnnouncementName <announcement name> -AnnouncementService <FQDN or service ID of the Announcement service>
    
      - <span data-ttu-id="de162-148">Exchange UM 自動応答の番号範囲を作成するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="de162-148">Or, to create a number range for Exchange UM Auto Attendant, run:</span></span>
        
            New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber <phone number> -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range>
    
    <span data-ttu-id="de162-149">例:</span><span class="sxs-lookup"><span data-stu-id="de162-149">For example:</span></span>
    
        New-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100" -AnnouncementName "Welcome Announcement" -AnnouncementService ApplicationServer:Redmond.contoso.com
    
    <span data-ttu-id="de162-150">または</span><span class="sxs-lookup"><span data-stu-id="de162-150">Or</span></span>
    
        New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber "+12065551234" -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100"
    
    <span data-ttu-id="de162-151">次の例は、既存の割り当てられていない番号範囲の番号を変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="de162-151">The following example shows how to modify the numbers in an existing unassigned number range:</span></span>
    
        Set-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551900"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="de162-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="de162-152">See Also</span></span>


[<span data-ttu-id="de162-153">Lync Server 2013 で、割り当てられていない番号範囲を削除する</span><span class="sxs-lookup"><span data-stu-id="de162-153">Delete an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-delete-an-unassigned-number-range.md)  


[<span data-ttu-id="de162-154">New-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="de162-154">New-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUnassignedNumber)  
[<span data-ttu-id="de162-155">Set-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="de162-155">Set-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUnassignedNumber)  
[<span data-ttu-id="de162-156">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="de162-156">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="de162-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de162-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

