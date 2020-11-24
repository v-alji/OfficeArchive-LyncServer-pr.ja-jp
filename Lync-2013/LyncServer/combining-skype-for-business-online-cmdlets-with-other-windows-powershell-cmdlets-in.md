---
title: Skype for Business Online のコマンドレットと他の Windows PowerShell コマンドレットの組み合わせ
description: Skype for Business Online のコマンドレットと他の Windows PowerShell コマンドレットの組み合わせ。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets
ms:assetid: 8bb8800a-f966-4570-8c8b-db87a91ad783
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362816(v=OCS.15)
ms:contentKeyID: 56558835
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bd18f60891d48a54eb2f77f189ea8417e0b5e93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398876"
---
# <a name="combining-skype-for-business-online-cmdlets-with-other-windows-powershell-cmdlets-in"></a><span data-ttu-id="98c7d-103">Skype for Business Online のコマンドレットと他の Windows PowerShell コマンドレットの組み合わせ</span><span class="sxs-lookup"><span data-stu-id="98c7d-103">Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets in</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98c7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98c7d-104">

<span> </span></span></span>

<span data-ttu-id="98c7d-105">_**最終更新日:** 2013-07-05_</span><span class="sxs-lookup"><span data-stu-id="98c7d-105">_**Topic Last Modified:** 2013-07-05_</span></span>

<span data-ttu-id="98c7d-106">Windows PowerShell を使用して Skype for Business Online に接続すると、約 40 Skype for Business Online のコマンドレットが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="98c7d-106">When you connect to Skype for Business Online by using Windows PowerShell, approximately 40 Skype for Business Online cmdlets will available for your use.</span></span> <span data-ttu-id="98c7d-107">ただし、Skype for Business Online を管理している場合は、これらの40コマンドレットのみを使用するように制限されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="98c7d-107">However, you are not limited to using just those 40 cmdlets when managing Skype for Business Online.</span></span> <span data-ttu-id="98c7d-108">Skype for Business Online のコマンドレットに加えて、コンピューターにインストールされている他の Windows PowerShell コマンドレットを使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="98c7d-108">In addition to the Skype for Business Online cmdlets, you can also use any other Windows PowerShell cmdlets that are installed on your computer.</span></span> <span data-ttu-id="98c7d-109">(Windows PowerShell 3.0 をインストールすると、数百種類の Windows PowerShell コマンドレットもインストールされます。)コマンドでは、Skype for Business Online のコマンドレットと、コンピューターで利用できるその他のコマンドレットを混在させることができます。</span><span class="sxs-lookup"><span data-stu-id="98c7d-109">(When you install Windows PowerShell 3.0, hundreds of core Windows PowerShell cmdlets are installed, as well.) Your commands can mix and match Skype for Business Online cmdlets and any other cmdlets available on your computer.</span></span>

<span data-ttu-id="98c7d-110">Windows PowerShell 3.0 の完全なコースはこの記事の範囲を超えていますが、コマンドレットを混在させて対応する理由を示すいくつかの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="98c7d-110">Although a complete course in Windows PowerShell 3.0 goes beyond the scope of this article, here are a few examples that show why you might want to mix and match cmdlets.</span></span> <span data-ttu-id="98c7d-111">まず、Skype for Business Online のコマンドレットには [印刷] コマンドが含まれていません。このコマンドは、Windows PowerShell コンソールでは見つかりません。</span><span class="sxs-lookup"><span data-stu-id="98c7d-111">First of all, none of the Skype for Business Online cmdlets include a Print command, and no such command can be found in the Windows PowerShell console, either.</span></span> <span data-ttu-id="98c7d-112">それでは、コマンドレットによって取得された情報の印刷イメージを取得するにはどうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="98c7d-112">So how do you get a printout of the information retrieved by a cmdlet?</span></span> <span data-ttu-id="98c7d-113">1つ目の方法は、情報を取得し、その情報を **Printer** コマンドレットに送信することです。</span><span class="sxs-lookup"><span data-stu-id="98c7d-113">One way is to retrieve the information, and then send that information to the **Out-Printer** cmdlet:</span></span>

    Get-CsTenant | Out-Printer

<span data-ttu-id="98c7d-114">追加のパラメーターは含まれていないため、 **Out-Printer** コマンドレットによって返されるすべての情報は、既定のプリンターに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="98c7d-114">Because no additional parameters are included, all the information returned by **the Out-Printer** cmdlet will be printed to the default printer.</span></span>

<span data-ttu-id="98c7d-115">同様に、Skype for Business Online のコマンドレットには、データをファイルに保存するためのパラメーターが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="98c7d-115">Likewise, none of the Skype for Business Online cmdlets include a parameter that allows you to save data to a file.</span></span> <span data-ttu-id="98c7d-116">ただし、このコマンドでは、**出力ファイル** コマンドレットを使って、返された情報をテキストファイル C: \\ LogsTenants.txt に保存します。 \\</span><span class="sxs-lookup"><span data-stu-id="98c7d-116">But that’s OK: this command uses the **Out-File** cmdlet to save the returned information to the text file C:\\Logs\\Tenants.txt:</span></span>

    Get-Tenant | Out-File -FilePath "C:\Logs\Tenants.txt"

