---
title: 'Lync Server 2013: ドメイン準備手続き'
description: 'Lync Server 2013: ドメインの準備を実行しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running domain preparation
ms:assetid: 95dab800-1f2c-4506-b36c-99986643b149
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398761(v=OCS.15)
ms:contentKeyID: 48184847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f2c4ebe94d07ed2d1fd9be013cd8e88204312f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442258"
---
# <a name="running-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="9a4e2-103">Lync Server 2013 のドメイン準備手続き</span><span class="sxs-lookup"><span data-stu-id="9a4e2-103">Running domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a4e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a4e2-104">

<span> </span></span></span>

<span data-ttu-id="9a4e2-105">_**最終更新日:** 2013-04-16_</span><span class="sxs-lookup"><span data-stu-id="9a4e2-105">_**Topic Last Modified:** 2013-04-16_</span></span>

<span data-ttu-id="9a4e2-106">セットアップまたは Lync Server 管理シェルコマンドレットを使用して、ドメインを準備することができます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-106">You can use Setup or Lync Server Management Shell cmdlets to prepare domains.</span></span> <span data-ttu-id="9a4e2-107">ドメインを準備するコマンドレットでは、 **CsAdDomain を有効に** することができます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-107">The cmdlet that prepares a domain is **Enable-CsAdDomain**.</span></span>

<span data-ttu-id="9a4e2-108">ドメインの準備は、Lync Server 2013 用の Active Directory ドメインサービスの準備での最終的な手順です。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-108">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span>

<div>

## <a name="to-use-setup-to-prepare-domains"></a><span data-ttu-id="9a4e2-109">セットアップを使用してドメインを準備するには</span><span class="sxs-lookup"><span data-stu-id="9a4e2-109">To use Setup to prepare domains</span></span>

1.  <span data-ttu-id="9a4e2-110">Domain Admins グループのメンバーとして、ドメイン内の任意のサーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-110">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="9a4e2-111">Lync Server 2013 のインストールフォルダーまたはメディアで Setup.exe を実行して、Lync Server 展開ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="9a4e2-112">[**Active Directory の準備**] をクリックして、展開状態が判別されるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="9a4e2-113">[**手順 5: 現在のドメインの準備**] で、[**実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-113">At **Step 5: Prepare Current Domain**, click **Run**.</span></span>

5.  <span data-ttu-id="9a4e2-114">[ **ドメインの準備** ] ページで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-114">On the **Prepare Domain** page, click **Next**.</span></span>

6.  <span data-ttu-id="9a4e2-115">[**コマンドの実行**] ページで [**タスク状態: 完了**] を見つけて、[**ログの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-115">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="9a4e2-116">[ **アクション** ] 列で、[ **domain Prep**] を展開し、 **\<Success\>** 各タスクの最後の実行結果を確認して、ドメインの準備が正常に完了したことを確認します。次に、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-116">Under the **Action** column, expand **Domain Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that domain preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="9a4e2-117">Active Directory のレプリケーションが完了するのを待ちます。または、フォレストルートドメインコントローラーの [Active Directory サイトとサービス] スナップインで一覧表示されているすべてのドメインコントローラーへの複製が強制されます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-117">Wait for Active Directory replication to complete or force replication to all the domain controllers listed in the Active Directory Sites and Services snap-in for the forest root domain controller.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-domain"></a><span data-ttu-id="9a4e2-118">コマンドレットを使用してドメインを準備するには</span><span class="sxs-lookup"><span data-stu-id="9a4e2-118">To use cmdlets to prepare the domain</span></span>

1.  <span data-ttu-id="9a4e2-119">Domain Admins グループのメンバーとして、ドメイン内の任意のサーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-119">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="9a4e2-120">Lync Server のコアコンポーネントは、次のようにインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-120">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="9a4e2-121">Lync Server 2013 のインストールフォルダーまたはメディアで Setup.exe を実行して、Lync Server 展開ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-121">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="9a4e2-122">Microsoft Visual C++ 再頒布可能パッケージをインストールするかどうかを確認するメッセージが表示されたら、[ **はい**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-122">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="9a4e2-123">[Lync Server 2013 セットアップ] ダイアログボックスで、Lync Server ファイルをインストールする場所を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-123">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="9a4e2-124">既定の場所を選ぶか、目的の場所を **参照** し、[ **インストール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-124">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="9a4e2-125">[使用許諾契約] ページで、[ **使用許諾契約書に同意** します] をオンにし、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-125">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="9a4e2-126">インストーラーは、Lync Server 2013 コアコンポーネントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-126">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="9a4e2-127">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-127">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="9a4e2-128">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-128">Run:</span></span>
    
        Enable-CsAdDomain [-Domain <DomainFQDN>] 
    
    <span data-ttu-id="9a4e2-129">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-129">For example:</span></span>
    
        Enable-CsAdDomain -Domain domain1.contoso.net 
    
    <span data-ttu-id="9a4e2-130">Domain パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-130">If you do not specify the Domain parameter, the default is the local domain.</span></span>

5.  <span data-ttu-id="9a4e2-131">ドメインの準備が正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-131">Verify that domain preparation was successful.</span></span> <span data-ttu-id="9a4e2-132">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-132">Run:</span></span>
    
        Get-CsAdDomain [-Domain <Domain FQDN>] [-DomainController <Domain controller FQDN>] [-GlobalCatalog <Global catalog server FQDN>] [-GlobalSettingsDomainController <Domain controller FQDN where global settings are stored>] 
    
    <span data-ttu-id="9a4e2-133">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-133">For example:</span></span>
    
        Get-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.com
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9a4e2-134">Parameter GlobalSettingsDomainController を使うと、グローバル設定が保存されている場所を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-134">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="9a4e2-135">設定がシステムコンテナーに保存されている場合 (つまり、グローバル設定が構成コンテナーに移行されていないアップグレード展開で一般的)、Active Directory フォレストのルートでドメインコントローラーを定義します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-135">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global settings migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="9a4e2-136">グローバル設定を構成コンテナーに保存する (新しい展開または構成コンテナーに設定を移行しているアップグレードの展開で一般的) 場合、フォレストに任意のドメイン コントローラーを定義します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-136">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="9a4e2-137">このパラメーターを指定しない場合、設定は構成コンテナーに保存され、AD DS の任意のドメインコントローラーを参照することがコマンドレットによって想定され &nbsp; ます。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-137">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>
    
    <span data-ttu-id="9a4e2-138">**Domain** パラメーターを指定しない場合、既定値はローカルドメインです。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-138">If you do not specify the **Domain** parameter, the default is the local domain.</span></span>
    
    <span data-ttu-id="9a4e2-139">このコマンドレットは、ドメインの準備が正常に完了した場合に、 **LC \_ domainsettings \_ 状態 \_** の値を返します。</span><span class="sxs-lookup"><span data-stu-id="9a4e2-139">This cmdlet returns a value of **LC\_DOMAINSETTINGS\_STATE\_READY** if domain preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9a4e2-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a4e2-140">See Also</span></span>


[<span data-ttu-id="9a4e2-141">Lync Server 2013 のコマンドレットの使用によるドメインの準備の無効化</span><span class="sxs-lookup"><span data-stu-id="9a4e2-141">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)  


[<span data-ttu-id="9a4e2-142">Lync Server 2013 のドメインの準備</span><span class="sxs-lookup"><span data-stu-id="9a4e2-142">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="9a4e2-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a4e2-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

