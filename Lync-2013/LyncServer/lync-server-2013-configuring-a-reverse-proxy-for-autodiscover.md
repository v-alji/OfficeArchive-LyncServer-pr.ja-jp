---
title: 'Lync Server 2013: 自動検出用のリバースプロキシの構成'
description: 'Lync Server 2013: 自動検出用のリバースプロキシを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a reverse proxy for Autodiscover
ms:assetid: 1e3c3cc2-fe55-408b-99c4-c6e0a9252689
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945619(v=OCS.15)
ms:contentKeyID: 51541456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f7873df063c526b4e51678ded02ca11d27c5e01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433480"
---
# <a name="configuring-a-reverse-proxy-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="9ae81-103">Lync Server 2013 での自動検出用のリバースプロキシの構成</span><span class="sxs-lookup"><span data-stu-id="9ae81-103">Configuring a reverse proxy for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ae81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ae81-104">

<span> </span></span></span>

<span data-ttu-id="9ae81-105">_**最終更新日:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="9ae81-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="9ae81-106">自動検出と、自動検出を使用するクライアントのサポートでは、既存の web 公開ルールを変更したり、リバースプロキシ用の新しい web 公開ルールを作成したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae81-106">Autodiscover and the support of clients using autodiscover requires modification of an existing web publishing rule or creating a new web publishing rule for the reverse proxy.</span></span> <span data-ttu-id="9ae81-107">新しい公開ルールの変更や作成は、リバースプロキシ証明書のサブジェクト代替名の一覧を更新するかどうかに関係なく、更新の決定には依存しません。</span><span class="sxs-lookup"><span data-stu-id="9ae81-107">The modification or creation of a new publishing rule is not dependent on the decision to update or not update the subject alternative name lists on the reverse proxy certificates.</span></span>

<span data-ttu-id="9ae81-108">Lync Server 2013 の最初の自動検出サービス要求に HTTPS を使用し、リバースプロキシ証明書のサブジェクト代替名の一覧を更新する場合は、リバースプロキシの Secure Sockets Layer (SSL) リスナーに、更新された公開証明書を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae81-108">If you decide to use HTTPS for initial Lync Server 2013 Autodiscover Service requests and update the subject alternative names lists on the reverse proxy certificates, you need to assign the updated public certificate to the Secure Sockets Layer (SSL) Listener on your reverse proxy.</span></span> <span data-ttu-id="9ae81-109">外部 (公開) 証明書の必須の更新プログラムには、lyncdiscover のサブジェクト代替名 (SAN) エントリが含ま \<domain name\> れます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-109">The required update to the external (public) certificate will include the subject alternate name (SAN) entry for lyncdiscover.\<domain name\>.</span></span> <span data-ttu-id="9ae81-110">次に、外部 web サービスの既存のリスナーを変更するか、外部自動検出サービス URL 用の新しい web 公開ルールを作成する必要があります (例 **lyncdiscover.contoso.com**)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-110">You then need to modify the existing listener for the external web services or create a new web publishing rule for the external Autodiscover Service URL, for example **lyncdiscover.contoso.com**.</span></span> <span data-ttu-id="9ae81-111">フロントエンドプールとディレクタープールの外部 Lync Server 2013 Web サービスの URL (ディレクターを展開している場合) に対して web 公開ルールをまだ持っていない場合は、そのためのルールを公開する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="9ae81-111">If you do not already have a web publishing rule for the external Lync Server 2013 Web Services URL for your Front End pool and Director pool (if you have deployed Directors), you also need to publish a rule for that.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9ae81-112">リスナーに割り当てられている証明書に必要なサブジェクト名および両方のサブジェクト代替名が含まれていれば、リバースプロキシの公開ルールとリスナーは、外部 web サービスと自動検出サービスの両方をサービスすることができます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-112">The reverse proxy publishing rule and listener can service both the external web services and the Autodiscover Service, as long as the certificate assigned to the listener contains the necessary subject name and subject alternative names for both.</span></span> <span data-ttu-id="9ae81-113">Web リスナーと公開ルールの既定の構成の詳細については、「 <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Lync Server 2013 のリバースプロキシサーバー</A> をセットアップする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ae81-113">For details on the default configuration of the web listener and publishing rule, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> for more details.</span></span>



</div>

<span data-ttu-id="9ae81-114">リバースプロキシのサブジェクト代替名を更新する必要がないように、最初の自動検出サービス要求に HTTP を使用する場合は、ポート80用の web 発行ルールを作成または変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae81-114">If you decide to use HTTP for initial Autodiscover Service requests so that you do not need to update subject alternative names for the reverse proxy, you need to create or modify a web publishing rule for port 80.</span></span>

