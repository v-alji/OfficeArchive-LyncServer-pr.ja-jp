---
title: インスタントメッセージング (IM) のファイル転送と URL フィルタリングの構成
description: インスタントメッセージング (IM) のファイル転送と URL フィルタリングを構成する。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring file transfer and URL filtering for instant messaging (IM)
ms:assetid: 115a1a2c-599f-474c-a063-52f7144b5246
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520952(v=OCS.15)
ms:contentKeyID: 48183440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92f11c3f3bb924c1d92361c2635bfb37e1f03175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433109"
---
# <a name="configuring-file-transfer-and-url-filtering-for-instant-messaging-im-in-lync-server-2013"></a><span data-ttu-id="2fe80-103">Lync Server 2013 でのインスタントメッセージング (IM) のファイル転送と URL フィルタリングの構成</span><span class="sxs-lookup"><span data-stu-id="2fe80-103">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fe80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fe80-104">

<span> </span></span></span>

<span data-ttu-id="2fe80-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2fe80-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2fe80-106">インテリジェント IM フィルターツールは、ユーザーエクスペリエンスの低下を最小限に抑えて、最も一般的な種類のウイルスの蔓延に対して Lync Server 2013 の展開を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-106">The Intelligent IM Filter tool helps protect your Lync Server 2013 deployment against the spread of the most common forms of viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="2fe80-107">インテリジェント IM フィルターを使用して、組織外のエンドポイントからの不要または有害なインスタントメッセージをブロックするようにフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-107">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="2fe80-108">フィルターを設定するには、ブロックする必要があるものを決定するために使用する条件を指定します。たとえば、特定のプレフィックスと特定の拡張子を持つファイルが含まれるハイパーリンクを含むインスタントメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-108">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks with specific prefixes and files with specific extensions.</span></span>

<span data-ttu-id="2fe80-109">インテリジェント IM フィルターでは、次の機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-109">Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="2fe80-110">強化された URL フィルター機能。</span><span class="sxs-lookup"><span data-stu-id="2fe80-110">Enhanced URL filtering.</span></span>

  - <span data-ttu-id="2fe80-111">拡張されたファイル転送フィルター機能。</span><span class="sxs-lookup"><span data-stu-id="2fe80-111">Enhanced file transfer filtering.</span></span>

<span data-ttu-id="2fe80-112">インテリジェント IM フィルターを構成するには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-112">Configuring Intelligent IM Filter includes the following:</span></span>

  - <span data-ttu-id="2fe80-113">URL フィルタリングを構成する。</span><span class="sxs-lookup"><span data-stu-id="2fe80-113">Configuring URL filtering.</span></span>

  - <span data-ttu-id="2fe80-114">ファイル転送フィルター処理を構成します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-114">Configuring file transfer filtering.</span></span>

<div>

## <a name="how-filtering-options-are-applied-to-instant-messages"></a><span data-ttu-id="2fe80-115">フィルターオプションがインスタントメッセージに適用される方法</span><span class="sxs-lookup"><span data-stu-id="2fe80-115">How Filtering Options Are Applied to Instant Messages</span></span>

<span data-ttu-id="2fe80-116">インテリジェント IM メッセージフィルターツールを展開する前に、メールが1つの Lync Server 2013 サーバーから別のサーバーにルーティングされるときのフィルターオプションの適用方法を理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-116">Before you deploy the Intelligent IM Message Filter tool, you need to understand how filtering options are applied as messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="2fe80-117">これらのフィルターオプションの適用方法は、サーバーが1つの組織内に配置されているか、組織の境界を超えているかに関係なく一貫しています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-117">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="2fe80-118">この一貫性は、カスタマイズされた通知や警告テキストをメッセージに挿入し、サーバー間で送信する方法に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-118">This consistency applies to the way that the customized notice and warning texts are inserted into messages and sent across servers.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2fe80-119">インスタントメッセージフィルターは、メッセージ内の Url を処理するために必要な CPU リソースの量を増やします。</span><span class="sxs-lookup"><span data-stu-id="2fe80-119">The instant message filter increases the amount of CPU resources required to process URLs in a message.</span></span> <span data-ttu-id="2fe80-120">また、このような CPU 需要の増加は、Lync Server のパフォーマンスにも影響します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-120">This increase in CPU demand also affects the performance of Lync Server.</span></span>



