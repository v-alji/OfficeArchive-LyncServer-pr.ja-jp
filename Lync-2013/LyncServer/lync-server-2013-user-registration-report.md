---
title: 'Lync Server 2013: ユーザー登録レポート'
description: 'Lync Server 2013: ユーザー登録レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Registration Report
ms:assetid: 151d5cc9-cc1b-4cfa-be9c-55ebe321f7a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558614(v=OCS.15)
ms:contentKeyID: 48183486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adb8ef7e94a24f0fd088f12e009fc9d63f3be9d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398666"
---
# <a name="user-registration-report-in-lync-server-2013"></a><span data-ttu-id="1bb25-103">Lync Server 2013 のユーザー登録レポート</span><span class="sxs-lookup"><span data-stu-id="1bb25-103">User Registration Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1bb25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1bb25-104">

<span> </span></span></span>

<span data-ttu-id="1bb25-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="1bb25-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="1bb25-106">ユーザー登録レポートには、指定した期間 (1 時間、毎日、毎週、毎月) に Microsoft Lync Server 2013 にログオンしたユーザーの数についての概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-106">The User Registration Report provides an overview of user logon activity, most notably information about the number of users who logged on to Microsoft Lync Server 2013 during a specified time period (hourly, daily, weekly, monthly).</span></span> <span data-ttu-id="1bb25-107">このレポートで示されるのは、ログオンしたユーザーの数のみです。</span><span class="sxs-lookup"><span data-stu-id="1bb25-107">Keep in mind that the report only tells you how many people logged on.</span></span> <span data-ttu-id="1bb25-108">*どの* ユーザーがログオンしたかは示されません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-108">It does not tell you *which* people logged on.</span></span> <span data-ttu-id="1bb25-109">レポートの監視では、どのユーザーが Lync Server 2013 を使用しているか (また、どのユーザーがいないか) についての情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-109">Monitoring Reports do not provide information about which specific users are using Lync Server 2013 (and which ones are not).</span></span> <span data-ttu-id="1bb25-110">ただし、ユーザー アクティビティ レポートを使用してユーザー情報の概算は把握できます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-110">However, you can get a rough estimate of user information by using the User Activity Report.</span></span>

<span data-ttu-id="1bb25-111">ユーザー登録レポートでは、ユーザー ログオンに関する情報を示す場合に 2 つの重要な分類が行われます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-111">When providing information about user logons, the User Registration Report draws two important distinctions.</span></span> <span data-ttu-id="1bb25-112">まず、内部ログオンと外部ログオンという 2 つの大きなカテゴリにログオンが分類されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-112">First, it breaks logons down into two primary categories: internal logons and external logons.</span></span> <span data-ttu-id="1bb25-113">内部ログオンは、組織のファイアウォール内から (企業ネットワークに接続中に) ログオンしたユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-113">Internal logons represent users who logged on from inside your organization's firewall (that is, while connected to the corporate network).</span></span> <span data-ttu-id="1bb25-114">[外部ログオン] は、ファイアウォールの外側からエッジサーバーを介してログオンしたユーザーを示します (たとえば、インターネットカフェからログオンしたユーザーは外部ログオンとしてカウントします)。</span><span class="sxs-lookup"><span data-stu-id="1bb25-114">External logons represent users who logged on from outside the firewall through an Edge Server (for example, a user who logged on from an Internet café counts as an external logon).</span></span> <span data-ttu-id="1bb25-115">ファイアウォールの外部からログオンしたユーザーの数が必要な場合、ユーザー登録レポートでその情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-115">If you need to know how many of your users are logging on from outside the firewall, the User Registration Report can provide you with this information.</span></span>

<span data-ttu-id="1bb25-116">また、ユーザー登録レポートは、指定した期間内に存在した *アクティブ* ユーザーの数も示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-116">In addition, the User Registration Report notes how many *active* users were present during a given time period.</span></span> <span data-ttu-id="1bb25-117">アクティブなユーザーとは、インスタントメッセージング (IM) セッションに参加しているか、Lync 会議に参加しているか、通話を発信または受信したか、その期間中に Lync Server を使用していたユーザーのことです。</span><span class="sxs-lookup"><span data-stu-id="1bb25-117">An active user is a user who took part in an instant messaging (IM) session, participated in a Lync Meeting, made or received a phone call, or otherwise used Lync Server during that period of time.</span></span> <span data-ttu-id="1bb25-118">ログオンしただけで実際にシステムを使用しなかったユーザーとは異なります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-118">This is different from a user who logged on, but never actually used the system.</span></span>