<span data-ttu-id="98c7d-117">このコマンドは、 **オブジェクトの選択** コマンドレットを使って、画面に表示されるデータを制限します。</span><span class="sxs-lookup"><span data-stu-id="98c7d-117">And this command uses the **Select-Object** cmdlet to limit the data that is returned and displayed onscreen.</span></span> <span data-ttu-id="98c7d-118">この例では、 [ユーザーのアクセス](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) コマンドレットを使用して、すべての Skype For business Online ユーザーに関する情報を取得し、次に **Select-Object** コマンドレットを使用して、表示するデータをユーザーの id 値とそのアーカイブポリシーに制限します。</span><span class="sxs-lookup"><span data-stu-id="98c7d-118">In this example, the [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) cmdlet retrieves information for all of your Skype for Business Online users, and then the **Select-Object** cmdlet is used to limit the displayed data to the user’s Identity value and their archiving policy:</span></span>

    Get-CsOnlineUser | Select-Object Identity, ArchivingPolicy

<span data-ttu-id="98c7d-119">コンピューターで使用できるコマンドレットは100個あるため、どのコマンドレットが Skype for Business Online のコマンドレットであり、どのコマンドレットも含まれていないかを判断するのが困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="98c7d-119">Because there will be hundreds of cmdlets available for use on your computer, you might have difficulty determining which cmdlets are Skype for Business Online cmdlets and which ones are not.</span></span> <span data-ttu-id="98c7d-120">Skype for Business Online のコマンドレット (および Skype for Business Online のコマンドレットのみ) の一覧を返すには、まず、すべての Skype for Business Online コマンドレットが含まれている一時的な Windows PowerShell モジュールの名前を特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98c7d-120">To return a list of the Skype for Business Online cmdlets (and only Skype for Business Online cmdlets), you must first determine the name of the temporary Windows PowerShell module that contains all the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="98c7d-121">そのためには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="98c7d-121">To do that, run this command from the Windows PowerShell prompt:</span></span>

    Get-Module

<span data-ttu-id="98c7d-122">次のような情報が画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="98c7d-122">Information similar to the following will appear onscreen:</span></span>

    ModuleType Name                 ExportedCommands
    ---------- ----                 ----------------
    Manifest   Microsoft.PowerS...  {Add-Computer, Add-Content, A...}
    Script     tmp_5astd3uh.m5v     {Disable-CsMeetingRoom, Enabl...}

<span data-ttu-id="98c7d-123">ModuleType スクリプトを持つモジュールは、Skype for Business Online のコマンドレットを含むモジュールです。</span><span class="sxs-lookup"><span data-stu-id="98c7d-123">The module with the ModuleType Script is the module that contains the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="98c7d-124">これらのコマンドレットのリストを返すには、モジュール名としてスクリプトモジュールの名前を使用して、 **Command** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="98c7d-124">To return a list of those cmdlets, run the **Get-Command** cmdlet, using the name of the Script module as the module name:</span></span>

    Get-Command -Module tmp_5astd3uh.m5v

<span data-ttu-id="98c7d-125">ModuleType と Script との間に等しい複数のモジュールが存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="98c7d-125">It’s possible that you could have multiple modules with a ModuleType equal to Script.</span></span> <span data-ttu-id="98c7d-126">その場合は、次のコマンドを実行して、 **CsTenant** コマンドレットが含まれているモジュールを確認できます。</span><span class="sxs-lookup"><span data-stu-id="98c7d-126">In that case, you can run the following command to find out which module includes the **Get-CsTenant** cmdlet:</span></span>

    Get-Command Get-CsTenant

<span data-ttu-id="98c7d-127">**CsTenant** コマンドレットに対して返されるモジュールは、すべての Skype For business Online コマンドレットを含むモジュールになります。</span><span class="sxs-lookup"><span data-stu-id="98c7d-127">The module returned for the **Get-CsTenant** cmdlet will be the module containing all the Skype for Business Online cmdlets:</span></span>

    CommandType     Name                                               ModuleName
    -----------     ----                                               ----------
    Function        Get-CsTenant                                       tmp_5astd3uh.m5v

<div>

## <a name="see-also"></a><span data-ttu-id="98c7d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="98c7d-128">See Also</span></span>


<span data-ttu-id="98c7d-129">[Windows PowerShell と Skype for Business Online の概要](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="98c7d-129">[An introduction to Windows PowerShell and Skype for Business Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span></span>  
  

<span data-ttu-id="98c7d-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98c7d-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

