---
title: 'Lync Server 2013: Office Web Apps サーバーを使用するためのクライアントの構成'
description: 'Lync Server 2013: Office Web Apps サーバーで使用するクライアントを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring clients for use with Office Web Apps Server
ms:assetid: e5eaead7-0b32-42fb-97eb-ca203af59a9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205339(v=OCS.15)
ms:contentKeyID: 48185668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b9bd7cf1e76c481c40381234ba1a84cda5500dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399873"
---
# <a name="configuring-clients-of-lync-server-2013-for-use-with-office-web-apps-server"></a><span data-ttu-id="779c9-103">Lync Server 2013 のクライアントで Office Web Apps サーバーを使用するように構成する</span><span class="sxs-lookup"><span data-stu-id="779c9-103">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="779c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="779c9-104">

<span> </span></span></span>

<span data-ttu-id="779c9-105">_**最終更新日:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="779c9-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="779c9-106">ユーザーが Office Web App Server の全機能を使用できるようにする場合は、これらのユーザーを Microsoft Lync 2013 にアップグレードする必要があります。Lync 2013 のユーザーのみが、実際の PowerPoint プレゼンテーションに依存しない PowerPoint スライドをスクロールして、そのような作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="779c9-106">If you want users to experience the full capabilities of Office Web App Server then you should upgrade those users to Microsoft Lync 2013; only users of Lync 2013 will be able to do such things as scroll through PowerPoint slides independent of the actual PowerPoint presentation.</span></span> <span data-ttu-id="779c9-107">(つまり、これらのユーザーはプレゼンテーションの任意のスライドをいつでも見ることができ、実際のプレゼンテーションに影響を及ぼすことはありません)。Lync 2013 を使っていないユーザーは、引き続きオンライン会議に参加し、PowerPoint プレゼンテーションを表示することができます。ただし、それらのユーザーはスライドを個別にスクロールすることはできません。また、スライドの画面切り替えを表示したり、埋め込みビデオを表示したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="779c9-107">(That is, these users can look at any slide in the presentation at any time, without interfering in any way with the actual presentation.) Users who are not using Lync 2013 will still be able to join online conferences and view the PowerPoint presentation; however, they will not be able to independently scroll through the slides, nor will they be able to see slide transitions or view embedded videos.</span></span>

<span data-ttu-id="779c9-108">これらの機能は、Lync 2013 のユーザーがいつでも利用できることに注意してください。これは、PowerPoint の発表者が Microsoft Lync 2010 を実行している場合でも同様です。</span><span class="sxs-lookup"><span data-stu-id="779c9-108">Note that these capabilities will always be available to users of Lync 2013; this is true even if the PowerPoint presenter is running Microsoft Lync 2010.</span></span> <span data-ttu-id="779c9-109">PowerPoint プレゼンテーションが Lync 2010 を実行しているユーザーによってホストされている場合、lync Server 2013 では Office Web Apps サーバーを使用して、Lync 2013 ユーザーに Office Web Apps サーバーバージョンのプレゼンテーションが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="779c9-109">If a PowerPoint presentation is being hosted by a user running Lync 2010, Lync Server 2013 will coordinate with Office Web Apps Server to make sure that Lync 2013 users will view the Office Web Apps Server version of that presentation.</span></span> <span data-ttu-id="779c9-110">Office Web Apps サーバーは、Lync 2013 以外のクライアントを実行しているユーザー向けの PowerPoint サービスを提供していません。</span><span class="sxs-lookup"><span data-stu-id="779c9-110">Office Web Apps Server does not provide PowerPoint services for users running clients other than Lync 2013.</span></span> <span data-ttu-id="779c9-111">代わりに、これらのユーザーは会議サーバーサービスに接続し、Microsoft Lync Server 2010 と同じように PowerPoint プレゼンテーションを表示します。</span><span class="sxs-lookup"><span data-stu-id="779c9-111">Instead, those users connect to the Conferencing server service and view PowerPoint presentations the same way they did in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="779c9-112">また、これらのユーザーは、Lync Server 2010 によって提供される制限のある機能にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="779c9-112">This also means that these users will only have access to the more-limited capabilities offered by Lync Server 2010.</span></span>

<span data-ttu-id="779c9-113">Office Web Apps Server にはクライアントの構成は必要ありませんが (ユーザーを Lync 2013 にアップグレードすることはできません)、会議の出席者が Internet Explorer 9 にアップグレードすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="779c9-113">Although no client configuration is required for Office Web Apps Server (other than upgrading users to Lync 2013), it is recommended that conference attendees be upgrade to Internet Explorer 9.</span></span> <span data-ttu-id="779c9-114">電話会議には、Internet Explorer 8 を使ってアクセスできますが、その Web ブラウザーの使用にはいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="779c9-114">Although conferences can be accessed using Internet Explorer 8, there are some limitations to using that Web browser.</span></span> <span data-ttu-id="779c9-115">たとえば、Internet Explorer 8 のユーザーは、PowerPoint ステージのサイズをユーザー設定のサイズに変更することはできません。代わりに、3つの定義済みステージサイズのいずれかを使用するように制限されます。</span><span class="sxs-lookup"><span data-stu-id="779c9-115">For example, users of Internet Explorer 8 will not be able to resize the PowerPoint stage to a custom size; instead, they will be limited to using one of three predefined stage sizes.</span></span> <span data-ttu-id="779c9-116">同様に、Internet Explorer 8 ユーザーがメディアファイルを再生することはできません。</span><span class="sxs-lookup"><span data-stu-id="779c9-116">Likewise, Internet Explorer 8 users will not be able to play media files.</span></span>

<span data-ttu-id="779c9-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="779c9-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

