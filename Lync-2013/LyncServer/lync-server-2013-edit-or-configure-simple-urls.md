---
title: 'Lync Server 2013: 簡単な URL の編集または構成'
description: 'Lync Server 2013: 単純な Url を編集または構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397886"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a><span data-ttu-id="9d1a7-103">Lync Server 2013 での簡単な URL の編集または構成</span><span class="sxs-lookup"><span data-stu-id="9d1a7-103">Edit or configure simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d1a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d1a7-104">

<span> </span></span></span>

<span data-ttu-id="9d1a7-105">_**最終更新日:** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="9d1a7-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="9d1a7-106">この手順では、ローカル管理者または特権ドメイングループのメンバーシップは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-106">This procedure does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="9d1a7-107">コンピューターに標準ユーザーとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-107">You should log on to a computer as a standard user.</span></span>

<span data-ttu-id="9d1a7-108">Lync Server 2013 では、展開されている場合、フロントエンドサーバーまたはディレクター上のサービスに対して、内部および外部の通話を転送するために、シンプルな Url を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-108">Lync Server 2013 uses simple URLs to direct internal and external calls to services on the Front End Server or on the Director, if one has been deployed.</span></span> <span data-ttu-id="9d1a7-109">単純な Url の詳細については、計画ドキュメントの「 [Lync Server 2013 での単純な url の計画](lync-server-2013-planning-for-simple-urls.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-109">For more information about simple URLs, see [Planning for simple URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) in the Planning documentation.</span></span> <span data-ttu-id="9d1a7-110">簡単な Url の書式は、いくつかのオプションから選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-110">You can select the format for your simple URLs from several options.</span></span> <span data-ttu-id="9d1a7-111">これらのオプションの詳細については、計画ドキュメントの「 [Lync Server 2013 での単純な url の DNS 要件](lync-server-2013-dns-requirements-for-simple-urls.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-111">For details about these options, see [DNS requirements for simple URLs in Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) in the Planning documentation.</span></span>

<span data-ttu-id="9d1a7-112">既定では、単純な Url は、の形式 (ダイヤルインの単純な URL など) で構成され https://dialin ます。\<SIP Domain\></span><span class="sxs-lookup"><span data-stu-id="9d1a7-112">By default, simple URLs will be configured in the form of (for example, the dial-in simple URL): https://dialin.\<SIP Domain\></span></span>

<div>

## <a name="to-configure-simple-urls"></a><span data-ttu-id="9d1a7-113">単純な Url を構成するには</span><span class="sxs-lookup"><span data-stu-id="9d1a7-113">To configure simple URLs</span></span>

1.  <span data-ttu-id="9d1a7-114">[トポロジビルダー] で、[ **Lync Server** ] ノードを右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-114">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="9d1a7-115">[**簡易 URL**] ウィンドウで、編集する [**電話アクセスの URL:**] (Dial-in) または [**会議の URL:**] (Meet) のいずれかを選択し、[**URL の編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-115">In the **Simple URLs** pane, select either **Phone access URLs:** (Dial-in) or **Meeting URLs:** (Meet) to edit, and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="9d1a7-116">URL を目的の値に更新し、[**OK**] をクリックして編集した URL を保存します。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-116">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span> <span data-ttu-id="9d1a7-117">次に示す例では、ダイヤルイン URL がに変更されました https://pool01.contoso.net/dialin 。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-117">The example shown here has modified the Dial-in URL to https://pool01.contoso.net/dialin.</span></span>

4.  <span data-ttu-id="9d1a7-118">必要に応じて、同じ手順を使用して会議 URL を編集します。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-118">Edit the Meet URL by using the same steps, if necessary.</span></span>

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a><span data-ttu-id="9d1a7-119">オプションの管理用の簡易 URL を定義する</span><span class="sxs-lookup"><span data-stu-id="9d1a7-119">To define the optional Admin simple URL</span></span>

1.  <span data-ttu-id="9d1a7-120">[トポロジビルダー] で、[ **Lync Server** ] ノードを右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-120">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="9d1a7-121">[ **管理アクセスの url** ] ボックスに、Lync Server 2013 コントロールパネルへの管理アクセスに使用する単純な url を入力し、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-121">In the **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="9d1a7-122">管理 URL には、できる限りシンプルな URL を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-122">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="9d1a7-123">最も簡単なオプションは<STRONG> https://admin です。</STRONG> &lt;ドメイン &gt; 。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-123">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9d1a7-124">最初の展開後に簡易 URL を変更する場合、簡易 URL のドメイン ネーム システム (DNS) レコードと証明書に影響する変更について注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-124">If you change a simple URL after initial deployment, you must be aware of what changes impact your Domain Name System (DNS) records and certificates for simple URLs.</span></span> <span data-ttu-id="9d1a7-125">変更が単純な URL のベースに影響する場合は、DNS レコードと証明書も変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-125">If the change impacts the base of a simple URL, then you must change the DNS records and certificates as well.</span></span> <span data-ttu-id="9d1a7-126">たとえば、to から meet.contoso.com への https://lync.contoso.com/Meet https://meet.contoso.com ベース URL の変更は、lync.contoso.com を参照するように DNS レコードと証明書を変更する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-126">For example, changing from https://lync.contoso.com/Meet to https://meet.contoso.com changes the base URL from lync.contoso.com to meet.contoso.com, so you would need to change the DNS records and certificates to refer to meet.contoso.com.</span></span> <span data-ttu-id="9d1a7-127">Simple URL をからに変更した場合、 https://lync.contoso.com/Meet https://lync.contoso.com/Meetings lync.contoso.com のベース url は変わりません。そのため、DNS や証明書の変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-127">If you changed the simple URL from https://lync.contoso.com/Meet to https://lync.contoso.com/Meetings, the base URL of lync.contoso.com stays the same, so no DNS or certificate changes are needed.</span></span> <span data-ttu-id="9d1a7-128">ただし、単純な URL 名を変更した場合は必ず、各ダイレクタとフロントエンドサーバーで、 <STRONG>CsComputer</STRONG> コマンドレットを実行して変更を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d1a7-128">Whenever you change a simple URL name, however, you must run the <STRONG>Enable-CsComputer</STRONG> cmdlet on each Director and Front End Server to register the change.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9d1a7-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d1a7-129">See Also</span></span>


[<span data-ttu-id="9d1a7-130">Lync Server 2013 での簡単な URL の計画</span><span class="sxs-lookup"><span data-stu-id="9d1a7-130">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="9d1a7-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d1a7-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