<div>

## <a name="accessing-the-user-registration-report"></a><span data-ttu-id="1bb25-119">ユーザー登録レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="1bb25-119">Accessing the User Registration Report</span></span>

<span data-ttu-id="1bb25-p104">ユーザー登録レポートには、監視レポートのホーム ページからアクセスできます。ユーザー登録レポートからは他のレポートへリンクしません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p104">You access the User Registration Report only from the Monitoring Reports home page. The User Registration Report does not link to any other reports.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-registration-report"></a><span data-ttu-id="1bb25-122">ユーザー登録レポートの効果的な活用方法</span><span class="sxs-lookup"><span data-stu-id="1bb25-122">Making the Best Use of the User Registration Report</span></span>

<span data-ttu-id="1bb25-123">Lync Server を展開した後、よく寄せられる質問として、ユーザーがこの新しいテクノロジを実際に使用しているかどうかを知る方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="1bb25-123">After you've deployed Lync Server one commonly-asked question is this: How do I know if my users are actually using this new technology?</span></span> <span data-ttu-id="1bb25-124">いくつか制限はありますが、ユーザー登録レポートがこの疑問の解決に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-124">Although it has a few limitations in this regard, the User Registration Report can help you answer this question.</span></span> <span data-ttu-id="1bb25-125">ユーザーが Lync Server を使用しているかどうかを判断するには、次の2つの操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-125">To determine whether or not users are using Lync Server, you need to do two things.</span></span> <span data-ttu-id="1bb25-126">まず、ユーザー登録レポートで [一意のログオン ユーザー数] 指標の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-126">First, get the value of the Unique logon users metric from the User Registration Report.</span></span> <span data-ttu-id="1bb25-127">この値は、Lync Server にログオンしている個別の個人の数を示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-127">This value tells you how many distinct individuals logged on to Lync Server.</span></span>

<span data-ttu-id="1bb25-128">比較すると、[ログオンの合計数] には、Lync Server にログオンした合計回数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-128">By comparison, the Total logons metric shows how many total times anyone logged on to Lync Server.</span></span> <span data-ttu-id="1bb25-129">たとえば、Ken Myer が Lync Server に1日に異なる5回ログオンしているとします。</span><span class="sxs-lookup"><span data-stu-id="1bb25-129">For example, suppose Ken Myer logged on to Lync Server five different times in a single day.</span></span> <span data-ttu-id="1bb25-130">この場合、Ken Myer は、[ログオン合計数] 指標ではログオン セッション回数 5 回として記録されますが、[一意のログオン ユーザー数] 指標ではログオン ユーザー 1 人として記録されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-130">In that case, Ken Myer would count as five separate logon sessions for the Total logons metric, but just one logon user for the Unique logon users metric.</span></span> <span data-ttu-id="1bb25-131">また、1 人のユーザーが複数のデバイスまたは複数の場所からログオンすることも珍しくありません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-131">Likewise, it's not uncommon for a user to log on from multiple devices or multiple locations.</span></span> <span data-ttu-id="1bb25-132">たとえば、ユーザーは自分のデスクトップコンピューター、自分のラップトップコンピューターを使ってログオンでき、Lync Server に自動的にログオンする IP 電話を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-132">For example, a user can log on using her desktop computer, her laptop computer, and she can have an IP phone that automatically logs on to Lync Server.</span></span> <span data-ttu-id="1bb25-133">この場合、一意のユーザー数は 1 人、ログオン回数は 3 回になります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-133">In this example, there is one unique user with three logons.</span></span>

