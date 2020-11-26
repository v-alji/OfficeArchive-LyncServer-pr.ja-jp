---
title: 'Lync Server 2013: Lync Server ベストプラクティスアナライザー'
description: 'Lync Server 2013: Lync Server ベストプラクティスアナライザー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Best Practices Analyzer
ms:assetid: 3124be9d-ad21-4a70-9c21-d2fc1adb3386
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558584(v=OCS.15)
ms:contentKeyID: 48183768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22c162dc73ce92ada18ee98d6956b7ed3e5c07a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426285"
---
# <a name="lync-server-2013-best-practices-analyzer"></a><span data-ttu-id="c4406-103">Lync Server 2013 ベスト プラクティス アナライザー</span><span class="sxs-lookup"><span data-stu-id="c4406-103">Lync Server 2013 Best Practices Analyzer</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4406-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4406-104">

<span> </span></span></span>

<span data-ttu-id="c4406-105">_**最終更新日:** 2012-06-13_</span><span class="sxs-lookup"><span data-stu-id="c4406-105">_**Topic Last Modified:** 2012-06-13_</span></span>

<span data-ttu-id="c4406-106">Lync Server 2013 のベストプラクティスアナライザーは、Lync Server 2013 環境から構成情報を収集し、Microsoft のベストプラクティスに従って構成を設定するかどうかを決定する診断ツールです。</span><span class="sxs-lookup"><span data-stu-id="c4406-106">Lync Server 2013, Best Practices Analyzer is a diagnostic tool that gathers configuration information from Lync Server 2013 environments and determines whether the configuration is set according to Microsoft best practices.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c4406-107">Lync Server 2013 のベストプラクティスアナライザーは、Lync Server 2013 コンポーネントの問題のみをスキャンして報告します。</span><span class="sxs-lookup"><span data-stu-id="c4406-107">Lync Server 2013, Best Practices Analyzer scans and reports issues only with Lync Server 2013 components.</span></span> <span data-ttu-id="c4406-108">展開に Lync Server 2010 または Office Communications Server 2007 R2 コンポーネントが含まれている場合は、前のバージョンのベストプラクティスアナライザーを使用して、それらのコンポーネントを分析します。</span><span class="sxs-lookup"><span data-stu-id="c4406-108">If your deployment includes Lync Server 2010 or Office Communications Server 2007 R2 components, use the previous version of Best Practices Analyzer to analyze those components.</span></span> <span data-ttu-id="c4406-109">詳細については、「 <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Lync Server 2013 でベストプラクティスアナライザーを実行するための要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4406-109">For details, see <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Requirements for running Best Practices Analyzer in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c4406-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="c4406-110">In This Section</span></span>

  - [<span data-ttu-id="c4406-111">Lync Server 2013 のベストプラクティスアナライザーの概要</span><span class="sxs-lookup"><span data-stu-id="c4406-111">Overview of Best Practices Analyzer in Lync Server 2013</span></span>](lync-server-2013-overview-of-best-practices-analyzer.md)

  - [<span data-ttu-id="c4406-112">Lync Server 2013 でのベストプラクティスアナライザーの準備とインストール</span><span class="sxs-lookup"><span data-stu-id="c4406-112">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>](lync-server-2013-preparing-for-and-installing-best-practices-analyzer.md)

  - [<span data-ttu-id="c4406-113">ベストプラクティスアナライザーを使用して Lync Server 2013 の展開で発生する可能性のある問題を特定する</span><span class="sxs-lookup"><span data-stu-id="c4406-113">Using Best Practices Analyzer to identify potential issues in your Lync Server 2013 deployment</span></span>](lync-server-2013-using-best-practices-analyzer-to-identify-potential-issues-in-your-deployment.md)

  - <span data-ttu-id="c4406-114">[[スキャン結果] を使用して、Lync Server 2013 のベストプラクティスアナライザーによって報告された問題を分析し、解決する](lync-server-2013-using-scan-results-to-analyze-and-resolve-issues-reported-by-best-practices-analyzer.md)</span><span class="sxs-lookup"><span data-stu-id="c4406-114">[Using scan results to analyze and resolve issues reported by Best Practices Analyzer in Lync Server 2013](lync-server-2013-using-scan-results-to-analyze-and-resolve-issues-reported-by-best-practices-analyzer.md)</span></span>

<span data-ttu-id="c4406-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4406-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

