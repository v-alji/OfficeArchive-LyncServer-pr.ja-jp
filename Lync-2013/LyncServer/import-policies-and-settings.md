---
title: ポリシーと設定をインポートする
description: ポリシーと設定をインポートします。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439605"
---
# <a name="import-policies-and-settings"></a><span data-ttu-id="6df0e-103">ポリシーと設定をインポートする</span><span class="sxs-lookup"><span data-stu-id="6df0e-103">Import policies and settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6df0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6df0e-104">

<span> </span></span></span>

<span data-ttu-id="6df0e-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6df0e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6df0e-106">Office Communications Server 2007 R2 のトポロジ情報を Lync Server 2013 パイロットプールに統合したら、Lync Server 2013 Management Shell コマンドレットを実行して、Office Communications Server 2007 R2 ポリシーと構成設定を Lync Server 2013 パイロットプールに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df0e-106">After you merge your Office Communications Server 2007 R2 topology information with your Lync Server 2013 pilot pool, you need to run a Lync Server 2013 Management Shell cmdlet to migrate your Office Communications Server 2007 R2 policies and configuration settings to your Lync Server 2013 pilot pool.</span></span>

<span data-ttu-id="6df0e-107">**CsLegacyConfiguration** コマンドレットは、ポリシー、音声ルート、ダイヤルプラン、Communicator Web Access url、ダイヤルインアクセス番号を Lync Server 2013 にインポートします。</span><span class="sxs-lookup"><span data-stu-id="6df0e-107">The **Import-CsLegacyConfiguration** cmdlet imports policies, voice routes, dial plans, Communicator Web Access URLs, and dial-in access numbers to Lync Server 2013.</span></span>

<div>

## <a name="to-migrate-policies-and-settings"></a><span data-ttu-id="6df0e-108">ポリシーと設定を移行するには</span><span class="sxs-lookup"><span data-stu-id="6df0e-108">To migrate policies and settings</span></span>

1.  <span data-ttu-id="6df0e-109">Lync Server 2013 フロントエンドサーバーで、Lync Server 管理シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-109">On the Lync Server 2013 Front End server, start the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="6df0e-110">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-110">At the command line, type the following:</span></span>
    
        Import-CsLegacyConfiguration
    
    <span data-ttu-id="6df0e-111">ポリシーがインポートされたら、次の手順を実行して、Lync Server コントロールパネルにインポートされたポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-111">After the policies are imported, use the procedure that follows to see the imported policies in the Lync Server Control Panel .</span></span>

</div>

<div>

## <a name="to-view-imported-policies"></a><span data-ttu-id="6df0e-112">インポートしたポリシーを表示するには</span><span class="sxs-lookup"><span data-stu-id="6df0e-112">To view imported policies</span></span>

1.  <span data-ttu-id="6df0e-113">Lync Server 2013 コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6df0e-113">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="6df0e-114">[ **音声ルーティング** ] をクリックして、インポートしたポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-114">Click **Voice Routing** and view the imported policies.</span></span>

3.  <span data-ttu-id="6df0e-115">[ **会議** ] をクリックして、インポートしたポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-115">Click **Conferencing** and view the imported policies.</span></span>

4.  <span data-ttu-id="6df0e-116">[ **フェデレーションと外部アクセス** ] をクリックし、インポートされたポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-116">Click **Federation and External Access** and view the imported policies.</span></span>

5.  <span data-ttu-id="6df0e-117">[ **監視およびアーカイブ** ] をクリックして、インポートしたポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="6df0e-117">Click **Monitoring and Archiving** and view the imported policies.</span></span>

<span data-ttu-id="6df0e-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6df0e-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

