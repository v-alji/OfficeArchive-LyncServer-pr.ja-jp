---
title: 'Lync Server 2013: Windows PowerShell 3.0 のインストール'
description: 'Lync Server 2013: Windows PowerShell 3.0 をインストールしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Windows PowerShell 3.0
ms:assetid: d87bf21e-0a43-41cb-8fdc-626cedec8538
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205328(v=OCS.15)
ms:contentKeyID: 48185621
ms.date: 06/28/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4605231f4e73f6aada4fb34de895cdeb883d82b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426901"
---
# <a name="installing-windows-powershell-30-for-lync-server-2013"></a><span data-ttu-id="2d0e3-103">Lync Server 2013 用の Windows PowerShell 3.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="2d0e3-103">Installing Windows PowerShell 3.0 for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d0e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d0e3-104">

<span> </span></span></span>

<span data-ttu-id="2d0e3-105">_**最終更新日:** 2014-06-27_</span><span class="sxs-lookup"><span data-stu-id="2d0e3-105">_**Topic Last Modified:** 2014-06-27_</span></span>

<span data-ttu-id="2d0e3-106">Lync Server 2013 を正常に展開するには、Lync Server トポロジの一部である各コンピューターに Windows PowerShell 3.0 が必要です。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-106">To deploy Lync Server 2013 successfully, you’ll need Windows PowerShell 3.0 on each computer that’s part of your Lync Server topology.</span></span>

<span data-ttu-id="2d0e3-107">Windows Server 2012 または Windows Server 2012 R2 を実行しているシステムでは、何もする必要はありません。また、これらのオペレーティングシステムに PowerShell 3.0 が含まれているため、次の展開の段階に進むことができます。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-107">Now, for systems running Windows Server 2012 or Windows Server 2012 R2, you don’t need to do anything here, and can go ahead to the next stage of deployment, because PowerShell 3.0 is included with those operating systems.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2d0e3-108">ただし、Windows Server 2008 R2 SP1 を実行しているシステムの場合は、Lync Server 2013 をインストールする前に PowerShell 3.0 を前提条件としてインストールする必要があります。そうしないと、動作しません。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-108">But for systems running Windows Server 2008 R2 SP1, you’ll need to install PowerShell 3.0 as a prerequisite before you install Lync Server 2013, or things won’t work.</span></span> <span data-ttu-id="2d0e3-109">PowerShell 3.0 をインストールするには、「 <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3.0</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-109">To install PowerShell 3.0, see <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3.0</A>.</span></span> <span data-ttu-id="2d0e3-110">これは、PowerShell 3.0 ダウンロードページへの直接リンクであり、正常にインストールされることに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-110">This is a direct link to the PowerShell 3.0 download page, along with information relating to installing it successfully.</span></span>



</div>

<span data-ttu-id="2d0e3-111">インストールが完了したら、または確認して、Lync Server の展開を続行する前に確認してください。次のような場合は、PowerShell 3.0 がサーバーにインストールされていることを確認することが簡単です。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-111">Once you’ve done the install, or if you just want to check and be sure before continuing with the Lync Server deployment, confirming that PowerShell 3.0 is on a server is pretty straightforward if you do this:</span></span>

1.  <span data-ttu-id="2d0e3-112">確認するサーバーで、[ **スタート**]、[すべての **プログラム**]、[ **アクセサリ**]、[ **windows powershell**] の順にクリックして、[ **windows powershell**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-112">On the server you want to check, choose **Start**, click **All Programs**, click **Accessories**, click **Windows PowerShell**, and then click **Windows PowerShell**.</span></span>

2.  <span data-ttu-id="2d0e3-113">Windows PowerShell コンソールで、コマンドプロンプトで次のコマンドを入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-113">In the Windows PowerShell console, type the following command at the command prompt, and then press ENTER:</span></span>
    
        Get-Host | Select-Object Version

3.  <span data-ttu-id="2d0e3-114">Windows PowerShell 3.0 がインストールされている場合は、次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d0e3-114">If Windows PowerShell 3.0 is installed you’ll see output that looks like this:</span></span>
    
        Version
        -------
        3.0

<span data-ttu-id="2d0e3-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d0e3-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

