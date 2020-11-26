---
title: 承認されたホストエントリを削除する
description: 承認されたホストエントリを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443259"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="a0266-103">承認されたホストエントリを削除する</span><span class="sxs-lookup"><span data-stu-id="a0266-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0266-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0266-104">

<span> </span></span></span>

<span data-ttu-id="a0266-105">_**最終更新日:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="a0266-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="a0266-106">このトピックでは、従来の承認済みホストエントリ (Lync Server 2013 の *信頼済みアプリケーションエントリ* と呼ばれます) を削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a0266-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="a0266-107">リモート通話コントロールを Lync Server 2013 の展開に移行する場合、Office Communications Server 2007 R2 の展開で、すべての SIP/CSTA ゲートウェイの既存の承認済みホストエントリを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0266-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="a0266-108">既存の承認済みホストのエントリを削除するには、Office Communications Server 2007 R2 に含まれている管理ツールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0266-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="a0266-109">Office Communications Server 2007 R2 の展開で承認されているホストエントリを削除するには</span><span class="sxs-lookup"><span data-stu-id="a0266-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="a0266-110">Office Communications Server 2007 R2 管理コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="a0266-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="a0266-111">ツリーを展開し、承認済みホストが作成されたプールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="a0266-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="a0266-112">[ **プロパティ**] をクリックし、[ **フロントエンドプロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0266-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="a0266-113">[ **Host Authorization** ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0266-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="a0266-114">サーバーを選択し、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0266-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="a0266-115">[ **プロパティ**] で [ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0266-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="a0266-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0266-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

