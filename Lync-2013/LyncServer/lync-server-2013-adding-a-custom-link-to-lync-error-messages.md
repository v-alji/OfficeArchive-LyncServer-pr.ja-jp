---
title: 'Lync Server 2013: Lync エラー メッセージへのユーザー設定リンクの追加'
description: 'Lync Server 2013: Lync のエラーメッセージへのカスタムリンクを追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding a custom link to Lync error messages
ms:assetid: de756088-fcc3-4e47-bde8-4fa4cc852fd1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398979(v=OCS.15)
ms:contentKeyID: 48185607
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5d333b6f27e10e5092de23fcdf1d37fd75e75a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439283"
---
# <a name="adding-a-custom-link-to-lync-error-messages-in-lync-server-2013"></a><span data-ttu-id="86c3d-103">Lync Server 2013 での Lync エラー メッセージへのユーザー設定リンクの追加</span><span class="sxs-lookup"><span data-stu-id="86c3d-103">Adding a custom link to Lync error messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86c3d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86c3d-104">

<span> </span></span></span>

<span data-ttu-id="86c3d-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="86c3d-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="86c3d-106">トラブルシューティングまたはヘルプデスクの情報へのリンクを追加して、Lync 2013 のエラーメッセージをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="86c3d-106">Customize Lync 2013 error messages by adding a link to your own troubleshooting or help desk information.</span></span> <span data-ttu-id="86c3d-107">これを行うには、CustomLinkInErrorMessages パラメーターを使用して、 **新しい csclientpolicy** または **Set-csclientpolicy** Lync Server Management Shell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="86c3d-107">To do this, use the **New-CSClientPolicy** or **Set-CSClientPolicy** Lync Server Management Shell cmdlets with the CustomLinkInErrorMessages parameter.</span></span> <span data-ttu-id="86c3d-108">カスタムリンクのテキストは、「管理者からのサポートトピックをここでクリックしてください」というテキストが表示され、カスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="86c3d-108">The text of the custom link is "Click here for support topics from your administrator," and it cannot be customized.</span></span>

<span data-ttu-id="86c3d-109">たとえば、次のコマンドを実行すると、すべての Lync 2013 エラーメッセージの [脚注] 領域にユーザー設定のリンクが表示され、リンク先が次のように設定されます。 http://contoso.com/help/LyncHelpDesk.aspx:</span><span class="sxs-lookup"><span data-stu-id="86c3d-109">For example, the following command causes the custom link to appear in the footnote area of every Lync 2013 error message and sets the link destination to http://contoso.com/help/LyncHelpDesk.aspx:</span></span>

    New-CsClientPolicy -Identity LyncErrorLink -CustomLinkInErrorMessages "http://contoso/help/LyncHelpDesk.aspx"

<span data-ttu-id="86c3d-110">ユーザーにこの新しいポリシーを割り当てるには **、グラント Clientpolicy** を使用します。</span><span class="sxs-lookup"><span data-stu-id="86c3d-110">Use **Grant-CSClientPolicy** to assign this new policy to users.</span></span> <span data-ttu-id="86c3d-111">詳細については、「 **新しい-CSClientPolicy** 」と「Lync Server 管理シェルドキュメントの **権限を付与** する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c3d-111">For details, see **New-CSClientPolicy** and **Grant-CSClientPolicy** in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="86c3d-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86c3d-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

