---
title: 'Lync Server 2013: 外部ユーザー アクセスに関するグローバル ポリシーのリセット'
description: 'Lync Server 2013: 外部ユーザーアクセスのグローバルポリシーをリセットします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset the global policy for external user access
ms:assetid: 8207e1b1-de9e-461f-975f-fcc5c526849a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182545(v=OCS.15)
ms:contentKeyID: 48184675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 061f86fd454cea851a8e8cfbd4f40921daeecd98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436364"
---
# <a name="reset-the-global-policy-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="99a98-103">Lync Server 2013 での外部ユーザー アクセスに関するグローバル ポリシーのリセット</span><span class="sxs-lookup"><span data-stu-id="99a98-103">Reset the global policy for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99a98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99a98-104">

<span> </span></span></span>

<span data-ttu-id="99a98-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="99a98-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="99a98-106">グローバルポリシーを完全に削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="99a98-106">You cannot completely delete a global policy.</span></span> <span data-ttu-id="99a98-107">グローバルポリシーの [ **削除** ] オプションを使うと、グローバルポリシーは既定の設定にリセットされます。これには、外部ユーザーアクセスオプションのサポートは含まれません。</span><span class="sxs-lookup"><span data-stu-id="99a98-107">Using the **Delete** option on the global policy only resets the global policy to the default settings, which do not include support for any external user access options.</span></span>

<div>

## <a name="to-reset-the-global-policy-to-the-default-settings"></a><span data-ttu-id="99a98-108">グローバルポリシーを既定の設定にリセットするには</span><span class="sxs-lookup"><span data-stu-id="99a98-108">To reset the global policy to the default settings</span></span>

1.  <span data-ttu-id="99a98-109">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="99a98-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="99a98-110">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="99a98-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="99a98-111">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="99a98-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="99a98-112">左側のナビゲーションバーで、[ **外部ユーザーアクセス**]、[ **外部アクセスポリシー**] の順番にクリックします。</span><span class="sxs-lookup"><span data-stu-id="99a98-112">In the left navigation bar, click **External User Access**, click **External Access Policy**.</span></span>

4.  <span data-ttu-id="99a98-113">[ **外部アクセスポリシー** ] タブで、グローバルポリシーをクリックし、[ **編集**] をクリックして、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99a98-113">On the **External Access Policy** tab, click the global policy, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="99a98-114">削除を確認するメッセージが表示されたら、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99a98-114">When prompted to confirm the deletion, click **OK**.</span></span> <span data-ttu-id="99a98-115">ページの上部に、グローバルポリシーがリセットされたことを通知するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="99a98-115">A message appears at the top of the page informing you that the global policy has been reset.</span></span>

</div>

<div>

## <a name="resetting-the-global-external-access-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="99a98-116">Windows PowerShell コマンドレットを使用してグローバル外部アクセスポリシーをリセットする</span><span class="sxs-lookup"><span data-stu-id="99a98-116">Resetting the Global External Access Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="99a98-117">グローバル外部アクセスポリシーをリセットするには、Windows PowerShell と Remove-CsExternalAccessPolicy コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="99a98-117">The global external access policy can be reset by using Windows PowerShell and the Remove-CsExternalAccessPolicy cmdlet.</span></span> <span data-ttu-id="99a98-118">このコマンドレットは、Lync Server 2013 Management Shell またはリモートセッション Windows PowerShell から実行できます。</span><span class="sxs-lookup"><span data-stu-id="99a98-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="99a98-119">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="99a98-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-reset-the-global-external-access-policy"></a><span data-ttu-id="99a98-120">グローバル外部アクセスポリシーをリセットするには</span><span class="sxs-lookup"><span data-stu-id="99a98-120">To reset the global external access policy</span></span>

  - <span data-ttu-id="99a98-121">このコマンドは、グローバル外部アクセスポリシーをリセットします。</span><span class="sxs-lookup"><span data-stu-id="99a98-121">This command resets the global external access policy:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity "global"

</div>

<span data-ttu-id="99a98-122">詳細については、 [CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="99a98-122">For more information, see the help topic for the [Remove-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) cmdlet.</span></span>

<span data-ttu-id="99a98-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99a98-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

