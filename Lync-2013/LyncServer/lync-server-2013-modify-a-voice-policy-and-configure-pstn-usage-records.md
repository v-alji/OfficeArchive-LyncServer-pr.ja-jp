---
title: 'Lync Server 2013: 音声ポリシーを変更し、PSTN 使用状況レコードを構成する'
description: 'Lync Server 2013: 音声ポリシーを変更し、PSTN 使用状況レコードを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a voice policy and configure PSTN usage records
ms:assetid: 6c53aaf5-218b-4bd4-8cea-31bc9d53f1bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398511(v=OCS.15)
ms:contentKeyID: 48184419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e26d6c8654ebf758f8b5a185c21468443e0451a9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445779"
---
# <a name="modify-a-voice-policy-and-configure-pstn-usage-records-in-lync-server-2013"></a><span data-ttu-id="84f11-103">Lync Server 2013 で音声ポリシーを変更し、PSTN 使用状況レコードを構成する</span><span class="sxs-lookup"><span data-stu-id="84f11-103">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84f11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84f11-104">

<span> </span></span></span>

<span data-ttu-id="84f11-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="84f11-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="84f11-106">音声ポリシーを変更する場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-106">Follow these steps if you want to modify a voice policy.</span></span> <span data-ttu-id="84f11-107">新しい音声ポリシーを作成する場合は、手順について「 [Lync Server 2013 で音声ポリシーを作成し、PSTN 使用状況レコードを構成](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-107">If you want to create a new voice policy, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md) for the procedure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="84f11-108">ボイスポリシーにユーザーが割り当てられている場合、公衆交換電話網 (PSTN) 利用状況レコードが関連付けられていない場合、ユーザーは送信通話を発信できません。</span><span class="sxs-lookup"><span data-stu-id="84f11-108">If a user is assigned to a voice policy has no associated public switched telephone network (PSTN) usage records, the user cannot place outbound calls.</span></span> <span data-ttu-id="84f11-109">エンタープライズ Voip 展開で利用できるすべての PSTN 使用状況レコードの一覧を表示してプロパティを表示するには、「 <A href="lync-server-2013-view-pstn-usage-records.md">Lync Server 2013 で pstn 使用状況レコードを表示</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-109">For a listing of all PSTN usage records available in your Enterprise Voice deployment and view their properties, see <A href="lync-server-2013-view-pstn-usage-records.md">View PSTN usage records in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-modify-a-voice-policy"></a><span data-ttu-id="84f11-110">音声ポリシーを変更するには</span><span class="sxs-lookup"><span data-stu-id="84f11-110">To modify a voice policy</span></span>

1.  <span data-ttu-id="84f11-111">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="84f11-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="84f11-112">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="84f11-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="84f11-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="84f11-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="84f11-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="84f11-115">左側のナビゲーション バーで [**音声のルーティング**] をクリックし、[**音声ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-115">In the left navigation bar, click **Voice Routing**, and then click **Voice Policy**.</span></span>

4.  <span data-ttu-id="84f11-116">[**音声ポリシー**] ページで、音声ポリシー名をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-116">On the **Voice Policy** page, double-click a voice policy name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84f11-p105">スコープと名前は、音声ポリシーの作成時に設定されています。これらは変更できません。</span><span class="sxs-lookup"><span data-stu-id="84f11-p105">The scope and name were set when the voice policy was created. They cannot be changed.</span></span>

    
    </div>

5.  <span data-ttu-id="84f11-119">(オプション) [**音声ポリシーの編集**] に、音声ポリシーの説明情報を追加で入力します。</span><span class="sxs-lookup"><span data-stu-id="84f11-119">(Optional) In **Edit Voice Policy**, enter additional descriptive information for the voice policy.</span></span>

