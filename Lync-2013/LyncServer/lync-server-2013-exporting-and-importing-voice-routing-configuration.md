---
title: 'Lync Server 2013: 音声ルーティング構成のエクスポートとインポート'
description: 'Lync Server 2013: ボイスルーティング構成のエクスポートとインポート'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting and importing voice routing configuration
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48185398
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a94a9c02672debae9f5b30e3a1a96856050d6ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428357"
---
# <a name="exporting-and-importing-voice-routing-configuration-in-lync-server-2013"></a><span data-ttu-id="68e43-103">Lync Server 2013 での音声ルーティング構成のエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="68e43-103">Exporting and importing voice routing configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68e43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68e43-104">

<span> </span></span></span>

<span data-ttu-id="68e43-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="68e43-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="68e43-106">音声ルーティング構成を公開せずに保存する場合は、次の手順に従って、Lync Server コントロールパネルの構成のエクスポートとインポートのコマンドを使用して、ボイスルーティング構成のスナップショットを保存して取得します。</span><span class="sxs-lookup"><span data-stu-id="68e43-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="68e43-107">ボイスルーティング構成ファイル (vcfg) をインポートする場合は、その間もサーバー上の音声ルーティング構成に変更が加えられたため、Lync Server コントロールパネルの [ **ボイスルーティング** ] グループのページには、音声ルーティングに対する変更がコミットされていないことが示されます。</span><span class="sxs-lookup"><span data-stu-id="68e43-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="68e43-108">こうした未確定の変更は、調整が必要な 2 つの構成間の相違です。</span><span class="sxs-lookup"><span data-stu-id="68e43-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="68e43-109">[ <STRONG>ボイスルーティング</STRONG> ] グループ内の任意のページの設定に対してコミットされていない変更を加えた場合、変更はエクスポートされた音声構成ファイル (vcfg) に保存されます。</span><span class="sxs-lookup"><span data-stu-id="68e43-109">If you have made any uncommitted changes to the settings on any page within the <STRONG>Voice Routing</STRONG> group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="68e43-110">これにより、複数の Lync Server コントロールパネルセッション中に、変更を公開する前に、ボイスルーティング構成の変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="68e43-110">This enables you to make voice routing configuration changes during multiple Lync Server Control Panel sessions before you publish the changes.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="68e43-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="68e43-111">In This Section</span></span>

  - [<span data-ttu-id="68e43-112">ボイスルート構成ファイルを Lync Server 2013 でエクスポートする</span><span class="sxs-lookup"><span data-stu-id="68e43-112">Export a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [<span data-ttu-id="68e43-113">Lync Server 2013 でのボイス ルート構成ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="68e43-113">Import a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-import-a-voice-route-configuration-file.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="68e43-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="68e43-114">Related Sections</span></span>

<span data-ttu-id="68e43-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68e43-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