</div>

<span data-ttu-id="2fe80-121">Lync Server コントロールパネルの **IM とプレゼンス** グループで [ **URL フィルター** ] ページを使うと、一部またはすべてのハイパーリンクをブロックしたり、警告を構成したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-121">By using the **URL Filter** page in the **IM and Presence** group in Lync Server Control Panel, you can block some or all hyperlinks or configure a warning.</span></span> <span data-ttu-id="2fe80-122">**ハイパーリンクのプレフィックス** オプションを選択したときに **警告メッセージを送信** すると、ハイパーリンクが含まれているインスタントメッセージの先頭に警告が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-122">The warning is inserted at the beginning of an instant message that contains a hyperlink when you choose the **Hyperlink prefix** option **Send warning message**.</span></span>

<span data-ttu-id="2fe80-123">インスタントメッセージがあるサーバーから別のサーバーに移動する場合、次の一般的なガイドラインが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-123">When an instant message travels from one server to another, the following general guidelines apply:</span></span>

  - <span data-ttu-id="2fe80-124">サーバーがインスタントメッセージをブロックしている場合 ([ **Url フィルター** ] ページで [**ファイル拡張子を含む url をブロック\*\*\*\*する] チェック** ボックスをオンにしている場合、または [ハイパーリンクの **接頭辞**] オプションを選択した場合)、クライアントにエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-124">If a server blocks an instant message (because you selected the **Block URLs with file extension** check box on the **URL Filter** page or because you chose the **Hyperlink prefix** option **Block hyperlinks**), an error message is returned to the client.</span></span> <span data-ttu-id="2fe80-125">後続のサーバーはこのインスタントメッセージを受け取りません。</span><span class="sxs-lookup"><span data-stu-id="2fe80-125">Subsequent servers do not receive this instant message.</span></span>

  - <span data-ttu-id="2fe80-126">サーバー (Server1) がアクティブなハイパーリンクが含まれているインスタントメッセージに警告を追加した場合、その後のサーバー (Server2) は、インスタントメッセージに表示されているこのアクティブハイパーリンクに基づいて別のアクションを実行し、インスタントメッセージをブロックするか、または警告を追加します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-126">If a server (Server1) adds a warning to an instant message that contains an active hyperlink, a subsequent server (Server2) that receives this instant message can still take a different action based on this active hyperlink present in the instant message and block the instant message or add a warning.</span></span> <span data-ttu-id="2fe80-127">Server2 がこの URL に対して警告を追加するように構成されている場合、Server1 によって追加された以前の警告が削除され、Server2 に設定されている警告がインスタントメッセージの先頭に追加されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-127">If Server2 is configured only to add a warning for this URL, the earlier warning added by Server1 is removed, and the warning configured on Server2 is added to the beginning of the instant message.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2fe80-128">混在環境で Lync Server 2013 を実行している場合、インテリジェント IM フィルターアプリケーションを使用するために必要な最小バージョンは、Live Communications Server 2005 SP1 です。</span><span class="sxs-lookup"><span data-stu-id="2fe80-128">If you are running Lync Server 2013 in a mixed environment, Live Communications Server 2005 with SP1 is the minimum version required to use the Intelligent IM Filter application.</span></span> <span data-ttu-id="2fe80-129">インテリジェント IM フィルターは、SP1 が適用されていない Live Communications Server 2005 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2fe80-129">The Intelligent IM Filter is not supported on Live Communications Server 2005 without SP1.</span></span>



</div>

<div>

