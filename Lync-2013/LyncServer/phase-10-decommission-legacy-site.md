---
title: 'フェーズ 10: レガシサイトの廃止'
description: 'フェーズ 10: レガシサイトを廃止します。'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 10: Decommission legacy site'
ms:assetid: d591a310-3b5c-4092-b19e-0349616e40df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205300(v=OCS.15)
ms:contentKeyID: 48185540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9692301a1da38cfd69780ce2524f00dd428454e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443273"
---
# <a name="phase-10-decommission-legacy-site"></a><span data-ttu-id="a48d2-103">フェーズ 10: レガシサイトの廃止</span><span class="sxs-lookup"><span data-stu-id="a48d2-103">Phase 10: Decommission legacy site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a48d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a48d2-104">

<span> </span></span></span>

<span data-ttu-id="a48d2-105">_**最終更新日:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="a48d2-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="a48d2-106">次のトピックでは、Office Communications Server 2007 R2 のレガシ展開でのプールの廃止、サーバーとプールの無効化と削除に関するガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a48d2-106">The following topics provide guidance in decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Office Communications Server 2007 R2.</span></span> <span data-ttu-id="a48d2-107">このセクションに記載されているすべての手順を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a48d2-107">Not all of the procedures listed in this section are required.</span></span> <span data-ttu-id="a48d2-108">以下の各トピックの情報を読み、使用する使用停止手順を確認してください。</span><span class="sxs-lookup"><span data-stu-id="a48d2-108">Read the information in each of these topics to determine which decommissioning procedure to use.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="a48d2-109">ダイヤルイン会議用の会議ディレクトリを Lync Server 2013 にインポートした場合は、プールの廃止を開始する前に、会議ディレクトリの所有権を Lync Server 2013 に移行することが重要です。</span><span class="sxs-lookup"><span data-stu-id="a48d2-109">If you imported conference directories for dial-in conferencing to Lync Server 2013, it is important to transition conference directory ownership to Lync Server 2013 before you begin to decommission your pools.</span></span> <span data-ttu-id="a48d2-110">最初に会議ディレクトリの所有権を移行することなくプールを廃止すると、移行したすべての会議のダイヤルイン機能が機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="a48d2-110">If you decommission a pool without first transitioning conference directory ownership, the dial-in feature for all migrated meetings will no longer work.</span></span> <span data-ttu-id="a48d2-111">従来のプールの各会議ディレクトリについて、所有権を1回移行する手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a48d2-111">You must perform the step to transition ownership once for each conference directory in your legacy pool.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a48d2-112">Microsoft ユニファイドコミュニケーションマネージ API (UCMA) アプリケーションの移行とアップグレードに関する情報については、「従来の環境を廃止する前に」を参照してください。 <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span><span class="sxs-lookup"><span data-stu-id="a48d2-112">For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a48d2-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="a48d2-113">In This Section</span></span>

  - [<span data-ttu-id="a48d2-114">会議ディレクトリを移動する</span><span class="sxs-lookup"><span data-stu-id="a48d2-114">Move conference directories</span></span>](move-conference-directories.md)

  - [<span data-ttu-id="a48d2-115">DNS SRV レコードの更新</span><span class="sxs-lookup"><span data-stu-id="a48d2-115">Update DNS SRV records</span></span>](update-dns-srv-records.md)

  - [<span data-ttu-id="a48d2-116">サーバーとプールの無効化</span><span class="sxs-lookup"><span data-stu-id="a48d2-116">Decommissioning servers and pools</span></span>](decommissioning-servers-and-pools.md)

  - [<span data-ttu-id="a48d2-117">BackCompatSite を削除する</span><span class="sxs-lookup"><span data-stu-id="a48d2-117">Remove BackCompatSite</span></span>](remove-backcompatsite.md)

<span data-ttu-id="a48d2-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a48d2-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

