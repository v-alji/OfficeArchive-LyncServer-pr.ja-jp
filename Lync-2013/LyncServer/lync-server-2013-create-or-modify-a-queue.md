---
title: 'Lync Server 2013: キューを作成または変更する'
description: 'Lync Server 2013: キューを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a queue
ms:assetid: b9d6366a-839f-4651-a01d-9254546cadeb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205207(v=OCS.15)
ms:contentKeyID: 48185247
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbd8d6d00df8d6a09ef5861d876bd1363db09e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431758"
---
# <a name="create-or-modify-a-queue-in-lync-server-2013"></a><span data-ttu-id="f1683-103">Lync Server 2013 でキューを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="f1683-103">Create or modify a queue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1683-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1683-104">

<span> </span></span></span>

<span data-ttu-id="f1683-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f1683-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f1683-106">キューを作成または変更するには、以下のいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f1683-106">Use one of the following procedures to create or modify a queue.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-create-or-modify-a-queue"></a><span data-ttu-id="f1683-107">Lync Server コントロールパネルを使用してキューを作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="f1683-107">To use Lync Server Control Panel to create or modify a queue</span></span>

1.  <span data-ttu-id="f1683-108">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="f1683-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-109">管理ワークフローを委任された応答グループ マネージャーのいずれかである場合は、応答グループ キューを作成または変更して、管理するワークグループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f1683-109">If you are one of the delegated Response Group Managers for a managed workflow, you can create or modify response group queues and assign them to the workflows that you manage.</span></span>

    
    </div>

