---
title: 'Lync Server 2013: ベストプラクティスアナライザーによって作成されたレポートについて'
description: 'Lync Server 2013: ベストプラクティスアナライザーによって作成されたレポートについて。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding reports created by Best Practices Analyzer
ms:assetid: 1386dd6c-7f3e-4da9-905b-cef1468bf14a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591344(v=OCS.15)
ms:contentKeyID: 48183471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5fbb84cdffe6e6e6f079c2d72aba4799f5538776
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399482"
---
# <a name="understanding-reports-created-by-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="b9a78-103">Lync Server 2013 のベストプラクティスアナライザーによって作成されたレポートについて</span><span class="sxs-lookup"><span data-stu-id="b9a78-103">Understanding reports created by Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9a78-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9a78-104">

<span> </span></span></span>

<span data-ttu-id="b9a78-105">_**最終更新日:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="b9a78-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="b9a78-106">ベストプラクティスアナライザーには、問題の分析と解決を容易にするために、複数の種類のレポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b9a78-106">Best Practices Analyzer provides multiple types of reports that are organized to facilitate the analysis and resolution of issues.</span></span> <span data-ttu-id="b9a78-107">ベストプラクティスアナライザーは、エラー、警告、その他の情報などの問題を特定します。</span><span class="sxs-lookup"><span data-stu-id="b9a78-107">Best Practices Analyzer identifies issues such as errors, warnings, and other information.</span></span>

<div>

## <a name="reports"></a><span data-ttu-id="b9a78-108">レポート</span><span class="sxs-lookup"><span data-stu-id="b9a78-108">Reports</span></span>

<span data-ttu-id="b9a78-109">スキャンの結果にアクセスするには、次の各レポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="b9a78-109">You can access the results of a scan by viewing each of the following reports:</span></span>

  - <span data-ttu-id="b9a78-110">**リストレポート**   リストレポートは、特定の条件に基づいて整理されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-110">**List reports**   List reports are organized by specific criteria.</span></span> <span data-ttu-id="b9a78-111">クラス、重大度、または問題によって結果を並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-111">You can arrange the results by class, severity, or issue.</span></span> <span data-ttu-id="b9a78-112">たとえば、クラスによって結果をまとめる場合、ディレクターに関連する問題はレポートの [ディレクター] セクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-112">For example, if you organize results by class, issues related to Directors are included under the Directors section of the report.</span></span> <span data-ttu-id="b9a78-113">すべての問題を表示したり、情報項目のみを表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-113">You can view all of the issues, or just the informational items.</span></span> <span data-ttu-id="b9a78-114">リストレポートで、メモリなどの特定の項目を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-114">You can search a list report for specific items, such as memory.</span></span> <span data-ttu-id="b9a78-115">レポートを印刷したり、エクスポートしたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-115">You can also print the report or export it.</span></span>

  - <span data-ttu-id="b9a78-116">**ツリーレポート**   ツリーレポートは、スキャンの実行時に指定したスキャンなどのオプションを実行するために使用されるルールによって整理されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-116">**Tree reports**   Tree reports are organized by the rules that are used to run the scan and other options that you specified at the time the scan was run.</span></span> <span data-ttu-id="b9a78-117">たとえば、テストトポロジの規則に関連する問題は、レポートの [テストトポロジ] セクションに含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9a78-117">For example, issues related to the Test Topology rules are included under the Test Topology section of the report.</span></span> <span data-ttu-id="b9a78-118">すべての問題の詳細を表示したり、単に問題の概要を表示したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-118">You can view the details of all the issues, or just a summary of the issues.</span></span> <span data-ttu-id="b9a78-119">ツリーレポートで、メモリなどの特定の項目を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-119">You can search a tree report for specific items, such as memory.</span></span> <span data-ttu-id="b9a78-120">レポートを印刷したり、エクスポートしたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-120">You can also print the report or export it.</span></span>

  - <span data-ttu-id="b9a78-121">**その他のレポート**   他のレポートのアイテムには、スキャンに含まれているタスクの実行時ログが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-121">**Other reports**   Items in other reports include the run-time log of tasks that were included in the scan.</span></span> <span data-ttu-id="b9a78-122">他のレポートの項目で、メモリなどの特定の項目を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-122">You can search the items in other reports for specific items, such as memory.</span></span> <span data-ttu-id="b9a78-123">レポートを印刷したり、エクスポートしたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-123">You can also print the report or export it.</span></span>

