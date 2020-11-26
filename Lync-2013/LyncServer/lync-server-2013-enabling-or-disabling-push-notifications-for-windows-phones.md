---
title: 'Lync Server 2013: Windows Phone のプッシュ通知を有効または無効にする'
description: 'Lync Server 2013: Windows Phone のプッシュ通知を有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling push notifications for Windows Phones
ms:assetid: a34f0c5c-4228-40e3-9d93-bc0b5df4895d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688162(v=OCS.15)
ms:contentKeyID: 49733767
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba3748c56291b8c6eb236edaac7e23a9e00e5e98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428770"
---
# <a name="enabling-or-disabling-push-notifications-for-windows-phones-in-lync-server-2013"></a><span data-ttu-id="9411b-103">Lync Server 2013 での Windows Phone のプッシュ通知を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="9411b-103">Enabling or disabling push notifications for Windows Phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9411b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9411b-104">

<span> </span></span></span>

<span data-ttu-id="9411b-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="9411b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="9411b-106">プッシュ通知は、モバイルアプリケーションが非アクティブになっている場合でも、バッジ、アイコン、または警告の形式で Windows Phone に送信できます。</span><span class="sxs-lookup"><span data-stu-id="9411b-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a Windows Phone even when the mobile application is inactive.</span></span> <span data-ttu-id="9411b-107">プッシュ通知は、新規または不在着信した IM の招待状やボイスメールなどのイベントをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9411b-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="9411b-108">Windows Phone デバイスのプッシュ通知を有効または無効にするには、Lync Server 2013 コントロールパネルまたは Lync Server 2013 Management Shell を使用します。</span><span class="sxs-lookup"><span data-stu-id="9411b-108">You can enable or disable push notifications for Windows Phone devices by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-enable-push-notifications-for-windows-phone-by-using-lync-server-control-panel"></a><span data-ttu-id="9411b-109">Lync Server コントロールパネルを使用して Windows Phone のプッシュ通知を有効にするには</span><span class="sxs-lookup"><span data-stu-id="9411b-109">To enable push notifications for Windows Phone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9411b-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9411b-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9411b-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9411b-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9411b-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9411b-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9411b-113">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **プッシュ通知の構成** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="9411b-114">[ **プッシュ通知の構成** ] ページで、編集するサイトをクリックし、[ **編集** ] メニューをクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-114">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="9411b-115">[ **Microsoft プッシュ通知を有効にする** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9411b-115">Click the **Enable Microsoft push notifications** checkbox.</span></span>

6.  <span data-ttu-id="9411b-116">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-push-notifications-for-windows-phone-by-using-lync-server-control-panel"></a><span data-ttu-id="9411b-117">Lync Server コントロールパネルを使用して Windows Phone のプッシュ通知を無効にするには</span><span class="sxs-lookup"><span data-stu-id="9411b-117">To disable push notifications for Windows Phone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9411b-118">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9411b-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9411b-119">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9411b-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9411b-120">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9411b-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9411b-121">左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **プッシュ通知の構成** ] ナビゲーションボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-121">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="9411b-122">[ **プッシュ通知の構成** ] ページで、編集するサイトをクリックし、[ **編集** ] メニューをクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-122">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="9411b-123">[ **Microsoft プッシュ通知を有効にする** ] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="9411b-123">Clear the **Enable Microsoft push notifications** checkbox.</span></span>

6.  <span data-ttu-id="9411b-124">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9411b-124">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-push-notifications-for-windows-phone-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="9411b-125">Windows PowerShell コマンドレットを使用して、Windows Phone のプッシュ通知を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="9411b-125">Enabling or Disabling Push Notifications for Windows Phone by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="9411b-126">Windows Phone のプッシュ通知を有効または無効にするには、 **Set-csp・の設定** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9411b-126">You can enable or disable push notifications for Windows Phone by using the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="9411b-127">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="9411b-127">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="9411b-128">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="9411b-128">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-push-notifications-for-windows-phone"></a><span data-ttu-id="9411b-129">Windows Phone のプッシュ通知を有効にするには</span><span class="sxs-lookup"><span data-stu-id="9411b-129">To enable push notifications for Windows Phone</span></span>

  - <span data-ttu-id="9411b-130">Windows Phone のプッシュ通知を有効にするには、EnableMicrosoftPushNotificationService プロパティの値を True ($True) に設定します。</span><span class="sxs-lookup"><span data-stu-id="9411b-130">To enable push notifications for Windows Phone set the value of the EnableMicrosoftPushNotificationService property to True ($True).</span></span> <span data-ttu-id="9411b-131">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9411b-131">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableMicrosoftPushNotificationService $True

</div>

<div>

## <a name="to-disable-push-notifications-for-windows-phone"></a><span data-ttu-id="9411b-132">Windows Phone のプッシュ通知を無効にするには</span><span class="sxs-lookup"><span data-stu-id="9411b-132">To disable push notifications for Windows Phone</span></span>

  - <span data-ttu-id="9411b-133">Windows Phone のプッシュ通知を無効にするには、EnableMicrosoftPushNotificationService プロパティの値を False ($False) に設定します。</span><span class="sxs-lookup"><span data-stu-id="9411b-133">To disable push notifications for Windows Phone set the value of the EnableMicrosoftPushNotificationService property to False ($False).</span></span> <span data-ttu-id="9411b-134">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9411b-134">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableMicrosoftPushNotificationService $False

</div>

<span data-ttu-id="9411b-135">詳細については、「 [Set-cspの設定](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) 」の「ヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9411b-135">For more information, see the help topic for the [Set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9411b-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="9411b-136">See Also</span></span>


[<span data-ttu-id="9411b-137">Lync Server 2013 でプッシュ通知を構成する</span><span class="sxs-lookup"><span data-stu-id="9411b-137">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="9411b-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9411b-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

