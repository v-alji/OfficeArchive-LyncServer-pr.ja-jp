---
title: 'Lync Server 2013: 既定のファイル転送フィルターを変更する'
description: 'Lync Server 2013: 既定のファイル転送フィルターを変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default file transfer filter
ms:assetid: 791774a2-0bb6-4b5b-aeb0-ff69abb170f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521017(v=OCS.15)
ms:contentKeyID: 48184584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8091dfebea87b793c56b9a670cfeeeab15ce6c44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445723"
---
# <a name="modify-the-default-file-transfer-filter-in-lync-server-2013"></a><span data-ttu-id="ef9db-103">Lync Server 2013 で既定のファイル転送フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="ef9db-103">Modify the default file transfer filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef9db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef9db-104">

<span> </span></span></span>

<span data-ttu-id="ef9db-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ef9db-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ef9db-106">Lync Server 2013 では、Lync Server 2013 の展開における次のファイル関連のアクティビティ中に、特定の種類のファイルをブロックするグローバルファイル転送フィルターが提供されています。</span><span class="sxs-lookup"><span data-stu-id="ef9db-106">Lync Server 2013 provides a global file transfer filter that blocks specific types of files during the following file-related activities within your Lync Server 2013 deployment:</span></span>

  - <span data-ttu-id="ef9db-107">インスタントメッセージング (IM) 会話中のファイル送信要求</span><span class="sxs-lookup"><span data-stu-id="ef9db-107">File transfer requests during instant messaging (IM) conversations</span></span>

  - <span data-ttu-id="ef9db-108">Office Live Meeting 2007 クライアントで配布資料機能を使用しているときにファイルのアップロードとダウンロードを行う</span><span class="sxs-lookup"><span data-stu-id="ef9db-108">File uploads and downloads while using the handout feature in the Office Live Meeting 2007 client</span></span>

  - <span data-ttu-id="ef9db-109">会議中のマルチメディア再生</span><span class="sxs-lookup"><span data-stu-id="ef9db-109">Multimedia playback during conferences</span></span>

<span data-ttu-id="ef9db-110">ブロックまたは許可するファイルの種類に応じて、Lync Server コントロールパネルを使用してグローバルフィルターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ef9db-110">Depending on the types of files you want to block or allow, you can use Lync Server Control Panel to modify the global filter.</span></span> <span data-ttu-id="ef9db-111">ファイル転送フィルターの詳細については、「 [Lync Server 2013 でインスタントメッセージング (IM) のためのファイル送信と URL フィルタリングを構成する](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef9db-111">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-modify-the-default-file-transfer-filter"></a><span data-ttu-id="ef9db-112">既定のファイル転送フィルターを変更するには</span><span class="sxs-lookup"><span data-stu-id="ef9db-112">To modify the default file transfer filter</span></span>

1.  <span data-ttu-id="ef9db-113">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ef9db-114">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ef9db-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ef9db-115">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ef9db-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ef9db-116">左側のナビゲーションバーで、[ **IM とプレゼンス** ] をクリックし、[ **ファイルフィルター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-116">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="ef9db-117">[ **ファイルフィルター** ] ページで、 **グローバル** フィルターをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-117">On the **File Filter** page, double-click the **Global** filter.</span></span>

5.  <span data-ttu-id="ef9db-118">[ **ファイルフィルターの編集**] で、[ **ファイルフィルターを有効にする** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-118">In **Edit File Filter**, select the **Enable file filter** check box.</span></span>

6.  <span data-ttu-id="ef9db-119">[ **ファイル転送** ] ドロップダウンリストボックスで、[ **ブロック** する] または [ **特定の種類のファイルをブロック** する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-119">In the **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

7.  <span data-ttu-id="ef9db-120">[ **すべてブロック**] をクリックした場合は、手順9に進みます。</span><span class="sxs-lookup"><span data-stu-id="ef9db-120">If you clicked **Block All**, skip to step 9.</span></span>

8.  <span data-ttu-id="ef9db-121">[特定の **種類のファイルをブロック** する] をクリックした場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ef9db-121">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="ef9db-122">[ **選択** ] をクリックして、ブロックするファイルの種類の拡張子の既定のリストを変更します。</span><span class="sxs-lookup"><span data-stu-id="ef9db-122">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="ef9db-123">[ファイルの **種類の選択**] で、ブロックまたは削除するファイルの種類を [ファイルの **種類の拡張子**] の下にあるカテゴリから選びます。</span><span class="sxs-lookup"><span data-stu-id="ef9db-123">In **Select File Type**, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="ef9db-124">ブロックするファイルの種類の拡張子が表示されない場合は、[ **ファイルの種類の拡張子を追加する**] の下のテキストボックスに拡張子を入力し、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-124">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="ef9db-125">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-125">Click **OK**.</span></span>

9.  <span data-ttu-id="ef9db-126">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef9db-126">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ef9db-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef9db-127">See Also</span></span>


[<span data-ttu-id="ef9db-128">Lync Server 2013 でのインスタントメッセージング (IM) のファイル転送と URL フィルタリングの構成</span><span class="sxs-lookup"><span data-stu-id="ef9db-128">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="ef9db-129">Lync Server 2013 で特定のサイト用の新しいファイル転送フィルターを作成する</span><span class="sxs-lookup"><span data-stu-id="ef9db-129">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="ef9db-130">Lync Server 2013 で新しい URL フィルターを作成して、IM 会話のハイパーリンクを処理する</span><span class="sxs-lookup"><span data-stu-id="ef9db-130">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  


[<span data-ttu-id="ef9db-131">Lync Server 2013 で既定の URL フィルターを変更する</span><span class="sxs-lookup"><span data-stu-id="ef9db-131">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="ef9db-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef9db-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

