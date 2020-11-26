---
title: 'Lync Server 2013: フォレストの準備の実行'
description: 'Lync Server 2013: フォレストの準備を実行しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442216"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="64048-103">Lync Server 2013 でのフォレストの準備の実行</span><span class="sxs-lookup"><span data-stu-id="64048-103">Running forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64048-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64048-104">

<span> </span></span></span>

<span data-ttu-id="64048-105">_**最終更新日:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="64048-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="64048-106">セットアップまたは Lync Server 管理シェルコマンドレットを使用して、フォレストを準備することができます。</span><span class="sxs-lookup"><span data-stu-id="64048-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the forest.</span></span> <span data-ttu-id="64048-107">フォレストを準備するコマンドレットでは、 **CsAdForest を有効** にします。</span><span class="sxs-lookup"><span data-stu-id="64048-107">The cmdlet that prepares the forest is **Enable-CsAdForest**.</span></span>

<span data-ttu-id="64048-108">フォレストを準備したら、ドメインの準備を実行する前に、グローバル設定がレプリケートされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64048-108">After you prepare the forest, you must verify that global settings have been replicated before running domain preparation.</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a><span data-ttu-id="64048-109">セットアップを使用してフォレストを準備するには</span><span class="sxs-lookup"><span data-stu-id="64048-109">To use Setup to prepare the forest</span></span>

1.  <span data-ttu-id="64048-110">フォレストルートドメインの Enterprise Admins グループのメンバーとしてドメインに参加しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="64048-110">Log on to a computer that is joined to a domain as a member of the Enterprise Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="64048-111">Lync Server 2013 のインストールフォルダーまたはメディアから、Setup.exe を実行して展開ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="64048-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="64048-112">[**Active Directory の準備**] をクリックして、展開状態が判別されるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="64048-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="64048-113">**手順 3: 現在のフォレストを準備** するには、[**実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-113">At **Step 3: Prepare Current Forest**, click **Run**.</span></span>

5.  <span data-ttu-id="64048-114">[ **フォレストの準備** ] ページで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-114">On the **Prepare Forest** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="64048-115">フォレストの準備 Lync Server 2013 のユニバーサルグループを配置する場所を選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="64048-115">Forest Preparation allows you to choose where to place the Universal Groups for Lync Server 2013.</span></span> <span data-ttu-id="64048-116">組織の要件と一致する配置先を選択してください。</span><span class="sxs-lookup"><span data-stu-id="64048-116">Choose a location that is consistent with the requirements of your organization.</span></span>

    
    </div>

6.  <span data-ttu-id="64048-117">[**コマンドを実行しています**] ページで [**タスク状態: 完了**] を見つけて、[**ログの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-117">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="64048-118">[ **アクション** ] 列の [ **forest Prep**] を展開し、 **\<Success\>** 各タスクの最後の実行結果を確認して、フォレストの準備が正常に完了したことを確認します。次に、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-118">Under the **Action** column, expand **Forest Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that forest preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="64048-119">Active Directory のレプリケーションが完了するまで待機するか、フォレストルートドメインコントローラーの **Active Directory サイトとサービス** スナップインに記載されているすべてのドメインコントローラーに対して強制的にレプリケーションを実行してから、ドメインの準備を実行します。</span><span class="sxs-lookup"><span data-stu-id="64048-119">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span> <span data-ttu-id="64048-120">すべての Active Directory サイトのドメインコントローラー間で強制的にレプリケーションを実行して、サイト内での複製が分単位で行われるようにします。</span><span class="sxs-lookup"><span data-stu-id="64048-120">Force replication between the domain controllers in all Active Directory sites to cause replication within the sites to occur within minutes.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a><span data-ttu-id="64048-121">コマンドレットを使用してフォレストを準備するには</span><span class="sxs-lookup"><span data-stu-id="64048-121">To use cmdlets to prepare the forest</span></span>

1.  <span data-ttu-id="64048-122">フォレストルートドメインの Domain Admins グループのメンバーとしてドメインに参加しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="64048-122">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="64048-123">Lync Server のコアコンポーネントは、次のようにインストールします。</span><span class="sxs-lookup"><span data-stu-id="64048-123">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="64048-124">Lync Server 2013 のインストールフォルダーまたはメディアで Setup.exe を実行して、Lync Server 展開ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="64048-124">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="64048-125">Microsoft Visual C++ 再頒布可能パッケージをインストールするかどうかを確認するメッセージが表示されたら、[ **はい**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-125">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="64048-126">[Lync Server 2013 セットアップ] ダイアログボックスで、Lync Server ファイルをインストールする場所を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="64048-126">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="64048-127">既定の場所を選ぶか、目的の場所を **参照** し、[ **インストール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-127">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="64048-128">[使用許諾契約] ページで、[ **使用許諾契約書に同意** します] をオンにし、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-128">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="64048-129">インストーラーは、Lync Server 2013 コアコンポーネントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="64048-129">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="64048-130">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="64048-130">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="64048-131">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="64048-131">Run:</span></span>
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    <span data-ttu-id="64048-132">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="64048-132">For example:</span></span>
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    <span data-ttu-id="64048-133">GroupDomain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="64048-133">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span> <span data-ttu-id="64048-134">ユニバーサルグループが、既定のドメインではないドメインで以前に作成された場合は、GroupDomain パラメーターを明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64048-134">If universal groups were created previously in a domain that is not the default domain, you must specify the GroupDomain parameter explicitly.</span></span>

5.  <span data-ttu-id="64048-135">Active Directory のレプリケーションが完了するまで待機するか、フォレストルートドメインコントローラーの **Active Directory サイトとサービス** スナップインに記載されているすべてのドメインコントローラーに対して強制的にレプリケーションを実行してから、ドメインの準備を実行します。</span><span class="sxs-lookup"><span data-stu-id="64048-135">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span>

6.  <span data-ttu-id="64048-136">フォレストの準備が正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="64048-136">Verify that forest preparation was successful.</span></span> <span data-ttu-id="64048-137">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="64048-137">Run:</span></span>
    
        Get-CsAdForest 
    
    <span data-ttu-id="64048-138">フォレストの準備が正常に完了した場合、このコマンドレットは **LC \_ FORESTSETTINGS \_ STATE \_** の値を返します。</span><span class="sxs-lookup"><span data-stu-id="64048-138">This cmdlet returns a value of **LC\_FORESTSETTINGS\_STATE\_READY** if forest preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="64048-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="64048-139">See Also</span></span>


[<span data-ttu-id="64048-140">コマンドレットの使用による Lync Server 2013 のフォレストの準備のリバース</span><span class="sxs-lookup"><span data-stu-id="64048-140">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[<span data-ttu-id="64048-141">Lync Server 2013 でのフォレストの準備</span><span class="sxs-lookup"><span data-stu-id="64048-141">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="64048-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64048-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