</div>

<div>

## <a name="issues"></a><span data-ttu-id="b9a78-124">問題</span><span class="sxs-lookup"><span data-stu-id="b9a78-124">Issues</span></span>

<span data-ttu-id="b9a78-125">ベストプラクティスアナライザーによって生成されたレポートは、次の種類の問題を含む、環境のスキャン中に特定された特定の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="b9a78-125">The reports generated by Best Practices Analyzer indicate specific issues that are identified during the scan of your environment, including following types of issues:</span></span>

  - <span data-ttu-id="b9a78-126">**エラー**   環境を変更する必要がある重大な問題。</span><span class="sxs-lookup"><span data-stu-id="b9a78-126">**Errors**   Critical issues that require you to make a change in your environment.</span></span> <span data-ttu-id="b9a78-127">たとえば、Lync Server 2013 コアコンポーネントがインストールされていない場合、エラーがログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-127">For example, if Lync Server 2013 Core Components are not installed, an error is logged.</span></span>

    <span data-ttu-id="b9a78-128">エラーとして分類された問題は、レポート内で赤い X 記号によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-128">Issues that are classified as errors are identified in the report by a red X symbol.</span></span> <span data-ttu-id="b9a78-129">エラーは、[**リスト] レポート** ビューの [**すべての問題**] タブ、および [**詳細表示**] タブ、および **ツリーレポート** ビューの [**概要ビュー** ] タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-129">Errors are displayed on the **All Issues** tab of the **List Reports** view, and on the **Detailed View** tab and the **Summary View** tab of the **Tree Reports** view.</span></span> <span data-ttu-id="b9a78-130">レポートに特定のエラーが表示されないようにするには、1つのインスタンスまたはレポート内のそのエラーのすべてのインスタンスに対してエラーが表示されないように指定できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-130">If you do not want to see a specific error in a report, you can specify that the error not be shown for a single instance or for all instances of that error in the report.</span></span> <span data-ttu-id="b9a78-131">このエラーは、設定を変更し、エラーをレポートに表示することを指定しない限り、**他のレポート** ビューの [**非表示アイテム**] タブにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-131">The error is then displayed only on the **Hidden Items** tab of the **Other Reports** view, unless you change the setting and specify that the error be displayed in the report.</span></span>

  - <span data-ttu-id="b9a78-132">**警告**   ベストプラクティスの実装と一貫性がない問題。</span><span class="sxs-lookup"><span data-stu-id="b9a78-132">**Warnings**   Issues that are not consistent with the implementation of a best practice.</span></span> <span data-ttu-id="b9a78-133">これにより、お客様の環境での変更が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9a78-133">This may or may not indicate the need for a change in your environment.</span></span> <span data-ttu-id="b9a78-134">この問題は、変更する必要がない特定の設定に関する既知の問題である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9a78-134">The issue could be a known issue with a specific setting that you do not need to change.</span></span> <span data-ttu-id="b9a78-135">たとえば、サーバーで開始されていないサービスは、警告として記録されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-135">For example, services that are not started on a server are logged as warnings.</span></span>

    <span data-ttu-id="b9a78-136">警告として分類された問題は、レポート内で三角形の黄色の警告記号によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-136">Issues that are classified as warnings are identified in the report by a triangular yellow warning symbol.</span></span> <span data-ttu-id="b9a78-137">警告は、**リスト** の [レポート] ビューの [**すべての問題**] タブ、および [**詳細表示**] タブおよび **ツリーレポート** ビューの [**概要ビュー** ] タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-137">Warnings are displayed on the **All Issues** tab of the **List Reports** view, as well as on the **Detailed View** tab and the **Summary View** tab of the **Tree Reports** view.</span></span> <span data-ttu-id="b9a78-138">レポートに特定のエラーが表示されないようにするには、1つのインスタンスまたはレポート内のそのエラーのすべてのインスタンスに対してエラーが表示されないように指定できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-138">If you do not want to see a specific error in a report, you can specify that the error not be shown for a single instance or for all instances of that error in the report.</span></span> <span data-ttu-id="b9a78-139">この警告は、設定を変更し、レポートに警告を表示することを指定しない限り、**他のレポート** ビューの [**非表示アイテム**] タブにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-139">The warning is then displayed only on the **Hidden Items** tab of the **Other Reports** view, unless you change the setting and specify that the warning be displayed in the report.</span></span>

  - <span data-ttu-id="b9a78-140">**情報**   エラーまたは警告として分類されないすべての問題が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-140">**Information**   Includes all issues that are not classified as errors or warnings.</span></span> <span data-ttu-id="b9a78-141">たとえば、Active Directory ドメインサービス内の Lync Server 2013 Standard Edition server オブジェクトの数は、情報の問題として分類されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-141">For example, the number of Lync Server 2013 Standard Edition server objects in Active Directory Domain Services is classified as an information issue.</span></span>

    <span data-ttu-id="b9a78-142">情報の問題は、[**リスト] レポート** ビューの [**すべての問題**] タブと、**ツリーレポート** ビューの [**詳細表示**] タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-142">Information issues are displayed on the **All Issues** tab of the **List Reports** view, and on the **Detailed View** tab of the **Tree Reports** view.</span></span>

