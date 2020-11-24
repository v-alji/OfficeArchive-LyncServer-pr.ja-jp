---
title: 'Lync Server 2013: 一般的なエリア電話の連絡先オブジェクトを削除する'
description: 'Lync Server 2013: 一般的なエリア電話の連絡先オブジェクトを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a common area phone Contact object
ms:assetid: f4c139dc-f07c-4c75-9345-e291aea41173
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994087(v=OCS.15)
ms:contentKeyID: 51803999
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e918f7a46269f70577f28b2c3e55297959430721
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399872"
---
# <a name="delete-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="6f463-103">Lync Server 2013 で一般的なエリア電話の連絡先オブジェクトを削除する</span><span class="sxs-lookup"><span data-stu-id="6f463-103">Delete a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f463-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f463-104">

<span> </span></span></span>

<span data-ttu-id="6f463-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="6f463-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="6f463-106">一般的な市外局番に関連付けられた連絡先オブジェクトを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="6f463-106">You might want to delete the contact object associated with a common area phone.</span></span> <span data-ttu-id="6f463-107">たとえば、従業員 lounge から電話を削除した場合、その電話に連絡先オブジェクトを関連付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6f463-107">For example, if you remove the phone from an employee lounge, there’s no need to have a contact object associated with that phone.</span></span> <span data-ttu-id="6f463-108">**CsCommonAreaPhone** コマンドレットを使用すると、一般的な市外局番のアカウントを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="6f463-108">The **Remove-CsCommonAreaPhone** cmdlet provides a way for you to delete common area phone accounts.</span></span> <span data-ttu-id="6f463-109">このコマンドレットを実行すると、 **CsCommonAreaPhone** によって返される一般的なエリアの携帯電話の一覧から電話が削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f463-109">When you run this cmdlet, the phone is deleted from the list of common area phones returned by **Get-CsCommonAreaPhone**.</span></span> <span data-ttu-id="6f463-110">さらに、その電話に関連付けられている連絡先オブジェクトが Active Directory ドメインサービスから削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f463-110">In addition, the contact object associated with that phone is deleted from Active Directory Domain Services.</span></span>

<span data-ttu-id="6f463-111">共通の市外局番を1つ、または、表示名や国番号、市外局番などの共通の市外局番を持つ携帯電話のいずれかを削除するには、 **CsCommonAreaPhone** を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f463-111">Use **Remove-CsCommonAreaPhone** to remove one common area phone or all common area phones that have a common element, such as a display name or country and area code.</span></span> <span data-ttu-id="6f463-112">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f463-112">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="6f463-113">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f463-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="removing-a-specified-common-area-phone"></a><span data-ttu-id="6f463-114">指定した共通の市外局番を削除する</span><span class="sxs-lookup"><span data-stu-id="6f463-114">Removing a Specified Common Area Phone</span></span>

  - <span data-ttu-id="6f463-115">次のコマンドは、SIP アドレス sip:mainlobby@litwareinc.com を持つ一般的なエリアの電話を削除します。</span><span class="sxs-lookup"><span data-stu-id="6f463-115">The following command removes the common area phone with the SIP address sip:mainlobby@litwareinc.com:</span></span>
    
        Remove-CsCommonAreaPhone -Identity "sip:mainlobby@litwareinc.com"

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-display-name"></a><span data-ttu-id="6f463-116">表示名に基づいて一般的なエリア電話を削除する</span><span class="sxs-lookup"><span data-stu-id="6f463-116">Removing Common Area Phones Based on Their Display Name</span></span>

  - <span data-ttu-id="6f463-117">このコマンドは、表示名に "建物 14" という文字列値が含まれているすべての共通領域の電話を削除します。</span><span class="sxs-lookup"><span data-stu-id="6f463-117">This command removes all the common area phones where the display name includes the string value "Building 14":</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.DisplayName -match "Building 14"} | Remove-CsCommonAreaPhone

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-country-and-area-codes"></a><span data-ttu-id="6f463-118">国と市外局番に基づいて一般的なエリア電話を削除する</span><span class="sxs-lookup"><span data-stu-id="6f463-118">Removing Common Area Phones Based on Their Country and Area Codes</span></span>

  - <span data-ttu-id="6f463-119">このコマンドを実行すると、米国 (国コード 1) と市外局番425の一般的な市外局番がすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f463-119">This command removes all the common area phones for the United States (country code 1) and the area code 425:</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.LineUri  -match "^tel:\+1425"} | Remove-CsCommonAreaPhone

</div>

<span data-ttu-id="6f463-120">詳細については、 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f463-120">For details, see the Help topic for the [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f463-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f463-121">See Also</span></span>


[<span data-ttu-id="6f463-122">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="6f463-122">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="6f463-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f463-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