## <a name="url-filtering"></a><span data-ttu-id="2fe80-130">URL フィルター</span><span class="sxs-lookup"><span data-stu-id="2fe80-130">URL Filtering</span></span>

<span data-ttu-id="2fe80-131">Url は、ハイパーリンクのプレフィックスに基づいてフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-131">URLs are filtered according to their hyperlink prefix.</span></span> <span data-ttu-id="2fe80-132">有効なプレフィックスの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-132">The following examples are valid prefixes:</span></span>

  - <span data-ttu-id="2fe80-133">www \* 。</span><span class="sxs-lookup"><span data-stu-id="2fe80-133">www\*.</span></span>

  - <span data-ttu-id="2fe80-134">プロトコル.</span><span class="sxs-lookup"><span data-stu-id="2fe80-134">ftp.</span></span>

  - <span data-ttu-id="2fe80-135">http</span><span class="sxs-lookup"><span data-stu-id="2fe80-135">http:</span></span>

<span data-ttu-id="2fe80-136">任意の URL フィルター処理を実行するようにインスタントメッセージフィルターを構成していない場合、インスタントメッセージに含まれるすべての Url は、そのままサーバー経由で転送されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-136">If you do not configure the instant message filter to perform any URL filtering, all URLs contained in instant messages are passed unmodified through the server.</span></span> <span data-ttu-id="2fe80-137">URL フィルタリングを実行するようにインスタントメッセージフィルターを構成した場合、インスタントメッセージ内の Url は、[ **Url フィルターの編集** ] または [ **新しい url フィルター** ] ダイアログボックスで選択したオプションに基づいてフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-137">If you configure the instant message filter to perform URL filtering, URLs in instant messages are filtered according to the options that you select in the **Edit URL Filter** or **New URL Filter** dialog box.</span></span>

  - <span data-ttu-id="2fe80-138">**URL フィルターを有効にする**   このオプションでは、グローバル展開または選択したサイトの URL フィルタリングが有効になります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-138">**Enable URL filter**   This option enables URL filtering for the global deployment or for the site that you select.</span></span>

  - <span data-ttu-id="2fe80-139">**ファイル拡張子を持つ url をブロック** する  インスタントメッセージフィルターは、[**ファイルフィルターの編集**] ダイアログボックスの [**ブロックするファイルの種類の拡張子**] の下に一覧表示されている拡張子を持つファイルを含む、アクティブなイントラネットまたはインターネット URL をブロックします。</span><span class="sxs-lookup"><span data-stu-id="2fe80-139">**Block URLs with file extension**   The instant message filter blocks any active intranet or Internet URL that contains a file with an extension listed under **File type extensions to block** in the **Edit File Filter** dialog box.</span></span> <span data-ttu-id="2fe80-140">URL がブロックされると、送信者にエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-140">When a URL is blocked, an error message is displayed to the sender.</span></span> <span data-ttu-id="2fe80-141">このオプションは、[ **ブロックするファイルの種類の拡張子**] で定義されているすべてのファイル拡張子について、他のすべてのフィルターオプションよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-141">When selected, this option takes precedence over all other filtering options for any file extensions defined under **File type extensions to block**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="2fe80-142">ファイル拡張子のフィルター処理は、標準のファイル名に制限されています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-142">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="2fe80-143">他の名前に埋め込まれているファイル拡張子では、フィルター処理が機能しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-143">Filtering may not work with file extensions embedded in other names.</span></span>

    
    </div>

