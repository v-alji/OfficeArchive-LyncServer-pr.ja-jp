---
title: 'Lync Server 2013: ファイルストアを復元する'
description: 'Lync Server 2013: ファイルストアを復元しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436252"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a><span data-ttu-id="5f98f-103">Lync Server 2013 でのファイルストアの復元</span><span class="sxs-lookup"><span data-stu-id="5f98f-103">Restoring a file store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f98f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f98f-104">

<span> </span></span></span>

<span data-ttu-id="5f98f-105">_**最終更新日:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="5f98f-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="5f98f-106">標準エディション用のファイルストアは、通常 Standard Edition サーバーにあります。</span><span class="sxs-lookup"><span data-stu-id="5f98f-106">File Stores for Standard Edition are typically located on the Standard Edition server.</span></span> <span data-ttu-id="5f98f-107">Enterprise Edition のファイルストアは、通常はファイルサーバーまたはクラスターにあります。</span><span class="sxs-lookup"><span data-stu-id="5f98f-107">File Stores for Enterprise Edition are typically located on a file server or cluster.</span></span> <span data-ttu-id="5f98f-108">次の手順では、ファイルストアを復元する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f98f-108">The following procedure describes how to restore a File Store.</span></span>

<div>

## <a name="to-restore-a-file-store"></a><span data-ttu-id="5f98f-109">ファイルストアを復元するには</span><span class="sxs-lookup"><span data-stu-id="5f98f-109">To restore a File Store</span></span>

1.  <span data-ttu-id="5f98f-110">ファイルストアに障害が発生した場合は、該当するファイルストアを $Backup から \\ ファイルサーバーまたは Standard Edition サーバー上のファイルストアの場所にコピーして、フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="5f98f-110">If a File Store fails, copy the appropriate File Store from $Backup\\ to the File Store location on the file server or Standard Edition server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5f98f-111">復元されたファイルストアのパスとファイル名は、バックアップされたファイルストアとまったく同じである必要があります。これにより、ファイルを使用するコンポーネントがアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="5f98f-111">The path and file name for the restored File Store should be exactly the same as the backed up File Store, so that components that use the files can access them.</span></span>

    
    </div>

2.  <span data-ttu-id="5f98f-112">必要に応じて、ファイルストアのアクセス制御リスト (Acl) を設定します。</span><span class="sxs-lookup"><span data-stu-id="5f98f-112">If necessary, set the access control lists (ACLs) for the File Store.</span></span> <span data-ttu-id="5f98f-113">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f98f-113">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5f98f-114">この手順を実行する必要があるのは、復元プロセスでトポロジビルダーを実行していない場合のみです。</span><span class="sxs-lookup"><span data-stu-id="5f98f-114">You need to perform this step only if you have not otherwise run Topology Builder during your restoration process.</span></span>

    
    <span data-ttu-id="5f98f-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f98f-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

