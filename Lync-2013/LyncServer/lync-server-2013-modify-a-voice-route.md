---
title: 'Lync Server 2013: ボイスルートを変更する'
description: 'Lync Server 2013: ボイスルートを変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a voice route
ms:assetid: afc562cc-8807-489b-8850-dbbe1c1ab9f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412838(v=OCS.15)
ms:contentKeyID: 48185143
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0aa507f3d0f459dd200b9c772f3a330d7da36197
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425536"
---
# <a name="modify-a-voice-route-in-lync-server-2013"></a><span data-ttu-id="02d6e-103">Lync Server 2013 での音声ルートの変更</span><span class="sxs-lookup"><span data-stu-id="02d6e-103">Modify a voice route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02d6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02d6e-104">

<span> </span></span></span>

<span data-ttu-id="02d6e-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="02d6e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="02d6e-106">このトピックでは、ボイスルートを編集する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-106">This topic explains how to edit a voice route.</span></span> <span data-ttu-id="02d6e-107">新しいルートを作成するには、「 [Lync Server 2013 での音声ルートの作成](lync-server-2013-create-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-107">To create a new route, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>

<div>

## <a name="to-modify-a-voice-route"></a><span data-ttu-id="02d6e-108">音声ルートを変更するには</span><span class="sxs-lookup"><span data-stu-id="02d6e-108">To modify a voice route</span></span>

