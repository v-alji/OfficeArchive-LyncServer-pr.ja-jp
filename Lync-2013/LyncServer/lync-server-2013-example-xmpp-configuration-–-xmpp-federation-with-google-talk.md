---
title: XMPP 構成の例  - Google Talk との XMPP フェデレーション
description: XMPP の構成の例– Google Talk との XMPP フェデレーション。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428452"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="2fc80-103">Lync Server 2013 での XMPP 構成の例  - Google Talk との XMPP フェデレーション</span><span class="sxs-lookup"><span data-stu-id="2fc80-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fc80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fc80-104">

<span> </span></span></span>

<span data-ttu-id="2fc80-105">_**最終更新日:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="2fc80-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="2fc80-106">XMPP プロキシを展開するための構成例では、Google Talk とのフェデレーションを定義しています。</span><span class="sxs-lookup"><span data-stu-id="2fc80-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="2fc80-107">XMPP 構成の例  - Google Talk との XMPP フェデレーション</span><span class="sxs-lookup"><span data-stu-id="2fc80-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="2fc80-108">フロントエンドサーバーで、Lync Server 展開ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="2fc80-109">[ **Lync Server System** の **インストール** または更新] をクリックし、[ **lync server コンポーネント** の **セットアップ** または削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="2fc80-110">[ **実行] をもう一度** クリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="2fc80-111">**Lync Server コンポーネントのセットアップ** で、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="2fc80-112">概要画面には、実行中の操作が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="2fc80-113">展開が完了したら、[ **ログの表示** ] をクリックして、利用可能なログファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="2fc80-114">[ **完了** ] をクリックして展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="2fc80-115">エッジサーバーで、Lync Server 展開ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="2fc80-116">[ **Lync Server System** の **インストール** または更新] をクリックし、[ **lync server コンポーネント** の **セットアップ** または削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="2fc80-117">[ **実行] をもう一度** クリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="2fc80-118">Google の会話を XMPP で許可されているパートナーとして追加します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="2fc80-119">Google Talk では、現時点では、サーバー間の XMPP フェデレーション向けの暗号化されていない TCP 接続のみをサポートしており、身元確認のためのサーバーコールバックのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2fc80-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="2fc80-120">( <http://xmpp.org/extensions/xep-0220.html> を参照)。</span><span class="sxs-lookup"><span data-stu-id="2fc80-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="2fc80-121">エッジフェデレーションを有効にするには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="2fc80-122">**Lync Server コンポーネントのセットアップ** で、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="2fc80-123">概要画面には、実行中の操作が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="2fc80-124">展開が完了したら、[ **ログの表示** ] をクリックして、利用可能なログファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="2fc80-125">[ **完了** ] をクリックして展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="2fc80-126">エッジサーバーの Lync Server 展開ウィザードで、[ **手順 3: 証明書の要求、インストール、または割り当て**] の横にある [実行] を **もう一度** クリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="2fc80-127">初めてエッジサーバーを展開する場合は、[実行] ではなく、[実行] と表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="2fc80-128">[**利用可能な証明書タスク**] ページで、[**新しい証明書要求を作成する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="2fc80-129">[ **証明書の要求** ] ページで、[ **外部境界の証明書**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="2fc80-130">[ **遅延または即時要求** ] ページで、[ **今すぐ要求を準備するが、後で送信** する] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="2fc80-131">[ **証明書要求ファイル** ] ページで、要求を保存するファイルの完全パスとファイル名を入力します (たとえば、c: \\ cert \_ 外部 \_ edge)。</span><span class="sxs-lookup"><span data-stu-id="2fc80-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="2fc80-132">[ **代替証明書テンプレートの指定** ] ページで、既定の web サーバテンプレート以外のテンプレートを使用するには、[ **選択された証明機関に別の証明書テンプレートを使用** する] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="2fc80-133">[ **名前とセキュリティの設定** ] ページで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="2fc80-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="2fc80-134">[ **フレンドリ名**] に、証明書の表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="2fc80-135">**ビット長** では、ビット長 (通常は **2048** の既定値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="2fc80-136">[ **証明書の秘密キーをエクスポート可能としてマーク** する] チェックボックスがオンになっていることを確認する</span><span class="sxs-lookup"><span data-stu-id="2fc80-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="2fc80-137">[ **組織の情報** ] ページで、組織の名前と組織単位 (たとえば、部門や部署) を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="2fc80-138">[ **地理情報** ] ページで、場所情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="2fc80-139">[ **Subject Name/Subject name** ] ページには、ウィザードによって自動的に入力される情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="2fc80-140">追加の件名の代替名が必要な場合は、次の2つの手順で指定します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="2fc80-141">[ **サブジェクト代替名 (san)] ページの Sip ドメイン設定** で、[Domain] チェックボックスをオンにして sip を追加します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="2fc80-142">\<sipdomain\> [サブジェクトの別名] リストに入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="2fc80-143">[ **追加のサブジェクト代替名の構成** ] ページで、必要なその他のサブジェクトの代替名を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="2fc80-144">XMPP プロキシがインストールされている場合、既定では、ドメイン名 (contoso.com など) が SAN エントリに設定されます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="2fc80-145">他のエントリが必要な場合は、この手順で追加します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="2fc80-146">[ **要求の概要** ] ページで、要求の生成に使用する証明書情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="2fc80-147">コマンドの実行が完了したら、 **ログを表示** するか、[ **次へ** ] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="2fc80-148">[**証明書要求ファイル**] ページで、[**完了**] をクリックして、証明書ウィザードの [**表示**] または [終了] をクリックし、生成された証明書署名要求 (CSR) ファイルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="2fc80-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="2fc80-149">要求ファイルをコピーして、公開証明機関に提出します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="2fc80-150">公開証明書の受信、インポート、割り当てが完了したら、Edge Server サービスを停止して再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fc80-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="2fc80-151">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc80-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="2fc80-152">Lync Server 管理シェルで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="2fc80-153">XMPP フェデレーション用の DNS を構成するには、次の SRV レコードを外部 DNS に追加します。 \_ xmpp-サーバー。 \_tcp.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="2fc80-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="2fc80-154">SRV レコードは、エッジサーバーのアクセスエッジ FQDN に解決され、ポート値は5269になります。</span><span class="sxs-lookup"><span data-stu-id="2fc80-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="2fc80-155">フロントエンドサーバーで Lync Server 管理シェルを開き、次のように入力して、すべてのユーザーを有効にするように新しい外部アクセスポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="2fc80-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="2fc80-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fc80-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