6.  <span data-ttu-id="84f11-120">次のチェック ボックスをオンまたはオフにして、[**通話機能**] をそれぞれ有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="84f11-120">Select or clear the following check boxes to enable or disable each of the **Calling features**:</span></span>
    
      - <span data-ttu-id="84f11-121">[**ボイス メール エスケープ**] は、同時呼び出しが構成されている場合に、電話が電源オフ、電池切れ、または圏外になっているときに、通話がユーザーの携帯電話のボイス メール システムにすぐにルーティングされることを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="84f11-121">**Voice mail escape** prevents calls from being immediately routed to the user’s mobile phone voice mail system when simultaneous ringing is configured and the phone is turned off, out of battery, or out of range.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="84f11-122">この機能を構成できるのは、Lync Server 管理シェルを使用した場合のみです。</span><span class="sxs-lookup"><span data-stu-id="84f11-122">This feature is only configurable through the Lync Server Management Shell</span></span>

        
        </div>
    
      - <span data-ttu-id="84f11-123">[**着信の転送**] では、他の電話機やクライアント デバイスに通話を転送できます。</span><span class="sxs-lookup"><span data-stu-id="84f11-123">**Call forwarding** enables users to forward calls to other phones and client devices.</span></span> <span data-ttu-id="84f11-124">Lync Server 2013 には、通話転送に関するさまざまな構成オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="84f11-124">Lync Server 2013 provides a significantly wider range of configuration options for call forwarding.</span></span> <span data-ttu-id="84f11-125">たとえば、着信が外部で PSTN に転送されることを組織が許可しない方針の場合、管理者は特殊な音声ポリシーを適用して、この制限を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-125">For example, if an organization does not want to allow incoming calls to be forwarded externally to the PSTN, an administrator can apply a special voice policy to deploy this restriction.</span></span> <span data-ttu-id="84f11-126">既定では有効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-126">Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-127">[**委任**] では、代わりに通話を送受信する他のユーザーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="84f11-127">**Delegation** enables users to specify other users to send and receive calls on their behalf.</span></span> <span data-ttu-id="84f11-128">Lync Server 2013 では、代理人が同時呼び出しを設定することで、そのマネージャーが着信したときに、すべての代理人の同時呼び出し先が呼び出されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-128">In Lync Server 2013, a delegate can configure simultaneous ringing that enables incoming calls to his or her manager to ring all of the delegate’s simultaneous ringing targets.</span></span> <span data-ttu-id="84f11-129">これにより、上司に転送された通話に応答するときの柔軟性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-129">This provides the delegate with greater flexibility in responding to calls directed to the manager.</span></span> <span data-ttu-id="84f11-130">既定では有効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-130">Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-p108">[**通話の転送**] では、他のユーザーに通話を転送できます。既定では有効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-p108">**Call transfer** enables users to transfer calls to other users. Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-p109">[**コール パーク**] では、通話を保留 (パーク) し、別の電話機やクライアントで受けることができます。既定では無効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-p109">**Call park** enables users to park calls on hold, and then pick up the call from a different phone or client. Disabled by default.</span></span>
    
      - <span data-ttu-id="84f11-135">[**同時呼び出し**] では、追加の電話機 (携帯電話など) や他のエンドポイント デバイスで、着信の呼び出し音を鳴らすことができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-135">**Simultaneous ringing** enables incoming calls to ring on additional phones (for example, a mobile phone) or other endpoint devices.</span></span> <span data-ttu-id="84f11-136">Lync Server 2013 では、同時呼び出しの構成オプションが大きく広がります。</span><span class="sxs-lookup"><span data-stu-id="84f11-136">Lync Server 2013 provides a significantly wider range of configuration options for simultaneous ringing.</span></span> <span data-ttu-id="84f11-137">既定では有効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-137">Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-138">[**チーム呼び出し**] では、定義したチームのユーザーがチームの他のメンバーの呼び出しに応答できます。</span><span class="sxs-lookup"><span data-stu-id="84f11-138">**Team call** enables users on a defined team to answer calls for other members of the team.</span></span> <span data-ttu-id="84f11-139">既定では有効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-139">Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-140">**Pstn の再ルーティング** では、WAN が混雑しているか利用できない場合は、このポリシーが割り当てられているユーザーによる電話による公衆交換電話網 (PSTN) の再ルーティングが可能になります。</span><span class="sxs-lookup"><span data-stu-id="84f11-140">**PSTN re-route** enables calls made by users who are assigned this policy to other enterprise users to be rerouted on the public switched telephone network (PSTN) if the WAN is congested or unavailable.</span></span> <span data-ttu-id="84f11-141">既定では有効になっています。</span><span class="sxs-lookup"><span data-stu-id="84f11-141">Enabled by default.</span></span>
    
      - <span data-ttu-id="84f11-142">**帯域幅ポリシー上書き** により、管理者は、特定のユーザーに対して通話受付制御 (CAC) ポリシーの決定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-142">**Bandwidth policy override** enables administrators to override call admission control (CAC) policy decisions for a particular user.</span></span> <span data-ttu-id="84f11-143">既定では無効です。</span><span class="sxs-lookup"><span data-stu-id="84f11-143">Disabled by default.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="84f11-p114">ポリシーが上書きされるのはユーザーに着信する通話のみです。ユーザーが発信する通話は上書きされません。セッションの確立後、使用帯域幅は正確に記録されます。この設定は慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-p114">The policy will be overridden only for incoming calls to the user and not for outgoing calls that are placed by the user. After the session is established, the bandwidth consumption will be accurately recorded. This setting should be used sparingly.</span></span>

        
        </div>
    
      - <span data-ttu-id="84f11-147">**悪意のある通話トレース** を使用すると、ユーザーはクライアント UI を使って悪意のある呼び出し (爆弾の脅威など) を報告することができます。これは、呼び出しの詳細レコード (CDRs) の呼び出しにフラグを付けます。</span><span class="sxs-lookup"><span data-stu-id="84f11-147">**Malicious call tracing** enables users to report malicious calls (such as bomb threats) using the client UI, which in turn flags the calls in the call detail records (CDRs).</span></span> <span data-ttu-id="84f11-148">既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="84f11-148">Disabled by default.</span></span>