<span data-ttu-id="1bb25-134">ログオン合計数と一意のログオン ユーザー数の相違についてさらにわかりやすく説明にするために、ある期間内のログオンが次の表のようになっていた場合を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-134">To further explain the difference between total logons and unique logons, consider the logons for a given time period in the following table.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bb25-135">ユーザー</span><span class="sxs-lookup"><span data-stu-id="1bb25-135">User</span></span></th>
<th><span data-ttu-id="1bb25-136">ログオン時刻</span><span class="sxs-lookup"><span data-stu-id="1bb25-136">Logon time</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-137">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="1bb25-137">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="1bb25-138">7/7/2012 8:45 AM</span><span class="sxs-lookup"><span data-stu-id="1bb25-138">7/7/2012 8:45 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-139">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="1bb25-139">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="1bb25-140">7/7/2012 8:46 AM</span><span class="sxs-lookup"><span data-stu-id="1bb25-140">7/7/2012 8:46 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-141">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="1bb25-141">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="1bb25-142">7/7/2012 9:17 AM</span><span class="sxs-lookup"><span data-stu-id="1bb25-142">7/7/2012 9:17 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-143">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="1bb25-143">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="1bb25-144">7/7/2012 9:22 AM</span><span class="sxs-lookup"><span data-stu-id="1bb25-144">7/7/2012 9:22 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-145">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="1bb25-145">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="1bb25-146">7/7/2012 9:31 AM</span><span class="sxs-lookup"><span data-stu-id="1bb25-146">7/7/2012 9:31 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bb25-p107">この場合、ログオン合計数は 5 回ですが、ログオンしたユーザーは Ken Myer (ログオン回数 3 回) と Pilar Ackerman (ログオン回数 2 回) の 2 人だけです。ログオン合計数と一意のログオン ユーザー数はこのように異なります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p107">Notice that there is a total of five logons; however, there are only two unique logon users: Ken Myer (who logged on three times) and Pilar Ackerman (who logged on twice). That's the difference between logons and unique logon users.</span></span>

<span data-ttu-id="1bb25-149">一意のログオンの数に加えて、Lync Server に対して有効になっているユーザーの合計数を把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-149">In addition to knowing the number of unique logons, you need to know the total number of users who have been enabled for Lync Server.</span></span> <span data-ttu-id="1bb25-150">この値を取得するには、Lync Server 2013 管理シェルを開き、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-150">That value can be retrieved by opening the Lync Server 2013 Management Shell and running the following Windows PowerShell command:</span></span>

    (Get-CsUser).Count