<span data-ttu-id="2fe80-144">インスタントメッセージの会話でハイパーリンクを処理する方法を構成するには、[ **ハイパーリンクの接頭** 文字] で次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-144">To configure how hyperlinks are handled in instant message conversations, select one of the following options under **Hyperlink prefix**:</span></span>

  - <span data-ttu-id="2fe80-145">**フィルター処理しない**   メッセージ内の Url は、サーバー経由で送信されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-145">**Do not filter**   URLs in messages are sent through the server.</span></span> <span data-ttu-id="2fe80-146">このオプションを選択すると、[ **許可] メッセージ** ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-146">When you choose this option, the **Allow message** box appears.</span></span> <span data-ttu-id="2fe80-147">[ **許可] メッセージ** ボックスで、ハイパーリンクが含まれている各インスタントメッセージの先頭に挿入する通知を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-147">In the **Allow message** box, specify the notice that you want to insert at the beginning of each instant message containing hyperlinks.</span></span> <span data-ttu-id="2fe80-148">この通知は、65535文字以下で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-148">This notice can consist of no more than 65535 characters.</span></span>

  - <span data-ttu-id="2fe80-149">**ハイパーリンクをブロック**   する  アクティブなハイパーリンクを含むインスタントメッセージの配信が Lync Server によってブロックされ、送信者にエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-149">**Block hyperlinks**   Delivery of instant messages containing active hyperlinks is blocked by Lync Server, and an error message is displayed to the sender.</span></span>

  - <span data-ttu-id="2fe80-150">**警告メッセージを送信**   する  Lync Server では、インスタントメッセージ内にアクティブなハイパーリンクが許可されていますが、警告が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-150">**Send warning message**   Lync Server permits active hyperlinks in instant messages, but it includes a warning.</span></span> <span data-ttu-id="2fe80-151">このオプションを選択すると、 **警告メッセージ** ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-151">When you choose this option, the **Warning message** box appears.</span></span> <span data-ttu-id="2fe80-152">[ **警告メッセージ** ] ボックスに、有効なハイパーリンクが含まれたインスタントメッセージに含める警告を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-152">In the **Warning message** box, you must type the warning that you want to include with instant messages containing valid hyperlinks.</span></span> <span data-ttu-id="2fe80-153">たとえば、この警告は、不明なリンクをクリックしたときに発生する可能性のある危険を示す可能性があります。または、組織の関連ポリシーと要件を参照している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-153">For example, this warning might state the potential dangers of clicking an unknown link, or it might refer to your organization’s relevant policies and requirements.</span></span> <span data-ttu-id="2fe80-154">警告は65535文字以下でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2fe80-154">The warning can be no more than 65535 characters.</span></span>

<span data-ttu-id="2fe80-155">[ハイパーリンクの **ブロック** ] または [ **警告メッセージの送信**] を選択した場合は、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-155">If you select **Block hyperlinks** or **Send warning message**, the following options are available:</span></span>

  - <span data-ttu-id="2fe80-156">**ローカルイントラネットのハイパーリンクを除外**   する  インスタントメッセージフィルターは、インターネットの Url のみをブロックします。</span><span class="sxs-lookup"><span data-stu-id="2fe80-156">**Exclude local intranet hyperlinks**   The instant message filter blocks only Internet URLs.</span></span> <span data-ttu-id="2fe80-157">イントラネット内の場所の Url は、サーバー経由では変更されません。</span><span class="sxs-lookup"><span data-stu-id="2fe80-157">URLs for locations within your intranet are passed unmodified through the server.</span></span> <span data-ttu-id="2fe80-158">ただし、Lync Server を実行している個々のサーバーがパスするイントラネット Url は、イントラネットゾーンの一部と見なされるローカル web サイトの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-158">However, the intranet URLs that individual servers running Lync Server pass depend on which types of local websites are considered part of their intranet zone.</span></span> <span data-ttu-id="2fe80-159">サーバーのイントラネットゾーンの設定を確認するには、「 [Lync server 2013 の既定の URL フィルターを変更](lync-server-2013-modify-the-default-url-filter.md)する」の手順の「Internet Explorer でイントラネット設定を構成する」の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2fe80-159">To check a server’s intranet zone settings, see the “To configure your intranet settings in Internet Explorer” procedure in [Modify the default URL filter in Lync Server 2013](lync-server-2013-modify-the-default-url-filter.md).</span></span>

  - <span data-ttu-id="2fe80-160">**ハイパーリンクのプレフィックスをフィルター処理**   する  ブロックする接頭番号を選択するには、[ **選択**] をクリックし、[ **ハイパーリンクの接頭** 文字] で [ **ハイパーリンク** のプレフィックス] の一覧にプレフィックスを追加します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-160">**Filter these hyperlink prefixes**   To choose which prefixes you want to block, click **Select**, and then, in **Select Hyperlink Prefix**, add the prefixes to the **Hyperlink prefixes** list.</span></span>
    
    <span data-ttu-id="2fe80-161">**Href** を除くすべてのプレフィックスは、ピリオドまたはコロンで終わるか、アスタリスクの後にピリオドが続いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-161">All prefixes except **href** must end with a period or a colon, or an asterisk followed by a period.</span></span> <span data-ttu-id="2fe80-162">有効なプレフィックスには、アスタリスク () を除く、有効な URL 文字のセット内の任意の文字を含めることができ \* ます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-162">Valid prefixes can contain any characters in the set of valid URL characters except the asterisk (\*).</span></span> <span data-ttu-id="2fe80-163">有効な URL 文字のセットは次のとおりです。 \# \* +/0123456789 = @ABCDEFGHIJKLMNOPQRSTUVWXYZ ^ \_ \` ABCDEFGHIJKLMNOPQRSTUVWXYZ | ~</span><span class="sxs-lookup"><span data-stu-id="2fe80-163">The set of valid URL characters is: \#\*+/0123456789=@ABCDEFGHIJKLMNOPQRSTUVWXYZ^\_\` abcdefghijklmnopqrstuvwxyz|~</span></span>

