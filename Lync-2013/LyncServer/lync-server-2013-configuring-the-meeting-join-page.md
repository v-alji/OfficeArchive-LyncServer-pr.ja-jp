---
title: 'Lync Server 2013: 会議参加ページの構成'
description: 'Lync Server 2013: 会議の参加ページを構成する'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the meeting join page
ms:assetid: 45880423-47f4-49af-b825-cbd8e3fc1046
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204861(v=OCS.15)
ms:contentKeyID: 48184037
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e7c9dde0fdb6829da7bd11e16261a4bd76b7554
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432535"
---
# <a name="configuring-the-meeting-join-page-in-lync-server-2013"></a><span data-ttu-id="f3d63-103">Lync Server 2013 での会議参加ページの構成</span><span class="sxs-lookup"><span data-stu-id="f3d63-103">Configuring the meeting join page in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3d63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3d63-104">

<span> </span></span></span>

<span data-ttu-id="f3d63-105">_**最終更新日:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="f3d63-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="f3d63-106">ユーザーが会議出席依頼の会議リンクをクリックすると、[会議の参加] ページによって、ユーザーのコンピューターに Lync 2013 クライアントが既にインストールされているかどうかが検出されます。</span><span class="sxs-lookup"><span data-stu-id="f3d63-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="f3d63-107">クライアントが既にインストールされている場合は、クライアントが開き、会議に参加します。</span><span class="sxs-lookup"><span data-stu-id="f3d63-107">If a client is already installed, the client opens and joins the meeting.</span></span> <span data-ttu-id="f3d63-108">クライアントがインストールされていない場合、既定では、2013バージョンの Lync Web App が開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d63-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="f3d63-109">ユーザーが Office Communicator 2007 R2 または Lync 2010 アテンダントを使って会議に参加できるようにする場合は、[会議参加] ページの動作を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="f3d63-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="f3d63-110">これらの構成オプションは、Lync Server 2013 コントロールパネルから削除されていますが、Set-CsWebServiceConfiguration コマンドレットを使用して構成します。</span><span class="sxs-lookup"><span data-stu-id="f3d63-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the Set-CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-set-cswebserviceconfiguration-parameters"></a><span data-ttu-id="f3d63-111">Set-CsWebServiceConfiguration パラメーターの会議参加ページ</span><span class="sxs-lookup"><span data-stu-id="f3d63-111">Meeting Join Page Set-CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3d63-112">Set-CsWebServiceConfiguration パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3d63-112">Set-CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="f3d63-113">説明</span><span class="sxs-lookup"><span data-stu-id="f3d63-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3d63-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="f3d63-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="f3d63-115">True に設定すると、Lync 以外のクライアントアプリケーションを使用して会議に参加するユーザーには、Office Communicator 2007 R2 を使用して会議に参加する機会が与えられます。</span><span class="sxs-lookup"><span data-stu-id="f3d63-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="f3d63-116">既定値は False です。</span><span class="sxs-lookup"><span data-stu-id="f3d63-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3d63-117">Showalternatejoinoptionている</span><span class="sxs-lookup"><span data-stu-id="f3d63-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="f3d63-118">True に設定すると、オンライン会議に参加するための代替オプション (Office Communicator 2007 R2 など) が自動的に展開され、ユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3d63-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="f3d63-119">False (既定値) に設定した場合、これらのオプションは使用できますが、ユーザーは自分のオプションの一覧を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d63-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="f3d63-120">Lync Server 2013 管理シェルを使用して会議の参加ページを構成するには</span><span class="sxs-lookup"><span data-stu-id="f3d63-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="f3d63-121">Lync Server 2013 管理シェルを起動します。 [ **スタート**]、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d63-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f3d63-122">Web サービスの構成設定を表示するには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="f3d63-122">To view the web service configuration settings, run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration

3.  <span data-ttu-id="f3d63-123">次のコマンドを実行します。設定に応じてパラメーターが True または False に設定されています (このコマンドレットのパラメーターの詳細については、Lync Server 2013 管理シェルドキュメントの「 [set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) 」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f3d63-123">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) in the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f3d63-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3d63-124">See Also</span></span>


[<span data-ttu-id="f3d63-125">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3d63-125">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="f3d63-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3d63-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

