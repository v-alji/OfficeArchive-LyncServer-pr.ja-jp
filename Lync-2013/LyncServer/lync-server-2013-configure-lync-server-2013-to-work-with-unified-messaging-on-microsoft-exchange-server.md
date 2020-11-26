---
title: 'Lync Server 2013: Microsoft Exchange Server のユニファイド メッセージングと連動させるための Lync Server 2013 の構成'
description: 'Lync Server 2013: Microsoft Exchange Server のユニファイドメッセージングと連携するように Lync Server 2013 を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server
ms:assetid: 1098ae4d-f57f-44f3-804e-39889d9fc14e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398193(v=OCS.15)
ms:contentKeyID: 48183430
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 05ef2902ffc03b14e04b378a2ef18e03c8c58372
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433958"
---
# <a name="configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server"></a><span data-ttu-id="4ca30-103">Microsoft Exchange Server のユニファイド メッセージングと連動させるための Lync Server 2013 の構成</span><span class="sxs-lookup"><span data-stu-id="4ca30-103">Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span data-ttu-id="4ca30-104">_**最終更新日:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="4ca30-104">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="4ca30-105">この手順を実行するには、Exchange UM 統合ユーティリティ (OcsUmUtil.exe) が必要です。</span><span class="sxs-lookup"><span data-stu-id="4ca30-105">This step requires the Exchange UM Integration Utility (OcsUmUtil.exe).</span></span> <span data-ttu-id="4ca30-106">このツールは、の Lync Server 2013 サーバーにあります。 \\Program Files \\ の一般的なファイル \\ Microsoft Lync Server 2013 \\ サポートフォルダー。</span><span class="sxs-lookup"><span data-stu-id="4ca30-106">This tool is located on the Lync Server 2013 server in the ..\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Support folder.</span></span>

<div>

## <a name="running-the-exchange-um-integration-utility"></a><span data-ttu-id="4ca30-107">Exchange UM 統合ユーティリティの実行</span><span class="sxs-lookup"><span data-stu-id="4ca30-107">Running the Exchange UM Integration Utility</span></span>

<span data-ttu-id="4ca30-108">Exchange UM 統合ユーティリティは、次の特徴を持つユーザーアカウントから実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-108">The Exchange UM Integration Utility must be run from a user account with the following characteristics:</span></span>

  - <span data-ttu-id="4ca30-109">RTCUniversalServerAdmins グループおよび RtcUniversalUserAdmins groups のメンバーシップ (Exchange Server ユニファイドメッセージングの設定を確認するためのアクセス許可を含みます)。</span><span class="sxs-lookup"><span data-stu-id="4ca30-109">Membership in the RTCUniversalServerAdmins and RtcUniversalUserAdmins groups (which includes permission to read Exchange Server Unified Messaging settings).</span></span>

  - <span data-ttu-id="4ca30-110">ドメイン内のユーザー権利。指定された組織単位 (OU) コンテナーに連絡先オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-110">User rights within the domain to create contact objects in the specified organizational unit (OU) container.</span></span>

<span data-ttu-id="4ca30-111">Exchange UM 統合ユーティリティを実行すると、次のタスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4ca30-111">When you run the Exchange UM Integration Utility, it performs the following tasks:</span></span>

  - <span data-ttu-id="4ca30-112">エンタープライズボイスユーザーが使用する自動応答とサブスクライバーアクセス番号ごとに連絡先オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-112">Creates contact objects for each auto-attendant and subscriber access number to be used by Enterprise Voice users.</span></span>

  - <span data-ttu-id="4ca30-113">各エンタープライズボイスダイヤルプランの名前が、対応するユニファイドメッセージング (UM) ダイヤルプランの電話コンテキストに一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-113">Verifies that the name of each Enterprise Voice dial plan matches its corresponding unified messaging (UM) dial plan phone context.</span></span> <span data-ttu-id="4ca30-114">この照合が必要なのは、UM ダイヤルプランが Exchange 2010 Service Pack 1 (SP1) よりも *前* のバージョンの exchange で実行されている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="4ca30-114">This matching is necessary only if the UM dial plan is running on a version of Exchange *earlier* than Exchange 2010 Service Pack 1 (SP1).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ca30-115">Exchange UM 統合ユーティリティを実行する前に、次の作業を行っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-115">Before running the Exchange UM Integration Utility, be sure that you have done the following:</span></span>
