---
title: パイロット プール展開の DNS レコードの構成
description: パイロットプール展開用の DNS レコードを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398871"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="4ef81-103">パイロット プール展開の DNS レコードの構成</span><span class="sxs-lookup"><span data-stu-id="4ef81-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ef81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ef81-104">

<span> </span></span></span>

<span data-ttu-id="4ef81-105">_**最終更新日:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="4ef81-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="4ef81-106">Lync Server 2013 パイロットプールを展開する前に、パイロットプールの DNS ホストのエントリを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ef81-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="4ef81-107">この手順を完了するには、サーバーまたはドメインに、Domain Admins グループのメンバーまたは DnsAdmins グループのメンバーとしてログオンしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ef81-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="4ef81-108">**DNS ホスト A レコードを構成するには**</span><span class="sxs-lookup"><span data-stu-id="4ef81-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="4ef81-109">ドメインネームシステム (DNS) サーバーで、[ **スタート**] をクリックし、[ **管理ツール**]、[ **DNS**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef81-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="4ef81-110">ドメインのコンソールツリーで [ **前方参照ゾーン**] を展開し、Lync Server 2013 がインストールされているドメインを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef81-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="4ef81-111">[ **新しいホスト (A または AAAA)**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef81-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="4ef81-112">[ **名前**] をクリックして、Lync Server 2013 プールのホスト名を入力します (ドメイン名は、レコードが定義されていて、A レコードの一部として入力する必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="4ef81-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="4ef81-113">[ **Ip アドレス**] をクリックして、フロントエンドプールの ip アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef81-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="4ef81-114">[ **ホストの追加**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef81-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="4ef81-115">完了したら、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef81-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="4ef81-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ef81-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

