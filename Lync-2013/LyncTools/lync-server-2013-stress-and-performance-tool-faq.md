---
title: Lync Server 2013 のストレスとパフォーマンスに関するツールについてよく寄せられる質問
description: Lync Server 2013 のストレスとパフォーマンスに関するツールについてよく寄せられる質問。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Stress and Performance Tool FAQ
ms:assetid: a5aff705-320c-4916-8094-23046b2a1b18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945600(v=OCS.15)
ms:contentKeyID: 51541426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 716325390bc33df209be3bdc67ed8b6cd7d1ec30
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446438"
---
# <a name="lync-server-2013-stress-and-performance-tool-faq"></a><span data-ttu-id="f3248-103">Lync Server 2013 のストレスとパフォーマンスに関するツールについてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f3248-103">Lync Server 2013 Stress and Performance Tool FAQ</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3248-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3248-104">

<span> </span></span></span>

<span data-ttu-id="f3248-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="f3248-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f3248-106">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f3248-106">Frequently Asked Questions</span></span>

<span data-ttu-id="f3248-107">ここでは、Lync Server 2013 のストレスとパフォーマンスツールについてよく寄せられる質問を示します。</span><span class="sxs-lookup"><span data-stu-id="f3248-107">Here are some frequently asked questions about the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="can-i-run-lyncperftoolexe-in-production"></a><span data-ttu-id="f3248-108">LyncPerfTool.exe を運用環境で実行できますか?</span><span class="sxs-lookup"><span data-stu-id="f3248-108">Can I run LyncPerfTool.exe in production?</span></span>

<span data-ttu-id="f3248-109">この方法はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f3248-109">We do not recommend this.</span></span> <span data-ttu-id="f3248-110">このツールは、サーバーのパフォーマンス、セキュリティ、ユーザーエクスペリエンスに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="f3248-110">This tool will impact server performance, security, and user experience.</span></span>

</div>

<div>

## <a name="i-am-logging-on-my-users-for-the-first-time-why-are-the-servers-running-at-such-high-load"></a><span data-ttu-id="f3248-111">ユーザーに初めてログオンしています。</span><span class="sxs-lookup"><span data-stu-id="f3248-111">I am logging on my users for the first time.</span></span> <span data-ttu-id="f3248-112">サーバーが高負荷で実行されているのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="f3248-112">Why are the servers running at such high load?</span></span>

<span data-ttu-id="f3248-113">ユーザーが初めてログオンしたときは、その他の操作が行われます。</span><span class="sxs-lookup"><span data-stu-id="f3248-113">The first time the users log on, there are additional operations that occur.</span></span> <span data-ttu-id="f3248-114">その結果、Microsoft SQL Server バックエンドサーバーのパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="f3248-114">As a result, the performance on the Microsoft SQL Server Back End Server will be degraded.</span></span> <span data-ttu-id="f3248-115">すべてのユーザーにログを記録する短いテストを実行してから、結果を測定する前にクライアントを再起動することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3248-115">We recommend that you run a short test that logs on all of the users, and then restart the clients before you measure results.</span></span> <span data-ttu-id="f3248-116">1秒あたり12回の同時ユーザーログオンセッションはサポートされませんが、これはハードウェア構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f3248-116">We do not support more than 12 concurrent user logon sessions per second, but this depends on your hardware configuration.</span></span>

</div>

<div>

## <a name="my-clients-are-running-out-of-memory-what-should-i-do"></a><span data-ttu-id="f3248-117">クライアントでメモリが不足しています。</span><span class="sxs-lookup"><span data-stu-id="f3248-117">My clients are running out of memory.</span></span> <span data-ttu-id="f3248-118">どうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="f3248-118">What should I do?</span></span>

<span data-ttu-id="f3248-119">クライアントのメモリが不足している場合は、コンピューターあたりのユーザー数を減らす必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3248-119">If your clients are running out of memory, you need to reduce the number of users per computer.</span></span>

</div>

<div>

## <a name="my-clients-are-at-100-percent-cpu-all-the-time-what-should-i-do"></a><span data-ttu-id="f3248-120">クライアントは、常に100% の CPU を搭載しています。</span><span class="sxs-lookup"><span data-stu-id="f3248-120">My clients are at 100 percent CPU all the time.</span></span> <span data-ttu-id="f3248-121">どうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="f3248-121">What should I do?</span></span>