> <ul>
> <li><p><span data-ttu-id="4ca30-116">Exchange 製品のドキュメントで説明されているように、1つ以上の Exchange UM ダイヤルプランを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-116">Create one or more Exchange UM dial plans, as described in the Exchange product documentation.</span></span></p>
> <p><span data-ttu-id="4ca30-117">Microsoft Exchange Server 2010 については、「 &quot; at で UM ダイヤルプランを作成する」をご覧ください &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=186177">https://go.microsoft.com/fwlink/p/?linkId=186177</a> 。</span><span class="sxs-lookup"><span data-stu-id="4ca30-117">For Microsoft Exchange Server 2010, see &quot;Create a UM Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=186177">https://go.microsoft.com/fwlink/p/?linkId=186177</a>.</span></span></p>
> <p><span data-ttu-id="4ca30-118">Microsoft Exchange Server 2007 Service Pack 1 (SP1) については、「 &quot; ユニファイドメッセージング SIP URI ダイヤルプランを作成する方法」を参照してください &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=185771">https://go.microsoft.com/fwlink/p/?linkId=185771</a> 。</span><span class="sxs-lookup"><span data-stu-id="4ca30-118">For Microsoft Exchange Server 2007 Service Pack 1 (SP1), see &quot;How to Create a Unified Messaging SIP URI Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=185771">https://go.microsoft.com/fwlink/p/?linkId=185771</a>.</span></span></p></li>
> <li><p><span data-ttu-id="4ca30-119">「 <a href="lync-server-2013-create-a-dial-plan.md">Lync server 2013 でダイヤルプランを作成</a>する」の説明に従って、1つまたは複数の lync server のダイヤルプランを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-119">Create one or more corresponding Lync Server dial plans, as described in <a href="lync-server-2013-create-a-dial-plan.md">Create a dial plan in Lync Server 2013</a>.</span></span></p></li>
> <ul><li><span data-ttu-id="4ca30-120">Microsoft Exchange Server 2010 SP1 より前のバージョンの Exchange を使用している場合は、Lync Server 2013 の [ダイヤルプランの <STRONG>簡易名</STRONG> ] フィールドに、対応する Exchange ユニファイドメッセージング (UM) SIP ダイヤルプランの完全修飾ドメイン名 (FQDN) を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-120">If you are using a version of Exchange that is earlier than Microsoft Exchange Server 2010 SP1, you must enter the fully qualified domain name (FQDN) of the corresponding Exchange Unified Messaging (UM) SIP dial plan in the Lync Server 2013 dial plan <STRONG>Simple name</STRONG> field.</span></span> <span data-ttu-id="4ca30-121">Microsoft Exchange Server 2010 SP1 または最新の service pack を使用している場合、このダイヤルプランの名前の一致は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4ca30-121">If you are using Microsoft Exchange Server 2010 SP1 or latest service pack, this dial plan name matching is not necessary.</span></span></li></ul>
> <li><span data-ttu-id="4ca30-122">自動応答を作成し、サブスクライバーアクセス番号と自動応答番号の両方が必ず164形式になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-122">Create an auto-attendant and make sure that both the subscriber access number and auto-attendant number are in E.164 format.</span></span></li></ul>


<div>

## <a name="to-run-the-exchange-um-integration-utility"></a><span data-ttu-id="4ca30-123">Exchange UM 統合ユーティリティを実行するには</span><span class="sxs-lookup"><span data-stu-id="4ca30-123">To run the Exchange UM Integration Utility</span></span>

1.  <span data-ttu-id="4ca30-124">フロントエンドサーバーでコマンドプロンプトを開き、「 **cd% CommonProgramFiles% \\ Microsoft Lync Server 2013 \\ サポート**」と入力して、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-124">On a Front End Server, open a command prompt and type **cd %CommonProgramFiles%\\Microsoft Lync Server 2013\\Support**, and then press ENTER.</span></span>

2.  <span data-ttu-id="4ca30-125">「 **OcsUmUtil.exe**」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-125">Type **OcsUmUtil.exe**, and then press ENTER.</span></span>

3.  <span data-ttu-id="4ca30-126">[ **データの読み込み** ] をクリックして、信頼できるすべての Exchange フォレストを検索します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-126">Click **Load Data** to find all trusted Exchange forests.</span></span>

4.  <span data-ttu-id="4ca30-127">**Sip ダイヤルプラン** リストで、コンタクトオブジェクトを作成する UM SIP ダイヤルプランを選択し、「**追加**」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ca30-127">In the **SIP Dial Plans** list, select a UM SIP dial plan for which you want to create contact objects, and then click **Add**.</span></span>

