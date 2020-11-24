---
title: 'Lync Server 2013: Outlook の有効化リストを更新する'
description: 'Lync Server 2013: Outlook の有効化リストを更新しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399471"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a><span data-ttu-id="3d0e9-103">Lync Server 2013 の Outlook 有効化リストを更新する</span><span class="sxs-lookup"><span data-stu-id="3d0e9-103">Updating the Outlook enable list in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d0e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d0e9-104">

<span> </span></span></span>

<span data-ttu-id="3d0e9-105">_**最終更新日:** 2013-01-07_</span><span class="sxs-lookup"><span data-stu-id="3d0e9-105">_**Topic Last Modified:** 2013-01-07_</span></span>

<span data-ttu-id="3d0e9-106">Microsoft Lync 2013 用のオンライン会議アドインは、Outlook のアドイン管理リストに含めるポリシーを作成することによって、ユーザーが常に有効にしていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-106">You can ensure that Online Meeting Add-in for Microsoft Lync 2013 always remains enabled for users by creating a policy that includes it in the Add-in Management List for Outlook.</span></span> <span data-ttu-id="3d0e9-107">アドイン管理リストポリシーは、グループポリシー管理コンソールの Office 管理用テンプレートファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-107">The Add-in Management List policy is included in the Office administrative template files for the Group Policy Management Console.</span></span> <span data-ttu-id="3d0e9-108">[HKCU Software ポリシー] の下に、レジストリキーが作成さ \\ \\ \\ \\ \\ \\ れます。 Microsoft Office 15.0 Outlook15 \\ 弾力性 \\ AddinList。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-108">It creates a registry key under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList.</span></span> <span data-ttu-id="3d0e9-109">このキーに ucaddin.dll の値を追加して、常に有効にし、ユーザーが手動で無効にすることができないように ucaddin.dll 値を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-109">You can add a value for the ucaddin.dll to this key, and configure the ucaddin.dll value so that it is always enabled and so that users cannot manually disable it</span></span>

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a><span data-ttu-id="3d0e9-110">Outlook アドインの一覧に ucaddin.dll を追加するには</span><span class="sxs-lookup"><span data-stu-id="3d0e9-110">To Add ucaddin.dll to the Outlook Add-in List</span></span>

  - <span data-ttu-id="3d0e9-111">AddinList レジストリキーに、[HKCU \\ Software \\ ポリシー \\ Microsoft \\ Office \\ 15.0 \\ Outlook15 弾力性 AddinList] にある \\ \\ 次の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-111">To the AddinList registry key, located under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList, add the following value:</span></span>
    
      - <span data-ttu-id="3d0e9-112">レジストリの種類 = REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3d0e9-112">Registry Type = REG\_SZ</span></span>
    
      - <span data-ttu-id="3d0e9-113">Name = ucaddin.dll</span><span class="sxs-lookup"><span data-stu-id="3d0e9-113">Name = ucaddin.dll</span></span>
    
      - <span data-ttu-id="3d0e9-114">値 = 1 (アドインを常に有効にし、エンドユーザーが管理できないことを指定します)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-114">Value = 1 (specifies that the add-in is always enabled and cannot be managed by the end user)</span></span>

<span data-ttu-id="3d0e9-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d0e9-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