<span data-ttu-id="9ae81-115">このセクションの手順では、Microsoft Forefront Threat Management Gateway 2010 で自動検出用の web 公開ルールを作成または変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-115">The procedures in this section describe how to create or modify the web publishing rules in Microsoft Forefront Threat Management Gateway 2010 for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9ae81-116">以下の手順では、標準エディションの Forefront Threat Management Gateway (TMG) 2010 をインストールしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="9ae81-116">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010.</span></span> <span data-ttu-id="9ae81-117">別のリバースプロキシを使用している場合、手順は似ていますが、サードパーティ製品のドキュメントにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae81-117">If you are using another reverse proxy, the procedures are similar, but will need to be mapped to the documentation for the third-party product.</span></span>



</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-the-external-autodiscover-url"></a><span data-ttu-id="9ae81-118">外部の自動検出 URL 用の web 公開ルールを作成するには</span><span class="sxs-lookup"><span data-stu-id="9ae81-118">To create a web publishing rule for the external Autodiscover URL</span></span>

1.  <span data-ttu-id="9ae81-119">[ **スタート**] をクリックし、[ **プログラム**]、[ **Microsoft Forefront tmg**] の順にポイントして、[ **forefront tmg 管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-119">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="9ae81-120">左側のウィンドウで、[ **ServerName**] を展開して、[ **ファイアウォールポリシー**] を右クリックし、[ **新規作成**] をポイントして、[ **Web サイト発行ルール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-120">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="9ae81-121">[ **新しい Web 公開ルールへようこそ** ] ページで、新しい公開ルールの表示名を入力します (たとえば、LyncDiscoveryURL)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-121">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, LyncDiscoveryURL).</span></span>

4.  <span data-ttu-id="9ae81-122">**[ルールアクションの選択**] ページで、[**許可**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-122">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="9ae81-123">[ **発行の種類** ] ページで、[ **単一の Web サイトまたはロードバランサーを発行する**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-123">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="9ae81-124">[ **サーバー接続セキュリティ** ] ページで、[ **SSL を使用して公開された Web サーバーまたはサーバーファームに接続する**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-124">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="9ae81-125">[ **内部発行の詳細** ] ページの [ **内部サイト名**] に、ディレクタープールの完全修飾ドメイン名 (FQDN) を入力します (たとえば、lyncdir01)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-125">On the **Internal Publishing Details** page, in **Internal Site name**, type the fully qualified domain name (FQDN) of your Director pool (for example, lyncdir01.contoso.local).</span></span> <span data-ttu-id="9ae81-126">フロントエンドプールで外部 Web サービスの URL のルールを作成する場合は、フロントエンドプールの FQDN (たとえば、lyncpool01) を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-126">If you are creating a rule for the external Web Services URL on the Front End pool, type the FQDN of the Front End pool (for example, lyncpool01.contoso.local).</span></span>

8.  <span data-ttu-id="9ae81-127">[**内部発行の詳細**] ページの [ **Path (オプション)**] で、 **/ \* *公開するフォルダーのパスとして「_」と* 入力して、[元のホストヘッダーを転送する] を選択** します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-127">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header\*\*.</span></span>

9.  <span data-ttu-id="9ae81-128">[ **パブリック名の詳細** ] ページで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9ae81-128">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="9ae81-129">[ **要求の承認**] で、[ **このドメイン名**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-129">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="9ae81-130">[ **パブリック名**] に「lyncdiscover」と入力 **します。**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="9ae81-130">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="9ae81-131">(外部自動検出サービス URL)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-131">(the external Autodiscover Service URL).</span></span> <span data-ttu-id="9ae81-132">フロントエンドプールで外部 Web サービスの URL のルールを作成する場合は、外部 Web サービスの FQDN をフロントエンドプールに入力します (たとえば、lyncwebextpool01.contoso.com)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-132">If you are creating a rule for the external Web Services URL on the Front End pool, type the FQDN for the external Web Services on your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>
    
      - <span data-ttu-id="9ae81-133">[ **Path**] に「\* _」と入力 */\** します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-133">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="9ae81-134">_ *Select Web listener*\* ページの **web リスナー** で、更新された公開証明書を使って既存の SSL リスナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-134">On _ *Select Web Listener*\* page, in **Web Listener**, select your existing SSL Listener with the updated public certificate.</span></span>

11. <span data-ttu-id="9ae81-135">[ **認証の委任** ] ページで、[委任しない] を選択します。クライアントは、直接認証を行う **ことができ** ます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-135">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

12. <span data-ttu-id="9ae81-136">[ **ユーザー設定** ] ページで、[ **すべてのユーザー**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-136">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="9ae81-137">[ **新しい Web 公開ルールウィザードの完了** ] ページで、web 公開ルールの設定が正しいことを確認し、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-137">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="9ae81-138">Web 公開ルールの Forefront TMG リストで、追加した新しいルールをダブルクリックして **プロパティ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-138">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="9ae81-139">[ **宛先** ] タブで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9ae81-139">On the **To** tab, do the following:</span></span>
    
      - <span data-ttu-id="9ae81-140">**実際のホストヘッダーではなく、[元のホストヘッダーを転送する**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-140">Select **Forward the original host header instead of the actual one**.</span></span>
    
      - <span data-ttu-id="9ae81-141">[ **要求] は、FOREFRONT TMG コンピューターから送信され** ます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-141">Select **Requests appear to come from the Forefront TMG computer**.</span></span>

16. <span data-ttu-id="9ae81-142">[ **ブリッジ** ] タブで、次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-142">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="9ae81-143">[ **Web server**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-143">Select **Web server**.</span></span>
    
      - <span data-ttu-id="9ae81-144">[ **要求を HTTP ポートにリダイレクトする**] を選び、ポート番号に「 **8080** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-144">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="9ae81-145">[ **要求を SSL ポートにリダイレクトする**] を選び、ポート番号に「 **4443** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-145">Select **Redirect requests to SSL port**, and type **4443** for the port number.</span></span>

17. <span data-ttu-id="9ae81-146">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-146">Click **OK**.</span></span>

18. <span data-ttu-id="9ae81-147">[詳細] ウィンドウの [ **適用** ] をクリックして、変更を保存し、構成を更新します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-147">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

19. <span data-ttu-id="9ae81-148">[ **ルールのテスト** ] をクリックして、新しいルールが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-148">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-modify-an-existing-web-publishing-rule-to-add-the-external-autodiscover-san-and-url"></a><span data-ttu-id="9ae81-149">既存の web 公開ルールを変更して、外部自動検出 SAN と URL を追加するには</span><span class="sxs-lookup"><span data-stu-id="9ae81-149">To modify an existing web publishing rule to add the external Autodiscover SAN and URL</span></span>

1.  <span data-ttu-id="9ae81-150">[ **スタート**] をクリックし、[ **プログラム**]、[ **Microsoft Forefront tmg**] の順にポイントして、[ **forefront tmg 管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-150">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9ae81-151">所有している発行ルールとリスナーごとに変更を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-151">You will repeat the modification for each publishing rule and listener that you have.</span></span> <span data-ttu-id="9ae81-152">通常、これはフロントエンドプールのルールとリスナーの1つであり、展開している場合は、オプションのディレクターまたはディレクタープールに対しても使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-152">Typically, this will be one rule and listener for the Front End pools and one for the optional Directors or Director pools, if you have deployed them.</span></span>

    
    </div>

2.  <span data-ttu-id="9ae81-153">左側のウィンドウで、[ **ServerName**] を展開し、[ **ファイアウォールポリシー**] を右クリックして、該当するルールをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-153">In the left pane, expand **ServerName**, right-click **Firewall Policy**, click the applicable rule.</span></span> <span data-ttu-id="9ae81-154">[ **タスク** ] タブで、[ **選択したルールの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-154">On the **Tasks** tab, click **Edit Selected rule**.</span></span>

3.  <span data-ttu-id="9ae81-155">[ **パブリック名** ] タブの [ **適用** 対象] で、 **次の Web サイトに対する要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-155">On the **Public Name** tab, in **This rule applies to**, select **Requests for the following Web sites**.</span></span>

4.  <span data-ttu-id="9ae81-156">[ **追加**] をクリックし、新しい自動検出サイトの名前 (たとえば、"lyncdiscover.contoso.com") を入力して、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-156">Click **Add**, type the name of the new Autodiscover site (for example, “lyncdiscover.contoso.com”), and then click **OK**.</span></span>

5.  <span data-ttu-id="9ae81-157">[ **リスナー** ] タブで、[ **証明書の選択** ] をクリックし、自動検出 SAN エントリを追加した新しい証明書を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-157">On the **Listener** tab, click **Select Certificate** and assign the new certificate with the added Autodiscover SAN entries.</span></span> <span data-ttu-id="9ae81-158">リスナープロパティと Web 発行プロパティを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-158">Close the Listener and Web Publishing properties.</span></span>

6.  <span data-ttu-id="9ae81-159">[詳細] ウィンドウの [ **適用** ] をクリックして、変更を保存し、構成を更新します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-159">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

7.  <span data-ttu-id="9ae81-160">[ **ルールのテスト** ] をクリックして、新しいルールが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-160">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-port-80"></a><span data-ttu-id="9ae81-161">ポート80用の web 公開ルールを作成するには</span><span class="sxs-lookup"><span data-stu-id="9ae81-161">To create a web publishing rule for port 80</span></span>

1.  <span data-ttu-id="9ae81-162">[ **スタート**] をクリックし、[ **プログラム**]、[ **Microsoft Forefront tmg**] の順にポイントして、[ **forefront tmg 管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-162">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="9ae81-163">左側のウィンドウで、[ **ServerName**] を展開して、[ **ファイアウォールポリシー**] を右クリックし、[ **新規作成**] をポイントして、[ **Web サイト発行ルール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-163">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="9ae81-164">[ **新しい Web 公開ルールへようこそ** ] ページで、新しい公開ルールの表示名を入力します (たとえば、[Lync の自動検出 (HTTP)] など)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-164">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, Lync Autodiscover (HTTP)).</span></span>

4.  <span data-ttu-id="9ae81-165">**[ルールアクションの選択**] ページで、[**許可**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-165">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="9ae81-166">[ **発行の種類** ] ページで、[ **単一の Web サイトまたはロードバランサーを発行する**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-166">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="9ae81-167">[ **サーバー接続セキュリティ** ] ページで、[セキュリティで保護されてい **ない接続を使用して、公開された Web サーバーまたはサーバーファームに接続する**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-167">On the **Server Connection Security** page, select **Use non-secured connections to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="9ae81-168">[ **内部発行の詳細** ] ページの [ **内部サイト名**] に、フロントエンドプールの内部 Web サービス FQDN (たとえば、lyncpool01) を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-168">On the **Internal Publishing Details** page, in **Internal Site name**, type the internal Web Services FQDN for your Front End pool (for example, lyncpool01.contoso.local).</span></span>

8.  <span data-ttu-id="9ae81-169">[**内部発行の詳細**] ページの [ **Path (オプション)**] で、 **/ \* *公開するフォルダーのパスとして「_」* と入力し、[内部サイト名] フィールドで指定されたものではなく、元のホストヘッダーを [転送] を選択** します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-169">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header instead of the one specified in the Internal site name field\*\*.</span></span>

9.  <span data-ttu-id="9ae81-170">[ **パブリック名の詳細** ] ページで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9ae81-170">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="9ae81-171">[ **要求の承認**] で、[ **このドメイン名**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-171">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="9ae81-172">[ **パブリック名**] に「lyncdiscover」と入力 **します。**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="9ae81-172">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="9ae81-173">(外部自動検出サービス URL)。</span><span class="sxs-lookup"><span data-stu-id="9ae81-173">(the external Autodiscover Service URL).</span></span>
    
      - <span data-ttu-id="9ae81-174">[ **Path**] に「\* _」と入力 */\** します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-174">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="9ae81-175">_ *Select Web listener*\* ページの **web リスナー** で、web リスナーを選択するか、新しい web リスナー定義ウィザードを使用して新しい web リスナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-175">On _ *Select Web Listener*\* page, in **Web Listener**, select a Web Listener or use the New Web Listener Definition Wizard to create a new one.</span></span>

11. <span data-ttu-id="9ae81-176">[ **認証の委任** ] ページで、[委任しない] を選択し、 **クライアントで直接認証を行うことはできません**。</span><span class="sxs-lookup"><span data-stu-id="9ae81-176">On the **Authentication Delegation** page, select **No delegation, and client cannot authenticate directly**.</span></span>

12. <span data-ttu-id="9ae81-177">[ **ユーザー設定** ] ページで、[ **すべてのユーザー**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-177">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="9ae81-178">[ **新しい Web 公開ルールウィザードの完了** ] ページで、web 公開ルールの設定が正しいことを確認し、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-178">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="9ae81-179">Web 公開ルールの Forefront TMG リストで、追加した新しいルールをダブルクリックして **プロパティ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-179">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="9ae81-180">[ **ブリッジ** ] タブで、次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-180">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="9ae81-181">[ **Web server**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="9ae81-181">Select **Web server**.</span></span>
    
      - <span data-ttu-id="9ae81-182">[ **要求を HTTP ポートにリダイレクトする**] を選び、ポート番号に「 **8080** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-182">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="9ae81-183">**SSL ポートへの要求のリダイレクト** が選択されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-183">Verify that **Redirect requests to SSL port** is not selected.</span></span>

16. <span data-ttu-id="9ae81-184">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ae81-184">Click **OK**.</span></span>

17. <span data-ttu-id="9ae81-185">[詳細] ウィンドウの [ **適用** ] をクリックして、変更を保存し、構成を更新します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-185">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

18. <span data-ttu-id="9ae81-186">[ **ルールのテスト** ] をクリックして、新しいルールが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-186">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

19. <span data-ttu-id="9ae81-187">外部自動検出サービスの URL が、他の web 公開ルールで定義されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ae81-187">Verify that the external Autodiscover Service URL is not defined on any other web publishing rule.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9ae81-188">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ae81-188">See Also</span></span>


[<span data-ttu-id="9ae81-189">Lync Server 2013 のリバース プロキシ サーバーの設定</span><span class="sxs-lookup"><span data-stu-id="9ae81-189">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)  
  

<span data-ttu-id="9ae81-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ae81-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

