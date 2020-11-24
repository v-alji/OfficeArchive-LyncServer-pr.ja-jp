---
title: 既存の展開環境からトポロジをダウンロードする
description: 既存の展開からトポロジをダウンロードします。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Download topology from existing deployment
ms:assetid: e39065a2-d4b0-4f27-8c49-f56be78fa55b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721913(v=OCS.15)
ms:contentKeyID: 49733847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c22d746f8faf3fdf14a44e751eeb3c88bf3eef4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398792"
---
# <a name="download-topology-from-existing-deployment"></a><span data-ttu-id="d5b1a-103">既存の展開環境からトポロジをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="d5b1a-103">Download topology from existing deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5b1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5b1a-104">

<span> </span></span></span>

<span data-ttu-id="d5b1a-105">_**最終更新日:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="d5b1a-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="d5b1a-106">Lync Server 2013 プールを作成する場合は、Lync Server 2010 に関連付けられている中央管理ストアを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-106">When creating a Lync Server 2013 pool, you will use the Central Management Store that is associated with Lync Server 2010.</span></span> <span data-ttu-id="d5b1a-107">最初の使用時と後続の編集セッションでトポロジビルダーを起動すると、トポロジビルダーで現在の構成ドキュメントを読み込む場所を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-107">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="d5b1a-108">既に Lync Server 2010 トポロジを定義しており、全体管理ストアを確立しているため、既存の展開からトポロジをダウンロードすることを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-108">Because you already have a Lync Server 2010 topology defined and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="d5b1a-109">トポロジビルダーはデータベースを読み取り、現在の定義を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-109">Topology Builder will read the database and retrieve the current definition.</span></span>

<span data-ttu-id="d5b1a-110">**既存の展開からトポロジをダウンロードするには**</span><span class="sxs-lookup"><span data-stu-id="d5b1a-110">**To download a topology from an existing deployment**</span></span>

1.  <span data-ttu-id="d5b1a-111">**Lync Server 展開ウィザード** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-111">Open the **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="d5b1a-112">[ **Lync Server 2013-展開ウィザード** ] ページで、[ **管理ツールのインストール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-112">From the **Lync Server 2013 – Deployment Wizard** page, click **Install Administrative Tools**.</span></span>

3.  <span data-ttu-id="d5b1a-113">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013** ]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-113">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013** , and then click **Lync Server Topology Builder**.</span></span>

4.  <span data-ttu-id="d5b1a-114">[ **既存の展開からトポロジをダウンロード**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-114">Select **Download Topology from existing deployment**.</span></span>
    
    <span data-ttu-id="d5b1a-115">![展開ウィザードのトポロジビルダーの設定](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "展開ウィザードのトポロジビルダーの設定")</span><span class="sxs-lookup"><span data-stu-id="d5b1a-115">![Deployment Wizard Topology Builder settings](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Deployment Wizard Topology Builder settings")</span></span>

5.  <span data-ttu-id="d5b1a-116">ファイル名を選択し、tbxml ファイルの種類が設定されたトポロジを保存します。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-116">Choose a file name and save the topology with the default .tbxml file type.</span></span>

6.  <span data-ttu-id="d5b1a-117">表示されている [Lync Server] ノードを展開して、展開内のさまざまなサーバーの役割を表示します。</span><span class="sxs-lookup"><span data-stu-id="d5b1a-117">Expand the Lync Server node, as shown, to reveal the various server roles in the deployment.</span></span>
    
    <span data-ttu-id="d5b1a-118">![トポロジビルダーサーバーの役割の全般プロパティ](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "トポロジビルダーサーバーの役割の全般プロパティ")</span><span class="sxs-lookup"><span data-stu-id="d5b1a-118">![Topology Builder server role general properties](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Topology Builder server role general properties")</span></span>

<span data-ttu-id="d5b1a-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5b1a-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

