---
title: 'Lync Server 2013: 新しいクライアントのバージョンポリシールールを作成または変更する'
description: 'Lync Server 2013: 新しいクライアントのバージョンポリシールールを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a new client version policy rule
ms:assetid: 6f879d99-8401-41e0-a562-195c890d63ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898478(v=OCS.15)
ms:contentKeyID: 50873758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11ebcf17d5cb14fd519fba8ad36be10894fabdb9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399170"
---
# <a name="create-or-modify-a-new-client-version-policy-rule-in-lync-server-2013"></a><span data-ttu-id="9401e-103">Lync Server 2013 で新しいクライアントのバージョンポリシールールを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="9401e-103">Create or modify a new client version policy rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9401e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9401e-104">

<span> </span></span></span>

<span data-ttu-id="9401e-105">_**最終更新日:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="9401e-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="9401e-106">クライアントのバージョンポリシールールは、ユーザーが特定のクライアントとクライアントバージョンでログオンしようとしたときに実行される操作を定義します。</span><span class="sxs-lookup"><span data-stu-id="9401e-106">Client version policy rules define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span> <span data-ttu-id="9401e-107">Lync Server 2013 コントロールパネルからクライアントのバージョンポリシーの個々のルールを作成または変更することができます。</span><span class="sxs-lookup"><span data-stu-id="9401e-107">You can create or modify individual rules for a client version policy from Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9401e-108">ルールは優先順位の順に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="9401e-108">Rules are listed in order of precedence.</span></span> <span data-ttu-id="9401e-109">たとえば、バージョン1.5 を実行しているクライアントに対して接続を許可するルールがあり、その後に2.0 より前のバージョンを実行しているクライアントをブロックするルールがある場合は、最初のルールが優先され、バージョン1.5 を実行しているクライアントで接続が許可されます。</span><span class="sxs-lookup"><span data-stu-id="9401e-109">For example, if you have a rule that allows clients running version 1.5 to connect, followed by a rule that blocks clients running a version earlier than 2.0, the first rule takes precedence, and clients running version 1.5 are allowed to connect.</span></span>



</div>

<div>

## <a name="to-create-or-modify-client-version-policy-rules-with-lync-server-control-panel"></a><span data-ttu-id="9401e-110">Lync Server コントロールパネルでクライアントのバージョンポリシールールを作成または変更するには</span><span class="sxs-lookup"><span data-stu-id="9401e-110">To create or modify client version policy rules with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9401e-111">Lync server 2013 で Lync Server コントロールパネルを使用して[、新しいクライアントバージョンポリシーを作成または変更](lync-server-2013-create-or-modify-a-new-client-version-policy.md)します。</span><span class="sxs-lookup"><span data-stu-id="9401e-111">[Create or modify a new client version policy in Lync Server 2013](lync-server-2013-create-or-modify-a-new-client-version-policy.md) with Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="9401e-112">[ **クライアントのバージョンポリシーの編集** ] ページで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9401e-112">On the **Edit Client Version Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="9401e-113">[ **新規** ] をクリックして、新しいクライアントバージョン規則を作成します。</span><span class="sxs-lookup"><span data-stu-id="9401e-113">Click **New** to create a new client version rule.</span></span>
    
      - <span data-ttu-id="9401e-114">リストで定義されているクライアントの種類のいずれかをクリックし、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-114">Click one of the defined client types in the list, and then click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9401e-115">ワイルドカードを使用して、クライアントの種類を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="9401e-115">You can use wildcards to indicate the client type.</span></span>

    
    </div>

3.  <span data-ttu-id="9401e-116">[ **ユーザーエージェント**] で、クライアントの種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="9401e-116">In **User agent**, select a client type.</span></span>

