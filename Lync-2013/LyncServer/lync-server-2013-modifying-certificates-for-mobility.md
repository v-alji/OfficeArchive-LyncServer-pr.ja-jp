---
title: 'Lync Server 2013: モビリティに合わせた証明書の変更'
description: 'Lync Server 2013: モバイル用の証明書を変更しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modifying certificates for mobility
ms:assetid: 4e9107af-20f4-4c2a-8c98-ca35b39a4e2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690015(v=OCS.15)
ms:contentKeyID: 48184120
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 099122b1773c3f15d8ae0034ee5fa404225cdfd2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445695"
---
# <a name="modifying-certificates-for-mobility-in-lync-server-2013"></a><span data-ttu-id="b5a01-103">Lync Server 2013 でのモビリティに合わせた証明書の変更</span><span class="sxs-lookup"><span data-stu-id="b5a01-103">Modifying certificates for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5a01-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5a01-104">

<span> </span></span></span>

<span data-ttu-id="b5a01-105">_**最終更新日:** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="b5a01-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="b5a01-106">Lync 環境とモバイルクライアント間のセキュリティで保護された接続をサポートするために、ディレクタープール、フロントエンドプール、リバースプロキシのセキュリティで保護されたソケットレイヤー (SSL) 証明書を更新する必要があります。これには、追加のサブジェクト代替名 (SAN) エントリが必要です。</span><span class="sxs-lookup"><span data-stu-id="b5a01-106">To support secure connections between your Lync environment and your mobile clients, the Secure Socket Layer (SSL) certificates for your Director pool, Front End pool, and reverse proxy are going to need to be updated with some additional subject alternative name (SAN) entries.</span></span> <span data-ttu-id="b5a01-107">モビリティの証明書の要件の詳細について確認する必要がある場合は、「 [Lync Server 2013 でのモビリティの技術要件](lync-server-2013-technical-requirements-for-mobility.md)」の「証明書の要件」セクションを参照してください。基本的に、追加の SAN エントリが含まれる証明機関から新しい証明書を取得し、この記事の手順を使ってそれらの証明書を追加する必要が</span><span class="sxs-lookup"><span data-stu-id="b5a01-107">If you need to check out more details about the certificate requirements for mobility, see the Certificate Requirements section in [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), but basically you’ll need to get new certificates from the Certificate Authority with the additional SAN entries included, and then add those certificates using this article’s steps.</span></span>

<span data-ttu-id="b5a01-108">もちろん、作業を開始する前に、証明書に既に登録されているサブジェクトの代替名を知っておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-108">Of course before you begin, it’s usually a good idea to know what subject alternative names your certificates already have.</span></span> <span data-ttu-id="b5a01-109">まだ設定されているものがわからない場合は、さまざまな方法で確認できます。このオプションでは、ユーザーがこの情報を表示するために、[ **Get-CsCertificate** ] とその他の PowerShell コマンドを実行することができます。これは、既定ではデータが切り捨てられるため、必要なすべてのプロパティを表示することができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-109">If you’re not sure what’s already been configured, there are a lot of ways to find out. While the option’s there to run the **Get-CsCertificate** and other PowerShell commands to view this information, (which we walk through below) by default that data will be truncated, so you may not get to see all the properties you need.</span></span> <span data-ttu-id="b5a01-110">証明書とそのすべてのプロパティについて詳しく理解するには、Microsoft 管理コンソール (MMC) に移動して、証明書スナップインを読み込むか (以下を参照)、Lync Server 展開ウィザードを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b5a01-110">In order to get a good look at the certificate and all its properties, you can go to the Microsoft Management Console (MMC) and load the Certificates snap-in (which we also walk through below), or you can just check in the Lync Server Deployment Wizard.</span></span>