<span data-ttu-id="f3248-122">すべてのユーザーがログオンした後でクライアントが非常に高い CPU で実行されている場合は、コンピューターあたりのユーザー数を減らす必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3248-122">If your clients are running with very high CPU after all the users have logged on, you need to reduce the number of users per computer.</span></span> <span data-ttu-id="f3248-123">CPU のスパイクの増加は許容されていますが、持続する場合は、読み込みを減らす必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3248-123">High CPU spikes are acceptable, but if it is sustained, you need to reduce the load.</span></span>

</div>

<div>

## <a name="can-i-run-the-tool-on-the-server-itself"></a><span data-ttu-id="f3248-124">サーバー自体でツールを実行できますか?</span><span class="sxs-lookup"><span data-stu-id="f3248-124">Can I run the tool on the server itself?</span></span>

<span data-ttu-id="f3248-125">いいえ。</span><span class="sxs-lookup"><span data-stu-id="f3248-125">No.</span></span> <span data-ttu-id="f3248-126">このシナリオはサポートされていないため、バイナリの不一致のために失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="f3248-126">This scenario is not supported and may fail due to a binary mismatch.</span></span> <span data-ttu-id="f3248-127">また、ポイントはサーバー上のリソース消費量を測定するため、ツールを実行すると、測定の意味がありません。</span><span class="sxs-lookup"><span data-stu-id="f3248-127">Also, because the point is to measure resource consumption on the server, running the tool there would render the measurements meaningless.</span></span>

</div>

<div>

## <a name="can-i-run-lyncperftoolexe-on-a-virtual-server-or-on-microsoft-hyper-v-server-20082012"></a><span data-ttu-id="f3248-128">仮想サーバーまたは Microsoft Hyper-v Server 2008/2012 で LyncPerfTool.exe を実行できますか?</span><span class="sxs-lookup"><span data-stu-id="f3248-128">Can I run LyncPerfTool.exe on a Virtual Server or on Microsoft Hyper-V Server 2008/2012?</span></span>

<span data-ttu-id="f3248-129">はい。</span><span class="sxs-lookup"><span data-stu-id="f3248-129">Yes.</span></span>

</div>

<div>

## <a name="what-does-mpop-mean"></a><span data-ttu-id="f3248-130">MPOP は何を意味していますか?</span><span class="sxs-lookup"><span data-stu-id="f3248-130">What does MPOP mean?</span></span>

<span data-ttu-id="f3248-131">MPOP は、複数のプレゼンスポイントを表します。</span><span class="sxs-lookup"><span data-stu-id="f3248-131">MPOP stands for multiple points of presence.</span></span> <span data-ttu-id="f3248-132">これは、ユーザーが複数のコンピューターから Lync 2013 にログオンしているシナリオをシミュレートすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="f3248-132">It is meant to simulate the scenario where users are logged on to Lync 2013 from multiple machines.</span></span> <span data-ttu-id="f3248-133">LyncPerfTool.exe では、各エンドポイントが既定のプロファイルを使用していることに注意してください (つまり、プロファイルが2つのプレゼンス間で分割されていません)。</span><span class="sxs-lookup"><span data-stu-id="f3248-133">Note that in LyncPerfTool.exe, each endpoint uses the default profile (that is, the profile is not split between the two points of presence).</span></span>

</div>

<div>

## <a name="i-started-lyncperftoolexe-but-nothing-is-happening-whats-going-on"></a><span data-ttu-id="f3248-134">LyncPerfTool.exe 開始しましたが、何も起こりません。</span><span class="sxs-lookup"><span data-stu-id="f3248-134">I started LyncPerfTool.exe but nothing is happening.</span></span> <span data-ttu-id="f3248-135">どうなっているのですか。</span><span class="sxs-lookup"><span data-stu-id="f3248-135">What’s going on?</span></span>