2.  <span data-ttu-id="f1683-110">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f1683-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f1683-111">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f1683-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f1683-112">左側のナビゲーション バーで [**応答グループ**] をクリックし、[**キュー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-112">In the left navigation bar, click **Response Groups**, and then click **Queue**.</span></span>

4.  <span data-ttu-id="f1683-113">[**キュー**] ページで、次のいずれかの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-113">On the **Queue** page, do one of the following:</span></span>
    
      - <span data-ttu-id="f1683-114">新しいキューを作成するには、[**新規作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-114">To create a new queue, click **New**.</span></span> <span data-ttu-id="f1683-115">[**サービスの選択**] の検索フィールドに、キューを追加する **ApplicationServer** サービスの名前の一部またはすべてを入力します。</span><span class="sxs-lookup"><span data-stu-id="f1683-115">In **Select a Service**, type part or all of the name of the **ApplicationServer** service where you want to add the queue in the search field.</span></span> <span data-ttu-id="f1683-116">表示されたサービスの一覧で、目的のサービスをクリックし、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="f1683-p103">既存のキューを変更するには、キューの名前または名前の一部を検索フィールドに入力します。結果のキューの一覧で、対象のキューをクリックし、[**編集**]、[**詳細の表示**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-p103">To modify an existing queue, type all or part of the queue name in the search field. In the resulting list of queues, click the queue that you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f1683-119">[**名前**] にキューの識別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1683-119">In **Name**, type an identifying name for the queue.</span></span>

6.  <span data-ttu-id="f1683-120">[**説明**] に、キューの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1683-120">In **Description**, type a description for the queue.</span></span>

7.  <span data-ttu-id="f1683-p104">[**グループ**] で、キューに割り当てるグループを指定します。次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1683-p104">In **Groups**, specify the groups you want to assign to the queue. Do one of the following:</span></span>
    
      - <span data-ttu-id="f1683-p105">キューにグループを追加するには、[**選択**] をクリックします。[**グループの選択**] の検索フィールドに、キューに割り当てるエージェント グループの名前または名前の一部を入力し、一覧で目的のエージェント グループをクリックして、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-p105">To add a group to the queue, click **Select**. In the **Select Groups** search field, type all or part of the name of the agent group that you want to assign to the queue, click the agent group that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="f1683-125">キューからグループを削除するには、エージェント グループの一覧で、削除するグループをクリックし、[**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-125">To remove a group from the queue, in the list of agent groups, click the group that you want to remove, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="f1683-126">エージェントを検索する順序を変更するには、エージェント グループの一覧でグループをクリックし、上矢印または下矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-126">To change the order in which agents are searched, in the list of agent groups, click a group, and then click the up arrow or down arrow.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="f1683-p106">サーバーでは、キューで利用可能なエージェントを検索するときには、グループの順序が使用されます。つまり、一覧の最初のグループが最初に検索され、一覧の 2 番目のグループが次に検索され、以降も同様に検索されます。</span><span class="sxs-lookup"><span data-stu-id="f1683-p106">When the server searches for an available agent for the queue, it uses group order. That is, the first group in the list is searched first, followed by the second group in the list, and so on.</span></span>

        
        </div>

8.  <span data-ttu-id="f1683-129">エージェントが通話に応答するまで発信者を保留状態にする最長時間を指定するには、[**キューのタイムアウトを有効にする**] チェック ボックスをオンにして次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-129">To specify a maximum period of time for a caller to wait on hold before an agent answers the call, select the **Enable queue time-out** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="f1683-130">[**タイムアウト時間 (秒)**] で、エージェントが通話に応答するのを発信者が待つ最大秒数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1683-130">In **Time-out period (seconds)**, specify the maximum number of seconds a caller waits for an agent to answer the call.</span></span>
    
    2.  <span data-ttu-id="f1683-131">[**通話アクション**] で、呼び出しがタイムアウトになったときに行う動作を次のように選択します。</span><span class="sxs-lookup"><span data-stu-id="f1683-131">In **Call Action**, select the action that occurs when a call times out as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="f1683-132">タイムアウト後通話を終了するには、[**切断**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-132">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="f1683-133">通話をボイスメールに転送するには、[**ボイスメールに転送**] をクリックし、[ **sip アドレス**] フィールドに、「sip:」という形式でボイスメールアドレスを入力します \<username\> @ \<domainname\> (たとえば、sip:bob@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="f1683-133">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="f1683-134">別の電話番号に通話を転送するには、[**電話番号に転送**] をクリックして、[ **sip アドレス**] フィールドに電話番号を「sip:」の形式で入力します \<number\> @ \<domainname\> (たとえば、sip:+14255550121@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="f1683-134">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="f1683-135">通話を別のユーザーに転送するには、[ **sip アドレスに転送**] をクリックし、[ **sip アドレス**] フィールドにユーザーの URI を「sip:」という形式で入力し \<username\> @ \<domainname\> ます。</span><span class="sxs-lookup"><span data-stu-id="f1683-135">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="f1683-136">別のキューに通話を転送する場合は [**別のキューに転送**] をクリックし、使用するキューを参照します。</span><span class="sxs-lookup"><span data-stu-id="f1683-136">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

9.  <span data-ttu-id="f1683-137">キューに保持できる最大通話数を指定するには、[**キューのオーバーフローを有効にする**] チェック ボックスをオンにして次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-137">To specify a maximum number of calls that the queue can hold, select the **Enable queue overflow** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="f1683-138">[**最大通話数**] で、キューで保持する最大通話数を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1683-138">In **Maximum number of calls**, select the maximum number of calls that you want the queue to hold.</span></span>
    
    2.  <span data-ttu-id="f1683-139">[**通話の転送**] で、キューが一杯になったときに転送する通話を、[**最新の通話**] または [**最も古い通話**] から選択します。</span><span class="sxs-lookup"><span data-stu-id="f1683-139">In **Forward the call**, select which call is to be forwarded when the queue is full: **Newest Call** or **Oldest Call**.</span></span>
    
    3.  <span data-ttu-id="f1683-140">[**通話アクション**] で、オーバーフローしきい値に達したときに実行する処理を、次のように選択します。</span><span class="sxs-lookup"><span data-stu-id="f1683-140">In **Call action**, select the action that occurs when the overflow threshold is met as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="f1683-141">タイムアウト後通話を終了するには、[**切断**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-141">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="f1683-142">通話をボイスメールに転送するには、[**ボイスメールに転送**] をクリックし、[ **sip アドレス**] フィールドに、「sip:」という形式でボイスメールアドレスを入力します \<username\> @ \<domainname\> (たとえば、sip:bob@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="f1683-142">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="f1683-143">別の電話番号に通話を転送するには、[**電話番号に転送**] をクリックして、[ **sip アドレス**] フィールドに電話番号を「sip:」の形式で入力します \<number\> @ \<domainname\> (たとえば、sip:+14255550121@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="f1683-143">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="f1683-144">通話を別のユーザーに転送するには、[ **sip アドレスに転送**] をクリックし、[ **sip アドレス**] フィールドにユーザーの URI を「sip:」という形式で入力し \<username\> @ \<domainname\> ます。</span><span class="sxs-lookup"><span data-stu-id="f1683-144">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="f1683-145">別のキューに通話を転送する場合は [**別のキューに転送**] をクリックし、使用するキューを参照します。</span><span class="sxs-lookup"><span data-stu-id="f1683-145">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

10. <span data-ttu-id="f1683-146">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-146">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-queue"></a><span data-ttu-id="f1683-147">Windows PowerShell を使用してキューを作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="f1683-147">To use Windows PowerShell to create or modify a queue</span></span>

1.  <span data-ttu-id="f1683-148">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="f1683-148">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-149">管理ワークフローを委任された応答グループ マネージャーのいずれかである場合は、エージェント グループおよびキューを作成して、エージェント グループをキューに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f1683-149">If you are one of the delegated Response Group Managers for a managed workflow, you will be able to create agent groups and queues, and assign agent groups to queues.</span></span>

    
    </div>

2.  <span data-ttu-id="f1683-150">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1683-150">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f1683-p107">キューのタイムアウトしきい値に達したときに再生されるプロンプトを作成し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p107">Create the prompt to be played when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptTO = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="f1683-153">例:</span><span class="sxs-lookup"><span data-stu-id="f1683-153">For example:</span></span>
    
        "All agents are currently busy. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-154">プロンプトにオーディオ ファイルを使用するには、 <STRONG>Import-CsRgsAudioFile</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1683-154">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="f1683-155">詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">インポート-CsRgsAudioFile</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1683-155">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="f1683-p109">キューのタイムアウトしきい値に達したときに実行されるアクションを定義し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p109">Define the action to be taken when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionTO = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-158">可能なアクションとその構文の詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">新しい-CsRgsCallAction</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1683-158">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="f1683-159">例:</span><span class="sxs-lookup"><span data-stu-id="f1683-159">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptTO -Action Terminate

5.  <span data-ttu-id="f1683-p110">キューのオーバーフローしきい値に達したときに再生されるプロンプトを作成し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p110">Create the prompt to be played when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="f1683-162">例:</span><span class="sxs-lookup"><span data-stu-id="f1683-162">For example:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "Too many calls are waiting. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-163">プロンプトにオーディオ ファイルを使用するには、 <STRONG>Import-CsRgsAudioFile</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1683-163">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="f1683-164">詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">インポート-CsRgsAudioFile</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1683-164">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

6.  <span data-ttu-id="f1683-p112">キューのオーバーフローしきい値に達したときに実行されるアクションを定義し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p112">Define the action to be taken when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionOV = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-167">可能なアクションとその構文の詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">新しい-CsRgsCallAction</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1683-167">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="f1683-168">例:</span><span class="sxs-lookup"><span data-stu-id="f1683-168">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptOV -Action Terminate

7.  <span data-ttu-id="f1683-p113">応答グループ サービスのサービス名を取得し、変数に割り当てます。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p113">Retrieve the service name for the Response Group service and assign it to a variable. At the command line, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -Like "*RGS*"}).ServiceId;

8.  <span data-ttu-id="f1683-p114">キューに割り当てるエージェント グループの Identity を取得します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p114">Get the identity of the agent group to be assigned to the queue. At the command line, run:</span></span>
    
        $agid = (Get-CsRgsAgentGroup -Name "Help Desk").Identity;
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1683-173">エージェントグループの作成の詳細については、「<A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">新しい-CsRgsAgentGroup</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1683-173">For details about creating the agent group, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">New-CsRgsAgentGroup</A></span></span>

    
    </div>

9.  <span data-ttu-id="f1683-p115">キューを作成します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p115">Create the queue. At the command line, run:</span></span>
    
        $q = New-CsRgsQueue -Parent <saved service ID from previous step> -Name "<name of queue>" [-Description "<description for queue>"] [-TimeoutThreshold <# seconds before call times out>] [-TimeoutAction <saved timeout action>] [-OverflowThreshold <# calls queue can hold>] [-OverflowCandidate <call to be acted on when overflow threshold met>] [-OverflowAction <saved overflow action>] [-AgentGroupIDList(<agent group identity>)];
    
    <span data-ttu-id="f1683-176">例:</span><span class="sxs-lookup"><span data-stu-id="f1683-176">For example:</span></span>
    
        $q = New-CsRgsQueue -Parent $serviceId -Name "Help Desk" -Description "Contoso Help Desk" -TimeoutThreshold 300 -TimeoutAction $actionTO -OverflowThreshold 10 -OverflowCandidate NewestCall -OverflowAction $actionOV -AgentGroupIDList($agid.Identity;

10. <span data-ttu-id="f1683-p116">キューが作成されたことを確認します。次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="f1683-p116">Confirm that the queue is created. Run:</span></span>
    
        Get-CsRgsQueue -Name "Help Desk"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f1683-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1683-179">See Also</span></span>


[<span data-ttu-id="f1683-180">New-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="f1683-180">New-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue)  
[<span data-ttu-id="f1683-181">Set-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="f1683-181">Set-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsQueue)  
[<span data-ttu-id="f1683-182">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="f1683-182">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="f1683-183">New-CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="f1683-183">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
[<span data-ttu-id="f1683-184">Get-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="f1683-184">Get-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsQueue)  
[<span data-ttu-id="f1683-185">Import-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="f1683-185">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
[<span data-ttu-id="f1683-186">Remove-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="f1683-186">Remove-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsQueue)  
  

<span data-ttu-id="f1683-187"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1683-187"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

