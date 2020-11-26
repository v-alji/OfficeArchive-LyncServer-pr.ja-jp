---
title: Skype for Business Online のレポートコマンドレットと REST web サービス
description: Skype for Business Online のレポートコマンドレットと REST web サービス。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423408"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a><span data-ttu-id="a2a89-103">Skype for Business Online のレポートコマンドレットと REST web サービス</span><span class="sxs-lookup"><span data-stu-id="a2a89-103">The Skype for Business Online reporting cmdlets and REST web service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2a89-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2a89-104">

<span> </span></span></span>

<span data-ttu-id="a2a89-105">_**最終更新日:** 2014-09-05_</span><span class="sxs-lookup"><span data-stu-id="a2a89-105">_**Topic Last Modified:** 2014-09-05_</span></span>

<span data-ttu-id="a2a89-106">Skype for Business Online は、レポート機能と併用することで、これらのレポートを生成するのに役立つ5つの Windows PowerShell コマンドレットへのアクセスを提供します。また、カスタマイズされたレポートデータを返すために管理者が使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-106">In conjunction with the reporting features, Skype for Business Online provides access to five Windows PowerShell cmdlets that help generate those reports and are also can be used by administrators to return customized reporting data.</span></span> <span data-ttu-id="a2a89-107">Skype for Business Online には、REST (対象指定) も含まれます。これは、開発者がカスタマイズしたレポート情報を取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-107">Skype for Business Online also includes the REST (Representational State Transfer), which can be used by developers to retrieve customized reporting information.</span></span>

<span data-ttu-id="a2a89-108">管理者が利用できるレポートコマンドレットには、次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="a2a89-108">The reporting cmdlets available to administrators include:</span></span>

  - <span data-ttu-id="a2a89-109">CsActiveUserReport を取得します。これは、アクティブなユーザー (つまり、Skype for Business Online にログインしていて、少なくとも1つの会議またはピアツーピア通信セッションに参加しているユーザー) の数に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-109">Get-CsActiveUserReport, which provides information about the number of active users (that is, users who have logged on to Skype for Business Online and participated in at least one conference or peer-to-peer communication session).</span></span>

  - <span data-ttu-id="a2a89-110">CsAVConferenceTimeReport は、音声/ビデオ会議で費やした時間 (分) に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-110">Get-CsAVConferenceTimeReport, which provides information about the amount of time (in minutes) users spent in audio/video conferences.</span></span>

  - <span data-ttu-id="a2a89-111">CsConferenceReport は、ユーザーが参加した会議の数と種類に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-111">Get-CsConferenceReport, which provides information about the number and type of conferences that users participated in.</span></span>

  - <span data-ttu-id="a2a89-112">CsP2PAVTimeReport は、オーディオやビデオが含まれているピアツーピアセッションでユーザーが費やした時間 (分) に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-112">Get-CsP2PAVTimeReport, which provides information about the amount of time (in minutes) users spent in peer-to-peer sessions that included audio and/or video.</span></span>

  - <span data-ttu-id="a2a89-113">Get-CsP2PSessionReport は、ユーザーが参加したピアツーピアセッションの数と種類に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-113">Get-CsP2PSessionReport, which provides information about the number and type of peer-to-peer sessions that users participated in.</span></span>

<span data-ttu-id="a2a89-114">ほとんどの管理者は、Microsoft 365 管理センターで利用可能なレポートを使用します。これらのレポートは自動生成されるだけでなく、レポートコマンドレットによって返される生の数値よりも簡単に解釈されるデータのグラフィカル表現を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-114">Most administrators will use the reports available in the Microsoft 365 admin center: not only are those reports auto-generated, but they also provide a graphical representation of the data that is often easier to interpret than the raw number values returned by the reporting cmdlets.</span></span> <span data-ttu-id="a2a89-115">ただし、Windows PowerShell を使用している管理者は、レポートコマンドレットを使用して、Lync Online レポートからすぐに利用できないデータを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-115">However, administrators familiar with Windows PowerShell can use the reporting cmdlets to return data that is not readily available from the Lync Online reports.</span></span> <span data-ttu-id="a2a89-116">たとえば、レポートコマンドレットはセッションの継続時間 (各セッションが継続した時間) に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-116">For example, the reporting cmdlets return information about session duration (the amount of time, in minutes, that each session lasted).</span></span> <span data-ttu-id="a2a89-117">Lync Online レポートを使用して、個別のセッション期間を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2a89-117">Individual session durations are not available using the Lync Online reports.</span></span> <span data-ttu-id="a2a89-118">同様に、[毎日] ビューでは、Lync Online レポートには、過去14日間の情報のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-118">Likewise, in daily view the Lync Online reports display information only for the preceding 14 days.</span></span> <span data-ttu-id="a2a89-119">1日の日数の合計 (たとえば、4か月前の日付) を確認するには、レポートコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-119">If you would like to review the daily totals for a different day (for example, a date from four months ago) you can do so by using the reporting cmdlets.</span></span>