</div>

<div>

## <a name="file-transfer-filtering"></a><span data-ttu-id="2fe80-164">ファイル転送フィルター処理</span><span class="sxs-lookup"><span data-stu-id="2fe80-164">File Transfer Filtering</span></span>

<span data-ttu-id="2fe80-165">フィルター転送フィルターは、インスタントメッセージと会議の両方に影響します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-165">Filter transfer filtering affects both instant messages and conferences.</span></span> <span data-ttu-id="2fe80-166">会議の場合、これらの設定は、Office Live Meeting 2007 クライアントとマルチメディア再生機能の配布資料機能に影響します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-166">For conferences, these settings affect the handout feature in the Office Live Meeting 2007 client and multimedia playback features.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2fe80-167">Lync Server では、ファイル転送設定オプションも提供されています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-167">Lync Server also offers file transfer setting options.</span></span> <span data-ttu-id="2fe80-168">このサーバー側のオプションは、Lync Server で利用可能なクライアント側のコントロールに加えて提供されています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-168">This server-side option is offered in addition to the client-side controls available in Lync Server.</span></span>



</div>

<span data-ttu-id="2fe80-169">Office Live Meeting 2007 クライアントで配布資料機能を使用している場合、またはすべてのファイルの種類に対してマルチメディア再生機能を使用している場合、インスタントメッセージの会話中にファイル転送をフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-169">You can filter file transfers during instant message conversations, when you are using the handout feature in the Office Live Meeting 2007 client, and for multimedia playback features for all file types.</span></span> <span data-ttu-id="2fe80-170">ファイル転送を制御するために、次のオプションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-170">You can set the following options to control file transfers:</span></span>

  - <span data-ttu-id="2fe80-171">**ファイルフィルターを有効にする**   このオプションでは、グローバル展開または選択したサイトに対してファイルのフィルター処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-171">**Enable file filter**   This option enables file filtering for the global deployment or for the site that you select.</span></span>
    
    <span data-ttu-id="2fe80-172">ファイルフィルターを有効にすると、[ **ファイル送信**] で次のいずれかのオプションを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="2fe80-172">When you enable the file filter, you can choose one of the following options in **File transfer**:</span></span>
    
      - <span data-ttu-id="2fe80-173">**特定の種類のファイルをブロック**   する  ブロックするファイル拡張子の一覧を指定して、サーバーによってフィルター処理されるファイル転送要求を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-173">**Block specific file types**   You specify which file transfer requests are filtered by the server by specifying a list of file extensions to block.</span></span> <span data-ttu-id="2fe80-174">リスト内のエントリには、すべての標準文字を含めることができますが、ワイルドカード文字 () は使用できません \* 。</span><span class="sxs-lookup"><span data-stu-id="2fe80-174">Entries in the list can contain all standard characters, but not the wildcard character (\*).</span></span> <span data-ttu-id="2fe80-175">Office Live Meeting 2007 クライアントでは、配布資料機能は有効になっていますが、この拡張子のファイルをアップロードまたはダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2fe80-175">In the Office Live Meeting 2007 client the handout feature is enabled, but any file with this extension cannot be uploaded or downloaded.</span></span> <span data-ttu-id="2fe80-176">[ **Url フィルター** ] タブに表示されている url フィルターの設定で、[**ファイル拡張子を含む url をブロック** する] チェックボックスをオンにした場合、url フィルターはこの同じリストを使って、これらのファイル拡張子を含むアクティブなハイパーリンクをブロックします。</span><span class="sxs-lookup"><span data-stu-id="2fe80-176">If you select the **Block URLs with file extension** check box on the settings for a URL filter listed on the **URL Filter** tab, the URL filter uses this same list to block active hyperlinks that contain any of these file extensions.</span></span> <span data-ttu-id="2fe80-177">ブロックするファイルの種類を選択するには、[ **選択**] をクリックし、[ **ファイルの種類の選択**] で、選択したファイルの種類の **拡張子** の一覧にファイルの種類の拡張子を追加します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-177">To choose which file types you want to block, click **Select**, and then, in **Select File Type**, add the file type extensions to the **Selected file type extensions** list.</span></span>
    
      - <span data-ttu-id="2fe80-178">**すべてブロック**   サーバーは、ファイル転送要求を含むすべてのインスタントメッセージを破棄し、要求の送信者にエラーメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="2fe80-178">**Block All**   The server drops all instant messages that contain file transfer requests and returns an error message to the sender of the request.</span></span> <span data-ttu-id="2fe80-179">Office Live Meeting 2007 クライアントの配布資料機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-179">The handout feature in the Office Live Meeting 2007 client is disabled.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="2fe80-180">ファイル拡張子のフィルター処理は、標準のファイル名に制限されています。</span><span class="sxs-lookup"><span data-stu-id="2fe80-180">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="2fe80-181">他の名前に埋め込まれているファイル拡張子では、フィルター処理が機能しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="2fe80-181">Filtering may not work with file extensions embedded in other names.</span></span>