<span data-ttu-id="b9a78-143">Lync Server 2013 のベストプラクティスアナライザーは、問題を解決するために環境を変更することはありません。</span><span class="sxs-lookup"><span data-stu-id="b9a78-143">The Lync Server 2013, Best Practices Analyzer does not make changes to your environment to resolve issues.</span></span> <span data-ttu-id="b9a78-144">スキャンは、潜在的な問題を検出し、各問題を解決する方法に関する情報を含むレポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="b9a78-144">The scan only detects potential issues and provides reports that contain information about how to resolve each issue.</span></span>

<span data-ttu-id="b9a78-145">問題をクリックすると、特定の問題について説明と一部のオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-145">If you click an issue, an explanation and some options are displayed for specific issues.</span></span> <span data-ttu-id="b9a78-146">その後、次のいずれかの操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-146">Then, you can do any of the following:</span></span>

  - <span data-ttu-id="b9a78-147">この問題の詳細と解決方法については、こちらを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9a78-147">Find more detailed information about the issue, and how to resolve it.</span></span>

  - <span data-ttu-id="b9a78-148">レポートの問題を表示しないようにする:</span><span class="sxs-lookup"><span data-stu-id="b9a78-148">Stop showing issues in reports:</span></span>

      - <span data-ttu-id="b9a78-149">選択したインスタンスの問題を表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="b9a78-149">Stop showing issues for the selected instance.</span></span>

      - <span data-ttu-id="b9a78-150">その問題のすべてのインスタンスの問題を表示しなくなります。</span><span class="sxs-lookup"><span data-stu-id="b9a78-150">Stop showing issues for all instances of that issue.</span></span>

    <span data-ttu-id="b9a78-151">レポートで表示されていない問題を確認するには、[**その他のレポート**] ビューの [**非表示アイテム**] タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="b9a78-151">To see the issues you have stopped showing in reports, go to the **Hidden Items** tab of the **Other Reports** view.</span></span> <span data-ttu-id="b9a78-152">そこから、レポートの問題の表示を再び開始するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="b9a78-152">From there, you can specify to start showing issues in reports again.</span></span>

<span data-ttu-id="b9a78-153">特定の問題を解決する方法の詳細については、「 [Lync Server 2013 のベストプラクティスアナライザーによって識別](lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md)された問題を分析して解決する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9a78-153">For details about resolving specific issues, see [Analyzing and resolving issues identified by Best Practices Analyzer in Lync Server 2013](lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md).</span></span>

<span data-ttu-id="b9a78-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9a78-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