4.  <span data-ttu-id="9401e-117">[ **バージョン番号**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9401e-117">Under **Version number**, do the following:</span></span>
    
      - <span data-ttu-id="9401e-118">[ **メジャーバージョン**] に、クライアントのメジャーリリースに対応する番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9401e-118">In **Major version**, type the number that corresponds to the major release of the client.</span></span>
    
      - <span data-ttu-id="9401e-119">[ **マイナーバージョン**] に、クライアントのマイナーリリースに対応する番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9401e-119">In **Minor version**, type the number that corresponds to the minor release of the client.</span></span>
    
      - <span data-ttu-id="9401e-120">[ **ビルド**] に、クライアントのメジャーとマイナーのリリースに対応する番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9401e-120">In **Build**, type the number that corresponds to the major and minor release of the client.</span></span>
    
      - <span data-ttu-id="9401e-121">[ **Update**] に、更新されたクライアントのリリースに対応する番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9401e-121">In **Update**, type the number that corresponds to the updated release of the client.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9401e-122">クライアントのバージョン番号を示すには、ワイルドカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9401e-122">You can use wildcards to indicate the client version number.</span></span>

    
    </div>

5.  <span data-ttu-id="9401e-123">前の手順で指定したクライアントのバージョンに対して一致する操作を指定するには、 **比較操作** で次のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-123">To specify the matching operation for the client version you specified in the preceding steps, in **Comparison operation**, click one of the following:</span></span>
    
      - <span data-ttu-id="9401e-124">**[同じ]**</span><span class="sxs-lookup"><span data-stu-id="9401e-124">**Same as**</span></span>
    
      - <span data-ttu-id="9401e-125">**[等しくない]**</span><span class="sxs-lookup"><span data-stu-id="9401e-125">**Is not**</span></span>
    
      - <span data-ttu-id="9401e-126">**[より新しい]**</span><span class="sxs-lookup"><span data-stu-id="9401e-126">**Newer than**</span></span>
    
      - <span data-ttu-id="9401e-127">**[より新しいか同じ]**</span><span class="sxs-lookup"><span data-stu-id="9401e-127">**Newer than or same as**</span></span>
    
      - <span data-ttu-id="9401e-128">**[より古い]**</span><span class="sxs-lookup"><span data-stu-id="9401e-128">**Older than**</span></span>
    
      - <span data-ttu-id="9401e-129">**[より古いか同じ]**</span><span class="sxs-lookup"><span data-stu-id="9401e-129">**Older than or same as**</span></span>

6.  <span data-ttu-id="9401e-130">前の手順の条件が満たされたときに実行する操作を指定するには、次の **操作** のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-130">To specify the action to perform when the criteria in the preceding steps are met, click one of the following in **Action**:</span></span>
    
      - <span data-ttu-id="9401e-131">クライアントがログオンできるようにするには、[ **許可**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-131">To allow the client to log on, click **Allow**.</span></span>
    
      - <span data-ttu-id="9401e-132">クライアントが Windows Server Update Service または Microsoft Update からの更新プログラムをログオンして受信できるようにするには、[ **許可/アップグレード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-132">To allow the client to log on and receive updates from Windows Server Update Service or Microsoft Update, click **Allow and Upgrade**.</span></span> <span data-ttu-id="9401e-133">この操作は、ユーザーエージェント **OC** が選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9401e-133">This action is available only when user agent **OC** is selected.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9401e-134">このアクションを選ぶと、次回ユーザーが Lync 2013 にサインインしたときに通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9401e-134">Selecting this action causes a notification to appear the next time users sign in to Lync 2013.</span></span> <span data-ttu-id="9401e-135">この通知では、Windows Server Update Service または Microsoft Update に更新がまだリリースされていなくても、更新が利用できるようになったことが伝えられます。</span><span class="sxs-lookup"><span data-stu-id="9401e-135">The notification states that an update is available, even if updates have not yet been released to Windows Server Update Service or Microsoft Update.</span></span> <span data-ttu-id="9401e-136">混乱を避けるため、このアクションは必ず更新が利用できるようになってから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9401e-136">To avoid confusion, you should choose this action only after updates become available.</span></span>

        
        </div>
    
      - <span data-ttu-id="9401e-137">クライアントがログオンして、別のクライアントバージョンをダウンロードする場所に関するメッセージを表示できるようにするには、[ **URL で許可**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-137">To allow the client to log on and display a message about where to download another client version, click **Allow with URL**.</span></span> <span data-ttu-id="9401e-138">この手順の後半で、URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="9401e-138">You specify the URL later in this procedure.</span></span>
    
      - <span data-ttu-id="9401e-139">クライアントがログオンしないようにするには、[ **ブロック**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-139">To prevent the client from logging on, click **Block**.</span></span>
    
      - <span data-ttu-id="9401e-140">クライアントがログオンし、Windows Server Update Service または Microsoft Update から更新プログラムを受信できるようにするには、[ **ブロックとアップグレード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-140">To prevent the client from logging on and allow the client to receive updates from Windows Server Update Service or Microsoft Update, click **Block and Upgrade**.</span></span> <span data-ttu-id="9401e-141">この操作は、ユーザーエージェント **OC** が選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9401e-141">This action is available only when user agent **OC** is selected.</span></span>
    
      - <span data-ttu-id="9401e-142">クライアントがログオンして、別のクライアントバージョンをダウンロードする場所に関するメッセージを表示するには、[ **URL を含むブロック**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-142">To prevent the client from logging on and display a message about where to download another client version, click **Block with URL**.</span></span> <span data-ttu-id="9401e-143">この手順の後半で、URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="9401e-143">You specify the URL later in this procedure.</span></span>

7.  <span data-ttu-id="9401e-144">省略前の手順で [URL を指定して **許可** ] または [ **Url を含むブロック** ] をクリックした場合は、クライアントのダウンロード url を入力して、 **url** のメッセージに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9401e-144">(Optional) If you clicked **Allow with URL** or **Block with URL** in the previous step, type the client download URL to include in the message in **URL**.</span></span>

8.  <span data-ttu-id="9401e-145">[ **OK**] をクリックし、[ **コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9401e-145">Click **OK**, and then click **Commit**.</span></span>

<span data-ttu-id="9401e-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9401e-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