<span data-ttu-id="a2a89-120">また、管理者は、「 [Excel を使用して office 365 レポートデータを取得する](https://msdn.microsoft.com/library/dn781442.aspx)」を参照してください。 Microsoft Excel の OData データ照会機能を使用して、カスタムの office 365 レポートを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-120">Administrators might also be interested in the article [Using Excel to Retrieve Office 365 Reporting Data](https://msdn.microsoft.com/library/dn781442.aspx), which explains how to use the OData data querying feature in Microsoft Excel to create custom office 365 report.</span></span> <span data-ttu-id="a2a89-121">カスタムレポートを使用すると、Office 365 レポートサービスから返されるデータ (およびデータ量) を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-121">Custom reports give you the ability to dictate which data (and how much data) is returned from the Office 365 reporting service.</span></span> <span data-ttu-id="a2a89-122">カスタムレポートを使用すると、データの並べ替えやグループ化の方法を指定したり、管理センターに表示されていない情報へのアクセスを提供したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-122">Custom reports also enable you to do such things as specify how the data should be sorted and grouped, and provide access to information that is not displayed in the admin center.</span></span>

<span data-ttu-id="a2a89-123">開発のバックグラウンドの管理者は、REST web サービスを使用して、Skype for Business Online 管理センターに表示されない情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-123">Administrators with a development background can use the REST web service to obtain information not displayed in the Skype for Business Online admin center.</span></span> <span data-ttu-id="a2a89-124">REST サービスは SOAP サービスと似ていますが、各テクノロジでクライアントとサーバーの間で XML データを転送する方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a2a89-124">The REST service is similar to the SOAP service, in that each technology provides a way to transfer XML data between a client and a server.</span></span> <span data-ttu-id="a2a89-125">ただし、REST サービスには SOAP サービスに関して少なくとも2つの利点があります。</span><span class="sxs-lookup"><span data-stu-id="a2a89-125">However, the REST service has at least two advantages over the SOAP service.</span></span> <span data-ttu-id="a2a89-126">1つ目は、ATOM シンジケーション形式と呼ばれる標準化された形式を使って XML データ転送を実行します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-126">For one, REST performs XML data transfers using a standardized format known as the ATOM syndication format.</span></span> <span data-ttu-id="a2a89-127">これに対して、データ転送時の SOAP では、標準以外の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2a89-127">By contrast, SOAP using a non-standard format when transferring data.</span></span> <span data-ttu-id="a2a89-128">また、REST は、GET と POST 以外の HTTP 動詞をブロックするネットワーク間でデータを転送することができます。</span><span class="sxs-lookup"><span data-stu-id="a2a89-128">In addition, REST is able to transfer data across networks that block HTTP verbs other than GET and POST.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="a2a89-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2a89-129">See Also</span></span>


<span data-ttu-id="a2a89-130">[Lync Online レポート](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="a2a89-130">[Lync Online reporting](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span></span>  


[<span data-ttu-id="a2a89-131">Office 365 レポート Web サービス</span><span class="sxs-lookup"><span data-stu-id="a2a89-131">The Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[<span data-ttu-id="a2a89-132">Office 365 レポート Web サービスについて学習する</span><span class="sxs-lookup"><span data-stu-id="a2a89-132">Learning About the Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984321.aspx)  
<span data-ttu-id="a2a89-133">[Exchange Online のレポートコマンドレット](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span><span class="sxs-lookup"><span data-stu-id="a2a89-133">[The Exchange Online Reporting Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span></span>  
[<span data-ttu-id="a2a89-134">Excel を使用して Office 365 レポートデータを取得する</span><span class="sxs-lookup"><span data-stu-id="a2a89-134">Using Excel to Retrieve Office 365 Reporting Data</span></span>](https://msdn.microsoft.com/library/dn781442.aspx)  
  

<span data-ttu-id="a2a89-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2a89-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