<span data-ttu-id="f3248-136">クライアントの [アクティブなエンドポイントの合計数カウンターを確認して、ユーザーが接続しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3248-136">Check the Total Active Endpoints counter on the clients to see if the users are connecting.</span></span> <span data-ttu-id="f3248-137">ユーザーが接続していない場合は、Lync Server 2013 の構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="f3248-137">If users are not connecting, verify your Lync Server 2013 configuration.</span></span> <span data-ttu-id="f3248-138">この問題は、サーバー名、ユーザーのプレフィックス、またはパスワードが正しくないことが原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="f3248-138">This issue usually occurs because the server name, the user prefix, or the password is incorrect.</span></span> <span data-ttu-id="f3248-139">外部クライアントでは、TargetServer 値としてアクセスプロキシを指定する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f3248-139">Note that external clients should specify the Access Proxy as the TargetServer value.</span></span> <span data-ttu-id="f3248-140">構成ファイルでポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3248-140">Verify the port in the configuration file.</span></span>

</div>

<div>

## <a name="how-do-i-know-something-is-happening"></a><span data-ttu-id="f3248-141">何が起こっているかを知る方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="f3248-141">How do I know something is happening?</span></span>

<span data-ttu-id="f3248-142">さまざまな LyncPerfTool パフォーマンスカウンターは、ユーザーが接続して操作を実行しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f3248-142">The various LyncPerfTool performance counters indicate whether or not users are connecting and performing actions.</span></span> <span data-ttu-id="f3248-143">ただし、Lync 2013 を使用して、必要な操作を実行して、アカウントの1つにログオンすることを簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="f3248-143">However, an easy way to check is to log on to one of the accounts by using Lync 2013 and performing the action you want.</span></span>

</div>

<div>

## <a name="i-have-live-communications-server-2007-r2-capacity-planning-tools-andor-lync-server-2010-installed-is-that-ok"></a><span data-ttu-id="f3248-144">Live Communications Server 2007 R2 キャパシティプランニングツールまたは Lync Server 2010 がインストールされています。</span><span class="sxs-lookup"><span data-stu-id="f3248-144">I have Live Communications Server 2007 R2 Capacity Planning Tools and/or Lync Server 2010 installed.</span></span> <span data-ttu-id="f3248-145">よろしいですか?</span><span class="sxs-lookup"><span data-stu-id="f3248-145">Is that OK?</span></span>

<span data-ttu-id="f3248-146">いいえ。</span><span class="sxs-lookup"><span data-stu-id="f3248-146">No.</span></span> <span data-ttu-id="f3248-147">相互運用性の問題があるため、この製品の以前のバージョンをすべてアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3248-147">There are interoperability issues, and you must uninstall all previous versions of this product.</span></span>

</div>

<div>

## <a name="will-the-stress-and-performance-tools-set-up-the-caa-call-information-server-topology"></a><span data-ttu-id="f3248-148">ストレスとパフォーマンスのツールで CAA を Call Information server topology をセットアップしますか?</span><span class="sxs-lookup"><span data-stu-id="f3248-148">Will the Stress and Performance tools set up the CAA Call Information server topology?</span></span>

<span data-ttu-id="f3248-149">いいえ。</span><span class="sxs-lookup"><span data-stu-id="f3248-149">No.</span></span> <span data-ttu-id="f3248-150">このツールでは、ユーザー、連絡先、配布リストが作成され、ユーザーロードがシミュレートされます。</span><span class="sxs-lookup"><span data-stu-id="f3248-150">The tools only create users, contacts, and distribution lists, and simulate user load.</span></span>

</div>

<div>

## <a name="what-is-the-maximum-number-of-users-that-the-tools-support"></a><span data-ttu-id="f3248-151">ツールでサポートされるユーザーの最大数は何人ですか?</span><span class="sxs-lookup"><span data-stu-id="f3248-151">What is the maximum number of users that the tools support?</span></span>

<span data-ttu-id="f3248-152">これらのツールを使用して、最大で8万ユーザーを作成し、合計3万ユーザーを実行しました。</span><span class="sxs-lookup"><span data-stu-id="f3248-152">We have created up to a total of 80,000 users and executed tests totaling 30,000 users, using these tools.</span></span> <span data-ttu-id="f3248-153">使用できるクライアントとサーバーのハードウェアによっては、最大で12万のユーザーを対象としていますが、技術的な制限により、高い価値を実現することができます。</span><span class="sxs-lookup"><span data-stu-id="f3248-153">We suggest a maximum of 120,000 users, although the technical limitations allow for a higher value, depending on the client and server hardware available.</span></span>

<span data-ttu-id="f3248-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3248-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