<span data-ttu-id="b5a01-111">上で説明したように、次の手順では、Lync Server 管理シェルと MMC を使用して証明書を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-111">As noted above, the following steps will walk you through updating the certificates using the Lync Server Management Shell and the MMC.</span></span> <span data-ttu-id="b5a01-112">代わりに Lync Server Deployment ウィザードで証明書ウィザードを使用する場合は、ディレクターまたはディレクタープールを構成している場合は、 [Lync server 2013 でディレクターの証明書を構成](lync-server-2013-configure-certificates-for-the-director.md) することができます (存在しない可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="b5a01-112">If you’re interested in using the Certificate Wizard in the Lync Server Deployment Wizard for this instead, you can check [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md) out for the Director or Director pool, if you configured one (you may not have).</span></span> <span data-ttu-id="b5a01-113">フロントエンドサーバーまたはフロントエンドプールについては、「 [Lync Server 2013 でサーバーの証明書を構成](lync-server-2013-configure-certificates-for-servers.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a01-113">For the Front End Server or Front End pool, you’ll want to see [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span></span>

<span data-ttu-id="b5a01-114">最後に、Lync Server 2013 環境に1つの既定の証明書がある場合、または既定の証明書 (web サービス以外はすべて) が存在する場合があることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="b5a01-114">One last thing to keep in mind is that you may have a single Default certificate in your Lync Server 2013 environment, or you may have separate certificates for Default (which is everything but the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="b5a01-115">どのような構成にしても、これらの手順は役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-115">Whatever your configuration, these steps should help you out.</span></span>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="b5a01-116">Lync Server 管理シェルを使用して新しいサブジェクト別の名前を使用して証明書を更新するには</span><span class="sxs-lookup"><span data-stu-id="b5a01-116">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="b5a01-117">ローカルの管理者権限と権限を持つアカウントを使用して、Lync Server 2013 サーバーにログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-117">You need to log on to your Lync Server 2013 server using an account that has local administrator rights and permissions.</span></span> <span data-ttu-id="b5a01-118">さらに、手順12以降で PowerShell **要求-CsCertificate** を実行している場合、アカウントは指定された証明機関 (CA) に対する権利を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-118">Additionally, if you’re running the PowerShell **Request-CsCertificate** in Steps 12 and beyond, the account needs to have rights to the specified Certificate Authority (CA).</span></span>

2.  <span data-ttu-id="b5a01-119">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b5a01-120">更新された証明書を割り当てる前に、サーバーに割り当てられている証明書と使用の種類を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-120">Before you can assign an updated certificate, you’ll need to find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="b5a01-121">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-121">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="b5a01-122">前の手順からの出力を確認して、複数の使用に対して1つの証明書が割り当てられているかどうか、または使用ごとに異なる証明書が割り当てられているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-122">Review the output from the previous step to see whether a single certificate has been assigned for multiple uses, or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="b5a01-123">証明書がどのように使われているかを確認するには、Use パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a01-123">Look in the Use parameter to find out how a certificate’s being used.</span></span> <span data-ttu-id="b5a01-124">表示された証明書の Thumbprint パラメーターと比較して、同じ証明書に複数の使用が含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-124">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span> <span data-ttu-id="b5a01-125">拇印のパラメーターを常に把握しておきます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-125">Keep your eye on the Thumbprint parameter.</span></span>

5.  <span data-ttu-id="b5a01-126">証明書を更新します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-126">Update the certificate.</span></span> <span data-ttu-id="b5a01-127">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-127">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="b5a01-128">たとえば、 **CsCertificate** コマンドレットで、既定値を使用する証明書が表示され、もう1つは Webservices internal を使用していて、もう1つは WebServicesExternal を使用していて、それらのすべてに同じ拇印値が含まれている場合、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-128">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, you should type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="b5a01-129">**重要:**</span><span class="sxs-lookup"><span data-stu-id="b5a01-129">**Important:**</span></span>
    
    <span data-ttu-id="b5a01-130">各使用に個別の証明書が割り当てられている場合 (上記でチェックした拇印の値が各証明書に対して異なる場合) は、上の例のように、複数の種類の **Set-cscertificate** コマンドレットを実行し **ない** ことが重要です。</span><span class="sxs-lookup"><span data-stu-id="b5a01-130">If a separate certificate is assigned for each use (so the Thumbprint value you checked above is different for each certificate), it’s vital that you **don’t** run the **Set-CsCertificate** cmdlet with multiple types, as in the example above.</span></span> <span data-ttu-id="b5a01-131">この場合は、使用するたびに、 **Set-CsCertificate** コマンドレットを個別に実行します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-131">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="b5a01-132">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-132">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="b5a01-133">証明書 (または証明書) を表示するには、[ **スタート**] をクリックし、[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-133">To view the certificate (or certificates), click **Start**, click **Run…**.</span></span> <span data-ttu-id="b5a01-134">「MMC」と入力して Microsoft 管理コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-134">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="b5a01-135">MMC のメニューで、[ **ファイル**]、[ **スナップインの追加と削除**] の順番に選択し、[証明書] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-135">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="b5a01-136">**[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-136">Click **Add**.</span></span> <span data-ttu-id="b5a01-137">メッセージが表示されたら、[ **コンピューターアカウント**] を選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-137">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="b5a01-138">証明書が配置されているサーバーの場合は、[ **ローカルコンピューター**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-138">If this is the server where the certificate’s located, select **Local computer**.</span></span> <span data-ttu-id="b5a01-139">証明書が別のコンピューターにある場合は、 **別のコンピューター** を選んでから、コンピューターの完全修飾ドメイン名を入力するか、[ **参照** ] をクリックして **選択するオブジェクト名** を入力し、コンピューターの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-139">If the certificate’s located on another computer, you should select **Another computer**, and then you can either type in the fully qualified domain name of the computer, or click **Browse** in **Enter the object name to select**, and type the name of the computer.</span></span> <span data-ttu-id="b5a01-140">[ **名前の確認**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-140">Click **Check Names**.</span></span> <span data-ttu-id="b5a01-141">コンピューターの名前が解決されると、下線が引かれます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-141">When the name of the computer resolves, it’ll be underlined.</span></span> <span data-ttu-id="b5a01-142">[ **OK**] をクリックし、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5a01-142">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="b5a01-143">[ **OK** ] をクリックして選択内容を確定し、[スナップインの **追加と削除** ] ダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-143">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>

9.  <span data-ttu-id="b5a01-144">証明書のプロパティを表示するには、[ **証明書**]、[ **個人用**] の順に展開し、[ **証明書**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-144">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="b5a01-145">表示する証明書を選択し、証明書を右クリックして、[ **開く**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-145">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="b5a01-146">**証明書** ビューで、[**詳細**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-146">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="b5a01-147">ここでは、[ **件名** ] を選択して証明書のサブジェクト名を選択し、割り当てられたサブジェクト名と関連付けられたプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-147">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="b5a01-148">割り当てられたサブジェクト別の名前を表示するには、[ **件名の代替名**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-148">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="b5a01-149">すべての割り当てられた件名の代替名がここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-149">All assigned subject alternative names are displayed here.</span></span> <span data-ttu-id="b5a01-150">ここで見つかった件名の代替名は、既定で **DNS 名** の種類になっています。</span><span class="sxs-lookup"><span data-stu-id="b5a01-150">The subject alternative names found here are of type **DNS Name** by default.</span></span> <span data-ttu-id="b5a01-151">次のメンバーが表示されている必要があります (すべてのメンバーが DNS host (A または IPv6 AAAA の場合は、完全修飾ドメイン名になります)。</span><span class="sxs-lookup"><span data-stu-id="b5a01-151">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="b5a01-152">このプールのプール名、または1つのサーバー名 (プールではない場合)</span><span class="sxs-lookup"><span data-stu-id="b5a01-152">Pool name for this pool, or the single server name if this isn’t a pool</span></span>
    
      - <span data-ttu-id="b5a01-153">証明書が割り当てられているサーバー名</span><span class="sxs-lookup"><span data-stu-id="b5a01-153">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="b5a01-154">単純な URL レコード、通常は会議とダイヤルイン</span><span class="sxs-lookup"><span data-stu-id="b5a01-154">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="b5a01-155">Web サービスの内部および Web サービス外部名 (webpool01.contoso.net、webpool01.contoso.com など) は、トポロジビルダーでの選択肢と、[web サービスの変更] オプションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="b5a01-155">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="b5a01-156">既に割り当てられている場合は、lyncdiscover です。\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="b5a01-156">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="b5a01-157">lyncdiscoverinternal。\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="b5a01-157">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="b5a01-158">記録.</span><span class="sxs-lookup"><span data-stu-id="b5a01-158">records.</span></span>
    
    <span data-ttu-id="b5a01-159">最後の項目は、lyncdiscover と lyncdiscoverinternal の SAN エントリがある場合に最も興味を持っている項目です。</span><span class="sxs-lookup"><span data-stu-id="b5a01-159">The last item is what you’re most interested in – if there’s a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="b5a01-160">複数の証明書を確認する場合は、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-160">Repeat these steps if you have multiple certificates to check.</span></span> <span data-ttu-id="b5a01-161">この情報を取得したら、証明書ビューと MMC を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="b5a01-161">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="b5a01-162">自動検出サービスのサブジェクトの別名が表示されておらず、既定の Webservices 内部と WebServiceExternal 外部タイプに対して単一の既定の証明書を使用している場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b5a01-162">If an Autodiscover Service subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="b5a01-163">Lync Server 管理シェルのコマンドラインプロンプトで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-163">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="b5a01-164">SIP ドメインが複数ある場合は、新しい AllSipDomain パラメーターを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="b5a01-164">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="b5a01-165">代わりに、DomainName パラメーターを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-165">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="b5a01-166">DomainName パラメーターを使用する場合は、lyncdiscoverinternal レコードと lyncdiscover レコードの FQDN を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-166">When you use the DomainName parameter, you’ve got to define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="b5a01-167">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-167">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="b5a01-168">証明書を割り当てるには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-168">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="b5a01-169">"拇印" は、新しく発行された証明書に対して表示される拇印です。</span><span class="sxs-lookup"><span data-stu-id="b5a01-169">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="b5a01-170">既定の証明書を使用する場合、内部の自動検出 SAN が見つからない場合は、次の手順を実行します。 WebServicesExternal</span><span class="sxs-lookup"><span data-stu-id="b5a01-170">For a missing internal Autodiscover SAN when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="b5a01-171">Lync Server 管理シェルのコマンドラインプロンプトで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-171">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="b5a01-172">SIP ドメインが複数ある場合は、新しい AllSipDomain パラメーターを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="b5a01-172">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="b5a01-173">代わりに、DomainName パラメーターを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-173">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="b5a01-174">DomainName パラメーターを使用する場合は、SIP ドメイン FQDN に適切なプレフィックスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-174">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="b5a01-175">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-175">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="b5a01-176">外部の自動検出サブジェクトの代替名が見つからない場合は、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-176">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="b5a01-177">SIP ドメインが複数ある場合は、新しい AllSipDomain パラメーターを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="b5a01-177">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="b5a01-178">代わりに、DomainName パラメーターを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-178">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="b5a01-179">DomainName パラメーターを使用する場合は、SIP ドメイン FQDN に適切なプレフィックスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-179">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="b5a01-180">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-180">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="b5a01-181">個々の証明書の種類を割り当てるには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a01-181">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="b5a01-182">"拇印" は、新しく発行された個々の証明書に対して表示される拇印です。</span><span class="sxs-lookup"><span data-stu-id="b5a01-182">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b5a01-183">手順12と13は、実行しているアカウントが適切な権限で証明機関にアクセスしている場合にのみ実行されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b5a01-183">Just to note, Steps 12 and 13 should be run only if the account running them has access to the Certificate Authority with appropriate permissions.</span></span> <span data-ttu-id="b5a01-184">これらのアクセス許可が付与されているアカウントでログインできない場合、または証明書にパブリックまたはリモートの証明機関を使用している場合は、この記事の上部にある「Lync Server 展開ウィザード」で操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a01-184">If you are unable to log in with an account that’s got those permissions, or if you’re using a public or remote Certificate Authority for your certificates, you would need to request them through the Lync Server Deployment Wizard, which was touched on at the top of the article.</span></span>

    
    <span data-ttu-id="b5a01-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5a01-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