1.  <span data-ttu-id="02d6e-109">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="02d6e-110">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="02d6e-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="02d6e-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="02d6e-113">左側のナビゲーション バーで [**音声のルーティング**] をクリックし、[**ルート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-113">In the left navigation bar, click **Voice Routing**, and then click **Route**.</span></span>

4.  <span data-ttu-id="02d6e-114">[**ルート**] ページで、次のいずれかの方法を使用して音声ルートを変更します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-114">On the **Route** page, use either of the following methods to modify a voice route:</span></span>
    
      - <span data-ttu-id="02d6e-115">音声ルート名をクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-115">Click a voice route name, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="02d6e-p104">音声ルート名をクリックし、[**編集**] をクリックし、[**コピー**] をクリックしてから、[**貼り付け**] をクリックします。直前に作成した音声ルートの新しいコピーをクリックし、[**編集**] をクリックしてから、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-p104">Click a voice route name, click **Edit**, click **Copy**, and then click **Paste**. Click the new copy of the voice route that you just created, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="02d6e-118">[**音声ルートの編集**] ページの "**名前**" フィールドに、音声ルートのわかりやすい名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-118">In the **Name** field on the **Edit Voice Route** page, type a descriptive name for the voice route.</span></span>

6.  <span data-ttu-id="02d6e-119">(オプション) "**説明**" フィールドに、音声ルートのわかりやすい追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-119">(Optional) In the **Description** field, type in additional descriptive information for the voice route.</span></span>

7.  <span data-ttu-id="02d6e-120">このルートが対応するパターンを指定するには、**照合するパターンの作成** ツールを使用して正規表現を生成するか、手動で正規表現を記述します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-120">To specify the patterns you want this route to accommodate, you can either use the **Build a pattern to match** tool to generate a regular expression, or write the regular expression manually.</span></span>
    
      - <span data-ttu-id="02d6e-p105">**照合するパターンの作成** ツールを使用して正規表現を生成するには、次の値を入力します。次の 2 種類の照合パターンを指定できます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-p105">To use the **Build a pattern to match** tool to generate a regular expression, enter values as follows. You can specify two types of pattern matching:</span></span>
        
          - <span data-ttu-id="02d6e-123">**許可する数値の開始数字:** このルートに含める必要のあるプレフィックスの値を入力します (先頭の + が必要な場合)。</span><span class="sxs-lookup"><span data-stu-id="02d6e-123">**Starting digits for numbers that you want to allow:** Enter prefix values that this route must accommodate (including the leading + if needed).</span></span> <span data-ttu-id="02d6e-124">たとえば、「**+425**」と入力して、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-124">For example, type **+425** and then click **Add**.</span></span> <span data-ttu-id="02d6e-125">このルートに含める各プレフィックス値について、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-125">Repeat this for each prefix value that you want to include in the route.</span></span>
        
          - <span data-ttu-id="02d6e-126">**例外:** プレフィックス値に1つまたは複数の例外を指定する場合は、プレフィックスを強調表示し、[ **例外処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-126">**Exceptions:** If you want to specify one or more exceptions for a prefix value, highlight the prefix and click **Exceptions**.</span></span> <span data-ttu-id="02d6e-127">このルートが *対応しない* 照合パターンの値を 1 つまたは複数入力します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-127">Type in one or more values for the matching patterns that you do *not* want this route to accommodate.</span></span> <span data-ttu-id="02d6e-128">たとえば、ルートから +425237 で始まる番号を除外するには、"**例外**" フィールドに「**+425237**」と入力して、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-128">For example, to exclude numbers starting with +425237 from the route, enter a value of **+425237** in the **Exceptions** field, and then click **OK**.</span></span>
    
      - <span data-ttu-id="02d6e-129">照合パターンを手動で定義するには、**照合するパターンの作成** ツールの [**編集**] をクリックし、.NET Framework の正規表現を入力して、ルートが適用される相手電話番号の照合パターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-129">To define the matching pattern manually, click **Edit** in the **Build a pattern to match** tool and then type in a .NET Framework regular expression to specify the matching pattern for destination phone numbers to which the route is applied.</span></span> <span data-ttu-id="02d6e-130">正規表現の記述方法については、「.NET Framework の正規表現」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) 。</span><span class="sxs-lookup"><span data-stu-id="02d6e-130">For information about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

8.  <span data-ttu-id="02d6e-p109">通話を発信する電話の ID を呼び出し先に表示しない場合は、[**発信者番号を表示しない**] を選択します。このオプションを選択した場合、呼び出し先の発信者 ID 表示に表示される、[**代替発信者番号**] を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02d6e-p109">Select **Suppress caller ID** if you do not want the ID of the phone that is making the outbound call to appear to the call recipient. If you select this option, you must specify an **Alternate caller ID** that will appear on the recipient’s caller ID display.</span></span>

9.  <span data-ttu-id="02d6e-133">1 つまたは複数の公衆交換電話網 (PSTN) トランクを音声ルートに関連付けるには、[**追加**] をクリックして、一覧からトランクを選択します。</span><span class="sxs-lookup"><span data-stu-id="02d6e-133">To associate one or more public switched telephone network (PSTN) trunks with the voice route, click **Add**, and then select a trunk from the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02d6e-134">展開に Microsoft Office Communications Server 2007 R2 仲介サーバーが含まれている場合は、それらも一覧で利用できます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-134">If your deployment includes any Microsoft Office Communications Server 2007 R2 Mediation Servers, they will also be available in the list.</span></span>

    
    </div>

10. <span data-ttu-id="02d6e-135">1つまたは複数の PSTN の使用状況をボイスルートに関連付けるには、[ **選択** ] をクリックし、エンタープライズ voip 展開用に定義されている pstn 使用状況レコードのリストからレコードを選びます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-135">To associate one or more PSTN usages with the voice route, click **Select** and choose a record from the list of PSTN usage records that have been defined for your Enterprise Voice deployment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02d6e-136">利用可能な各 PSTN 使用状況レコードのプロパティを表示するには、「 <A href="lync-server-2013-view-pstn-usage-records.md">Lync Server 2013 で pstn 使用状況レコードを表示</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-136">To view the properties of each of the available PSTN usage records, see <A href="lync-server-2013-view-pstn-usage-records.md">View PSTN usage records in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="02d6e-137">PSTN 使用状況レコードを作成または編集するには、「lync server <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">2013</A> <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">2013 でボイスポリシーを作成</A>する」および「pstn 使用状況レコードを構成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-137">To create or edit PSTN usage records, see <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">Create a voice policy and configure PSTN usage records in Lync Server 2013</A> or <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">Modify a voice policy and configure PSTN usage records in Lync Server 2013</A>.</span></span>

    
    </div>

11. <span data-ttu-id="02d6e-p110">最適なパフォーマンスを得るために、PSTN 使用法レコードを並べ替えます。一覧内でのレコードの位置を変更するには、レコードの名前を選択状態にして、上矢印または下矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-p110">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, highlight the record name and click the up or down arrow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02d6e-140">PSTN 利用状況レコードが記載されている順序が重要である場合、ボイスルーティングでの PSTN 使用状況レコードの順序は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="02d6e-140">In contrast to a voice policy where the order in which PSTN usage records are listed is important, the order of PSTN usage records in a voice route is insignificant.</span></span> <span data-ttu-id="02d6e-141">ただし、リストを使用頻度で整理することをお勧めします。例: RedmondLocal、RedmondLongDist、Redmondlocal、Redmondlocal。</span><span class="sxs-lookup"><span data-stu-id="02d6e-141">However, we recommend that you organize the list by frequency of use, for example: RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span></span> <span data-ttu-id="02d6e-142">(Lync Server は、一覧を上から下に移動します。)</span><span class="sxs-lookup"><span data-stu-id="02d6e-142">(Lync Server traverses the list from the top down.)</span></span>

    
    </div>

12. <span data-ttu-id="02d6e-p112">(オプション) "**テストする変換後の番号**" フィールドに値を入力して、[**実行**] をクリックします。テスト結果がフィールドの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-p112">(Optional) Type a value into the **Enter a translated number to test** field and click **Go**. The test results are displayed under the field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02d6e-145">まだテストに合格しない音声ルートを保存し、後で再構成することができます。</span><span class="sxs-lookup"><span data-stu-id="02d6e-145">You can save a voice route that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="02d6e-146">詳細については、「 <A href="lync-server-2013-test-voice-routing.md">Lync Server 2013 での音声ルーティングのテスト</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-146">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

13. <span data-ttu-id="02d6e-147">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-147">Click **OK**.</span></span>

14. <span data-ttu-id="02d6e-148">[**ルート**] ページの [**確定**] をクリックして、[**すべて確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02d6e-148">On the **Route** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02d6e-149">音声ルートを作成または変更するときは常に、[<STRONG>すべて確定</STRONG>] コマンドを実行して、構成の変更を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02d6e-149">Whenever you create or modify a voice route, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="02d6e-150">詳細については、「操作のドキュメントで「 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 のボイスルーティング構成に保留中の変更を発行する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d6e-150">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="02d6e-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="02d6e-151">See Also</span></span>


[<span data-ttu-id="02d6e-152">Lync Server 2013 での音声ルートの作成</span><span class="sxs-lookup"><span data-stu-id="02d6e-152">Create a voice route in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-route.md)  
[<span data-ttu-id="02d6e-153">Lync Server 2013 での PSTN 使用状況レコードの表示</span><span class="sxs-lookup"><span data-stu-id="02d6e-153">View PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-view-pstn-usage-records.md)  
[<span data-ttu-id="02d6e-154">Lync Server 2013 で音声ポリシーを作成し、PSTN 使用状況レコードを構成する</span><span class="sxs-lookup"><span data-stu-id="02d6e-154">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="02d6e-155">Lync Server 2013 で音声ポリシーを変更し、PSTN 使用状況レコードを構成する</span><span class="sxs-lookup"><span data-stu-id="02d6e-155">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="02d6e-156">Lync Server 2013 の音声ルーティング構成に保留中の変更を発行する</span><span class="sxs-lookup"><span data-stu-id="02d6e-156">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="02d6e-157">Lync Server 2013 での音声ルーティングのテスト</span><span class="sxs-lookup"><span data-stu-id="02d6e-157">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="02d6e-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02d6e-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

