---
title: 会議の構成設定の既存のコレクションを削除する
description: 会議の構成設定の既存のコレクションを削除します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430533"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="51689-103">Lync Server 2013 で既存の会議構成設定のコレクションを削除する</span><span class="sxs-lookup"><span data-stu-id="51689-103">Delete an existing collection of meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51689-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51689-104">

<span> </span></span></span>

<span data-ttu-id="51689-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="51689-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="51689-106">サイトまたはユーザーの構成を削除できます。</span><span class="sxs-lookup"><span data-stu-id="51689-106">You can delete a site or user configuration.</span></span> <span data-ttu-id="51689-107">グローバル構成を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="51689-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="51689-108">グローバル構成を削除すると、グローバル構成は自動的に既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="51689-108">If you delete the global configuration, it is automatically reset to the default values.</span></span>

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a><span data-ttu-id="51689-109">サイトまたはユーザーの会議の設定を削除するには</span><span class="sxs-lookup"><span data-stu-id="51689-109">To delete a site or user meeting configuration</span></span>

1.  <span data-ttu-id="51689-110">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="51689-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="51689-111">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="51689-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="51689-112">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="51689-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="51689-113">左側のナビゲーションバーで、[ **会議** ] をクリックし、[ **会議の設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51689-113">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="51689-114">会議構成の一覧で、削除するサイトまたはプールの構成をクリックし、[**編集**] をクリックして、[**削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51689-114">In the list of meeting configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="51689-115">Windows PowerShell コマンドレットを使用して会議の構成設定を削除する</span><span class="sxs-lookup"><span data-stu-id="51689-115">Removing Meeting Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="51689-116">会議の設定は、Windows PowerShell と Remove-CsMeetingConfiguration コマンドレットを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="51689-116">Meeting settings can be deleted by using Windows PowerShell and the Remove-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="51689-117">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="51689-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="51689-118">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="51689-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a><span data-ttu-id="51689-119">会議の構成設定の指定したコレクションを削除するには</span><span class="sxs-lookup"><span data-stu-id="51689-119">To remove a specified collection of meeting configuration settings</span></span>

  - <span data-ttu-id="51689-120">このコマンドを実行すると、Redmond サイトに適用された会議の構成設定が削除されます。</span><span class="sxs-lookup"><span data-stu-id="51689-120">This command removes the meeting configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="51689-121">サイトの範囲に適用されているすべての会議の設定を削除するには</span><span class="sxs-lookup"><span data-stu-id="51689-121">To remove all the meeting configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="51689-122">このコマンドを実行すると、サイトのスコープに適用されているすべての会議の構成設定が削除されます。</span><span class="sxs-lookup"><span data-stu-id="51689-122">This command removes all the meeting configuration settings applied to the site scope:</span></span>
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a><span data-ttu-id="51689-123">既定で匿名ユーザーを許可する会議の構成設定をすべて削除するには</span><span class="sxs-lookup"><span data-stu-id="51689-123">To remove all the meeting configuration settings that admit anonymous users by default</span></span>

  - <span data-ttu-id="51689-124">また、匿名ユーザーが既定で許可される設定をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="51689-124">And this one removes all the settings that allow anonymous users to be admitted by default:</span></span>
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

<span data-ttu-id="51689-125">詳細については、「 [Cs会議構成の削除](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) 」コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="51689-125">For more information, see the help topic for the [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="51689-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51689-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