</div>

</div>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2fe80-182">このセクション中</span><span class="sxs-lookup"><span data-stu-id="2fe80-182">In This Section</span></span>

  - [<span data-ttu-id="2fe80-183">Lync Server 2013 で既定のファイル転送フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="2fe80-183">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)

  - [<span data-ttu-id="2fe80-184">Lync Server 2013 で特定のサイト用の新しいファイル転送フィルターを作成する</span><span class="sxs-lookup"><span data-stu-id="2fe80-184">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)

  - [<span data-ttu-id="2fe80-185">Lync Server 2013 で既定の URL フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="2fe80-185">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)

  - [<span data-ttu-id="2fe80-186">Lync Server 2013 で新しい URL フィルターを作成して、IM 会話のハイパーリンクを処理する</span><span class="sxs-lookup"><span data-stu-id="2fe80-186">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2fe80-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="2fe80-187">See Also</span></span>


[<span data-ttu-id="2fe80-188">Lync Server 2013 での IM とプレゼンス設定の管理</span><span class="sxs-lookup"><span data-stu-id="2fe80-188">Managing IM and presence settings in Lync Server 2013</span></span>](lync-server-2013-managing-im-and-presence-settings.md)  
  

<span data-ttu-id="2fe80-189"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fe80-189"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

