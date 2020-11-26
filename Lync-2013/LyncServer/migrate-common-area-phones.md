---
title: 共通領域電話の移行
description: 一般的なエリア電話を移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443826"
---
# <a name="migrate-common-area-phones"></a><span data-ttu-id="f4cd7-103">共通領域電話の移行</span><span class="sxs-lookup"><span data-stu-id="f4cd7-103">Migrate Common Area Phones</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4cd7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4cd7-104">

<span> </span></span></span>

<span data-ttu-id="f4cd7-105">_**最終更新日:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="f4cd7-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="f4cd7-106">一般的なエリア携帯電話は、共通のワークスペースや一般的な領域 (ロビー、台所、工場など) に存在する IP 電話です。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-106">Common Area Phones are IP phones that most often reside in a shared workspace or common area, like a lobby, kitchen, or factory floor.</span></span> <span data-ttu-id="f4cd7-107">Lync Server UC 機能を提供するには、一般的なエリア携帯電話がコンピューターに接続されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-107">Common Area Phones do not need to be connected to a computer to provide Lync Server UC functionality.</span></span> <span data-ttu-id="f4cd7-108">Lync Server 2010 の展開を Lync Server 2013 に移行した後、従来の一般的な市外局番に関連付けられた連絡先オブジェクトも移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-108">After migrating an Lync Server 2010 deployment to Lync Server 2013, you must also migrate the contact objects associated with the legacy Common Area Phone.</span></span> <span data-ttu-id="f4cd7-109">Lync Server 管理シェルを使用して、まず Lync Server 2010 共通エリア電話に関連付けられているすべての連絡先オブジェクトを取得してから、それらのオブジェクトを Lync Server 2013 プールに移動します。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-109">Using Lync Server Management Shell you will first retrieve all contact objects associated with the Lync Server 2010 Common Area Phones, and then move those objects to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f4cd7-110">**共通領域電話の移行**</span><span class="sxs-lookup"><span data-stu-id="f4cd7-110">**Migrate Common Area Phones**</span></span>

1.  <span data-ttu-id="f4cd7-111">Lync Server 2013 フロントエンドサーバーから、Lync Server 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-111">From the Lync Server 2013 Front End server, open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="f4cd7-112">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-112">From the command line, type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  <span data-ttu-id="f4cd7-113">すべての連絡先オブジェクトが Lync Server 2013 プールに移動されたことを確認するには、Lync Server 管理シェルで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-113">To verify all contact objects have been moved to the Lync Server 2013 pool, from the Lync Server Management Shell type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    <span data-ttu-id="f4cd7-114">すべての連絡先オブジェクトが Lync Server 2013 プールと関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4cd7-114">Verify all contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f4cd7-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4cd7-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