5.  <span data-ttu-id="4ca30-128">[ **連絡先** ] ボックスで、既定の組織単位をそのまま使用するか、[ **参照** ] をクリックして **OU 選択** を開始します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-128">In the **Contact** box, accept the default organizational unit, or click **Browse** to start the **OU Picker**.</span></span> <span data-ttu-id="4ca30-129">[ **Ou の選択** ] ボックスで、ou を選んで [ **OK**] をクリックします。または、ドメイン内のルートまたは他の ou (たとえば、"OU = RTC Special account, dc = 4 thコーヒー, dc = com") に新しい組織単位を作成 **するには** 、[ **ok**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ca30-129">In the **OU Picker** box, you can select an OU and click **OK**, or you can click **Make New OU** to create a new organizational unit under the root or any other OU in the domain (for example, "OU=RTC Special Accounts,DC=fourthcoffee,DC=com"), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ca30-130">選択または作成した OU の識別名 (DN) が [ <STRONG>組織単位</STRONG> ] ボックスに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-130">The distinguished name (DN) of the OU that you have selected or created is now displayed in the <STRONG>Organizational Unit</STRONG> box.</span></span>

    
    </div>

6.  <span data-ttu-id="4ca30-131">[ **名前** ] ボックスで、既定のダイヤルプラン名をそのまま使うか、作成している連絡先オブジェクトの新しい表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-131">In the **Name** box, either accept the default dial plan name or type a new display name for the contact object that you are creating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ca30-132">たとえば、サブスクライバーアクセスの contact オブジェクトを作成する場合は、"サブスクライバーアクセス" という名前を付けるだけです。</span><span class="sxs-lookup"><span data-stu-id="4ca30-132">For example, if you are creating a subscriber access contact object, you might simply name it Subscriber Access.</span></span>

    
    </div>

7.  <span data-ttu-id="4ca30-133">[ **Sip アドレス** ] ボックスに、既定の sip アドレスをそのまま使うか、新しい sip アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-133">In the **SIP Address** box, either accept the default SIP address or type a new SIP address.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ca30-134">新しい SIP アドレスを入力する場合は、 <STRONG>sip</STRONG> で始める必要があります (つまり、コロンを含む "sip:")。</span><span class="sxs-lookup"><span data-stu-id="4ca30-134">If you type a new SIP address, it must begin with <STRONG>SIP:</STRONG> (that is, "SIP:" including the colon).</span></span>

    
    </div>

8.  <span data-ttu-id="4ca30-135">[ **サーバーまたはプール** ] ボックスの一覧で、連絡先オブジェクトを有効にする標準エディションサーバーまたはフロントエンドプールを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-135">In the **Server or Pool** list, select the Standard Edition server or Front End pool in which the contact object is to be enabled.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ca30-136">可能であれば、選択したプールは、エンタープライズボイスと Exchange UM が有効になっているユーザーが展開する1つのプールである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-136">Preferably, the pool you select is the same one pool where users enabled for Enterprise Voice and Exchange UM are deployed.</span></span>

    
    </div>

9.  <span data-ttu-id="4ca30-137">[ **電話番号** ] ボックスの一覧で、[ **電話番号を入力** するか、 **Exchange UM からこのパイロット番号を使用する** ] を選択し、電話番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-137">In the **Phone Number** list, select either **Enter phone number** or **Use this pilot number from Exchange UM** and then enter a phone number.</span></span>

10. <span data-ttu-id="4ca30-138">[ **連絡先の種類** ] ボックスの一覧で、作成する連絡先の種類を選び、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ca30-138">In the **Contact Type** list, select the contact type that you want to create, and then click **OK**.</span></span>

11. <span data-ttu-id="4ca30-139">作成する追加の連絡先オブジェクトについて、手順 1 ~ 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-139">Repeat steps 1 through 10 for additional contact objects that you want to create.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ca30-140">自動応答ごとに、少なくとも1つの連絡先を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-140">You should create at least one contact for each auto attendant.</span></span> <span data-ttu-id="4ca30-141">外部アクセスが必要な場合は、サブスクライバーへのアクセスにもサブスクライバーへのアクセスが必要です。また、直接の内側ダイヤル (DID) 番号を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ca30-141">If you want external access, you also need a Subscriber Access contact and to specify Direct Inward Dial (DID) numbers.</span></span>

    
    </div>

</div>

<span data-ttu-id="4ca30-142">連絡先オブジェクトが作成されたことを確認するには、[Active Directory ユーザーとコンピューター] を開き、オブジェクトが作成された OU を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ca30-142">To verify that the contact objects have been created, open Active Directory Users and Computers and select the OU in which the objects were created.</span></span> <span data-ttu-id="4ca30-143">連絡先オブジェクトが詳細ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ca30-143">The contact objects should appear in the details pane.</span></span>

<span data-ttu-id="4ca30-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ca30-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

