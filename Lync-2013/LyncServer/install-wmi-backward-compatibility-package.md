---
title: WMI の下位互換性パッケージをインストールする
description: WMI の下位互換性パッケージをインストールします。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439586"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="972e6-103">WMI の下位互換性パッケージをインストールする</span><span class="sxs-lookup"><span data-stu-id="972e6-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="972e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="972e6-104">

<span> </span></span></span>

<span data-ttu-id="972e6-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="972e6-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="972e6-106">WMI 下位互換性パッケージをインストールせずに、トポロジビルダーのマージウィザードを実行しようとすると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="972e6-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="972e6-107">![WMI エラーメッセージ](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI エラーメッセージ")</span><span class="sxs-lookup"><span data-stu-id="972e6-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="972e6-108">WMI の下位互換性パッケージをインストールせずに **CsLegacytopology** コマンドレットを実行しようとすると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="972e6-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="972e6-109">![Windows PowerShell WMI プロバイダーエラー](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI プロバイダーエラー")</span><span class="sxs-lookup"><span data-stu-id="972e6-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="972e6-110">WMI 下位互換性パッケージをインストールするには</span><span class="sxs-lookup"><span data-stu-id="972e6-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="972e6-111">インストールメディアから、 \\ セットアップ \\OCSWMIBC.MSI AMD64 セットアップに \\ 移動 \\ します。</span><span class="sxs-lookup"><span data-stu-id="972e6-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="972e6-112">OCSWMIBC.MSI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="972e6-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="972e6-113">トポロジビルダーの結合ウィザードが実行されているコンピューターに OCSWMIBC.msi がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="972e6-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="972e6-114">ただし、トポロジ内のすべてのフロントエンドサーバーに OCSWMIBC.msi をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="972e6-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="972e6-115">OCSWMIBC.msi は、Lync Server 2013 コアコンポーネントと Lync Server 2013 Management Shell がインストールされていて、Office Communications Server 2007 R2 トポロジ (WMI プロバイダーから Active Directory Domain Services (AD DS) と SQL Server) にアクセスできる、ドメイン内の任意のコンピューターにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="972e6-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="972e6-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="972e6-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

