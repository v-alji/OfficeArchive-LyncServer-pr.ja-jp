---
title: 'Lync Server 2013: 位置情報データベースを発行する'
description: 'Lync Server 2013: 位置情報データベースを公開します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399056"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="19d50-103">Lync Server 2013 からロケーションデータベースを発行する</span><span class="sxs-lookup"><span data-stu-id="19d50-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19d50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19d50-104">

<span> </span></span></span>

<span data-ttu-id="19d50-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="19d50-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="19d50-106">場所データベースに追加した新しい場所は、公開されるまでクライアントで使用できません。</span><span class="sxs-lookup"><span data-stu-id="19d50-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="19d50-107">詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="19d50-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="19d50-108">**公開-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="19d50-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="19d50-109">緊急位置識別番号 (ELIN) ゲートウェイを使用する場合は、公衆交換電話網 (PSTN) の通信事業者の自動ロケーション識別 (ALI) データベースに ELIN をアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="19d50-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="19d50-110">ELIN レコードに特定の形式を使用するように PSTN の通信事業者が求める場合があります。</span><span class="sxs-lookup"><span data-stu-id="19d50-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="19d50-111">詳細については、PSTN の通信事業者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="19d50-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="19d50-112">場所情報サービスデータベースからレコードをエクスポートし、必要に応じて書式設定することができます。</span><span class="sxs-lookup"><span data-stu-id="19d50-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="19d50-113">場所データベースを公開するには</span><span class="sxs-lookup"><span data-stu-id="19d50-113">To publish the location database</span></span>

  - <span data-ttu-id="19d50-114">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="19d50-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="19d50-115">場所データベースを公開するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="19d50-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="19d50-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19d50-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

