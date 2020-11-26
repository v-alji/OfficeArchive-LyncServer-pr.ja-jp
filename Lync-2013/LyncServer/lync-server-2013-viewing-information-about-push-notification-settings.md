---
title: 'Lync Server 2013: プッシュ通知設定に関する情報の表示'
description: 'Lync Server 2013: プッシュ通知設定に関する情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing information about push notification settings
ms:assetid: be5c6b01-4294-4d17-9772-fed40201e8a5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721868(v=OCS.15)
ms:contentKeyID: 49733801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44ee876df341833c93e97fd16664940629754a6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443980"
---
# <a name="viewing-information-about-push-notification-settings-in-lync-server-2013"></a><span data-ttu-id="db977-103">Lync Server 2013 でのプッシュ通知設定に関する情報の表示</span><span class="sxs-lookup"><span data-stu-id="db977-103">Viewing information about push notification settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db977-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db977-104">

<span> </span></span></span>

<span data-ttu-id="db977-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="db977-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="db977-106">プッシュ通知は、モバイルアプリケーションが非アクティブになっている場合でも、バッジ、アイコン、または通知の形式でモバイルデバイスに送信できます。</span><span class="sxs-lookup"><span data-stu-id="db977-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="db977-107">プッシュ通知は、新規または不在着信した IM の招待状やボイスメールなどのイベントをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="db977-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="db977-108">Lync Server 2013 コントロールパネルまたは Lync Server 2013 Management Shell を使用して、モバイルデバイスの情報プッシュ通知の設定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="db977-108">You can view information push notifications settings for mobile devices by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-view-push-notification-information-from-lync-server-control-panel"></a><span data-ttu-id="db977-109">Lync Server コントロールパネルからプッシュ通知情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="db977-109">To view push notification information from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="db977-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="db977-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="db977-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="db977-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="db977-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="db977-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="db977-113">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **プッシュ通知の構成** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="db977-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="db977-114">[ **プッシュ通知の構成** ] ページで、表示するサイトをクリックし、[ **編集** ] メニューをクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db977-114">On the **Push Notification Configuration** page, click the site you want to view, click the **Edit** menu, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-push-notification-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="db977-115">Windows PowerShell コマンドレットを使用したプッシュ通知情報の表示</span><span class="sxs-lookup"><span data-stu-id="db977-115">Viewing Push Notification Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="db977-116">プッシュ通知の構成設定を表示するには、Windows PowerShell と、" **Get-Cspの設定** " コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="db977-116">You can view push notification configuration settings by using Windows PowerShell and the **Get-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="db977-117">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="db977-117">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="db977-118">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="db977-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-push-notification-configuration-information"></a><span data-ttu-id="db977-119">プッシュ通知の構成情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="db977-119">To view push notification configuration information</span></span>

  - <span data-ttu-id="db977-120">すべてのプッシュ通知の構成設定に関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="db977-120">To view information about all your push notification configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsPushNotificationConfiguration
    
    <span data-ttu-id="db977-121">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="db977-121">That will return information similar to this:</span></span>
    
        Identity                               : Global
        EnableApplePushNotificationService     : False
        EnableMicrosoftPushNotificationService : False

</div>

<span data-ttu-id="db977-122">詳細については、「 [収集-Cspの設定](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) 」の「ヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db977-122">For more information, see the help topic for the [Get-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="db977-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="db977-123">See Also</span></span>


[<span data-ttu-id="db977-124">Lync Server 2013 でプッシュ通知を構成する</span><span class="sxs-lookup"><span data-stu-id="db977-124">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="db977-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db977-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