<span data-ttu-id="1bb25-151">上記のコマンドによって、1236の値が返され、固有のログオンユーザーのメトリックが返される場合は、667の平均値を返します。54これは、ユーザーが Lync を有効にしているわずかな半数のユーザーが、実際に毎日システムにログオンしていることを示します (つまり、667を1236で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="1bb25-151">If the preceding command returns a value of 1,236 and Unique logon users metric returns an average value of 667, that suggests that a little over half of your users enable for Lync are actually logging on to the system each day (that is, 667 divided by 1,236, which is approximately 54%).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="1bb25-152">ログオンの指標に記録されるのは、指定した期間内に実際にログオンしたユーザーの数である点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="1bb25-152">Keep in mind that the logon metrics record users who actually logged on during the specified time period.</span></span> <span data-ttu-id="1bb25-153">その前に既にシステムにログオンしていたユーザーは追跡されません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-153">They don't keep track of users who were already logged on to the system.</span></span> <span data-ttu-id="1bb25-154">たとえば、[一意のログオン ユーザー数] 指標が 667、ユーザー数が 1,236 の場合、約半分のユーザーがシステムにログオンしたことになります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-154">For example, if your Unique logon users metric shows 667 logons and you have 1,236 users, that suggests that about half your users are logging on to the system.</span></span> <span data-ttu-id="1bb25-155">ただし、ログオン データのチェックを開始する前に既に 300 人のユーザーがシステムにログオンしていたとします。</span><span class="sxs-lookup"><span data-stu-id="1bb25-155">However, suppose 300 users were already logged on to the system at the time you began checking the logon data.</span></span> <span data-ttu-id="1bb25-156">これは、実際には Lync Server にログオンしているユーザーが、1000実際にはログオンしているユーザーの80% に近いということを意味します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-156">That would mean that you actually had nearly 1,000 users logged on to Lync Server, which would mean that closer to 80% of your users were logged on.</span></span>



</div>

<span data-ttu-id="1bb25-157">また、[一意のログオン ユーザー数] の値と [一意のアクティブなユーザー数] 指標も比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-157">You should also compare the Unique logon users value with the value of the Unique active users metric.</span></span> <span data-ttu-id="1bb25-158">一意のアクティブユーザーのメトリックには、実際に Lync Server を使用した一意のユーザーの数が表示されます。通話を発信したか、Lync 会議に参加したか、または IM セッションに参加しているかがわかります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-158">The Unique active users metric tells you how many unique users actually used Lync Server: they made a phone call, they joined a Lync Meeting, or they participated in an IM session.</span></span> <span data-ttu-id="1bb25-159">Microsoft Lync 2013 は、ユーザーが Windows を起動するたびに自動的に開始するように構成できるため、この情報が役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-159">This is useful information, because Microsoft Lync 2013 can be configured to automatically start each time a user starts Windows.</span></span> <span data-ttu-id="1bb25-160">そのため、ユーザーが毎日 Windows にログオンしたときに Lync に自動的にログオンするユーザーが多数存在する可能性がありますが、その期間中に Lync Server を実際に使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="1bb25-160">Because of that, you might have a large number of users who automatically log on to Lync when they log on to Windows each day, but then never actually use Lync Server during that time period.</span></span>

<span data-ttu-id="1bb25-161">また、一意のアクティブユーザーのメトリックには、組織内で、ユーザーが通常はその日の終了時に Windows をログオフしない、意味のあるデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-161">The Unique active users metric also provides more meaningful data in an organization where users typically do not log off Windows at the end of the day.</span></span> <span data-ttu-id="1bb25-162">代わりに、コンピューターをロックし、Windows と Lync を実行したままにします。</span><span class="sxs-lookup"><span data-stu-id="1bb25-162">Instead, they simply lock their computers and leave Windows and Lync running.</span></span> <span data-ttu-id="1bb25-163">このような状態では、ユーザーは何日もログオンしたままでログオフしないので、1 日あたりのログオン数は非常に低くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1bb25-163">In a situation like that, you might end up with very few logons per day because your users logged on several days ago and never logged off.</span></span> <span data-ttu-id="1bb25-164">ただし、固有のアクティブユーザーは、ユーザーが Lync または別の Lync Server クライアントを使用しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-164">However, Unique active users tells you whether users are actively using Lync or another Lync Server client.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="1bb25-165">フィルター</span><span class="sxs-lookup"><span data-stu-id="1bb25-165">Filters</span></span>

<span data-ttu-id="1bb25-166">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-166">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="1bb25-167">たとえば、ユーザー登録レポートでは、すべてのレジストラープールおよびエッジサーバーのデータを表示したり、個々のプールのデータを表示したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-167">For example, the User Registration Report enables you to view data for all your Registrar pool and Edge Servers or to view data for an individual pool.</span></span> <span data-ttu-id="1bb25-168">また、データをグループ化する方法を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-168">You can also choose how data should be grouped.</span></span> <span data-ttu-id="1bb25-169">この場合は、登録が、時間、日、週、または月を基準にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="1bb25-169">In this case, registrations grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="1bb25-170">次の表に、ユーザー登録レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-170">The following table lists the filters that you can use with the User Registration Report.</span></span>

### <a name="user-registration-report-filters"></a><span data-ttu-id="1bb25-171">ユーザー登録レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="1bb25-171">User Registration Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bb25-172">名前</span><span class="sxs-lookup"><span data-stu-id="1bb25-172">Name</span></span></th>
<th><span data-ttu-id="1bb25-173">説明</span><span class="sxs-lookup"><span data-stu-id="1bb25-173">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-174"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-174"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-p113">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p113">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="1bb25-177">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1bb25-177">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1bb25-p114">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p114">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1bb25-180">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1bb25-180">7/7/2012</span></span></p>
<p><span data-ttu-id="1bb25-181">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="1bb25-181">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1bb25-182">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1bb25-182">7/3/2012</span></span></p>
<p><span data-ttu-id="1bb25-183">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="1bb25-183">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-184"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-184"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-p115">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p115">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="1bb25-187">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1bb25-187">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1bb25-p116">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p116">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1bb25-190">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1bb25-190">7/7/2012</span></span></p>
<p><span data-ttu-id="1bb25-191">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="1bb25-191">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1bb25-192">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1bb25-192">7/3/2012</span></span></p>
<p><span data-ttu-id="1bb25-193">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="1bb25-193">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-194"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-194"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-p117">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p117">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="1bb25-197">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="1bb25-197">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="1bb25-198">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="1bb25-198">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="1bb25-199">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="1bb25-199">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="1bb25-200">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="1bb25-200">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="1bb25-201">開始日と終了日が、選択されている期間内で許容される値の最大数を超えると、(開始日から起算した) 値の最大数のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-201">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="1bb25-202">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-202">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-203"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-203"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-204">レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="1bb25-204">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server.</span></span> <span data-ttu-id="1bb25-205">個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-205">You can either select an individual pool or choose <strong>[All]</strong> to view data for all the pools.</span></span> <span data-ttu-id="1bb25-206">このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-206">This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="1bb25-207">指標</span><span class="sxs-lookup"><span data-stu-id="1bb25-207">Metrics</span></span>

<span data-ttu-id="1bb25-208">次の表に、ユーザー登録レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-208">The following table lists the information provided in the User Registration Report.</span></span>

### <a name="user-registration-report-metrics"></a><span data-ttu-id="1bb25-209">ユーザー登録レポートの指標</span><span class="sxs-lookup"><span data-stu-id="1bb25-209">User Registration Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bb25-210">名前</span><span class="sxs-lookup"><span data-stu-id="1bb25-210">Name</span></span></th>
<th><span data-ttu-id="1bb25-211">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="1bb25-211">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="1bb25-212">説明</span><span class="sxs-lookup"><span data-stu-id="1bb25-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-213"><strong>[毎時]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-213"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="1bb25-214"><strong>[毎日]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-214"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="1bb25-215"><strong>[毎週]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-215"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="1bb25-216"><strong>[毎月]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-216"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-217">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-217">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-218">フィルター ツール バーで選択した期間を示します。</span><span class="sxs-lookup"><span data-stu-id="1bb25-218">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="1bb25-219">場合によっては、特定の期間をクリックして、その期間の詳細情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-219">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="1bb25-220">たとえば、毎日の間隔を使用していて、[7/7/2012] をクリックすると、その日付のユーザー登録アクティビティの時間の内訳が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-220">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-221"><strong>[ログオン合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-221"><strong>Total logons</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-222">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-222">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-223">成功したログオン セッションの総数です。</span><span class="sxs-lookup"><span data-stu-id="1bb25-223">Total number of successful logon sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-224"><strong>[内部ログオン数]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-224"><strong>Internal logons</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-225">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-225">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-226">内部ネットワーク内でのログオンの総数です。</span><span class="sxs-lookup"><span data-stu-id="1bb25-226">Total number of logons within the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-227"><strong>[外部ログオン数]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-227"><strong>External logons</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-228">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-228">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-229">エッジ サーバーを使用した、内部ネットワークの外部からのログオンの総数です。</span><span class="sxs-lookup"><span data-stu-id="1bb25-229">Total number of logons from outside the internal network, using the Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bb25-230"><strong>[一意のログオン ユーザー数]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-230"><strong>Unique logon users</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-231">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-231">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-p121">少なくとも 1 つのログオン セッションを使用したユーザーの総数です。複数のログオン セッションを使用したユーザーも、ログオン セッションを 1 つしか使用しなかったユーザーと同じように、1 ユーザーとしてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p121">Total number of users who had at least one logon session. A user who had multiple logon sessions counts as one user, the same as a person who had just a single logon session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bb25-234"><strong>[一意のアクティブなユーザー数]</strong></span><span class="sxs-lookup"><span data-stu-id="1bb25-234"><strong>Unique active users</strong></span></span></p></td>
<td><p><span data-ttu-id="1bb25-235">不可</span><span class="sxs-lookup"><span data-stu-id="1bb25-235">No</span></span></p></td>
<td><p><span data-ttu-id="1bb25-p122">ピアツーピア セッションまたは会議セッションに関係したユーザーの総数です。複数のセッションを使用したユーザーも、セッションを 1 つしか使用しなかったユーザーと同じように、1 ユーザーとしてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="1bb25-p122">Total number of users who were involved in a peer-to-peer or conferencing session. A user who had multiple sessions counts as one user, the same as a person who had just a single session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1bb25-238">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1bb25-238">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

