---
title: 'Lync Server 2013: ハントグループワークフローを作成または変更する'
description: 'Lync Server 2013: ハントグループのワークフローを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a hunt group workflow
ms:assetid: dcb9effb-5d12-4dee-80fc-ab9654222d5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205321(v=OCS.15)
ms:contentKeyID: 48185596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95f6374352c87d13b1e5c09bcef267059016eae0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431835"
---
# <a name="create-or-modify-a-hunt-group-workflow-in-lync-server-2013"></a><span data-ttu-id="9d46b-103">Lync Server 2013 でハントグループワークフローを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="9d46b-103">Create or modify a hunt group workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d46b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d46b-104">

<span> </span></span></span>

<span data-ttu-id="9d46b-105">_**最終更新日:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="9d46b-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="9d46b-106">ハントグループワークフローを作成または変更するには、次のいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-106">Use one of the following procedures to create or modify a hunt group workflow.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9d46b-107">Lync Server 管理シェルまたは応答グループ構成ツールを使用して、ハントグループワークフローを作成し、変更することができます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-107">You can use Lync Server Management Shell or the Response Group Configuration Tool to create and modify hunt group workflows.</span></span> <span data-ttu-id="9d46b-108">Lync Server コントロールパネルから応答グループの構成ツールにアクセスするか、次の URL を入力して web ブラウザーから直接 web ページを開く ( <STRONG>Https://</STRONG> &lt; webpoolfqdn/RgsConfig) ことができ &gt; <STRONG>/RgsConfig</STRONG>ます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-108">You can access the Response Group Configuration Tool from Lync Server Control Panel, or by opening the webpage directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>



</div>

<div>

## <a name="to-use-response-group-configuration-tool-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="9d46b-109">応答グループの構成ツールを使用して、ハントグループのワークフローを作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="9d46b-109">To use Response Group Configuration Tool to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="9d46b-110">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-110">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="9d46b-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9d46b-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9d46b-113">左側のナビゲーション バーで、[**応答グループ**] をクリックし、[**ワークフロー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-113">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="9d46b-114">[**ワークフロー**] ページで、[**ワークフローの作成または編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-114">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="9d46b-115">[**サービスの選択**] 検索フィールドに、作成または変更するワークフローをホストする **ApplicationServer** サービスの名前の全体または一部を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-115">In the **Select a Service** search field, type all or part of the name of the **ApplicationServer** service that hosts the workflow that you want to create or change.</span></span> <span data-ttu-id="9d46b-116">サービスの結果一覧で、対象のサービスをクリックして [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-117">応答グループ構成ツールが開きます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-117">The Response Group Configuration Tool opens.</span></span> <span data-ttu-id="9d46b-118">次の URL を入力して、web ブラウザーから直接応答グループ構成ツールを開くこともできます。 <STRONG>Https://</STRONG> &lt; webpoolfqdn &gt; <STRONG>/RgsConfig</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="9d46b-118">You can also open the Response Group Configuration Tool directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="9d46b-119">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9d46b-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-120">[**新規ワークフローの作成**] で、[**ハント グループ**] の横にある [作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-120">Under **Create a New Workflow**, next to **Hunt Group, click Create**.</span></span>
    
      - <span data-ttu-id="9d46b-121">[**既存ワークフローの管理**] で変更するワークフローを見つけて、[**アクション**] の [**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-121">Under **Manage an Existing Workflow**, locate the workflow you want to change, and then under **Action**, click **Edit**.</span></span>

7.  <span data-ttu-id="9d46b-122">ユーザーがワークフローへの通話を開始する準備ができている場合は、[**ワークフローのアクティブ化**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-122">If you are ready for users to start calling the workflow, select **Activate the workflow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-p105">管理ワークフローを作成する場合は、[<STRONG>ワークフローのアクティブ化</STRONG>] を選択する必要があります。アクティブな管理ワークフローを保存した後、そのワークフローを変更したり、非アクティブ化したりできます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p105">If you are to creating a managed workflow, you need to select <STRONG>Activate the workflow</STRONG>. After you save the active, managed workflow, you can then modify and deactivate it.</span></span>

    
    </div>

8.  <span data-ttu-id="9d46b-125">フェデレーション ユーザーにグループへの通話を許可するには、[**フェデレーションを有効にする**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-125">To allow federated users to call the group, select the **Enable for federation** check box.</span></span> <span data-ttu-id="9d46b-126">フェデレーション用に構成された応答グループアプリケーションに適用される外部アクセスポリシーも必要です。</span><span class="sxs-lookup"><span data-stu-id="9d46b-126">You must also have an external access policy that applies to the Response Group application configured for federation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-127">グローバル外部アクセスポリシーは、応答グループアプリケーションに適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-127">The global external access policy applies to the Response Group application.</span></span> <span data-ttu-id="9d46b-128">Lync Server コントロールパネルを使用するか、 <STRONG>CsExternalAccessPolicy</STRONG> コマンドレットを使用して EnableOutsideAccess パラメーターを True に設定することによって、応答グループのフェデレーションのグローバルポリシーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-128">You can configure the global policy for response group federation by using Lync Server Control Panel or by using the <STRONG>Set-CsExternalAccessPolicy</STRONG> cmdlet to set the EnableOutsideAccess parameter to True.</span></span> <span data-ttu-id="9d46b-129">グローバル ポリシー設定は、サイトやユーザー ポリシーに割り当てられていない限り、すべてのユーザーに適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-129">Keep in mind that global policy settings apply to all users unless they are assigned a site or user policy.</span></span> <span data-ttu-id="9d46b-130">そのため、応答グループ向けにこの設定を変更する前に、フェデレーション設定が組織の要件を満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-130">Therefore, before changing this setting for response groups, make sure that the federation setting meets the requirements of your organization.</span></span> <span data-ttu-id="9d46b-131">ポリシーがユーザーに適用される方法の詳細については、「 <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Lync Server 2013 で外部アクセスポリシーを管理</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-131">For details about how policies apply to users, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span> <span data-ttu-id="9d46b-132">フェデレーション設定の詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">Set-CsExternalAccessPolicy</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-132">For details about the federation setting, see <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">Set-CsExternalAccessPolicy</A>.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-133">Lync Online でホストされているユーザーは、オンプレミスの展開でホストされている応答グループに通話を発信することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d46b-133">Users who are hosted in Lync Online can’t place calls to response groups that are hosted in an on-premise deployment.</span></span> <span data-ttu-id="9d46b-134">これは、ハイブリッド展開と、オンプレミスの展開が Lync Online 展開とフェデレーションされている場合に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-134">This is true in both hybrid deployments and in cases where an on-premise deployment is federated with a Lync Online deployment.</span></span>

    
    </div>

9.  <span data-ttu-id="9d46b-135">通話中、エージェントの ID を非表示にするには、[**エージェントの匿名性を有効にする**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-135">To hide the identity of agents during calls, select the **Enable agent anonymity** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-p109">匿名の通話は、インスタント メッセージング (IM) やビデオから開始することはできません。ただし、通話の確立後、エージェントまたは発信者が IM やビデオを追加することはできます。匿名のエージェントは、通話の保留、通話の転送 (無条件転送と取次転送)、および通話の保留と保留解除を行うこともできます。匿名の通話では、会議、アプリケーション共有とデスクトップ共有、ファイル転送、ホワイトボードとデータのグループ作業、および通話の記録はサポートされません。Lync VDI プラグインを使用するエージェントは、着信通話を匿名で受信できますが、発信通話を匿名で行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p109">Anonymous calls cannot start with instant messaging (IM) or video, although the agent or the caller can add IM and video after the call is established. An anonymous agent can also put calls on hold, transfer calls (both blind and consultative transfers), and park and retrieve calls. Anonymous calls do not support conferencing, application sharing and desktop sharing, file transfer, whiteboarding and data collaboration, and call recording. Agents using the Lync VDI Plugin can receive incoming calls anonymously, but they cannot make outgoing calls anonymously.</span></span>

    
    </div>

10. <span data-ttu-id="9d46b-140">[**通話を受けるグループのアドレスを入力します**] に、ワークフローへの通話に応答するグループのプライマリ SIP Uniform Resource Identifier (URI) アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-140">Under **Enter the address of the group that will receive the calls**, type the primary SIP uniform resource identifier (URI) address of the group that will answer calls to the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-141">ワークフローのプライマリ URI は、ワークフローをどのように識別および参照するかを表します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-141">The primary URI for a workflow is how the workflow is identified and referenced.</span></span> <span data-ttu-id="9d46b-142">入力した SIP URI は、Active Directory ドメインサービスで連絡先オブジェクトとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-142">The SIP URI that you enter is created as a contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="9d46b-143">URI を作成するには、オブジェクトが Active Directory 内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-143">To create the URI, the object must be unique in Active Directory.</span></span>

    
    </div>

11. <span data-ttu-id="9d46b-144">[ **表示名**] に、ワークフローに対して表示する名前を入力します (たとえば、[売上高応答] グループ)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-144">In **Display name**, type the name that you want to display for the workflow (for example, Sales Response Group).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-145">&lt;表示名に "" または "" という文字を含めないでください &gt; 。</span><span class="sxs-lookup"><span data-stu-id="9d46b-145">Do not include the "&lt;" or "&gt;" characters in the display name.</span></span> <span data-ttu-id="9d46b-146">以下の表示名は、予約されているため使用しないでください。 <STRONG>Rg プレゼンスウォッチャー</STRONG> または <STRONG>お知らせサービス</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="9d46b-146">Do not use the following display names because they are reserved: <STRONG>RGS Presence Watcher</STRONG> or <STRONG>Announcement Service</STRONG>.</span></span>

    
    </div>

12. <span data-ttu-id="9d46b-147">[**電話番号**] に、応答グループの回線 URI を入力します (入力例 +14255550165)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-147">Under **Telephone number**, type the line URI for the response group (for example, +14255550165).</span></span>

13. <span data-ttu-id="9d46b-148">[**表示番号**] に、応答グループに対して表示する番号を入力します (入力例 +1 (425) 555-0165)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-148">In **Display number**, type the number as you want it to appear for the response group (for example, +1 (425) 555-0165).</span></span>

14. <span data-ttu-id="9d46b-149">省略[ **説明**] に、Lync クライアントの連絡先カードに表示するワークフローの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-149">(Optional) In **Description**, type a description for the workflow as you want it to appear on the contact card in Lync client.</span></span>

15. <span data-ttu-id="9d46b-150">このワークフローを応答グループのマネージャーが管理する場合は、[**ワークフローの種類**] で [**管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-150">In **Workflow Type**, select **Managed** if this workflow will be managed by a Response Group Manager.</span></span> <span data-ttu-id="9d46b-151">応答グループマネージャーをワークフローに割り当てるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-151">Do the following to assign Response Group Managers to the workflow:</span></span>
    
    1.  <span data-ttu-id="9d46b-152">このワークフローのマネージャーの SIP URI を入力して、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-152">Type the SIP URI of a manager for this workflow, and click **Add**.</span></span>
    
    2.  <span data-ttu-id="9d46b-153">ワークフローに追加するマネージャーの SIP URI を入力して、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-153">Type the SIP URI of additional managers to add to the workflow, and click **Add**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9d46b-p113">応答グループのマネージャーに指定されているすべてのユーザーに CsResponseGroupManager ロールを割り当てる必要があります。このロールが割り当てられていない場合、ユーザーは応答グループを管理できません。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p113">Every user who is designated as a manager of a response group must be assigned the CsResponseGroupManager role. If users are not assigned this role, they cannot manage response groups.</span></span>

    
    </div>

16. <span data-ttu-id="9d46b-156">[**ステップ 2 言語の選択**] で、音声認識と音声合成で使用する言語をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-156">Under **Step 2 Select a Language**, click the language that you want to use for speech recognition and text-to-speech.</span></span>

17. <span data-ttu-id="9d46b-157">開始メッセージを構成する場合は、[**ステップ 3 開始メッセージの構成**] で [**開始メッセージを再生する**] チェック ボックスをオンにして、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9d46b-157">If you want to configure a welcome message, under **Step 3 Configure a Welcome Message**, select the **Play a welcome message** check box, and then do one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-158">発信者用の音声に変換される開始メッセージをテキストとして入力するには、[**音声合成を使用する**] をクリックして、テキスト ボックスに開始メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-158">To enter the welcome message as text that is converted to speech for callers, click **Use text-to-speech**, and then type the welcome message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-p114">入力するテキストに HTML タグを含めないでください。HTML タグを含めると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p114">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="9d46b-p115">開始メッセージに Wave (.wav) または Windows Media オーディオ (.wma) ファイルの録音を使用するには、[**録音を選択する**] をクリックします。新しいオーディオ ファイルをアップロードする場合は、[**録音**] リンクをクリックしてください。新しいブラウザー ウィンドウで [**参照**] をクリックし、使用するオーディオ ファイルを選択して、[**開く**] をクリックします。[**アップロード**] をクリックしてオーディオ ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p115">To use a wave (.wav) or Windows Media audio (.wma) file recording for the welcome message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the audio file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-165">ユーザーが指定したすべてのオーディオ ファイルは、特定の要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-165">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="9d46b-166">サポートされているファイル形式の詳細については、「 <A href="lync-server-2013-technical-requirements-for-response-group.md">Lync Server 2013 の「回答グループの技術要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-166">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

18. <span data-ttu-id="9d46b-167">[**ステップ 4 営業時間の指定**] の [**タイム ゾーン**] で、ワークフローのタイム ゾーンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-167">Under **Step 4 Specify Your Business Hours**, in **Your time zone**, click the time zone for the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-p117">このタイム ゾーンは、ワークフローの発信者とエージェントの所在地のタイム ゾーンです。これを使用して、始業時間と終業時間が計算されます。たとえば、北アメリカ東部標準時を使用するようにワークフローが構成されており、ワークフローで始業が午前 7:00、終業が午後 11:00 にスケジュールされている場合は、東部標準時の 7:00 と 23:00 がそれぞれ始業時刻と終業時刻になります (時間は 24 時間表記で入力する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p117">The time zone is the time zone where the callers and agents of the workflow reside. It is used to calculate the open and close hours. For example, if the workflow is configured to use the North American Eastern Time zone and the workflow is scheduled to open at 7:00 A.M. and close at 11:00 P.M., the open and close times are assumed to be 7:00 Eastern Time and 23:00 Eastern Time respectively. (You must enter the times in 24-hour time notation.)</span></span>

    
    </div>

19. <span data-ttu-id="9d46b-173">次のいずれかの操作を実行して、使用する営業時間スケジュールの種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-173">Select the type of business hours schedule you want to use by doing one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-174">事前に定義した営業時間スケジュールを使用するには、[**プリセット スケジュールを使用する**] をクリックして、ドロップダウン リストから使用するスケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-174">To use a predefined schedule of business hours, click **Use a preset schedule**, and then select the schedule you want to use from the drop-down list.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-175">このオプションを選択できるようにするには、あらかじめ少なくとも 1 つのプリセット スケジュールを定義しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-175">You must have defined at least one preset schedule previously to be able to select this option.</span></span> <span data-ttu-id="9d46b-176"><STRONG>New-CSRgsHoursOfBusiness</STRONG> コマンドレットを使用してプリセット スケジュールを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-176">You define preset schedules by using the <STRONG>New-CSRgsHoursOfBusiness</STRONG> cmdlet.</span></span> <span data-ttu-id="9d46b-177">詳細については、「 <A href="lync-server-2013-optional-define-response-group-business-hours.md">(オプション) Lync Server 2013 で回答グループの営業時間を定義</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-177">For details, see <A href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</A>.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-178">プリセット スケジュールを選択すると、応答グループの対応日時で、[<STRONG>曜日</STRONG>]、[<STRONG>開始</STRONG>]、[<STRONG>終了</STRONG>] が自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-178">When you select a preset schedule, <STRONG>Day</STRONG>, <STRONG>Open</STRONG>, and <STRONG>Close</STRONG> are automatically filled with the days and hours that the response group is available.</span></span>

        
        </div>
    
      - <span data-ttu-id="9d46b-179">このワークフローのみに適用するカスタム スケジュールを使用するには、[**カスタム スケジュールを使用する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-179">To use a custom schedule that applies only to this workflow, click **Use a custom schedule**.</span></span>

20. <span data-ttu-id="9d46b-180">このワークフロー用のカスタム スケジュールを作成する場合は、応答グループが対応可能な曜日のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-180">If you are creating a custom schedule for this workflow, click the check boxes for the days of the week that the response group is available.</span></span>

21. <span data-ttu-id="9d46b-181">カスタム スケジュールを作成する場合は、応答グループが対応可能な各曜日の [**開始**] 時間と [**終了**] 時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-181">If you are creating a custom schedule, type the **Open** and **Close** hours for each day of the week that the response group available.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-p119">[<STRONG>開始</STRONG>] 時間と [<STRONG>終了</STRONG>] 時間は 24 時間表記で入力する必要があります。たとえば、職場の営業時間が営業日の 9 時から 5 時までで、昼休みのために正午にオフィスを一度閉める場合、営業時間は [<STRONG>開始</STRONG>] 9:00、[<STRONG>終了</STRONG>] 12:00、[<STRONG>開始</STRONG>] 13:00、[<STRONG>終了</STRONG>] 17:00 として指定します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p119">The <STRONG>Open</STRONG> and <STRONG>Close</STRONG> hours must be in 24-hour time notation. For example, if your office works a 9-to-5 work day and closes at noon for lunch, the business hours are specified as <STRONG>Open</STRONG> 9:00, <STRONG>Close</STRONG> 12:00, <STRONG>Open</STRONG> 13:00, and <STRONG>Close</STRONG> 17:00.</span></span>

    
    </div>

22. <span data-ttu-id="9d46b-184">営業時間外にメッセージを再生するには、[**応答グループの営業時間外にメッセージを再生する**] チェック ボックスをオンにしてから、次のいずれかの操作を実行して再生するメッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-184">If you want to play a message when the office is not open, select the **Play a message when the response group is outside of business hours** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-185">発信者用に音声に変換されるメッセージをテキストとして入力するには、[**音声合成を使用する**] をクリックして、テキスト ボックスにメッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-185">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-p120">入力するテキストに HTML タグを含めないでください。HTML タグを含めると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p120">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="9d46b-p121">メッセージにオーディオ ファイルの録音を使用するには、[**録音を選択する**] をクリックします。新しいオーディオ ファイルをアップロードする場合は、[**録音**] リンクをクリックしてください。新しいブラウザー ウィンドウで [**参照**] をクリックし、使用するファイルを選択して、[**開く**] をクリックします。[**アップロード**] をクリックしてオーディオ ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p121">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-192">ユーザーが指定したすべてのオーディオ ファイルは、特定の要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-192">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="9d46b-193">サポートされているオーディオファイル形式の詳細については、「 <A href="lync-server-2013-technical-requirements-for-response-group.md">Lync Server 2013 の「応答グループの技術要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-193">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

23. <span data-ttu-id="9d46b-194">メッセージが構成されている場合は、メッセージ再生後の通話の処理方法を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-194">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="9d46b-195">通話を終了するには、[**終話**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-195">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="9d46b-196">通話をボイス メールに転送するには、[**ボイス メールに転送**] をクリックして、ボイス メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-196">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="9d46b-197">ボイスメールのアドレスの形式 \<username\> @ \<domainName\> (たとえば、bob@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-197">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="9d46b-198">通話を別のユーザーに転送するには、[**SIP URI に転送**] をクリックして、ユーザー アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-198">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="9d46b-199">ユーザーアドレスの形式は \<username\> @ \<domainName\> です。</span><span class="sxs-lookup"><span data-stu-id="9d46b-199">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="9d46b-200">通話を別の電話番号に転送するには、[**電話番号に転送**] をクリックして、電話番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-200">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="9d46b-201">電話番号の形式 \<number\> @ \<domainName\> (+ 14255550121@contoso.com など)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-201">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="9d46b-202">発信者は、ドメイン名を使用して適切な宛先にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-202">The domain name is used to route the caller to the correct destination.</span></span>

24. <span data-ttu-id="9d46b-203">[**ステップ 5 休日の指定**] で、応答グループが営業しない日を定義する、1 つまたは複数の休日セットのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-203">Under **Step 5 Specify Your Holidays**, click the check boxes for one or more sets of holidays that define the days when the response group is closed for business.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-204">ワークフローを構成する前に、休日および休日セットを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-204">You need to define holidays and holiday sets before you configure the workflow.</span></span> <span data-ttu-id="9d46b-205">休日および休日セットを定義するには、<STRONG>New-CsRgsHoliday</STRONG> コマンドレットおよび <STRONG>New-CsRgsHolidaySet</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-205">Use the <STRONG>New-CsRgsHoliday</STRONG> and <STRONG>New-CsRgsHolidaySet</STRONG> cmdlets to define holidays and holiday sets.</span></span> <span data-ttu-id="9d46b-206">詳細については、「 <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(オプション) Lync Server 2013 で応答グループの休日セットを定義</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-206">For details, see <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</A>.</span></span>

    
    </div>

25. <span data-ttu-id="9d46b-207">休日にメッセージを再生するには、[**休日にメッセージを再生する**] チェック ボックスをオンにしてから、次のいずれかの操作を実行して再生するメッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-207">If you want to play a message on holidays, select the **Play a message during holidays** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-208">発信者用に音声に変換されるメッセージをテキストとして入力するには、[**音声合成を使用する**] をクリックして、テキスト ボックスにメッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-208">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-p127">入力するテキストに HTML タグを含めないでください。HTML タグを含めると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p127">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="9d46b-p128">メッセージにオーディオ ファイルの録音を使用するには、[**録音を選択する**] をクリックします。新しいオーディオ ファイルをアップロードする場合は、[**録音**] リンクをクリックしてください。新しいブラウザー ウィンドウで [**参照**] をクリックし、使用するファイルを選択して、[**開く**] をクリックします。[**アップロード**] をクリックしてオーディオ ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p128">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-215">ユーザーが指定したすべてのオーディオ ファイルは、特定の要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-215">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="9d46b-216">サポートされているオーディオファイル形式の詳細については、「 <A href="lync-server-2013-technical-requirements-for-response-group.md">Lync Server 2013 の「応答グループの技術要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-216">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

26. <span data-ttu-id="9d46b-217">メッセージが構成されている場合は、メッセージ再生後の通話の処理方法を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-217">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="9d46b-218">通話を終了するには、[**終話**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-218">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="9d46b-219">通話をボイス メールに転送するには、[**ボイス メールに転送**] をクリックして、ボイス メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-219">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="9d46b-220">ボイスメールのアドレスの形式 \<username\> @ \<domainName\> (たとえば、bob@contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-220">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="9d46b-221">通話を別のユーザーに転送するには、[**SIP URI に転送**] をクリックして、ユーザー アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-221">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="9d46b-222">ユーザーアドレスの形式は \<username\> @ \<domainName\> です。</span><span class="sxs-lookup"><span data-stu-id="9d46b-222">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="9d46b-223">通話を別の電話番号に転送するには、[**電話番号に転送**] をクリックして、電話番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-223">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="9d46b-224">電話番号の形式 \<number\> @ \<domainName\> (+ 14255550121@contoso.com など)。</span><span class="sxs-lookup"><span data-stu-id="9d46b-224">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="9d46b-225">発信者は、ドメイン名を使用して適切な宛先にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-225">The domain name is used to route the caller to the correct destination.</span></span>

27. <span data-ttu-id="9d46b-226">[**ステップ 6 キューの構成**] の [**通話を受け取るキューを選択します**] で、エージェントが応答可能になるまで発信者を保留するキューを選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-226">Under **Step 6 Configure a Queue**, in **Select the queue that will receive the calls**, select the queue that you want to hold callers until an agent becomes available.</span></span>

28. <span data-ttu-id="9d46b-227">[**ステップ 7 保留音の構成**] で次のいずれかの操作を実行して、発信者がエージェントの応答を待機しているときの保留音を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-227">Under **Step 7 Configure Music on Hold**, choose the music you want callers to listen to while waiting for an agent by doing one of the following:</span></span>
    
      - <span data-ttu-id="9d46b-228">既定の保留音の録音を使用するには、[**既定値を使用する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-228">To use the default music-on-hold recording, click **Use default**.</span></span>
    
      - <span data-ttu-id="9d46b-p133">保留音にオーディオ ファイルの録音を使用するには、[**音楽ファイルを選択する**] をクリックします。新しいオーディオ ファイルをアップロードする場合は、[**音楽ファイル**] リンクをクリックします。新しいブラウザー ウィンドウで [**参照**] をクリックし、使用するファイルを選択して、[**開く**] をクリックします。[**アップロード**] をクリックしてオーディオ ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p133">To use an audio file recording for the music on hold, click **Select a music file**. If you want to upload a new audio file, click the **a music file** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9d46b-233">ユーザーが指定したすべてのオーディオ ファイルは、特定の要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-233">All user provided audio files must meet certain requirements.</span></span> <span data-ttu-id="9d46b-234">サポートされているオーディオファイル形式の詳細については、「 <A href="lync-server-2013-technical-requirements-for-response-group.md">Lync Server 2013 の「応答グループの技術要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-234">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

29. <span data-ttu-id="9d46b-235">[**展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-235">Click **Deploy**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="9d46b-236">Windows PowerShell を使用してハントグループのワークフローを作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="9d46b-236">To use Windows PowerShell to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="9d46b-237">RTCUniversalServerAdmins グループのメンバーまたは応答グループをサポートする定義済みの管理者の役割のいずれかのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-237">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="9d46b-238">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d46b-238">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="9d46b-p135">開始メッセージで再生されるプロンプトを作成し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p135">Create the prompt to be played for the welcome message, and save it in a variable. At the command line, run:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="9d46b-241">例:</span><span class="sxs-lookup"><span data-stu-id="9d46b-241">For example:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "Welcome to Contoso. Please wait for an available agent."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-242">プロンプトにオーディオ ファイルを使用するには、 <STRONG>Import-CsRgsAudioFile</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-242">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="9d46b-243">詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">インポート-CsRgsAudioFile</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-243">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="9d46b-244">通話が転送されることになるキューまたは質問の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-244">Get the identity of the queue or question where the calls will be directed.</span></span> <span data-ttu-id="9d46b-245">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-245">At the command line, run:</span></span>
    
        $qid = (Get-CsRgsQueue -Name "Help Desk").Identity
    
    <span data-ttu-id="9d46b-246">キューの作成の詳細については、「 [新しい-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-246">For details about creating the queue, see [New-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue).</span></span>

5.  <span data-ttu-id="9d46b-p138">営業時間中にワークフローを開いたときに実行される既定のアクションを定義し、変数に格納します。コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p138">Define the default action to be taken when a workflow is opened during business hours, and save it in a variable. At the command line, run:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken> -QueueID $qid
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-p139">ハント グループ ワークフローでは、既定のアクションにより通話がキューに転送される必要があります。アクティブなワークフローでは、このパラメーターが必要です。非アクティブなワークフローでは不要です。</span><span class="sxs-lookup"><span data-stu-id="9d46b-p139">For hunt group workflows, the default action must direct the call to a queue. This is parameter is required for active workflows. It is not required for inactive workflows.</span></span>

    
    </div>
    
    <span data-ttu-id="9d46b-252">例:</span><span class="sxs-lookup"><span data-stu-id="9d46b-252">For example:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt $promptWM -Action TransferToQueue -QueueID $qid.Identity

6.  <span data-ttu-id="9d46b-253">営業時間と休日を定義する場合は、ワークフローを作成または変更する前に、営業時間と休日を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-253">If you want to define business hours and holidays, you need to create them before you create or modify the workflow.</span></span> <span data-ttu-id="9d46b-254">詳細については、「 [(オプション) Lync server 2013 で回答グループの業務時間を定義](lync-server-2013-optional-define-response-group-business-hours.md) する」を参照してください。 [lync Server 2013 で応答グループの休日セットを定義](lync-server-2013-optional-define-response-group-holiday-sets.md)します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-254">For details, see [(Optional) Define Response Group business hours in Lync Server 2013](lync-server-2013-optional-define-response-group-business-hours.md) and [(Optional) Define Response Group holiday sets in Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md).</span></span>

7.  <span data-ttu-id="9d46b-255">営業時間外または休日に受信する通話用のプロンプトを保持する場合は、**New-CsRgsPrompt** コマンドレットを使用してプロンプトを定義し、**New-CsRgsCallAction** を使用して、プロンプトの後に実行するアクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-255">If you want to have prompts for calls that are received out of business hours or on holidays, use the **New-CsRgsPrompt** cmdlet to define the prompt, and use the **New-CsRgsCallAction** to define the action to be taken after the prompt.</span></span> <span data-ttu-id="9d46b-256">詳しくは、「 [新しい-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) 」と「 [新規-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-256">For details, see [New-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) and [New-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction).</span></span>

8.  <span data-ttu-id="9d46b-257">Lync サーバー応答グループサービスのサービス名を取得して、それを変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9d46b-257">Retrieve the service name for the Lync Server Response Group service and assign it to a variable.</span></span> <span data-ttu-id="9d46b-258">コマンド ラインで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-258">At the command, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -like "*RGS*"}).ServiceId;

9.  <span data-ttu-id="9d46b-259">ワークフローを作成または変更します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-259">Create or modify the workflow.</span></span> <span data-ttu-id="9d46b-260">ワークフローを作成するには、**New-CsRgsWorkflow** を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-260">To create a workflow, use **New-CsRgsWorkflow**.</span></span> <span data-ttu-id="9d46b-261">ワークフローを変更するには、**Set-CsRgsWorkflow** を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-261">To modify a workflow, use **Set-CsRgsWorkflow**.</span></span> <span data-ttu-id="9d46b-262">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="9d46b-262">At the command line, type:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent <service ID for the Response Group service> -Name "<hunt group name>" [-Description "<hunt group description>"] -PrimaryUri "<SIP address for the workflow>" [-LineUri "<Phone number for the workflow>"] [-DisplayNumber "<Phone number displayed in Lync>"] [-Active <$true | $false>] [-Anonymous <$true | $false>] [-DefaultAction <variable from preceding step>] [-EnabledForFederation <$true | $false>] [-Managed <$true | $false>] [-MangersByUri <SIP addresses for Response Group Managers who can manage the workflow>]
    
    <span data-ttu-id="9d46b-263">例:</span><span class="sxs-lookup"><span data-stu-id="9d46b-263">For example:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent $serviceID -Name "Human Resources" -Description "Human Resources workflow" -PrimaryUri "sip:humanresources@contoso.com" -LineUri "TEL:+14255551219" -DisplayNumber "555-1219" -Active $true -Anonymous $true -DefaultAction $actionWM -EnabledForFederation $false -Managed $true -ManagersByUri "sip:bob@contoso.com", "mindy@contoso.com"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9d46b-264">ワークフローのマネージャーに指定されているすべてのユーザーに CsResponseGroupManager ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d46b-264">All users who are designated managers for workflows must be assigned the CsResponseGroupManager role.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9d46b-265">追加のオプションパラメーターの詳細については、「<A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">新しい-csrgsworkflow</A> 」または「 <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">Set-csrgsworkflow</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d46b-265">For details about additional optional parameters, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">New-CsRgsWorkflow</A> or <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">Set-CsRgsWorkflow</A></span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9d46b-266">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d46b-266">See Also</span></span>


[<span data-ttu-id="9d46b-267">省略Lync Server 2013 で回答グループの休日セットを定義する</span><span class="sxs-lookup"><span data-stu-id="9d46b-267">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="9d46b-268">省略Lync Server 2013 での応答グループの営業時間の定義</span><span class="sxs-lookup"><span data-stu-id="9d46b-268">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  


[<span data-ttu-id="9d46b-269">New-CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="9d46b-269">New-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow)  
[<span data-ttu-id="9d46b-270">Set-CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="9d46b-270">Set-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow)  
[<span data-ttu-id="9d46b-271">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="9d46b-271">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="9d46b-272">New-CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="9d46b-272">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
  

<span data-ttu-id="9d46b-273"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d46b-273"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