7.  <span data-ttu-id="84f11-149">この音声ポリシーの PSTN 使用法レコードの関連付けと構成を行うには、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-149">To associate and configure PSTN usage records for this voice policy, do any of the following:</span></span>
    
      - <span data-ttu-id="84f11-p116">エンタープライズ VoIP 展開で利用できるすべての PSTN 使用法レコードの一覧から、1 つ以上のレコードを選択するには、[**選択**] をクリックします。この音声ポリシーに関連付けるレコードを選択状態にし、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-p116">To choose one or more records from a list of all PSTN usage records available in your Enterprise Voice deployment, click **Select**. Highlight the records that you want to associate with this voice policy, and then click **OK**.</span></span>
    
      - <span data-ttu-id="84f11-152">PSTN 使用法レコードをこの音声ポリシーから削除するには、レコードを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-152">To remove a PSTN usage record from this voice policy, highlight the record and click **Remove**.</span></span>
    
      - <span data-ttu-id="84f11-153">新しい PSTN 使用法レコードを定義してこの音声ポリシーに関連付けるには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-153">To define a new PSTN usage record and associate it with this voice policy, do the following:</span></span>
        
        1.  <span data-ttu-id="84f11-154">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-154">Click **New**.</span></span>
        
        2.  <span data-ttu-id="84f11-p117">"**名前**" フィールドに、レコードを説明する一意の名前を入力します。たとえば、Redmond で勤務しているフルタイム従業員用に **Redmond** という名前の PSTN 使用法レコードを作成し、パートタイム従業員用に **RedmondTemps** という別の名前の PSTN 使用法レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="84f11-p117">In the **Name** field, enter a unique descriptive name for the record. For example, you may want to create a PSTN usage record named **Redmond** for full-time employees located in Redmond, and another record named **RedmondTemps** for temporary employees.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="84f11-p118">PSTN 使用法レコードの名前は、エンタープライズ VoIP 展開内で一意である必要があります。レコードの保存後、"<STRONG>名前</STRONG>" フィールドを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="84f11-p118">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

            
            </div>
        
        3.  <span data-ttu-id="84f11-159">次のいずれかの方法を使用して、この PSTN 使用法レコードのルートの関連付けと構成を行います。</span><span class="sxs-lookup"><span data-stu-id="84f11-159">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="84f11-160">エンタープライズ VoIP 展開で利用できるすべてのルートの一覧から、1 つ以上のルートを選択するには、[**選択**] をクリックし、この PSTN 使用法レコードに関連付けるルートを選択状態にして、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-160">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
            
              - <span data-ttu-id="84f11-161">PSTN 使用法レコードからルートを削除するには、ルートを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-161">To remove a route from the PSTN usage record, highlight the route and click **Remove**.</span></span>
            
              - <span data-ttu-id="84f11-162">新しいルートを定義してこの PSTN 使用法レコードに関連付けるには、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-162">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="84f11-163">詳細については、「 [Lync Server 2013 での音声ルートの作成](lync-server-2013-create-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-163">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="84f11-164">この PSTN 使用法レコードに既に関連付けられているルートを編集するには、ルートを選択状態にして [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-164">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="84f11-165">詳細については、「 [Lync Server 2013 での音声ルートの変更](lync-server-2013-modify-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-165">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        4.  <span data-ttu-id="84f11-166">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-166">Click **OK**.</span></span>
    
      - <span data-ttu-id="84f11-167">この音声ポリシーに既に関連付けられている PSTN 使用法レコードを編集するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-167">To edit a PSTN usage record that is already associated with this voice policy, do the following:</span></span>
        
        1.  <span data-ttu-id="84f11-168">編集する PSTN 使用法レコードを選択状態にし、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-168">Highlight the PSTN usage record that you want to edit and click **Show details**.</span></span>
        
        2.  <span data-ttu-id="84f11-169">次のいずれかの方法を使用して、この PSTN 使用法レコードのルートの関連付けと構成を行います。</span><span class="sxs-lookup"><span data-stu-id="84f11-169">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="84f11-170">エンタープライズ VoIP 展開で利用できるすべてのルートの一覧から、1 つ以上のルートを選択するには、[**選択**] をクリックし、この PSTN 使用法レコードに関連付けるルートを選択状態にして、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-170">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
            
              - <span data-ttu-id="84f11-171">この PSTN 使用法レコードからルートを削除するには、ルートを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-171">To remove a route from this PSTN usage record, highlight the route and click **Remove**.</span></span>
            
              - <span data-ttu-id="84f11-172">新しいルートを定義してこの PSTN 使用法レコードに関連付けるには、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-172">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="84f11-173">詳細については、「 [Lync Server 2013 での音声ルートの作成](lync-server-2013-create-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-173">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="84f11-174">この PSTN 使用法レコードに既に関連付けられているルートを編集するには、ルートを選択状態にして [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-174">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="84f11-175">詳細については、「 [Lync Server 2013 での音声ルートの変更](lync-server-2013-modify-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-175">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        3.  <span data-ttu-id="84f11-176">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-176">Click **OK**.</span></span>

8.  <span data-ttu-id="84f11-p123">最適なパフォーマンスを得るために、PSTN 使用法レコードを並べ替えます。一覧内でのレコードの位置を変更するには、レコードの名前を選択状態にして、上矢印または下矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-p123">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, highlight the record name and click the up or down arrow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84f11-179">ボイスポリシーに表示される PSTN 使用状況レコードの順序は重要です。</span><span class="sxs-lookup"><span data-stu-id="84f11-179">The order in which PSTN usage records are listed in the voice policy is significant.</span></span> <span data-ttu-id="84f11-180">Lync Server は、一覧を上から下に移動します。</span><span class="sxs-lookup"><span data-stu-id="84f11-180">Lync Server traverses the list from the top down.</span></span> <span data-ttu-id="84f11-181">リストを使用頻度で整理することをお勧めします。例: RedmondLocal、RedmondLongDist、Redmondlocal、Redmondlocal。</span><span class="sxs-lookup"><span data-stu-id="84f11-181">We recommend that you organize the list by frequency of use, for example: RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span></span>

    
    </div>

9.  <span data-ttu-id="84f11-182">この音声ポリシーの着信転送および同時呼び出しの PSTN 使用法レコードの関連付けと構成を行うには、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-182">To associate and configure PSTN usage records for call forwarding and simultaneous ringing in this voice policy, do any of the following:</span></span>
    
      - <span data-ttu-id="84f11-183">この音声ポリシーのように着信の転送および同時呼び出しに対して同じ PSTN 使用法レコードを使用するには、ドロップダウン メニューから [**呼び出し PSTN 使用法を使用したルーティング**] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="84f11-183">To use the same PSTN usage records for call forwarding and simultaneous ringing as this voice policy, select the option **Route using the call PSTN usages** from the drop-down menu.</span></span>
    
      - <span data-ttu-id="84f11-184">着信の転送と同時呼び出しを内部の Lync ユーザーのみに許可するには、ドロップダウンメニューから [ **内部の lync ユーザーへのルーティングのみ** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="84f11-184">To allow call forwarding and simultaneous ringing to internal Lync users only, select **Route to internal Lync users only** from the drop-down menu.</span></span> <span data-ttu-id="84f11-185">Calls will not be forwarded to external PSTN numbers.</span><span class="sxs-lookup"><span data-stu-id="84f11-185">Calls will not be forwarded to external PSTN numbers.</span></span>
    
      - <span data-ttu-id="84f11-p126">この音声ポリシーに使用されているのとは別の PTSN 使用法レコードを着信の転送と同時呼び出しに指定する場合は、ドロップダウン メニューから [**カスタムの PSTN 使用法を使用したルーティング**] を選択します。このオプションを選択するとコントロールが表示され、着信の転送と同時呼び出しに対して、既存の PSTN 使用法レコードを選択するかまたは新しい PSTN 使用法レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="84f11-p126">To specify different PSTN usage records for call forwarding and simultaneous ringing than those used for this voice policy, select the option **Route using custom PSTN usages** from the drop-down menu. This option displays a control to select existing PSTN usage records or to create new PSTN usage records, specifically for call forwarding and simultaneous ringing.</span></span>
        
          - <span data-ttu-id="84f11-p127">着信の転送および同時呼び出しの PSTN 使用法レコードの一覧から、1 つ以上のレコードを選択するには、[**選択**] をクリックします。この着信の転送および同時呼び出しポリシーに関連付けるレコードを選択状態にし、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-p127">To choose one or more records from a list of PSTN usage records for call forwarding and simultaneous ringing, click **Select**. Highlight the records that you want to associate with this call forwarding and simultaneous ringing policy, and then click **OK**.</span></span>
        
          - <span data-ttu-id="84f11-190">PSTN 使用法レコードをこの着信の転送および同時呼び出しポリシーから削除するには、レコードを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-190">To remove a PSTN usage record from this call forwarding and simultaneous ringing policy, highlight the record and click **Remove**.</span></span>
        
          - <span data-ttu-id="84f11-191">新しい PSTN 使用法レコードを定義してこの着信の転送および同時呼び出しポリシーに関連付けるには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-191">To define a new PSTN usage record and associate it with this call forwarding and simultaneous ringing policy, do the following:</span></span>
            
            1.  <span data-ttu-id="84f11-192">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-192">Click **New**.</span></span>
            
            2.  <span data-ttu-id="84f11-193">"**名前**" フィールドに、レコードを説明する一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="84f11-193">In the **Name** field, enter a unique descriptive name for the record.</span></span>
                
                <div>
                

                > [!NOTE]  
                > <span data-ttu-id="84f11-p128">PSTN 使用法レコードの名前は、エンタープライズ VoIP 展開内で一意である必要があります。レコードの保存後、"<STRONG>名前</STRONG>" フィールドを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="84f11-p128">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

                
                </div>
            
            3.  <span data-ttu-id="84f11-196">次のいずれかの方法を使用して、この PSTN 使用法レコードのルートの関連付けと構成を行います。</span><span class="sxs-lookup"><span data-stu-id="84f11-196">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
                
                  - <span data-ttu-id="84f11-197">エンタープライズ VoIP 展開で利用できるすべてのルートの一覧から、1 つ以上のルートを選択するには、[**選択**] をクリックし、この PSTN 使用法レコードに関連付けるルートを選択状態にして、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-197">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
                
                  - <span data-ttu-id="84f11-198">PSTN 使用法レコードからルートを削除するには、ルートを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-198">To remove a route from the PSTN usage record, highlight the route and click **Remove**.</span></span>
                
                  - <span data-ttu-id="84f11-199">新しいルートを定義してこの PSTN 使用法レコードに関連付けるには、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-199">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="84f11-200">詳細については、「 [Lync Server 2013 での音声ルートの作成](lync-server-2013-create-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-200">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
                
                  - <span data-ttu-id="84f11-201">この PSTN 使用法レコードに既に関連付けられているルートを編集するには、ルートを選択状態にして [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-201">To edit a route that is already associated with this PSTN usage record, highlight the route, and then click **Show details**.</span></span> <span data-ttu-id="84f11-202">詳細については、「 [Lync Server 2013 での音声ルートの変更](lync-server-2013-modify-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-202">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
            
            4.  <span data-ttu-id="84f11-203">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-203">Click **OK**.</span></span>
        
          - <span data-ttu-id="84f11-204">この音声ポリシーに既に関連付けられている PSTN 使用法レコードを編集するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="84f11-204">To edit a PSTN usage record that is already associated with this voice policy, do the following:</span></span>
            
            1.  <span data-ttu-id="84f11-205">編集する PSTN 使用法レコードを選択状態にし、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-205">Highlight the PSTN usage record that you want to edit and click **Show details**.</span></span>
            
            2.  <span data-ttu-id="84f11-206">次のいずれかの方法を使用して、この PSTN 使用法レコードのルートの関連付けと構成を行います。</span><span class="sxs-lookup"><span data-stu-id="84f11-206">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
                
                  - <span data-ttu-id="84f11-207">エンタープライズ VoIP 展開で利用できるすべてのルートの一覧から、1 つ以上のルートを選択するには、[**選択**] をクリックし、この PSTN 使用法レコードに関連付けるルートを選択状態にして、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-207">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes you want to associate with this PSTN usage record, and then click **OK**.</span></span>
                
                  - <span data-ttu-id="84f11-208">この PSTN 使用法レコードからルートを削除するには、ルートを選択状態にして [**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-208">To remove a route from this PSTN usage record, highlight the route and click **Remove**.</span></span>
                
                  - <span data-ttu-id="84f11-209">新しいルートを定義してこの PSTN 使用法レコードに関連付けるには、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-209">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="84f11-210">詳細については、「 [Lync Server 2013 での音声ルートの作成](lync-server-2013-create-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-210">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
                
                  - <span data-ttu-id="84f11-211">この PSTN 使用法レコードに既に関連付けられているルートを編集するには、ルートを選択状態にして [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-211">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="84f11-212">詳細については、「 [Lync Server 2013 での音声ルートの変更](lync-server-2013-modify-a-voice-route.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-212">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
            
            3.  <span data-ttu-id="84f11-213">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-213">Click **OK**.</span></span>

10. <span data-ttu-id="84f11-p133">(オプション) 音声ポリシーをテストする番号を入力して、[**実行**] をクリックします。テスト結果は、[**テストする変換後の番号**] の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="84f11-p133">(Optional) Enter a number to test the voice policy and click **Go**. The test results are displayed under **Translated number to test**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84f11-216">まだテストに合格しない音声ポリシーを保存し、後で再構成することができます。</span><span class="sxs-lookup"><span data-stu-id="84f11-216">You can save a voice policy that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="84f11-217">詳細については、「 <A href="lync-server-2013-test-voice-routing.md">Lync Server 2013 での音声ルーティングのテスト</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-217">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

11. <span data-ttu-id="84f11-218">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-218">Click **OK**.</span></span>

12. <span data-ttu-id="84f11-219">[**音声ポリシー**] ページで [**確定**] をクリックし、[**すべて確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84f11-219">On the **Voice Policy** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84f11-220">音声ポリシーを作成または変更するときは常に、[<STRONG>すべて確定</STRONG>] コマンドを実行して、構成の変更を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84f11-220">Whenever you create or modify a voice policy, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="84f11-221">詳細については、「操作のドキュメントで「 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 のボイスルーティング構成に保留中の変更を発行する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-221">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

13. <span data-ttu-id="84f11-222">(オプション) ボイスメール エスケープは、着信がユーザーの携帯電話のボイス メールによって即座に応答されたことを検出し、携帯電話のボイス メールへの通話を切断します。</span><span class="sxs-lookup"><span data-stu-id="84f11-222">(Optional) Voicemail Escape detects that a call was immediately answered by the user’s mobile phone voice mail, and disconnects the call to the mobile phone voice mail.</span></span> <span data-ttu-id="84f11-223">これにより、ユーザーの他のエンドポイントで着信の呼び出しが続けられるので、ユーザーは着信に応答できるようになります。</span><span class="sxs-lookup"><span data-stu-id="84f11-223">This allows the call to continue to ring on the user’s other endpoints giving the user the opportunity to answer the call.</span></span> <span data-ttu-id="84f11-224">ボイスメールのポリシーを構成する方法の詳細については、「 [Lync Server 2013 でボイスメールのエスケープを構成](lync-server-2013-configuring-voice-mail-escape.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84f11-224">For details about how to configure a voice mail policy, see [Configuring voice mail escape in Lync Server 2013](lync-server-2013-configuring-voice-mail-escape.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="84f11-225">関連項目</span><span class="sxs-lookup"><span data-stu-id="84f11-225">See Also</span></span>


[<span data-ttu-id="84f11-226">Lync Server 2013 で音声ポリシーを作成し、PSTN 使用状況レコードを構成する</span><span class="sxs-lookup"><span data-stu-id="84f11-226">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="84f11-227">Lync Server 2013 での PSTN 使用状況レコードの表示</span><span class="sxs-lookup"><span data-stu-id="84f11-227">View PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-view-pstn-usage-records.md)  
[<span data-ttu-id="84f11-228">Lync Server 2013 での音声ルートの作成</span><span class="sxs-lookup"><span data-stu-id="84f11-228">Create a voice route in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-route.md)  
[<span data-ttu-id="84f11-229">Lync Server 2013 での音声ルートの変更</span><span class="sxs-lookup"><span data-stu-id="84f11-229">Modify a voice route in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-route.md)  
[<span data-ttu-id="84f11-230">Lync Server 2013 の音声ルーティング構成に保留中の変更を発行する</span><span class="sxs-lookup"><span data-stu-id="84f11-230">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  
[<span data-ttu-id="84f11-231">Lync Server 2013 でボイスメールのエスケープを構成する</span><span class="sxs-lookup"><span data-stu-id="84f11-231">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)  


[<span data-ttu-id="84f11-232">Lync Server 2013 での音声ルーティングのテスト</span><span class="sxs-lookup"><span data-stu-id="84f11-232">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="84f11-233"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84f11-233"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

